---
title: Hantera lagring genom att ta bort dokument eller komprimera data
description: Lär dig att hantera historiska dokument (och minska mängden data som lagras i en databas) genom att ta bort eller komprimera dem.
author: edupont04
ms.topic: conceptual
ms.search.form: 107, 9040
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: a5c79da88ec49f6d9ff763b6712b0777158d2805
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147917"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Hantera lagring genom att ta bort dokument eller komprimera data

En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.  

> [!TIP]
> Information om andra sätt att minska mängden data som lagras i en databas finns i [Minska mängden data som lagras i Business Central-databaser](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i vår dokumentation för utvecklare och IT-proffs.

## <a name="delete-documents"></a>Ta bort dokument

I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder som inte raderats. I [!INCLUDE[prod_short](includes/prod_short.md)] kontrolleras att borttagna inköpsorder har fakturerats helt. Du kan inte ta bort order som inte har fakturerats och inlevererats helt.  

Returorder tas vanligtvis bort när de har fakturerats. När du bokför en faktura överförs den till sidan **Bokförd inköpskreditnota**. Om du har markerat kryssrutan **Returutleverans i kreditnota** på sidan **Inköpsinställningar** överförs fakturan till sidan **Bokförd returutleverans**. Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**. Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.  

Avropsorder tas inte bort när du har behandlat och fakturerat alla relaterade inköpsorder. Du kan ta bort avropsorder med batch-jobbet **Ta bort fakturerade avropsorder**.  

Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt. När en faktura bokförs skapas en motsvarande transaktion på sidan **Bokförda servicefakturor**. Det bokförda dokumentet kan visas från sidan **Bokförd servicefaktura**.  

Tjänsteordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från sidan **Servicefaktura**, gäller följande. Då kan du behöva ta bort fakturerade order som inte har tagits bort. Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.  

## <a name="compress-data-with-date-compression"></a>Komprimera data med datumkomprimering

Du kan komprimera data i [!INCLUDE [prod_short](includes/prod_short.md)] för att spara utrymme i databasen, som i [!INCLUDE [prod_short](includes/prod_short.md)] online kan spara pengar. Komprimeringen baseras på datum och fungerar genom att flera gamla transaktioner kombineras till en ny. 

Du kan komprimera poster på följande villkor:

* De gäller stängda räkenskapsår
* Fältet **Öppen** ställs in på **Nej**. 
* De är minst fem år gamla. Om du vill komprimera data som är mindre än fem år ska du kontakta din Microsoft-partner.

Leverantörsreskontratransaktioner från föregående räkenskapsår kan exempelvis komprimeras så att endast en kredittransaktion och en debettransaktion skapas per konto och månad. Den nya transaktionens belopp är summan av alla komprimerade transaktioner. Det datum som tilldelas är det första datumet i perioden som komprimerats, t. ex. den första dagen i månaden (om transaktionerna är komprimerade per månad). När komprimeringen är utförd kan du fortfarande se nettoförändringen för respektive konto under föregående räkenskapsår.

Antalet transaktioner som skapas från en datumkomprimering beror på hur många filter du definierar, vilka fält som kombineras och hur lång period du väljer. Det kommer alltid att skapas åtminstone en transaktion. När batch-jobbet har slutförts visas resultatet på sidan **Datumkomprimeringsjournaler**.

Du kan komprimera följande typer av data med hjälp av batch-jobb. Det finns ett batchjobb för varje typ av data.

* Banktransaktioner – redovisningstransaktioner, momstransaktioner, bankkontotransaktioner, redovisningsbudgettransaktioner, kundreskontratransaktioner, leverantörsreskontratransaktioner.
* Dist.lagertransaktioner 
* Resurstransaktioner
* Artikelbudgettransaktioner
* Anläggningstillgång – Anl. transaktioner, Anl. underhållstransaktioner, Anl. försäkringstransaktioner.

När du definierar kriterier för komprimeringen kan du använda alternativen under **Behåll fältinnehåll** för att behålla innehållet i vissa fält. Vilka fält som är tillgängliga beror på vilka data du komprimerar.

> [!NOTE]
> Innan du kan köra datumkomprimeringen måste analysvyer vara aktuella. Mer information finns i [så här uppdaterar du en analysvy](bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Efter komprimeringen behålls alltid innehållet i följande fält: **Bokföringsdatum**, **Leverantörsnr**, **Dokumenttyp**, **Valutakod**, **Bokföringsmall**, **Belopp**, **Återstående belopp**, **Originalbelopp (BVA)**, **Återstående belopp (BVA)**, **Belopp (BVA)**, **Inköp (BVA)**, **Fakturarabatt (BVA)**, **Givet kassarabattbelopp (BVA)** och **Möjlig kassarabatt**.

## <a name="posting-compressed-entries"></a>Bokför komprimerade poster
Komprimerade transaktioner bokförs något annorlunda än standardbokföring. Detta är att minska antalet nya redovisningstransaktioner som skapas av datumkomprimering och är särskilt viktigt när du behåller information som dimensioner och dokumentnummer. Datumkomprimering skapar nya poster enligt följande:
* På sidan **Redovisningstransaktioner** skapas nya transaktioner med nya transaktionsnummer för de komprimerade transaktionerna. Fältet **Beskrivning** innehåller **Komprimeringsdatum** så att de komprimerade transaktionerna är lätta att identifiera. 
* På redovisningssidor, till exempel **Kundreskontratransaktioner**, skapas en eller flera transaktioner med nya transaktionsnummer. 

Bokföringsprocessen skapar luckor i nummerserien för transaktioner på sidan **Redovisningstransaktioner**. Dessa nummer tilldelas endast transaktionerna på redovisningssidorna. Det nummerintervall som har tilldelats transaktionerna finns på sidan **Bokförd redovisningsjournal** i fälten **Från transaktion nr.** och **Till transaktrionsnr.**. 

> [!NOTE]
> När du har kört datumkomprimeringen är alla konton i redovisningen låsta. Du kan till exempel inte koppla leverantörs- eller bankredovisningstransaktioner för några konton under den period för vilken datumen komprimeras.

Antalet transaktioner som skapas från en datumkomprimering beror på hur många filter du definierar, vilka fält som kombineras och hur lång period du väljer. Det kommer alltid att skapas åtminstone en transaktion. 

> [!WARNING]
> Datumkomprimeringen raderar poster. Därför ska du alltid ta en säkerhetskopia av databasen innan du kör batch-jobbet.

### <a name="to-run-a-date-compression"></a>För att köra en datakomprimering
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Dataadministration** och välj sedan relaterad länk.
2. Gör något av följande:
    * Om du vill använda en assisterad installationshandbok för att ställa in datum komprimering för en eller flera typer av data väljer du **Guide för dataadministration**.
    * Om du vill ställa in komprimering för en enskild typ av data väljer du **datumkomprimering** , **komprimeringstransaktioner** och väljer sedan de data som ska komprimeras.

   > [!NOTE]
   > Du kan bara komprimera data som är äldre än fem år. Om du vill komprimera data som är mindre än fem år ska du kontakta din Microsoft-partner.

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Hantera lagring genom att ta bort dokument eller komprimera data
description: Lär dig att hantera historiska dokument (och minska mängden data som lagras i en databas) genom att ta bort eller komprimera dem.
author: edupont04
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: edupont
---
# Hantera lagring genom att ta bort dokument eller komprimera data

En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.  

> [!TIP]
> Lär dig mer om andra sätt att minska mängden data som lagras i en databas genom att läsa [Minska mängden data som lagras i Business Central-databaser](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i vår dokumentation för utvecklare och IT-proffs.

## Ta bort dokument

I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder. Du kan emellertid inte ta bort dem om du inte helt har fakturerat och tagit emot artiklarna på inköpsordern. [!INCLUDE[prod_short](includes/prod_short.md)] hjälper dig att söka efter det.

Returorder tas vanligtvis bort när de har fakturerats. När du bokför en faktura överförs den till sidan **Bokförd inköpskreditnota**. Om du har markerat kryssrutan **Returutleverans i kreditnota** på sidan **Inköpsinställningar** överförs fakturan till sidan **Bokförd returutleverans**. Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**. Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.  

Avropsorder tas inte bort automatiskt när du har behandlat och fakturerat alla relaterade inköpsorder. Istället kan du ta bort dem med batch-jobbet **Ta bort fakturerade avropsorder**.  

Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt. När en faktura bokförs skapas en motsvarande transaktion som sedan kan visas på sidan **Bokförda servicefakturor**.  

Serviceorder tas inte bort automatiskt, om det totala antalet i ordern har bokförts från sidan **Servicefaktura** istället för från själva serviceordern. Du kan behöva ta bort sådana fakturerade order manuellt genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.  

## Komprimera data med datumkomprimering

Du kan komprimera data i [!INCLUDE [prod_short](includes/prod_short.md)] för att spara i databasen&mdash;vilket i [!INCLUDE [prod_short](includes/prod_short.md)] online till och med kan spara pengar. Komprimeringen, baseras på datum och funktioner, kombinerar flera gamla transaktioner till en ny.

Du kan komprimera poster som uppfyller alla följande villkor:

* De gäller stängda räkenskapsår.
* Fältet **Öppen** ställs in på **Nej**.
* De är minst fem år gamla. Om du vill komprimera data som är mindre än fem år ska du kontakta din Microsoft-partner.

Leverantörsreskontratransaktioner från föregående räkenskapsår kan exempelvis komprimeras så att endast en kredittransaktion och en debettransaktion skapas per konto och månad. Den nya transaktionens belopp är summan av alla komprimerade transaktioner. Det datum som tilldelas är det första datumet i perioden som komprimerats, t.ex. den första dagen i månaden (om transaktionerna är komprimerade per månad). När komprimeringen är utförd kan du fortfarande se nettoförändringen för respektive konto under föregående räkenskapsår.

Antalet transaktioner som skapas från en datumkomprimering beror på hur många filter du definierar, vilka fält som kombineras och hur lång period du väljer. Det finns alltid minst en transaktion. När batch-jobbet har slutförts visas resultatet på sidan **Datumkomprimeringsjournaler**.

Du kan komprimera följande typer av data med hjälp av batch-jobb.

* Banktransaktioner – redovisningstransaktioner, momstransaktioner, bankkontotransaktioner, redovisningsbudgettransaktioner, kundreskontratransaktioner och leverantörsreskontratransaktioner.
* Dist.lagertransaktioner
* Resurstransaktioner
* Artikelbudgettransaktioner
* Anläggningstillgång – Anl. transaktioner, Anl. underhållstransaktioner och Anl. försäkringstransaktioner.

När du definierar kriterier för komprimeringen kan du behålla innehållet för vissa fält med hjälp av alternativen under **Behåll fältinnehåll**. Vilka fält som är tillgängliga beror på vilka data du komprimerar.

> [!NOTE]
> Innan du kan köra datumkomprimeringen måste analysvyer vara aktuella. Läs mer i avsnittet [Uppdatera en analysvy](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Efter komprimeringen behålls alltid innehållet i följande fält: **Bokföringsdatum**, **Leverantörsnr**, **Dokumenttyp**, **Valutakod**, **Bokföringsmall**, **Belopp**, **Återstående belopp**, **Originalbelopp (BVA)**, **Återstående belopp (BVA)**, **Belopp (BVA)**, **Inköp (BVA)**, **Fakturarabatt (BVA)**, **Givet kassarabattbelopp (BVA)** och **Möjlig kassarabatt**.

## Bokför komprimerade poster

Komprimerade transaktioner bokförs något annorlunda än standardbokföring. Detta är att minska antalet nya redovisningstransaktioner som skapas av datumkomprimering och är särskilt viktigt när du behåller information som dimensioner och dokumentnummer. Datumkomprimering skapar nya poster enligt följande:

* På sidan **Redovisningstransaktioner** skapas nya transaktioner för de komprimerade transaktionerna. Fältet **Beskrivning** innehåller **Komprimeringsdatum** så att de komprimerade transaktionerna är lätta att identifiera. 
* På redovisningssidor, till exempel **Kundreskontratransaktioner**, skapas en eller flera nya transaktioner. 

Bokföringsprocessen skapar luckor i nummerserien för transaktioner på sidan **Redovisningstransaktioner**. Dessa nummer tilldelas endast transaktionerna på redovisningssidorna. Det nummerintervall som har tilldelats transaktionerna finns på sidan **Bokförd redovisningsjournal** i fälten **Från transaktion nr.** och **Till transaktrionsnr.**. 

> [!NOTE]
> När du har kört datumkomprimeringen är alla konton i redovisningen låsta. Det innebär till exempel att du inte kan återföra leverantörs- eller bankredovisningstransaktioner för några konton som påverkades av komprimeringen.

Antalet transaktioner som skapas från en datumkomprimering beror på hur många filter du definierar, vilka fält som kombineras och hur lång period du väljer. Det kommer alltid att skapas åtminstone en transaktion.

> [!WARNING]
> Datumkomprimeringen raderar poster. Därför ska du alltid ta en säkerhetskopia av databasen innan du kör batch-jobbet.

### För att köra en datakomprimering

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Dataadministration** och välj sedan relaterad länk.
2. Gör något av följande:
    * Om du vill använda en assisterad guide för att ställa in datumkomprimering för en eller flera typer av data väljer du **Guide för dataadministration**.
    * Om du vill ställa in komprimering för en enskild typ av data väljer du **Datakomprimering** , **Komprimeringstransaktioner** och väljer sedan de data som ska komprimeras.

   > [!NOTE]
   > Du kan bara komprimera data som är äldre än fem år. Om du vill komprimera data som är mindre än fem år ska du kontakta din Microsoft-partner.

## Se även

[Administration](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

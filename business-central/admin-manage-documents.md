---
title: Hantera lagring genom att ta bort dokument eller komprimera data
description: Lär dig hur du kan behålla historiska data genom att komprimera bokföringsposter eller hur du tar bort den.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f0d713f57345c312ddbfe6b5462f2623b1088dfc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753873"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Hantera lagring genom att ta bort dokument eller komprimera data

En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.  

> [!TIP]
> Information om andra sätt att minska mängden data som lagras i en databas finns i [Minska mängden data som lagras i Business Central-databaser](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i hjälpen för utvecklare och IT-proffs.

## <a name="delete-documents"></a>Ta bort dokument

I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder som inte raderats. I [!INCLUDE[prod_short](includes/prod_short.md)] kontrolleras att borttagna inköpsorder har fakturerats helt. Du kan inte ta bort order som inte har fakturerats och inlevererats helt.  

Returorder tas vanligtvis bort när de har fakturerats. När du bokför en faktura överförs den till sidan **Bokförd inköpskreditnota**. Om du har markerat kryssrutan **Returutleverans i kreditnota** på sidan **Inköpsinställningar** överförs fakturan till sidan **Bokförd returutleverans**. Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**. Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.  

Avropsorder tas inte bort när du har behandlat och fakturerat alla relaterade inköpsorder. Du kan ta bort avropsorder med batch-jobbet **Ta bort fakturerade avropsorder**.  

Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt. När en faktura bokförs skapas en motsvarande transaktion på sidan **Bokförda servicefakturor**. Det bokförda dokumentet kan visas från sidan **Bokförd servicefaktura**.  

Tjänsteordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från sidan **Servicefaktura**, gäller följande. Då kan du behöva ta bort fakturerade order som inte har tagits bort. Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.  

## <a name="compress-data-with-date-compression"></a>Komprimera data med datumkomprimering

Du kan komprimera data i [!INCLUDE [prod_short](includes/prod_short.md)] så att du sparar utrymme i databasen, som i [!INCLUDE [prod_short](includes/prod_short.md)] online kan spara pengar. Komprimeringen baseras på datum och fungerar genom att flera gamla transaktioner kombineras till en ny. Du kan bara komprimera transaktioner som tillhör avslutade räkenskapsår och leverantörsreskontratransaktioner där fältet **Öppen** är inställt på *Nej*.  

Leverantörsreskontratransaktioner från föregående räkenskapsår kan exempelvis komprimeras så att endast en kredittransaktion och en debettransaktion skapas per konto och månad. Den nya transaktionens belopp är summan av alla komprimerade transaktioner. Det datum som tilldelas är det första datumet i perioden som komprimerats, t.ex. den första dagen i månaden (om transaktionerna är komprimerade per månad). När komprimeringen är utförd kan du fortfarande se nettoförändringen för respektive konto under föregående räkenskapsår.

Antalet transaktioner som skapas från en datumkomprimering beror på hur många filter du definierar, vilka fält som kombineras och hur lång period du väljer. Det kommer alltid att skapas åtminstone en transaktion. När batch-jobbet har slutförts visas resultatet på sidan **Datumkomprimeringsjournaler**.

Du kan komprimera följande typer av data i [!INCLUDE [prod_short](includes/prod_short.md)] med hjälp av batch-jobb:

* Bankkontotransaktioner

  Efter komprimeringen med funktionen **Bibehåll fältinnehåll** kan du behålla innehållet i fälten **Dokumentnr, vår kontakt**, **Global dimension 1 kod** och **Global dimension 2 kod**.
* Lev.reskontratransaktioner

  Efter komprimeringen behålls alltid innehållet i följande fält: **Bokföringsdatum**, **Leverantörsnr**, **Dokumenttyp**, **Valutakod**, **Bokföringsmall**, **Belopp**, **Återstående belopp**, **Originalbelopp (BVA)**, **Återstående belopp (BVA)**, **Belopp (BVA)**, **Inköp (BVA)**, **Fakturarabatt (BVA)**, **Givet kassarabattbelopp (BVA)** och **Möjlig kassarabatt**.

  Med funktionen **Bibehåll fältinnehåll** kan du också bibehålla innehållet i följande fält: **Dokumentnr**, **Inköpsleverantörsnr**, **Inköparkod**, **Global dimension 1 kod** och **Global dimension 2 kod**.

> [!NOTE]
> När du har kört datumkomprimeringen är alla konton i redovisningen låsta. Du kan till exempel inte koppla leverantörs- eller bankredovisningstransaktioner för några konton under den period för vilken datumen komprimeras.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Antalet transaktioner som skapas från ett batch-jobb för datumkomprimering beror på hur många filter du definierar, vilka fält som kombineras och hur lång period du väljer. Det kommer alltid att skapas åtminstone en transaktion. 

> [!WARNING]
> Datumkomprimeringen tar bort transaktioner. Därför ska du alltid ta en säkerhetskopia av databasen innan du kör batch-jobbet.

I följande tabell visas de fält på snabbfliken **Alternativ** som är tillgängliga för alla batch-jobb. Avsnittet **Bibehåll fältinnehåll** innehåller ytterligare fält som beskrivs ovan.

|Fält  |Beskrivning  |
|-------|-------------|
|Startdatum     |Ange det första datum som ska ingå i datumkomprimeringen. Komprimeringen kommer att påverka alla transaktioner fr.o.m. det här datumet t.o.m. datumet i fältet Slutdatum.|
|Slutdatum     |Skriv in det sista datumet som ska tas med i datumkomprimeringen. Komprimeringen kommer att påverka alla transaktioner fr.o.m. datumet i fältet Startdatum t.o.m. datumet som du anger här.|
|Period |Välj längden på perioden vars transaktioner ska kombineras. Välj fältet för att se alternativen. Om du har valt perioden *Kvartal*, *Månad* eller *Vecka*, komprimeras bara transaktioner med samma bokföringsperiod.|
|Bibehåll fältinnehåll     |Markera kryssrutorna om du vill bibehålla innehållet i vissa fält trots att transaktionerna komprimeras. Desto fler fält du väljer, desto mer detaljerade kommer de komprimerade transaktionerna att bli. Om du inte markerar några av dessa fält kommer batchjobbet att skapa en transaktion per dag, vecka eller annan period enligt perioden som du valde i fältet **Period**. |

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  

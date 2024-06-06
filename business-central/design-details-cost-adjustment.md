---
title: Designdetaljer – Kostnadsjustering
description: 'Kostnadsjustering flyttar fram kostnadsändringar från kostnadskällor till kostnadsmottagare, enligt en artikels värderingsprincip, för att leverera rätt lagervärdering.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-cost-adjustment"></a>Designdetaljer: Kostnadsjustering

Huvudsyftet med kostnadsjustering är att flytta fram kostnadsändringar från kostnadskällor till kostnadsmottagare, enligt en artikels värderingsprincip, för att leverera rätt lagervärdering.  

En artikel kan vara försäljningsfakturerad innan den har inköpsfakturerats, så att det registrerade lagervärdet för försäljningen inte matchar den faktiska inköpkostnaden. Kostnadsjustering uppdaterar kostnaden för sålda varor (KSV) för historiska försäljningsposter för att se till att de matchar kostnaderna för inkommande transaktioner som de kopplas till. Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md).  

Följande är sekundära syften eller funktioner för kostnadsjustering:  

* Fakturera färdiga produktionsorder:  

  * Ändra statusen på värdetransaktioner från **Förväntad** till **Faktisk**.  
  * Rensa PIA-konton. Mer information finns i [Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md)  
  * Bokför avvikelse. Mer information finns i [Designdetaljer: Varians](design-details-variance.md).  
  * Uppdatera styckkostnaden på artikelkortet.  

Lagerkostnader måste justeras innan de relaterade värdetransaktionerna kan stämmas av med redovisningen. Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Identifiera justeringen

Uppgiften att identifiera om kostnadsjustering ska inträffa utförs i huvudsak av rutinen Artikeljournal – bokför rad, medan uppgiften att beräkna och skapa kostnadsjusteringstransaktioner utförs av batchjobbet **Justera kost. – artikeltrans.**.  

För att kunna flytta kostnader framåt fastställer identifieringmekanismen vilka källor som har ändrats när det gäller kostnader och till vilken destination de här kostnaderna ska flyttas fram. Följande tre identifieringsfunktioner finns i [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Artikelkopplingstransaktion  
* Ingångspunkt för genomsnittlig kostnadsjustering  
* Ordernivå  

### <a name="item-application-entry"></a>Artikelkopplingstransaktion

Identifieringsfunktionen används för artiklar som använder värderingsprinciperna FIFO, LIFO, Standard och Specifik för fasta kopplingsscenarion. Funktionen fungerar så här:  

* Kostnadsjustering upptäcks genom att markera de ursprungliga artikeltransaktionerna som *Kopplad trans. att justera* när en artikeltransaktion eller värdetransaktion bokförs.  
* Kostnader speditioneras enligt kostnadskedjorna som finns i **Artikelkopplingstransaktion**.  

### <a name="average-cost-adjustment-entry-point"></a>Ingångspunkt för genomsnittlig kostnadsjustering

Identifieringsfunktionen används för artiklar som använder värderingsprincipen Genomsnitt. Funktionen fungerar så här:  

* Kostnadsjustering upptäcks, genom att markera en post i  **Ingångspunkt för genomsn.kostn.justering** tabellen, när en värdelöpnummer bokförs.  
* Kostnader speditioneras genom att använda kostnaderna till värdetransaktioner med ett senare värderingsdatum.  

### <a name="order-level"></a>Ordernivå

Den här identifieringsfunktionen används i konverteringsscenarion, produktion och montering. Funktionen fungerar så här:  

* Kostnadsjustering upptäcks genom att markera ordern när ett material/en resurs bokförs som förbrukad/använd.  
* Kostnader speditioneras genom att använda kostnaderna från material/resurs till de utflödetransaktioner som är kopplade till samma order.  

Ordernivåfunktionen används för att identifiera justeringar i monteringsbokföring. Följande grafik visar strukturen för justeringstransaktionen:  

![Postflöde för kostnadsjustering.](media/design_details_assembly_posting_3.png "Postflöde för kostnadsjustering")  

Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  

## <a name="manual-versus-automatic-cost-adjustment"></a>Manuell kontra automatisk kostnadsjustering

Kostnadsjustering kan utföras på två sätt:  

* Manuellt, genom att köra batch-jobbet **Justera kost – artikeltransaktioner**. Du kan köra det här batchjobbet antingen för alla artiklar, eller endast för vissa artiklar eller artikelkategorier. Det här batchjobbet kör en kostnadsjustering för artiklarna i lagret som en inkommande transaktion har gjorts för, till exempel ett inköp. För artiklar som använder värderingsprincipen Genomsnitt gör batchjobbet även en justering om utgående transaktioner skapas.  
* Automatiskt, genom att justera kostnaderna varje gång som du bokför en lagertransaktion, och när du avslutar en produktionsorder. Kostnadsjustering körs endast för den specifika artikeln eller artiklarna som påverkas av bokföringen. Detta ställs in när du väljer kryssrutan **automatisk kostnadsjustering** på sidan **Lagerinställningar**.  

Det är bra övning att köra kostnadsjustering automatiskt när du bokför, eftersom styckkostnader uppdateras oftare och därför är mer korrekta. Nackdelen är att databasens prestanda kan påverkas genom att köra kostnadsjustering så ofta.  

Eftersom det är viktigt att hålla styckkostnaden för en artikel aktuell, rekommenderas du att köra batchjobbet **Justera kost – Artikeltransaktioner** så ofta som möjligt, under lediga timmar. Du kan också använda automatisk kostnadsjustering. Detta säkerställer att styckkostnaden uppdateras dagligen för artiklar.  

Oavsett om du har kört kostnadsjusteringen manuellt eller automatiskt, är justeringen och dess konsekvenser desamma. [!INCLUDE[prod_short](includes/prod_short.md)] beräknar värdet för inkommande transaktionen och skickar denna kostnad för alla utgående transaktioner, till exempel försäljning eller förbrukning som har kopplats till den inkommande transaktionen. Kostnadsjustering skapar värdetransaktioner som innehåller justeringsbelopp och belopp som ska kompensera för avrundning.  

De nya justerings- och avrundningsvärdetransaktionerna har bokföringsdatumet för den relaterade fakturan. Undantaget är om de värdetransaktioner faller inom en stängd bokföringsperiod eller lagerperiod, eller om bokföringsdatumet infaller tidigare än datumet i fältet på sidan **Tillåt bokföring fr.o.m.**  i fönstret **Redovisningsinställningar**. Om det inträffar tilldela batchjobbet bokföringsdatumet som det första datumet i nästa öppna period.  

## <a name="adjust-cost---item-entries-batch-job"></a>Batch-jobbet Justera kost. – artikeltrans.

När du kör batchjobbet **Just kost. – artikeltrans** har du alternativet att köra batchjobbet för alla artiklar eller endast för vissa artiklar eller kategorier.  

> [!NOTE]  
> Vi rekommenderar att du alltid kör batchjobbet för alla artiklar och endast använder filtreringsalternativet för att minska bearbetningstiden för batchjobbet eller för att lösa kostnaden för en viss artikel.  

### <a name="example"></a>Exempel

Följande exempel visar om du bokför en inköpt artikel som inlevererad och fakturerad den 01-01-20. Du bokför senare den sålda artikeln som levererad och fakturerad på 01-15-20. Sedan kör du batchjobben **Justera kost – artikeltrans** och **Bokför lagerkostnad i redov.** Följande transaktioner upprättas.  

#### <a name="value-entries-1"></a>Värdetransaktioner (1)

|Bokföringsdatum|Artikeltransaktionstyp|Kost.belopp (aktuellt)|Kostnad bokförd i redov.|Fakturerat antal|Löpnr|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01-01-20|Inköp|10,00|10,00|1|1|  
|01-15-20|Försäljning|-10.00|-10.00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation (1)

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Redovisningstransaktioner (1)

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)|Belopp|Löpnr|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Lagerkonto]|2130|10,00|1|  
|01-01-20|[Direkt kostnad kopplad – konto]|7291|-10.00|2|  
|01-15-20|[Lagerkonto]|2130|-10.00|3|  
|01-15-20|[KSV-konto]|7290|10,00|4|  

Senare bokför du en relaterad inköpsartikelkostnad på 2,00 BVA som har fakturerats den 02-10-20. Kör batch-jobbet **Justera kost – artikeltrans** och sedan batch-jobbet **Bokför lagerkostnad i redov.**. Batch-jobbet Kostnadsjustering justerar kostnaden för försäljningen med -2,00 BVA, och batch-jobbet **Bokför lagerkostnad i redov.** bokför de nya värdetransaktioner till redovisningen. Resultatet är som följer.  

#### <a name="value-entries-2"></a>Värdetransaktioner (2)

|Bokföringsdatum|Artikeltransaktionstyp|Kost.belopp (aktuellt)|Kostnad bokförd i redov.|Fakturerat antal|Justering|Löpnr|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|02-10-20|Inköp|2,00|2,00|0|Nej|3|  
|01-15-20|Försäljning|-2.00|-2.00|0|Ja|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation (2)

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Redovisningstransaktioner (2)

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)|Belopp|Löpnr|  
|------------|-----------|------------------------|------|---------|  
|02-10-20|[Lagerkonto]|2130|2,00|5|  
|02-10-20|[Direkt kostnad kopplad – konto]|7291|-2.00|6|  
|01-15-20|[Lagerkonto]|2130|-2.00|7|  
|01-15-20|[KSV-konto]|7290|2,00|8|  

## <a name="automatic-cost-adjustment"></a>Automatisk kostnadsjustering

Om du vill ställa in kostnadsjusteringen att köras automatiskt när du bokför en lagertransaktion använder du fältet **Automatisk kostnadsjustering** på sidan **Lagerinställning**. Detta fält ger dig möjlighet att välja hur lång tillbaka i tiden från det aktuella arbetsdatumet som du vill att den automatiska kostnadsjusteringen ska utföras. Följande alternativ finns.  

|Alternativ|Description|
|------|-----------|
|Aldrig|Kostnaderna justeras inte vid bokföringen.|  
|Dag|Kostnaderna justeras om bokföringen sker inom ett dygn från arbetsdatumet.|  
|Vecka|Kostnaderna justeras om bokföringen sker inom en vecka från arbetsdatumet.|  
|Månad|Kostnaderna justeras om bokföringen sker inom en månad från arbetsdatumet.|  
|Kvartal|Kostnaderna justeras om bokföringen sker inom ett kvartal från arbetsdatumet.|  
|År|Kostnaderna justeras om bokföringen sker inom ett år från arbetsdatumet.|  
|Alltid|Kostnaderna justeras alltid vid bokföringen, oavsett bokföringsdatum.|  

Urvalet som du gör i fältet **Automatisk kostnadsjustering** är viktigt för prestanda och dina kostnaders korrekthet. Kortare tidsperioder, till exempel **Dag** eller **Vecka**, påverkar systemprestanda mindre, eftersom har strängare krav att endast kostnader som har bokförts inom den sista dagen eller veckan kan justeras automatiskt. Det innebär att den automatiska kostnadsjusteringen inte körs lika ofta och därför påverkar systemprestanda mindre. Det betyder också¨att styckkostnaderna kan vara mindre exakta.  

### <a name="example-1"></a>Exempel

Följande exempel visar ett automatiskt kostnadsjusteringscenario:  

* Den 10 januari bokför du en inköpt artikel som inlevererad och fakturerad.  
* Den 15 januari bokför du en försäljningsorder för artikeln som levererad och fakturerad.
* Den 5 februari får du en faktura för en fraktkostnad på det ursprungliga inköpet. Du bokför fraktkostnaden, och kopplar den till den ursprungliga inköpsfakturan, vilket ökar kostnaden för det ursprungliga inköpet.  

Om du har ställt in automatisk kostnadsjustering som ska kopplas till bokföringar som uppstår inom en månad eller ett kvartal från datumet för aktuellt arbetsdatum, körs den automatiska kostnadsjusteringen och kostnaden för köpet speditioneras till försäljningen.  

Om du har ställt in automatisk kostnadsjustering som ska kopplas till bokföringar som uppstår under en dag eller en vecka från datumet för aktuellt arbetsdatum, körs den automatiska kostnadsjusteringen inte och kostnaden för köpet speditioneras inte till försäljningen förrän du kör batch-jobbet **Justera kost. – artikeltrans.**.  

## <a name="see-also"></a>Se även

[Justera artikelkostnader](inventory-how-adjust-item-costs.md)  
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
[Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md)  
[Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)  
[Designdetaljer: Varians](design-details-variance.md)  
[Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  
[Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

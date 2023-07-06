---
title: Designdetaljer – Lagerbokföring | Microsoft Docs
description: 'Varje lagertransaktion, t.ex en inköpsinleverans eller en utleverans, bokför två transaktioner av olika typer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-inventory-posting"></a><a name="design-details-inventory-posting"></a><a name="design-details-inventory-posting"></a>Designdetaljer: Lagerbokföring

Varje lagertransaktion, t.ex en inköpsinleverans eller en utleverans, bokför två transaktioner av olika typer.  

|Transaktionstyp|Description|  
|----------|-----------|  
|Antal|Återspeglar förändringen av antalet i lager. Informationen lagras som artikeltransaktioner.<br /><br /> Tillsammans med artikelkopplingstransaktioner.|  
|Värde|Återspeglar förändringen av lagervärdet. Informationen lagras som värdetransaktioner.<br /><br /> Det kan finnas en eller flera värdetransaktioner för varje artikeltransaktion eller kapacitetstransaktion.<br /><br /> Se [Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md) för information om kapacitetvärdetransaktioner som rör användningen av produktions- eller monteringsresurser.|  

 I relation till antalsbokföringar finns artikelkopplingstransaktioner för att koppla lagerökning till lagerminskning. Det gör det möjligt för värderingsmotorn att flytta kostnader framåt från ökningar till de relaterade minskningarna och vice versa. Mer information finns i [Designdetaljer: Artikelkoppling](design-details-item-application.md).  

 Artikeltransaktioner, värdetransaktioner och artikelkopplingstransaktioner skapas som ett resultat av att bokföra en artikeljournalrad, antingen indirekt genom att bokföra en orderrad eller direkt på sidan Artikeljournal.  

 Med regelbundna intervall bokförs värdetransaktioner som skapas i inventeringen i redovisningen för att stämma av de två redovisningarna för ekonomisk kontroll. Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).  

 ![Transaktionsflöde vid avstämning av lager med redovisning.](media/design_details_inventory_costing_1_entry_flow.png "Transaktionsflöde vid avstämning av lager med redovisning")  

## <a name="example"></a><a name="example"></a><a name="example"></a>Exempel

Följande exempel visar hur artikeltransaktioner, värdetransaktioner och artikelkopplingstransaktioner skapas i redovisningstransaktioner.  

 Du bokför en inköpsorder som har inlevererats och fakturerats för 10 artiklar med en direkt styckkostnad på BVA 7 och en omkostnad på BVA 1. Bokföringsdatumet är 20-01-01. Följande transaktioner upprättas.  

### <a name="item-ledger-entries-1"></a><a name="item-ledger-entries-1"></a><a name="item-ledger-entries-1"></a>Artikeltransaktioner (1)

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Antal|Löpnr|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Inköp|80.00|10|1|  

### <a name="value-entries-1"></a><a name="value-entries-1"></a><a name="value-entries-1"></a>Värdetransaktioner (1)

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Inköpskostnad|70,00|1|1|  
|01-01-20|Indirekt kostnad|10,00|1|2|  

### <a name="item-application-entries-1"></a><a name="item-application-entries-1"></a><a name="item-application-entries-1"></a>Kopplingstransaktioner för artikel (1)

|Löpnr|Artikeltrans.löpnr|inkommande artikeltrans.nr|utgående artikeltrans.nr|Antal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Nu bokför du en försäljning på 10 enheter av artikeln med ett bokföringsdatum på 01-15-20.  

### <a name="item-ledger-entries-2"></a><a name="item-ledger-entries-2"></a><a name="item-ledger-entries-2"></a>Artikeltransaktioner (2)

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Antal|Löpnr|  
|------------|----------|--------------------|--------|---------|  
|01-15-20|Försäljning|-80.00|-10|2|  

### <a name="value-entries-2"></a><a name="value-entries-2"></a><a name="value-entries-2"></a>Värdetransaktioner (2)

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------|----------|--------------------|---------------------|---------|  
|01-15-20|Direkt kostnad|-80.00|2|3|  

### <a name="item-application-entries-2"></a><a name="item-application-entries-2"></a><a name="item-application-entries-2"></a>Kopplingstransaktioner för artikel (2)

|Löpnr|Artikeltrans.löpnr|inkommande artikeltrans.nr|utgående artikeltrans.nr|Antal|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

Vid slutet av bokföringsperioden kör du batchjobbet **Bokför lagerkostnad i redov** för att stämma av de här lagertransaktionerna med redovisningen.  

 Mer information finns i [Desigdetaljer: konton i redovisningen](design-details-accounts-in-the-general-ledger.md).  

 Följande tabeller visar resultatet av avstämningen av lagertransaktionerna i det här exemplet med redovisningen.  

### <a name="value-entries-3"></a><a name="value-entries-3"></a><a name="value-entries-3"></a>Värdetransaktioner (3)

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Kostnad bokförd i redov.|Artikeltrans.löpnr|Löpnr|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Inköpskostnad|70,00|70,00|1|1|  
|01-01-20|Indirekt kostnad|10,00|10,00|1|2|  
|01-15-20|Direkt kostnad|-80.00|-80.00|2|3|  

### <a name="general-ledger-entries-3"></a><a name="general-ledger-entries-3"></a><a name="general-ledger-entries-3"></a>Redovisningstransaktioner (3)

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)|Belopp|Löpnr|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Lagerkonto]|2130|70,00|1|  
|01-01-20|[Direkt kostnad kopplad – konto]|7291|-70.00|2|  
|01-01-20|[Lagerkonto]|2130|10,00|3|  
|07.01.01|[Omkostnader kopplade, konto]|7292|-10.00|4|  
|01-15-20|[Lagerkonto]|2130|-80.00|5|  
|01-15-20|[KSV-konto]|7290|80.00|6|  

> [!NOTE]  
> Bokföringsdatumet för redovisningstransaktionerna är samma som för de relaterade värdetransaktionerna.  
> 
> Fältet **Kostnad bokförd i redov** i tabellen **Värdetransaktion**.  

 Relationen mellan värdetransaktioner och bokföringstransaktioner lagras i tabellen **Artikeltrans.relation**.  

### <a name="relation-entries-in-the-gl--item-ledger-relation-table-3"></a><a name="relation-entries-in-the-gl--item-ledger-relation-table-3"></a><a name="relation-entries-in-the-gl--item-ledger-relation-table-3"></a>Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation (3)

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a><a name="assembly-and-production-posting"></a><a name="assembly-and-production-posting"></a>Montering- och produktionsbokföring

Kapacitets – och resurstransaktioner representerar den tid som bokförs som förbrukad i produktionen eller monteringen. Dessa bearbetningskostnader bokförs som värdetransaktioner i redovisningen tillsammans med relevanta materialkostnader i en liknande struktur som den som beskrivs för artikeltransaktioner i det här avsnittet.  

Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)  
 [Designdetaljer: Konton i redovisningen](design-details-accounts-in-the-general-ledger.md)  
 [Designdetaljer: Kostnadskomponenter](design-details-cost-components.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

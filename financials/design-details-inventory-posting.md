---
title: "Designdetaljer - Lagerbokföring | Microsoft Docs"
description: "Varje lagertransaktion, t.ex en inköpsinleverans eller en utleverans, bokför två transaktioner av olika typer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9bc177d45efa1e6e772ed70cc66de393e6250def
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-posting"></a>Designdetaljer: Lagerbokföring
Varje lagertransaktion, t.ex en inköpsinleverans eller en utleverans, bokför två transaktioner av olika typer.  

|Transaktionstyp|Description|  
|----------------|---------------------------------------|  
|Antal|Återspeglar förändringen av antalet i lager. Informationen lagras som artikeltransaktioner.<br /><br /> Tillsammans med artikelkopplingstransaktioner.|  
|Värde|Återspeglar förändringen av lagervärdet. Informationen lagras som värdetransaktioner.<br /><br /> Det kan finnas en eller flera värdetransaktioner för varje artikeltransaktion eller kapacitetstransaktion.<br /><br /> Se [Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md) för information om kapacitetvärdetransaktioner som rör användningen av produktions- eller monteringsresurser.|  

 I relation till antalsbokföringar finns artikelkopplingstransaktioner för att koppla lagerökning till lagerminskning. Det gör det möjligt för värderingsmotorn att flytta kostnader framåt från ökningar till de relaterade minskningarna och vice versa. Mer information finns i [Designdetaljer: Artikelspårning](design-details-item-application.md).  

 Artikeltransaktioner, värdetransaktioner och artikelkopplingstransaktioner skapas som ett resultat av att bokföra en artikeljournalrad, antingen indirekt genom att bokföra en orderrad eller direkt i fönstret Artikeljournal.  

 Med regelbundna intervall bokförs värdetransaktioner som skapas i inventeringen i redovisningen för att stämma av de två redovisningarna för ekonomisk kontroll. Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).  

 ![Transaktionsflöde mellan lager och redovisning & #47; L](media/design_details_inventory_costing_1_entry_flow.png "design_details_inventory_costing_1_entry_flow")  

## <a name="example"></a>Exempel  
 Följande exempel visar hur artikeltransaktioner, värdetransaktioner och artikelkopplingstransaktioner skapas i redovisningstransaktioner.  

 Du bokför en inköpsorder som har inlevererats och fakturerats för 10 artiklar med en direkt enhetskostnad på BVA 7 och en omkostnad på BVA 1. Bokföringsdatumet är 20-01-01. Följande transaktioner upprättas.  

 **Artikeltransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Antal|Löpnr|  
|------------------|----------------|----------------------------|--------------|---------------|  
|01-01-20|Inköp|80.00|10|1|  

 **Värdetransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|01-01-20|Inköpskostnad|70,00|1|1|  
|01-01-20|Indirekt kostnad|10,00|1|2|  

 **Kopplingstransaktioner för artikel**  

|Löpnr|Artikeltrans.löpnr|Ankommande artikeltrans.nr|Avgående artikeltrans.nr|Antal|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|1|1|1|0|10|  

 Nu bokför du en försäljning på 10 enheter av artikeln med ett bokföringsdatum på 01-15-20.  

 **Artikeltransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)||Antal|Löpnr|  
|------------------|----------------|----------------------------|-|--------------|---------------|  
|01-15-20|Försäljning|-80.00||-10|2|  

 **Värdetransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|01-15-20|Inköpskostnad|-80.00|2|3|  

 **Kopplingstransaktioner för artikel**  

|Löpnr|Artikeltrans.löpnr|Internt artikeltrans.nr|Externt artikeltrans.nr|Antal|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|2|2|0|2|-10|  

 Vid slutet av bokföringsperioden kör du batchjobbet **Bokför lagerkostnad i redov** för att stämma av de här lagertransaktionerna med redovisningen.  

 Mer information finns i [Desigdetaljer: konton i redovisningen](design-details-accounts-in-the-general-ledger.md).  

 Följande tabeller visar resultatet av avstämningen av lagertransaktionerna i det här exemplet med redovisningen.  

 **Värdetransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (aktuellt)|Kostnad bokförd i redov.|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|----------------------------|-------------------------|---------------------------|---------------|  
|01-01-20|Inköpskostnad|70,00|70,00|1|1|  
|01-01-20|Indirekt kostnad|10,00|10,00|1|2|  
|01-15-20|Inköpskostnad|-80.00|-80.00|2|3|  

 **Redovisningstransaktioner**  

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)||Belopp|Löpnr|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|01-01-20|[Lagerkonto]|2130||70,00|1|  
|01-01-20|[Direkt kostnad kopplad - konto]|7291||-70.00|2|  
|01-01-20|[Lagerkonto]|2130||10,00|3|  
|07.01.01|[Omkostnader kopplade, konto]|7292||-10.00|4|  
|01-15-20|[Lagerkonto]|2130||-80.00|5|  
|01-15-20|[KSV-konto]|7290||80.00|6|  

> [!NOTE]  
>  Bokföringsdatumet för redovisningstransaktionerna är samma som för de relaterade värdetransaktionerna.  
>   
>  Fältet **Kostnad bokförd i redov** i tabellen **Värdetransaktion**.  

 Relationen mellan värdetransaktioner och bokföringstransaktioner lagras i tabellen **Artikeltrans.relation**.  

 **Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**  

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a>Montering- och produktionsbokföring  
Kapacitets - och resurstransaktioner representerar den tid som bokförs som förbrukad i produktionen eller monteringen. Dessa bearbetningskostnader bokförs som värdetransaktioner i redovisningen tillsammans med relevanta materialkostnader i en liknande struktur som den som beskrivs för artikeltransaktioner i det här avsnittet.  

Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Konton i redovisningen](design-details-accounts-in-the-general-ledger.md)   
 [Designdetaljer: Kostnadskomponenter](design-details-cost-components.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


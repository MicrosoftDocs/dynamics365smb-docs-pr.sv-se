---
title: Designdetaljer - Tabellstruktur | Microsoft Docs
description: "För att förstå hur lagringen och bokföringen av dimensionstransaktioner har omdesignats är det viktigt att förstå tabellstrukturen."
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
ms.openlocfilehash: a1d7337abcb538ef310ea6f87312934d01540b00
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-table-structure"></a>Designdetaljer: Tabellstruktur
För att förstå hur lagringen och bokföringen av dimensionstransaktioner har omdesignats är det viktigt att förstå tabellstrukturen.  

## <a name="new-tables"></a>Nya tabeller  
 Tre nya tabeller har utformats för att hantera dimensionsuppsättningstransaktioner.  

### <a name="table-480-dimension-set-entry"></a>Tabell 480 Dimensionsuppsättnings transaktion  
 Tabell 480 **Dimensionsuppsättnings transaktion** är en ny tabell. Tabellen kan inte ändras. Följande data har upprättats skriftligt till tabellen. Du kan inte ta bort eller redigera dem. När du tar bort data måste du kontrollera mot alla förekomster av dimensionsuppsättning-ID i hela databasen, inklusive partnerlösningar.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Heltal|>0,0 har reserverats för den tomma dimensionsuppsättningen. Referensfält 3 i tabell 481.|  
|2|**Dimensionskod**|Kod 20|Tabellrelation till tabell 348.|  
|3|**Dimensionsvärdekod**|Kod 20|Tabellrelation till tabell 349.|  
|4|**Dimensionsvärde-ID**|Heltal|Referensfält 12 i tabell 349. Det är den sekundära nyckeln som du använder för att gå igenom tabellen 481.|  
|5|**Dimensionsnamn**|Text 30|CalcField. Uppslag i tabell 348.|  
|6|**Dimensionsvärdesnamn**|Text 30|CalcField. Uppslag i tabell 349.|  

#### <a name="table-481-dimension-set-tree-node"></a>Tabell 481 Trädnod för dimensionsuppsättning  
 Tabell 481 **Trädnod för dimensionsuppsättning** är en ny tabell. Tabellen kan inte ändras. Den används för att söka efter en dimensionsuppsättning. Om dimensionsuppsättningen inte hittas, skapas en ny uppsättning.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|1|**ID för överordnad dimensionsuppsättning**|Heltal|0 för nod för högsta nivå.|  
|2|**Dimensionsvärde-ID**|Heltal|Tabellrelation till fält 12 i tabell 349.|  
|3|**Dimensionsuppsättnings-ID**|Heltal|AutoIncrement. Använt i fält 1 i tabell 480.|  
|4|**Används**|Booleskt|Falskt om det inte används.|  

##### <a name="table-482-reclas-dimension-set-buffer"></a>Tabell 482 Gruppera dimensionsuppsättningsbuffert  
 Tabell 482 **Gruppera dimensionsuppsättningsbuffert** är en ny tabell. Tabellen används för att redigera ett dimensionsuppsättnings-ID. Det krävs när du redigerar en dimensionsvärdekod och en ny dimensionsvärdekod, till exempel i tabellen **Artikelgrupperingsjournal**.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensionskod**|Kod 20|Tabellrelation till tabell 348.|  
|2|**Dimensionsvärdekod**|Kod 20|Tabellrelation till tabell 349.|  
|3|**Dimensionsvärde-ID**|Heltal|Referensfält 12 i tabell 349.|  
|4|**Ny dimensionsvärdekod**|Kod 20|Tabellrelation till tabell 349.|  
|5|**Nytt dimensionsvärde-ID**|Heltal|Referensfält 12 i tabell 349.|  
|6|**Dimensionsnamn**|Text 30|CalcField. Uppslag i tabell 348.|  
|7|**Dimensionsvärdesnamn**|Text 30|CalcField. Uppslag i tabell 349.|  
|8|**Nytt dimensionsvärdesnamn**|Text 30|CalcField. Uppslag i tabell 349.|  

## <a name="modified-tables"></a>Ändrade tabeller  
 Alla transaktions- och budgettabeller har ändrats för att hantera dimensionsuppsättningposter.  

### <a name="changes-to-transaction-and-budget-tables"></a>Ändringar i transaktions- och budgettabeller  
 Ett nytt fält har lagts till alla i transaktions- och budgettabeller.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsuppsättnings-ID**|Heltal|Referensfält 1 i tabell 480.|  

#### <a name="changes-to-table-83-item-journal-line"></a>Ändringar i tabell 83 Artikeljournalrad  
 Två nya fält har lagts till i tabellen 83 **Artikeljournalrad**.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsuppsättnings-ID**|Heltal|Referensfält 1 i tabell 480.|  
|481|**Nytt dimensionsuppsättnings-ID**|Heltal|Referensfält 1 i tabell 480.|  

##### <a name="changes-to-table-349-dimension-value"></a>Ändringar i tabell 349 Dimensionsvärde  
 Ett nytt fält har lagts till i tabellen 349 **Dimensionsvärde**.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensionsvärde-ID**|Heltal|AutoIncrement. Använt för referenser i tabell 480 och tabell 481.|  

###### <a name="tables-that-get-new-field-480-dimension-set-id"></a>Tabeller som får nytt dimensionsuppsättning-ID för fält 480  
 Ett nytt fält, 480, **Dimensionsuppsättnings-ID**har lagts till i efterföljande tabeller. För tabellerna som lagrar bokförda data visar fältet endast icke-redigerbara dimensioner som är markerade som Gå nedåt. För tabellerna som lagrar arbetsdokument är fältet redigerbart. Bufferttabellerna som används internt behöver inte redigerbara eller icke-redigerbara möjligheter.  

 Fältet 480 kan inte redigeras i följande tabeller.  

|Tabellnr|Tabellnamn|  
|---------------|----------------|  
|17|**Redovisningstransaktion**|  
|21|**Kundreskontra**|  
|25|**Lev.reskontratransaktion**|  
|32|**Artikeltransaktion**|  
|110|**Utleveranshuvud**|  
|111|**Förs.utleveransrad**|  
|112|**Försäljningsfakturahuvud**|  
|113|**Försäljningsfakturarad**|  
|114|**Kreditnotahuvud**|  
|115|**Kreditnotarad**|  
|120|**Inleveranshuvud**|  
|121|**Inleveransrad**|  
|122|**Inköpsfakturahuvud**|  
|123|**Inköpsfakturarad**|  
|124|**Inköpskreditnotahuvud**|  
|125|**Inköpskreditnotarad**|  
|169|**Projekttransaktion**|  
|203|**Resurstransaktion**|  
|271|**Bankkontotransaktion**|  
|281|**Inventeringstransaktion**|  
|297|**Utskickat bet.påminnelsehuvud**|  
|304|**Utskickat räntefakturahuvud**|  
|5107|**Förs.huvud arkiv**|  
|5108|**Förs.rad arkiv**|  
|5109|**Inköpshuvud arkiv**|  
|5110|**Inköpsrad arkiv**|  
|5601|**Anl. transaktion**|  
|5625|**Underhållstransaktion**|  
|5629|**Försäkringstransaktion**|  
|5744|**Överföringsutleveranshuvud**|  
|5745|**Överföringsutleveransrad**|  
|5746|**Överföring inleveranshuvud**|  
|5747|**Överföring inleveransrad**|  
|5802|**Värdetransaktion**|  
|5832|**Kapacitetstrans.**|  
|5907|**Servicetransaktion**|  
|5908|**Servicehuvud**|  
|5933|**Tjänsteorder bokf.buffer**|  
|5970|**Arkiverat serv.kontrakt huvud**|  
|5990|**Serviceutleveranshuvud**|  
|5991|**Serviceutleveransrader**|  
|5992|**Servicefakturahuvud**|  
|5993|**Servicefakturarad**|  
|5994|**Servicekreditnota, huvud**|  
|5995|**Servicekreditnota, rad**|  
|6650|**Returutleverans huvud**|  
|6651|**Returutleveransrad**|  
|6660|**Returinleveranshuvud**|  
|6661|**Förs.inleverans rad**|  

 Fältet 480 kan redigeras i följande tabeller.  

|Tabellnr|Tabellnamn|  
|---------------|----------------|  
|36|**Försäljningshuvud**|  
|37|**Försäljningsrad**|  
|38|**Inköpshuvud**|  
|39|**Inköpsrad**|  
|81|**Redovisningsjournalrad**|  
|83|**Artikeljournalrad**|  
|89|**Strukturjournalrad**|  
|96|**Redov.budgettransaktion**|  
|207|**Resursjournalrad**|  
|210|**Projektjournalrad**|  
|221|**Redovisningsjnl med fördelning**|  
|246|**Rekvisitionsrad**|  
|295|**Betalningspåminnelsehuvud**|  
|302|**Räntefakturahuvud**|  
|5405|**Produktionsorder**|  
|5406|**Prod.orderrad**|  
|5407|**Prod.orderkomponent**|  
|5615|**Anl. fördelning**|  
|5621|**Anl. journalrad**|  
|5635|**Försäkringsjournalrad**|  
|5740|**Överföringshuvud**|  
|5741|**Överföringsrad**|  
|5900|**Servicehuvud**|  
|5901|**Serviceartikelrad**|  
|5902|**Servicerad**|  
|5965|**Servicekontrakt huvud**|  
|5997|**Standardservicerad**|  
|7134|**Artikelbudgettransaktion**|  
|99000829|**Planeringskomponent**|  

 Fältet 480 har lagts till i följande bufferttabeller.  

|Tabellnr|Tabellnamn|  
|---------------|----------------|  
|49|**Fakturabokföringsbuffert**|  
|212|**Projektbokföringsbuffert**|  
|372|**Betalningsbuffer**|  
|382|**KL resk.trans. buffer**|  
|461|**Buffert för fakturarad (förskottsbetalning)**|  
|5637|**Anl. redov. bokf.buffer**|  
|7136|**Buffert för artikelbudget**|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Dimensionsuppsättningstransaktioner](design-details-dimension-set-entries.md)   
 [Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   
 [Designdetaljer: Kodenhet 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
 [Designdetaljer: Kodexempel på ändrade mönster i ändringar](design-details-code-examples-of-changed-patterns-in-modifications.md)


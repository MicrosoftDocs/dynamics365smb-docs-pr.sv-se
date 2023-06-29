---
title: Designdetaljer – Tabellstruktur | Microsoft Docs
description: För att förstå hur lagringen och bokföringen av dimensionstransaktioner har omdesignats är det viktigt att förstå tabellstrukturen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-table-structure"></a><a name="design-details-table-structure"></a>Designdetaljer: Tabellstruktur
För att förstå hur dimensionstransaktioner lagras och bokförs är det viktigt att förstå tabellstrukturen.  

## <a name="table-480-dimension-set-entry"></a><a name="table-480-dimension-set-entry"></a>Tabell 480, dimensionsuppsättningstransaktion
Tabellen kan inte ändras. Följande data har upprättats skriftligt till tabellen. Du kan inte ta bort eller redigera dem.

|Fältnummer|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Heltal|>0,0 har reserverats för den tomma dimensionsuppsättningen. Referensfält 3 i tabell 481.|  
|2|**Dimensionskod**|Kod 20|Tabellrelation till tabell 348.|  
|3|**Dimensionsvärdekod**|Kod 20|Tabellrelation till tabell 349.|  
|4|**Dimensionsvärde-ID**|Heltal|Referensfält 12 i tabell 349. Det är den sekundära nyckeln som du använder för att gå igenom tabellen 481.|  
|5|**Dimensionsnamn**|Text 30|CalcField. Uppslag i tabell 348.|  
|6|**Dimensionsvärdesnamn**|Text 30|CalcField. Uppslag i tabell 349.|  

## <a name="table-481-dimension-set-tree-node"></a><a name="table-481-dimension-set-tree-node"></a>Tabell 481, Trädnod för dimensionsuppsättning
Tabellen kan inte ändras. Den används för att söka efter en dimensionsuppsättning. Om dimensionsuppsättningen inte hittas, skapas en ny uppsättning.  

|Fältnr|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|1|**ID för överordnad dimensionsuppsättning**|Heltal|0 för nod för högsta nivå.|  
|2|**Dimensionsvärde-ID**|Heltal|Tabellrelation till fält 12 i tabell 349.|  
|3|**Dimensionsuppsättnings-ID**|Heltal|AutoIncrement. Använt i fält 1 i tabell 480.|  
|4|**Används**|Booleskt|Falskt om det inte används.|  

## <a name="table-482-reclas-dimension-set-buffer"></a><a name="table-482-reclas-dimension-set-buffer"></a>Tabell 482 Gruppera dimensionsuppsättningsbuffert
Tabellen används om du till exempel ändrar en dimensionsvärdekod i en artikeltransaktion med hjälp av sidan **artikelgrupperingsjournal**.  

|Fältnummer|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensionskod**|Kod 20|Tabellrelation till tabell 348.|  
|2|**Dimensionsvärdekod**|Kod 20|Tabellrelation till tabell 349.|  
|3|**Dimensionsvärde-ID**|Heltal|Referensfält 12 i tabell 349.|  
|4|**Ny dimensionsvärdekod**|Kod 20|Tabellrelation till tabell 349.|  
|5|**Nytt dimensionsvärde-ID**|Heltal|Referensfält 12 i tabell 349.|  
|6|**Dimensionsnamn**|Text 30|CalcField. Uppslag i tabell 348.|  
|7|**Dimensionsvärdesnamn**|Text 30|CalcField. Uppslag i tabell 349.|  
|8|**Nytt dimensionsvärdesnamn**|Text 30|CalcField. Uppslag i tabell 349.|  

## <a name="transaction-and-budget-tables"></a><a name="transaction-and-budget-tables"></a>Transaktions- och budgettabeller
Det här fältet är viktigt förutom andra dimensionsfälten i tabellen:  

|Fältnummer|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsuppsättnings-ID**|Heltal|Referensfält 1 i tabell 480.|  

### <a name="table-83-item-journal-line"></a><a name="table-83-item-journal-line"></a>Tabell 83, artikeljournalrad
Det här fältet är viktigt förutom andra dimensionsfälten i tabellen:  

|Fältnummer|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionsuppsättnings-ID**|Heltal|Referensfält 1 i tabell 480.|  
|481|**Nytt dimensionsuppsättnings-ID**|Heltal|Referensfält 1 i tabell 480.|  

### <a name="table-349-dimension-value"></a><a name="table-349-dimension-value"></a>Tabell 349, dimensionsvärde
Det här fältet är viktigt förutom andra dimensionsfälten i tabellen:  

|Fältnummer|Fältnamn|Datatyp|Kommentar|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensionsvärde-ID**|Heltal|AutoIncrement. Använt för referenser i tabell 480 och tabell 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field"></a><a name="tables-that-contain-the-dimension-set-id-field"></a>Tabeller som innehåller fältet dimensionsuppsättning-ID
 Fältet **dimensionsuppsättning-ID** (480) finns i följande tabeller. För tabellerna som lagrar bokförda data visar fältet endast icke-redigerbara dimensioner som är markerade som Gå nedåt. För tabellerna som lagrar arbetsdokument är fältet redigerbart. Bufferttabellerna som används internt behöver inte redigerbara eller icke-redigerbara möjligheter.  

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

Fältet 480 finns i följande bufferttabeller.  

|Tabellnr|Tabellnamn|  
|---------------|----------------|  
|49|**Fakturabokföringsbuffert**|  
|212|**Projektbokföringsbuffert**|  
|372|**Betalningsbuffer**|  
|382|**KL resk.trans. buffer**|  
|461|**Buffert för fakturarad (förskottsbetalning)**|  
|5637|**Anl. redov. bokf.buffer**|  
|7136|**Buffert för artikelbudget**|  

## <a name="see-also"></a><a name="see-also"></a>Se även

[Översikt över dimensionsuppsättningstransaktioner](design-details-dimension-set-entries-overview.md)  
[Designdetaljer: Söka efter dimensionskombinationer](design-details-searching-for-dimension-combinations.md)   

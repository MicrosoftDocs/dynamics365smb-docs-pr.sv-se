---
title: Serviceprishantering | Microsoft Docs
description: "Det här ämnet beskriver hur du tillämparbästa pris på serviceorder, lägga upp egna serviceprisavtal för kunder, förbättra de anställdas effektivitet och effektivisera faktureringen."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 75c50a7044e3494df5aadb90caa1c008a6ac101c
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="service-price-management"></a>Serviceprishantering
Med funktionen för serviceprishantering kan du tillämpa bästa pris på serviceorder, lägga upp egna serviceprisavtal för kunder, förbättra de anställdas effektivitet och effektivisera faktureringen.  
  
Med serviceprishanteringen kan du också lägga upp olika serviceprisgrupper, så att du kan ta hänsyn till serviceartikeln eller serviceartikelgruppen, samt till vilken typ av fel serviceuppgiften gäller. Du kan lägga upp dessa grupper för en begränsad tidsperiod eller för en viss kund eller valuta. Du kan använda prisberäkningsstrukturer som mallar om du vill koppla ett visst pris till en viss serviceuppgift.  
  
Du kan till exempel koppla specifika artiklar som ingår i servicepriset samt vilken typ av uppgifter som ingår. Det går också att använda olika moms- och rabattbelopp för olika serviceprisgrupper. Om du vill se till att rätt pris används tilldelar du fasta, minsta eller högsta priser – beroende på vilka avtal som du har med kunderna.  
  
Innan priset på en serviceartikel justeras på en serviceorder får du en översikt över resultatet av prisjusteringen. Du kan godkänna de här resultaten eller göra ytterligare ändringar om du vill ha ett annat slutresultat. Hela justeringen görs rad för rad, vilket innebär att inga extra rader skapas.  
  
Slutligen kan du med hjälp av statistik och standardrapporter följa upp lönsamheten för varje serviceprisgrupp.  
  
## <a name="service-price-adjustment-groups"></a>Serviceprisjusteringsgrupper  
Du använder serviceprisjusteringsgrupper när du vill lägga upp olika typer av prisjusteringar. Du kan till exempel lägga upp en serviceprisjusteringsgrupp som justerar priset för reservdelar, en som justerar priset för arbetstid och en som justerar priset för kostnader och så vidare. Du kan också ange om serviceprisjusteringen ska gälla för bara en viss artikel eller resurs, eller för alla artiklar eller resurser.  
  
Varje serviceprisjusteringsgrupp innehåller information om de justeringar som du vill göra av serviceraderna.  
  
Serviceprisjusteringsfunktionen används inte för serviceartiklar som hör till servicekontrakt. Du kan bara justera servicepriserna för artiklar som finns på serviceordern. Du kan inte justera priset för en serviceartikel med garanti. Det går inte att justera priset för en serviceartikel i en serviceorder om serviceraden som är kopplad till artikeln har bokförts som faktura, antingen helt eller delvis.  
  
När du kör serviceprisjusteringsfunktionen ersätts alla rabatter i ordern av värdena för serviceprisjusteringen.  
  
## <a name="service-price-groups"></a>Serviceprisgrupper  
Du kan lägga upp serviceprisgrupper om du vill skapa grupper med serviceartiklar som har samma speciella serviceprissättning. När du har definierat serviceprisgrupper kan du fördela dem till serviceartiklar på serviceartikelraderna. Du kan även tilldela serviceprisgrupper till serviceartikelgrupper.  
  
Innan du tilldelar en serviceprisgrupp till en serviceartikel måste du bestämma vilken feltyp, valuta eller serviceprisjusteringsgrupp som serviceprisgruppen ska gälla för. Du måste bestämma vilket belopp som servicepriset ska justeras till, och om moms och rabatter ingår i detta belopp. Du ska också ange om denna justering gäller ett fast belopp eller om den bara ska användas under vissa villkor.  
  
När du tilldelar en serviceprisgrupp till en serviceartikel, kommer all specifik serviceprissättning som du anger i den här gruppen att gälla för denna serviceartikel.  
  
## <a name="service-pricing"></a>Serviceprissättning  
Du anger faktiska prissättningstyper (prisjusteringstyp och pris) för en kombination av serviceprisgrupper och kundprisgrupper. För varje typ av serviceprissättning väljer du en serviceprisjusteringsgrupp. Du anger även serviceprisjusteringstypen – fast, maximum eller minimum – och det faktiska priset.  
  
Du kan t.ex. ange typer av serviceprissättning för prissättningsgruppen radio. För kunder utan prisgrupp kan du välja att ha serviceprissättning med maximalt pris för arbete, vilket är prisjusteringsgruppen för arbete. För kunder med en särskild prisgrupp kan du välja serviceprissättning med ett fast pris för arbete, vilket är samma prisjusteringsgrupp för arbete.  
  
## <a name="service-price-adjustment"></a>Serviceprisjustering  
Med serviceprisjustering kan du justera priset för en artikel, resurs, ett redovisningskonto eller en kostnad på en serviceorder.  
  
När du har registrerat en artikel på en serviceartikelrad anger du all information om kostnaderna för artikeln på serviceraderna. När du kör funktionen Justera servicepris, kan du förhandsgranska prisjusteringarna. Du kan ändra om det behövs. När du har godkänt ändringarna beräknas justeringarna. Sedan överförs de till serviceraderna. Sedan bokför du serviceordern.  
  
Beroende på typ av serviceprisjustering beräknas det totala beloppet för justeringarna på följande sätt.  
  
Beräkningarna beskrivs i tabellen nedan.  
  
|Alternativ | Description |  
|----------------------------------|---------------------------------------|  
|**Fast pris**|Detta innebär att du debiterar ett fast pris för serviceartikeln, resursen, redovisningskontot eller kostnaden, oavsett faktiska kostnader eller normala avgifter. Om du väljer det här alternativet innebär det att serviceprisjusteringen uppgår till exakt det belopp som anges i serviceprisgruppen.|  
|**Maximal**|Detta innebär att du anger en övre gräns för avgiften till kunden, oavsett faktiska kostnader eller andra avgifter. Om du väljer det här alternativet innebär det att serviceprisjusteringen bara utförs om det totala priset överskrider det belopp som anges i serviceprisgruppen.|  
|**Minimal**|Detta innebär att du anger en undre gräns för avgiften till kunden, oavsett faktiska kostnader eller andra avgifter. Om du väljer det här alternativet innebär det att serviceprisjusteringen bara utförs om det totala priset är lägre än det belopp som anges i serviceprisgruppen.|  
  
## <a name="see-also"></a>Se även  
[Registrera prissättning och alternativa kostnader för tjänster](service-how-setup-service-costs-pricing.md)  
[Ställa in tjänstehantering](service-setup-service.md)  


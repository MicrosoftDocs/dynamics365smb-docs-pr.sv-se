---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
När du tar emot en faktura från ett företag i en utländsk valuta är det ganska enkelt att beräkna det lokala valutavärdet (BVA) på fakturan baserat på dagens valutakursbelopp. Fakturan levereras emellertid ofta med betalningsvillkor så att du kan försena betalningen till ett senare datum, vilket innebär en potentiellt annorlunda valutakurs. Det här problemet är i kombination med det faktum att bankens valutakurser alltid skiljer sig från de officiella valuta kurserna, vilket gör det omöjligt att förutsäga det exakta belopp i lokal valuta (BVA) som krävs för att täcka fakturan. Om fakturans förfallo datum gäller till nästa månad måste du kanske också revaluate beloppet i den lokala valutan (BVA) i slutet av månaden. Valuta justeringen är nödvändig eftersom det nya BVA-värdet som krävs för att täcka faktura beloppet kan vara ett annat, och företagets skuld till leverantören kan ha ändrats. Det nya beloppet i BVA kan vara högre eller lägre än det föregående beloppet och kommer därför att utgöra en vinst eller en förlust. Men eftersom fakturan ännu inte har betalats betraktas vinsten eller förlusten som *Orealiserad*. Senare betalas fakturan och banken har returnerat den faktiska valutakursen för betalningen. Det är inte förrän nu den *realiserade* vinsten eller förlusten beräknas. Den här orealiserade vinsten eller förlusten återförs sedan och den realiserade vinsten eller förlusten bokförs i stället.

I följande exempel inlevereras en faktura den 1 januari med valutabeloppet 1 000. När valutakursen är 1,123.

|Datum|Åtgärd|Valutabelopp|Dokumentkurs|BVA-belopp på dokument|Justeringskurs|Okonstaterat vinstbelopp|Betalningskurs|Konstaterat förlustbelopp|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fakturera**|1000|1,123|1123|||||
|1/31|**Justering**|1000||1125|1,125|2|||
|2/15|**Justeringsåterföring vid betalning**|1000||||-2|||
|2/15|**Betalning**|1000||1120|||1,120|-3|

I slutet av månaden utförs en valutajustering där den justerade valutakursen har angetts till 1,125, vilket utlöser en orealiserad vinst på 2.

Vid tidpunkten för betalningen visar den faktiska valutakurs som registrerats i banktransaktionen en valutakurs på 1,120.

Här finns en orealiserad transaktion som därför kommer att återföras tillsammans med betalningen.

Slutligen registreras betalningen och den faktiska förlusten bokförs i kontot för konstaterade förluster.

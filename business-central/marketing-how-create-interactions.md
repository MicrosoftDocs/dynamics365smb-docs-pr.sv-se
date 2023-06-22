---
title: Så här skapar du interaktioner på kontakter och segment
description: 'Beskriver hur du kan skapa interaktioner för den kommunikation som du har med dina kontakter och segment i Business Central, till exempel direktmail.'
documentationcenter: ''
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="create-interactions-on-contacts-and-segments" />Så här skapar du interaktioner på kontakter och segment
Du kan skapa interaktioner för att registrera all interaktion och kommunikation som du har med dina kontakter och segment, till exempel direktreklam.

Innan du skapar interaktioner måste du lägga upp interaktionsmallar. Mer information finns i  [Skapa interaktionsmallar](marketing-interactions.md).

## <a name="to-create-an-interaction" />Skapa interaktioner så här
1. Öppna kontakten, säljaren eller interaktionsloggtransaktionen.
2. Välj åtgärden **Skapa interaktion**.
3. Fyll i fälten och välj sedan knappen **OK**.

> [!NOTE]  
>   Om du behöver göra något annat aktivitet i **Avbryt** innan du avslutar interaktionen, kan du avsluta guiden och välja om du vill avsluta interaktionen senare. Detta senarelägger interaktionen.

## <a name="to-finish-and-delete-postponed-interactions" />Så här slutför du och tar bort senarelagda åtgärder
1. Öppna kontakten, säljaren eller interaktionsloggtransaktionen.
2. Välj **Senarelagda interaktioner**.
3. Markera den åtgärd som du vill slutföra och klicka på åtgärden **Fortsätt**.

## <a name="to-create-an-interaction-on-a-segment" />Så här skapar du interaktioner för segment
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Segment** och väljer sedan relaterad länk.
2. På sidan **Segment**, i avsnittet **Interaktion**, fyller du i fälten för att specificera vilken interaktion som du vill tilldela segmentet.

    När du har tilldelat segmentet en interaktion kan du anpassa interaktionen till respektive kontakt i segmentet, exempelvis genom att välja en annan interaktionsmall på raderna på sidan **Segment**.  
3. För att logga segmentet och interaktionerna väljer du åtgärden **Logg**. Sidan **Loggsegment** öppnas.
4. Om du vill skapa ett nytt segment med samma kontakter markerar du kryssrutan **Skapa uppföljningssegment**. Innan ett uppföljningssegment kan skapas måste du ange en nummerserie för segment på sidan **Affärsstödsinställning**.

Interaktionen registreras för varje kontakt i segmentet i tabellen **Interaktion loggtrans.** och segmentet loggas. Loggade segment återfinns på sidan **Segmentlogg**.

Om du har markerat kryssrutan **Skapa uppföljningssegment** skapas automatiskt ett nytt segment med samma kontakter som det segment som du precis har loggat.

## <a name="see-also" />Se även
[Registrera interaktioner](marketing-interactions.md)  
[Hantera kontakter](marketing-contacts.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Skapa interaktioner i kontakter och segment
description: Lär dig skapa interaktioner i Business Central för den kommunikation som du har med dina kontakter och segment.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.reviewer: ivkoleti
ms.date: 12/13/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5077, 5078, 5074, 5076, 5186, 5075, 5079'
---
# Skapa interaktioner i kontakter och segment

Du kan skapa interaktioner för att spåra den kommunikation du har med en enda kontakt eller med flera kontakter i dina segment. Om du vill göra det enkelt att skapa interaktioner tillhandahåller [!INCLUDE [prod_short](includes/prod_short.md)] den assisterade konfigurationsguiden **Skapa interaktion**. Denna guide hjälper dig att överföra viktiga detaljer om interaktionen.

Innan du skapar interaktioner måste du emellertid konfigurera interaktionsmallar. Mer information om interaktionsmallar finns på [Konfigurera interaktionsmallar](marketing-interactions.md).

## För att skapa en interaktion med en kontakt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Kontakter**, **Säljare** eller **Interaktion loggtrans.** och väljer sedan tillhörande länk.
2. Välj åtgärden **Skapa interaktion**.
3. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Om du behöver avbryta innan du är klar med interaktionen kan du välja **Avbryt** och sedan ange om du vill spara inställningarna så att du kan fortsätta senare. Mer information om senarelagda interaktioner finns i [Så här konfigurerar du en senarelagd interaktion](#to-finish-setting-up-a-postponed-interaction).

## Så här skapar du interaktioner för segment

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Segment** och väljer sedan relaterad länk.
2. Välj åtgärden **Skapa interaktion**.
3. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> När du har tilldelat en interaktion till ett segment finns det flera andra åtgärder som du kan vidta på sidan **Segment**:
>
> * Anpassa interaktionen efter respektive kontakt i segmentet, exempelvis genom att välja en annan interaktionsmall på raderna.  
>* Logga segmentet och interaktionerna genom att välja åtgärden **Logg** för att öppna sidan **Loggsegment**.
> * Skapa ett nytt segment med samma kontakt genom att välja kryssrutan **Skapa uppföljningssegment**. Denna inställning kräver att en nummerserie har angetts för segment på sidan **Marknadsföringsinställningar**.

Interaktionen registreras för varje kontakt i segmentet i tabellen **Interaktion loggtrans.** och segmentet loggas. Loggade segment finns på sidan **Loggad segment**.

## Så här slutför du konfigurationen av en senarelagd interaktion

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Senarelagda interaktioner** och väljer sedan relaterad länk.
2. Välj den interaktion som du vill slutföra och klicka på åtgärden **Fortsätt**.

## Se även

[Registrera interaktioner](marketing-interactions.md)  
[Hantera kontakter](marketing-contacts.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
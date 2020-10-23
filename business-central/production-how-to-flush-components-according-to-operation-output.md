---
title: Bokföra komponenter utifrån operationens utflöde | Microsoft Docs
description: För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**. Mer information finns i  Bokföringsmetod.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 366c450924367ba70eece30809035895c42a0838
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921623"
---
# <a name="flush-components-according-to-operation-output"></a>Bokföra komponenter utifrån verksamhetens utflöde
För artiklar, som har upprättats med bokföringsmetoden Bakåt, är standarden att beräkna och bokföra komponentförbrukning när du ändrar produktionsorderstatusen från släppt till **Färdig**.  

Om du definierar verksamhetsföljdslänkkoder också utförs beräkning och bokföring när varje operation har slutförts, och antal, som faktiskt förbrukades i operationen, bokförs. Mer information finns i [Skapa verksamhetsföljder](production-how-to-create-routings.md).  

Om t.ex. en produktionsorder för att kunna producera 800 meter kräver 8 kg av en komponent så, när du bokför 200 meter som utflöde, bokförs 2 kg automatiskt som förbrukning.  

Den här funktionen är användbar för följande:  

-   **Lagervärdering** - värdetransaktioner för förbrukning och utflöde har skapats parallellt, i takt med att produktionsordern fortskrider. Utan verksamhetsföljdslänkkoder minskar lagervärdet när utflödet bokförs och ökar sedan vid en senare tidpunkt, när värdet för komponentförbrukning bokförs tillsammans med färdig produktionsorder.  
-   **Lagerdispositionen** - med tidsfasad förbrukningsbokföring, är tillgängligheten till komponentartiklarna mer uppdaterad, vilket är viktigt för att underhålla det interna saldot mellan tillgång och efterfrågan. Utan verksamhetsföljdslänkkoder kan andra behov av komponenten tro att den är tillgänglig så länge det finns en väntande försenad förbrukningsbokföring.  
-   **JIT** – med möjligheten att anpassa produkter till pågående kundförfrågningar kan du reducera kassation genom att se till att arbets- och systemändringar endast görs när det behövs.  

Följande procedur visar hur kopplingskoder för bokföring bakåt och rörelsekostnad kan kombineras så att antalet som bokföras per operation, är proportionell till det faktiska utflödet av operationen.  

## <a name="to-flush-components-according-to-operation-output"></a>Bokföra komponenter utifrån operationens utflöde  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Välj åtgärden **Redigera**.  
3.  På snabbfliken **Återanskaffning**, i fältet **Bokföringsmetod**, markera **framåt**.  

    > [!NOTE]  
    >  Välj **Plocka + framåt** om komponenten ska användas på ett lagerställe som har skapats för dirigerad artikelinförsel och plockning.  

4.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **verksamhetsföljder** och välj sedan relaterad länk.  
5.  Definiera verksamhetsföljdslänkkoder för varje operation som förbrukar komponenten. Mer information finns i [Skapa verksamhetsföljder ](production-how-to-create-routings.md).  
6.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Prod.struktur** och välj sedan relaterad länk.  
7.  Definiera verksamhetsföljdslänkkoder från varje instans av komponenten till operationen där den förbrukas.

    > [!IMPORTANT]  
    >  Komponenten måste ha en verksamhetsföljdlänk till den sista operationen i verksamhetsföljden.  

## <a name="see-also"></a>Se även  
[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planerad](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

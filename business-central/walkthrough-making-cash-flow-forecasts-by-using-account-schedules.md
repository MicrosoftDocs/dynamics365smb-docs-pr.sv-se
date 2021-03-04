---
title: 'Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar | Microsoft Docs'
description: Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser. Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden. I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a210792a187bde0217917659f118c58a6a135df2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756547"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar
Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser. Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden. I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
I den här genomgången tas följande aktiviteter upp:  

- Lägga upp ett nytt namn för kassaflödeskontouppställningen.  
- Skapa kontouppställningsrader.  
- Lägga upp en ny kolumnlayout.  
- Koppla en kolumnlayout till en kontouppställning.  
- Visa och skriva ut kassaflödesprognosen.  

### <a name="prerequisites"></a>Förutsättningar  
För att kunna utföra den här genomgången behöver du:  

- [!INCLUDE[prod_short](includes/prod_short.md)] installerad.  
- Kassaflödeskalkylarksraderna är bokförda.  

## <a name="roles"></a>Roller  
Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroll:  

- Controller  

## <a name="story"></a>Situation  
Ken är controller på CRONUS som varje månad gör kassaflödesprognoser. Han tar med ekonomi, försäljning, inköp och anläggningstillgångar i prognosen, och sedan visar han den till Sara som är ekonomichef.  

## <a name="setting-up-a-new-account-schedule-name"></a>Lägga upp ett nytt kontouppställningsnamn  
En kontouppställning består av ett kontouppställningsnamn för kassaflöde med en serie rader och en kolumnlayout.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Så här skapar du ett nytt kontouppställningsnamn  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontoscheman** och välj sedan relaterad länk.  
2.  På sidan **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn för kassaflöde.  
3.  I fältet **Namn** anger du **Prognos**.  
4.  I fältet **Beskrivning**, ange **Kassaflödesprognos**.  
5.  Lämna fälten **Standard kolumnlayout** och **Analysvynamn** tomma.  

## <a name="setting-up-account-schedule-lines"></a>Skapa kontouppställningsrader  
När ett kontouppställningsnamn har upprättats, definierar Ken varje rad som visas i kontouppställningen för kassaflödet. Ken definierar rader som kan visas i rapporter förutom rader som bara används vid beräkning.  

### <a name="to-set-up-account-schedule-lines"></a>Så här skapar du kontouppställningsrader  

1.  På sidan **Kontouppställningsnamn** väljer du det nya kontouppställningsnamnet **Prognos** som du har skapat och väljer sedan åtgärden **Redigera kontouppställning**.  
2.  På sidan **Kontouppställning** anger du varje rad exakt som det visas i följande tabell.  

    > [!NOTE]  
    >  Med hjälp av funktionen **Infoga kassaflödeskonton** kan du snabbt välja kassaflödeskonton från kontoplanen för kassaflöde och kopiera dem till kontouppställningsrader.  

    |Rad-nr|Beskrivning|Summeringstyp|Summeringsintervall|Radtyp|Beloppstyp|Visa|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |C10|Belopp|Nettoförändring|Transaktioner|Nettobelopp|Alltid|  
    |C20|Belopp till datum|Saldo t.o.m. datum|Transaktioner|Nettobelopp|Alltid|  
    |C30|Hela räkenskapsåret|Hela räkenskapsåret|Transaktioner|Nettobelopp|Alltid|  

4.  Välj **OK**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Koppla kolumnlayouten till kontouppställningsnamnet  
Nu kan Ken koppla kolumnlayouten till kontouppställningsnamnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Så här kopplar du kolumnlayouten till kontouppställningsnamnet  

1.  På sidan **Kontouppställningsnamnet** väljer du **Prognos** i fältet **Namn**.  
2.  I fältet **Standard kolumnlayout**, välj kolumnlayouten **Kassaflöde** som standardkolumnlayout.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Så här visar och skriver du ut kassaflödesprognosen  
1.  På sidan **Kontouppställningsnamn** väljer du åtgärden **Översikt** för att visa kassaflödesprognosen.  
2.  På sidan **Kontouppställning översikt** kan du ange ett belopp och sedan visa transaktionerna i kassaflödesprognosen som utgör beloppet. Dessutom kan du visa formeln som används för att beräkna beloppet. Du kan också filtrera beloppen efter datum och dimension.  
3.  Välj åtgärden **Skriv ut** när du vill skriva ut kassaflödesprognosen.  

## <a name="see-also"></a>Se även  
 [Arbeta med kontouppställningar](bi-how-work-account-schedule.md)   
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
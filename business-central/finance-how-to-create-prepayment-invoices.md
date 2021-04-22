---
title: Så här skapar du förskottsfakturor | Microsoft Docs
description: Mer information om hur du hanterar situationer där du eller leverantören kräver förskottsbetalning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 72a073fcde9ddf20df7c138ab544afb6719b93ce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782169"
---
# <a name="create-prepayment-invoices"></a>Skapa förskottsfakturor

Om du kräver att dina kunder betalar innan du levererar en order till dem kan du använda funktionen för förskottsbetalning. Detsamma gäller om leverantören kräver att du betalar innan han/hon levererar en order till dig.  

När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura. Om du har en standardprocentandel för förskottsbetalning för kunden eller leverantören tas den automatiskt med i den resulterande förskottsfakturan. Du kan också ange en procentandel för förskottsbetalning för hela dokumentet.

När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura. Du kan använda standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs. Till exempel, en totalsumma för hela ordern.  

I följande procedur beskrivs hur du fakturerar en förskottsbetalning för en försäljningsorder. Momenten är liknande för en inköpsorder.  

## <a name="to-create-a-prepayment-invoice"></a>Så här skapar du en förskottsfaktura

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan tillhörande länk.  
2. Skapa en ny försäljningsorder för relevant kund. Mer information finns i [Sälja produkter](sales-how-sell-products.md).  

    På snabbfliken **Förskottsbetalning** i fältet **Förskottsbetalning %** anges den procentandel som ska användas för att beräkna förskottsbeloppet. Om det finns en standardprocentandel på kundkortet fylls fältet i automatiskt. Du kan ändra procentandelen. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Välj fältet **Komprimera förskottsbetalning** om du vill skapa rader på den förskottsfaktura som kombinerar rader från försäljningsordern om:  

    - De har samma redovisningskonto för förskottsbetalningar, enligt de allmänna bokföringsinställningarna.  
    - De har samma dimensioner.  

    Låt fältet vara tomt om du vill skapa en förskottsfaktura med en rad för varje försäljningsorderrad som det finns en procentandel för förskottsbetalning för, välj då inte fältet **Komprimera förskottsbetalning**.  

    Förfallodatumet för förskottsbetalningen beräknas automatiskt baserat på värdet i fältet **Betalningsvillkorskod för förskottsbetalning**.

3. Fyll i försäljningsraderna.  

    Om du har angett en standard procentandel för förskottsbetalning för kunden eller på snabbfliken **förskottsbetalning** i det här dokumentet kopieras det här värdet till varje rad. Du kan ändra innehållet i fältet **Förskottsbetalning %** på raden.  

4. Visa det totala förskottsbeloppet genom att välja åtgärden **statistik**.

    Om du vill justera det totala förskottsbetalningsbeloppet för ordern kan du ändra innehållet i fältet **Förskottsbetalningsbelopp** på sidan **Förs.orderstatistik**.  

    Om fältet **Priser inkl. moms** är markerat, kan fältet **Förskottsbetalningsbelopp inkl moms** redigeras  

    Om du ändrar innehållet i fältet **Förskottsbetalningsbelopp** fördelas beloppet proportionellt på alla rader, förutom på de rader där värdet **0** i fältet **Förskottsbetalning %**.  

5. Du skriver ut en testrapport innan du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan välja åtgärden **Testrapport för förskottsbetalning**.  
6. Du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan åtgärden **Bokför förskottsfaktura**.  

    Om du vill bokföra och skriva ut förskottsfakturan väljer du åtgärden **Bokför och skriv ut faktura på förskottsbet.**.  

Du kan skicka ut ytterligare förskottsfakturor för ordern. Om du vill göra detta höjer du förskottsbetalningsbeloppet på minst en rad, justerar dokumentdatumet om det behövs och bokför sedan förskottsfakturan. En ny faktura skapas för skillnaden mellan de förskottsbetalningsbelopp som hittills har fakturerats och det nya förskottsbetalningsbeloppet.  

> [!NOTE]  
> Om du befinner dig i Nordamerika kan ändra du inte procentandelen för förskottsbetalning när förskottsfakturan har bokförts. Detta förhindras i den amerikanska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] eftersom beräkning av moms på annat sätt blir felaktiga.  

 När du vill bokföra resten av fakturan bokför du den som en vanlig faktura. Förskottsbetalningsbeloppet dras automatiskt av från beloppet som ska betalas.  

## <a name="see-also"></a>Se även

[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
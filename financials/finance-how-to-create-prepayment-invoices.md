---
title: "Så här skapar du förskottsfakturor | Microsoft Docs"
description: "Mer information om hur du hanterar situationer där du eller leverantören kräver förskottsbetalning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd090720943d0d7271200e087642a80157cbdbbd
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="create-prepayment-invoices"></a>Skapa förskottsfakturor
Om du vill att dina kunder ska betala innan du levererar en order till dem eller om en leverantör kräver att du betalar innan de levererar en order till dig, kan du använda funktionen för förskottsbetalning.  

När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura. Du kan använda standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs. Till exempel, en totalsumma för hela ordern.  

I följande procedur beskrivs hur du fakturerar en förskottsbetalning för en försäljningsorder. Momenten är liknande för en inköpsorder.  

## <a name="to-create-a-prepayment-invoice"></a>Så här skapar du en förskottsfaktura  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Skapa en ny försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).  

    På snabbfliken **Förskottsbetalning** fylls fältet **Förskottsbetalning %** fylls i automatiskt om det finns en standardprocentandel för förskottsbetalning på kundkortet. Du kan ändra innehållet i fältet. Procentandelen för förskottsbetalning kopieras bara från huvudet till de rader där standardprocentandelen inte kopieras från artikeln.  

    Om fältet **Komprimera förskottsbetalning** är markerat kombineras rader på fakturan om:  
    - De har samma redovisningskonto för förskottsbetalningar, enligt de allmänna bokföringsinställningarna.  
    - De har samma dimensioner.  

    Låt fältet vara tomt om du vill skapa en förskottsfaktura med en rad för varje försäljningsorderrad som det finns en procentandel för förskottsbetalning för.  

3. Fyll i försäljningsraderna.  

    Om standardprocentandelar för förskottsbetalning har angetts för artiklarna kopieras de automatiskt till fältet **Förskottsbetalning %** på raden. Annars kopieras den förskottsbetalda procentandelen från huvudet. Du kan ändra innehållet i fältet **Förskottsbetalning %** på raden.  
4. Om du vill koppla en procentandel för förskottsbetalning till hela ordern ändrar du fältet **Förskottsbetalning %** i huvudet när du har fyllt i raderna.  
5. Visa det totala förskottsbeloppet genom att välja åtgärden **statistik**.

    Om du vill justera det totala förskottsbetalningsbeloppet för ordern kan du ändra innehållet i fältet **Förskottsbetalningsbelopp** i fönstret **Förs.orderstatistik**.  

    Om fältet **Priser inkl. moms** är markerat, kan fältet **Förskottsbetalningsbelopp inkl moms** redigeras  

    Om du ändrar innehållet i fältet **Förskottsbetalningsbelopp** fördelas beloppet proportionellt på alla rader, förutom på de rader där värdet **0** i fältet **Förskottsbetalning %**.  
6. Du skriver ut en testrapport innan du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan välja åtgärden **Testrapport för förskottsbetalning**.  
7. Du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan åtgärden **Bokför förskottsfaktura**.  

    Om du vill bokföra och skriva ut förskottsfakturan väljer du åtgärden **Bokför och skriv ut faktura på förskottsbet.**.  

Du kan skicka ut ytterligare förskottsfakturor för ordern. Om du vill göra detta höjer du förskottsbetalningsbeloppet på minst en rad, justerar dokumentdatumet om det behövs och bokför sedan förskottsfakturan. En ny faktura skapas för skillnaden mellan de förskottsbetalningsbelopp som hittills har fakturerats och det nya förskottsbetalningsbeloppet.  

> [!NOTE]  
>  Om du befinner dig i Nordamerika kan ändra du inte procentandelen för förskottsbetalning när förskottsfakturan har bokförts. Detta förhindras i den amerikanska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] eftersom beräkning av moms på annat sätt blir felaktiga.  

 När du vill bokföra resten av fakturan bokför du den som en vanlig faktura. Förskottsbetalningsbeloppet dras automatiskt av från beloppet som ska betalas.  

## <a name="see-also"></a>Se även  
[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
title: "Konfigurerar standardrader för återkommande försäljning och inköp | Microsoft Docs"
description: "Du kan definiera försäljningsrader och inköpsrader som du gör ofta och infoga dem på försäljnings- och inköpsdokument för att snabbt fylla i raderna med standardinformationen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Skapa återkommande försäljnings- och inköpsrader
Om du ofta behöver skapa försäljnings- och inköpsrader med liknande information, kan du ställa in standardraderna så att du sedan kan infoga på återkommande försäljning och inköpsdokument, till exempel för återkommande påfyllningsorder.  

I följande procedur beskrivs hur du arbetar med in standardförsäljningsrader. Det fungerar på liknande sätt för standardstandardinköpsrader.  

## <a name="to-set-up-standard-sales-lines"></a>Så här skapar du standardförsäljningsrader  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Standard förs.rader** och välj sedan relaterad länk.  
2. I fönstret **Standard förs.rader** väljer du åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I snabbfliken **Rader** ange information i fälten för att förbereda försäljningsrader som återspeglar de standardrader som du förväntar dig att använda som återkommande rader på försäljningsdokument.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Infoga standardförsäljningsrader i en försäljningsfaktura
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Fakturor** och välj sedan relaterad länk.
2. Öppna den försäljningsfaktura du vill infoga en eller flera standardförsäljningsrader på.
3. Välj åtgärden **få återkommande förs.rader**.
4. I fönstret **återkommande försäljningsrader** välj sökknappen i fältet **kod** och välj sedan en uppsättning standardförsäljningsrader.

    > [!NOTE]
    > För att använda återkommande rader tillsammans med batch-jobbet **Skapa återkommande fakturor** måste du även fylla i fälten **Giltigt från den** och **Giltigt till den** fönstret **återkommande försäljningsrader**. För mer information, se Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder.

5. Välj **OK** för att infoga standardförsäljningsraderna på fakturan, där du kan använda eller redigera informationen.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder
Du kan använda batch-jobbet **Skapa återkommande försäljningsfakt.** för att skapa försäljningsfakturor enligt standardförsäljningsrader som tilldelats till kunderna och med bokföringsdatum som infaller inom de giltighetsdatum som du anger på standardförsäljningsraden.

> [!NOTE]
> I fönstret **Återkommande försäljningsrader** kan du också ange en metod för autogirobetalning och medgivande för autogiro. De försäljningsfakturor som skapas med batch-jobbet **Skapa återkommande försäljningsfakt.** tar sedan med information som krävs för att kräva betalning för försäljningsfakturorna med SEPA-autogiro. Mer information finns i [Kräva in betalningar med SEPA direktdebitering](finance-collect-payments-with-sepa-direct-debit.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Skapa återkommande försäljningsfakturor** och välj sedan relaterad länk.
2. I fönstret **Skapa återkommande försäljningsfakt.** fyller du i de fälten efter behov.
3. I fältet **kod**filter anger du koden för standardförsäljningsrader som tilldelats kunden som du vill skapa fakturor för.
4. Välj **OK**.

Fakturor skapas för kunder med den angivna standardkundförs.koden och angiven information om direktdebitering, för bokföring på det angivna datumet.

## <a name="see-also"></a>Se även  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


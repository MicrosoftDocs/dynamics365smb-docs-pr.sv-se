---
title: Konfigurerar standardrader för återkommande försäljning och inköp | Microsoft Docs
description: Du kan definiera försäljningsrader och inköpsrader som du gör ofta och infoga dem på försäljnings- och inköpsdokument för att snabbt fylla i raderna med standardinformationen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a85fb48251d5c1465dcd4be7aaf868d857a07fd4
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311962"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Skapa återkommande försäljnings- och inköpsrader
Om du ofta behöver skapa försäljnings- och inköpsrader med liknande information, kan du ställa in standardraderna så att du sedan kan infoga på återkommande försäljning och inköpsdokument, till exempel för återkommande påfyllningsorder.  

I följande procedur visas hur du arbetar med in standardförsäljningsrader på en försäljningsfaktura. Den fungerar på ungefär samma sätt för alla andra försäljningsdokument och för alla inköpsdokument.  

## <a name="to-set-up-standard-sales-lines"></a>Så här skapar du standardförsäljningsrader  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Standard förs.rader** och välj sedan relaterad länk.  
2. På sidan **Standard förs.rader** väljer du åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I snabbfliken **Rader** ange information i fälten för att förbereda försäljningsrader som återspeglar de standardrader som du förväntar dig att använda som återkommande rader på försäljningsdokument.  

> [!NOTE]
> Du kan inte definiera priser på standardförsäljningsrader eftersom priser, rabatter och så vidare beräknas på de faktiska försäljningsdokument när du infogar standardförsäljningsraderna.

## <a name="to-assign-standard-sales-lines-to-a-customer"></a>Så här tilldelar du standardförsäljningsrader till kunder
Tilldela en eller flera standardförsäljningsrader till en kund, så att de blir tillgängliga att infoga i försäljningsdokument för kunden.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kunder** och välj sedan relaterad länk.
2. Öppna kortet för ett relevant kund.
3. Välj åtgärden **Få återkommande förs.rader**.
4. På sidan **Återkommande försäljningsrader**, välj koderna för återkommande försäljningsrader som du vill infoga i ett försäljningsdokument för kunden.
5. Fyll i ytterligare fält för att definiera när, hur och var återkommande försäljningsraderna ska användas.
6. I de fyra fälten där du väljer hur raderna infogas på fyra typer av dokument, väljer du ett av följande alternativ:

|Alternativ|Beskrivning|
|-|-|
|**Manuell**|Du måste manuellt söka efter och markera en återkommande försäljningsrad för kunden.|
|**Automatiskt**|Om det finns flera återkommande försäljningsrader för kunden, får du ett meddelande där du kan välja vilken som ska infogas. Om det bara finns en återkommande försäljningsrad kommer den att infogas automatiskt.<br /><br />Observera att detta endast fungerar om det nya dokumentet har skapats från en dokumentlista, t.ex. genom att välja ny åtgärd **Ny** på sidan **Försäljningsorder**. Det fungerar inte om dokumentet har skapats från ett kundkort, till exempel.|
|**Fråga alltid**|Ett meddelande visas och alla befintliga återkommande försäljningsrader visas så att du kan välja ett.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>För att infoga återkommande försäljningsrader i en försäljningsfaktura
Om det finns återkommande försäljningsrader för kunden, kan du infoga dem i alla typer av försäljningsdokument, t.ex. en försäljningsfaktura. Om du har aktiverat det aktuella meddelandet får du information om återkommande försäljningsrader finns.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Fakturor** och välj sedan relaterad länk.
2. Öppna den försäljningsfaktura du vill infoga en eller flera standardförsäljningsrader på.
3. Välj åtgärden **få återkommande förs.rader**.
4. På sidan **återkommande försäljningsrader** välj sökknappen i fältet **kod** och välj sedan en uppsättning standardförsäljningsrader.

    > [!NOTE]
    > För att använda återkommande rader tillsammans med batch-jobbet **Skapa återkommande fakturor** måste du även fylla i fälten **Giltigt från den** och **Giltigt till den** på sidan **återkommande försäljningsrader**. För mer information, se [Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Välj **OK** för att infoga standardförsäljningsraderna på fakturan, där du kan använda eller redigera informationen.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder
Du kan använda batch-jobbet **Skapa återkommande försäljningsfakt.** för att skapa försäljningsfakturor enligt standardförsäljningsrader som tilldelats till kunderna och med bokföringsdatum som infaller inom de giltighetsdatum som du anger på standardförsäljningsraden.

> [!NOTE]
> På sidan **Återkommande försäljningsrader** kan du också ange en metod för autogirobetalning och medgivande för autogiro. De försäljningsfakturor som skapas med batch-jobbet **Skapa återkommande försäljningsfakt.** tar sedan med information som krävs för att kräva betalning för försäljningsfakturorna med SEPA-autogiro. Mer information finns i [kräva in betalningar med SEPA direktdebitering](finance-collect-payments-with-sepa-direct-debit.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Skapa återkommande försäljningsfakturor** och välj sedan relaterad länk.
2. På sidan **Skapa återkommande försäljningsfakt.** fyller du i de fälten efter behov.
3. I fältet **kod**filter anger du koden för standardförsäljningsrader som tilldelats kunden som du vill skapa fakturor för.
4. Välj **OK**.

Fakturor skapas för kunder med den angivna standardkundförs.koden och angiven information om direktdebitering, för bokföring på det angivna datumet.

## <a name="see-also"></a>Se även  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

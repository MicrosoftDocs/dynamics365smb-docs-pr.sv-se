---
title: Konfigurerar standardrader för återkommande försäljning och inköp | Microsoft Docs
description: Du kan definiera försäljningsrader och inköpsrader som du gör ofta och infoga dem på försäljnings- och inköpsdokument för att snabbt fylla i raderna med standardinformationen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 05/25/2020
ms.author: sgroespe
ms.openlocfilehash: 4da1195333f6b36866f55ee02123f75df4778de0
ms.sourcegitcommit: d4a77522859c5561c1f3dc43178d45657ffa31b5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/26/2020
ms.locfileid: "3402565"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Skapa återkommande försäljnings- och inköpsrader
Om du ofta behöver skapa försäljnings- och inköpsrader med liknande information, kan du ställa in standardraderna så att du sedan kan infoga på återkommande försäljning och inköpsdokument, till exempel för återkommande påfyllningsorder.  

I följande procedur visas hur du arbetar med in standardförsäljningsrader på en försäljningsfaktura. Den fungerar på ungefär samma sätt för alla andra försäljningsdokument och för alla inköpsdokument.  

## <a name="to-set-up-recurring-sales-lines"></a>Så här skapar du återkommande försäljningsrader

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Återkommande försäljningsrader** och välj sedan relaterad länk.  
2. På sidan **Återkommande försäljningsrader** väljer du åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I snabbfliken **Rader** ange information i fälten för att förbereda försäljningsrader som återspeglar de standardrader som du förväntar dig att använda som återkommande rader på försäljningsdokument.  

> [!NOTE]
> Du kan inte definiera priser på återkommande standardförsäljningsrader eftersom priser, rabatter och så vidare beräknas på de faktiska försäljningsdokumenten när du infogar återkommande standardförsäljningsrader.

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Så här tilldelar du återkommande försäljningsrader till kunder

Tilldela en eller flera återkommande försäljningsrader till en kund så att dessa kan läggas in i försäljningsdokument för kunden.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kortet för ett relevant kund.
3. Välj åtgärden **Få återkommande förs.rader**.
4. På sidan **Återkommande försäljningsrader**, välj koderna för återkommande försäljningsrader som du vill infoga i ett försäljningsdokument för kunden.
5. Fyll i ytterligare fält för att definiera när, hur och var återkommande försäljningsraderna ska användas.  

    Om du tänker använda återkommande försäljningsrader tillsammans med batchjobbet **Skapa återkommande färsäljningsfakturor** använder du fälten **Giltigt från den** och **Giltigt till den** för att begränsa perioden då de återkommande försäljningsraderna används för att skapa fakturor. För mer information, se [Så här: skapa flera försäljningsfakturor utifrån standardförsäljningskoder](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Du kan också ange ett betalningssätt för autogirobetalning och medgivande för autogiro. De försäljningsfakturor som skapas med batch-jobbet **Skapa återkommande försäljningsfakturor** omfattar sedan den information som krävs för att kräva betalning med SEPA-autogiro. Mer information finns i [kräva in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md).

6. I de fyra fälten där du väljer hur raderna infogas på fyra typer av dokument, väljer du ett av följande alternativ:

|Alternativ|Beskrivning|
|------|-----------|
|**Manuell**|Du måste manuellt söka efter och markera en återkommande försäljningsrad för kunden.|
|**Automatiskt**|Om det finns flera återkommande försäljningsrader för kunden, får du ett meddelande där du kan välja vilken som ska infogas. Om det bara finns en återkommande försäljningsrad kommer den att infogas automatiskt.<br /><br />Observera att detta endast fungerar om det nya dokumentet har skapats från en dokumentlista, t.ex. genom att välja ny åtgärd **Ny** på sidan **Försäljningsorder**. Det fungerar inte om dokumentet har skapats från ett kundkort, till exempel.|
|**Fråga alltid**|Ett meddelande visas och alla befintliga återkommande försäljningsrader visas så att du kan välja ett.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>För att infoga återkommande försäljningsrader i en försäljningsfaktura

Om det finns återkommande försäljningsrader för kunden kan du infoga dem (eller få dem infogade) i alla typer av försäljningsdokument, t.ex. en försäljningsfaktura. Om du har aktiverat alternativen **Fråga alltid** får du information om återkommande försäljningsrader finns.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Fakturor** och välj sedan relaterad länk.
2. Öppna den försäljningsfaktura du vill infoga en eller flera standardförsäljningsrader på.
3. Välj åtgärden **få återkommande förs.rader**.
4. På sidan **återkommande försäljningsrader** välj sökknappen i fältet **kod** och välj sedan en uppsättning standardförsäljningsrader.
5. Välj **OK** för att infoga standardförsäljningsraderna på fakturan, där du kan använda eller redigera informationen.

## <a name="to-create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Skapa flera försäljningsfakturor utifrån återkommande försäljningsrader
Du kan använda batch-jobbet **Skapa återkommande försäljningsfakt.** för att skapa försäljningsfakturor enligt standardförsäljningsrader som tilldelats till kunderna och med bokföringsdatum som infaller inom de giltighetsdatum som du anger på standardförsäljningsraden.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Skapa återkommande försäljningsfakturor** och välj sedan relaterad länk.
2. På sidan **Skapa återkommande försäljningsfakt.** fyller du i de fälten efter behov.
3. I fältet **kod** filter anger du koden för standardförsäljningsrader som tilldelats kunden som du vill skapa fakturor för.
4. Välj **OK**.

Fakturor skapas för kunder med den angivna standardkundförs.koden och angiven information om direktdebitering, för bokföring på det angivna datumet.

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

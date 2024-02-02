---
title: Återkommande standardinköpsrader
description: Ställ in ofta använda inköpsrader och inköpsrader för att infoga dem på inköpsdokument och snabbt fylla i raderna med standardinformationen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-recurring-purchase-lines"></a>Skapa återkommande inköpsrader

Om du ofta behöver skapa inköpsrader med liknande information, kan du ställa in standardraderna så att du sedan kan infoga på återkommande inköpsdokument, till exempel för återkommande påfyllningsorder.

## <a name="set-up-recurring-purchase-lines"></a>Ställ in återkommande inköpsrader

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **återkommande inköpsrader** och väljer sedan relaterad länk.
2. På sidan **Återkommande inköpsrader** väljer du åtgärden **Ny**.
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I snabbfliken **Rader** ange information i fälten som återspeglar de standardrader som du förväntar dig att använda som återkommande rader på inköpsdokument.

> [!NOTE]
> Du kan inte definiera priser på återkommande inköpsrader eftersom priser, rabatter och så vidare beräknas på de faktiska inköpsdokumenten när du infogar återkommande inköpsrader.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-purchase-lines-to-a-vendor"></a>Tilldela en leverantör återkommande inköpsrader

Tilldela en eller flera återkommande inköpsrader till en leverantör så att de är tillgängliga att infoga på inköpsdokument från den leverantören.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna kortet för ett relevant leverantör.
3. Välj åtgärden **Få återkommande inköpsrader**.
4. På sidan **Återkommande inköpsrader**, välj koderna för återkommande inköpsrader som du vill infoga i ett inköpsdokument för leverantören.
5. Fyll i andra fält för att definiera när, hur och var återkommande inköpsraderna ska användas.
6. I de fyra fälten där du väljer hur raderna infogas på fyra typer av dokumenttyp, väljer du ett av följande alternativ:

|Alternativ|Description|
|------|-----------|
|**Manuell**|Du måste manuellt söka efter och markera en återkommande inköpsrad för leverantören.|
|**Automatiskt**|Om det finns flera återkommande inköpsrader för leverantören, får du ett meddelande där du kan välja vilken som ska infogas. Om det bara finns en återkommande inköpsrad kommer den att infogas automatiskt.<br /><br />Detta fungerar endast om det nya dokumentet har skapats från en dokumentlista, t. ex. genom att välja ny åtgärd **Ny** på sidan **Inköpsorder**. Det fungerar inte om dokumentet har skapats från ett leverantörskort, till exempel.|
|**Fråga alltid**|Ett meddelande visas och alla befintliga återkommande inköpsrader visas så att du kan välja ett.

## <a name="insert-recurring-purchase-lines-on-a-purchase-invoice"></a>Så här kan du automatiskt infoga återkommande inköpsrader på en inköpsfaktura

Om det finns återkommande inköpsrader för leverantören kan du infoga dem, eller få dem automatiskt tillagda, på alla typer av inköpsdokument, till exempel en inköpsfaktura. Om du har aktiverat alternativen **Fråga alltid** när du tilldelar återkommande inköpsrader till leverantörer kommer du att informeras om det finns återkommande inköpsrader.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.
2. Öppna den inköpsfaktura du vill infoga en eller flera standardinköpsrader på.
3. Välj åtgärden **få återkommande inköpsrader**.
4. På sidan **återkommande inköpsrader** välj sökknappen i fältet **kod** och välj sedan en uppsättning standardinköpsrader.
5. Välj **OK** för att infoga standardinköpsraderna på fakturan, där du kan använda eller redigera informationen.

## <a name="see-also"></a>Se även

[Inköp](purchasing-manage-purchasing.md)  
[Konfigurera inköp](purchasing-setup-purchasing.md)  
[Skapa återkommande försäljning](sales-how-work-standard-lines.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

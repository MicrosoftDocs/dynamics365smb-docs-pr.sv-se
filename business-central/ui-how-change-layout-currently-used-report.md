---
title: Ändra hur rapporten ska se ut genom att välja en annan layout | Microsoft Docs
description: Du kan använda olika layouter för en rapport och växla mellan layouter för att ändra utseendet på en rapport.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: f24f1cd24a31ddbd0b455b876821ae0173a677c3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249448"
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Ändra den layout som används i en rapport för närvarande
En rapport kan ställas in med fler än en rapportlayout som du kan växla mellan.

Beroende på layouterna som finns tillgängliga för en rapport kan du välja att använda en inbyggd RDLC-rapportlayout, en inbyggd Word-rapportlayout eller en anpassad layout. Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).

> [!TIP]  
> Dokumentrapporter (inte listor) som använder en Word-rapportlayout är vanligtvis snabbare än de med en RDLC-rapportlayout. Om du har möjlighet att välja mellan ett ord eller en RDLC-rapportlayout för en dokumentrapport kan du alltså använda Word-rapportlayouten för bästa prestanda.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Så här ändrar du layout som används i en rapport
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Val av rapportlayout** och välj sedan relaterad länk.  
   Sidan **Val av rapportlayout** visar alla rapporter som är tillgängliga i företaget som har angetts i fältet Företag högst upp på sidan. Fältet Vald layout anger den layout som används i rapporten för närvarande.
2. Ange fältet **Företag** fältet högst upp på sidan till företaget som inkluderar rapporten.
3. I raden för rapporten i listan och anger du fältet **Vald layout** till ett av följande alternativ för att ändra layouten som används för en rapport:
   * RDLC (inbyggd), använder den inbyggda RDLC-rapportlayouten i rapporten.
   * Word (inbyggd), använder den inbyggda Word-rapportlayouten i rapporten.
   * Anpassad använder en anpassad layout i rapporten.  
     Du kan se vilka anpassade layouter som är tillgängliga för rapporten i faktaboxen Rapportlayoutdelar. Om det inte finns några anpassade layouter för rapporten, måste du skapa en först. Om du väljer det här alternativet, gå vidare till nästa procedur för att ange den anpassade layout som du vill använda.

    > [!NOTE]  
    >   Om du väljer **RDLC (inbyggt)** eller **Word (inbyggt)** och du får ett felmeddelande att rapporten inte har en layout för den angivna typen, måste du välja ett annat layoutalternativ eller skapa en anpassad rapportlayout av den typ som du vill använda.

Om du har valt en inbyggd RDLC- eller Word-rapportlayout krävs ingen mer åtgärd och layouten används i när rapporten körs nästa gång.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Så här anger du en anpassad layout på en rapport
1. Du anger vilken anpassad layout som ska användas i rapporten på sidan **Anpassad rapportlayout**. Om sidan **Anpassad rapportlayout** inte är öppet väljer du sökknappen i fältet **Rapportlayoutbeskrivning**.
2. På sidan **Rapportlayoutbeskrivning** markera raden för anpassad layout som du vill använda, och stäng sedan sidan.

Du återgår till sidan **Val av rapportlayout**. Namnet på den valda anpassade layouten visas i fältet **Anpassad layoutbeskrivning**. Den anpassade layouten används nästa gången som du kör rapporten.

## <a name="see-also"></a>Se även
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

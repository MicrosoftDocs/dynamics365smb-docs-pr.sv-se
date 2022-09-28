---
title: Ställ in rapportlayouten
description: Lär dig att ange layout som används i en rapport för granskning och utskrift.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 03/07/2022
ms.author: jswymer
ms.openlocfilehash: e59a57e6cac21f4909088defc42da795e5550562
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535860"
---
# <a name="setting-the-layout-used-by-a-report"></a>Ange layout för en rapport

> **GÄLLER:** Business Central Online, Business Central lokal utgivningscykel 1 år 2022 och senare. Gå till tidigare versioner [här](ui-how-change-layout-currently-used-report.md).

En rapportlayout bestämmer utseendet på en rapport. Det styr vilka data fält i en rapport datauppsättning som visas, hur de är ordnade och formaterade med mera. En rapport kan ha mer än en layout som du kan växla mellan.

När det finns flera företag i kopplingen anges layouterna för varje företag. Samma rapport i ett företag kan ha olika layout i ett annat företag.

## <a name="get-started"></a>Kom igång

Det finns två sätt att ange vilken layout en rapport använder. Ett sätt är från sidan **Val av rapportlayout**. På det andra sättet kommer du från sidan **rapportlayouter**. Varje sida har olika fördelar, t.ex.: 

- På sidan för **val av rapportlayout** visas en lista över alla rapporter.

  På den här sidan visas den aktuella layouten för en rapport. Dessutom kan du ange layouter i olika företag utan att behöva byta det företag som du arbetar med.

- På sidan **rapportlayout** visas alla tillgängliga layouter för varje rapport i det aktuella företaget.

  Det är enkelt att hitta en speciell layout genom att sortera eller filtrera listan. När du har hittat layouten kan du ange den för en rapport med ett enda val.

  > [!NOTE]
  > Du kan inte använda sidan **rapportlayout** för Word- och RDLC layouter som har skapats med hjälp av de äldre **anpassade layouterna**. Du behöver inte ens visa dessa egna layouter på sidan **rapportmallar**. För dessa layouter kan du bara ställa in dem med hjälp av sidan **val av rapportlayout**.

## <a name="set-the-layout-from-the-report-layouts-page"></a>Ange layout från sidan rapportlayout

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Leta reda på layouten i listan, markera den och välj sedan **ange standard** åtgärd överst på sidan.

## <a name="set-the-layout-from-report-layout-selection-page"></a>Ange layout från sidan Val av rapportlayout

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Val av rapportlayouter** och väljer sedan relaterad länk.
  
   Val av rapportlayout visar alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företag** högst upp på sidan. Fältet **Layoutbeskrivning** anger den layout som används i rapporten för närvarande.
2. Ange fältet **Företag** fältet högst upp till företaget som inkluderar rapporten.
3. Sök reda på och markera rapporten i listan och gör sedan något av följande:

   - Om layouten som du vill växla till är en annan typ än den aktuella layouten markerar du fältet **layouttyp** och väljer den typ av layout som du vill använda i rapporten. 
   - Om layouten som du vill ändra till samma typ som den aktuella layouten väljer du alternativet **Välj layout** längst upp.

4. På sidan **Rapportlayouter** välj layout, välj sedan **OK**.

## <a name="revert-to-the-original-default-layout"></a>Återgå till ursprunglig standardlayout

Rapporter är avsedda att använda en layout som standard. Du kan växla tillbaka till det ursprungliga standardlayout sidan **Val av rapportlayout**. Markera bara rapporten och välj **Återställ standard åtgärd** för val längst upp på sidan.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

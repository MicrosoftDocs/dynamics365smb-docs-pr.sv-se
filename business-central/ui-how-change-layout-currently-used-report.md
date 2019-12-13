---
title: Ändra hur rapporten ska se ut genom att välja en annan layout | Microsoft Docs
description: Du kan använda olika layouter för en rapport och växla mellan layouter för att ändra utseendet på en rapport.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: af33d0679242e9915bc3e0de5825bf293e22c585
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809087"
---
# <a name="change-the-current-report-layout"></a>Ändra aktuell rapportlayout
En rapport kan ställas in med fler än en rapportlayout som du kan växla mellan.

Beroende på layouterna som finns tillgängliga för en rapport kan du välja att använda en inbyggd RDLC-rapportlayout, en inbyggd Word-rapportlayout eller en anpassad layout. Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).

När anpassade layouter för rapporter definieras kan du välja dem från kund- och leverantörskort för att ange att valda layouter ska användas för de dokument som du skapar för kunden eller leverantören i fråga. Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Dokumentrapporter (inte listor) som använder en Word-rapportlayout är vanligtvis snabbare än de med en RDLC-rapportlayout. Om du har möjlighet att välja mellan ett ord eller en RDLC-rapportlayout för en dokumentrapport kan du alltså använda Word-rapportlayouten för bästa prestanda.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Ändra vilken rapportlayout som ska användas för en rapport eller ett dokument
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Val av rapportlayout** och välj sedan relaterad länk.  
   Sidan **Val av rapportlayout** visar alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företag** högst upp på sidan. Fältet **Vald layout** anger den layout som används i rapporten för närvarande.
2. Ange fältet **Företag** fältet högst upp på sidan till företaget som inkluderar rapporten.
3. I raden för rapporten och anger du fältet **Vald layout** till ett av följande alternativ för att ändra layouten som används för en rapport:
   * **RDLC (inbyggd)**, använder den inbyggda RDLC-rapportlayouten i rapporten.
   * **Word (inbyggd)**, använder den inbyggda Word-rapportlayouten i rapporten.
   * **Anpassad** använder en anpassad layout i rapporten.  

> [!NOTE]
> Om du väljer en rapportlayout av typen **RDLC (inbyggt)** eller **Word (inbyggt)** och du får ett felmeddelande att rapporten inte har en layout för den angivna typen, måste du välja ett annat layoutalternativ eller skapa en anpassad rapportlayout av den typ som du vill använda. Visa nästa procedur.

Om du har valt en inbyggd RDLC- eller Word-rapportlayout krävs ingen mer åtgärd och layouten används i när rapporten körs nästa gång.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Så här ändrar du den anpassade layouten som ska användas för en rapportlayout
Du kanske också vill ändra den anpassade layout som används. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

Alla layouter för anpassade rapporter som finns för rapportmallar i ett företag visas på sidan **Anpassa rapportlayouter**. På sidan **Val av rapportlayout** kan du se vilka anpassade layouter som är tillgängliga för rapporten i faktaboxen **Anpassade layouter**.

1. På sidan **Val av rapportlayout** på raden för den rapportlayout som du vill ändra, väl uppslagsknappen i fältet **anpassad layoutbeskrivning** .
2. På sidan **Rapportlayoutbeskrivning** markera raden för anpassad layout som du vill använda, och välj sedan knappen **OK**.

Namnet på den valda anpassade layouten visas nu i fältet **Anpassad layoutbeskrivning** kommer att användas nästa gång rapporten eller dokumentet förhandsgranskas, skrivs ut eller skickas.

Du kan nu gå till kund- och leverantörskorten för att ange vilka layouter som ska användas för olika dokument som du har för kunden eller leverantören i fråga, t.ex. orderbekräftelser eller betalningspåminnelser. Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).

## <a name="see-also"></a>Se även
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

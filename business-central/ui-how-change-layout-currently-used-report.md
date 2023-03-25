---
title: Ändra hur rapporten ska se ut genom att välja en annan layout
description: Du kan använda olika layouter för en rapport och växla mellan layouter för att ändra utseendet på en rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
---
# (Äldre) Ange layout för en rapport

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

En rapport kan ställas in med fler än en rapportlayout som du kan växla mellan.

Beroende på layouterna som finns tillgängliga för en rapport kan du välja att använda en inbyggd RDLC-rapportlayout, en inbyggd Word-rapportlayout eller en anpassad layout. Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).

När anpassade layouter för rapporter definieras kan du välja dem från kund- och leverantörskort för att ange att valda layouter ska användas för de dokument som du skapar för kunden eller leverantören i fråga. Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Dokumentrapporter (inte listor) som använder en Word-rapportlayout är vanligtvis snabbare än de med en RDLC-rapportlayout. Om du har möjlighet att välja mellan ett ord eller en RDLC-rapportlayout för en dokumentrapport kan du alltså använda Word-rapportlayouten för bästa prestanda.

## Ändra vilken rapportlayout som ska användas för en rapport eller ett dokument

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Val av rapportlayouter** och väljer sedan relaterad länk.
  
   Sidan **Val av rapportlayout** visar alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företag** högst upp på sidan. **Layoutbeskrivning** <!-- **Selected Layout** -->anger den rapportlayout som används i rapporten för närvarande.
2. Ange fältet **Företag** fältet högst upp till företaget som inkluderar rapporten.

   I det här fältet kan du ange olika layouter för samma rapport i olika företag.

3. I raden för rapporten och anger du fältet **Vald layout** till ett av följande alternativ för att ändra layouten som används för en rapport:
   * **RDLC (inbyggd)**, använder den inbyggda RDLC-rapportlayouten i rapporten.
   * **Word (inbyggd)**, använder den inbyggda Word-rapportlayouten i rapporten.
   * **Anpassad** använder en anpassad layout i rapporten.  

> [!NOTE]
> Om du väljer en rapportlayout av typen **RDLC (inbyggt)** eller **Word (inbyggt)** och du får ett felmeddelande att rapporten inte har en layout för den angivna typen, måste du välja ett annat layoutalternativ eller skapa en anpassad rapportlayout av den typ som du vill använda. Visa nästa procedur.

Om du har valt en inbyggd RDLC- eller Word-rapportlayout krävs ingen mer åtgärd och layouten används i när rapporten körs nästa gång.

## Så här ändrar du den anpassade layouten som ska användas för en rapportlayout

Du kanske också vill ändra den anpassade layout som används. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

Alla layouter för anpassade rapporter som finns för rapportmallar i ett företag visas på sidan **Anpassa rapportlayouter**. På sidan **Val av rapportlayout** kan du se vilka anpassade layouter som är tillgängliga för rapporten i faktaboxen **Anpassade layouter**.

1. På sidan **Val av rapportlayout** på raden för den rapportlayout som du vill ändra, väl uppslagsknappen i fältet **anpassad layoutbeskrivning** .
2. På sidan **Rapportlayoutbeskrivning** markera raden för anpassad layout som du vill använda, och välj sedan knappen **OK**.

Namnet på den valda anpassade layouten visas nu i fältet **Anpassad layoutbeskrivning** kommer att användas nästa gång rapporten eller dokumentet förhandsgranskas, skrivs ut eller skickas.

Du kan nu gå till kund- och leverantörskorten för att ange vilka layouter som ska användas för olika dokument som du har för kunden eller leverantören i fråga, t. ex. orderbekräftelser eller betalningspåminnelser. Mer information finns i [definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md).

## Se relaterad [Microsoft utbildning](/training/modules/change-documents-dynamics-365-business-central/index)

## Se även
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

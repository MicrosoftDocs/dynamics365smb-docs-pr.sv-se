---
title: Använd artikelreferenser
description: Skapa referenser mellan de beskrivningar som du och din leverantör använder för en artikel så att du kan infoga leverantörens artikelbeskrivning på inköpsdokument.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588607"
---
# <a name="use-item-references"></a>Använd artikelreferenser
Om du har skapat en referens mellan den artikelbeskrivning som du använder för en artikel och den beskrivning som används för leverantören som levererar den artikeln och leverantörens artikelbeskrivning infogas automatiskt på inköpsdokument för en leverantör när du fyller i fältet **Artikelreferensnr** . Samma sak gäller för kundens artikelnummer i försäljningsdokument.

I följande procedurer beskrivs hur du använder artikelns referens på inköpssidan. Momenten är liknande för försäljningssidan.

> [!NOTE]
> Alla företag använder inte artikelreferenser, så för att minimera sammanhängande sidor vi har dolt de relaterade fälten och åtgärderna. Om du bestämmer dig för att använda dem kan du aktivera växlingsknappen **Använd artikelreferenser** på sidan **Lagerinställning**. När du har aktiverat artikelreferenser finns fälten och åtgärderna på artikel-, leverantörs- och kundkortsidor och från försäljnings- och inköpsdokument.

## <a name="to-start-using-item-references"></a>Börja använda artikelreferenser
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerinställning** och väljer sedan relaterad länk.
2. Aktivera växlingsknappen **Använd artikelreferenser**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Så här skapar du en artikelreferens för en leverantörs artikelbeskrivning

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Öppna kortet för en artikel som du vill skapa en referens till för den artikelbeskrivning som leverantören använder för artikeln.
3. Välj åtgärden **Artikelreferens**.

     Om du inte hittar åtgärden **Artikelreferenser** väljer du om du vill visa fler alternativ och sedan söker du under **Relaterat** > **Artikel**.
  
4. På en ny rad på sidan **Artikel referenstrans.**, fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Ange leverantörens artikelbeskrivning på en inköpsorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. Skapa en inköpsorder för leverantören som du ställer in en artikelreferens för ovan.
3. Skapa en inköpsorderrad för artikeln som du ställer in en artikelreferens för ovan.
4. I **Artikelreferensnummer.** välj artikeln artikelreferens som du har skapat och välj sedan knappen **OK**.

Fältet **beskrivning** på raden skrivs över med leverantörens artikelbeskrivning som ställs in på referensartikelns transaktion.

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
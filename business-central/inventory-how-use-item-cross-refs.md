---
title: Använd korsreferenser för objektet | Microsoft Docs
description: Skapa referenser mellan de beskrivningar som du och din leverantör använder för en artikel så att du kan infoga leverantörens artikelbeskrivning på inköpsdokument.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 056897c799dd12755432637690446a0797c9f18c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919444"
---
# <a name="use-item-cross-references"></a>Använd artikeltvärreferenser
Om du har skapat en tvärreferens mellan den artikelbeskrivning som du använder för en artikel och den beskrivning som används för leverantören som levererar den artikeln och leverantörens artikelbeskrivning infogas automatiskt på inköpsdokument för en leverantör när du fyller i fältet **Tvärreferensnr** . Samma sak gäller för kundens artikelnummer i försäljningsdokument.

I följande procedurer beskrivs hur du använder artikelns tvärreferens på inköpssidan. Momenten är liknande för försäljningssidan.

> [!NOTE]
> Det blir allt vanligare för artikelidentifierare som GTIN eller GUID som innehåller 30 eller fler tecken, vilket är mer än den aktuella funktionen för korsreferenser kan hanteras. Om du behöver använda referenser som innehåller fler än 30 tecken kan administratören aktivera funktionen **Skriv längre artikelreferenser** på sidan [Funktionshantering](https://businesscentral.dynamics.com/?page=xzy) (länken kräver att du har en [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisation). Hur du använder referenser ändras inte, men namn på sådant som sidor och knappar gör det. Exempelvis kommer sidan **Transaktioner för korsreferens av artikel** att bli sidan **Transaktioner för artikelreferens**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Så här skapar du en artikeltvärreferens för en leverantörs artikelbeskrivning

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för en artikel som du vill skapa en korsreferens till för den artikelbeskrivning som leverantören använder för artikeln.
3. Välj åtgärd **tvärreferenser**.

     Om du inte hittar åtgärden **Korsreferenser** väljer du om du vill visa fler alternativ och sedan söker du under **Relaterat** > **Artikel**.
  
4. På en ny rad på sidan **Artikel tvärreferenstrans**, fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Ange leverantörens artikelbeskrivning på en inköpsorder

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.
2. Skapa en inköpsorder för leverantören som du ställer in en artikeltvärreferens för ovan.
3. Skapa en inköpsorderrad för artikeln som du ställer in en artikeltvärreferens för ovan.
4. I **Tvärreferensnummer** välj artikeln artikelkorsreferens som du har skapat och välj sedan knappen **OK**.

Fältet **beskrivning** på raden skrivs över med leverantörens artikelbeskrivning som ställs in på korsreferensartikelns transaktion.

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

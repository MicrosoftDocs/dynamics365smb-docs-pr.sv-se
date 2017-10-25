---
title: "Så här överför du artiklar mellan olika distributionslagerplatser | Microsoft Docs"
description: "Beskriver hur du flytta lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41804dc183f9fa05ec1599db34c2b4f76a790a72
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-inventory-between-locations"></a>Så här överför du lager mellan olika lagerställen
Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder. Du kan även använda artikelgrupperingsjournalen.

Med överföringsorder kan du leverera en utgående överföring från ett lagerställe och ta emot den ankommande överföringen på det andra lagerstället. Detta gör det möjligt att administrera relevanta lageraktiviteter, och ger en större trygghet att lagerkvantiteterna uppdateras på rätt sätt.

Med grupperingsjournalen fyller du helt enkelt i fälten **Lagerställeskod** och **Ny Lagerställeskod**. När du bokför journalen, justeras artikeltransaktionerna på berörda lägerställen. På så sätt administreras inga lageraktiviteter.

> [!NOTE]  
>   Om du har artiklar i lagret utan lagerställekod, till exempel från en tid när du bara hade ett lage, kan du inte överföra objekten med överföringsorder. I stället måste du använda grupperingsjournalen för att gruppera artiklar från en tom lagerställekod till en faktisk lagerställekod.  Mer information finns i steg 3 i avsnittet "Att överföra artiklar med artikelgrupperingsjournalen".

Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in. Mer information finns i [Så här skapar du lägerställen](inventory-how-setup-locations.md).

> [!NOTE]  
>   Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>För att överföra artiklar med en överföringsorder.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Överföringsorder** och välj sedan relaterad länk.
2. I fönstret **Överföringsorder** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Om du har fyllt i fälten **Transitkod**, **Speditörkod** och **Speditör servicekod** i fönstret **Överföringsflödespec.** när du lade upp överföringsflödet, fylls motsvarande fält i automatiskt på överföringsordern.

    När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.

    Som lagerarbetare på utleveranslagerstället fortsätter du med att leverera artiklarna.
3. Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.

    Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med angivet överföringsflöde.

    Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna.
4. Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Så här överför du artiklar med artikelgrupperingsjournalen
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artikelgrupperingsjournaler** och välj sedan relaterad länk.
2. I fönstret **Artikelgrupp.journal** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.

    > [!NOTE]  
>   För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod**.
4. I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.
5. Välj åtgärden **Bokföra**.

## <a name="see-also"></a>Se även
[Hantera lager](inventory-manage-inventory.md)  
[Så här skapar du lagerställen](inventory-how-setup-locations.md)  
  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

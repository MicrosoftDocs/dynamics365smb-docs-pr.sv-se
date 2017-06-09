---
title: "Så här överför du lager mellan olika lagerställen | Microsoft Docs"
description: "Beskriver hur du överför lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 43a60a6eb646de13ca9bf1458061f0bbefbeab12
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a>Så här överför du lager mellan olika lagerställen
Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder. Du kan även använda artikelgrupperingsjournalen.

Med överföringsorder kan du leverera en utgående överföring från ett lagerställe och ta emot den ankommande överföringen på det andra lagerstället. Detta gör det möjligt att administrera relevanta lageraktiviteter, och ger en större trygghet att lagerkvantiteterna uppdateras på rätt sätt.

Med grupperingsjournalen fyller du helt enkelt i fälten **Lagerställeskod** och **Ny Lagerställeskod**. När du bokför journalen, justeras artikeltransaktionerna på berörda lägerställen. På så sätt administreras inga lageraktiviteter.

**Obs!** Om du har artiklar i lagret utan lagerställekod, till exempel från en tid när du bara hade ett lage, kan du inte överföra objekten med överföringsorder. I stället måste du använda grupperingsjournalen för att gruppera artiklar från en tom lagerställekod till en faktisk lagerställekod.  Mer information finns i steg 3 i avsnittet "Att överföra artiklar med artikelgrupperingsjournalen".

Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in. Mer information finns i [Så här skapar du lägerställen](inventory-how-setup-locations.md).

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i avsnittet [Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)] upplevelse](ui-experiences.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>För att överföra artiklar med en överföringsorder.
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Överföringsorder**, och väljer sedan relaterad länk.
2. I fönstret **Överföringsorder** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Obs!** Om du har fyllt i fälten **Transitkod**, **Speditörskod**, och **Speditörsservice** i fönstret **Överföringsflödesspec.** när du skapar överföringsflödet, kommer motsvarande fält på överföringsordern att fyllas i automatiskt.

    När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.

    Som lagerarbetare på utleveranslagerstället fortsätter du med att leverera artiklarna.
3. Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.

    Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med angivet överföringsflöde.

    Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna.
4. Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Så här överför du artiklar med artikelgrupperingsjournalen
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Artikelgrupperingsjournaler**, och välj sedan relaterad länk.
2. I fönstret **Artikelgrupp.journal** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.

    **Obs!** För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod** tomt.
4. I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.
5. Välj åtgärden **Bokföra**.

## <a name="see-also"></a>Se även
[Hantera lager](inventory-manage-inventory.md)  
[Så här skapar du lagerställen](inventory-how-setup-locations.md)  
[Logistik](madeira-supply-chain.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

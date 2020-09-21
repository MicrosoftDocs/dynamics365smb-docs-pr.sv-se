---
title: Så här överför du artiklar mellan olika distributionslagerplatser | Microsoft Docs
description: Beskriver hur du flytta lager från en plats eller ett lagerställe till en annan med grupperingsjournalen eller med överföringsorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fcd88d3fc8c933863bd79ab8b3405b68a3e1f1e1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778017"
---
# <a name="transfer-inventory-between-locations"></a>Överföra lager mellan olika lagerställen
Du kan överföra lagerartiklar mellan olika lägerställen genom att skapa överföringsorder. Du kan även använda artikelgrupperingsjournalen.

Med överföringsorder kan du leverera en utgående överföring från ett lagerställe och ta emot den ankommande överföringen på det andra lagerstället. Detta gör det möjligt att administrera relevanta lageraktiviteter, och ger en större trygghet att lagerkvantiteterna uppdateras på rätt sätt.

Med grupperingsjournalen fyller du helt enkelt i fälten **Lagerställeskod** och **Ny Lagerställeskod**. När du bokför journalen, justeras artikeltransaktionerna på berörda lägerställen. På så sätt administreras inga lageraktiviteter.

> [!NOTE]  
>   Om du har artiklar i lagret utan lagerställekod, till exempel från en tid när du bara hade ett lage, kan du inte överföra objekten med överföringsorder. I stället måste du använda grupperingsjournalen för att gruppera artiklar från en tom lagerställekod till en faktisk lagerställekod.  Mer information finns i steg 3 i [Att överföra artiklar med artikelgrupperingsjournalen](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Om du vill överföra artiklar måste lägerställen och överföringsflöden ställas in. Mer information finns i [Ange platser](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>För att överföra artiklar med en överföringsorder.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Överföringsorder** och välj sedan tillhörande länk.
2. I huvudet på sidan **Överföringsorder** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Om du har fyllt i fälten **Transitkod**, **Speditörkod** och **Speditör servicekod** på sidan **Överföringsflödespec.** när du lade upp överföringsflödet, fylls motsvarande fält i automatiskt på överföringsordern.

    När du fyller i fältet **Speditörsservice** beräknas datum för inleverans till det aktuella lagerstället genom att speditörens leveranstid tillförs utleveransdatumet.

3. Om du vill fylla i raderna anger du dem manuellt eller väljer ett av följande alternativ under åtgärdsfönstret **funktioner**:
    - Välj åtgärden **Hämta lagerplatsinnehåll** om du vill välja befintliga artiklar från en viss lagerplats på lagerstället.
    - Välj **Hämta inleveransrader** för att välja artiklar som precis har anlänt till det lagerställe där överföringen sker.   

    Som lagerarbetare på utleveranslagerstället fortsätter du med att leverera artiklarna.
4. Välj åtgärden **bokför**, välj alternativet **leverera**, och välj sedan **OK**-knappen.

    Artiklarna är nu på väg mellan de angivna lägerställena i enlighet med angivet överföringsflöde.

    Som lagerarbetare på utleveranslagerstället fortsätter du med att inleverera artiklarna. Överföringsorderraderna är desamma som när de levereras och kan inte redigeras.
5. Välj åtgärden **bokför**, välj alternativet **inleverera**, och välj sedan **OK**-knappen.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Så här överför du artiklar med artikelgrupperingsjournalen
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelgrupperingsjournaler** och välj sedan tillhörande länk.
2. På sidan **Artikelgrupp.journal** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I fältet **Lagerställeskod** ställer du in det lagerställe där artiklarna lagras för tillfället.

    > [!NOTE]  
    >   För att överföra artiklar som inte har någon platskod, lämnar du fältet **lagerställekod**.
4. I fältet **Ny lagerställeskod** ställer du in det lagerställe som du vill överföra artiklarna till.
5. Välj åtgärden **Bokföra**.

## <a name="see-also"></a>Se även
[Hantera lager](inventory-manage-inventory.md)  
[Konfigurera platser](inventory-how-setup-locations.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

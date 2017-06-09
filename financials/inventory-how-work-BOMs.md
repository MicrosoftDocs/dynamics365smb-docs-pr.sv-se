---
title: "Så här arbetar med strukturer | Microsoft Docs"
description: "Monteringsstrukturer anger vilka komponenter eller resurser som krävs för att sammanställa artikeln som monteringsstrukturen representerar. Monteringsstrukturer innehåller vanligtvis artiklar men kan också innehålla en eller flera resurser som utför monteringsarbetet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: ce75a9d292e12c58efc51c4db2fbc5a37b7553c7
ms.openlocfilehash: f55dcf4b391ae42ab46a22b729597a96645d9b71
ms.contentlocale: sv-se
ms.lasthandoff: 05/05/2017


---
# <a name="how-to-work-with-bills-of-materials"></a>Så här arbetar du med strukturer
**Obs!** Den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller bara den första delen av funktionen monteringshantering. Nu kan du bara skapa monteringsstrukturer och därefter hantera de relaterade överordnade artiklarna som normala lagerartiklar. I en kommande uppdatering kan du hantera den faktiska monteringen av artiklar från komponenter, antingen i montering mot lager eller montering mot orderflöden, och du kan sälja komponenter som satser.

Använd strukturer för att strukturera de överordnade artiklar som du säljer som satser som består av komponenter som du monterar till order eller lager.

I [!INCLUDE[d365fin](includes/d365fin_md.md)],  är en struktur en monteringsstruktur. Monteringsstrukturer anger vilka komponenter som finns i överordnade artiklar. I den här dokumentationen kallas en artikel en "monteringsartikel".

Monteringsstrukturer innehåller vanligtvis artiklar men kan också innehålla en eller flera resurser som krävs för att utföra monteringsarbetet.

Monteringsstrukturer kan ha flera nivåer, vilket innebär att en komponent på monteringsstruktur kan vara en monteringsartikel själv. I så fall innehåller fältet **Monteringsstruktur** på monteringsstrukturraden **Ja**.

Särskilda krav gäller artiklarna på moneringsstrukturer med avseende på tillgängligheten. Mer information finns i avsnittet "För att visa tillgängligheten för en artikel med dess användning i monteringsstrukturer" i [så här skapar du en översikt av disposition](inventory-how-availability-overview.md).

**Obs!** den här funktionen kräver att din upplevelse är inställd på **Paket **. Mer information finns i [anpassa din finansiella upplevelse](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Skapa en monteringsstruktur
Om du vill definiera en överordnad artikel som består av andra artiklar eller resurser som krävs för att montera den överordnade, måste du skapa en monteringsstruktur.  

Det finns två delar för att skapa en monteringsstruktur:
- Skapa en ny artikel
- Ange strukturem för monteringsartikeln.

1. Skapa en ny artikel. Mer information finns i [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).

    Fortsätt med att ange komponenter eller resurser i monteringsstrukturen.  
2. I fönstret **artikelkort** för en monteringsartikel väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.
3. I fönstret **Monteringsstruktur** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Att visa komponenter i en monteringsartikel som dras in enligt strukturen
Från fönstret **Monteringsstruktur** kan du öppna ett separat fönster som visar komponenterna och resurserna med indrag enligt deras strukturplats under monteringsartikeln.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Artikel**, och välj sedan relaterad länk.
2. Öppna kortet för monteringsartikeln. (Fältet **Monteringsstruktur** i fönstret **artiklar** innehåller **Ja**.)
3. I fönstret **artikelkort** väljer du åtgärden **montering** och väljer sedan åtgärden **Monteringsstruktur**.
4. I fönstret **Monteringsstruktur** väljer du åtgärden **visa struktur**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Att köpa, sälja eller överföra monteringsartiklar
Eftersom den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] endast innehåller förmågan att definiera och tilldela strukturer till artiklar kan du hantera monteringsartiklar på rader som endast vanliga artiklar.

**Varning**: lagerkvantiteten för strukturkomponenter justeras inte om du gör detta.

## <a name="see-also"></a>Se även
[Så här registrerar du nya objekt](inventory-how-register-new-items.md)  
[Så här skapar du en tillgänglighetsöversikt](inventory-how-availability-overview.md)     
[Lager](inventory-manage-inventory.md)  
[Arbetar med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)


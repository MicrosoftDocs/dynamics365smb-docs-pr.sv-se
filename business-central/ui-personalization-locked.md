---
title: Varför kan jag inte anpassa en sida? | Microsoft Docs
description: Förklarar varför du inte kan anpassa en sida, och vad du kan göra om du vill låsa upp den för att anpassa den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "911702"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Varför är en sida låst för anpassning?

Det finns två villkor som hindrar dig från att anpassa en sida. Antingen är sidan låst (som indikeras av ![anpassa lås](media/personalization-lock-icon.png "anpassa lås")) eller spärrad (som indikeras av ![anpassning spärrad](media/personalization-blocked-icon.png "anpassning spärrad")).

## <a name="locked-from-personalizing"></a>Låst för att anpassa

Om det finns en ikon ![anpassa lås](media/personalization-lock-icon.png "anpassa lås") i banderollen **anpassa** när du öppnar en sida (enligt bilden), betyder det att du för tillfället inte kan göra några fler anpassningsändringar på sidan.

![Anpassa låsning](media/personalization-locked.png "Anpassa låsning")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Det finnas två orsaker till detta:

1. Du har anpassat sidan tidigare, men det har gjorts med hjälp av en tidigare version av produkten. Vi har ändrat hur anpassningen fungerar i bakgrunden sedan senaste gången du anpassade sidan. Tyvärr fungerade inte det gamla och det nya sättet tillsammans.

2. Hittills har du bara använt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] för att anpassa sidan.

### <a name="unlocking-the-page"></a>Låsa upp sidan

Om du vill låsa upp en sida och fortsätta anpassa den, välj ![anpassa lås](media/personalization-lock-icon.png "anpassa lås") och sedan **lås upp**.  

Innan du låser upp sidan, ska du tänka på följande:

- Den aktuella anpassningen på sidan kommer att tas bort. Sidan går tillbaka till sin ursprungliga layout och du måste börja om från början.

- I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] kommer sidan att behållas som den är och påverkas inte av de nya anpassningar i Business Central-klienten. Sedan kommer anpassningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] och Business Central-klienten att vara helt skilda från varandra.

## <a name="blocked-from-personalizing"></a>Blockerad från att anpassa

Om det finns en ikon för ![anpassning spärrad](media/personalization-blocked-icon.png "anpassning spärrad") i anpassningsbanderoll innebär detta att du blockeras från att göra alla anpassningar till sidan.

![Anpassa spärrad](media/personalization-blocked.png "Anpassa spärrad")

Orsaken till detta är att det rollcenter eller den profil som för närvarande är associerad med ditt användarkonto ändrar sidan specifikt för din roll. Kontakta administratören om du behöver hjälp eller, om det passar, kan du försöka att byta till ett rollcenter (från [**Mina inställningar**](https://businesscentral.dynamics.com?page=9176 "gå direkt till sidan användare inställningar i Business Central")) som innehåller rollanpassning för sidan.

## <a name="see-also"></a>Se även
[Anpassa din arbetsyta](ui-personalization-manage.md)  
[Hantera anpassning](ui-personalization-manage.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

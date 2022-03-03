---
title: Varför kan jag inte anpassa en sida?
description: Förklarar varför du inte kan anpassa en sida och vad du kan göra om du vill låsa upp den så att du kan anpassa den.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd94d467961cf4f01fdffa35241d84371be64527
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335324"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Varför är en sida låst för anpassning?

Det finns två villkor som hindrar dig från att anpassa en sida. Antingen är sidan låst (vilket indikeras av ikonen ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås")) eller spärrad (vilket indikeras av ikonen ![Anpassning spärrad.](media/personalization-blocked-icon.png "Anpassning spärrad") ).

## <a name="locked-from-personalizing"></a>Låst för att anpassa

Om det finns ett ![Anpassa lås.](media/personalization-lock-icon.png "Anpassa lås") i banderollen **Anpassa** när du öppnar en sida, betyder det att du för tillfället inte kan göra några fler anpassningsändringar på sidan.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Det finnas två orsaker till detta:

1. Du har anpassat sidan tidigare, men det har gjorts med hjälp av en tidigare version av produkten. Vi har ändrat hur anpassningen fungerar i bakgrunden sedan senaste gången du anpassade sidan. Tyvärr fungerade inte det gamla och det nya sättet tillsammans.

2. Hittills har du bara använt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] för att anpassa sidan.

### <a name="unlocking-the-page"></a>Låsa upp sidan

Om du vill låsa upp en sida och fortsätta anpassa den väljer du ikonen ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås") och sedan åtgärden **Lås upp**.  

Innan du låser upp sidan, ska du tänka på följande:

- Den aktuella anpassningen på sidan kommer att tas bort. Sidan går tillbaka till sin ursprungliga layout och du måste börja om från början.

- I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] kommer sidan att behållas som den är och påverkas inte av de nya anpassningar i Business Central-klienten. Sedan kommer anpassningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] och Business Central-klienten att vara helt skilda från varandra.

## <a name="blocked-from-personalizing"></a>Blockerad från att anpassa

Om det finns en ikon för ![Anpassning spärrad](media/personalization-blocked-icon.png "Anpassning spärrad") i banderollen **Anpassning** innebär detta att du spärras från att utgöra några anpassningar på sidan.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Orsaken till detta är att det rollcenter eller den roll som för närvarande är associerad med ditt användarkonto ändrar sidan specifikt för din roll. Kontakta administratören om du behöver hjälp. Du kan också försöka växla till ett rollcenter som innehåller rollspecifika roller för den här sidan. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).

## <a name="see-also"></a>Se även
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Anpassa sidor för profiler](ui-personalization-manage.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

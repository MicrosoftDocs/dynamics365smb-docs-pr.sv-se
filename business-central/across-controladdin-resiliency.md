---
title: Styra tillägget för återhämtning i Business Central
description: Vad du bör göra om tillägg för styrning eller anpassade kontroller ger nedsatt funktionalitet i Business Central.
ms.topic: conceptual
author: brentholtorf
ms.author: bholtorf
ms.date: 12/12/2023
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="control-add-in-resiliency-in-business-central"></a>Styra tillägget för återhämtning i Business Central

Från och med version 20.0 av [!INCLUDE[prod_short](includes/prod_short.md)] identifieras kontrolltillägg som utförs långsamt automatiskt, och en dialogruta av följande slag visas:

![Kontrolltillägg upptaget.](media/controladdin-resiliency.png "Kontrolltillägg upptaget.")

Ett kontrolltillägg som är skadat kan påverka din Business Central-upplevelse och få den sida du arbetar med att starta långsamt. Detta har ingen effekt på datan och ändringarna sparas alltid. Om varningen ovan visas kan du dölja den, men den kan komma att dyka upp igen. Om problemet kvarstår bör du kontakta administratören.

## <a name="see-also"></a>Se även
[Kontrollera bästa praxis för tilläggsprestanda](/dynamics365/business-central/dev-itpro/developer/devenv-control-addin-bestpractices)  

---
title: Installera tillägg för att anpassa Business Central | Microsoft Docs
description: Lär dig mer om att lägga till funktioner och att anpassa Business Central genom att installera tillägg.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765927"
---
# <a name="customizing-business-central-using-extensions"></a>Anpassa Business Central med tillägg

Du kan ändra [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att installera tillägg som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster.

> [!NOTE]
> Om du vill installera tillägg från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i användargruppen D365 Tilläggshant. eller så måste du ha behörighetsuppsättningen D365 Tilläggshant. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget.<br /><br />
Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

> [!IMPORTANT]  
> Överföring av tillägg per innehavare och installation av AppSource-tillägg stöds inte via sidan **Tilläggshantering** för lokala installationer.

När du först startar först [!INCLUDE[d365fin](includes/d365fin_md.md)], har du dessutom några tillägg installerade. Med tiden kommer fler tillägg att göras tillgängliga till dig, och du kan då välja om du vill använda tillägg eller inte.

Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard. Detta tillägg instalelras dessutom som standard.
Men om ett annat tillägg är tillgängligt som erbjuder integrering med en annan utbetalningtjänst, kan du installera det nya tillägget och sedan välja vilka av de två tjänsterna som ska användas.  

Du hanterar tilläggen på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken. Mer information finns i [Installera och avinstallera tillägg](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Om du tror att du borde ha åtkomst till ett tillägg, men dess funktioner inte går att hitta kontrollerar du sidan **tilläggshantering** om tillägget inte finns, kan du installera det enligt vad som beskrivs i följande avsnitt.  

> [!NOTE]  
> Tillägg är inte tillgängliga i AppSource så snart vi meddelar en uppdatering. Du kan hålla utkik efter tilläggen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="see-also"></a>Se även

[Utökning av Dynamics 365 Business Central](about-develop-extensions.md)  
[Business Central-tillägg från andra leverantörer](ui-extensions-other.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Konfigurera tillägget GetAddress.io för postnummer i Storbritannien](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-tillägg från andra leverantörer](ui-extensions-other.md)  
[Komma igång](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

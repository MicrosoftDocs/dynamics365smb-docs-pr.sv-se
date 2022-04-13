---
title: Anpassa Business Central Online med hjälp av tillägg
description: Lär dig mer om att lägga till funktioner och att anpassa Business Central genom att installera tillägg.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont
ms.openlocfilehash: 56c564274e396d9699286b18d882c2a21f8721ef
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510693"
---
# <a name="customizing-business-central-online-using-extensions"></a>Anpassa Business Central Online med hjälp av tillägg

Du kan ändra [!INCLUDE[prod_short](includes/prod_short.md)] online genom att installera tillägg som lägger till funktioner, ändrar beteende eller ger dig tillgång till nya onlinetjänster.

> [!NOTE]
> Om du vill installera eller avinstallera tillägg från AppSource eller lägga till tillägg per klientorganisation måste du ha rätt behörigheter. Du måste antingen vara medlem i användargruppen **D365 Extension Mgt.** eller ha behörighetsuppsättningen **EXTENSION MGT - ADMIN**. Om du är administratör kan du tilldela användargrupper och behörigheter till andra användare i företaget. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).  
>
> Om du vill använda funktionen som tillhandahålls av ett tillägg, till exempel att öppna sidor, köra rapporter, välja åtgärder och så vidare, måste du koppla behörighetsuppsättningarna som installeras som en del av tillägget.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

> [!IMPORTANT]  
> Överföring av tillägg per innehavare och installation av AppSource-tillägg stöds inte via sidan **Tilläggshantering** för lokala installationer. Du kan inte installera AppSource-tillägg lokalt, inklusive i Docker-baserade distributioner.

När du först startar först [!INCLUDE[prod_short](includes/prod_short.md)], har du dessutom några tillägg installerade. Med tiden kommer fler tillägg att göras tillgängliga till dig, och du kan då välja om du vill använda tillägg eller inte.

Till exempel ger Microsoft ett tillägg som ger integrering med PayPal Payments Standard. Detta tillägg instalelras dessutom som standard.
Men om ett annat tillägg är tillgängligt som erbjuder integrering med en annan utbetalningtjänst, kan du installera det nya tillägget och sedan välja vilka av de två tjänsterna som ska användas.  

Du hanterar tilläggen på sidan **Tilläggshantering**. Du kan öppna den här sidan från startsidan. Du kan också välja ikonen **Sök efter sidan eller rapporten** ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") i övre högra hörnet och ange **tillägg** och välj sedan den relaterade länken. Mer information finns i [Installera och avinstallera tillägg](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Om du tror att du borde ha åtkomst till ett tillägg, men dess funktioner inte går att hitta kontrollerar du sidan **tilläggshantering** om tillägget inte finns, kan du installera det enligt vad som beskrivs i följande avsnitt.  

> [!NOTE]  
> Logga in på [AppSource.microsoft.com](https://appsource.microsoft.com/) med hjälp av det e-postkonto som du använder för [!INCLUDE[prod_short](includes/prod_short.md)] online. Använd samma e-postkonto för andra tjänster och produkter för en bra upplevelse.  

Du kan också komma till marknadsplatsen från [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Tilläggshantering** kan du se tilläggen som installeras för närvarande, och du kan öppna sidan **tilläggmarknadsplatsen** som visar tilläggen för [!INCLUDE[prod_short](includes/prod_short.md)] som för närvarande finns tillgängliga i AppSource. Om du väljer länken *Fler appar* tas du till [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Om du väljer ett tillägg kan du läsa om vad tillägget används till och du kan få mer information om tillägget. När du väljer att få ett tillägg, måste du godkänna användningsvillkoret. Om du får tillägget från AppSource-webbplatsen kommer du att loggas in på [!INCLUDE[prod_short](includes/prod_short.md)] för att slutföra installationen.  

När du installerar tillägget kanske du behöver måste konfigurera det, till exempel ange ett konto för användning med tillägget **PayPal Payments Standard för [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andra tillägg lägger bara till i fält på en befintlig sida, eller lägger till en ny sida, till exempel.   

Om du avinstallerar tillägget och du sedan ändrar dig kan du installera det på nytt. När du avinstallerar tillägg som du har använt, bevaras data så att de är tillgängliga om du installerar tillägget igen. Det finns vissa tillägg som krävs. Du kan inte avinstallera dem från sidan för **tilläggshantering**. Om du försöker visas ett felmeddelande.  

Några tillägg ges ut av Microsoft, och andra tillägg ges ut av [andra företag](ui-extensions-other.md). Alla tillägg testas innan de görs tillgängliga för dig, men vi rekommenderar att du öppnar länkarna som tillhandahålls med varje tillägg om du vill veta mer om tillägget innan du väljer att installera det.  

> [!NOTE]  
> Du kan hålla utkik efter nya tillägg från Microsoft och andra leverantörer på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Tillägg och dataöverföring

Eftersom följande tillägg kommunicerar med andra tjänster kan de överföra data ur geografi för [!INCLUDE[prod_short](includes/prod_short.md)]-miljö:

* AMC Banking 365 Fundamentals-tillägg
* Image Analyzer
* Prediktion om sen betalning
* PayPal Payments Standard
* Försäljnings- och lagerprognos
* WorldPay Payments Standard

Detta gäller även vissa funktioner i basprogrammet, till exempel följande funktioner:

* Kassaflödesprognos
* Dokumentväxlingstjänst
* Dataverse-anslutningar
* OCR-tjänst
* Online Map
* EU:s momsregistreringsnummer Service

## <a name="recommended-apps"></a>Rekommenderade appar
Microsofts partner och återförsäljare kan skapa ett tillägg som de kan använda för att sammanställa listor över appar som de ofta rekommenderar till sina kunder. Om de gör det och har distribuerat tillägget till din klientorganisation kommer programmen att vara tillgängliga på sidan **rekommenderade appar**. Där kan du läsa om varje app och bestämma om du ska installera dem.

> [!NOTE]
> Om du är Microsoft-partner eller återförsäljare och vill tillhandahålla en lista över rekommenderade appar, se [rekommendationer för appar från AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-also"></a>Se även

[Installera och avinstallera tillägg](ui-extensions-install-uninstall.md)  
[Anpassa Business Central](ui-customizing-overview.md)  
[Business Central-tillägg från andra leverantörer](ui-extensions-other.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Konfigurera tillägget GetAddress.io för postnummer i Storbritannien](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-tillägg från andra leverantörer](ui-extensions-other.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]

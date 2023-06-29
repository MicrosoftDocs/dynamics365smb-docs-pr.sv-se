---
title: Översikt över skrivarinställning och hantering
description: Ta reda på vad de olika möjligheterna för skrivare i Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 02/10/2023
ms.custom: bap-template
---

# <a name="printer-setup-and-management-overview"></a><a name="printer-setup-and-management-overview"></a>Översikt över skrivarinställning och hantering

Att skriva ut dokument och rapporter från [!INCLUDE[prod_short](includes/prod_short.md)] är en viktig uppgift för företagsanvändare. Du vill vanligtvis skicka utskriftsjobb direkt till en av organisationens skrivare&mdash;oavsett vilken [!INCLUDE[prod_short](includes/prod_short.md)]-klient eller -app som du använder. Eftersom [!INCLUDE[prod_short](includes/prod_short.md)] online är en molntjänst kan den inte direkt nå lokala skrivare som är anslutna till användarnas enheter, men du kan ansluta den till molnbaserade skrivare.

## <a name="what-are-your-printer-possibilities-in-business-central"></a><a name="what-are-your-printer-possibilities-in-business-central"></a>Vilka skrivar möjligheter finns i Business Central?

För att stödja dina utskriftsbehov [!INCLUDE[prod_short](includes/prod_short.md)] finns följande funktioner:

|Funktion|Beskrivning|Webbklient| Mobilapp|App för Teams|
|-------|-----------|----------|-----------|--------------|
|Universell utskrift|Universell utskrift är en lösning för skrivarhantering som finns tillgänglig som en molntjänst från Microsoft. Med den här funktionen kan du ställa in skrivarna i Universell utskrift och sedan registrera dem för användning i [!INCLUDE[prod_short](includes/prod_short.md)]. För den här funktionen krävs en Universell utskrift-prenumeration och tillägget **Universell utskrift-integrering**|![arbetar online.](media/check.png)|![arbetar online.](media/check.png)|![arbetar online](media/check.png)|
|E-postutskrift|Med den här funktionen kan du konfigurera skrivare som har stöd för e-post. [!INCLUDE[prod_short](includes/prod_short.md)] skickar sedan utskriftsjobben till en skrivare med hjälp av skrivarens e-postadress. För den här funktionen krävs e-postaktive rad skrivare och tillägget **Skicka till e-postskrivare**.|![arbetar online.](media/check.png)|![arbetar online](media/check.png)|![arbetar online](media/check.png)|
|Webbläsarutskrift|Utskriftsjobb hanteras av utskriftsfunktionen i användarens webbläsare. Om en molnskrivare inte har installerats eller konfigurerats, eller om en installerad skrivare havererar, kommer utskriften att ske via webbläsarens standardalternativ för utskrift. Fältet **Skrivare** på sida för rapportförfrågan visas *(hanteras av webbläsaren)*.|![arbetar online](media/check.png)|||

Det mesta av arbetet med att installera skrivare kan du göra från sidan**Skrivarhantering** i [!INCLUDE[prod_short](includes/prod_short.md)]. Även med skrivare med universell utskrift kan du också behöva arbeta i Microsoft 365 administrationscenter eller Azure Portal.

> [!IMPORTANT]
> För Business Central lokalt används universell utskrift och e-postutskrift som Azure Active Directory (AD) eller NavUserPassword-autentisering.

## <a name="custom-printer-extensions"></a><a name="custom-printer-extensions"></a>Anpassade skrivartillägg

[!INCLUDE[prod_short](includes/prod_short.md)] stöder andra anpassade skrivartillägg som lägger till ännu fler utskriftsfunktioner. Om du har installerat anpassade skrivartillägg kan det till exempel vara utskriftsfunktioner som inte beskrivs i den här artikeln.

Om du är en AL-utvecklare och vill veta mer om hur du skapar skrivartillägg kan du gå till [Utveckla skrivartillägg i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## <a name="next-steps"></a><a name="next-steps"></a>Nästa steg

- [Konfigurera skrivare för Universell utskrift](admin-printer-setup-universal-print.md)  
- [Konfigurera e-postutskrift](admin-printer-setup-email.md)  
- [Ställa in standardskrivare](ui-specify-printer-selection-reports.md)

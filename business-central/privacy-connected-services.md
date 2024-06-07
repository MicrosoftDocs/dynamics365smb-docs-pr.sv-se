---
title: Test funktioner som kan anslutas till andra Microsoft-tjänster
description: Översikt över Microsoft-tjänster som Business Central ansluter till med testversionen.
author: jswymer
ms.topic: overview
ms.service: dynamics-365-business-central
ms.search.keywords: 'privacy, trial, Microsoft services'
ms.date: 04/14/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---
# Test funktioner som kan anslutas till andra Microsoft-tjänster 

[!INCLUDE[prod_long](includes/prod_long.md)] är en omfattande affärshanteringslösning som är djupt integrerad med Microsoft 365 produktivitetsprogram och Power Platform. Din kostnadsfria testversion av Business Central kan ansluta till många olika Microsoft-tjänster som måste konfigureras och aktiveras först. För att få ut det mesta av din kostnadsfria utvärderingsversion har vissa av dessa funktioner aktiveras automatiskt. Även om anslutningen från [!INCLUDE[prod_short](includes/prod_short.md)] är aktiverad ingår inte dessa tjänster i testversionen och måste köpas separat om du inte redan har dem.

Tabellen nedan visar anslutningarna till Microsoft-tjänster som har aktiveras automatiskt för [!INCLUDE[prod_short](includes/prod_short.md)] utvärderingsversioner:

|Servicenamn|Anslutningen aktiveras automatiskt |Tjänsten kontaktas när du loggar in på Business Central |Exempelfunktion som använder den här tjänsten | Lär dig hur du hanterar den anslutning och de funktioner som använder den|  
|------------|-------------|--------|------------|-------------|
|Microsoft Teams|Ja|Nr|**Dela till Teams**-åtgärd på **artikel** kort |[Hantera Teams-integrering med Business Central](admin-teams-integration.md)|  
|Microsoft OneDrive för företag|Ja|Nr|**Öppna i OneDrive** åtgärd på **objekt** bilagor |[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup)|  
| Microsoft Power Automate |Ja|Nr|**Automatisera** åtgärder på **artikel** kort |[Konfigurera Power Automate integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|
| Microsoft Azure OpenAI Service |Ja |Nr|**Copilot** |[Konfigurera marknadsföringstext för AI-baserad artikel med Copilot](enable-ai.md)|

> [!NOTE]
> Med hjälp av funktioner som ansluter till dessa tjänster: 
>
> - Du medgivande på att dina data delas med Microsoft-tjänsten. Om organisationen har distribuerat dessa tjänster i ett annat land eller en annan region kan en anslutning till tjänsten leda till att data korsar datahemvistgränser. Se till att bekräfta organisationens principer och myndighetsefterföljandekrav för datahemvist innan du använder dessa funktioner. 
> - Det kan påverka tjänster som inte är testversioner. Om dessa tjänster används i produktionen av organisationen och inte är utvärderade tillsammans med Business Central, andra användare av dessa tjänster som inte deltar i denna testversion av [!INCLUDE[prod_short](includes/prod_short.md)] påverkas.
> - [!INCLUDE[prod_short](includes/prod_short.md)] kan också ansluta till Microsoft-tjänster eller tjänster från tredje part beroende på de anpassningar och tillägg som du eller administratören har installerat i din [!INCLUDE[prod_short](includes/prod_short.md)] testversion. Om du vill ha information om hur dina data kommer att bearbetas, kontaktar du tilläggsutvecklaren eller följer sekretesslänken för tillägget AppSource.
> - För funktioner i förhandsversion godkänner du [villkor för förhandsversion](https://powerplatform.microsoft.com/en-us/legaldocs/supp-powerplatform-preview/?wt.mc_id=power-virtual-agents_inproduct).

Din sekretess är viktig för oss. Om du vill veta mer om hur Microsoft behandlar dina data, se [Microsofts sekretesspolicy](https://go.microsoft.com/fwlink/?linkid=521839).

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Felsöka Copilot- och AI-funktioner
description: Lär dig hur du åtgärdar vanliga problem som du kan stöta på när du arbetar med Copilot- och AI-funktioner i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 02/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Felsöka Copilot- och AI-funktioner

Copilot är en AI-driven funktion i Business Central som hjälper till med olika uppgifter som att skriva marknadsföringstext och stämma av bankkonton. Om du har problem med Copilot eller andra AI-funktioner kan den här artikeln hjälpa dig att identifiera och åtgärda vanliga problem.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot visas inte på sidorna

Om Copilot-funktionalitet, såsom åtgärden **Utkast med Copilot** för marknadsföringstextförslag eller åtgärden **Stämma av med Copilot** för hjälp med bankkontoavstämning, visas inte på en sida som förväntat, kontrollera följande:

- Om funktionen styrs under Funktionshantering, se till att den är aktiverad. [Läs mer om funktionshantering](admin-feature-management.md).

- Se till att funktionen inte döljs av anpassning. [Läs mer om hur du arbetar med personanpassning](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot visas på sidorna, men du får ett felmeddelande om att den inte är aktiverad

När du försöker använda Copilot och du får ett felmeddelande som liknar **Tyvärr är Copilot inte aktiverat för \[funktionen\]**, det finns ett par saker att kontrollera:

- Se först till att funktionen är aktiverad på **Copilot och AI-funktioner**. [Läs mer om hur du aktiverar Copilot- och AI-funktioner](enable-ai.md#activate-features). 
- Se sedan till att sekretessmeddelandet för Azure OpenAI integration inte är inställt på **Acceptera inte för alla**. Om det är det, ändra det till **Acceptera för alla**. [Läs mer om sekretessmeddelanden](privacy-notices-status.md).

## <a name="copilot-capabilities-from-microsoft-not-listed-on-copilot--ai-capabilities-page"></a>Copilot-funktioner från Microsoft visas inte på sidan Copilot- och AI-funktioner

Om ingen av AI-funktionerna från Microsoft visas på sidan **Copilot- och AI-funktioner** beror det troligen på att du har en eller flera inbäddade appar installerade i din miljö. Inbäddade appar kan erbjuda egna Copilot-funktioner, men funktioner som publiceras av Microsoft är inte kompatibla med miljöer som har inbäddade appar.

## <a name="see-also"></a>Se även

[Konfigurera Copilot- och AI-funktioner](enable-ai.md)  
[Marknadsföringstextförslag med Copilot](ai-overview.md)  
[Stäm av bankkonton med Copilot](bank-reconciliation-with-copilot.md)  

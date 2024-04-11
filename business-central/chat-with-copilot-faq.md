---
title: Vanliga frågor och svar om chatt med Copilot
description: Den här artikeln svarar på några vanliga frågor om att chatta med Copilot i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 02/27/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Vanliga frågor och svar om chatt med Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Den här artikeln svarar på några vanliga frågor om att chatta med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du har frågor om AI och chatt läser du [Vanliga frågor om ansvarsfull AI för chatt med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kan administratörer bevilja eller neka enskilda användare behörighet att få åtkomst till chatten?

Nej, det finns ingen behörighet eller behörighet för chatt. Om chatten är aktiverad på sidan [Copilot- och AI-funktioner](enable-ai.md) har alla användare i en miljö åtkomst till chatten.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Är chatten tillgänglig på surfplatta, telefon eller andra formfaktorer?

Nej, chattfönstret är bara tillgängligt på webbklienten [!INCLUDE[web_client](includes/web_client.md)].

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Jag använder inte Business Central på engelska. Vilka är mina alternativ?

För närvarande är chatten endast tillgänglig på engelska. Du kan ändra ditt användarspråk till engelska i [Mina inställningar](ui-change-basic-settings.md#language).

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Vilken Business Central-version behöver jag för att uppleva chatt?

Chatt är tillgänglig som allmänt tillgänglig förhandsversion från version 24.0 (2024 utgivningscykel 1).

## <a name="does-chat-work-with-my-customizations"></a>Fungerar chatten med mina anpassningar?

Det beror på vilken typ av fråga du ställer till Copilot. Till exempel:

- När du ställer frågor för att hitta poster kan Copilot hitta poster i dina anpassade tabeller som identifieras med hjälp av anpassade fält.
- När du ber om en förklaring eller vägledning har Copilot inte tillgång till någon information om dina anpassningar eller dokumentation för dina tillägg.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Copilot verkar aldrig öppna skivan eller sidan jag bad om. Vad gör jag för fel?

När du ber Copilot att söka efter poster i [!INCLUDE[prod_short](includes/prod_short.md)] visas alla poster som hittas som valbara paneler eller länkar i chattfönstret. I förhandsversionen navigerar Copilot inte automatiskt till någon sida.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>Svaren jag får från Copilot varierar trots att jag ställer samma fråga. Är det ett fel?

Copilot kan ibland svara på olika sätt. Svaren är inte nödvändigtvis identiska.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>När ska jag använda kopieringsfunktionen i chattmeddelanden?

Du kan använda knappen Kopiera för att kopiera ett meddelande från tidigare i konversationen med Copilot, klistra in det i inmatningsrutan för att försöka igen eller prova en variant av meddelandet till Copilot.

## <a name="how-do-i-customize-or-extend-chat"></a>Hur anpassar eller utökar jag chatten?

I förhandsversionen kan chattfönstret och Copilot-svar inte ändras på något sätt via anpassning, tillägg eller anpassning.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Hittar Copilot data i andra företag eller miljöer?

Även om din organisation använder flera miljöer eller företag för att separera data söker Copilot bara efter poster i det företag som du för närvarande är inloggad på.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Chattfönstret Copilot visas inte. Vad kan jag göra?

Kontrollera att ditt användarspråk i Mina inställningar är inställt på engelska och att din miljö är av version 24.0 eller senare. På sidan Copilot- och AI-funktioner kontrollerar du att administratörer har aktiverat samtycke för data mellan geografiska områden och har aktiverat chatt. Kontrollera att din miljölokalisering inte är Kanada.

Om du fortfarande inte ser chatten med Copilot-funktionen är det möjligt att Microsoft fortfarande lanserar detta till din region. Copilot lanseras till amerikanska kunder först i april 2024 och kommer sedan under veckorna att distribueras till andra landslokaliseringar.

## <a name="next-steps"></a>Nästa steg

[Chatt med Copilot (förhandsversion)](chat-with-copilot.md)

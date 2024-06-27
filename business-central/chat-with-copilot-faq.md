---
title: Vanliga frågor och svar om chatt med Copilot
description: 'Lär dig hur du chattar med Copilot, en virtuell assistent som hjälper dig att använda Business Central. Hitta svar på vanliga frågor om chattfunktioner, inställningar och begränsningar.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Vanliga frågor och svar om chatt med Copilot

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Den här artikeln svarar på några vanliga frågor om att chatta med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du har frågor om AI och chatt läser du [Vanliga frågor om ansvarsfull AI för chatt med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kan administratörer bevilja eller neka enskilda användare behörighet att få åtkomst till chatten?

Nej, det finns ingen behörighet eller behörighet för chatt. Om chatten är aktiverad på sidan [Copilot- och AI-funktioner](enable-ai.md) har alla användare i en miljö åtkomst till chatten.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Är chatten tillgänglig på surfplatta, telefon eller andra formfaktorer?

Nej, chattfönstret är bara tillgängligt på webbklienten [!INCLUDE[web_client](includes/web_client.md)].

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Jag använder inte Business Central på engelska. Vilka är mina alternativ?

För närvarande är chatten endast tillgänglig på engelska. Du kan ändra ditt användarspråk till engelska i [Mina inställningar](ui-change-basic-settings.md#language).

## <a name="what-version-of-business-central-do-i-need-for-chat"></a>Vilken Business Central-version behöver jag för chatt?

Chatt är tillgänglig som allmänt tillgänglig förhandsversion från version 24.0 (2024 utgivningscykel 1).

## <a name="does-chat-work-with-my-customizations"></a>Fungerar chatten med mina anpassningar?

Det beror på vilken typ av fråga du ställer till Copilot. Till exempel:

- Om du ställer frågor för att hitta poster kan den hitta poster i dina anpassade tabeller som använder anpassade fält.
- När du ber Copilot om en förklaring eller vägledning har den inte tillgång till någon information om dina anpassningar eller dokumentation för dina tillägg.

## <a name="how-do-i-open-a-record-or-page-with-chat"></a>Hur öppnar jag en post eller sida med chatt?

När du ber Copilot att söka efter poster i [!INCLUDE[prod_short](includes/prod_short.md)] visas alla poster som hittas som valbara paneler eller länkar i chattfönstret. I förhandsversionen navigerar Copilot inte automatiskt till någon sida.

## <a name="why-do-i-get-different-answers-from-copilot-for-the-same-question"></a>Varför får jag olika svar från Copilot på samma fråga?

Copilot kan ibland svara på olika sätt. Svaren är inte alltid identiska.

## <a name="how-do-i-use-the-copy-function-on-chat-messages"></a>Hur använder jag kopieringsfunktionen i chattmeddelanden?

Du kan använda knappen Kopiera för att kopiera ett meddelande från tidigare i konversationen med Copilot, klistra in det i inmatningsrutan för att försöka igen eller prova en variant av meddelandet till Copilot.

## <a name="can-i-customize-or-extend-chat"></a>Kan jag anpassa eller utöka chatten?

I förhandsversionen kan chattfönstret och Copilot-svar inte ändras på något sätt via anpassning, tillägg eller anpassning.

## <a name="does-copilot-search-for-data-in-other-companies-or-environments"></a>Söker Copilot data i andra företag eller miljöer?

Copilot söker bara efter poster i det företag du för närvarande är inloggad på. Den söker inte efter data i flera miljöer eller företag.

## <a name="what-can-i-do-if-the-chat-pane-doesnt-show"></a>Vad kan jag göra om chattfönstret inte visas?

Kontrollera att ditt användarspråk i **Mina inställningar** är inställt på engelska och att din miljö är av version 24.0 eller senare. På sidan Copilot- och AI-funktioner kontrollerar du att administratörer har aktiverat samtycke för data mellan geografiska områden och har aktiverat chatt. Kontrollera också att din miljölokalisering inte är Kanada.

Om du fortfarande inte ser chatten med Copilot-funktionen är det möjligt att Microsoft fortfarande lanserar detta till din region. Copilot lanseras till amerikanska kunder först i april 2024 och kommer sedan under veckorna att distribueras till andra lands-/regionslokaliseringar.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Varför visar Copilot bara tre poster i chattfönstret?

När du ber Copilot att hitta poster avgör sättet du formulerar frågan på hur Copilot identifierar och använder filter på sidor för att hitta det du letar efter. För att hålla svaren kortfattade visas högst tre postpaneler i chattfönstret, även när Copilot hittar mer relevanta poster.

## <a name="why-does-copilot-give-incorrect-answers-to-calculations"></a>Varför ger Copilot felaktiga svar på beräkningar?

I förhandsversionen kan Chatt med Copilot hjälpa dig att hitta poster, förklara begrepp och vägleda dig till hur du utför uppgifter i Business Central. Andra användningsfall stöds inte, till exempel att lägga till ett fält över poster eller beräkna det genomsnittliga månadsbeloppet. Vi hoppas kunna lägga till grundläggande matematiska förmågor till Copilot i framtiden.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kan jag använda tal i stället för att skriva mina uppmaningar?

Du kan chatta med Copilot genom att använda röstinmatning för att prata i stället för att skriva dina ord i chattfönstret. Röstinmatning använder taligenkänning online och är tillgängligt med Windows. Om du vill använda rösten aktiverar du chattmeddelanderutan, använder sedan <kbd>Windows</kbd>+<kbd>H</kbd>-kortkommando och börjar prata. Mer information finns i [Använda röstinmatning för att prata i stället för att skriva på datorn](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Nästa steg

- [Chatt med Copilot (förhandsversion)](chat-with-copilot.md)

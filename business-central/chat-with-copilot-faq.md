---
title: Vanliga frågor och svar om chatt med Copilot
description: Den här artikeln svarar på några vanliga frågor om att chatta med Copilot i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# Vanliga frågor och svar om chatt med Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Den här artikeln svarar på några vanliga frågor om att chatta med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du har frågor om AI och chatt läser du [Vanliga frågor om ansvarsfull AI för chatt med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Kan administratörer bevilja eller neka enskilda användare behörighet att få åtkomst till chatten?

Nej, det finns ingen behörighet eller behörighet för chatt. Om chatten är aktiverad på sidan [Copilot- och AI-funktioner](enable-ai.md) har alla användare i en miljö åtkomst till chatten.
 
## Är chatten tillgänglig på surfplatta, telefon eller andra formfaktorer?

Nej, chattfönstret är bara tillgängligt på webbklienten [!INCLUDE[web_client](includes/web_client.md)].

## Jag använder inte Business Central på engelska. Vilka är mina alternativ?

För närvarande är chatten endast tillgänglig på engelska. Du kan ändra ditt användarspråk till engelska i [Mina inställningar](ui-change-basic-settings.md#language).

## Vilken Business Central-version behöver jag för att uppleva chatt?

Chatt är tillgänglig som allmänt tillgänglig förhandsversion från version 24.0 (2024 utgivningscykel 1).

## Fungerar chatten med mina anpassningar?

Det beror på vilken typ av fråga du ställer till Copilot. Till exempel:

- När du ställer frågor för att hitta poster kan Copilot hitta poster i dina anpassade tabeller som identifieras med hjälp av anpassade fält.
- När du ber om en förklaring eller vägledning har Copilot inte tillgång till någon information om dina anpassningar eller dokumentation för dina tillägg.

## Copilot verkar aldrig öppna skivan eller sidan jag bad om. Vad gör jag för fel?

När du ber Copilot att söka efter poster i [!INCLUDE[prod_short](includes/prod_short.md)] visas alla poster som hittas som valbara paneler eller länkar i chattfönstret. I förhandsversionen navigerar Copilot inte automatiskt till någon sida.

## Svaren jag får från Copilot varierar trots att jag ställer samma fråga. Är det ett fel?

Copilot kan ibland svara på olika sätt. Svaren är inte nödvändigtvis identiska.

## När ska jag använda kopieringsfunktionen i chattmeddelanden?

Du kan använda knappen Kopiera för att kopiera ett meddelande från tidigare i konversationen med Copilot, klistra in det i inmatningsrutan för att försöka igen eller prova en variant av meddelandet till Copilot.

## Hur anpassar eller utökar jag chatten?

I förhandsversionen kan chattfönstret och Copilot-svar inte ändras på något sätt via anpassning, tillägg eller anpassning.

## Hittar Copilot data i andra företag eller miljöer?

Copilot söker bara efter poster i det företag du för närvarande är inloggad på&mdash;, även om din organisation använder flera miljöer eller företag för att åtskilja data.

## Chattfönstret Copilot visas inte. Vad kan jag göra?

Kontrollera att ditt användarspråk i Mina inställningar är inställt på engelska och att din miljö är av version 24.0 eller senare. På sidan Copilot- och AI-funktioner kontrollerar du att administratörer har aktiverat samtycke för data mellan geografiska områden och har aktiverat chatt. Kontrollera att din miljölokalisering inte är Kanada.

Om du fortfarande inte ser chatten med Copilot-funktionen är det möjligt att Microsoft fortfarande rullar ut funktionen till din region. Copilot distribueras först till kunder i USA i april 2024 och distribueras sedan under veckorna till andra lokaliseringar i länder/regioner.

## Varför visar Copilot bara tre poster i chattfönstret?

När du ber Copilot att hämta poster avgör hur du formulerar frågan hur Copilot identifierar och tillämpar filter på sidor för att hitta det du letar efter. För att hålla svaren kompakta och koncisa visas högst tre postpaneler i chattfönstret, även när Copilot hittar ett större antal relevanta poster.

## Copilot returnerar felaktiga svar på summor och andra beräkningar

I förhandsversionen kan Chat with Copilot hitta poster, förklara begrepp och vägleda dig till hur du utför uppgifter i Business Central. Andra användningsfall stöds inte, till exempel att lägga till ett fält över poster eller beräkna det genomsnittliga månadsbeloppet. Vi hoppas kunna lägga till grundläggande matematiska förmågor till Copilot i framtiden.

## Kan jag använda tal i stället för att skriva mina uppmaningar?

Du kan chatta med Copilot genom att använda röstinmatning för att prata i stället för att skriva dina ord i chattfönstret. Röstinmatning använder taligenkänning online och är tillgängligt med Windows. För att använda röst, aktivera chattmeddelanderutan, använd sedan Windows <kbd>H-genvägen</kbd>+<kbd></kbd> och börja tala. Mer information finns [i Använda röstinmatning för att prata i stället för att skriva på datorn](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Nästa steg

[Chatt med Copilot (förhandsversion)](chat-with-copilot.md)

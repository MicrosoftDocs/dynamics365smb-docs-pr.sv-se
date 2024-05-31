---
title: Marknadsföringstext för AI-baserad artikel (förhandsversion) med vanliga frågor och svar om Copilot
description: Få svar på vanliga frågor om AI-genererad textkapacitet med Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# Marknadsföringstext för AI-baserad artikel (förhandsversion) med vanliga frågor och svar om Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

I den här artikeln används frågor och svar för att förklara viktiga aspekter på AI-tekniken bakom Copilot och den text som genereras.

## [Allmänt](#tab/general)

### Vad är Copilot?

Copilot tillhandahåller AI-genererade text förslag för artiklar i Business Central. Den är avsedd för användare som skriver marknadsföringstext för artiklar för att hjälpa dem att producera och övertygande innehåll. Några viktiga fördelar:

- Minskar den tid som används vid copywriting, vilket kan påskynda en tid-till-marknad för artiklar som säljs i onlinebutiker.
- Låser upp kreativitet för att ge mer engagerande produktbeskrivningar.
- Förbättrar konsistensen av marknadsföringsmaterial för produktlinjer.

Användare bör ta hänsyn till AI-genererad text som ett förslag som måste granskas och redigeras med precision innan den är allmänt tillgänglig.

### Varför är inte Copilot tillgängliga för marknadsföringstext på mina artiklar på Business Central?

För att Copilot ska vara tillgänglig, måste följande villkor vara uppfyllda:

- Det språk som du använder i Business Central måste vara engelska. Alla tillgängliga engelska språk kommer att fungera, t.ex. engelska (USA), engelska (Storbritannien) eller engelska (Sydafrika).

  Om du vill ändra språk väljer du ikonen **Inställningar** i det övre högra hörnet ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") > **Mina inställningar** > **Språk**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md#language).
- Du måste använda Business Central Online version 22 eller senare (om du är en befintlig kund) eller en provversion.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Om du vill kontrollera versionen markerar du frågetecknet i det övre högra hörnet och **Hjälp och support**. Under **Felsökning**, leta efter programversionen. För information om hur du får rätt förhandsgranskningsversion, gå till [Komma igång med Business Central förhandsversionen](ai-preview-getstarted.md).
- Funktionen **Skapa AI-baserade produktbeskrivningar med Copilot** måste aktiveras.

   Om du vill ha mer information går du till [Aktivera eller inaktivera funktionen "Skapa AI-baserad produktbeskrivningar med Copilot"](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- En administratör har samtyckt med villkoren.

   För mer information, gå till [Samtycke till eller avvisa förhandsgranskning och sekretessvillkor för alla användare](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### Är Copilot tillgänglig för förhandsversion i Business Central lokal?

Nej, den stöds inte för närvarande i Business Central lokal.

### Hur fungerar Copilot, var kommer den föreslagna texten från?

Copilot använder [Microsofts Azure-tjänst OpenAI](/azure/cognitive-services/openai/overview) för att få tillgång till kraftfulla språkmodeller som analyserar och genererar naturligt språk. Dessa modeller har tränats på en stor mängd textdatauppsättningar. Som ett resultat kan Copilot generera föreslagna, personliga svar på engelska baserat på en minimal mängd indata, som en artikels attribut, kategori eller beskrivning. 

### Vilken är kvaliteten på den text som föreslås av Copilot?

Eftersom den underliggande tekniken bakom Copilot använder AI som har tränats på ett brett utbud av källor, är det genererade innehållet inte alltid sakligt eller lämpligt. Vissa förslag kan till och med innehålla tveksamt eller olämpligt innehåll. Det är ditt ansvar att granska och redigera de förslag som har skapats för att säkerställa att det är korrekt och lämpligt.

För information om olämpliga förslag, gå till vad som [Vad har gjorts med kränkande och skadliga textförslag?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### Hur kan jag förbättra de förslag jag får från en Copilot?

Det finns några saker du kan göra för att få ut så mycket som möjligt av de förslag som medföljer Copilot:

- Lägga till fler attribut till en artikel för att framhäva de specifika egenskaper som du är intresserad av.
- Ändra alternativen för tonfall och betoning på kvalitet för att matcha dina personliga inställningar.
- Förbättra artikelns beskrivning.
- Kontrollera att elementet är tilldelat till den lämpligaste kategorin.

Mer information finns i [Förbättra och anpassa textförslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

### Vad händer om jag inte är nöjd med den genererade texten?

För att hjälpa oss att förbättra texten, välj **Är detta ett bra förslag?** på sidan **Skapa med Copilot** som du kan svara med en tumme upp (jag gillar) eller tumme ner (behöver förbättras).

![Visar artikelkort med fönstret marknadsföringstext](media/create-with-copilot-window-feedback.png)

### Kan administratörer inaktivera Copilot? Hur gör jag?

Business Central erbjuder administratörer två sätt att inaktivera Copilot i förhandsgranskningen:

- Godkänn inte Azures OpenAI sekretessmeddelande för alla användare.

  eller

- Inaktivera funktionen **Skapa AI-baserade produktbeskrivningar med Copilot** på sidan **Funktionshantering**.

För att lära dig mer [Konfigurera marknadsföringstext (förhandsversion) för AI-baserad artikel med Copilot som en administratör](enable-ai.md).

## [Rättvisa](#tab/fairness)

### Fungerar Copilot med andra språk än engelska?

För närvarande stöder Copilot endast engelska. Felaktiga svar kan returneras om användarna talar med systemet på andra språk än engelska.

## [Den mänskliga kontrollen](#tab/oversight)

### Vad har man gjort åt kränkande och skadliga textförslag?

Azure-tjänsten OpenAI lagrar uppmaningar och slutföranden från tjänsten för att övervaka missbruk och för att utveckla och förbättra kvaliteten på Azures OpenAI innehållshanteringssystem. [Lär dig mer om innehållshantering och filtrering.](/azure/cognitive-services/openai/concepts/content-filter)

Behöriga Microsoft-anställda kan komma åt dina snabb- och ifyllnadsdata som har utlöst våra automatiska system i syfte att undersöka och verifiera potentiellt missbruk. För kunder som har distribuerat Azure-tjänsten OpenAI i EU finns de auktoriserade Microsoft-medarbetarna i EU. Dessa data kan användas för att förbättra våra system för innehållshantering.I händelse av ett bekräftat policyfel kan vi be dig att vidta omedelbara åtgärder för att åtgärda problemet och förhindra ytterligare missbruk. Om det inte går att adressera problemet kan det leda till att Azure OpenAI-resursåtkomst upphör att fungera.

Mer information finns i [Data, sekretess och säkerhet för Azure-tjänsten OpenAI](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### Kan jag välja bort processen för loggning och mänsklig granskning?  

Som en del av tillhandahållandet av förhandsversionerna av Azure OpenAI behandlar och lagrar Microsoft kunddata som skickas till tjänsten, samt utdatainnehåll, i syfte att övervaka och förhindra missbruk eller skadliga användningar eller utdata av tjänsten och för att utveckla, testa och förbättra funktioner som utformats för att förhindra missbruk av eller skadliga utdata från tjänsten. 

Auktoriserad Microsoft-personal kan granska data som har utlösta våra automatiserade system för att undersöka och kontrollera eventuella missbruk och kan vid begränsade stickprov av termer som inte har flaggats av våra automatiserade system för att säkerställa till att systemen fungerar som de ska. Behörig Microsoft-personal kan också komma åt och använda dessa data för att förbättra våra system som övervakar och förhindrar grova eller skadliga användningar av tjänsten.Läs mer om [villkor för förhandsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Sekretess](#tab/privacy)

### Vilken data samlar kapaciteten in? Hur används uppgifterna?

Förmågan samlar ditt svar till frågan **Är detta ett bra förslag?** på sidan **Skapa med Copilot** som kan vara antingen tumme upp (jag gillar) eller tummen ner (behöver förbättras).

Vi använder dessa uppgifter för att utvärdera och förbättra kvaliteten på kapaciteten. Mer information om vilka data som samlas in finns i villkoren för [förhandsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Visar artikelkort med fönstret marknadsföringstext](media/create-with-copilot-window-feedback.png)

---

## Se även

[Översikt över marknadsföringstext för AI-baserad artikel med Copilot](ai-overview.md)  
[Konfigurera marknadsföringstext för AI-baserad artikel med Copilot som en administratör](enable-ai.md)  
[Skapa marknadsföringstext för artiklar som använder Copilot](item-marketing-text.md)  


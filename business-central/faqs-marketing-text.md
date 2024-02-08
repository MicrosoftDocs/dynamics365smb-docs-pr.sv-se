---
title: Frågor och svar om marknadsföringstext för artikel
description: 'Vanliga frågor och svar om ansvarsfull AI innehåller information om AI-tekniken som används i Business Central, tillsammans med viktiga överväganden och detaljer om hur AI används, hur den testades och utvärderades och eventuella specifika begränsningar.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-marketing-text-suggestions-with-copilot"></a>Vanliga frågor för marknadsföringstextförslag med Copilot

Dessa vanliga frågor beskriver AI-effekten av [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] funktionen i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-item-marketing-text-suggestions"></a>Vad är textförslag för artikelmarknadsföring?

Copilot tillhandahåller skrivhjälp för användare som ansvarar för att skapa marknadsföringstext (kallas även kopia) för objekt i [!INCLUDE[prod_short](includes/prod_short.md)]. Den här funktionen är känd som [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] funktionen ger skrivhjälp för användare som ansvarar för att skapa marknadsföringstext (även känd som *kopia*) på objekt i [!INCLUDE[prod_short](includes/prod_short.md)].

Funktionen är tillgänglig på alla artikelkort i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du vill använda den öppnar du bara ett objekt och väljer sedan **Marknadsföringstext** > **Utkast med Copilot**. Den här åtgärden genererar automatiskt ett textförslag som är engagerande, kreativt och specifikt för objektet som visas. Förslagen baseras på olika indata, inklusive:

- Objektets attribut, kategori och namn.
- Personliga skrivstilspreferenser, som tonfall, betonade kvalitet, format och längd.

Du kan ändra värdet på dessa inmatningsalternativ för att påverka resultatet av den AI-genererade texten. Innan du sparar ett förslag kan du enkelt granska och redigera det för att se om det stämmer eller prova ett annat förslag.

Några viktiga fördelar med den här funktionen är:

- Minskar den tid som används vid copywriting, vilket kan påskynda en tid-till-marknad för artiklar som säljs i onlinebutiker.
- Låser upp kreativitet för att ge mer engagerande produktbeskrivningar.
- Förbättrar konsistensen av marknadsföringsmaterial för produktlinjer.

## <a name="what-are-the-systems-capabilities"></a>Vilka funktioner finns i systemet?

Funktionen [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] använder [Microsoft Azure OpenAI Service](/azure/cognitive-services/openai/overview) för att komma åt kraftfulla språkmodeller som analyserar och genererar naturligt språk. Dessa modeller har tränats på en stor mängd textdatauppsättningar. Som ett resultat kan Copilot generera föreslagna, personliga svar på engelska baserat på en minimal mängd indata, som en artikels attribut, kategori eller beskrivning. 

## <a name="what-is-the-systems-intended-use"></a>Vad är systemets avsedda användning?

Den här funktionen är avsedd att hjälpa användare att skapa marknadsföringstext för artiklar i [!INCLUDE[prod_short](includes/prod_short.md)]. Författare använder funktionen för att snabbt få övertygande och engagerande textförslag, som sedan granskas och redigeras för noggrannhet. 

## <a name="how-was-item-marketing-text-evaluated-what-metrics-are-used-to-measure-performance"></a>Hur utvärderades artikelmarknadsföringstext? Vilka mått används för att mäta prestanda?

- Funktionen genomgick omfattande tester där många texter på olika språk utvärderades av språkexperter mot olika kriterier. Testningen baserades på [!INCLUDE[prod_short](includes/prod_short.md)] demonstrationsdata och andra fiktiva produktkataloger.
- Den här funktionen är byggd i enlighet med Microsofts standard för ansvarsfull AI. [Läs mer om ansvarsfull AI från Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hur övervakar Microsoft kvaliteten på genererat innehåll?

Microsoft har olika system på plats för att säkerställa att Copilot-funktionerna fortsätter att fungera och genererar innehåll av högsta kvalitet.

- Användare har möjlighet att ge feedback för att rapportera olämpligt innehåll och förbättra funktionaliteten.

  - Om du stöter på olämpligt genererat innehåll rapporterar du det till Microsoft med hjälp av det här feedbackformuläret: [Rapportera missbruk](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft kan inaktivera Copilot-drivna funktioner för utvalda kunder om missbruk av funktionen upptäcks. 

  - Vi spårar feedback från användare av [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] för att hjälpa oss att förbättra förslagen. 

    Du ger feedback genom att använda ikonen gilla (tummen upp) eller ogilla (tummen ned) på sidan **Copilot** i [!INCLUDE[prod_short](includes/prod_short.md)]. Vi samlar in telemetrin för dessa gester för varje AI-utdata som du skickar feedback för.

    ![Visar artikelkort med fönstret marknadsföringstext](media/create-with-copilot-window-feedback.svg)

- I Azure OpenAI Service lagras frågor och slutprodukter från tjänsten som används för att övervaka missbruk och för att utveckla och förbättra kvaliteten på Azure OpenAI innehållshanteringssystem. [Lär dig mer om innehållshantering och filtrering.](/azure/cognitive-services/openai/concepts/content-filter). Dina företagsdata används inte för att träna AI-modeller i Azure OpenAI Service.

   Auktoriserade Microsoft-anställda kan få åtkomst till dina meddelanden och kompletteringsdata som har utlöst våra automatiserade system i syfte att undersöka och verifiera potentiellt missbruk. För kunder som använder [!INCLUDE[prod_short](includes/prod_short.md)] i Europeiska Unionen kommer de auktoriserade Microsoft-anställda att finnas i Europeiska Unionen. Dessa data kan användas för att förbättra våra system för innehållshantering. I händelse av ett bekräftat policyfel kan vi be dig att vidta omedelbara åtgärder för att åtgärda problemet och förhindra ytterligare missbruk. Om det inte går att adressera problemet kan det leda till att Azure OpenAI-resursåtkomst upphör att fungera.

   Mer information finns i [Data, sekretess och säkerhet för Azure OpenAI Service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## <a name="is-there-a-logging-and-human-review-process-as-part-of-azure-openai-service-and-if-so-can-i-opt-out"></a>Finns det en process för loggning och mänsklig granskning som en del av Azure OpenAI Service och kan jag i så fall avanmäla mig?

Som en del av att tillhandahålla Azure OpenAI Service förhandsversion, behandlar Microsoft och lagrar kunddata som skickas till tjänsten, samt utlämnande av innehåll, i syfte att övervaka och förebygga grova eller skadliga användningar av tjänsten och utveckling, testning och förbättring av möjligheterna avsedda att förhindra missbruk av och/eller skadliga resultat från tjänsten. 

Auktoriserad Microsoft-personal kan granska data som har utlösta våra automatiserade system för att undersöka och kontrollera eventuella missbruk och kan vid begränsade stickprov av termer som inte har flaggats av våra automatiserade system för att säkerställa till att systemen fungerar som de ska. Behörig Microsoft-personal kan också komma åt och använda dessa data för att förbättra våra system som övervakar och förhindrar grova eller skadliga användningar av tjänsten.Läs mer om [villkor för förhandsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

För att Microsoft ska kunna skydda tjänsten och dess kunder är det inte möjligt att välja bort loggnings- och granskningsprocesser.

## <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Vilken data samlar kapaciteten in? Hur används uppgifterna?

Funktionen för marknadsföringstextförslag samlar in de minsta data som krävs av Business Central för att erbjuda tjänsten. Mer information finns i [Dynamics 365-termer för Azure OpenAI-drivna funktioner](https://go.microsoft.com/fwlink/?linkid=2236010).

Funktionen samlar också in data från den feedback som användarna kan ge med hjälp av ikonerna för liknande (tummen upp) eller ogillar (tummen ned) högst upp på sidan **Copilot**. Data är anonym och inkluderar valet av gilla eller ogilla, anledningen till ogillandet om den anges och den Copilot-funktion som feedbacken gäller. Vi använder dessa uppgifter för att utvärdera och förbättra kvaliteten på kapaciteten.

## <a name="what-are-the-limitations-of--how-can-users-minimize-the-impact-of-the-includefeature-marketing-text-suggestions-limitations-when-using-the-system"></a>Vilka är de begränsningarna för [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? Hur kan användare minimera påverkan av [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]-begränsning när de använder systemet?

- Eftersom den underliggande tekniken bakom funktionen använder AI som har tränats på ett brett utbud av källor, är det genererade innehållet inte alltid sakligt eller lämpligt. Vissa förslag kan till och med innehålla tveksamt eller olämpligt innehåll. Det är ditt ansvar att granska och redigera de förslag som har skapats för att säkerställa att det är korrekt och lämpligt.
- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Felaktiga svar kan returneras om användarna interagerar med systemet på andra språk än de språk som stöds. Felaktig text kan också genereras när användarens språk och primära dataspråk i [!INCLUDE[prod_short](includes/prod_short.md)] databasen inte är identiska.


## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-system"></a>Vilka driftfaktorer och inställningar gör det möjligt att på ett effektivt och ansvarigt sätt använda systemet?

Det finns några saker du kan göra för att få ut så mycket som möjligt av funktionen:

- Lägga till fler attribut till en artikel för att framhäva de specifika egenskaper som du är intresserad av.
- Ändra alternativen för tonfall och betoning på kvalitet för att matcha dina personliga inställningar.
- Förbättra artikelns beskrivning.
- Kontrollera att elementet är tilldelat till den lämpligaste kategorin.

Mer information finns i [Förbättra och anpassa textförslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Granska alltid förslagen på noggrannhet innan du sparar dem och publicerar dem för offentlig användning.


## <a name="see-also"></a>Se även

- [Förslag på marknadsföringstext](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

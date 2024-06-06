---
title: Vanliga frågor och svar om analyshjälp (förhandsversion)
description: 'Dessa vanliga frågor och svar innehåller information om AI-tekniken som används för att analysera data på sidor i Business Central. Den innehåller också viktiga saker att tänka på och information om hur AI används, hur den har testats och utvärderats samt eventuella specifika begränsningar.'
ms.date: 02/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-analysis-assist-preview"></a>Vanliga frågor och svar om analyshjälp (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Dessa vanliga frågor beskriver AI-effekten av analyshjälpfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-analysis-assist"></a>Vad är analyshjälp?

Analyshjälp är en Copilot som ger hjälp med att arbeta med [dataanalysläget](analysis-mode.md) i Business Central. Med dataanalysläget kan du ordna, aggregera och sammanfatta data på sidor och frågor för att göra dem mer lämpade för att analysera och extrahera meningsfulla insikter. Med analyshjälp kan du automatiskt skapa vyn över de data du vill analysera genom att uttrycka dina behov på ett enkelt och naturligt språk, till exempel "visa leverantörer efter plats sorterade efter antal inköp". Analyshjälp gör det enklare att arbeta med data utan att behöva komplicerade tekniska kunskaper.

## <a name="what-are-capabilities-of-analysis-assist"></a>Vilka är funktionerna för analyshjälp?

Analyshjälp bygger på utvecklarverktygen för Copilot i Business Central. Den använder Azure Open AI Azure OpenAI för att konvertera ostrukturerade instruktioner till en strukturerad design för att visa data i analysläge, utan att skapa, ändra eller uppdatera själva kundens affärsdata.

## <a name="what-is-the-intended-use-of-analysis-assist"></a>Vad är den avsedda användningen av analyshjälp?

Den avsedda användningen av analyshjälp är att hjälpa till att skapa analysflikar i dataanalysläget för att presentera data på ett sätt som gör det lättare att dra slutsatser. Det är dock viktigt att notera att analyshjälp inte ger direkta insikter eller slutsatser om data. Det är ett verktyg som hjälper användare att organisera och visa sina data. Det är emellertid upp till användaren att extrahera användbar information, upptäcka trender och fatta välgrundade beslut för att driva affärsvärde.

## <a name="how-was-analysis-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hur utvärderades analyshjälp? Vilka mått används för att mäta prestanda?

- Funktionen genomgick omfattande tester baserat på [!INCLUDE[prod_short](includes/prod_short.md)] demonstrationsdata och andra fiktiva produktkataloger. Copilot fick många uppmaningar på de engelska språk som stöds. Prompterna omfattade ett brett spektrum av dataanalysinstruktioner och stilar för att uttrycka avsikt. Resultaten utvärderades mot noggrannhet, relevans och säkerhet.

- Funktionen är byggd i enlighet med Microsofts standard för ansvarsfull AI. [Läs mer om ansvarsfull AI från Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hur övervakar Microsoft kvaliteten på genererat innehåll?

Microsoft har olika system inrättade för att säkerställa att innehåll som genereras av Copilot är av högsta kvalitet, upptäcka missbruk och säkerställa säkerheten för våra kunder och deras data.

Användare har möjlighet att ge feedback på varje Copilot-svar och rapportera felaktigt eller olämpligt innehåll för att hjälpa Microsoft att förbättra den här funktionen.

- Om du stöter på olämpligt genererat innehåll rapporterar du det till Microsoft med hjälp av det här feedbackformuläret: [Rapportera missbruk](https://go.microsoft.com/fwlink/?linkid=2249810).

- Vi analyserar och använder användarfeedback om funktionen för att hjälpa oss att förbättra svaren.

  Du ger feedback genom att använda ikonen gilla (tummen upp) eller ogilla (tummen ned) på rutan **Copilot** i [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft kan inaktivera Copilot-drivna funktioner för utvalda kunder om missbruk av funktionen upptäcks.

## <a name="what-are-the-limitations-of-analysis-assist-how-can-users-minimize-the-impact-of-the-analysis-assist-limitations-when-using-the-system"></a>Vilka är begränsningarna för analyshjälp? Hur kan användare minimera effekten av analyshjälp begränsningar när de använder systemet?

- Allmänna AI-begränsningar

  AI-system är värdefulla verktyg, men de är icke-deterministiska. Innehållet de genererar kanske inte är korrekt. Därför är det viktigt att använda ditt omdöme för att granska och verifiera svaren i Copilot innan du fattar beslut som kan påverka intressenter som kunder och partner.

- Språkliga och geografiska begränsningar:

  - Analyshjälp stöds endast på engelska för följande språk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Om visningsspråket i Business Central inte är ett av de angivna språken är funktionen inte tillgänglig.

  - Kvaliteten på svaren kan vara lägre om:
    - Språkspråket i Business Central är något annat än en-US.
    - Språkinställningen för användaren i Business Central skiljer sig från det primära språket för affärsdata i [!INCLUDE[prod_short](includes/prod_short.md)] databasen.
  
  - Geografisk begränsning:
  
    Funktionen är tillgänglig i alla som stöds [Business Central länder/regioner](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) utom Kanada, på grund av regelspråksefterlevnad. Funktionen använder Microsoft Azure OpenAI Service, som för närvarande endast är tillgänglig för Business Central i vissa geografiska regioner. Om din miljö finns i ett land/en region där Azure OpenAI-tjänsten inte är tillgänglig måste administratörer tillåta att data flyttas mellan geografiska områden. [Läs mer](/dynamics365/business-central/ai-copilot-data-movement).

- Vissa bransch-, produkt- och ämnesbegränsningar:

  Organisationer som är verksamma inom vissa affärsområden, till exempel medicinska, läkemedel, juridiska och vapen, kan uppleva lägre servicekvalitet.

## <a name="what-data-does-analysis-collect-and-how-is-it-used"></a>Vilka data samlar analysen in och hur används den

Funktionen för analyshjälpförmåga samlar in de minsta data som krävs av Business Central för att erbjuda tjänsten. Microsoft använder inte dina företagsdata, inklusive den text du skickar till Copilot, för att träna de grundläggande modellerna till förmån för andra. Mer information finns i [Dynamics 365-termer för Azure OpenAI-drivna funktioner](https://go.microsoft.com/fwlink/?linkid=2236010).

Samlar också in data från den feedback som användarna kan ge med hjälp av ikonerna för liknande (tummen upp) eller ogillar (tummen ned) analyshjälp på sidan **Copilot**. Data är anonym och inkluderar valet av gilla eller ogilla, anledningen till ogillandet om den anges och den Copilot-funktion som feedbacken gäller.

## <a name="see-also"></a>Se även

[Analysera data med Copilot (förhandsversion)](analysis-assist.md)

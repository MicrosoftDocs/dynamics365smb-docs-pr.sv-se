---
title: Klassificera datakänslighet
description: Du måste ange vilken typ av data du sparar om olika personer så att du kan svara på begäranden från dessa (datasubjekten).
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.search.form: 1752
ms.date: 06/14/2021
---

# <a name="classifying-data-sensitivity-fields" />Fältet Klassificera datakänslighet
Om du vill klassificera de fält som innehåller känsliga eller personliga data kan en Microsoft-partner ange egenskapen ```DataClassification``` för fält. Detta kräver åtkomst till databastabeller, antingen via utvecklingsmiljön eller genom att köra ett skript för Windows PowerShell. Mer information finns i [Klassificera data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Som kund kan du lägga till en andra klassificeringsnivå genom att ange känslighetsnivåer för de data som du lagrar i standard- respektive anpassade fält. Klassificering av datakänslighet gör att du vet var i ditt system du förvarar personuppgifter och gör det enklare att svara på förfrågningar från datasubjekt. Om exempelvis en kontakt eller en kund ber dig att exportera deras personuppgifter. Mer information finns i [Svara på begäranden om personuppgifter](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft tillhandahåller denna funktion för klassificering av datakänslighet endast i komfortsyfte. Det är ditt ansvar att klassificera uppgifterna korrekt samt att uppfylla alla lagar och regelverk som gäller för dig. Microsoft frånsäger sig allt ansvar gentemot alla anspråk som kan relateras till din klassificering av data.  

I följande tabell beskrivs vilka datakänslighetnivåer som du kan tilldela.

|Känslighet|Description|
|----|----|
|Känslig | Information om ett datasubjekts rasmässiga eller etniska ursprung, politiska åsikter, religiösa övertygelse, engagemang i fackföreningar, fysiska eller psykiska hälsa, sexualitet eller information om brottsliga handlingar. |
|Personlig | Information som kan användas för att identifiera ett datasubjekt, antingen direkt eller i kombination med annan data eller information.|
|Konfidentiell | Affärsdata som du använder för redovisning eller andra affärsändamål och inte vill visa för andra enheter. Detta kan till exempel omfatta transaktioner.|
|Normal | Allmänna uppgifter som inte tillhör andra kategorier.|

## <a name="how-do-i-classify-my-data" />Hur klassificerar jag mina data?
Klassificeringen av känsligheten för ett stort antal fält ett i taget skulle ta lång tid. För att skynda på processen tillhandahåller vi verktyg som kan användas för att massklassificera fältens känsligt och därefter finjustera klassificeringen för specifika fält. Du hittar verktyg i kalkylarket för klassificering av data som finns att tillgå i rollcentret för administrering av användare, användargrupper och behörigheter. Du måste vara systemadministratör för att kunna använda kalkylarket.

> [!Important]
> När du öppnar kalkylarket Dataklassificering för första gången är det tomt. Du måste köra guiden Dataklassificering om du vill generera fältlistan. Starta guiden genom att välja åtgärden **Konfigurera dataklassificering**.

Kalkylbladet Dataklassificering låter dig göra saker som exempelvis:  

* Använd guiden Dataklassifiering för att exportera dina fält till ett Excel-kalkylblad där du kan massklassificera dem. Att använda Excel-kalkylbladet är särskilt användbart om du samarbetar med en Microsoft-partner. När du har uppdaterat kalkylbladet kan du använda guiden för att importera och tillämpa klassificeringarna. Du kan också använda guiden för att klassificera fält manuellt.  
* Välj ett fält och filtrera sedan listan för att söka efter liknande fält som med stor sannolikhet tillhör samma klassificering som fältet du baserade sökningen på.  
* Undersöka ett fält genom att visa innehållet.  

> [!Tip]
> Vi har definierat känslighetsklassificeringsprov för tabeller och fält i demonstrationsföretaget Cronus. Du kan använda dessa klassificeringar som inspirationskälla när du klassificerar egna tabeller och fält.

## <a name="see-also" />Se även

[Klassificering av Data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

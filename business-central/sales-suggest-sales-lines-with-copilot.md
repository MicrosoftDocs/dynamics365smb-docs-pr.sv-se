---
title: Föreslå försäljningsrader med Copilot
description: Lär dig hur du föreslår rader på försäljningsorder med Copilot.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# Föreslå rader på försäljningsdokument med Copilot (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

I den här artikeln beskrivs hur du skapar försäljningsdokument snabbare genom att låta Copilot föreslå vilka artiklar som ska läggas till på rader i försäljningsdokument för dina kunder.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Om förslag på försäljningsrader med Copilot

Förslag på försäljningsrader med Copilot kan hjälpa dig att skapa rader i försäljningsdokument som försäljningsofferter, order och fakturor baserat på strukturerad inmatning eller naturligt språk. Funktionen är inte en allmän chatt, utan en mycket specifik och integrerad upplevelse som du kan använda på försäljningsdokument. Funktionen erbjuder två olika färdigheter som hjälper dig att hitta data om enskilda produkter eller hela dokument.

* Hitta produkter

  Information som beskriver produkter lagras på flera ställen i [!INCLUDE [prod_short](includes/prod_short.md)]. Artikelnummer och beskrivningar lagras till exempel i tabellen **Artikel** , flera streckkoder lagras i tabellen **Artikelreferens** och produktegenskaper lagras i tabellen **Artikelattribut**. Medan du kanske frågar efter *röd cykel* kan den faktiska produkten vara *Crimson tourer*, där *cykel* är en produktkategori och *röd* är ett attribut.

* Sök dokument efter referens

  Människor upprepar ofta en tidigare order, eller åtminstone använder den som utgångspunkt. Men det kan vara svårt att hitta rätt order i en bunt med order. Du kanske kommer ihåg en del av orderns ID, som kan vara ett företagsnummer eller ett referensnummer som du fått från en kund. Att kunna använda prompter som *Behöver sista fakturan från april* bör hjälpa dig att hitta en order snabbare.

## Förutsättningar

* Försäljningsradförslag med Copilot aktiveras av en administratör. Mer information om hur du aktiverar AI-funktioner finns i [Konfigurera Copilot- och AI-funktioner](enable-ai.md).
* Du känner till hur man skapar försäljningsorder.

## Geografisk tillgänglighet

I följande tabell visas de geografiska Microsoft Azure-områden där funktionen är tillgänglig.

|Miljö Azure-regionen  |Geografiska områden för Azure OpenAI Service   |Administratörsåtgärd krävs för att låsa upp Copilot  |
|---------|---------|---------|
|Tyskland (norra, västra centrala)     | Sverige eller Schweiz        |  Ja       |
|Norge (öst, väst)     | Sverige eller Schweiz        | Ja     |
|Singapore     |         |         |
|Sydafrika (nord, väst)     |   USA      |   Ja      |
|Schweiz (nord, väst)     |  Sverige eller Schweiz       |    Ja     |
|Förenade Arabemiraten (nord, väst)     |    USA     |   Ja     |
|USA (centrala, östra, norra centrala, södra centrala, västra)     |   USA      |   Nr      |
|Europa (väst, norr)     |   Sverige eller Schweiz      |   Ja      |
|Asien-Stillahavsområdet     |         |         |
|Australien (sydöstra)     |   USA      |    Ja     |
|Sydamerika     |         |         |
|Indien (centrala, södra)     |    USA     |   Ja      |
|Japan (öst, väst)     |    USA     |    Ja     |
|Frankrike (central, södra)     |    Sverige eller Schweiz     |    Ja     |
|Sydkorea (centrala, södra)     |    USA     |    Ja     |

## Exempel på prompter

Föreslå att försäljningsrader med Copilot kan hantera en mängd olika snabba indata. Det här avsnittet innehåller några exempel på uppmaningar för olika scenarier som vi har testat.

### Exempel på förfrågan för att upprepa det tidigare dokumentet

Prompt: *Behöver alla produkter från faktura 103031*

### Under telefonsamtalet skriver användaren snabbt en lista över nödvändiga produkter och kvantiteter, inte alltid tillräckligt exakt eller med interna produktnamn

Prompt: *2 röda barncyyklar*

Observera att prompten fungerar, även med flera stavfel.

### En användare kopierar en förfrågan från en inkommande kommunikation och klistrar in den på sidan Förslag på försäljningsrader

Prompt: *Hej, jag är intresserad av att köpa några tillbehör till min XXXX bärbara dator, till exempel en trådlös mus, ett tangentbordsskydd och en väska. Jag undrar om du har några rekommendationer eller förslag på dessa artiklar. Har du några specialerbjudanden eller rabatter för lojala kunder som mig? Vänliga hälsningar, M*

Observera att XXXX dator inte ingår i sökningen.

## Föreslå rader på ett försäljningsdokument

I den här processen beskrivs hur du föreslår rader på en försäljningsorder. Stegen är desamma som för försäljningsofferter och fakturor.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
1. Öppna försäljningsordern.
1. På snabbfliken **Rader** klickar du på åtgärden **Hämta radförslag**.
1. I fönstret **Föreslå rader med Copilot** anger du prompten eller väljer en från promptguiderna.

## Granska, spara, ignorera eller återskapa förslag

När Copilot har föreslagit de objekt som ska läggas till på raderna granskar du förslagen och avgör om de är vad du vill ha:

* Om du vill ignorera en enstaka föreslagen rad markerar du den i listan och väljer sedan åtgärden **Ta bort rad**.
* Om du vill ignorera alla föreslagna rader och stänga Copilot-fönstret väljer du knappen Ignorera (papperskorg) bredvid knappen **Behåll**.
* Om du vill överföra raderna som visas i fönstret Copilot väljer du **Behåll**. 

Det finns ett fält för **Tillförlitlighet** som visar **Höga (80+)**, **Medel (60 – 80)** och **Låga (60-)** poäng och pekar dig på rader som behöver åtgärdas.

Det här steget bekräftar att du vill överföra raderna till ett försäljningsdokument. Du kan ta bort eller redigera de överförda raderna där också, eller ta bort hela dokumentet.

## Se även

[Vanliga frågor och svar om försäljningsradförslag med Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Konfigurera Copilot- och AI-funktioner](enable-ai.md)

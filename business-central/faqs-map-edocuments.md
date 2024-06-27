---
title: Vanliga frågor om mappning av e-dokument med inköpsorder
description: 'Vanliga frågor och svar om ansvarsfull AI innehåller information om AI-tekniken som används i Business Central, tillsammans med viktiga överväganden och detaljer om hur AI används, hur den testades och utvärderades och eventuella specifika begränsningar.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# Vanliga frågor och svar om att mappa e-dokument mot inköpsorder med Copilot (förhandsversion)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Dessa vanliga frågor beskriver AI-effekten av funktionen **Matchningshjälp för e-dokument** i [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Vad är matchningshjälp för e-dokument?

Elektroniska dokument (e-dokument) är grunden för moderna affärstransaktioner. De representerar viktigt pappersarbete som fakturor och kvitton som flödar i båda riktningarna genom leverans och inleverans. Du kan generera och överföra elektroniska fakturor digitalt i ett strukturerat format som underlättar automatiserad fakturabearbetning. Hanteringen av inkommande digitala fakturor kan emellertid vara mer komplicerad för leverantörsreskontrateam.  

I små och medelstora företag spelar leverantörsreskontrateamet en avgörande roll för att korrekt spåra leverantörsförpliktelser. Deras primära ansvar är att korrekt registrera inkommande fakturor. Att uppnå precision kan kräva ansträngning, särskilt när de stämmer av externa fakturor från leverantörer med befintliga inköpsorder. Avvikelser i koder, beskrivningar och måttenheter innebär ofta utmaningar eftersom dessa element kanske inte matchar mellan olika system och företag. Oväntade kostnader, till exempel transportavgifter, kan också visas som separata rader som behöver justeras manuellt. Revisorer måste också inkludera fakturanummer och datum i dokumenten. Det är viktigt att förhållandet mellan inköpsorder och externa fakturor inte alltid är en-till-en. Du kan få flera externa fakturor för samma inköpsorder.

Historiskt sett kunde [!INCLUDE [prod_short](includes/prod_short.md)] generera nya inköpsfakturor baserat på mottagna elektroniska fakturor. Att manuellt matcha fakturor med befintliga inköpsorder var emellertid en tidskrävande och felbenägen process.

**Matchningshjälp för e-dokument** använder generativ AI för att effektivisera denna process genom att automatisera analysen av externa elektroniska fakturor. Funktionen gör det möjligt för revisorer att be Copilot att matcha rader på inkommande elektroniska fakturor med rader på inköpsorder i [!INCLUDE [prod_short](includes/prod_short.md)].

## Vilka är funktionerna för matchningshjälp för e-dokument?

Copilot tillhandahåller AI-driven hjälp för att matcha mottagen digital faktura med befintliga inköpsorder i [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot matchar rader baserat på följande:

- Likhet mellan beskrivningar
- Enhet
- Antal tillgängliga för fakturering
- Belopp

Copilot identifierar liknande beskrivningar om de har rätt måttenhet och priser, men kan också hitta matchningar i mer komplexa fall. Den kan till exempel identifiera om en elektronisk faktura har två rader med en variant av samma artikel och bara en rad på inköpsordern, matchar [!INCLUDE [prod_short](includes/prod_short.md)] dessa rader så länge beskrivningarna är liknande och priserna är desamma.

Copilot ansluter inte till slutpunktstjänsten för e-dokument för att hämta eller skicka digitala verifikationer. Denna uppgift förblir helt inom din kontroll och är en förutsättning för att använda hjälp från Copilot. Detta gäller oavsett om de digitala dokumenten läggs till i [!INCLUDE [prod_short](includes/prod_short.md)] med en anslutning till en slutpunktstjänst eller anges manuellt.  

## Vad är den avsedda användningen för matchningshjälp för e-dokument?  

Syftet med funktionen **matchningshjälp för e-dokument** är att hjälpa leverantörsreskontrateamet att matcha befintliga inköpsorder med inkommande elektroniska fakturor. Mycket av den här aktiviteten kretsar kring strängmatchning. [!INCLUDE [prod_short](includes/prod_short.md)] erbjuder en funktion som automatiserar en del av denna aktivitet och LLM har identifierats som en möjlighet att komplettera den funktionen och ytterligare minska manuellt arbete.  

## Hur utvärderades matchningshjälp för e-dokument? Vilka mått används för att mäta prestanda?

Den här funktionen har testats med kombinationer av följande information:

- Externa artikelbeskrivningar
- Enhet
- Antal och belopp
- Standardbeskrivning av artikel
- Olika språk
- Andra parametrar som täcker de typiska variationerna och datagränserna för varje fält 

Testdata representerar både typisk användning och användning av dåliga aktörer. Prestanda mättes jämfört med manuell matchning av samma data i elektroniska fakturor och inköpsorder.

## Vilka är begränsningarna för matchningshjälp för e-dokument? Hur kan användare minimera effekten av begränsningarna för matchningshjälp för e-dokument när de använder systemet?

**Matchningshjälp för e-dokument** fungerar bäst när externa (e-faktura) och interna ([!INCLUDE [prod_short](includes/prod_short.md)]) artikelbeskrivningar och måttenheter är på samma språk. Blandade språk eller blandat språk i artikelbeskrivningar resulterar ofta i färre matchningar och förslag.  

Förslag på matchning av artiklar från e-fakturor med artiklar i inköpsorder fungerar bäst på engelska. Även om du kan använda den här funktionen på alla språk som [!INCLUDE [prod_short](includes/prod_short.md)] stöder, kan du uppleva färre artikelmatchningar på andra språk. För mer information om språk, gå till [I vilka geografiska områden och på vilka språk är matchningshjälp för e-dokument tillgänglig?](#in-which-geographies-and-languages-is-e-documents-matching-assistance-available).

## I vilka geografiska områden och på vilka språk är matchningshjälp för e-dokument tillgänglig?

- Tillgängliga geografiska områden

   Copilot-funktionen är tillgänglig i alla geografiska [Business Central länder/regioner som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). För kundmiljöer i länder/regioner där Azure OpenAI Service inte distribueras måste administratörer först godkänna att data flyttas över gränserna för [!INCLUDE [prod_short](includes/prod_short.md)] för att ansluta till Azure OpenAI Service. Läs mer om [Copilot dataförflyttning mellan geografiska områden](ai-copilot-data-movement.md).

- Tillgängliga språk

   [!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## Vilka driftfaktorer och inställningar gör det möjligt att på ett effektivt och ansvarigt sätt använda funktionen?

Copilot kompletterar mappningsalgoritmen som [!INCLUDE [prod_short](includes/prod_short.md)] redan tillhandahåller och mappar de rader som algoritmen inte gjorde.

### Vad förväntas av användare när de använder matchningshjälp för e-dokument?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

När du har mappat inkommande elektroniska fakturor med inköpsorder måste du mappa raderna i dokumenten.

På sidan **Mappning av inköpsorder** visas alla rader från båda dokumenten. Här kan du göra mappningen manuellt, vilket kan vara svårt om det finns många rader.

Du kan använda **matchningshjälp för e-dokument** för att mappa rader baserat på följande kriterier:

- Likhet i deras beskrivningar
- Enhet
- Antal tillgängliga för fakturering
- Belopp

Copilot-matchningar kan vara felaktiga eller ofullständiga. Du bör alltid granska deras noggrannhet innan du väljer att behålla dem. Copilot-matchningar och förslag sparas i [!INCLUDE [prod_short](includes/prod_short.md)] du väljer **Behåll den** och avslutar Copilot. Du kan redigera och korrigera eventuella matchningar eller förslag innan du väljer att behålla dem. 

### Vad förväntas av administratörer och användare när de använder matchningshjälp för e-dokument?

Användare, till exempel revisorer eller andra som tar emot e-fakturor bör alltid granska riktigheten i matchningar och förslag från Copilot innan de väljer att behålla dem. Vi rekommenderar att du granskar inköpsorderraderna för att kontrollera att de stämmer och hitta eventuella avvikelser. Du bestämmer om du vill använda **matchningshjälp för e-dokument**. Även när funktionen är **matchningshjälp för e-dokument** aktiverad av administratörer och tillgänglig kan du fortfarande välja att använda den alltid, ibland eller aldrig.  

Administratörer fattar det övergripande beslutet om Copilot ska användas eller inte i [!INCLUDE [prod_short](includes/prod_short.md)]. Om de aktiverar Copilot bör administratörer se till att de ger åtkomst till lämplig.

> [OBS!]
> - Vi stöder inte funktionen för [!INCLUDE [prod_short](includes/prod_short.md)] lokalt eller i privata moln.
> - Partner kan inte utöka den här funktionen. Partnerutvecklare kan inte ändra, ersätta eller utöka denna funktion. 

## Är Copilot det enda sättet att matcha e-dokument med inköpsorder?  

Nej, om du använder Copilot eller inte är upp till dig. [!INCLUDE [prod_short](includes/prod_short.md)] erbjuder icke-AI-drivna sätt att matcha artiklar från mottagna elektroniska fakturor med artiklar på inköpsorder i [!INCLUDE [prod_short](includes/prod_short.md)]. Organisationer kan också använda båda metoderna samtidigt.  

## Hur ger jag feedback om AI-genererat innehåll?  

Varje gång Copilot ger matchningar eller förslag kan du ge feedback till Microsoft direkt från Copilot-fönstret med hjälp av kontrollerna **gilla** och **ogilla**. Din feedback förblir anonym och vi använder dessa uppgifter för att förbättra kvaliteten på tjänsten.  

## Se även

[Översikt över e-dokument](finance-edocuments-overview.md)  
[Mappa e-dokument mot inköpsorderrader med Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

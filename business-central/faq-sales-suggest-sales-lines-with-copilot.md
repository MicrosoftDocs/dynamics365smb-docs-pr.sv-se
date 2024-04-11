---
title: Vanliga frågor och svar om förslag på försäljningsrader med Copilot
description: Dessa vanliga frågor och svar innehåller information om AI-tekniken som används i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# <a name="faq-for-sales-line-suggestions-with-copilot-preview"></a>Vanliga frågor och svar om förslag på försäljningsrader med Copilot (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Dessa vanliga frågor beskriver AI-effekten av funktionen förslag på försäljningsrader i [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-sales-line-suggestions-with-copilot"></a>Vad är förslag på försäljningsrader med Copilot?

Förslag på försäljningsrader med Copilot kan hjälpa dig att skapa rader i försäljningsdokument som försäljningsofferter, order och fakturor baserat på strukturerad inmatning eller naturligt språk. Funktionen är inte en allmän chatt, utan en mycket specifik och integrerad upplevelse som du kan använda på försäljningsdokument. Funktionen erbjuder två olika färdigheter som hjälper dig att hitta data om enskilda produkter eller hela dokument.

## <a name="what-are-capabilities-of-sales-line-suggestions-with-copilot"></a>Vilka funktioner har förslag på försäljningsrader med Copilot?

* Hitta produkter

  Information som beskriver produkter lagras på flera ställen i [!INCLUDE [prod_short](includes/prod_short.md)]. Artikelnummer och beskrivningar lagras till exempel i tabellen **Artikel** , flera streckkoder lagras i tabellen **Artikelreferens** och produktegenskaper lagras i tabellen **Artikelattribut**. Medan du kanske frågar efter *röd cykel* kan den faktiska produkten vara *Crimson tourer*, där *cykel* är en produktkategori och *röd* är ett attribut.

* Sök ett dokument efter referens

  Människor upprepar ofta en tidigare order, eller åtminstone använder den som utgångspunkt. Men det kan vara svårt att hitta rätt order i en bunt med order. Du kanske kommer ihåg en del av orderns ID, som kan vara ett företagsnummer eller ett referensnummer som du fått från en kund. Att kunna använda prompter som *Behöver sista fakturan från april* bör hjälpa dig att hitta en order snabbare.

## <a name="what-is-the-intended-use-of-sales-line-suggestions-with-copilot"></a>Vilken är den avsedda användningen av förslag på försäljningsrader med Copilot?

* Hitta produkter

  Den är avsedd att svara på användarfrågor för att hitta produkter baserat på vaga, ofullständiga eller felaktiga beskrivningar.

  Eftersom det genomsnittliga antalet artiklar (produkter/tjänster) för [!INCLUDE [prod_short](includes/prod_short.md)] kunder är 10 000 kan det vara svårt att hitta rätt utan tidigare erfarenhet eller kunskap. Hur data lagras i [!INCLUDE [prod_short](includes/prod_short.md)] gör det inte lättare eftersom du måste göra flera sökningar eller filtreringsövningar på de olika sidorna där produktdata lagras.

  Copilot extraherar de begärda produkterna och kvantiteterna och identifierar de viktigaste söktermerna och attributen så att du kan skriva din fråga snabbare. Sedan gör Copilot en avancerad sökning genom flera relaterade tabeller, tillämpar synonymer, korrigerar stavfel och utvärderar kvaliteten på sökresultaten.

* Sök ett dokument efter referens

  Den är avsedd att besvara användarförfrågningar för att hitta befintliga försäljningsdokument för en specifik kund med partiell eller ungefärlig information.

  I B2B-miljöer hanterar människor ofta återkommande förfrågningar och orderhandläggare kan få förfrågningar om att upprepa ett tidigare dokument eller åtminstone använda det som utgångspunkt. Men det kan vara svårt att hitta en av flera orsaker:

  - Ett försäljningsdokument kan under sin livscykel utvecklas från offert till order till bokförd faktura eller leverans. Dokument kan också arkiveras.
  - Du kanske har en exakt identifierare, men kan inte säga vad den representerar. Är det till exempel ordernummer, fakturanummer eller extern referens?
  - Ibland har du ett datum eller en period, men inte ett ID för dokumentet.

  Om du vill söka efter ett källdokument manuellt måste du öppna flera sidor och använda sökning och filter flera gånger. Copilot kan emellertid förenkla detta med en enda fråga på naturligt språk som gör att du kan uttrycka vad du letar efter på ditt eget sätt. 

  * *Hämta produkter från beställning 103031*
  * *Behöver produkter från sista fakturan i augusti*

## <a name="how-was-sales-line-suggestions-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hur utvärderades förslag på försäljningsrad med Copilot? Vilka mått används för att mäta prestanda?

Funktionen genomgick omfattande tester där många uppmaningar på amerikansk engelska representerar både typisk användning och användning av dåliga aktörer. Testningen baserades på [!INCLUDE [prod_short](includes/prod_short.md)] demonstrationsdata och en stor märkt produktkatalog tillgänglig som öppen källkod.

Den här funktionen är byggd i enlighet med Microsofts standard för ansvarsfull AI. [Läs mer om ansvarsfull AI från Microsoft](https://aka.ms/RAI).

## <a name="what-are-the-limitations-of-sales-line-suggestions-with-copilot-how-can-users-minimize-the-impact-of-the-sales-line-suggestions-with-copilot-limitations-when-using-the-system"></a>Vilka är begränsningarna för förslag på försäljningsrader med Copilot? Hur kan användare minimera effekten av förslag på försäljningsrader med Copilot när de använder systemet?

* Hitta produkter
  
  Att söka produkter fungerar bäst på engelska. Du kan använda den här funktionen på vilket som helst av de språk som stöds av [!INCLUDE [prod_short](includes/prod_short.md)], men artikelsökningar på andra språk kan vara mindre exakta.

Om din bransch eller domän överlappar med vad Microsoft anser vara känsliga ämnen (till exempel droger, våld, vuxenunderhållning och så vidare) kan Copilot förlita sig på neutrala, utvalda svar eller ge felaktiga svar.

Förslag på försäljningsrader fyller bara i fälten **Typ** som **Artikel**, **Nr.** och **Antal** enligt beskrivningen. I andra fält, till exempel **Måttenhet**, **Enhetspris** och **Lagerställe** används den aktuella logiken och fylls i antingen baserat på artikelinställningar eller ärvda värden från dokumenthuvudet.

**Variantkoden** stöds inte för närvarande. Om du till exempel kan leverera en produkt i två olika färger hittar Copilot den produkt som behövs men lämnar fältet **Variantkod** tomt. Du måste fylla i fältet manuellt.

Resultatet kan påverkas av hur du namnger dina produkter. Om du till exempel använder kryptiska förkortningar jämfört med användarvänliga namn kan resultatets kvalitet försämras.

För produkter anger följande tabell de tabeller och fält som Copilot söker i.

|Bord  |Fält  |
|---------|---------|
|**Artiklar**     |  * Nr.<br>* Beskrivning<br>* Beskrivning 2<br>* Sökbeskrivning<br>* GTIN<br>* Leverantörens artikelnummer       |
|**Artikelvariant**     | * Kod<br>* Beskrivning<br>* Beskrivning 2          |
|**Artikelreferens**     | * Referensnr<br>* Beskrivning<br>* Beskrivning 2        |
|**Artikelattribut**     | * Namn<br>* Värde        |
|**Artikelkategori**     |  * Kod<br>* Beskrivning<br>* Överordnad kategori – 1 nivå           |
|**Artikelöversättning**     | * Språk<br>* Beskrivning<br>* Beskrivning 2          |
|**Artikelidentifierare**     |  * Kod       |
|**Extra textrad**     |  * Text      |

* Sök dokument efter referens

  För närvarande kan du starta förslag på försäljningsrader från försäljningsorder, fakturor och offerter och söka i följande dokument:

  * Försäljningsorder
  * Försäljningsofferter
  * Försäljningsfakturor
  * Bokförda försäljningsfakturor
  * Bokförda försäljningsutleveranser

  Copilot söker i följande fält

  * Verifikationsnr
  * Externt verifikationsnr
  * Er referens
  * Offertnr
  * Dokumentdatum
  * Försäljningskundnr

  Copilot returnerar inte alla rader av typen Artikel. Endast artikelnummer, variantkoder och kvantiteter överförs. Kvantiteter från källdokumentet konverteras till **Måttenhet för försäljning**.

## <a name="in-which-geographies-and-languages-is-sales-lines-suggestions-available"></a>I vilka geografiska områden och på vilka språk finns förslag på försäljningsrader tillgängligt?

Med undantag för Kanada är den här funktionen tillgänglig för alla länder/-regioner och på alla språk som stöds. På grund av begränsat språkstöd kommer funktionen inledningsvis inte att vara tillgänglig för kanadensiska kunder på grund av regelspråksefterlevnad. För att denna funktion ska vara tillgänglig för kundmiljöer i länder/regioner där Azure OpenAI Service inte distribueras måste administratörer först godkänna att data flyttas över gränserna för [!INCLUDE [prod_short](includes/prod_short.md)] för att ansluta till Azure OpenAI Service.  

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Vilka driftfaktorer och inställningar gör det möjligt att på ett effektivt och ansvarigt sätt använda funktionen?

AI-drivna förslag kan ibland vara felaktiga eller ofullständiga. Du bör alltid granska riktigheten i Copilot-förslag innan du väljer om du vill behålla dem. Copilot-förslag sparas inte i [!INCLUDE [prod_short](includes/prod_short.md)]-databasen förrän du väljer knappen **Behåll den** den och stänger Copilot-fönstret. Du kan redigera och korrigera eventuella förslag innan du väljer att behålla dem eller efter att de har infogats i ett försäljningsdokument.

### <a name="what-is-expected-of-administrators-and-end-users-when-using-sales-lines-suggestions"></a>Vad förväntas av administratörer och slutanvändare när de använder förslag på försäljningsrader?

Varje enskild användare väljer om han eller hon vill använda **förslag på försäljningsrader**. Även när funktionen är aktiverad av administratörer och tillgänglig kan du välja att använda den alltid, ibland eller aldrig.  

Administratörer fattar det övergripande beslutet om Copilot-funktioner ska användas eller inte i [!INCLUDE [prod_short](includes/prod_short.md)]. Om administratörer aktiverar Copilot bör de se till att bevilja åtkomst till lämpliga användare.   

> [OBS!]
> - Vi stöder inte den här funktionen i [!INCLUDE [prod_short](includes/prod_short.md)] lokalt eller i privata moln.
> - Partner kan inte utöka den här funktionen. Det innebär att partnerutvecklare inte kan ändra, ersätta eller utöka den.

## <a name="is-copilot-the-only-means-to-create-sales-lines"></a>Är Copilot det enda sättet att skapa försäljningsrader?

Nej, användning av Copilot är valfri. [!INCLUDE [prod_short](includes/prod_short.md)] erbjuder icke-AI-drivna sätt att infoga försäljningsrader eller kopiera dokument. Organisationer kan använda båda metoderna samtidigt.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hur ger jag feedback om AI-genererat innehåll?

Varje gång Copilot ger förslag kan du ge feedback till Microsoft direkt från Copilot-fönstret med hjälp av knapparna gilla och ogilla. Din feedback förblir anonym och vi använder dessa uppgifter för att förbättra kvaliteten på tjänsten.  

## <a name="see-also"></a>Se även

[Föreslå rader på försäljningsorder med Copilot](sales-suggest-sales-lines-with-copilot.md)  
[Konfigurera Copilot- och AI-funktioner](enable-ai.md)  
[Ansvarsfull AI, vanliga frågor för Dynamics 365 Business Central](responsible-ai-overview.md)  

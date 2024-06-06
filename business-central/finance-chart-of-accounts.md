---
title: Förstå kontoplanen
description: 'Beskriver kontoplanen, hur du lägger upp den och hur du använder den.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/17/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Förstå kontoplanen

En kontoplan (COA) fungerar som en omfattande katalog över finansiella konton och deras motsvarande referensnummer. En kontoplan består vanligtvis av två huvudkategorier av konton:

- Balansräkningskonton: Dessa konton spårar ditt företags tillgångar, skulder och nettovärde.
- Resultaträkningskonton: Dessa konton registrerar intäkter från olika källor och spårar även utgifter.

Balansräkningskonton kategoriseras vidare i tre grupper:

1. Tillgångskonton: Dessa konton spårar alla värdefulla resurser som ägs av ditt företag.
1. Skuldkonton: De registrerar ditt företags skulder.
1. Aktiekonton: Representerar restvärdet i verksamheten efter avdrag för skulder från tillgångar.

Inkomstkontona indelas i två grupper:

1. Intäktskonton: Dessa konton fångar ditt företags inkomster från olika källor.
1. Utgiftskonton: Dessa konton fångar alla företagets utgifter.

Använd kontoplanen för att registrera transaktioner i organisationens redovisning. Varje konto har vanligtvis en identifierare (kontonummer) och en beskrivande bildtext eller rubrik och de kodas systematiskt baserat på deras kontotyp.

[!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.

Sammansättningen av ditt företags kontoplan är ett strategiskt beslut som fattas av din ledning (eller genom landsspecifik reglering). Det varierar beroende på ditt företags bransch, affärsmodell och ekonomiska struktur. Beroende på din bransch kan du till exempel ha specifika tillgångskonton som är skräddarsydda för ditt företags unika verksamhet och behov:

* Ett detaljhandelsföretag kan betona lager och kundreskontra.
* Ett teknikföretag kan fokusera på immateriella tillgångar som patent och programvara.
* En tillverkningsanläggning skulle spåra anläggningstillgångar och leveranser.

## <a name="the-chart-of-accounts-page"></a>Sidan Kontoplan

Kontoplanen visar alla redovisningskonton. Från kontoplanen, kan du göra sådant som:  

* Visa rapporter som visar transaktioner och saldon.  
* Avslut av resultatkonton.  
* Öppna kortet för redovisningkonto där du kan lägga till eller ändra inställningar.  
* Visa en lista med bokföringsmallar för det kontot.
* Visa separatea debet- och kreditsaldon för ett enskilt konto.

Du kan lägga till, ändra eller ta bort konton i redovisningen. I syfte att undvika avvikelser kan du emelelrtid inte ta bort ett redovisningskonto om dess data används i kontoplanen. Du kan också blockera oavsiktlig borttagning av konton under känsliga perioder. Mer information om hur du skyddar konton från borttagning finns i [Ta bort konton](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>Kodhierarkin i redovisningskonton

Företag skapar vanligtvis en hierarkisk struktur i redovisningskontokoder för att återspegla var de hör hemma i kontoplanen. I vissa implementeringar betecknar redovisningskontokoder som börjar med **1** tillgångskonton, medan redovisningskontokoder som börjar med 3 betecknar kapitalkonton. I vissa regioner finns det lokala bestämmelser för användning av en standardkontoplan. Om du vill hjälpa användarna att förstå hierarkin utan att behöva känna till den interna kodstrukturen kan du definiera rubriker och delsummor i kontoplanen som kapslar in dessa interna strukturer.

## <a name="designing-your-chart-of-accounts"></a>Designar din kontoplan

Varje rad i kontoplanen är ett huvudkonto av en av typerna:

* Bokföring (journaler kan bokföra rader till dessa konton)
* Rubrik (definierar en övergripande rubrik i kontoplanen)
* Totalt (definierar en formel för en delsumma i kontoplanen)
* Från-summa (definierar en början rubrik för en delsumma i kontoplanen. Alla efterföljande rader fram till en rad/slutsumma dras in)
* Slutsumma (definierar en slutrubrik för en delsumma och formeln för den i kontoplanen. Alla efterföljande rader efter denna rad/slutsumma dras ut)

En minimalistisk kontoplan kan bara bestå av rader med bokföringskonton. Du använder de andra fyra typerna för att definiera hur kontoplanen också ska visa en ekonomisk rapport med rubriker och delsummor. Summeringskonton används ofta i finansiell rapportering.

> [!TIP]
> Om du använder andra kontotyper än **Bokföring** i kontoplanen kan du definiera olika vyer för att visa de "råa" bokföringskontona utan kontotyperna av rapporteringstyp för summering och rubriker. Till exempel Visa endast bokföringskonton och Dölj blockerade konton.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Använd dimensioner för att förenkla kontoplanen

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis försäljningsorder. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån. Så i stället för att skapa separata redovisningskonton för varje avdelning och projekt kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad kontoplan.

Om du vill lära dig mer om dimensioner går du till [Arbeta med dimensioner](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Få en snabb överblick över din ekonomi

På sidan **Kontoplan** visas i en hierarkisk lista de konton som ger snabb åtkomst till nyckelinformation för respektive konto. Listan är dock statisk, och om du har många konton måste du kanske bläddra för att kunna visa olika konton. Om du bara vill ha en snabb överblick över grunderna, till exempel nettoförändringar och saldon, är sidan **Kontoplansöversikt** ett användbart alternativ. Kolumnlayouten på sidan är samma som du hittar på sidan **Kontoplan** (men med färre kolumner), så det är lätt att förstå. Du kan expandera eller komprimera de hierarkiska nivåerna. För att det ska bli lättare att växla mellan sidorna är sidan **Kontoplansöversikt** tillgänglig på sidan **Kontoplanen**.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Åtkomst för att skapa och redigera kontoplaner

I en liten organisation, t.ex. demonstrationsföretaget CRONUS, kan de flesta användare redigera kontoplanen, utom användare med en licens som gruppmedlem. Större organisationer använder dock vanligtvis roller och behörigheter för att begränsa åtkomsten till att redigera kontoplanen. Om du är administratör eller har rollen Företagschef eller Revisor kan du kontrollera användarbehörigheter för att ge rätt personer tillgång till de relevanta tabellerna. Gå till [Så här får du en översikt en användares behörigheter](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions) för mer information.  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Bästa praxis för kontoplaner

Här är några metodtips som du kan tänka på när du utvecklar och underhåller kontoplaner:

* Komponera ditt företags kontoplan för att stödja de finansiella rapporteringsbehoven för din ledning att fatta strategiska beslut.
* Överväg att börja enkelt med färre redovisningskonton. Du kan alltid lägga till mer detaljerade konton om det behövs.
* Definiera rubriker och delsummor i kontoplanen som sammanfattar de interna strukturerna i redovisningskontona.
* Använd dimensioner för att förenkla kontoplanen. Ha inga specifika redovisningskonton för varje produkt eller avdelning.
* Lägg till nya redovisningskonton när de kommer in, men ta bara bort konton från kontoplanen under räkenskapsperiodens slut.

## <a name="see-also"></a>Se även

[Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md)  
[Förstå redovisningen](finance-general-ledger.md)
[Ekonomisk analys](bi.md)  
[Översikt över ekonomi](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

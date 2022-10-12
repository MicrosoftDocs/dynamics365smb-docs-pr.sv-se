---
title: Kortkommandon
description: En fullständig lista över kombinationer av kortkommandon för att arbeta effektivt med dina data.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding, keys
ms.date: 08/16/2022
ms.author: jswymer
ms.openlocfilehash: 38dec472417e49fe974ed72f6eac2fdf4dffde3c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606674"
---
# <a name="keyboard-shortcuts"></a>Kortkommandon

Den här artikeln innehåller en översikt över några av de kombinationer av kortkommandon som du kan använda när du arbetar med [!INCLUDE[prod_short](includes/prod_short.md)].

En översikt över de vanligaste kortkommandona finns i [Kortkommandon (endast dator)](keyboard-shortcuts-cheatsheet.md).

> [!TIP]
> Om du vill visa en grafisk vy över de mest använda kortkommandona väljer du följande bild och hämtar PDF-filen.  
> [ ![Ikon för PDF-filen.](media/keyboard_shortcut_inline.png) ](media/keyboard_shortcuts.pdf "Ikon som öppnar en PDF-fil")

## <a name="overview"></a>Översikt

Kortkommandona förbättrar tillgängligheten och kan göra det enklare och mer effektivt att navigera till olika områden och element på en sida. De stöds av de flesta webbläsare, beteendet kan dock variera något.

> [!NOTE]
> Kortkommandona som beskrivs här gäller amerikansk tangentbordslayout. Tangentlayouten på andra tangentbord kanske inte exakt motsvarar tangenterna på ett amerikanskt tangentbord.

De flesta kortkommandona är desamma oavsett om operativ systemet är Windows eller macOS. Vissa kortkommandon är emellertid olika för macOS. Dessa genvägar anges med hakparenteser i följande avsnitt.

> [!NOTE]
> Förutom de globala kortkommandon som beskrivs i denna artikel finns ett antal företagsspecifika genvägar. I den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] bokför F9 exempelvis ett dokument och CTRL + F7 visar redovisningstransaktionerna för en post när du öppnar posten i ett kort. I denna artikel beskrivs några av de vanligaste företagsspecifika kortkommandona, som visas med kursiv stil. Tänk på att de faktiska kortkommandona kan variera i just din lösning. I användargränssnittet visas kortkommandot i knappbeskrivningen för den aktuella åtgärden.

##  <a name="general-keyboard-shortcuts"></a><a name="Keyboard"></a> Allmänna kortkommandon

I tabellen nedan beskrivs kortkommandon för navigering och åtkomst av olika element på en sida. Element är t. ex. åtgärder, list rutor, uppslag m.m. Mer information om kortkommandon för att hantera poster när de visas i en lista finns i nästa avsnitt.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|Alt+nedpil|Öppna en listruta eller leta upp ett värde för ett fält.|
|Alt+Uppil|Visa knappbeskrivning för ett fält eller en kolumnrubrik i en tabell. Om det finns valideringsfel för fältet, trycker du på ”Alt + Uppil” för att visa innehålla valideringsfelet. Tryck på ”Esc” eller ”Alt + Uppil” för att stänga knappbeskrivningen.|
|F2|Växla för att växla mellan att markera hela fältets värde eller att placera markören på slutet av fältets värde.|
|Alt+F2|Visa och dölj rutan Faktabox|
|Alt+Shift+F2|Växla mellan **detaljer** och **bifogade filer** i rutan faktabox.|
|Alt+O|Lägg till en ny anteckning för den valda posten även om rutan faktabox inte är öppen.|
|Alt+Q<br />(Ctrl+alternativ+Q)|Öppna fönstret **Berätta**. Mer information finns i [söka efter sidor och information med berätta](ui-search.md).|
|Ctrl+Alt+Q<br />(Ctrl+alternativ+Cmd+Q)|Öppna sidan **Sök poster** för att söka efter dokument och transaktioner som är relaterade till varandra baserat på gemensam information, som verifikationsnummer eller bokföringsdatum. Mer information finns i [söka efter relaterade fullständiga filer för bokförda dokument](ui-find-entries.md)|
|Alt+N |Öppna en sida om du vill skapa en ny post. (Påminner om att välja **Ny** och **+** åtgärder.)|
|Alt+Shift+N |Stäng en nyligen skapad sida och öppna en ny för att skapa en ny post. På samma sätt bokför Alt + F9 ett dokument och skapar ett nytt.|
|Alt+T|Öppna sidan **Mina inställningar**.|
|Alt+Högerpil|Slå upp ytterligare information eller underliggande värden för ett fält som innehåller knappen ![AssistEdit](media/assist-edit-icon.png "Knappen AssistEdit"). knappen. Detta används när den vanliga listruteknappen (Alt + nedåtpil) i samma fält används för ett annat syfte.|
|Ctrl+Alt+Shift+C|Visa information på företagsbrickan. Det här kortkommandot slutade användas i Business Central 2022, utgivningscykel 2 (version 21) och ersattes av Ctrl + O. |
|Ctrl+Alt+F1|Öppna och stäng sidinspektionsrutan. Sidinspektionsrutan visar information om sidan, t. ex. dess källtabell, fält, filter, tillägg och annat.<br /><br />Mer information finns i [Inspektionssidor](across-inspect-page.md).|
|Ctrl+C |Kopiera värdet i fältet. Om fältet är i fokus och du inte har valt någon text i fältet, kommer hela värdet att kopieras. Om du har markerat en text i fältet, kopieras endast den markerade texten.|
|Ctrl+F1|Öppna [hjälpfönstret](product-help-and-support.md#help-pane) eller en Business Central-hjälpartikel på [Microsoft Learn](/dynamics365/business-central/), beroende på din Business Central-version.|
|Ctrl+F12|Växla mellan breda och smala vyn.|
|Ctrl + klicka|Navigera under anpassa personligt eller anpassa när åtgärden markeras med en pilspets. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).|  
|Ctrl+F5|Läs [!INCLUDE[prod_short](includes/prod_short.md)]-programmet på nytt. (Ungefär som att markera uppdatera/läsa in på nytt i webbläsaren).|
|F5|Uppdatera informationen på den aktuella sidan.<br /><br />Använd denna nyckel för att se till att informationen på sidan har uppdaterats med ändringarna som andra har gjort medan du arbetar.|
|Ctrl+O|Öppna rutan **Tillgängliga företag** för att växla till ett annat företag eller en annan miljö. Mer information finns i [byta till ett annat företag eller annan miljö](ui-organization-switch.md).|
|Enter|Aktivera eller nå elementet eller kontrollen som är i fokus.|
|Esc|Stäng den aktuella sidan eller listrutan.|
|Tabb|Flytta fokus till nästa kontroll eller element på en sida, till exempel åtgärder, knappar, fält eller listrubriker.|
|Skift+Tabb|Flytta fokus till föregående kontroll eller element på en sida, till exempel åtgärder, knappar, fält eller listrubriker.|
|Y och N|Aktivera knapparna **Ja** och **Nej** i dialogrutor. De faktiska nycklarna kan variera beroende på vilket språk som anges i **Mina inställningar**. Du kan t. ex. trycka på J för att aktivera **Ja**-knappen när du använder tyska språket.|

## <a name="keyboard-shortcuts-in-lists"></a>Kortkommandon i listor

I följande tabell beskrivs de kortkommandon som du kan använda i en listsida. Genvägsåtgärden skiljer sig något beroende på om sidan visas som listvy eller sida vid sida.
<!--
> [!Note]
> In the table that follows, the term *actionable field* refers to a field on which you can do something, like change a value or link to another page. In general, the shortcuts will skip over fields that display information that you cannot change from the list (in other words, fields that are read-only).
-->
### <a name="general"></a>Allmänt

|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista|För att göra detta som en panelvisning |
|--------------------------------|-------------------------|--------------------------|
|Alt+F7 |Sortera markerad kolumn i stigande eller fallande ordning.|Ej tillämpbart.|
|Alt+N|Infoga en ny rad i en redigerbar lista, till exempel sidan **redovisningsbudgetar**.|Samma.|
|Shift+F9|Bokför och skriv ut ett dokument.|Samma.|
|Shift+F10 |Öppna en meny med alternativ som är tillgängliga för den markerade raden.|Samma.|
|Alt+D|Öppna posterna för dimensionsuppsättning.|Samma.|
|Ctrl+F7|Öppna redovisningstransaktioner, loggtransaktioner, kostnadstransaktioner o.s.v.|
|Ctrl+F9|Frisläpp dokument.|Samma.|
|*F7*|Öppna statistik.|Samma.|
|*F9*|Bokföra, utfärda, registrera eller återföra dokument.|Samma.|
|*Shift+Ctrl+F*|Skicka förslag på rader på sidan för kalkylark för kassaflöde.|Ej tillämpbart.|
|*Shift+Ctrl+I*|Visa serie- och partinummer som har tilldelats till radartikeln för dokument eller journal.|Ej tillämpbart.|

### <a name="navigating-between-rows-and-columns"></a><a name="navigateshortcuts"></a>Navigera mellan rader och kolumner

Det finns stödraster som innehåller rader och kolumner på många olika sidtyper i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel listsidor och **Rad**-delar i dokument. Att flytta från en cell till en annan i ett rutnät kan ske helt och hållet via tangentbordet.

| Tryck på dessa tangenter<br />(i macOS) | För att göra detta som en lista | För att göra detta som en panelvisning |
|--|--|--|
| Ctrl+Home<br />(Fn+Ctrl+vänsterpil) | Markera den första raden i listan. Fokus är kvar i samma kolumn. | Flytta till första panelen i den första raden. |
| Ctrl+End<br />(Fn+Ctrl+högerpil) | Markera den sista raden i listan. Fokus är kvar i samma kolumn. | Flytta till den sista panelen i den sista raden. |
| Hem<br />(Fn+vänsterpil) | Flytta till första fältet i raden. | Flytta till första panelen i raden. |
| End<br />(Fn+högerpil) | Flytta till det sista fältet i raden. | Flytta till den sista panelen i raden. |
| Skriv in | Öppna posten som är associerad med fältet.<br /><br />Endast relevant om en sida med kort associerad med posten. | Posten öppnas.<br /><br />Endast relevant om en sida med kort associerad med posten. |
| Ctrl+Enter | Flytta fokus till nästa element utanför listan. | Flytta fokus till nästa element utanför listan. |
| Page Up<br />(Fn+uppåtpil) | Rulla för att visa uppsättningen med rader ovanför den aktuella raden i vyn. | Rullar för att visa uppsättningen med paneler ovanför den aktuella panelen i vyn. |
| Page Down<br />(Fn+Nedpil) | Rulla för att visa uppsättningen med rader nedanför den aktuella raden i vyn. | Rulla för att visa uppsättningen med paneler nedanför den aktuella panelen i vyn. |
| Nedpil | Flytta till fältet i raden nedanför i samma kolumn. | I samma kolumn, flytta till panelen i raden nedanför. |
| Uppil | Flytta till fältet i raden ovanför i samma kolumn | I samma kolumn, flytta till panelen i raden ovanför |
| Högerpil | I en skrivskyddad lista, flytta till samma rad till höger i samma fält.<br /><br />Flytta till höger i det aktuella fältet i en redigeringsbar lista. | Flytta till nästa ändringsbara panel till höger i samma rad. |
| Vänsterpil | I en skrivskyddad lista, flytta till samma rad till vänster i föregående fält. <br /><br />Flytta till vänster i det aktuella fältet i en redigeringsbar lista. | Flytta till föregående panel till vänster i samma rad. |
| Tabb | I en redigerbar lista, flytta till samma rad till höger i samma fält. | Ej tillämpbart. | 
| Skift+Tabb | I en redigerbar lista, flytta till samma rad till vänster i föregående fält. | Ej tillämpbart. |

### <a name="selecting-copying-and-pasting"></a><a name="CopyRows"></a>Välja kopiera och klistra in

|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista |För att göra detta som en panelvisning |
|--------------------------------|--------------------------|--------------------------|
|Ctrl + klicka<br />(Cmd + klicka)|Utöka radmarkeringen så att den rad som du klickar på inkluderas.|Ej tillämpbart.|
|Skift+klicka|Utöka radmarkeringen så att den rad som du klickar på och samtliga där emellan inkluderas.<br /><br />Du kan använda detta när du har använt Ctrl + uppåtpil eller Ctrl + uppåtpil/nedpil för att utöka ditt val.|Ej tillämpbart.|
|Ctrl+Uppil<br />(Ctrl+Cmd+uppil)|Flytta fokus till raden ovanför och behåll den aktuella raden som har valts.|Ej tillämpbart.|
|Ctrl+Nedpil<br />(Ctrl+Cmd+nedpil)|Flytta fokus till raden nedanför och behåll den aktuella raden som har valts.|Ej tillämpbart.|
|Ctrl+Blanksteg<br />(Ctrl + Cmd + blanksteg)|Utöka radmarkeringen så att den markerade raden inkluderas.<br /><br />Du kan använda detta när du har använt Ctrl + uppåtpil eller Ctrl + nedpil för att utöka ditt val.|Ej tillämpbart.|
|Ctrl+A|Markera alla rader.|Ej tillämpbart.|
|Ctrl+C<br />(Cmd+C)|Kopiera de markerade raderna till Urklipp.|Ja, men endast för en enstaka markerad panel.|
|Ctrl+V<br />(Cmd+V)|Klistra in de markerade raderna från Urklipp till den aktuella sidan eller ett externt dokument såsom Microsoft Excel eller Outlook e-post. Du kan bara göra detta i redigerbara listor.|Ej tillämpbart.|
|Shift+Uppil|Utöka radmarkeringen så att raden ovan inkluderas.|Ej tillämpbart.|
|Shift+nedpil|Utöka radmarkeringen så att raden nedan inkluderas.|Ej tillämpbart.|
|Shift+Page Up<br />(Shift+Fn+uppil)|Utöka radmarkeringen så att samtliga rader som visas ovanför den aktuella radmarkeringen inkluderas.|Ej tillämpbart.|
|Shift+Page Down<br />(Shift+Fn+nedpil)|Utöka radmarkeringen så att samtliga synliga rader nedanför den aktuella radmarkeringen inkluderas.|Ej tillämpbart.|
|F8|Kopiera fältet i samma kolumn i raden ovanför och klistra in den i den aktuella raden. Du kan bara göra detta i redigerbara listor. Med detta kortkommando följt av en flik kan du snabbt kan fylla i fält i radposter som du vill ska ha samma värde som raden ovan.|Ej tillämpbart.|

### <a name="searching-and-filtering-lists"></a><a name="KeyboardFilter"></a>Söka och filtrera listor

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|F3|Växlar sökrutan.<ul><li>Aktivera sökrutan så att du kan börja skriva söktexten.</li><li>Om sökrutan redan är aktiverad, återgår F3 till listan utan att radera söktexten.</li><ul>|
|Shift+F3|Öppna och stäng filterrutan.<ul><li> Om filterrutan inte är öppen öppnar du Skift + F3 det och fokuserar på åtgärden **+ filter** under **filterlistan**. Du kan sedan bara trycka på retur när du vill börja lägga till ett fältfilter.</li><li>Om filterrutan redan är öppen stängs den med SKIFT + F3 men rensar inte alla filter som du har lagt till.</li></ul>|
|Ctrl+Shift+F3|Öppna och stäng filterrutan.<ul><li> Om filterrutan inte är öppen öppnar du Ctrl + Skift + F3 det och fokuserar på åtgärden **+ filter** under **Filtrera summa efter**. Du kan sedan bara trycka på retur när du vill börja lägga till ett summeringsfilter.</li><li>Om filterrutan redan är öppen stängs den med Ctrl + Skift + F3 men rensar inte alla filter som du har lagt till.</li></ul>  |
|Alt+F3|Aktivera/inaktivera filtreringen till det valda värdet.<ul><li>Använder ett kolumnfilter på det markerade filtervärdet i listan. Detta är detsamma som att välja **filtrera på det här värdet** från en kolumnrubrik. Den öppnar filterrutan, ställer in filter till det valda värdet när fokus är på en cell i listan.</li><li>Om kolumnen redan är filtrerad rensar Alt + F3 filtret på den kolumnen.</li></ul> |
|Shift+Alt+F3|Öppna filterfönstret och lägg till ett filter för den markerade kolumnen i listan. Fokus är på det nya filterfältet som börjar skriva filterkriterierna direkt.<br /><br /> Detta innebär att välja **Filter** från kolumnrubriken.<br /><br />Om det redan finns ett filter i fältet, läggs ett nytt filter till. |
|Ctrl+Shift+Alt+F3|Återställ filter. Detta är detsamma som att välja **Återställ filter** i filterrutan och kopplar det till fält och totala filter.<br /><br /> Filter återgår till standardfilter för den aktuella vyn. Om den aktuella vyn är **alla** motsvarar detta att återvända till en ofiltrerad vy med alla poster. |
|Ctrl+Enter|Växla fokus från den filterrutan tillbaka till listan.|

## <a name="keyboard-shortcuts-in-cards-and-documents"></a>Kortkommandon i kort och dokument

Följande kortkommandon kan användas för kortsidorna t. ex. **kundkort** och dokumentsidor t. ex. **försäljningsorder** för att visa och ändra poster.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|Alt+D|Öppna posterna för dimensionsuppsättning.|
|Alt+F6|Växla dölj/expandera för den aktuella snabbfliken eller delen (underordnad sida).|
|Alt+F9|Skapa ett nytt dokument och bokföra det.|
|Alt+G|Öppna sidan **Hitta transaktioner** för att söka efter transaktioner som hör till det bokförda dokumentet. Fungerar även på listor.|
|Alt+N |Öppna en sida för att skapa en ny post. På samma sätt som om du markerar åtgärden **nytt**. |
|Alt+Shift+N |Stäng en sida och öppna en ny för att skapa en ny post. På samma sätt som om du markerar åtgärden **OK och Nytt**. |
|Alt+Shift+W |Öppna aktuellt kort eller dokument i ett nytt fönster. Mer information finns i [multikörning på flera sidor.](ui-enter-data.md#multitasking-across-multiple-pages)|
|Ctrl+Enter|Spara och stäng sidan.|
|Ctrl+Nedpil|Öppna nästa post för en enhet.|
|Ctrl+Uppil |Öppna föregående post för en enhet.|
|Ctrl+Ins |Infoga en ny rad i ett dokument|
|Ctrl+radera |Ta bort raden i ett dokument, en journal eller ett förslag.|
|Ctrl+F7|Öppna redovisningstransaktioner, loggtransaktioner, kostnadstransaktioner o.s.v.|
|Ctrl+F9|Frisläpp dokument.|
|Ctrl+Shift+F12 |Maximera radartikeldelen på en dokumentsida Tryck på knapparna igen för att återgå till normal visning. Mer information finns i [Fokusera på radartiklar](ui-enter-data.md#Focus).|
|F6|Flytta till nästa snabbflik eller del (underordnad sida).|
|*F7*|Öppna statistik.|
|*F9*|Bokföra, utfärda, registrera eller återföra dokument.|
|*Shift+Ctrl+F9*|Bokföra, skriva ut och föra in lagerinleverans.|
|Shift+F6|Flytta till föregående snabbflik eller del (underordnad sida).|
|*Shift+F9*|Bokför och skriv ut ett dokument.|

## <a name="quick-entry-shortcuts-for-fields"></a><a name="QuickEntry"></a>Kortkommandon för snabbinmatning för fält

Följande kortkommandon gäller funktionen snabbinmatning på kort, dokument och listsidor. På listor kan inte genvägar användas när listan är i panelvyn. Mer information om snabbinmatnings finns i [påskynda datainmatning med snabbinmatning](ui-enter-data.md#QuickEntry).

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|Anmärkningar|
|--------------------------------|----------|-------|
|Skriv in|Bekräfta värdet i nuvarande fält och gå till nästa snabbinmatningsfält.||
|Shift+Enter|Bekräfta värdet i nuvarande fält och gå till föregående snabbinmatningsfält.||
|Ctrl+Shift+Enter|Bekräfta värdet i nuvarande kolumn och gå till nästa snabbinmatningsfält utanför listan.<br /><br />Detta kortkommando gäller för inbäddade listor på en sida, till exempel radartiklar på en försäljningsorder. På så sätt kan du snabbt komma ut ur listan och fortsätta skriva in data i övriga fält på sidan.|

## <a name="keyboard-shortcuts-in-the-calendar-date-picker"></a><a name="calendarshortcuts"></a> Kortkommandon i kalendern (datumväljare)

När ett datumfält konfigureras kan du ange datumet manuellt eller öppna en kalender (datumväljare) där du kan välja önskat datum. I följande tabell beskrivs kortkommandon för kalendern.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|Ctrl+Home|Öppna kalendern om stängd. **Obs**! detta fungerar inte om datumfältet är i ett rutnät, där Ctrl + start går till den första raden.|
|Ctrl+Home<br />(Cmd+Start)|Flytta till aktuell månad, aktuell dag.|
|Ctrl+Vänsterpil<br />(Cmd+Vänsterpil)|Flytta till föregående dag.|
|Ctrl+Högerpil<br />(Cmd+Högerpil)|Flytta till nästa dag|
|Ctrl+Uppil<br />(Cmd+uppil)|Flytta till föregående vecka, samma dag i veckan.|
|Ctrl+Nedpil<br />(Cmd+nedpil)|Flytta till nästa vecka, samma dag i veckan.|
|Enter|Välj fokuserat datum.|
|Ctrl+End<br />(Cmd+End)|Stäng kalendern och ta bort aktuellt datum.|
|Esc|Stäng kalendern utan markering, och behåll aktuellt datum.|
|Page Down|Flytta till nästa månad|
|Page Up|Flytta till föregående månad|  

## <a name="keyboard-shortcuts-in-date-fields"></a>Kortkommandon i datumfält

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|d|Ange aktuellt datum. "I" betyder "i dag".|
|a|Ange arbetsdatum. Mer information finns i [Arbetsdatum](ui-change-basic-settings.md#work-date)|

## <a name="keyboard-shortcuts-in-the-report-preview"></a><a name="reportpreviewshortcuts"></a>Kortkommandon i Förhandsgranska rapport

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|Nedpil|Rulla nedåt på sidan.|  
|Uppil|Rulla uppåt på sidan.|
|CTRL+0 (noll)<br />(Cmd+0)|Passar in hela sidan på sidan. |
|Ctrl+Home<br />(Cmd+Start)|Gå till den första sidan i rapporten.|
|Ctrl+End<br />(Cmd+Start)|Gå till den sista sidan i rapporten.|
|Vänsterpil|Rulla åt vänster när sidan zoomas in så att den inte visas helt och hållet. |
|Högerpil|Rulla åt höger när sidan zoomas in så att den inte visas helt och hållet. |
|Page Down<br />(Fn+Nedpil)|Gå till nästa sida i rapporten.|
|Page Up<br />(Fn+uppåtpil)|Gå till föregående sida i rapporten.|

## <a name="keyboard-shortcuts-for-zooming-in-and-out"></a><a name="zoomshortcuts"></a>Kortkommandon för zoomning in och ut

|Tryck på dessa tangenter|Om du vill|
|--------------------------------|----------|
|Ctrl + plustecken (+)|Zooma in den aktuella sidan.|  
|Ctrl + minustecken (-)|Zooma ut på den aktuella sidan.|  
|Ctrl+0|Zooma in eller ut till 100 % på den aktuella sidan.|  

## <a name="keyboard-shortcuts-for-role-explorer"></a><a name="roleexplorer"></a>Kortkommandon för rollutforskaren

Rollutforskaren ger dig en översikt över och snabb åtkomst till alla affärsfunktioner som är tillgängliga för din roll. Mer information finns i [Söka efter sidor med rollutforskaren](ui-role-explorer.md).

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|Shift+F12|Öppna rollutforskaren.|
|F3|Öppna rutan **Sök** i rollutforskaren om du vill hitta funktioner baserade på ett visst sökord eller en viss term.|
|F3 eller Ctrl + Nedåtpil|Flyttar fokus till nästa funna funktion i rollutforskaren. F3 flyttar fokus till rutan **Sök** efter den senast funna funktionen.|
|Shift F3 eller Ctrl + Uppåtpil|Flytta fokus till föregående funna funktion i rollutforskaren.|
|Ctrl+Shift|Visa eller dölj alla undernoder – utöver noder på översta nivån – när du väljer åtgärden **Visa** eller **Dölj**.|

##  <a name="numeric-keypad-shortcuts"></a><a name="keypad"></a>Kortkommandon för numeriskt tangentbord

I följande tabell beskriver kortkommandon på en numerisk knappsats.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|--------------------------------|----------|
|Alt+ decimalavgränsare|Ändra resultatet av decimal tecknet till antingen en punkt (.) eller det tecken som bestäms av inställningen **region** på sidan **mina inställningar**. För mer information, se [Ange decimalavgränsare som används av numeriska tangentbord](ui-enter-data.md#decimal).|

## <a name="see-also"></a>Se även

[Snabbguide för kortkommandon – endast dator](keyboard-shortcuts-cheatsheet.md)  
[Hjälpmedelsfunktioner](ui-accessibility.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Vanliga frågor och svar](across-faq.yml)  
[Hitta transaktioner](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

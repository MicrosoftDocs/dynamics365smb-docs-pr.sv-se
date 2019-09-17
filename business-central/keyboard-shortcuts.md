---
title: Kortkommandon
description: En fullständig lista över kombinationer av kortkommandon för att arbeta effektivt med dina data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding, keys
ms.date: 09/06/2019
ms.author: sgroespe
ms.openlocfilehash: e6919dd3e09fcf13bf07b051abfea90a5a35eb01
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985916"
---
# <a name="keyboard-shortcuts"></a>Kortkommandon
Den här artikeln innehåller en översikt över några av de kombinationer av kortkommandon som du kan använda när du arbetar med [!INCLUDE[prodshort](includes/prodshort.md)].

> [!TIP]
> För en snabb utskriftsvänlig översikt över de vanligaste kortkommandona [se referensartikeln här](keyboard-shortcuts-cheatsheet.md) eller klicka på följande bild:
>
>[ ![Om du vill hämta för utskrift, högerklicka och välj spara bild som](media/bckeyboardmap-inline.png) ](media/bckeyboardmap.png#lightbox)

## <a name="overview"></a>Översikt
Kortkommandona förbättrar tillgängligheten och kan göra det enklare och mer effektivt att navigera till olika områden och element på en sida.

Kortkommandona stöds av de flesta webbläsare, beteendet kan dock variera något.

Kortkommandona som beskrivs här gäller amerikansk tangentbordslayout. Tangentlayouten på andra tangentbord kanske inte exakt motsvarar tangenterna på ett amerikanskt tangentbord.

De flesta av dessa genvägar är desamma oavsett om operativsystemet är Windows- eller macOS. Det finns dock några kortkommandon som är olika för macOS. Dessa anges i parantesen i tabellerna i följande avsnitt.

##  <a name="Keyboard"></a> Allmänna kortkommandon
I följande tabell beskrivs kortkommandon för navigering och åtkomst till olika delar av en sida, till exempel åtgärder, listrutor, sökningar och mycket mer. Mer information om kortkommandon för att hantera poster när de visas i en lista finns i nästa avsnitt.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|----------------|-----------|
|Alt+nedpil|Öppna en listruta eller leta upp ett värde för ett fält.|    
|Alt+Högerpil|Se de transaktioner som resulterade i ett beräknat värde i ett fält.|  
|Alt+F2|Visa och dölj rutan Faktabox|
|Alt+Q<br />(Ctrl+Alt+Q)|Öppna rutan **Berätta vad du vill göra** som hjälper dig att söka efter en sida, en rapport, en åtgärd på den aktuella sidan eller en artikel i dokumentationen.|
|Alt+T|Öppna sidan **Mina inställningar**.|
|Alt+Uppil|Visa knappbeskrivning för ett fält eller en kolumnrubrik i en tabell. Om det finns valideringsfel för fältet, trycker du på ”Alt + Uppil” för att visa innehålla valideringsfelet. Tryck på ”Esc” eller ”Alt + Uppil” för att stänga knappbeskrivningen.|
|Ctrl+Alt+F1|Öppna och stäng sidinspektionsrutan. Sidinspektionsrutan visar information om sidan, t.ex. dess källtabell, fält, filter, tillägg och annat.<br /><br />Mer information finns i [Inspektionssidor](across-inspect-page.md).|
|Ctrl+C |Kopiera värdet i fältet. Om fältet är i fokus och du inte har valt någon text i fältet, kommer hela värdet att kopieras. Om du har markerat en text i fältet, kopieras endast den markerade texten.|
|Ctrl+F1|Öppna Business Central-hjälpen för sidan.|
|Ctrl+F5|Läs [!INCLUDE[prodshort](includes/prodshort.md)]-programmet på nytt.<br/><br />Detta är ungefär som att markera uppdatera/läsa in på nytt i webbläsaren.|
|F5|Uppdatera informationen på den aktuella sidan.<br /><br />Använd detta för att se till att informationen på sidan har uppdaterats med ändringarna som andra har gjort medan du arbetar.|
|Ctrl+F12|Växla mellan breda och smala vyn.|
|Skriv in|Aktivera eller nå elementet eller kontrollen som är i fokus.|
|Esc|Stäng den aktuella sidan eller listan.|
|Tabb|Flytta fokus till nästa kontroll eller element på en sida, till exempel åtgärder, knappar, fält eller listrubriker.|
|Skift+Tabb|Flytta fokus till föregående kontroll eller element på en sida, till exempel åtgärder, knappar, fält eller listrubriker.|

## <a name="keyboard-shortcuts-in-lists"></a>Kortkommandon i listor

I följande tabell beskrivs de kortkommandon som du kan använda i en listsida. Genvägsåtgärden skiljer sig något beroende på om sidan visas som listvy eller sida vid sida.
<!--
> [!Note]
> In the table that follows, the term *actionable field* refers to a field on which you can do something, like change a value or link to another page. In general, the shortcuts will skip over fields that display information that you cannot change from the list (in other words, fields that are read-only).
-->
### <a name="general"></a>Allmänt

|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista|För att göra detta som en panelvisning |
|-----------------|-------|-------|
|Alt+F7 |Sortera markerad kolumn i stigande eller fallande ordning.|Ej tillämpbart.|
|Shift+F10 |Öppna en meny med alternativ som är tillgängliga för den markerade raden.|Ej tillämpbart.|
|Alt+N |Öppna en sida för att skapa en ny post. På samma sätt som om du markerar åtgärden **nytt**. |Samma.|

### <a name="navigateshortcuts"></a>Navigera mellan rader och kolumner

|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista |För att göra detta som en panelvisning |
|-----------------|-------|-------|
|Ctrl+Home<br />(Fn+Ctrl+vänsterpil)|Markera den första raden i listan. Fokus är kvar i samma kolumn.|Flytta till första panelen i den första raden. |
|Ctrl+End<br />(Fn+Ctrl+högerpil)|Markera den sista raden i listan. Fokus är kvar i samma kolumn.|Flytta till den sista panelen i den sista raden.|
|Hem<br />(Fn+vänsterpil)|Flytta till första fältet i raden.|Flytta till första panelen i raden.|
|End<br />(Fn+högerpil)|Flytta till det sista fältet i raden.|Flytta till den sista panelen i raden.|
|Skriv in|Öppna posten som är associerad med fältet.<br /><br />Endast relevant om en sida med kort associerad med posten.|Posten öppnas.<br /><br />Endast relevant om en sida med kort associerad med posten.|
|Ctrl+Enter|Flytta fokus till nästa element utanför listan.|Flytta fokus till nästa element utanför listan.|
|Nedpil|Flytta till fältet i raden nedanför i samma kolumn. |I samma kolumn, flytta till panelen i raden nedanför. |
|Uppil|Flytta till fältet i raden ovanför i samma kolumn| I samma kolumn, flytta till panelen i raden ovanför  |
|Högerpil|I en skrivskyddad lista, flytta till samma rad till höger i samma fält.<br /><br />Flytta till höger i det aktuella fältet i en redigeringsbar lista.| Flytta till nästa ändringsbara panel till höger i samma rad. |
|Vänsterpil|I en skrivskyddad lista, flytta till samma rad till vänster i föregående fält. <br /><br />Flytta till vänster i det aktuella fältet i en redigeringsbar lista.| Flytta till föregående panel till vänster i samma rad. |
|Page Up<br />(Fn+uppåtpil)|Rulla för att visa uppsättningen med rader ovanför den aktuella raden i vyn. |Rullar för att visa uppsättningen med paneler ovanför den aktuella panelen i vyn. |
|Page Down<br />(Fn+nedpil)|Rulla för att visa uppsättningen med rader nedanför den aktuella raden i vyn.|Rulla för att visa uppsättningen med paneler nedanför den aktuella panelen i vyn.|
|Tabb|I en redigerbar lista, flytta till samma rad till höger i samma fält.|Ej tillämpbart.||
|Skift+Tabb|I en redigerbar lista, flytta till samma rad till vänster i föregående fält. | Ej tillämpbart. |

### <a name="CopyRows"></a>Välja kopiera och klistra in

|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista |För att göra detta som en panelvisning |
|-----------------|-------|-------|
|Ctrl + klicka<br />(Cmd + klicka)|Utöka radmarkeringen så att den rad som du klickar på inkluderas.|Ej tillämpbart.|
|Skift+klicka|Utöka radmarkeringen så att den rad som du klickar på och samtliga där emellan inkluderas.<br /><br />Du kan använda detta när du har använt Ctrl + uppåtpil eller Ctrl + uppåtpil/nedpil för att utöka ditt val.|Ej tillämpbart.|
|Ctrl+Uppil<br />(Ctrl+Cmd+uppil)|Flytta fokus till raden ovanför och behåll den aktuella raden som har valts.|Ej tillämpbart.|
|Ctrl+Nedpil<br />(Ctrl+Cmd+nedpil)|Flytta fokus till raden nedanför och behåll den aktuella raden som har valts.|Ej tillämpbart.|
|Ctrl+Blanksteg<br />(Ctrl + Cmd + blanksteg )|Utöka radmarkeringen så att den markerade raden inkluderas.<br /><br />Du kan använda detta när du har använt Ctrl + uppåtpil eller Ctrl + nedpil för att utöka ditt val.|Ej tillämpbart.|
|Ctrl+A|Markera alla rader.|Ej tillämpbart.|
|Shift+Uppil|Utöka radmarkeringen så att raden ovan inkluderas.|Ej tillämpbart.|
|Shift+nedpil|Utöka radmarkeringen så att raden nedan inkluderas.|Ej tillämpbart.|
|Shift+Page Up<br />(Shift+Fn+uppil)|Utöka radmarkeringen så att samtliga rader som visas ovanför den aktuella radmarkeringen inkluderas.|Ej tillämpbart.|
|Shift+Page Down<br />(Shift+Fn+nedpil)|Utöka radmarkeringen så att samtliga synliga rader nedanför den aktuella radmarkeringen inkluderas.|Ej tillämpbart.|
|Ctrl+C<br />(Cmd+C)|Kopiera de markerade raderna till Urklipp.|Ej tillämpbart.|
|Ctrl+V<br />(Cmd+V)|Klistra in de markerade raderna från Urklipp till den aktuella sidan eller ett externt dokument såsom Microsoft Excel eller Outlook e-post. Du kan bara göra detta i redigerbara listor.|Ej tillämpbart.|
|F8|Kopiera fältet i samma kolumn i raden ovanför och klistra in den i den aktuella raden. Du kan bara göra detta i redigerbara listor. Med detta kortkommando följt av en flik kan du snabbt kan fylla i fält i radposter som du vill ska ha samma värde som raden ovan.|Ej tillämpbart.|

### <a name="KeyboardFilter"></a>Söka och filtrera listor

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|F3|Växlar sökrutan.<ul><li>Aktivera sökrutan så att du kan börja skriva söktexten.</li><li>Om sökrutan redan är aktiverad, återgår F3 till listan utan att radera söktexten.</li><ul>|
|Shift+F3|Öppna och stäng filterrutan.<ul><li> Om filterrutan inte är öppen kan du öppna den med Skift + F3 och visar åtgärden **+ Filter** enligt **Filtrera lista efter**, vilket gör att du bara behöver trycka på RETUR för att börja lägga till ett fältfilter.</li><li>Om filterrutan redan är öppen stängs den med SKIFT + F3 men rensar inte alla filter som du har lagt till.</li></ul>|
|Ctrl+Shift+F3|Öppna och stäng filterrutan.<ul><li> Om filterrutan inte är öppen kan du öppna den med Ctrl + Skift + F3 och visar åtgärden **+ Filter** enligt **Filtrera summa efter**, vilket gör att du bara behöver trycka på RETUR för att börja lägga till ett summeringsfilter.</li><li>Om filterrutan redan är öppen stängs den med Ctrl + Skift + F3 men rensar inte alla filter som du har lagt till.</li></ul>  |
|Alt+F3|Aktivera/inaktivera filtreringen till det valda värdet.<ul><li>Använder ett kolumnfilter på det markerade filtervärdet i listan. Detta är detsamma som att välja **filtrera på det här värdet** från en kolumnrubrik. Den öppnar filterrutan, ställer in filter till det valda värdet när fokus är på en cell i listan.</li><li>Om kolumnen redan är filtrerad rensar Alt + F3 filtret på den kolumnen.</li></ul> |
|Shift+Alt+F3|Öppna filterfönstret och lägg till ett filter för den markerade kolumnen i listan. Fokus är på det nya filterfältet som börjar skriva filterkriterierna direkt.<br /><br /> Detta innebär att välja **Filter** från kolumnrubriken.<br /><br />Om det redan finns ett filter i fältet, läggs ett nytt filter till. |
|Ctrl+Shift+Alt+F3|Återställ filter. Detta är detsamma som att välja **Återställ filter** i filterrutan och kopplar det till fält och totala filter.<br /><br /> Filter återgår till standardfilter för den aktuella vyn. Om den aktuella vyn är **alla** motsvarar detta att återvända till en ofiltrerad vy med alla poster. |
|Ctrl+Enter|Växla fokus från den filterrutan tillbaka till listan.|

## <a name="keyboard-shortcuts-in-cards-and-documents"></a>Kortkommandon i kort och dokument

Följande kortkommandon kan användas för kortsidorna (t.ex. **kund**) och dokumentsidor (t.ex. **försäljningsorder**) för att visa och ändra poster.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|----------------|-----------|
|Alt+F6|Komprimera och expandera den aktuella snabbfliken.|
|Alt+N |Öppna en sida för att skapa en ny post. På samma sätt som om du markerar åtgärden **nytt**. |
|Alt+Shift+N |Stäng den aktuella kortsidan och skapa ett nytt företag. samma som att välja bakåtpilen och sedan åtgärden **nytt**.|
|Ctrl+Nedpil|Öppna nästa post för en enhet.|
|Ctrl+Uppil |Öppna föregående post för en enhet.|
|Ctrl+Shift+F12 |Maximera radartiklar i ett dokument, t.ex. en försäljningsorder eller faktura. Andra delar av sidan är dolda och radartikeldelen utökas till hela arbetsytan. Tryck på knapparna igen för att återgå till normal visning.<br /><br />Mer information finns i [Fokusera på radartiklar](ui-enter-data.md#Focus).|
|F6|Flytta till nästa snabbflik eller del (underordnad sida).|
|Shift+F6|Flytta till föregående snabbflik eller del (underordnad sida).|

## <a name="QuickEntry"></a>Kortkommandon för snabbinmatning för fält

Följande kortkommandon gäller funktionen snabbinmatning på kort, dokument och listsidor. På listor kan inte genvägar användas när listan är i panelvyn. Mer information om snabbinmatnings finns i [påskynda datainmatning med snabbinmatning](ui-enter-data.md#QuickEntry).

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|Anmärkningar|
|-----------------|-------|-------|
|Skriv in|Bekräfta värdet i nuvarande fält och gå till nästa snabbinmatningsfält.||
|Shift+Enter|Bekräfta värdet i nuvarande fält och gå till föregående snabbinmatningsfält.||
|Ctrl+Shift+Enter|Bekräfta värdet i nuvarande kolumn och gå till nästa snabbinmatningsfält utanför listan.<br /><br />Detta kortkommando gäller för inbäddade listor på en sida, till exempel radartiklar på en försäljningsorder. På så sätt kan du snabbt komma ut ur listan och fortsätta skriva in data i övriga fält på sidan.|

## <a name="keyboard-shortcuts-in-worksheets"></a>Kortkommandon i kalkylark

Följande kortkommandon finns endast på kalkylarksidor, t.ex. **artikeljournaler**.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|  
|----------------|-----------|  
|Ctrl+radera| Ta bort en radartikel.|

## <a name="a-namecalendarshortcuts-keyboard-shortcuts-in-the-calendar-date-picker"></a><a name="calendarshortcuts"/> Kortkommandon i kalendern (datumväljare)

När ett datumfält konfigureras kan du ange datumet manuellt eller öppna en kalender (datumväljare) där du kan välja önskat datum. I följande tabell beskrivs kortkommandon för kalendern.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|Ctrl+Home|Öppna kalendern om stängd.|
|Ctrl+Home<br />(Cmd+Start)|Flytta till aktuell månad, aktuell dag.|
|Ctrl+Vänsterpil<br />(Cmd+Vänsterpil)|Flytta till föregående dag.|
|Ctrl+Högerpil<br />(Cmd+Högerpil)|Flytta till nästa dag|
|Ctrl+Uppil<br />(Cmd+uppil)|Flytta till föregående vecka, samma dag i veckan.|
|Ctrl+Nedpil<br />(Cmd+nedpil)|Flytta till nästa vecka, samma dag i veckan.|
|Enter|Välj fokuserat datum.|
|Ctrl+End<br />(Cmd+End)|Stäng kalendern och ta bort aktuellt datum.|
|Esc|Stäng kalendern utan markering, behåll aktuellt datum.|
|Page Down|Flytta till nästa månad|
|Page Up|Flytta till föregående månad|  

## <a name="keyboard-shortcuts-in-date-fields"></a>Kortkommandon i datumfält
|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|d|Ange aktuellt datum. "I" betyder "i dag".|
|a|Ange arbetsdatum. Mer information finns i [Arbetsdatum](ui-change-basic-settings.md#work-date)|

## <a name="a-namereportpreviewshortcutskeyboard-shortcuts-in-the-report-preview"></a><a name="reportpreviewshortcuts"/>Kortkommandon i Förhandsgranska rapport

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|Nedpil|Rulla nedåt på sidan.|  
|Uppil|Rulla uppåt på sidan.|
|CTRL+0 (noll)<br />(Cmd+0)|Passar in hela sidan på sidan. |
|Ctrl+Home<br />(Cmd+Start)|Gå till den första sidan i rapporten.|
|Ctrl+End<br />(Cmd+Start)|Gå till den sista sidan i rapporten.|
|Vänsterpil|Rulla åt vänster när sidan zoomas in så att den inte visas helt och hållet. |
|Högerpil|Rulla åt höger när sidan zoomas in så att den inte visas helt och hållet. |
|Page Down<br />(Fn+Nedpil)|Gå till nästa sida i rapporten.|
|Page Up<br />(Fn+uppåtpil)|Gå till föregående sida i rapporten.|

## <a name="see-also"></a>Se även

[Hjälpmedelsfunktioner](ui-accessibility.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vanliga frågor och svar](across-faq.md)  

---
title: Kortkommandon
description: En fullständig lista över kombinationer av kortkommandon för att arbeta effektivt med dina data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding, keys
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 5b7c5282a89a1dfb39f3e94feab8e00d2373f8af
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "806903"
---
# <a name="keyboard-shortcuts"></a>Kortkommandon
Den här artikeln innehåller en översikt över några av de kombinationer av kortkommandon som du kan använda när du arbetar med [!INCLUDE[prodshort](includes/prodshort.md)].

[Utskriftsvänlig kortkommandoreferens](keyboard-shortcuts-cheatsheet.md)

## <a name="overview"></a>Översikt
Kortkommandona förbättrar tillgängligheten och kan göra det enklare och mer effektivt att navigera till olika områden och element på en sida.

Kortkommandona stöds av de flesta webbläsare, beteendet kan dock variera något.

Kortkommandona som beskrivs här gäller amerikansk tangentbordslayout. Tangentlayouten på andra tangentbord kanske inte exakt motsvarar tangenterna på ett amerikanskt tangentbord.

De flesta av dessa genvägar är desamma oavsett om operativsystemet är Windows- eller macOS. Det finns dock några kortkommandon som är olika för macOS. Dessa anges i parantesen i tabellerna i följande avsnitt.

##  <a name="Keyboard"></a> Allmänna kortkommandon
I följande tabell beskrivs kortkommandon för navigering och åtkomst till olika delar av en sida, till exempel åtgärder, listrutor, sökningar och mycket mer. Mer information om kortkommandon för att hantera poster när de visas i en lista finns i nästa avsnitt.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|  
|----------------|-----------|  
|Alt+Q<br />(Ctrl+Alt+Q)|Öppna rutan **Berätta vad du vill göra** som hjälper dig att söka efter en sida, en rapport, en åtgärd på den aktuella sidan eller en artikel i dokumentationen.|
|Alt+Uppil|Visa knappbeskrivning för ett fält eller en kolumnrubrik i en tabell. Om det finns valideringsfel för fältet, trycker du på ”Alt + Uppil” för att visa innehålla valideringsfelet. Tryck på ”Esc” eller ”Alt + Uppil” för att stänga knappbeskrivningen.|
|Tabb|Flytta fokus till nästa kontroll eller element på en sida, till exempel åtgärder, knappar, fält eller listrubriker.|
|Skift+Tabb|Flytta fokus till föregående kontroll eller element på en sida, till exempel åtgärder, knappar, fält eller listrubriker.|   
|Enter|Aktivera eller nå elementet eller kontrollen som är i fokus.|   
|Alt+nedpil|Öppna en listruta eller leta upp ett värde för ett fält.|    
|Alt+Högerpil|Se de transaktioner som resulterade i ett beräknat värde i ett fält.|  
|F5|Uppdatera informationen på den aktuella sidan.|Använd detta för att se till att informationen på sidan har uppdaterats med ändringarna som andra har gjort medan du arbetar.|
|Ctrl+F5|Läs [!INCLUDE[prodshort](includes/prodshort.md)]-programmet på nytt.|Detta är ungefär som att markera uppdatera/läsa in på nytt i webbläsaren.|
|Esc|Stäng den aktuella sidan eller listan.|


## <a name="keyboard-shortcuts-in-lists"></a>Kortkommandon i listor

I följande tabell beskrivs de kortkommandon som du kan använda i en listsida. Genvägsåtgärden skiljer sig något beroende på om sidan visas som listvy eller sida vid sida.
<!--
> [!Note]
> In the table that follows, the term *actionable field* refers to a field on which you can do something, like change a value or link to another page. In general, the shortcuts will skip over fields that display information that you cannot change from the list (in other words, fields that are read-only).
-->

### <a name="navigateshortcuts"></a> Navigera mellan rader och kolumner

|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista |För att göra detta som en panelvisning |Anmärkningar|
|-----------------|-------|-------|-------|
|Uppil|Flytta till fältet i raden ovanför i samma kolumn| I samma kolumn, flytta till panelen i raden ovanför  |  |
|Nedpil|Flytta till fältet i raden nedanför i samma kolumn. |I samma kolumn, flytta till panelen i raden nedanför. | |
|Högerpil|I en skrivskyddad lista, flytta till samma rad till höger i samma fält.<br /><br />Flytta till höger i det aktuella fältet i en redigeringsbar lista.| Flytta till nästa ändringsbara panel till höger i samma rad. ||
|Vänsterpil|I en skrivskyddad lista, flytta till samma rad till vänster i föregående fält. <br /><br />Flytta till vänster i det aktuella fältet i en redigeringsbar lista.| Flytta till föregående panel till vänster i samma rad. ||
|Tabb|I en redigerbar lista, flytta till samma rad till höger i samma fält.|Ej tillämpbart.||
|Skift+Tabb|I en redigerbar lista, flytta till samma rad till vänster i föregående fält. | Ej tillämpbart. ||
|Hem<br />(Fn+vänsterpil)|Flytta till första fältet i raden.|Flytta till första panelen i raden.||
|End<br />(Fn+högerpil)|Flytta till det sista fältet i raden.|Flytta till den sista panelen i raden.||
|Page Up<br />(Fn+uppåtpil)|Rullar för att visa uppsättningen med rader ovanför den aktuella raden i vyn. |Rullar för att visa uppsättningen med paneler ovanför den aktuella panelen i vyn. ||
|Page Down<br />(Fn+nedpil)|Rullar för att visa uppsättningen med rader nedanför den aktuella raden i vyn.|Rullar för att visa uppsättningen med paneler nedanför den aktuella panelen i vyn.||
|Enter|Öppna posten som är associerad med fältet.|Posten öppnas.| Endast relevant om en sida med kort associerad med posten.|
|Ctrl+Enter|Flytta fokus till nästa element utanför listan.|Flytta fokus till nästa element utanför listan.||

### <a name="CopyRows"></a>Markera, kopiera och klistra in
|Tryck på dessa tangenter<br />(i macOS)|För att göra detta som en lista |För att göra detta som en panelvisning |Anmärkningar|
|-----------------|-------|-------|-------|
|Ctrl+Home<br />(Fn+Ctrl+vänsterpil)|Markera den första raden i listan. Fokus flyttas då till det första fältet i raden.|Flytta till första panelen i den första raden. ||
|Ctrl+End<br />(Fn+Ctrl+högerpil)|Markera den sista raden i listan. Fokus flyttas då till det sista fältet i raden.|Flytta till den sista panelen i den sista raden.||
|Ctrl + klicka<br />(Cmd + klicka)|Utöka radmarkeringen så att den rad som du klickar på inkluderas.|Ej tillämpbart.||
|Skift+klicka|Utöka radmarkeringen så att den rad som du klickar på och samtliga där emellan inkluderas.|Ej tillämpbart.|Du kan använda detta när du har använt Ctrl + uppåtpil eller Ctrl + uppåtpil/nedpil för att utöka ditt val.|
|Ctrl+Uppil<br />(Ctrl+Cmd+uppil)|Flytta fokus till raden ovanför och behåll den aktuella raden som har valts.|Ej tillämpbart.||
|Ctrl+Nedpil<br />(Ctrl+Cmd+nedpil)|Flytta fokus till raden nedanför och behåll den aktuella raden som har valts.|Ej tillämpbart.||
|Ctrl+Blanksteg<br />(Ctrl + Cmd + blanksteg )|Utöka radmarkeringen så att den markerade raden inkluderas.|Ej tillämpbart.|Du kan använda detta när du har använt Ctrl + uppåtpil eller Ctrl + nedpil för att utöka ditt val.|
|Ctrl+A|Markera alla rader.|Ej tillämpbart.||
|Shift+Uppil|Utöka radmarkeringen så att raden ovan inkluderas.|Ej tillämpbart.||
|Shift+nedpil|Utöka radmarkeringen så att raden nedan inkluderas.|Ej tillämpbart.||
|Shift+Page Up<br />(Shift+Fn+uppil)|Utöka radmarkeringen så att samtliga rader som visas ovanför den aktuella radmarkeringen inkluderas.|Ej tillämpbart.||
|Shift+Page Down<br />(Shift+Fn+nedpil)|Utöka radmarkeringen så att samtliga synliga rader nedanför den aktuella radmarkeringen inkluderas.|Ej tillämpbart.||
|Ctrl+C<br />(Cmd+C)|Kopiera de markerade raderna till Urklipp.|Ej tillämpbart.||
|Ctrl+V<br />(Cmd+V)|Klistra in de markerade raderna från Urklipp till den aktuella sidan eller ett externt dokument såsom Microsoft Excel eller Outlook e-post.|Ej tillämpbart.|Du kan bara göra dessa redigerbara listor.|
|F8|Kopiera fältet i samma kolumn i raden ovanför och klistra in den i den aktuella raden.|Ej tillämpbart.|Du kan bara göra detta i redigerbara listor. Med detta kortkommando följt av en flik kan du snabbt kan fylla i fält i radposter som du vill ska ha samma värde som raden ovan.|

### <a name="KeyboardFilter"></a> Kortkommandon för att söka och filtrera listor

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|F3|Växlar sökrutan.<ul><li>Aktiverar sökrutan så att du kan börja skriva söktexten.</li><li>Om sökrutan redan är aktiverad, återgår F3 till listan utan att radera söktexten.</li><ul>|  
|Shift+F3|Öppnar och stänger filterrutan.<ul><li> Om filterrutan inte är öppen kan du öppna den med Skift + F3 och visar åtgärden **+ Filter** enligt **Filtrera lista efter**, vilket gör att du bara behöver trycka på RETUR för att börja lägga till ett fältfilter.</li><li>Om filterrutan redan är öppen stängs den med SKIFT + F3 men rensar inte alla filter som du har lagt till.</li></ul>|
|Ctrl+Shift+F3|Öppnar och stänger filterrutan.<ul><li> Om filterrutan inte är öppen kan du öppna den med Ctrl + Skift + F3 och visar åtgärden **+ Filter** enligt **Filtrera summa efter**, vilket gör att du bara behöver trycka på RETUR för att börja lägga till ett summeringsfilter.</li><li>Om filterrutan redan är öppen stängs den med Ctrl + Skift + F3 men rensar inte alla filter som du har lagt till.</li></ul>  |
|Alt+F3|Växlar filtrering till det värdet.<ul><li>Använder ett kolumnfilter på det markerade filtervärdet i listan. Detta är detsamma som att välja **filtrera på det här värdet** från en kolumnrubrik. Den öppnar filterrutan, ställer in filter till det valda värdet när fokus är på en cell i listan.</li><li>Om kolumnen redan är filtrerad rensar Alt + F3 filtret på den kolumnen.</li></ul> |
|Shift+Alt+F3|Öppnar filterfönstret och lägger till ett filter för den markerade kolumnen i listan. Fokus är på det nya filterfältet som börjar skriva filterkriterierna direkt.<br /><br /> Detta innebär att välja **Filter** från kolumnrubriken. menyn. Visar filterrutan, lägger till filtret, ställer in fokus på det så att användaren kan ange ett värde att filtrera efter.<br /><br />Om det redan finns ett filter i fältet, läggs ett nytt filter till. |
|Ctrl+Shift+Alt+F3|Återställer filter. Detta är detsamma som att välja **Återställ filter** i filterrutan och kopplar det till fält och totala filter.<br /><br /> Filter återgår till standardfilter för den aktuella vyn. Om den aktuella vyn är **alla** motsvarar detta att återvända till en ofiltrerad vy med alla poster. |
|Ctrl+Enter|Går tillbaka till listan från filterrutan.|

## <a name="a-namecalendarshortcuts-keyboard-shortcuts-in-the-calendar-date-picker"></a><a name="calendarshortcuts"/> Kortkommandon i kalendern (datumväljare)
När ett datumfält konfigureras kan du ange datumet manuellt eller öppna en kalender (datumväljare) där du kan välja önskat datum. I följande tabell beskrivs kortkommandon för kalendern.

|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|Page Up|Flytta till föregående månad|  
|Page Down|Flytta till nästa månad|
|Ctrl+Home|Öppna kalendern om stängd.|
|Ctrl+Home<br />(Cmd+Start)|Flytta till aktuell månad, aktuell dag.|
|Ctrl+Vänsterpil<br />(Cmd+Vänsterpil)|Flytta till föregående dag.|
|Ctrl+Högerpil<br />(Cmd+Högerpil)|Flytta till nästa dag|
|Ctrl+Uppil<br />(Cmd+uppil)|Flytta till föregående vecka, samma dag i veckan.|
|Ctrl+Nedpil<br />(Cmd+nedpil)|Flytta till nästa vecka, samma dag i veckan.|
|Enter|Välj fokuserat datum.|
|Ctrl+End<br />(Cmd+End)|Stäng kalendern och ta bort aktuellt datum.|
|Esc|Stäng kalendern utan markering, behåll aktuellt datum.|

## <a name="a-namereportpreviewshortcutskeyboard-shortcuts-in-the-report-preview"></a><a name="reportpreviewshortcuts"/>Kortkommandon i Förhandsgranska rapport
|Tryck på dessa tangenter<br />(i macOS)|Om du vill|
|-----------------|-------|
|Nedpil|Rulla nedåt på sidan.|  
|Uppil|Rulla uppåt på sidan.|
|Högerpil|Rulla åt höger när sidan zoomas in så att den inte visas helt och hållet. |
|Vänsterpil|Rulla åt vänster när sidan zoomas in så att den inte visas helt och hållet. |
|CTRL+0 (noll)<br />(Cmd+0)|Passar in hela sidan på sidan. |
|Ctrl+Home<br />(Cmd+Start)|Gå till den första sidan i rapporten.|
|Ctrl+End<br />(Cmd+Start)|Gå till den sista sidan i rapporten.|
|Page Down<br />(Fn+Nedpil)|Gå till nästa sida i rapporten.|
|Page Up<br />(Fn+uppåtpil)|Gå till föregående sida i rapporten.|


<!--
## Keyboard shortcuts in list (shown as tiles)

The following table describes the keyboard shortcuts that you can use in a list page when the page is shown as a tiles.


|Keyboard Shortcut<br />(shortcut in osX)| Action|Remarks|
|-----------------|-------|-------|
|Up Arrow|Move to the tile above in the same column|  |   
|Down Arrow|Move to the tile below in the same column|  |
|Right Arrow|Move to the next tile in the same row| |
|Left Arrow|Move to the previous tile in the same row | |
|Home<br />(Fn+left Arrow)|Move to the first tile in the row|
|End<br />Fn+right Arrow)|Move to the last tile in the row|
|Page Up<br />(Fn+up Arrow)|Move up in the same column to the uppermost visible row|
|Page Down<br />(Fn+down Arrow)|Move down in the same column to the lowermost visible row|
|Enter<br />(Fn+down Arrow)|Opens the record (when a card page is available).|
-->

## <a name="see-also"></a>Se även
[Hjälpmedelsfunktioner](ui-accessibility.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vanliga frågor och svar](across-faq.md)  

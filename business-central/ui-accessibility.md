---
title: Hjälpmedelsfunktioner
description: Den här artikeln innehåller information om kortkommandon och andra hjälpfunktioner i Business Central för personer med funktionshinder.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accessibility, shortcuts, charts, tooltips, screen reader'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Hjälpmedel och kortkommandon

Den här artikeln innehåller information om de funktioner som gör [!INCLUDE[prod_short](includes/prod_short.md)] tillgängligt för användare med funktionshinder. [!INCLUDE[prod_short](includes/prod_short.md)] stöder följande hjälpmedelsfunktioner:  

- Kortkommandon. Se [Kortkommandon](keyboard-shortcuts.md).
- Gester för touch och penna för surfplatta och telefoner. Se [Gester för touch och penna](touch-gestures.md).
- Navigering  
- Rubriker  
- Alternativ text för bilder och länkar  
- Stöd för vanliga hjälpmedel 
- Zooma in eller ut på valfri sida
- Funktionsbeskrivningar för element i användargränssnittet

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="navigation"></a><a name="Navigation"></a>Navigering
  
Du kan använda olika kombinationer av TAB, SKIFT och piltangenter för att flytta mellan element på en sida. Element kan vara åtgärder, fält och kolumner, delar och andra kontroller. I allmänhet, välj <kbd>Tabb</kbd> eller <kbd>Shift</kbd>+<kbd>Tabb</kbd> för att gå till nästa eller föregående element.

När du fokuserar på ett område som innehåller åtgärder, som navigeringsfältet överst i rollcentret eller åtgärdsfältet på andra sidor, använder du piltangenterna för att förflytta dig mellan olika åtgärder och grupper. Välj <kbd>Retur</kbd> på en grupp för att öppna dess underliggande åtgärder och fortsätt sedan med piltangenterna. Välj <kbd>Tabb</kbd> eller <kbd>Shift</kbd>+<kbd>Tabb</kbd> om du vill flytta ut från åtgärdsområdet.

Med tabbordningen kan du också växla mellan den primära webbläsarsidan och dialogrutor som begär exempelvis bekräftelse eller inloggningssidan.  

## <a name="headings-in-content"></a><a name="Headings"></a>Rubriker i innehåll

HTML-källan för [!INCLUDE[prod_short](includes/prod_short.md)]-innehåll använder taggar för att hjälpa användare av tekniska hjälpmedel för att förstå sidans struktur och innehåll. På listsidor definieras exempelvis kolumnerna i TH-taggar, och kolumnrubrikerna anges med attributet TITLE inuti taggen. Rubriker för element, till exempel snabbflikar, faktaboxar och fält ingår i rubriktaggarna (H1, H2, H3 och H4).  

## <a name="image-and-links"></a><a name="Images"></a>Bilder och länkar

En beskrivande text för bilder anges med attributet ALT i IMG-taggen. En beskrivande text för hyperlänkar anges med rubrikattributet inuti A-taggen.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a>Hjälpmedel

[!INCLUDE[prod_short](includes/prod_short.md)] stöder olika hjälpmedel, till exempel hög kontrast, skärmläsare och program för röstigenkänning. Vissa hjälpmedel fungerar kanske inte tillsammans med vissa element på [!INCLUDE[prod_short](includes/prod_short.md)]-sidor.  

## <a name="zoom"></a><a name="zoom"></a>Zooma

I de flesta webbläsare används vanliga kortkommandon för att zooma in och ut på den aktuella sidan. Dessa kortkommandon är inte specifika för [!INCLUDE [prod_short](includes/prod_short.md)], men de fungerar när du använder [!INCLUDE [prod_short](includes/prod_short.md)] i en webbläsare. En lista över vilka kortkommandon som stöds finns i [Kortkommandon för att zooma in och ut](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Knappbeskrivningar

Beskrivningar är tillgängliga för de flesta element i användargränssnittet, t. ex. sidfält och kolumner, åtgärder, skärmtips och diagram. En knappbeskrivning innehåller extra text som förklarar ett element som gör det enklare att förstå dess syfte. 

Du kan använda funktionsbeskrivningar på olika sätt beroende på klienten (webb eller mobil) och den enhet som du arbetar med. Använd följande tabell som en guide. Vissa beskrivningar kan läsas av skärmläsare. I det här fallet kommer du åt knappbeskrivningarna som beskrivs i tabellen och använder sedan skärmläsaren för att navigera till knappbeskrivningen på samma sätt som med andra element.

#### <a name="accessing-tooltips"></a>Komma åt knappbeskrivningar

|Element|Musåtgärd för webbklient|Kortkommando för webbklient|Tryckgester på surfplatta/telefon för mobilapp|Stöd för skärmläsare|
|-------|-----------------|------------|--------------------------|---------------------|
|Sidfält och kolumnrubriker|Hovra över eller klicka på fältrubriken eller kolumnrubriken|Flytta fokus till fältet eller kolumnrubriken och välj tangenterna <kbd>Alt</kbd>+<kbd>Uppil</kbd>|Tryck på fältrubriken |ja|
|Diagramelement, som en stapel, linje, cirkelsegment|Hovra över elementet|Flytta fokus till element med hjälp av piltangenterna|Tryck och håll ned elementet|ja|
|Åtgärder|Hovra över åtgärden|ingen|ingen |nej|
|Stack-ikoner|Hovra över panelen |ingen|ingen|nej|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>Mer information om hjälpmedel

Du hittar mer information om åtkomst via Microsofts produkter och hjälpmedel på webbplatsen för [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).

## <a name="see-also"></a>Se även

[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Vanliga frågor och svar](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Vanliga frågor om listvyer
description: Detaljerad information om hur du sparar filter som listvyer.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: 7b992fe4f5db07605015a88ea69d9a510adbcca4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925515"
---
# <a name="list-views-faq"></a>Vanliga frågor om listvyer
I det här avsnittet besvaras frågor som våra erfarna användare ofta ställer på att arbeta med listvyer och spara filter.  

### <a name="how-do-views-handle-expressions"></a>Hur hanterar vyer uttryck?
När du sparar en vy som innehåller filter med uttryck, t.ex. datumintervall, operatorer, nyckelord eller filterspecifikationer, sparas uttrycket och inte resultatvärdena. Om du till exempel sparar en vy som filtrerar efter fältet **Sparad datum** med uttrycket **-1V..idag** kommer alltid poster att sökas i förhållande till det aktuella datumet, även om vyn öppnas nästa månad.

### <a name="where-are-list-views-saved"></a>Var sparas listvyer?
På samma sätt som du döljer ett fält eller sorterar om navigeringsmenyn är listvyn en del av användaranpassningen och lagras i databasen. Om du avmarkerar all anpassning i en lista kommer dina personliga vyer också att tas bort permanent och ytterligare anpassningar, till exempel omordning av vyer. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a>Varför har jag inte någon Spara-ikon?
Spara-ikonen och alternativmenyn visas inte bredvid vyer i filterrutan om anpassningar inaktiveras för en användarroll. Användare som inte har anpassningsfunktionen aktiverade kan fortfarande komma åt systemvyer som är en standarddel av sidan, ändra eller skapa fler filter.

### <a name="on-which-page-types-can-i-use-list-views"></a>På vilka sidtyper kan jag använda listvyer?
Vyer är bara tillgängliga för list- och kalkylbladssidor.

### <a name="are-views-also-available-on-other-form-factors"></a>Finns det även vyer för andra formulärfaktorer?
Ja. Alla vyer som du sparar i din webbläsare eller på en stationär dator kommer också att vara tillgängliga på din surfplatta eller smartphone. Du kan inte ändra eller anpassa vyer på mobila enheter.

### <a name="are-my-personal-views-always-accessible"></a>Är mina personliga vyer alltid tillgängliga?
Samma vyer är tillgängliga på en listsida om du öppnar den från navigeringsmenyn, via fönstret **berätta för mig** eller via en URL-länk till listsidan. Vyer är inte tillgängliga i listdelar, uppslag eller när en listsida visas som en dialog.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hur återställer jag de ursprungliga filtren i en vy när jag har ändrat dem?
Längst ned i filterrutan väljer du åtgärden **återställ filter** för att ta bort filterändringar som du har gjort i vyn och återgår till de ursprungliga filtrerade fälten och filtervillkoren.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Vad är skillnaden mellan att dölja och ta bort vyer?
Om du tar bort en vy tas vyn bort permanent. Om du döljer en vy kan du tillfälligt dölja den i filterrutan, men du kan dölja den igen senare genom att välja åtgärden **Visa**.

### <a name="how-can-i-share-my-views-with-others"></a>Hur gör jag för att dela mina vyer med andra?
[!INCLUDE[d365fin](includes/d365fin_md.md)] ger inget sätt att dela den exakta listvyn, men du kan dela med dig av de aktuella filtren så att andra användare kan se en liknande lista med poster. Kopiera bara URL-adressentill skrivbordet och dela den med dina kollegor. Det går inte att garantera att delningsfilter ger mottagaren en identisk uppsättning filter som du ser i webbläsaren.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Kan jag söka efter vyer i fönstret Berätta för mig?
Nr Fönstret **Berätta för mig** visar endast sökresultat för sidan, men det är bara ett steg borta från att komma till din favoritvy när du navigerar till sidan.

### <a name="what-is-shared-layout"></a>Vad är delad layout?
Alla vyer på en listsida delar en gemensam kolumnlayout som inkluderar vilka kolumner som ska visas, deras inställningar för sekvens, bredd, låst ruta och snabbinmatning. Om du anpassar vilken av kolumnlayouten som visas, påverkas även andra vyer som delar samma layout på listsidan.

Vissa systemvyer kan ha unika layouter för kolumnerna i listan. De kan t.ex. arrangera om kolumner så att endast de kolumner som är mest relevanta för den vyn visas. Du kan identifiera vilka vyer som har unika layouter genom att välja ikonen ![Visa fler alternativ](media/show-more-options-icon.png "Visa fler alternativ") och observera att kryssrutan **delad layout** inte är markerad. Som användare kan du anpassa kolumnlayouten för en vy med unik layout utan att påverka andra vyer på listsidan. Endast utvecklare kan definiera en unik kolumnlayout för en vy som ursprungligen har en delad layout.

### <a name="what-does-the-show-system-filters-link-do"></a>Vad gör länken Visa systemfilter?
På vissa listsidor visas filterrutan **Visa systemfilter** längst ned i filterrutan när sidan innehåller filter som anges av systemet. Dessa speciella filter används vanligtvis för att visa poster som baseras på den aktuella kontexten, till exempel när en lista med order ska filtreras för en specifik kund.

Systemfilter anges av utvecklare som använder filtergrupp 0. Teknisk information om systemfilter finns i [Filtergruppmetod](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### <a name="i-see-multiple-views-on-my-page-but-i-did-not-create-them-where-did-they-come-from"></a>Det finns flera vyer på sidan, men jag skapade dem inte. Varifrån kom de?
De vyer som visas i en lista är en kombination av dina personliga vyer tillsammans med systemvyer. Systemvyer kan komma från affärsprogrammet, från tillägg eller kan vara rollspecifika om listan har anpassats för din roll.

### <a name="why-do-some-views-provide-fewer-options"></a>Varför ger vissa vyer färre alternativ?
Vissa vyer ger bara möjlighet att spara en kopia av vyn medan andra inte tillåter att ändringar sparas i vyn. Hur vyn skapades avgör vilka alternativ som är tillgängliga för vyn. Vyer kan skapas på flera sätt:
- Personliga vyer som du har sparat
- Systemvyer som är en standarddel av affärsprogrammet, eller läggs till via tillägg eller rollspecifika vyer. Till skillnad från personliga vyer går det inte att spara tillbaka ändringar av filter till den systemvisningen.
- Äldre systemvyer som utgör en standarddel av affärsprogrammet men som har skapats med äldre versioner av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessa vyer ger betydligt färre alternativ. Du kan bara spara dem som en ny vy och inte heller dölja eller ändra ordningen på dem. Observera att äldre systemvyer kommer att avbrytas vid kommande uppdatering av [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hur konverterar jag äldre systemvyer?
Äldre systemvyer är listvyer som har skapats av utvecklare i äldre versioner av [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att placera dem på sidan rollcenter. Dessa vyer visas nu direkt på list sidan men ger en försämrad upplevelse och betydligt färre alternativ. Du kan konvertera en äldre systemvy till en personlig vy som är helt anpassningsbar, genom att spara den äldre vyn som en ny vy. På samma sätt kan administratörer välja att konvertera rollspecifika äldre systemvyer genom att anpassa användar rollen och spara den äldre vyn som en ny rollbaserad vy.

Observera att äldre systemvyer kommer att avbrytas vid kommande uppdatering av [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Andra i min organisation behöver liknande listvyer som standard. Vad kan jag göra?
Det går snabbt och effektivt att arbeta med personliga vyer, men [!INCLUDE[d365fin](includes/d365fin_md.md)] det finns ytterligare verktyg för att definiera listvyer som behövs för specifika användarroller eller för alla användare i organisationen.
 - Utvecklare kan anpassa miljön och skapa listvyer i tillägg för alla användare i organisationen.
 - Icke-kodare som administratörer eller avdelningschefer kan skapa rollspecifika listvyer när de anpassar en roll från sidan **Profiler (roller)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Du arbetar med flera språk: Hur gör jag för att översätta vyns namn?
När du sparar en ny vy eller byter namn på en befintlig vy måste du ange ett igenkännligt och meningsfullt namn för vyn. Namnet sparas på det aktuella språket och visas också när du eller andra användare arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)] på olika språk. Om du vill tillhandahålla översatta visningsnamn måste du växla språk med sidan **Mina inställningar** och sedan byta namn på vyn, där det översatta namnet används på det nya språket.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Fungerar vyer med uttryck på alla språk?
Uttryck som bara använder symboler, t.ex. "**|**" eller **..** betraktas som säkra för användare att komma åt på alla språk. Alla vyer med uttryck som innehåller bokstäver, nyckelord eller filter-token fungerar bara för det språk de har skapats i.


### <a name="see-also"></a>Se även  
[Spara och anpassa listvyer](ui-views.md)  
[Söka efter Funktioner och information](ui-search.md)    
[Sortera, söka och filtrera](ui-enter-criteria-filters.md)  

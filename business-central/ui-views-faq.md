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
ms.openlocfilehash: f39e20a9b4dae7e84c491d6d28308133f4691c05
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024520"
---
# <a name="list-views-faq"></a>Vanliga frågor om listvyer
I den här artikeln besvaras frågor som våra erfarna användare ofta ställer om att arbeta med listvyer och spara filter.  

### <a name="how-do-views-handle-expressions"></a>Hur hanterar vyer uttryck?

När du sparar en vy som innehåller filter med uttryck (t.ex. datumintervall, operatorer, nyckelord eller filterspecifikationer) sparas endast uttrycket &mdash; inte resultatvärdena. Om du till exempel sparar en vy som filtrerar efter fältet **Skapat datum** med uttrycket `-1W..today` kommer detta alltid att leda till att poster relaterade till aktuellt datum hittas, även när vyn öppnas först nästa månad.

### <a name="where-are-list-views-saved"></a>Var sparas listvyer?

På samma sätt som du döljer ett fält eller sorterar om navigeringsmenyn är listvyn en del av användaranpassningen och lagras i databasen. Om du avmarkerar all anpassning i en lista kommer dina personliga vyer och ytterligare anpassningar också att tas bort permanent , till exempel omordning av vyer. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Varför har jag inte någon Spara-ikon?

Det finns ett flertal anledningar till varför du kanske inte ser ikonen Spara och alternativmenyn bredvid vyerna i filterrutan.

En orsak kan vara att anpassningar inte är aktiverade för din användarroll. I det här fallet har du fortfarande tillgång till systemvyer som utgör en standarddel av sidorna. Du kan ändra dessa vyer, t. ex. ändra eller lägga till filter. Du kan bara spara ändringarna. En annan orsak kan vara att sidan du tittar på är av sidtypen *kalkylblad* &mdash; ingen lista.

### <a name="on-which-page-types-can-i-use-list-views"></a>På vilka sidtyper kan jag använda listvyer?

Vyer är bara tillgängliga på listsidor.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Hur vet jag om jag befinner mig på en listsida?

Använd sidinspektion. Om du vill öppna sidinspektionen trycker du på Ctrl + Alt + F1. I fältet **Sida** söker du sedan efter ordet **Lista** i parentesen i slutet.

### <a name="are-views-also-available-on-other-form-factors"></a>Finns det även vyer för andra formulärfaktorer?

Ja. Alla vyer som du sparar i din webbläsare eller på en stationär dator kommer också att vara tillgängliga på din surfplatta eller smartphone. Du kan inte ändra eller anpassa vyer på mobila enheter.

### <a name="are-my-personal-views-always-accessible"></a>Är mina personliga vyer alltid tillgängliga?

Dina vyer är tillgängliga på en listsida oavsett om du öppnar den från navigeringsmenyn, via fönstret **Berätta** eller via en URL-länk. Vyer är inte tillgängliga i listdelar, sökningar eller när en listsida visas som en dialog.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hur återställer jag de ursprungliga filtren i en vy när jag har ändrat dem?

Längst ned i filterrutan väljer du åtgärden **återställ filter** för att ta bort filterändringar som du har gjort i vyn och återgår till de ursprungliga filtrerade fälten och filtervillkoren.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Vad är skillnaden mellan att dölja och ta bort vyer?

Om du tar bort en vy tas vyn bort permanent. Om du döljer en vy kan du tillfälligt dölja den i filterrutan, men du kan dölja den igen senare genom att välja åtgärden **Visa**.

### <a name="how-can-i-share-my-views-with-others"></a>Hur gör jag för att dela mina vyer med andra?

[!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller inget sätt att dela den exakta listvyn. Du kan emellertid dela med dig av de aktuella filtren så att andra användare kan se en liknande lista över poster. Kopiera helt enkelt URL-adressen till din stationära webbläsare och dela den med dina kollegor. Det går inte att garantera att delade filter ger mottagaren en identisk uppsättning filter som du ser i webbläsaren.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Kan jag söka efter vyer i fönstret Berätta?

Nr Fönstret **Berätta** visar endast sökresultat för sidan, men du är bara ett steg borta från att nå din favoritvy när du navigerar till sidan.

### <a name="what-is-shared-layout"></a>Vad är delad layout?

Alla vyer på en listsida delar en gemensam kolumnlayout. Layouten innehåller de kolumner som visas, dessas inställningar för sekvens, bredd, låst ruta och snabbinmatning. Om du anpassar en kolumnlayout påverkas även andra vyer som delar samma layout på listsidan.

Vissa systemvyer kan ha unika layouter för kolumnerna i listan. De kan t.ex. arrangera om kolumner så att endast de kolumner som är mest relevanta för den vyn visas. Du kan identifiera vilka vyer som har unik layout genom att välja ikonen ![Visa fler alternativ](media/show-more-options-icon.png "Visa fler alternativ") och observera att kryssrutan **Delad layout** inte är markerad. Som användare kan du anpassa kolumnlayouten för en vy med unik layout utan att påverka andra vyer på listsidan. Endast utvecklare kan definiera en unik kolumnlayout för en vy som ursprungligen har en delad layout.

### <a name="what-does-the-show-system-filters-link-do"></a>Vad gör länken Visa systemfilter?

På vissa listsidor visar filterrutan **Visa systemfilter** längst ned, särskilt när sidan innehåller filter som anges av systemet. Dessa speciella filter används vanligtvis för att visa poster som baseras på det aktuella sammanhanget. Ett exempel på detta är när en orderlista måste filtreras för en specifik kund.

Systemfilter anges av app-utvecklare med hjälp av filtergrupp 0. Mer information om systemfilter finns i [Filtergruppmetod](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Det finns flera vyer på min sida, men jag har inte skapat dem. Varifrån kom de?

De vyer som visas i en lista är en kombination av dina personliga vyer tillsammans med systemvyer. Systemvyer kan komma från affärsprogrammet, från tillägg eller kan vara rollspecifika om listan har anpassats för din roll.

### <a name="why-do-some-views-provide-fewer-options"></a>Varför ger vissa vyer färre alternativ?

Vissa vyer ger bara möjlighet att spara en kopia av vyn, medan andra inte tillåter att ändringar sparas i vyn. Hur vyn skapades avgör vilka alternativ som är tillgängliga för vyn. Vyer kan skapas på flera sätt:

- Personliga vyer som du har sparat
- Systemvyer som är en standarddel av affärsprogrammet, eller läggs till via tillägg eller rollspecifika vyer. Till skillnad från personliga vyer kan du inte spara tillbaka ändringar av filter till den systemvyn.
- Äldre systemvyer som utgör en standarddel av affärsprogrammet men som har skapats med äldre versioner av [!INCLUDE[prod_short](includes/prod_short.md)]. Dessa vyer ger färre alternativ. Du kan bara spara dem som en ny vy – du kan inte dölja dem eller ändra ordningen på dem. Stödet för äldre systemvyer kommer att upphöra i en kommande uppdatering av [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hur konverterar jag äldre systemvyer?

Äldre systemvyer är listvyer som har skapats av utvecklare i äldre versioner av [!INCLUDE[prod_short](includes/prod_short.md)] genom att placera dem på sidan rollcenter. Dessa vyer visas nu direkt på listsidan, men ger en försämrad upplevelse och färre alternativ. Du kan konvertera en äldre systemvy till en personlig vy som är helt anpassningsbar, genom att spara den äldre vyn som en ny vy. På samma sätt kan administratörer välja att konvertera rollspecifika äldre systemvyer genom att anpassa användar rollen och spara den äldre vyn som en ny rollbaserad vy.

Stödet för äldre systemvyer kommer att upphöra i en kommande uppdatering av [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Andra i min organisation behöver liknande listvyer som standard. Vad kan jag göra?

Det går snabbt och effektivt att arbeta med personliga vyer, men [!INCLUDE[prod_short](includes/prod_short.md)] ger även andra verktyg för att definiera de listvyer som behövs för specifika användarroller eller för alla användare i organisationen.
 - Utvecklare kan anpassa miljön och skapa listvyer i tillägg för alla användare i organisationen.
 - Icke-kodare som administratörer eller avdelningschefer kan skapa rollspecifika listvyer när de anpassar en roll från sidan **Profiler (roller)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Du arbetar med flera språk: Hur gör jag för att översätta vyns namn?

När du sparar en ny vy eller byter namn på en befintlig vy måste du ange ett igenkännligt och meningsfullt namn för vyn. Namnet sparas på det aktuella språket och visas också när du eller andra användare arbetar med [!INCLUDE[prod_short](includes/prod_short.md)] på olika språk. Om du vill översatta visningsnamn byter du språk med hjälp av sidan **Mina inställningar**. Byt sedan namn på vyn så att det översatta namnet lagras på det nya språket.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Fungerar vyer med uttryck på alla språk?

Uttryck som bara använder symboler, t.ex. `|` eller `..` betraktas som säkra för användare att komma åt på alla språk. Alla vyer med uttryck som innehåller bokstäver, nyckelord eller filter-token fungerar bara för det språk de har skapats på.

### <a name="see-also"></a>Se även

[Spara och anpassa listvyer](ui-views.md)  
[Söka efter Funktioner och information](ui-search.md)  
[Sortera, söka och filtrera](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Anpassa sidor | Microsoft Docs
description: Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 34c09b4acdad057bd5accd388335439e555dc733
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953353"
---
# <a name="personalize-your-workspace"></a>Anpassa din arbetsyta
Du kan anpassa arbetsytan för att passa ditt arbete och dina inställningar genom att ändra sidor så att de endast visar den information som du behöver när du behöver den. De anpassningar som du gör kommer bara att påverka bara vad som visas, inte vad andra användare ser.

Du kan anpassa alla typer av sidor, inklusive sidan rollcenter. Mer information om rollcenter finns i [rollcenter.](ui-change-basic-settings.md#role-center)

Du kan göra olika ändringar, som att flytta och dölja fält, kolumner och åtgärder och hela delar och lägga till nya fält och mer beroende på vilken typ av sida och den innehåller. De flesta typer av anpassning måste göras med att först aktivera banderollen **Anpassa**, men mycket enkla ändringar, t.ex. kolumnbredden kan utföras direkt på vilken lista som helst.

> [!NOTE]
> Administratörer kan utföra samma layoutändringar när användare kan anpassa arbetsytan för en profil som tilldelas flera användare. Mer information finns i [Anpassa sidor för roller](ui-personalization-manage.md).<br /><br />
Administratörer kan också åsidosätta eller inaktivera användarnas anpassning och de kan definiera vilka funktioner som till och med är tillgängliga för användare att se i alla eller specifika företag. Mer information finns i [Anpassa Business Central](ui-customizing-overview.md).

## <a name="to-change-the-width-of-a-column"></a>För att ändra bredden på en kolumn
Du kan enkelt ändra storlek på kolumnerna i alla listor genom att dra gränsen mellan två kolumner till vänster eller höger.
1. Välj och dra gränsen mellan två kolumner i rubriken på en lista.
2. Du kan också dubbelklicka på kanten mellan två kolumner för att anpassa kolumnens bredd automatiskt. Då anges bredden till optimal storlek för läsbarhet.

Precis som för andra anpassningar lagras de ändringar du gör av kolumnbredden på ditt konto och du ser inte vilken enhet du loggar in på.

## <a name="to-personalize-a-page-through-the-personalizing-banner"></a>Anpassa en sida via banderollen **Anpassa**
1. Öppna sidan du vill anpassa.
2. I det övre högra hörnet väljer du ikonen ![Inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan åtgärden **Anpassa**.

    Banderollen **Anpassa** visas längst upp och anger därmed att du kan börja göra ändringar.

    > [!NOTE]
    > Använd Ctrl + klicka på en instruktion om den markeras av pilspetsen om du vill navigera under anpassningen.

    Om du ser ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås") eller ![Anpassning spärrad](media/personalization-blocked-icon.png "Anpassning spärrad") å¨banderollen kan du inte anpassa sidan. Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).

3. För att lägga till ett fält, välj åtgärden **+ Fält**.
4. I fönstret **Lägg till fält till en sida** drar och släpper du ett fält i önskad position på sidan.
5. Om du vill ändra ett element i användargränssnittet pekar du på elementet, t.ex. en åtgärd, ett fält eller en del. Elementet markeras omedelbart med en pilspets eller en kantlinje.
6. Välj elementet och välj sedan antingen **Flytta**, **Ta bort**, **Dölj**, **Visa**, **Visa under "Visa mer"**, **Visa vid komprimerad**, **Visa alltid**, **Ställ in/rensa låst ruta** eller **Inkludera/exkludera från snabbinmatning**, beroende på typ och tillstånd för elementet i användargränssnittet. Mer information finns i [Vad du kan anpassa](#What).
7. När du är klar med att ändra layouten på en eller flera sidor, välj knappen **Klar** på banderollen **Anpassa**.

## <a name="What"></a>Detta kan du anpassa

|Vad vill du göra|Hur du gör det.|Anmärkningar|
|----|------------|-------|
|Flytta någonting, precis som fält, kolumn i listan, panel, åtgärd eller del|Peka var som helst på vad du vill flytta och dra den till dess nya position. Positionen anges med antingen en tjock vågrät eller lodrät linje.<br /><br />Ikonen ![Kan inte flytta hit](media/personalization-cannot-move-here.png "Anpassningsläge - konen kan inte flytta hit") anger att du inte kan flytta elementet till vald position.|Delar är underavdelningar eller områden på en sida som innehåller flera fält, en annan sida, ett diagram eller paneler.<br /><br />Visa [Anpassa åtgärder](ui-personalization-user.md#Actions) för mer information om vanpassningsåtgärder. |
|Göm någonting, precis som fält, kolumn i listan, panel, åtgärd eller del|Välj pilen och välj <b>Dölj</b>.|Elementet är nedtonat när du arbetar i anpassa läge. I fältet du döljer visas också i rubriken på snabbfliken när snabbfliken komprimeras, visas fältet inte längre.|
|Visa dolda åtgärder och fält.|För ett nedtonat (dolt) element väljer du pilspets och väljer sedan <b>Visa</b>|Det dolda elementet visas igen.|
|Lägga till ett fält eller kolumn|I banderollen <b>anpassa</b>, välj åtgärd <b>+ fält</b>.<br /></br>Rutan <b>lägga till fält på sidan</b> öppnas till höger. Den visar de fält som du kan lägga till på sidan.<br /><br />Om du vill lägga till ett fält, drar du det från fönstret till den position där du vill ha den. Positionen anges med antingen en tjock vågrät eller lodrät linje.|Varje sida innehåller en fördefinierad uppsättning fält som kan visas. Använd den här proceduren för att lägga till fält eller kolumner som inte har visats tidigare eller för att visa fält som du har dolt.|
|Visa ett fält i rubriken av en artikelrad när snabbfliken komprimeras.|Välj pilen och välj <b>visa när den är komprimerad</b>. <br /> <br />Om du inte ser detta alternativ har du redan angett det. Då väljer du att stoppa visa fältet på snabbflikens rubrik och väljer <b>visa alltid</b>.|*Snabbflik* är den term som används för en uppsättning fält som visas under den vanliga rubriken. Använd alternativet <b>visa minimerad</b> om du vill visa de viktigaste fälten. Om du väljer ett fält i rubriken på snabbfliken och fokusera på det markerade fältet.<br /><br />Det här alternativet gäller endast om det finns mer än en snabbflik. Om det endast finns en snabbflik kan den inte komprimeras så alternativet <b>visa minimerad</b> är inte tillgängligt.|
|Gör att ett fält endast visas om du väljer **visa fler**.|Välj pilen och välj <b>visa under "Visa fler"</b>. <br /> <br />Om du inte ser alternativet <b>Visa under ”Visa fler”</b> har den redan angetts. I det här fallet, för att ett fält alltid ska visas, inte bara när du markerar **visa fler** väljer du <b>visa alltid</b>.||
|Ändra låsning i en lista till en annan kolumn |Välj pilen i kolumnen som du vill ska vara den sista kolumnen på låsningen och välj <b>Ange låsning</b>.<br /><br/>Om du vill ange låsningen tillbaka till den ursprungliga angivna positionen, välj pilen för den aktuella kolumnen i låsningen och välj <b>ta bort låsning</b>. Obs! Du kan inte ta bort denna låsta ruta.|Låst ruta anger vilka kolumner som visas till vänster, även när du bläddrar horisontellt.|  
|Hoppa över ett fält när du trycker på Retur.|Välj pilen bredvid fältet eller kolumnrubriken i en lista och välj **utesluta från snabbinmatning**. <br /><br /> Om du inte ser detta alternativ anges redan fältet till att hoppas över. I det här fallet väljer du att hoppa över fältet **Inkludera i snabbinmatning**. |Se [Påskynda datainmatning med snabbinmatning](ui-enter-data.md#QuickEntry)|
|Ordna om och ta bort vyer som representerar filtrerade listor.|Välj pilspetsen bredvid en vy och välj sedan **flytta**, **ta bort**, eller **dölj**.|Se [Spara och anpassa listvyer](ui-views.md)|

## <a name="Actions"></a>Anpassa åtgärder

Anpassning låter dig bestämma vilka åtgärder som ska visas i åtgärdsfältet och rollcenter och var de ska visas. Du kan visa, dölja eller flytta enskilda åtgärder eller åtgärdsgrupper. Anpassa åtgärdsfältet utförs ungefär på samma sätt som med andra element i användargränssnittet. Vad du kan göra med en åtgärd eller grupp beror emellertid på var den åtgärden eller gruppen finns. Det bästa sättet att ta reda på detta är att arbetar i anpassat läge och låta pilarna guida dig.

Det finns ett par termer som du bör känna till för att bättre förstå åtgärdsanpassning: *åtgärdsgrupp* och *prioriterad kategori*.  

En *åtgärdsgrupp* är ett element som kan expanderas för att visa andra åtgärder eller grupper. Till exempel på sidan **försäljningsorder** är åtgärden **Funktioner** som visas när du väljer åtgärden **Åtgärder** en åtgärdsgrupp.

En *prioriterad kategori* är en grupp före den lodräta linjen `|` i åtgärdsfältet. Kategorierna omfattar vanligtvis de mest använda åtgärderna så att du snabbt kan hitta dem. På sidan **Försäljningsorder** kan **Order**, **Släpp** och  **Bokför** prioriterade kategorier.

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>Om du vill ta bort, dölja och visa åtgärder och åtgärdsgrupper
När du vill visa eller dölja en åtgärd definierar alternativen under pilspetsen vad som kan göras beroende på åtgärdens tillstånd.
1. Välj pilspets för en åtgärd eller åtgärdsgrupp.
2. Välj något av följande alternativ:

|Alternativ|Vad den gör|
|------|------------
|**Ta bort**|Det här alternativet visas om den valda åtgärden visas någon annanstans i åtgärdsfältet. Om du väljer det här alternativet tar du bort åtgärden från den valda platsen så att den inte längre visas. Åtgärden eller åtgärdsgruppen sparas på andra platser. |
|**Dölj**|Det här alternativet visas om åtgärden eller grupp inte finns någon annanstans i åtgärdsfältet. Liksom **ta bort**, om du väljer det här alternativet kommer åtgärden eller åtgärdsgruppen att försvinna från åtgärdsfältet. Men i anpassningsläget visas åtgärd eller åtgärdsgrupp fortfarande på den aktuella positionen förutom att det verkar dämpat.|
|**Visa**|Det här alternativet visas om åtgärden eller åtgärdsgruppen är tidigare dolda (är nedtonade). Om du väljer detta alternativet kommer åtgärden eller åtgärdsgruppen att visas på åtgärdsfältet.|

### <a name="to-move-actions-and-action-groups"></a>Flytta åtgärder och åtgärdsgrupper
Där du kan släppa åtgärder eller åtgärdsgrupper indikeras av en horisontell linje mellan två åtgärder eller en gräns runt en åtgärdsgrupp. Följande begränsningar förekommer:

    - Du kan flytta enskilda åtgärder i de prioriterade kategorierna, men du kan inte ändra ordningen på åtgärderna i kategorin.
    - Du kan inte flytta en grupp till en kategori som är prioriterad.

1. Om du vill flytta en åtgärd eller en åtgärdsgrupp, dra och släpp den till önskad position, precis som med fält och kolumner.
2. Om du vill flytta en åtgärd eller åtgärdsgrupp till en åtgärdsgrupp som är tom, dra åtgärden eller åtgärdsgruppen till den nya gruppen och släpp den i rutan **släpp åtgärd här**.

## <a name="to-clear-personalization"></a>Rensa anpassning
Vid något tillfälle kanske du vill ångra några eller alla anpassningsändringar som du har gjort på sidan.

1. På banderollen **anpassning**, välj åtgärden **rensa anpassning**.
2. Välj något av följande alternativ: Tänk på att ta bort anpassningar som inte går att ångra.

|Alternativ|Vad den gör|
|------|------------
|**Endast åtgärder**|Rensar alla personanpassningsändringar som du har gjort i åtgärdsfältet på den här sidan.|
|**Endast fält, kolumner och delar**|Rensar alla personanpassningsändringar som du har gjort på sidan förutom de på åtgärdsfältet. Här ingår ändringar av fält, kolumner, delar och paneler. |
|**Alla**|Rensar alla personanpassningsändringar som du har gjort så att sidan ser ut som den gjorde från början. Här ingår ändringar av åtgärdsfält, fält, kolumner, delar och paneler.|

## <a name="additional-points-of-interest"></a>Ytterligare punkter av intresse
Här följer några tips som hjälper dig att bättre förstå anpassning.

- När du ändrar en kortsida som du öppnar från en lista påverkar ändringarna alla poster som du öppnar från listan. Anta till exempel att du öppnar en specifik kund från listsidan kunder och sedan anpassar sidan genom att lägga till ett fält. När du öppnar andra kunder från listan visas också det fält som du har lagt till.
- Ändringarna börjar gälla i alla dina rollcenter. Till exempel om du gör en ändring i kundlistan när rollcentret har angetts till Chef visas dessutom ändringen ipå sidan **Kunder** när rollcentret anges till Försäljningsorderhandläggare.
- Ändringar av en sida i rutan börjar gälla på sidan var den än visas.  
- Du kan bara lägga till fält och kolumner från en fördefinierad lista som baseras på sidan. Du kan inte skapa nya.

## <a name="see-related-training-at-microsoft-learnlearnmodulespersonalize-ui-dynamics-365-business-centralindex"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Anpassa sidor för profiler](ui-personalization-manage.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

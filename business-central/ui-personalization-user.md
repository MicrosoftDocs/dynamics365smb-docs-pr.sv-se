---
title: Anpassa sidor (innehåller video)
description: Lär dig mer om att anpassa användargränssnittet och din arbetsyta så att det passar ditt sätt att arbeta och personliga inställningar i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 10/11/2022
ms.author: bholtorf
---
# <a name="personalize-your-workspace"></a>Anpassa din arbetsyta

Du kan anpassa din arbetsyta efter ditt arbete och dina preferenser. Ändra sidor så att de endast visar information som du behöver, där du behöver den. Anpassningen påverkar endast din arbetsyta. Det påverkar inte hur andra fungerar.

Du kan anpassa alla typer av sidor, inklusive sidan rollcenter. Om du vill veta mer om rollcenter går du till [rollcenter](ui-change-basic-settings.md#role-center).  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Du kan göra olika ändringar, som att flytta och dölja fält, kolumner och åtgärder och hela delar samt lägga till nya fält. De flesta anpassningar kräver att banderollen **Anpassning** först aktiveras. Du kan göra enkla justeringar, t.ex. kolumnens bredd, direkt på valfri lista.

> [!NOTE]
> Administratörer kan utföra samma layoutändringar när användare kan anpassa arbetsytan för en profil som tilldelas flera användare. Om du vill veta mer om sidor för roller går du till [anpassa sidor för roller](ui-personalization-manage.md)<br /><br />
Administratörer kan också åsidosätta eller inaktivera användarnas anpassning och de kan definiera vilka funktioner som till och med är tillgängliga för användare att se i alla eller specifika företag. Mer information finns i [Anpassa Business Central](ui-customizing-overview.md).

## <a name="video"></a>Video

I följande video visas några av de sätt som du kan anpassa ditt rollcenter på.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column"></a>För att ändra bredden på en kolumn

Du kan lätt ändra storlek på kolumnerna i en lista. Det är bara att dra kantlinjen mellan kolumnerna i till vänster eller höger.  

1. Välj och dra gränsen mellan två kolumner i rubriken på en lista.
2. Du kan också dubbelklicka på kanten mellan två kolumner för att anpassa kolumnens bredd automatiskt. Då justeras bredden till optimal storlek för läsbarhet.

Precis som för andra anpassningar lagras de ändringar du gör av kolumnbredden på ditt konto och du ser inte vilken enhet du loggar in på.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>För at börja anpassa en sida via banderollen **Anpassa**

1. Öppna sidan du vill anpassa.
2. Längst upp till höger, välj ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan åtgärden **anpassa**.

    Banderollen **Anpassa** visas längst upp och anger därmed att du kan börja göra ändringar.

    > [!NOTE]
    > Använd Ctrl + klicka på en instruktion om den markeras av pilspetsen om du vill navigera under anpassningen.

    Om du ser ![Anpassa lås](media/personalization-lock-icon.png "Anpassa lås") eller ![Anpassning spärrad](media/personalization-blocked-icon.png "Anpassning spärrad") på banderollen kan du inte anpassa sidan. Mer information finns i [Anledningen till att anpassning är spärrad för en sida](ui-personalization-locked.md).

3. För att lägga till ett fält, välj åtgärden **+ Fält**.
4. I fönstret **Lägg till fält till en sida** drar och släpper du ett fält i önskad position på sidan.
5. Om du vill ändra ett element i användargränssnittet pekar du på elementet, t. ex. en åtgärd, ett fält eller en del. Elementet markeras omedelbart med en pilspets eller en kantlinje.
6. Välj elementet och välj sedan antingen **Flytta**, **Ta bort**, **Dölj**, **Visa**, **Visa under "Visa mer"**, **Visa vid komprimerad**, **Visa alltid**, **Ställ in/rensa låst ruta** eller **Inkludera/exkludera från snabbinmatning**, beroende på typ och tillstånd för elementet i användargränssnittet. Mer information finns i [Vad du kan anpassa](#What).
7. När du är klar med att ändra layouten på en eller flera sidor, välj knappen **Klar** på banderollen **Anpassa**.

## <a name="what-you-can-personalize"></a><a name="What"></a>Detta kan du anpassa

|Vad vill du göra|Hur du gör det.|Anmärkningar|
|----|------------|-------|
|Flytta någonting, precis som fält, kolumn i listan, panel, åtgärd eller del|Peka var som helst på vad du vill flytta och dra den till dess nya position. Positionen anges med antingen en tjock vågrät eller lodrät linje.<br /><br />Ikonen ![Kan inte flytta hit](media/personalization-cannot-move-here.png "Anpassningsläge – konen kan inte flytta hit") anger att du inte kan flytta elementet till vald position.|Delar är underavdelningar eller områden på en sida som innehåller flera fält, en annan sida, ett diagram eller paneler.<br /><br />Visa [Anpassa åtgärder](ui-personalization-user.md#Actions) för mer information om åtgärdsanpassning. |
|Göm någonting, precis som fält, kolumn i listan, panel, åtgärd eller del|Välj pilen och välj <b>Dölj</b>.|Elementet är nedtonat när du arbetar i anpassa läge. I fältet du döljer visas också i rubriken på snabbfliken när snabbfliken komprimeras, visas fältet inte längre.|
|Visa dolda åtgärder och delar.|För ett nedtonat (dolt) element väljer du pilspets och väljer sedan <b>Visa</b>|Det dolda elementet visas igen.|
|Lägga till ett fält eller kolumn|I banderollen <b>anpassa</b>, välj åtgärd <b>+ fält</b>.<br /></br>Rutan <b>lägga till fält på sidan</b> öppnas till höger. Den visar de fält som du kan lägga till på sidan.<br /><br />Om du vill lägga till ett fält, drar du det från fönstret till den position där du vill ha den. Positionen anges med antingen en tjock vågrät eller lodrät linje.|Varje sida innehåller en fördefinierad uppsättning fält som kan visas. Använd den här proceduren för att lägga till fält eller kolumner som inte har visats tidigare eller för att visa fält som du har dolt.|
|Visa ett fält i rubriken av en snabbflik när den komprimeras.|Välj pilen och välj <b>visa när den är komprimerad</b>. <br /> <br />Om du inte ser detta alternativ har du redan angett det. Då väljer du att stoppa visa fältet på snabbflikens rubrik och väljer <b>visa alltid</b>.|*Snabbflik* är den term som används för en uppsättning fält som visas under den vanliga rubriken. Använd alternativet <b>visa minimerad</b> om du vill visa de viktigaste fälten. Om du väljer ett fält i rubriken på snabbfliken och fokusera på det markerade fältet.<br /><br />Det här alternativet gäller endast om det finns mer än en snabbflik. Om det endast finns en snabbflik kan den inte komprimeras, så alternativet <b>Visa när komprimerad</b> är inte tillgängligt.|
|Gör att ett fält endast visas om du väljer **visa fler**.|Välj pilen och välj <b>visa under "Visa fler"</b>. <br /> <br />Om du inte ser alternativet <b>Visa under ”Visa fler”</b> har det redan angetts. I det här fallet, för att ett fält alltid ska visas, inte bara när du markerar **visa fler** väljer du <b>visa alltid</b>.||
|Ändra låsning i en lista till en annan kolumn |Välj pilen i kolumnen som du vill ska vara den sista kolumnen på låsningen och välj <b>Ange låsning</b>.<br /><br/>Om du vill ange låsningen tillbaka till den ursprungliga angivna positionen, välj pilen för den aktuella kolumnen i låsningen och välj <b>ta bort låsning</b>. Obs! Du kan inte ta bort denna låsta ruta.|Låst ruta anger vilka kolumner som visas till vänster, även när du bläddrar horisontellt.|  
|Hoppa över ett fält när du trycker på Retur.|Välj pilen bredvid fältet eller kolumnrubriken i en lista och välj **utesluta från snabbinmatning**. <br /><br /> Om du inte ser detta alternativ har fältet redan ställts in på att hoppas över. I det här fallet väljer du att hoppa över fältet **Inkludera i snabbinmatning**. |Se [Påskynda datainmatning med snabbinmatning](ui-enter-data.md#QuickEntry)|
|Ordna om och ta bort vyer som representerar filtrerade listor.|Välj pilspetsen bredvid en vy och välj sedan **flytta**, **ta bort**, eller **dölj**.|Se [Spara och anpassa listvyer](ui-views.md)|  
|Lägg till en ny åtgärd på en sida eller rapport i rollcentret.|Välj ikonen bokmärke på sida för rapportförfrågan, sida i rapporten eller berätta för mig-fönstret.|Se [Förse en sida eller rapport med ett bokmärke på ditt rollcenter](ui-bookmarks.md)|
|Starta alltid en lista som visad eller dold|Välj knappen **Expandera alla** eller **Komprimera alla** längst upp till vänster i listan. Alternativt väljer du åtgärden **Expandera alla** eller **Komprimera alla** i menyn för den första kolumnen. |Gäller för komprimerbara hierarkinivåer|

## <a name="personalizing-the-action-bar-and-menus"></a><a name="Actions"></a>Anpassa åtgärdsfältet och menyer

Anpassning låter dig bestämma vilka åtgärder som ska visas i navigerings- och åtgärdsfälten och i rollcenter, samt var de ska visas. Du kan visa, dölja eller flytta enskilda åtgärder eller åtgärdsgrupper.

I följande video visas hur du kan anpassa åtgärder på sidor och rollcenter.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Anpassning av navigerings- och åtgärdsfältet utförs ungefär på samma sätt som med andra element i användargränssnittet. Vad du kan göra med en åtgärd eller grupp beror emellertid på var den åtgärden eller gruppen finns. Det bästa sättet att ta reda på detta är att arbetar i anpassat läge och låta pilarna guida dig.

Det finns ett par termer som du bör känna till för att bättre förstå åtgärdsanpassning: *åtgärdsgrupp* och *prioriterad kategori*.  

En *åtgärdsgrupp* är ett element som kan expanderas för att visa andra åtgärder eller grupper. Till exempel på sidan **Försäljningsorder** är en åtgärdsgrupp åtgärden **Funktioner** som visas när du väljer åtgärden **Åtgärder**.

En *prioriterad kategori* är en grupp före den lodräta linjen `|` i åtgärdsfältet. Kategorierna omfattar vanligtvis de mest använda åtgärderna så att du snabbt kan hitta dem. På sidan **Försäljningsorder** kan **Order**, **Släpp** och  **Bokför** prioriterade kategorier.

> [!NOTE]  
> Om du vill rensa anpassningen markerar du pilspetsen runt delens designermeny och väljer **Rensa anpassning**.

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>Om du vill ta bort, dölja och visa åtgärder och åtgärdsgrupper

När du vill visa eller dölja en åtgärd definierar alternativen under pilspetsen vad som kan göras beroende på åtgärdens tillstånd. 

1. Välj pilspets för en åtgärd eller åtgärdsgrupp.
2. Välj något av följande alternativ:

|Alternativ|Vad den gör|
|------|------------
|**Ta bort**|Detta alternativ visas om den valda åtgärden visas någon annanstans i navigerings- eller åtgärdsfältet. Om du väljer det här alternativet tar du bort åtgärden från den valda platsen så att den inte längre visas. Åtgärden eller åtgärdsgruppen sparas på andra platser. |
|**Dölj**|Det här alternativet visas om åtgärden eller åtgärdsgruppen inte finns någon annanstans i navigerings- eller åtgärdsfältet. Liksom alternativet **Ta bort** får detta alternativ åtgärden eller åtgärdsgruppen att försvinna från navigerings- eller åtgärdsfältet. Men i anpassningsläget visas åtgärd eller åtgärdsgrupp fortfarande på den aktuella positionen förutom att det verkar dämpat.|
|**Visa**|Det här alternativet visas om åtgärden eller åtgärdsgruppen är tidigare dolda (är nedtonade). Om du väljer detta alternativ kommer åtgärden eller åtgärdsgruppen att visas på navigerings- eller åtgärdsfältet.|

### <a name="to-move-actions-and-action-groups"></a>Flytta åtgärder och åtgärdsgrupper

Där du kan släppa åtgärder eller åtgärdsgrupper indikeras av en horisontell linje mellan två åtgärder eller en gräns runt en åtgärdsgrupp. Följande begränsningar förekommer:

- Du kan flytta enskilda åtgärder i de prioriterade kategorierna, men du kan inte ändra ordningen på åtgärderna i kategorin.
- Du kan inte flytta en grupp till en kategori som är prioriterad.

1. Om du vill flytta en åtgärd eller en åtgärdsgrupp, dra och släpp den till önskad position, precis som med fält och kolumner.
2. Om du vill flytta en åtgärd eller åtgärdsgrupp till en åtgärdsgrupp som är tom, dra åtgärden eller åtgärdsgruppen till den nya gruppen och släpp den i rutan **släpp åtgärd här**.

## <a name="personalizing-parts"></a><a name="Parts"></a>Anpassa delar

Delar är områden på en sida som vanligtvis utgörs av flera fält, diagram eller annat innehåll. En del visar en färgad kantlinje när du fokuserar på delen. Startvyn för ett rollcenter har till exempel flera delar. På grund av deras väldefinierade gränser kan du anpassa hela delen samt dess innehåll.

- Om du vill flytta en del drar och släpper du den på önskad plats. En färgad linje indikerar giltiga positioner på skärmen. Faktaboxar kan t. ex. bara placeras bredvid andra faktaboxar i rutan Faktabox.
- Du kan dölja en del genom att välja alternativet **Dölj** under pilspetsen.
- När du börjar anpassa eller navigerar till en ny sida visas alla delar som för tillfället är dolda på sidan med särskiljande visuella effekter för att visa att de är dolda. Du kan visa en del genom att välja alternativet **Visa** under pilspetsen.

Du kan ta bort alla anpassningsändringar du har utfört i en enskild del genom att välja alternativet **Radera anpassning** under delens pilspets. När du rensar anpassningen för en viss del påverkar detta bara ändringar i innehållet i just den delen, inte delens placering eller synlighet på sidan.  

## <a name="to-clear-personalization"></a>Rensa anpassning

Vid något tillfälle kanske du vill ångra några eller alla anpassningsändringar som du har gjort på sidan.

1. På banderollen **anpassning**, välj åtgärden **rensa anpassning**.
2. Välj något av följande alternativ:  

> [!CAUTION]
> Det går inte att ångra rensade anpassningar.

|Alternativ|Vad den gör|
|------|------------
|**Endast navigeringsmeny**|Alla anpassningar som du har gjort i navigeringsmenyn som delas i rollcentret och andra sidor raderas. Sådana ändringar innefattar alla nya åtgärder som har lagts till som bokmärken och eventuella ändringar av länkar och grupper på menyn.|  
|**Endast åtgärder**|Rensar alla personanpassningsändringar som du någonsin har gjort i navigerings- eller åtgärdsfältet på sidan.|
|**Endast fält och kolumner**|Rensar alla anpassningsändringar som du någonsin har gjort på sidan förutom de i navigerings- eller åtgärdsfältet. Sådana ändringar inbegriper fält, kolumner, delar och paneler. |
|**Alla**|Rensar alla personanpassningsändringar som du har gjort så att sidan ser ut som den gjorde från början. Sådana ändringar inbegriper ändringar i navigerings- eller åtgärdsfält, fält, kolumner, delar och paneler.|

## <a name="other-points-of-interest"></a>Andra punkter av intresse

Här följer några tips som hjälper dig att bättre förstå anpassning.

- När du ändrar en kortsida som du öppnar från en lista påverkar ändringarna alla poster som du öppnar från listan. Anta till exempel att du öppnar en specifik kund från listsidan kunder och sedan anpassar sidan genom att lägga till ett fält. När du öppnar andra kunder från listan visas också det fält som du har lagt till.
- Ändringarna börjar gälla i alla dina rollcenter. Till exempel om du gör en ändring i kundlistan när rollcentret har angetts till Chef visas dessutom ändringen ipå sidan **Kunder** när rollcentret anges till Försäljningsorderhandläggare.
- Ändringar av en sida i rutan börjar gälla på sidan var den än visas.  
- Du kan bara lägga till fält och kolumner från en fördefinierad lista som baseras på sidan. Du kan inte skapa nya.
- **Power Automate** åtgärder i åtgärdsfältet
  - Du kan inte dölja eller flytta objektet **Automatisera** eller **Power Automate** underobjekt och dess åtgärder **Skapa ett flöde** och **Hantera flöden**.
  - Du kan flytta flöden som ingår i **Automatiserade** objektet, men du kan inte dölja dem med hjälp av anpassning. När du flyttar flödet skapas en kopia av flödet till målet. det går inte att ta bort det från det **Automatiserade**objektet.

   > [!TIP]
   > Som administratör kan du dölja **automatiserade** objekt från användare. Läs mer i [Ställa in Power Automate integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Anpassa sidor för profiler](ui-personalization-manage.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

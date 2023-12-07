---
title: Anpassa sidor för roller
description: Lär dig mer om att anpassa användargränssnittet för en profil (roll) så att alla användare som är tilldelade den rollen ser en anpassad arbetsyta.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# <a name="customize-pages-for-profiles"></a>Anpassa sidor för profiler

Business Central tillhandahåller både [anpassning](ui-personalization-user.md) för användare och anpassning för administratörer. Med anpassning kan användarna skräddarsy sin arbetsyta genom att justera sidlayouterna efter eget behov. Administratörer kan anpassa sidlayouter för en specifik profil, baserat på affärsroller eller avdelningar, så att alla tilldelade användare ser samma anpassade sida. Med anpassning kan användare visa, dölja och flytta fält och åtgärder på en sida, men anpassning ger extra funktioner. Med anpassning kan du till exempel visa fält som finns i sidans källtabell eller tilläggstabeller men som inte har definierats för sidobjektet &mdash; vilket inte är möjligt att anpassa.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> En typisk företagsanvändning är en roll. En profil har därför namnet *profil (roll)* i användargränssnittet.

Sid anpassningen startar från **profilsidan (rollerna)** och administratörens startpunkt används för att hantera användarprofiler på enskilda profilkort. Förutom att anpassa sidlayouten kan du styra olika inställningar för profiler på **profilsidan (roll)** för varje profil. Mer information finns i [Hantera profiler](admin-users-profiles-roles.md).

## <a name="prerequisites"></a>Förutsättningar

- Ditt Business Central-konto måste ha behörighetsgrupp **D365 Profilhant.** eller motsvarande behörigheter. 

   Behörighetsgruppen **D365 Profilhant.** innehåller körningsbehörigheten för systemobjektet **9026 lägg till fält i tabell**. Om du inte har den här behörigheten får du inte lägga till fält på sidan om de inte har definierats för sidobjektet. 

## <a name="customize-pages-for-a-profile"></a>Anpassa sidor för en profil

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Profiler (roller)** och väljer sedan relaterad länk.
2. Markera raden för den profil du vill anpassa sidor för och välj sedan åtgärden **Redigera**.
3. Välj åtgärden **anpassa sidor**.

    [!INCLUDE[prod_short](includes/prod_short.md)] öppnas på en ny flik i webbläsaren för den valda profilen med banderollen **anpassar** aktiverad. Banderollen **anpassar** ger användarna samma funktioner som banderollen **Anpassa personligt** som är tillgänglig för användare.

4. Anpassa sidor enligt de behov som gäller för den aktuella rollen eller avdelningen på samma sätt som en användare gör när du anpassar. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

    > [!NOTE]
    > Använd <kbd>Ctrl</kbd>+<kbd>klicka</kbd> på en instruktion om den markeras av pilspetsen om du vill navigera under anpassningen.

5. När du är klar med att ändra layouten på en eller flera sidor, välj knappen **Klar** på banderollen **Anpassa**.
6. Stäng fliken webbläsare.

Anpassningen av sidorna har nu registrerats för profilen.

## <a name="view-all-customized-pages-for-a-profile"></a>Visa alla anpassade sidor för en profil

Du kan få en översikt över vilka sidor som är anpassade för en profil, t.ex. för planering av vilka sidor du vill anpassa ytterligare eller ta bort.

- På sidan **Profil (roll)**, välj åtgärden **Hantera anpassade sidor**.

På sidan **Anpassade sidor** kan du ta bort anpassningar, och du kan felsöka genom att söka efter potentiella problem.  

## <a name="delete-all-customizations-for-a-profile"></a>Radera anpassningar för en profil

Du kan annullera alla anpassningar som du har gjort för en profil: Anpassningar som introduceras med ett tillägg och anpassningar som görs av en användare tas inte bort. Du kan ta bort alla anpassningar med en annan åtgärd. Mer information finns i [så här tar du bort alla anpassningar som görs av en användare](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Välj åtgärden **Profil (roll)** för en anpassad profil, välj åtgärden **Rensa anpassade sidor**.

Layouten på sidorna för profilen återställs till standardlayouten.  

## <a name="delete-customization-for-specific-pages-for-a-profile"></a>Ta bort anpassning av specifika sidor för en profil

Du kan ta bort individuella sidanpassningar som du har gjort för en profil. Anpassningar som introduceras med ett tillägg och anpassningar som görs av en användare tas inte bort. Du kan ta bort specifika sidanpassningar med en annan åtgärd. Mer information finns i [Så här tar du bort alla anpassningar för en viss sida](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. På sidan **Profil (roll)**, välj åtgärden **Hantera anpassade sidor**.
2. På sidan **Anpassade sidor**, välj en eller flera rader för sidanpassningar som du vill radera och välj sedan åtgärden **Radera**.

Layouten på de markerade sidorna justeras efter de ändringar som du har gjort.

## <a name="add-a-field"></a>Lägg till ett fält

Du lägger till fält på sidan från fönstret **Lägg till fält på sida**, som du öppnar genom att välja åtgärden **+ Fält** i anpassningsläget. Det är viktigt att förstå att fönstret **Lägg till fält i sidan** används för att visa fält som redan finns&mdash;antingen på sidan och dess källtabeller&mdash;men som för närvarande är dolda. Du kan inte skapa nya fält.

I fönstret **Lägg till fält på sida** visas alla fält som kan visas på sidan. Fälten är indelade i följande kategorier, beroende på den underliggande utformningen av själva sidan, källtabellen och tilläggen:

|Kategori|Description|
|-|-|
|Tabellfält som inte finns i sidobjekt|Innehåller fält som definieras i bastabellen eller tilläggstabellerna, men som inte definieras på sidan. Knappbeskrivningen för dessa fält innehåller etiketten **Definieras av tabellen**.<br><br>|
|Sidfält som är bundna till en tabell|Innehåller fält som definieras i bastabellen eller tabelltilläggen och som också definieras som antingen visade eller dolda på sidan. Knappbeskrivningen för dessa fält innehåller **Definieras av sidan**.|
|Sidfält som inte är bundna till en tabell| Fält som bara är definierade på sidan, inte i bastabellen eller tilläggstabellerna. Dessa fält används vanligtvis för variabel eller beräkning. Knappbeskrivningen för dessa fält innehåller **Definieras av sidan**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Använd filterknappen ovanför listan för att ändra vilken kategori av fält som visas i fönstret **Lägg till fält på sidan**.  

:::image type="content" source="media/customization-filter.svg" alt-text="Visar filterknappen i fönstret Lägg till ett fält i anpassningsläget.":::
 
### <a name="add-table-field-thats-not-on-the-page-object"></a>Lägg till tabellfält som inte finns på sidobjektet

Om du vill göra ett tabellfält tillgängligt på en sida för användare måste du först lägga till det på sidan. När du har lagt till fältet kan användarna välja att visa eller dölja fältet som de vill med hjälp av anpassning. Det finns några olika sätt att lägga till ett fält.

- Ett sätt är att dra den från fönster **Lägg till fält i sidan** till önskad position.
- Ett annat sätt är att markera fältet i rutan för att visa den rekommenderade platsen på sidan. Gå sedan till fältplatsen på sidorna, välj pilspetsen och välj sedan **Lägg till**. 

När fältet har lagts till växlar verktygstipset för fältet i fönstret **Lägg till fält** på sida till **Definieras av sidan**. Det tillagda fältet är låst från redigering och kan inte låsas upp.

## <a name="remove-a-field"></a>Ta bort ett fält

Om du har lagt till ett tabellfält som ursprungligen inte fanns i sidobjektet kan du ta bort det igen. Att ta bort ett fält är annorlunda än att dölja det. När du döljer ett fält kan användarna fortfarande visa det på sin arbetsyta genom anpassning. Men om du tar bort ett fält är fältet inte längre tillgängligt för användare att visa, eller dölja för den delen. Om fältet för närvarande visas på en användares arbetsyta försvinner det från användarens arbetsyta när du tar bort det. 

Om du vill ta bort ett fält väljer du pilspetsen på fältet på sidan och sedan på **Ta bort**. Om du inte hittar fältet markerar du det i fönstret **Lägg till fält på sidan** för att ange dess dolda plats. 

> [!IMPORTANT]
> När du tar bort ett fält tas inte data som lagras i fältet eller källtabeller bort. Det tar bara bort fältet från vyn. 

## <a name="lock-and-unlock-editing"></a>Låsa och låsa upp redigering

Med anpassning kan du låsa (tillåta redigering) eller låsa upp redigering (förhindra redigering) av de flesta fält på en sida. Om du vill låsa eller låsa upp redigeringen markerar du fältet på sidan, markerar pilspetsen och väljer sedan **Lås redigering** eller **Lås upp redigering**. Det är viktigt att komma ihåg några regler om låsning och upplåsning av fält:

- Fält som ursprungligen inte fanns på sidobjektet men som lades till på sidan genom anpassning är alltid låsta och kan inte låsas upp med anpassning.
- Fältets utformning kan också förhindra att det redigeras. Om AL-utvecklaren anger fältets [redigerbara egenskap](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) till `false` är den alltid låst och kan inte låsas upp.
- Det är viktigt att notera att låsredigeringsfunktionen är avsedd att hjälpa till med noggrannhet, konsekvens och tillförlitlighet för data. Det är inte avsett att skydda dataintegriteten.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## <a name="important-information-and-tips"></a>Viktig information och tips

- Alla tabellfält kanske inte är tillgängliga för anpassning från fönstret **Lägg till fält på sida**. Utvecklaren av en tabell kan välja att förhindra att ett fält visas i anpassningen genom att ange fältets [AllowInCustomization egenskap](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) till `false`.
- Du kan inte anpassa en sida som är i [analysläge](analysis-mode.md). Växeln **Analysera** är inaktiverad. Om du växlar till anpassningsläge medan sidan är i analysläge stängs analysläget automatiskt av. 
- Vissa sidor har flera sidfält som mappas till samma källtabell. I fönstret **Lägg till fält på sida** visas alla dessa sidfält oberoende av varandra. Du kan visa, dölja eller flytta dessa fält oberoende av varandra utan att påverka de övriga.
- Om en del eller grupp är dold kan du fortfarande identifiera dolda fält inuti delen eller gruppen, men du kan inte lägga till, flytta eller visa fält i delen eller gruppen förrän de har synliggjorts. 
## <a name="see-also"></a>Se även

[Anpassa arbetsytan](ui-personalization-user.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

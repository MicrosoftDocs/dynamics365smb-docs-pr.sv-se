---
title: Anpassa sidor | Microsoft Docs
description: Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: de7acb10c76acc05fc6e6a5c708a8d412e4d9b30
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632735"
---
# <a name="personalizing-your-workspace"></a>Anpassa din arbetsyta

Du kan *anpassa* arbetsytan för att passa ditt arbete och dina inställningar genom att ändra sidor så att de endast visar den information som du behöver när du behöver den. De anpassningar som du gör kommer bara att påverka bara vad som visas, inte vad andra användare ser.

Du kan göra olika saker, som att flytta och dölja fält, kolumner och åtgärder, flytta och dölja hela delar och mer beroende på vilken typ av sida och den innehåller.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Förutom vad användare kan anpassa kan administratörer och superanvändare åsidosätta användarnas anpassningar och definiera vilka funktioner som är tillgängliga i alla eller särskilda företag. Mer information finns i [Anpassa Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Så här anpassar du en sida

1. I det övre högra hörnet väljer du ikonen ![inställningar](media/ui-experience/settings_icon_small.png "ikonen inställningar för rollcenter") och sedan **anpassa**.

    Banderollen **Anpassa** visas längst upp och anger därmed att du kan börja göra ändringar.

    ![Anpassningsläget](media/ui_personalize_mode_small.png "Anpassningsläget")

2. Gå till sidan du vill anpassa.

    Om du ser ![anpassa lås](media/personalization-lock-icon.png "anpassa lås") eller ![anpassning spärrad](media/personalization-blocked-icon.png "anpassning spärrad") i banderollen kan du inte anpassa sidan. Mer information finns i [varför kan jag inte anpassa sidan](ui-personalization-locked.md).

3. Peka på ett område som du vill anpassa, t.ex. fält eller en kolumnrubrik i en lista. Allt som du kan anpassa markeras omedelbart med en pil eller en ram. Visa [nästa avsnitt](#What) för mer information om vad du kan göra.

4. Du kan fortsätta att göra ändringar på samma sida eller öppna en annan sida. Dina ändringar sparas automatiskt medan du gör dem. När du är klar väljer du i **anpassa** banderoll **Klar**.

## <a name="What"></a>Detta kan du anpassa

|Vad vill du göra|Hur du gör det.|Anmärkningar|
|----|------------|-------|
|Flytta någonting, precis som fält, kolumn i listan, panel, åtgärd eller del|Peka var som helst på vad du vill flytta och dra den till dess nya plats. Platsen anges med antingen en tjock vågrät eller lodrät linje.<br /><br />![Det går inte att flytta ikonen hit](media/personalization-cannot-move-here.png "anpassa läge - det går inte att flytta ikonen hit") anger att du inte kan flytta elementet till den angivna platsen.|Delar är underavdelningar eller områden på en sida som innehåller flera fält, en annan sida, ett diagram eller paneler.<br /><br />Visa [nästa avsnitt](ui-personalization-user.md#Actions) för mer information om vanpassningsåtgärder. |
|Dölj någonting, precis som fält, kolumn i listan, panel eller del|Markera pilen och välj <b>Dölj</b>.|I fältet du döljer visas också i rubriken på snabbfliken när snabbfliken komprimeras, visas fältet inte längre.|
|Lägga till ett fält eller kolumn|I banderollen <b>anpassa</b> välj <b>mer</b> och sedan <b>fält</b>.<br /></br>Rutan <b>lägga till fält på sidan</b> öppnas till höger. Den visar de fält som du kan lägga till på sidan.<br /><br />Om du vill lägga till ett fält, drar du det från fönstret till den plats där du vill ha den. Platsen anges med antingen en tjock vågrät eller lodrät linje.|Varje sida innehåller en fördefinierad uppsättning fält som kan visas. Använd den här proceduren för att lägga till fält eller kolumner som inte har visats tidigare eller för att visa fält som du har dolt.|
|Visa ett fält i rubriken av en artikelrad när snabbfliken komprimeras.|Markera pilen och välj <b>visa när den är komprimerad</b>. <br /> <br />Om du inte ser detta alternativ har du redan angett det. Då väljer du att stoppa visa fältet på snabbflikens rubrik och väljer <b>visa alltid</b>.|*Snabbflik* är den term som används för en uppsättning fält som visas under den vanliga rubriken. Använd alternativet <b>visa minimerad</b> om du vill visa de viktigaste fälten. Om du väljer ett fält i rubriken på snabbfliken och fokusera på det markerade fältet.<br /><br />Det här alternativet gäller endast om det finns mer än en snabbflik. Om det endast finns en snabbflik kan den inte komprimeras så alternativet <b>visa minimerad</b> är inte tillgängligt.|
|Gör att ett fält endast visas om du väljer **visa fler**.|Markera pilen och välj <b>visa under "Visa fler"</b>. <br /> <br />Om du inte ser alternativet <b>Visa under ”Visa fler”</b> har den redan angetts. I det här fallet, för att ett fält alltid ska visas, inte bara när du markerar **visa fler** väljer du <b>visa alltid</b>.||
|Ändra låsning i en lista till en annan kolumn |Markera pilen i kolumnen som du vill ska vara den sista kolumnen på låsningen och välj <b>Ange låsning</b>.<br /><br/>Om du vill ange låsningen tillbaka till den ursprungliga angivna platsen, markera pilen för den aktuella kolumnen i låsningen och välj <b>ta bort låsning</b>. Obs! Du kan inte ta bort denna låsta ruta.|Låst ruta anger vilka kolumner som visas till vänster, även när du bläddrar horisontellt.|  
|Ändra bredden på en kolumn|Dra kantlinjen mellan kolumnerna i huvudlistan. <br /><br />Du kan dubbelklicka på kanterna mellan kolumnrubrikerna för att passa in bredden, vilket ger en bekväm storlek för läsbarhet.||
|Hoppa över ett fält när du trycker på Retur.|Markera pilen bredvid fältet eller kolumnrubriken i en lista och välj **utesluta från snabbinmatning**. <br /><br /> Om du inte ser detta alternativ anges redan fältet till att hoppas över. I det här fallet väljer du att hoppa över fältet **Inkludera i snabbinmatning**. |Se [Påskynda datainmatning med snabbinmatning](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Anpassa åtgärder

Du kan anpassa åtgärdsfältet som finns längst upp på sidan som är markerade med det markerade området i bilden.

![Anpassa åtgärdsfältet](media/personalize-action-bar.png "Anpassa åtgärdsfältet")

Anpassning låter dig bestämma vilka åtgärder som ska visas i åtgärdsfältet och var de ska visas. Du kan visa, dölja eller flytta enskilda åtgärder eller åtgärdsgrupper. Anpassa åtgärdsfältet utförs ungefär på samma sätt som med andra delar av arbetsytan. Exakt vad du kan göra med en åtgärd eller grupp beror emellertid på var den åtgärden eller gruppen finns i åtgärdsfältet. Det bästa sättet att ta reda på detta är att bara testa saker och låta skärmen guida dig. I följande avsnitt beskrivs några av nyanserna för att anpassa Åtgärdsfältet.

### <a name="action-bar-overview"></a>Översikt av åtgärdsfältet

Det finns ett par termer som du bör känna till för att bättre förstå åtgärdsanpassning: *åtgärdsgrupp* och *prioriterad kategori*.  

En *åtgärdsgrupp* är objekt som kan expanderas för att visa andra åtgärder eller grupper. Till exempel i följande bild är **bokföra** är en åtgärdsgrupp.

En *prioriterad kategori* är en grupp mellan de två lodräta linjerna `|` i åtgärdsfältet. Kategorierna omfattar vanligtvis de mest använda åtgärderna så att du snabbt kan hitta dem. Till exempel i följande bild **version**, **bokföring**, **faktura** och **analysera** är prioriterade kategorier.

![Anpassa åtgärdsfältgrupp](media/personalize-action-bar-group-clip.png "Anpassa åtgärdsfältgrupp")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Om du vill ta bort, dölja och visa åtgärder och grupper

För att visa eller dölja och åtgärd eller åtgärdsgrupp, markerar du den och väljer sedan bland följande alternativ:

|Alternativ|Vad den gör|
|------|------------
|**Ta bort**|Det här alternativet visas om den valda åtgärden visas någon annanstans i åtgärdsfältet. Om du väljer det här alternativet tar du bort åtgärden från den valda platsen så att den inte längre visas. Åtgärden eller åtgärdsgruppen sparas på andra platser. |
|**Dölj**|Det här alternativet visas om åtgärden eller grupp inte finns någon annanstans i åtgärdsfältet. Liksom **ta bort**, om du väljer det här alternativet kommer åtgärden eller åtgärdsgruppen att försvinna från åtgärdsfältet. Men i anpassningsläget visas åtgärd eller åtgärdsgrupp fortfarande på den aktuella platsen förutom att det verkar dämpat.|
|**Visa**|Det här alternativet visas om åtgärden eller åtgärdsgruppen är tidigare dolda (är nedtonade). Om du väljer detta alternativet kommer åtgärden eller åtgärdsgruppen att visas på åtgärdsfältet.|

### <a name="to-move-actions-and-action-groups"></a>Flytta åtgärder och åtgärdsgrupper

Om du vill flytta en åtgärd eller en åtgärdsgrupp, dra och släpp den till önskad plats, precis som med fält och kolumner.

Där du kan släppa åtgärder eller åtgärdsgrupper indikeras av en horisontell linje mellan åtgärder eller gränser runt en åtgärdsgrupp.

- Du kan flytta enskilda åtgärder i de prioriterade kategorierna, men du kan inte ändra ordningen på åtgärderna i kategorin.
- Du kan inte flytta en grupp till en kategori som är prioriterad.
- Om du vill flytta en åtgärd eller åtgärdsgrupp till en åtgärdsgrupp som är tom, dra åtgärden eller åtgärdsgruppen till den nya gruppen och släpp den i rutan **släpp åtgärd här**.

## <a name="additional-points-of-interest"></a>Ytterligare punkter av intresse

Här följer några tips som hjälper dig att bättre förstå anpassning.

- När du ändrar en kortsida som du öppnar från en lista påverkar ändringarna alla poster som du öppnar från listan. Anta till exempel att du öppnar en specifik kund från listsidan kunder och sedan anpassar sidan genom att lägga till ett fält. När du öppnar andra kunder från listan visas också det fält som du har lagt till.
- Ändringarna börjar gälla i alla dina rollcenter. Till exempel om du gör en ändring i kundlistan när rollcentret har angetts till Chef visas dessutom ändringen i kundlistan när rollcentret anges till Försäljningsorderhandläggare.
- Ändringar av en sida i rutan börjar gälla på sidan var den än visas.  
- Du kan bara lägga till fält och kolumner från en fördefinierad lista som baseras på sidan. Du kan inte skapa nya.

## <a name="to-clear-personalization"></a>Rensa anpassning

Vid något tillfälle kanske du vill ångra några eller alla anpassningsändringar som du har gjort på sidan. För att göra detta väljer du i banderollen **anpassa** **mer**, och sedan **Avmarkera anpassning** och sedan väljer du ett av följande alternativ. Tänk på att ta bort anpassningar som inte går att ångra.

|Alternativ|Vad den gör|
|------|------------
|Endast åtgärder|Rensar alla personanpassningsändringar som du har gjort i åtgärdsfältet på den här sidan.|
|Allt utom åtgärder|Rensar alla personanpassningsändringar som du har gjort på sidan förutom de på åtgärdsfältet. Här ingår ändringar av fält, kolumner, delar och paneler. |
|Alla|Rensar alla personanpassningsändringar som du har gjort på sidan så att sidan ser ut som den gjorde från början. Här ingår ändringar av åtgärdsfält, fält, kolumner, delar och paneler.|

## <a name="see-also"></a>Se även

[Hantera anpassning](ui-personalization-manage.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

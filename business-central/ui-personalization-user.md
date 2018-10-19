---
title: Anpassa sidor | Microsoft Docs
description: "Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4c40e38b3f7784f9f7603cddbfd9ac8681d952
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="personalizing-your-workspace"></a>Anpassa din arbetsyta
<!--NAV in the Web client--> Du kan *anpassa* arbetsytan för att passa ditt arbete och dina inställningar genom att ändra sidor så att de endast visar den information som du behöver när du behöver den. De anpassningar som du gör kommer bara att påverka bara vad som visas, inte vad andra användare ser.

Beroende på vilken typ av sida och vad den innehåller kan göra du följande:

-   Lägga till, flytta och ta bort fält.
-   Lägga till, flytta och ta bort kolumner i en lista.
-   Ändra låsning av kolumner i listan. Låsningen låser en eller flera kolumner till vänster i en lista så att de alltid visas även om du bläddrar vågrätt.
-   Ändra bredden på kolumner i en lista.
-   Flytta och ta bort stack-ikoner (paneler).
-   Flytta och ta bort delar. Delar är underavdelningar eller områden på en sida som innehåller flera fält, en annan sida, ett diagram eller paneler.  

## <a name="to-personalize-a-page"></a>Så här anpassar du en sida

1. I det övre högra hörnet väljer du ikonen ![inställningar](media/ui-experience/settings_icon_small.png "ikonen inställningar för rollcenter") och sedan **anpassa**.

    Banderollen **Anpassa** visas längst upp och anger därmed att du kan börja göra ändringar.

    ![Anpassningsläget](media/ui_personalize_mode_small.png "Anpassningsläget")

2.  Gå till sidan du vill anpassa.

    Om du ser en låsikon i informationstexten, se [Varför sidan är låst](ui-personalization-locked.md) för mer information.

3.  Peka på ett område som du vill anpassa, t.ex. fält eller en kolumnrubrik i en lista. Allt som du kan anpassa markeras omedelbart med en pil eller en ram.
<!--
    -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
    -   If the component is a part, the extent of the part is indicated by a border.
    -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
    -->

4.  Använd den här tabellen för att göra ändringar:     <table>
        <tr><th>Vad vill du göra</td><th>Hur du gör det.</th></tr>
        <tr><td>Flytta någonting, precis som fält, kolumn i listan, panel eller del</td><td> Peka var som helst på vad du vill flytta och dra den till dess nya plats. Platsen anges med antingen en tjock vågrät eller lodrät linje.</td></tr>
        <tr><td>Ta bort någonting</td><td>Markera pilen och välj <b>Ta bort</b>. </td></tr>
        <tr><td>Lägga till ett fält eller kolumn</td><td>I banderollen <b>anpassa</b> välj <b>mer</b> och sedan <b>fält</b>.<br /></br>Rutan <b>lägga till fält på sidan</b> öppnas till höger. Den visar de fält som du kan lägga till på sidan. Fält som är markerade som <b>Placerad</b> finns redan finns på sidan. Fält som är markerade som <b>Klar</b> finns redan finns på sidan.<br /></br>Om du vill lägga till ett fält, drar du det från fönstret till den plats där du vill ha den. Platsen anges med antingen en tjock vågrät eller lodrät linje.</td></tr>
        <tr><td>Ändra låsning i en lista till en annan kolumn</td><td>Markera pilen i kolumnen som du vill ska vara den sista kolumnen på låsningen och välj <b>Ange låsning</b>.<br /><br/>Om du vill ange låsningen tillbaka till den ursprungliga angivna platsen, markera pilen för den aktuella kolumnen i låsningen och välj <b>ta bort låsning</b>. Obs! Du kan inte ta bort denna låsta ruta.</td></tr>
        <tr><td>Ändra bredden på en kolumn</td><td>Dra kolumnens högra kantlinje i tabellens rubrikrad. <br /><br />Om du vill maximera kolumnbredden efter den längsta textraden i kolumnen dubbelklickar du på den högra kantlinjen.</td></tr>
      </table>

    > [!IMPORTANT]  
    >   Du kan inte ändra en lista om listan visas som paneler. Måste du först ändra sidan till listvyn genom att välja ikonen ![visa som lista](media/ui_show_as_list_icon.png "Visa som listpil vänster").

5.  Du kan fortsätta att göra ändringar på samma sida eller flytta till en annan sida. Dina ändringar sparas automatiskt medan du gör dem. När du är klar väljer du i **anpassa** banderoll **Klar**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Ta bort anpassningar för att ändra en sida till dess ursprungliga layout
Vid något tillfälle kanske du vill ångra alla anpassningsändringar som du har gjort på sidan så att sidan ser ut som den gjorde från början För att göra detta väljer du i banderollen **anpassa** **mer**, och sedan **Avmarkera anpassning**.

## <a name="personalization-in-detail"></a>Anpassning i detalj
Här följer några tips som hjälper dig att bättre förstå anpassning.  
-   När du ändrar en kortsida som du öppnar från en lista påverkar ändringarna alla poster som du öppnar från listan. Anta till exempel att du öppnar en specifik kund från listsidan kunder och sedan anpassar sidan genom att lägga till ett fält. När du öppnar andra kunder från listan visas också det fält som du har lagt till.
-   Ändringarna börjar gälla i alla dina rollcenter. Till exempel om du gör en ändring i kundlistan när rollcentret har angetts till Chef visas dessutom ändringen i kundlistan när rollcentret anges till Försäljningsorderhandläggare.
-   Ändringar av en sida i rutan börjar gälla på sidan var den än visas.  
-   Du kan bara lägga till fält och kolumner från en fördefinierad lista som baseras på sidan. Du kan inte skapa nya.

## <a name="see-also"></a>Se även
[Hantera anpassning](ui-personalization-manage.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  


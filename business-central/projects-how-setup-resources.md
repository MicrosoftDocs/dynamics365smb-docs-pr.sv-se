---
title: 'Ange projektresurskostnader, priser och kapacitet'
description: 'Om du vill använda resurser och underlätta projekthantering, specificera kostnader och priser för enskilda resurser eller resursgrupper och ange en resurskapacitet.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-resources-for-projects"></a>Konfigurera resurser för projekt

Du måste lägga upp resurser och relaterade kostnader och priser för att hantera resursaktiviteter på rätt sätt. Projektrelaterade priser, rabatter och kostnadsfaktorregler är definierade på projektkortet. Du kan specificera kostnader och priser för enskilda resurser, resursgrupper eller alla tillgängliga resurser i företaget.

När resurser är förbrukade eller sålda i ett projekt hämtas associerade priser och kostnader från informationen som du anger.

Du kan ange standardbeloppet per timme när resursen skapas. Om du till exempel använder en viss maskin för ett projekt i 5 timmar beräknas projektet baserat på beloppet per timme.

> [!NOTE]
> Du kan också köpa externa resurser om du t.ex. vill fakturera en leverantör för levererat arbete. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).<br /><br />
> För externa resurser rekommenderar vi att du namnger eller grupperar dem så att de inte förväxlas med dina interna resurser.
>  
> Om du bokför koncerninterna transaktioner, även om du kan en resurs till en rad på en försäljningsorder, och du omvandlar försäljningsordern till en inköpsorder på den mottagande sidan, tas inte resursen med. Använd koncerninterna inköpstransaktioner om du vill använda fältet **Ink.red.ktonr konc.int partner** på resurskortet för att ange på vilket konto utgifterna ska bokföras.

## <a name="to-set-up-a-resource"></a>Så här skapar du resurser

Skapa ett kort för varje resurs som du vill använda i projekt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Så här skapar du en resursgrupp

Du kan kombinera flera resurser i en resursgrupp. All kapacitet och budget i resursgrupperna samlas från de individuella resurserna. Det är också möjligt att skriva in resursgruppskapacitet, antingen oberoende av de samlade värdena eller som tillägg till dem.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Resursgrupper** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs.

## <a name="to-set-capacity-for-a-resource"></a>Ställa in kapaciteten för en resurs

För att beräkna hur lång tid en resurs kan läggas på projekt, måste deras kapacitet först ställas in som tillgänglig tid per period i arbetskalendern. Denna inställning används när du fyller i projektplaneringsrader som innehåller resursen. Mer information finns i [Skapa projekt](projects-how-create-jobs.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.
2. Öppna det relevanta resurskortet och välj sedan åtgärden **Resurskapacitet**.
3. På sidan **Resurskapacitet** ställer du i fältet **Visa per** in periodlängden, exempelvis **Dag**, som visas i kolumnerna på **Matris för resurskapacitet** på snabbfliken.
4. För varje resurs på en rad anger du för respektive period i kolumnerna hur många timmar som resursen är tillgänglig.
5. Du kan också välja att ställa in resurskapaciteten veckovis med start- och slutdatum genom att välja åtgärden **Ställ in kapacitet**.
6. På sidan **Inställningar för resurskapacitet** fyller du i fälten efter behov.
7. Välj åtgärden **Uppdatera kapacitet**. Sidan **Resurskapacitet** uppdateras med den angivna kapaciteten.
8. Stäng sidan.

## <a name="to-set-up-alternate-resource-costs"></a>Så här skapar du alternativa resurskostnader

Förutom kostnaden som anges på resurskortet, kan du registrera alternativa kostnader för varje resurs. Om t. ex. en anställd har en annan timpenning för övertidsarbete kan du registrera en resurskostnad för denna övertidskostnad. Den alternativa kostnad som du skapar för resursen har företräde framför kostnaden på resurskortet när du använder resursen i resursjournalen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.  
2. Välj den resurs för det som du vill skapa en eller flera alternativa kostnader för och välj sedan åtgärden **Kostnader**.  
3. På sidan **Resurskostnader** fyller du i fälten på en rad efter behov.  
4. Upprepa steg 3 för varje alternativ kostadsresurs som du vill skapa.

**Obs**. Om du vill skapa resurskostnader som gäller alla resurser och resursgrupper öppnar du sidan  **Resurskostnader** och fyller i alla fält.

## <a name="to-set-up-alternate-resource-prices"></a>Så här skapar du alternativa resurspriser

Förutom priset som anges på resurskortet, kan du registrera alternativa priser för varje resurs. Dessa alternativa priser kan vara villkorliga. De kan bero på om resursen används med ett särskilt projekt eller en särskild arbetstyp.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.
2. Välj den resurs för det som du vill skapa en eller flera alternativa priser för och välj sedan åtgärden **Priser**.
3. På sidan **Resurspriser** fyller du i fälten på en rad efter behov.
4. Upprepa steg 3 för varje alternativt resurspris som du vill skapa.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/set-up-jobs-resources/)

## <a name="see-also"></a>Se även

[Ställa in projekthantering](projects-setup-projects.md)  
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

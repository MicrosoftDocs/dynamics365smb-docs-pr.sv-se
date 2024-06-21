---
title: Ställa in arbetstimmar och tjänstetider
description: Lär dig ställ in arbete och tjänsttimmar som används för att beräkna svarsdatum och svarstid för serviceorder och offerter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-work-hours-and-service-hours"></a>Ställa in arbetstimmar och tjänstetider
Ett tjänstehanteringssystem spårar vanligtvis resurstid och serviceorderstatus för prognostisering av arbetsbelastning och servicebehov. [!INCLUDE[prod_short](includes/prod_short.md)] har inbyggda verktyg som du kan anpassa om du vill registrera den här typen av information.  
  
När du har ställt in standardtjänsttid för företaget kan du beräkna svarstid för serviceorder eller skicka varningar eller aviseringar när servicesamtal kommer in. Aviseringsfunktionen implementeras tillsammans med projektschemat.   
  
När du arbetar på en serviceorder kan du uppdatera deras status, så att du kan övervaka framsteg. Tjänsteorderstatus visar reparationsstatus för alla serviceartiklar i serviceordern. Mer information finns i [om serviceordern och reparationsstatus](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Så här skapar du standard servicetider
Du kan använda sidan **Standard servicetider** för att definiera vilka servicearbetstider som gäller på företaget. Programmet använder dessa servicetider för att beräkna ett svarsdatum med tid för serviceorder och offerter och då svarstidsvarningar skickas ut. Standardservicetiden för servicekontrakt används automatiskt om du inte angett särskilda servicetider för ett kontrakt.  
  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Standard servicetider** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Om du inte fyller i raderna på sidan **Standard servicetider** används 24 timmar som standardvärde, som gäller bara för kalenderns arbetsdagar.  
  
## <a name="to-set-up-work-hour-templates"></a>Så här skapar du arbetstidsmallar
Du kan använda sidan **Arbetstidsmallar** för att skapa mallar som innehåller företagets vanligaste arbetstider. Du kan t.ex. skapa mallar för heltidstekniker och deltidstekniker. Använd arbetstidsmallar när du lägger till kapacitet i resurser.  
  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Mallar för arbetstimmar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> När du har angett arbetstimmar per dag beräknas värdet i fältet **Totalt per vecka** automatiskt.  

## <a name="to-set-up-contract-specific-service-hours"></a>Så här skapar du en kontraktspecifik servicekalender
Du använder sidan **Servicekalender** när du lägger upp servicetid för kunden som äger servicekontraktet. Servicekalendern används för att beräkna svarsdatum och svarstid för serviceorder och serviceofferter som tillhör servicekontraktet.  
  
Om du inte skapar en specifik servicekalender för ett servicekontrakt, används standardtjänstkalendern i stället.  
  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk.  
2. Öppna servicekontraktet du vill ställa in särskilda servicetimmar för och välj **Servicetimmar**.  
4. Om du vill lägga upp en servicekalender baserat på en standardtjänstkalender, väljer du åtgärden **Kopiera standardtjänsttider**.  
5. Redigera fälten i servicekalendertransaktionerna. Infoga eller ta bort transaktioner för att konfigurera servicekalendern för kontraktet. Observera att fälten **Dag**, **Starttid** och **Sluttid** måste anges för varje rad.  
6. Om du vill att servicekalendern ska gälla från ett visst datum fyller du i fältet **Startdatum**.  
7. Om du vill att servicekontraktet ska gälla under semestern markerar du kryssrutan i fältet **Giltigt på semestrar**.  

## <a name="see-also"></a>Se även
[Förstå fördelningsstatus och reparationsstatus](service-allocation-status-and-repair-status.md)  
[Ställa in tjänstehantering](service-setup-service.md)  
[Förstå serviceorderstatus och reparationsstatus](service-order-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

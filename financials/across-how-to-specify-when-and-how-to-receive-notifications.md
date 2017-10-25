---
title: "Så här anger du när och hur användare ska meddelas | Microsoft Docs"
description: "När du konfigurerar användare i godkännandearbetsflöden måste du ange hur och när varje användare meddelas om godkännandearbetsflödessteg i fönstret Konfigurera meddelanden och Meddelandeschema. Individuella användare kan också ändra sina meddelandeinställningar genom att välja knappen Ändra meddelandeinställningar i något meddelande."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: db0e3f159a0d6a793ed5881118ecff6d0bf6a529
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-specify-when-and-how-to-receive-notifications"></a>Så här anger du när och hur användare ska meddelas
När du konfigurerar användare i godkännandearbetsflöden måste du ange hur och när varje användare meddelas om godkännandearbetsflödessteg i fönstret **Konfigurera meddelanden** och **Meddelandeschema**. Individuella användare kan också ändra sina meddelandeinställningar genom att välja knappen **Ändra meddelandeinställningar** i något meddelande.  

 Innan du kan konfigurera meddelandeinställningar för en godkännandeanvändare måste du konfigurera användaren som en godkännandeanvändare. Mer information finns i [Så här konfigurerar du godkännandeanvändare](across-how-to-set-up-approval-users.md).  

 Du kan definiera layout och innehåll i meddelanden genom att konfiguera meddelandemallar. Mer information finns i [Så här hanterar du meddelandemallar](across-how-to-manage-notification-templates.md).  

 Många arbetsflödessvar för godkännande handlar om att meddela användare om att en händelse har skett som de måste agera på. Till exempel ett arbetsflödessteg kan vara att en händelse där användare 1 begär godkännande av en ny post. Det relaterade svaret är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten. Det relaterade svaret är att ett meddelande skickas till användare 3 om att starta en process med den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost. Mer information finns i [Arbetsflöden](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Ange när och hur användare ska meddelas  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användarinställningar för godkännande** och välj sedan relaterad länk.  
2.  Markera raden för användaren som du vill konfigurera meddelandeinställningar för och välj sedan åtgärden **Konfigurera meddelanden**.  
3.  I fönstret **Konfigurera meddelanden** kan du fylla i fälten enligt beskrivningen i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Meddelandetyp**|Ange vilken typ av händelse meddelandet handlar om.<br /><br /> Välj något av följande alternativ:<br /><br /> -   **Ny post** anger att meddelandet är en ny post, till exempel ett dokument, som användaren måste agera på.<br />-   **Godkännande** anger att meddelandet handlar om en eller flera godkännandebegäranden.<br />-   **Förfallna** anger att meddelandet är en påminnelse till användare om att de är sena i att agera på en händelse.|  
    |**Kod för meddelandemall**|Ange koden för meddelandemallen som används för att skapa meddelanden för användaren.|  
    |**Ej sammanfattade meddelanden**|Ange om användaren får ett meddelande för varje händelse eller samlade meddelanden.<br /><br /> Om kryssrutan **Ej sammanfattade meddelanden** inte har markerats får användaren meddelanden som samlad information om händelser som uppstår med samma upprepningsmönster i meddelandeschemat.|  

     Du har nu registrerat hur användaren ska meddelas. Fortsätt med att ange när användaren ska meddelas.  

4.  Välj åtgärden **Meddelandeschema**.  
5.  I fönstret **Meddelandeschema** kan du fylla i fälten enligt beskrivningen i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Återkommande**|Ange upprepningsmönstret för användarens mottagning av meddelanden.|  
    |**Tid**|Ange vid vilken tidpunkt på dagen som användaren får meddelanden när värdet i fältet **Återkommande** inte är **Omedelbart**.|  
    |**Daglig frekvens**|Ange på vilken typ av dagar användaren meddelas när värdet i fältet **Återkommande** är **Daglig**.<br /><br /> Markera **Vardag** för meddelanden varje arbetsdag i veckan. Markera **Daglig** för meddelanden varje veckodag inklusive helger.|  
    |**Måndag** till och med **söndag**|Ange på vilka dagar användaren meddelas när värdet i fältet **Återkommande** är **Veckovis**.|  
    |**Datum i månaden**|Ange om användaren meddelas på den första, den sista eller ett visst datum i månaden.|  
    |**Datum för månadsvis meddelande**|Ange månadsdag då användaren meddelas när värdet i fältet **Datum i månaden** är **Anpassat**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Ändra när och hur du ska meddelas  
1.  Välj knappen **Ändra meddelandeinställningar** i ett av meddelandena som du har tagit emot, antingen eller som e-post eller notering.  
2.  Ändra dina meddelandeinställningar så som beskrivs i föregående steg i fönstret **Konfigurera meddelanden**.  

## <a name="see-also"></a>Se även  
 [Så här konfigurerar du godkännandeanvändare](across-how-to-set-up-approval-users.md)   
 [Så här hanterar du meddelandemallar](across-how-to-manage-notification-templates.md)   
 [Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
 [Konfigurera arbetsflöden](across-set-up-workflows.md)   
 [Använda arbetsflöden](across-use-workflows.md)


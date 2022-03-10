---
title: Ange när och hur meddelanden om arbetsflöde ska tas emot
description: När du konfigurerar användare i arbetsflöden för godkännande kan du ange hur och när varje godkännandeanvändare får meddelanden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 3f663ca22cdcfde38b42ac0285eaf403a9e0982d
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129173"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Ange när och hur meddelanden om arbetsflöde ska tas emot
När du konfigurerar godkännandeanvändare i arbetsflöden där du vill att någon ska godkänna ändringar, till exempel när nya poster skapas eller när någon begär ett godkännande, måste du ange hur och när godkännandeanvändaren ska meddelas. Du kan t.ex. ange att en godkännandeanvändare direkt får ett e-postmeddelande när någon skapar en ny kund. Du kan också schemalägga att meddelanden ska levereras, t.ex. en gång per vecka eller per månad.

Man kan också ändra sina meddelandeinställningar genom att välja knappen **Ändra meddelandeinställningar** i något meddelande.  

> [!NOTE]
> Meddelandena levereras enligt meddelandeinställningarna för mottagaren, inte avsändaren. Det är en viktig skillnad eftersom det innebär att när någon begär ett godkännande som en del av ett arbetsflöde kommer deras förfrågan inte nödvändigtvis att skickas direkt. I stället levereras den enligt meddelandeschemat som anges i godkännarens meddelandeinställningar. 

Innan du kan konfigurera meddelandeinställningar för en godkännandeanvändare måste du konfigurera användaren som en godkännandeanvändare. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  

Du kan definiera layouten för e-postmeddelanden genom att anpassa rapporten 1320, e-postmeddelanden. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).  

> [!NOTE]
> Om du vill använda e-post som aviseringsmetod måste du konfigurera e-post för både avsändaren och mottagaren i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Steg i arbetsflöden 
Många arbetsflödessvar för godkännande handlar om att meddela användare om att en händelse har skett som de måste agera på. Till exempel ett arbetsflödessteg kan vara att en händelse där användare 1 begär godkännande av en ny post. Det relaterade svaret är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten. Det relaterade svaret är att ett meddelande skickas till användare 3 om att starta en process med den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost. Mer information finns i [Arbetsflöden](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Ange när och hur användare ska meddelas  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställningar för godkännande** och väljer sedan relaterad länk.  
2.  Markera raden för användaren som du vill konfigurera meddelandeinställningar för och välj sedan åtgärden **Konfigurera meddelanden**.  
3.  På sidan **Konfigurera meddelanden** kan du fylla i fälten enligt beskrivningen i följande tabell.  

    > [!NOTE]
    > Om du öppnar sidan **Konfigurera meddelanden** från sidan **Användarinställningar för godkännande** länkas meddelandeinställningarna till godkännandeanvändaren. Godkännandeanvändaren får alltid arbetsflödesmeddelanden i enlighet med meddelandeinställningen. Om du använder Tell Me för att öppna sidan **Konfigurera meddelanden** gäller meddelandeinställningen för alla användare.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Meddelandetyp**|Ange vilken typ av händelse meddelandet handlar om.<br /><br /> Välj något av följande alternativ:<br /><br /> -   **Ny post** anger att meddelandet är en ny post, till exempel ett dokument, som användaren måste agera på.<br />-   **Godkännande** anger att meddelandet handlar om en eller flera godkännandebegäranden.<br />-   **Förfallna** anger att meddelandet är en påminnelse till användare om att de är sena i att agera på en händelse.|  
    |**Meddelandemetod**|Ange om meddelandet ska skickas som ett e-postmeddelande eller som en intern kommentar.|

    Du kan definiera layouten för e-postmeddelanden genom att anpassa rapporten 1320, e-postmeddelanden. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

    Du har nu registrerat hur användaren ska meddelas. Fortsätt med att ange när användaren ska meddelas.  

4.  Välj åtgärden **Meddelandeschema**.  
5.  På sidan **Meddelandeschema** kan du fylla i fälten enligt beskrivningen i följande tabell.  

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
2.  Ändra dina meddelandeinställningar så som beskrivs i föregående steg på sidan **Konfigurera meddelanden**.  

## <a name="see-also"></a>Se även  
 [Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
 [Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)   
 [Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
 [Konfigurera arbetsflöden](across-set-up-workflows.md)   
 [Använda arbetsflöden](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
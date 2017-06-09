---
title: "Ställa in marknadsföringskampanjer i Financials | Microsoft Docs"
description: "Beskriver hur du kan skapa och genomföra kampanjer i Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Hantera marknadsföringskampanjer
Med en stark marknadsföringsplan kan du identifiera, attrahera och bibehålla kunderna. En marknadsföringsplan består av olika kampanjer och andra interaktioner i samband med försäljnings- och marknadsföringsaktiviteter. När du planerar en kampanj måste du bestämma vilka kontakter som är målgruppen, typ av kampanj (till exempel mässa eller direktmarknadsföring) och vilka säljare som ska utföra respektive uppgift.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Definiera enskilda kampanjer
Innan du kan skapa en kampanj måste du ställa in *kampanjens statuskoder*. Med hjälp av dessa koder hanterar du kampanjen genom att tilldela kampanjen en status. Medan du arbetar med kampanjens olika faser kan du se vilken fas kampanjen befinner sig i och vilket steg som kommer härnäst. Du kan ställa in kampanjens statuskoder i fönstret **kampanjstatus**.

Du kan skapa ett *kampanjkort* för varje kampanj som du vill hålla ordning på. Du kan också visa dessa kampanjkort om du vill visa allmän information om kampanjerna.
Du kan ta bort kampanjtransaktioner om de till exempel anger åtgärder som har avbrutits. Det är endast avbrutna kampanjtransaktioner som kan tas bort.

### <a name="selecting-the-target-audience"></a>Välja ut målgrupp
När du har skapat en kampanj kan du börja skapa de segment som angeer kampanjens målgrupp. Mer information finns i [Hantera segment](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrera rabattsatser
När du har skapat din kampanj, bestämt vilka segment som du vill att kampanjen ska omfatta, och angett start- och slutdatum, registrerar du den rabattsats som kunden ska få på de olika artiklarna på raderna i fönstret **Försäljningsradrabatter**. Du kan också registrera försäljningspriserna för de individuella artiklarna på raderna i fönstret **försäljningspriser**. Du kan öppna båda fönstren från kampanjkortet.

 När du har angett försäljningspriser/radrabatter och segment på kampanjkortet måste du aktivera dem så att kampanjpriserna/rabatterna avspeglas på raderna.

> [!NOTE]  
>  För att försäljningspriserna/radrabatterna ska aktiveras måste du ange om hela segmentet eller om bara några kontakter är kampanjens mål. Om försäljningspriserna/radrabatterna omfattar alla kontakter i segmentet markerar du fältet **Kampanjmål** på snabbfliken **Kampanj** på kortet **Segment**.
Om försäljningspriserna/radrabatterna inte erbjuds alla kontakter i segmentet kan du ta bort markeringen från fältet **Kampanjmål** för de relevanta kontakterna. Om fältet inte visas kan du lägga till det i din vy. Mer information finns i [Användaranpassning](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Hantera segment](marketing-segments.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med Financials](ui-work-product.md)  


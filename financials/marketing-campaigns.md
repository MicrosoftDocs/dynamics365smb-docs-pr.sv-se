---
title: "Ställa in marknadsföringskampanjer i Financials | Microsoft Docs"
description: "Beskriver hur du kan skapa och genomföra kampanjer i Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 05/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 92c5fb75f4f3d3180ba67b89481beed2e58c3dbe
ms.openlocfilehash: 68359d2dd2c2e07463babda91d86d47998f0912a
ms.contentlocale: sv-se
ms.lasthandoff: 05/31/2017


---
# <a name="managing-marketing-campaigns"></a>Hantera marknadsföringskampanjer
Med en stark marknadsföringsplan kan du identifiera, attrahera och bibehålla kunderna. En marknadsföringsplan består av olika kampanjer och andra interaktioner i samband med försäljnings- och marknadsföringsaktiviteter. När du planerar en kampanj måste du bestämma vilka kontakter som är målgruppen, typ av kampanj (till exempel mässa eller direktmarknadsföring) och vilka säljare som ska utföra respektive uppgift.

Varje kampanj består av olika aktiviteter eller uppgifter. Du kan kombinera flera uppgifter, till exempel uppgifter som var och en representerar ett steg i aktiviteter. Alla steg i en aktivitet är knutna till varandra med hjälp av en datumformel. Individuella uppgifter kan endast tilldelas enskilda säljare. Aktiviteter kan kopplas till affärsmöjligheter, säljare, säljpersonal och kontakter. För mer information, se [Så här konfigurerar du cykler och etapper för affärsmöjligheter](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Definiera enskilda kampanjer
Innan du kan skapa en kampanj måste du ställa in *kampanjens statuskoder*. Med hjälp av dessa koder hanterar du kampanjen genom att tilldela kampanjen en status. Medan du arbetar med kampanjens olika faser kan du se vilken fas kampanjen befinner sig i och vilket steg som kommer härnäst. Du kan ställa in kampanjens statuskoder i fönstret **kampanjstatus**.

Du kan skapa ett kampanjkort för varje kampanj som du vill hålla ordning på. Du kan också visa dessa kampanjkort om du vill visa allmän information om kampanjerna.
Du kan ta bort kampanjtransaktioner om de till exempel anger åtgärder som har avbrutits. Det är endast avbrutna kampanjtransaktioner som kan tas bort.

### <a name="selecting-the-target-audience"></a>Välja ut målgrupp
När du har skapat en kampanj kan du börja skapa de segment som angeer kampanjens målgrupp. Mer information finns i [Hantera segment](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrera rabattsatser
När du har skapat din kampanj, bestämt vilka segment som du vill att kampanjen ska omfatta, och angett start- och slutdatum, registrerar du den rabattsats som kunden ska få på de olika artiklarna på raderna i fönstret **Försäljningsradrabatter**. Du kan också registrera försäljningspriserna för de individuella artiklarna på raderna i fönstret **försäljningspriser**. Du kan öppna båda fönstren från kampanjkortet.

 När du har angett försäljningspriser/radrabatter och segment på kampanjkortet måste du aktivera dem så att kampanjpriserna/rabatterna avspeglas på raderna.

**Obs!**: För att försäljningspriserna/radrabatterna ska aktiveras måste du ange om hela segmentet eller om bara några kontakter är kampanjens mål. Om försäljningspriserna/radrabatterna omfattar alla kontakter i segmentet markerar du fältet **Kampanjmål** på snabbfliken **Kampanj** på kortet **Segment**.
Om försäljningspriserna/radrabatterna inte erbjuds alla kontakter i segmentet kan du ta bort markeringen från fältet **Kampanjmål** för de relevanta kontakterna. Om fältet inte visas kan du lägga till det i din vy. Mer information finns i [Användaranpassning](ui-user-personalization.md).

## <a name="conducting-campaigns"></a>Genomföra kampanjer
Medan kampanjen pågår registreras alla interaktioner med kontakterna, eller segmentet. Då kan du få fram statistik och annan information om kostnader och hur väl kampanjen lyckats.

Kampanjer utförs av säljare och du måste skapa aktiviteter för att representera varje aktivitet och tilldela dem till berörda säljare. För mer information, se [Så här konfigurerar du cykler och etapper för affärsmöjligheter](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Hantera segment](marketing-segments.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med Financials](ui-work-product.md)  


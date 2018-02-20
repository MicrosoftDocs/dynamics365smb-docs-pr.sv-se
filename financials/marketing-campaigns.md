---
title: "Konfigurera marknadsföringskampanjer i Finance and Operations, Business edition | Microsoft Docs"
description: "Beskriver hur du kan skapa och genomföra marknadsföringskampanjer i Finance and Operations, Business edition för att identifiera och attrahera presumtiva kunder och bibehålla befintliga."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4ca4fc6eee45c69be3de746ce1d799a481d7ea48
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

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

> [!NOTE]  
>   För att försäljningspriserna/radrabatterna ska aktiveras måste du ange om hela segmentet eller om bara några kontakter är kampanjens mål. Om försäljningspriserna/radrabatterna omfattar alla kontakter i segmentet markerar du fältet **Kampanjmål** på snabbfliken **Kampanj** på kortet **Segment**.

Om försäljningspriserna/radrabatterna inte erbjuds alla kontakter i segmentet kan du ta bort markeringen från fältet **Kampanjmål** för de relevanta kontakterna. Om fältet inte visas kan du lägga till det i din vy. Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).

## <a name="conducting-campaigns"></a>Genomföra kampanjer
Medan kampanjen pågår registreras alla interaktioner med kontakterna, eller segmentet. Då kan du få fram statistik och annan information om kostnader och hur väl kampanjen lyckats.

Kampanjer utförs av säljare och du måste skapa aktiviteter för att representera varje aktivitet och tilldela dem till berörda säljare. För mer information, se [Så här konfigurerar du cykler och etapper för affärsmöjligheter](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Hantera segment](marketing-segments.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med Finance and Operations, Business edition](ui-work-product.md)  


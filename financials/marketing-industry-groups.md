---
title: "Ställa in Branschgrupper för kontaktföretag | Microsoft Docs"
description: "Beskriver användning av Branschgrupper med kontakter i Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Ställa in Branschgrupper för kontaktföretag
Branschgrupper används för att visa vilken bransch kontakterna tillhör, exempelvis detaljhandel eller bilBransch.

Att använda Branschgrupper på kontakter är en två-stegsprocess. Först definierar du Branschgruppkoden. Du måste bara utföra den här steget en gång för varje Branschgrupp. När du har en Branschgrupp kan du börja koppla koden till kontaktföretag.

**Obs!** Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.

## <a name="to-define-an-industry-group-code"></a>Definiera en Branschgruppskod
Koden för branschgruppen definierar typen eller kategorin för den gruppen, till exempel ANNONS för annonsering eller PRESS för TV och radio. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du fönstret **branschgrupper**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Branschgrupper** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="AssignIndustryGroupContact"></a> Så här tilldelar du industrigrupper till en kontakt
Du kan inte tilldela branschgrupper till en kontaktperson, endast företag.

1. Öppna kontakten .
2. Välj åtgärden **företag** och sedan **branschgrupper**. Fönstret **Kontakt branschgrupper** öppnas.
3. I fältet **branschgruppkod**, markera den branschgrupp du vill tilldela.

Upprepa stegen för varje branschgrupp du vill skapa. Branschgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet branschgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal branschgrupper** på avnisttet **Segmentering** på **Kontakt**-fönstret.

När du har tilldelat kontakterna branschgrupper kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


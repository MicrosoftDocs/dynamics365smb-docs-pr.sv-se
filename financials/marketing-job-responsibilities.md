---
title: "Ställa in Arbetsansvar för kontakter | Microsoft Docs"
description: "Beskriver arbetsansvar för kontakter i Financials "
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 610ae314502e60b959f0e2ff705a48b936d79d68
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-job-responsibilities-for-contact-persons"></a>Ställa in arbetsansvar för kontaktpersonerna.
Du kan lägga till information om arbetsansvar för kontaktpersoner för att ange vad kontaktpersonen ansvarar för i företaget, till exempel IT, ledning eller produktion. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

Att använda arbetsansvar på kontakter är en två-stegsprocess. Först definierar du arbetsansvarkoden. Du måste bara utföra den här steget en gång för varje arbetsansvar. När du har en arbetsansvarkod kan du börja koppla koden till kontaktpersoner.

## <a name="tp-define-a-job-responsibility-code"></a>så här definierar du arbetsansvarkod
Arbetsansvarkoden definierar typen eller kategorin för projektet, som t.ex. MARKNADSFÖRING eller KÖP. Du kan ha flera arbetsansvarkoder. Att definiera arbetsansvaret använder du fönstret **Arbetsansvar**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Arbetsansvar**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>så här tilldelar du arbetsansvaret till en kontaktperson
Du kan inte tilldela arbetsansvar till kontaktföretag.

1. Öppna kontaktperson.
2. Välj åtgärden **Person** och sedan **Arbetsansvar**. Fönstret **Kontakt arbetsansvar** öppnas.
3. I fältet **Arbetsansvarskod**, markera det arbetsansvar du vill tilldela.

Upprepa stegen för varje arbetsansvar du vill tilldela. Arbetsansvar kan också tilldelas i kontaktlista på samma sätt.

Antalet arbetsansvar som du har tilldelat kontakter anges automatiskt i fältet **Antal arbetsansvar** i avsnittet **Segmentering** på fönstret **Kontakt**.

När du har tilldelat kontakterna arbetsansvar kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Arbeta med Financials](ui-work-product.md)


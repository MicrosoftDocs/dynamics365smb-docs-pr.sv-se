---
title: "Ställa in Arbetsansvar för kontakter | Microsoft Docs"
description: "Du kan definiera ett arbetsansvar och tilldela den till en kontakt för att ange vilka aktiviteter som kontakten ansvarar för i företaget, till exempel IT- eller produktionsorder."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 7bab8449c957048e49b84eed53647e2921123fe7
ms.contentlocale: sv-se
ms.lasthandoff: 06/01/2018

---
# <a name="set-up-job-responsibilities-for-contact-persons"></a>Ange arbetsansvar för kontaktpersonerna.
Du kan lägga till information om arbetsansvar för kontaktpersoner för att ange vad kontaktpersonen ansvarar för i företaget, till exempel IT, ledning eller produktion. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

Att använda arbetsansvar på kontakter är en två-stegsprocess. Först definierar du arbetsansvarkoden. Du måste bara utföra den här steget en gång för varje arbetsansvar. När du har en arbetsansvarkod kan du börja koppla koden till kontaktpersoner.

## <a name="to-define-a-job-responsibility-code"></a>Så här definierar du en arbetsansvarskod
Arbetsansvarkoden definierar typen eller kategorin för projektet, som t.ex. MARKNADSFÖRING eller KÖP. Du kan ha flera arbetsansvarkoder. Att definiera arbetsansvaret använder du fönstret **Arbetsansvar**.

1. Välj ikonen ![söka efter sida eller rapport](media/ui-search/search_small.png "ikonen söka efter sida eller rapport"), ange **arbetsansvar** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Så här tilldelar du arbetsansvar till en kontaktperson
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
[Arbeta med Business Central](ui-work-product.md)


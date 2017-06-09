---
title: "Ställa in befattningsnivåer för kontaktpersoner | Microsoft Docs"
description: "Beskriver befattningsnivåer för kontakter i Financials "
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bde26a2d5fcb7ec10dcd70fdd30c74893bcb34d5
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-organizational-levels-for-contact-persons"></a>Skapa befattningsnivåer för kontaktpersoner
Du kan använda befattningsnivåer på kontakterna om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

Att använda befattningsnivåer på kontakter är en två-stegsprocess. Först definierar du befattningsnivåkoden. Du måste bara utföra den här steget en gång för varje befattningsnivå. När du har en befattningsnivåkod kan du börja koppla koden till kontaktpersoner.

## <a name="to-define-an-organizational-level-code"></a>för att definiera en befattningsnivåkod
Befattningsnivåkoden anger typen eller kategorin av befattningsnivån, som t.ex. VD eller CFO. Du kan ha flera befattningsnivåkoder. För att definiera befattningsnivån använder du fönstret **Befattningsnivåer**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Befattningsnivåer** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>för att tilldela befattningsnivåer till en kontaktperson
Du kan endast tilldela befattningsnivåer till kontaktpersoner, inte kontaktföretag. Du kan endast tilldela en befattningsnivå per kontakt.

1. Öppna kontakten .
2. I fältet **Befattningsnivåer** väljer du den kod som du vill tilldela.

När du har fördelat befattningsnivåer till kontakterna kan du använda informationen för att skapa segment.

När du har tilldelat kontakterna arbetsansvar kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


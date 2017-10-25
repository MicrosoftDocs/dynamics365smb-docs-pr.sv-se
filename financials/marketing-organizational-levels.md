---
title: "Ställa in befattningsnivåer för kontaktpersoner | Microsoft Docs"
description: "Du kan definiera en befattningsnivå och tilldela den till din kontakt om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a>Så här: Skapa befattningsnivåer för kontaktpersoner
Du kan använda befattningsnivåer på kontakterna om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

Att använda befattningsnivåer på kontakter är en två-stegsprocess. Först definierar du befattningsnivåkoden. Du måste bara utföra den här steget en gång för varje befattningsnivå. När du har en befattningsnivåkod kan du börja koppla koden till kontaktpersoner.

## <a name="to-define-an-organizational-level-code"></a>För att definiera en befattningsnivåkod
Befattningsnivåkoden anger typen eller kategorin av befattningsnivån, som t.ex. VD eller CFO. Du kan ha flera befattningsnivåkoder. För att definiera befattningsnivån använder du fönstret **Befattningsnivåer**.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), gå till **Befattningsnivåer** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>För att tilldela befattningsnivåer till en kontaktperson
Du kan endast tilldela befattningsnivåer till kontaktpersoner, inte kontaktföretag. Du kan endast tilldela en befattningsnivå per kontakt.

1. Öppna kontakten .
2. I fältet **Befattningsnivåer** väljer du den kod som du vill tilldela.

När du har fördelat befattningsnivåer till kontakterna kan du använda informationen för att skapa segment.

När du har tilldelat kontakterna arbetsansvar kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


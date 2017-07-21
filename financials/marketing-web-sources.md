---
title: "Ställa in webbadresser för kontaktföretag | Microsoft Docs"
description: "Du kan definiera internet- eller webbadresser och tilldela dem till ett företag för att identifiera hur du vill söka efter information om kontakterna."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6e78a86ba3d29948b07777d0a346c1ef58d088e6
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a>Så här: Skapa Webbadresser för kontaktföretag
Du kan använda webbadresser med dina kontaktföretag för att t.ex. identifiera sökmotorer och webbplatser på Internet som du vill använda för att söka efter information om kontakterna. När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

Att använda webbadresser på kontakter är en två-stegsprocess. Först definierar du webbadresskoden. Du måste bara utföra den här steget en gång för varje webbadress. När du har en webbadresskod kan du börja koppla koden till kontaktpersoner.

## <a name="to-define-a-web-source-code"></a>för att definiera en webbadresskod
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Webbadresser** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten **Kod**, **Beskrivning** och **URL**.

    Skriv %1 i fältet **URL** för att infoga en platshållare för ett sökord i URL:en. När du startar webbadress från en kontakt ersätts %1 med sökordet (till exempel namnet på företaget) som du har angett i fönstret **Kontakt webbadresser**.

Upprepa stegen för varje webbkälla du vill skapa.

## <a name="to-assign-web-sources-to-a-contact-company"></a>för att tilldela webbadresser till ett kontaktföretag
När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

1. Öppna kontakten .
2. Välj åtgärden **företag** och sedan **webbadresser**. Fönstret **Kontakt webbadresser** öppnas.
3. I fältet **webbadresskod**, välj webbadressen som du vill tilldela.
4. Skriv i fältet **Sökord** det sökord som ska användas för att hitta informationen.

Upprepa stegen för varje webbkälla du vill skapa.

Webbadresser kan också tilldelas i fönstret  **Kontaktlista** på samma sätt.

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


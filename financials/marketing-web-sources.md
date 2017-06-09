---
title: "Ställa in webbadresser för kontaktföretag | Microsoft Docs"
description: "Beskriver hur du använder Webbadresser för kontakter i Financials "
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8a452619aeeee907cf61fd5d1a8fce409ad2e42d
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-web-sources-for-contact-companies"></a>Ställa in Webbadresser för kontaktföretag
Du kan använda webbadresser med dina kontaktföretag för att t.ex. identifiera sökmotorer och webbplatser på Internet som du vill använda för att söka efter information om kontakterna. När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

Att använda webbadresser på kontakter är en två-stegsprocess. Först definierar du webbadresskoden. Du måste bara utföra den här steget en gång för varje webbadress. När du har en webbadresskod kan du börja koppla koden till kontaktpersoner.

## <a name="to-define-a-web-source-code"></a>för att definiera en webbadresskod
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger **Webbadresser** och väljer sedan relaterad länk.
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
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


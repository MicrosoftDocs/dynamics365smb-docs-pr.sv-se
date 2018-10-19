---
title: "Ställa in webbadresser för kontaktföretag | Microsoft Docs"
description: "Du kan definiera internet- eller webbadresser och tilldela dem till ett företag för att identifiera hur du vill söka efter information om kontakterna."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b8c59f24eae07efe8f2c4ca1e4e22d05fd4f1b1c
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a>Skapa Webbadresser för kontaktföretag
Du kan använda webbadresser med dina kontaktföretag för att t.ex. identifiera sökmotorer och webbplatser på Internet som du vill använda för att söka efter information om kontakterna. När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

Att använda webbadresser på kontakter är en två-stegsprocess. Först definierar du webbadresskoden. Du måste bara utföra den här steget en gång för varje webbadress. När du har en webbadresskod kan du börja koppla koden till kontaktpersoner.

## <a name="to-define-a-web-source-code"></a>För att definiera en webbadresskod
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Webbadresser** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten **Kod**, **Beskrivning** och **URL**.

    Skriv %1 i fältet **URL** för att infoga en platshållare för ett sökord i URL:en. När du startar webbadress från en kontakt ersätts %1 med sökordet (till exempel namnet på företaget) som du har angett i fönstret **Kontakt webbadresser**.

Upprepa stegen för varje webbkälla du vill skapa.

## <a name="to-assign-web-sources-to-a-contact-company"></a>För att tilldela webbadresser till ett kontaktföretag
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


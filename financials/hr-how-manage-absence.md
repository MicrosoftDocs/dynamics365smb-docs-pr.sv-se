---
title: "Så här hanterar du personalfrånvaro | Microsoft Docs"
description: "Beskriver hur du registrerar anställdas frånvaro och analyserar frånvarostatistik."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4c5ce7e72c7084995b16b574f3ad670c815ef9ee
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-employee-absence"></a>Så här administrerar du personalfrånvaro
Om du vill kunna administrera en anställds frånvaro, måste du registrera frånvaron i fönstret **Frånvaroregistrering**. Frånvaron kan sedan visas på olika sätt i analys- och rapporteringsändamål.

Du kan visa personalfrånvaron i två olika fönster:

* Fönstret **Frånvaroregistrering**, där du registrerar all personalfrånvaro med en rad för varje frånvaro.
* Fönstret **Personalfrånvaro**, där frånvaron för en enskild anställd visas. Detta är den information som du angav i fönstret **Frånvaroregistrering**, filtrerad efter just denne anställde.

Använd alltid samma enhet (timmar eller dagar) när du registrerar personalfrånvaro för att få fram användbar statistik.

## <a name="to-register-employee-absence"></a>Så här registrerar du personalfrånvaro
Du kan registrera personalfrånvaron dagligen eller med något annat intervall som uppfyller organisationens behov.

1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Frånvaroregistrering** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i en rad för varje personalfrånvaro som du vill registrera.
4. Stäng fönstret.

    > [!Tip]
    > Använd alltid samma enhet (timmar eller dagar) när du registrerar personalfrånvaro för att få fram användbar statistik.

## <a name="to-view-an-individual-employees-absence"></a>Så här visar du frånvaron för en enskild anställd
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Personal** och välj sedan relaterad länk.
2. Välj relevant anställd och välj sedan åtgärden **Frånvaro**.

    Fönstret **Personalfrånvaro** öppnas och visar alla frånvarotillfällen, tillsammans med start- och slutdatum för dessa.

## <a name="to-view-an-employees-absence-by-categories"></a>Så här visar du en anställds frånvaro per kategori
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Personal** och välj sedan relaterad länk.
2. Välj relevant anställd och välj sedan åtgärden **Frånvaro per kategori**.
3. I fönstret **Personalfrånvaro per kategori** fyller du i filterfälten som behövs och klickar sedan på åtgärden **Visa matris**.

    Fönstret **Personalfrånvaro per kat.matris** öppnas och visar all frånvaro efter frånvaroorsak.

## <a name="to-view-all-employee-absences-by-category"></a>Så här visar du alla anställdas frånvaro per kategori
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Frånvaroregistrering** och välj sedan relaterad länk.
2. I fönstret **Frånvaroregistrering** väljer du åtgärden **Översikt per kategori**.
3. I fönstret **Frånvaroöversikt per kategori** ställer du in ett filter i fältet **Anställningsnr.filter** för att visa frånvaron för en enskild anställd eller en specifik grupp anställda.
4. Välj åtgärden **Visa matris**.

    Fönstret **Matris för frånvaroöversikt per kategori** öppnas och visar samtliga anställdas frånvaro uppdelad i frånvaroorsaker.

## <a name="to-view-all-employee-absences-by-period"></a>Så här visar du alla anställdas frånvaro per period
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Frånvaroregistrering** och välj sedan relaterad länk.
   I fönstret **Frånvaroregistrering** väljer du åtgärden **Översikt per period**.
2. I fönstret **Frånvaroöversikt per period** väljer du ett filter i fältet **Orsak till frånvarofilter** för att visa personalfrånvaron som gäller särskilt angivna frånvaroorsaker.
3. Välj åtgärden **Visa matris**.

    Fönstret **Matris för frånvaroöversikt per period** öppnas och visar anställdas frånvaro uppdelad i perioder.

## <a name="see-also"></a>Se även
[Administrera personal](hr-manage-human-resources.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)


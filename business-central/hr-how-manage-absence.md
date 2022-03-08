---
title: Hantera personalfrånvaro | Microsoft Docs
description: Beskriver hur du registrerar anställdas frånvaro och analyserar frånvarostatistik.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 42bd650cd3452be8c209e2ff12d1f5c06d6c4f21
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913619"
---
# <a name="manage-employee-absence"></a>Hantera personalfrånvaro
Om du vill kunna administrera en anställds frånvaro, måste du registrera frånvaron på sidan **Frånvaroregistrering**. Frånvaron kan sedan visas på olika sätt i analys- och rapporteringsändamål.

Du kan visa personalfrånvaro på två olika sidor:

* Sidan **Frånvaroregistrering**, där du registrerar all personalfrånvaro med en rad för varje frånvaro.
* Sidan **Personalfrånvaro**, där frånvaron för en enskild anställd visas. Detta är den information som du angav på sidan **Frånvaroregistrering**, filtrerad efter just denne anställde.

Använd alltid samma enhet (timmar eller dagar) när du registrerar personalfrånvaro för att få fram användbar statistik.

## <a name="to-register-employee-absence"></a>Så här registrerar du personalfrånvaro
Du kan registrera personalfrånvaron dagligen eller med något annat intervall som uppfyller organisationens behov.

1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Frånvaroregistrering** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i en rad för varje personalfrånvaro som du vill registrera.
4. Stäng sidan.

    > [!Tip]
    > Använd alltid samma enhet (timmar eller dagar) när du registrerar personalfrånvaro för att få fram användbar statistik.

## <a name="to-view-an-individual-employees-absence"></a>Så här visar du frånvaron för en enskild anställd
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Personal** och välj sedan relaterad länk.
2. Välj relevant anställd och välj sedan åtgärden **Frånvaro**.

    Sidan **Personalfrånvaro** öppnas och visar alla frånvarotillfällen, tillsammans med start- och slutdatum för dessa.

## <a name="to-view-an-employees-absence-by-categories"></a>Så här visar du en anställds frånvaro per kategori
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Personal** och välj sedan relaterad länk.
2. Välj relevant anställd och välj sedan åtgärden **Frånvaro per kategori**.
3. På sidan **Personalfrånvaro per kategori** fyller du i filterfälten som behövs och klickar sedan på åtgärden **Visa matris**.

    Sidan **Personalfrånvaro per kat.matris** öppnas och visar all frånvaro efter frånvaroorsak.

## <a name="to-view-all-employee-absences-by-category"></a>Så här visar du alla anställdas frånvaro per kategori
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Frånvaroregistrering** och välj sedan relaterad länk.
2. På sidan **Frånvaroregistrering** väljer du åtgärden **Översikt per kategori**.
3. På sidan **Frånvaroöversikt per kategori** ställer du in ett filter i fältet **Anställningsnr.filter** för att visa frånvaron för en enskild anställd eller en specifik grupp anställda.
4. Välj åtgärden **Visa matris**.

    Sidan **Matris för frånvaroöversikt per kategori** öppnas och visar samtliga anställdas frånvaro uppdelad i frånvaroorsaker.

## <a name="to-view-all-employee-absences-by-period"></a>Så här visar du alla anställdas frånvaro per period
1. Välj ikonen **Söka efter sida eller rapport** i det övre högra hörnet, ställ in **Frånvaroregistrering** och välj sedan relaterad länk.
   På sidan **Frånvaroregistrering** väljer du åtgärden **Översikt per perioder**.
2. På sidan **Frånvaroöversikt per period** väljer du ett filter i fältet **Orsak till frånvarofilter** för att visa personalfrånvaron som gäller särskilt angivna frånvaroorsaker.
3. Välj åtgärden **Visa matris**.

    Sidan **Matris för frånvaroöversikt per period** öppnas och visar anställdas frånvaro uppdelad i perioder.

## <a name="see-also"></a>Se även
[Administrera personal](hr-manage-human-resources.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)

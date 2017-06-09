---
title: Skapa kontaktpersoner | Microsoft Docs
description: 'Beskriver hur du skapar kontaktpersoner i Financials '
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
ms.openlocfilehash: 7f35e0b2b98d45f0e28bfb9e0bd43e18d60a3b79
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="create-contact-persons"></a>Skapa kontaktpersoner
Du kan skapa kontaktkort för varje kontakt som arbetar i de företag du har förbindelse med. För varje kontaktföretag kan du ange valfritt antal kontaktpersoner. Du kan också skapa kontaktkort för de personer du vill registrera som oberoende.

**Tips**: Innan du skapar en kontakt kan du markera inställningarna **Arv** i fönstret **Marknadsföringsinställningar**. Inställning av arv tillåter information om kontaktföretag som är vanliga för kontaktpersoner, som till exempel adressinformation, som automatiskt ska kopieras från kontaktföretaget till kontaktpersonen varje gång du skapar en kontaktperson för ett registrerat kontaktföretag.

## <a name="to-create-a-contact-card-for-a-person"></a>Så här skapar du ett kontaktkort för en person
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kontakter**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fältet **Nr.** anger du ett nummer för kontakten.

    Om du har definierat en nummerserie för kontakter i fönstret **Affärsstödsinställning** kan du i stället trycka på Retur så anges nästa tillgängliga kontaktnummer automatiskt. Mer information finns i [Skapa nummerserier](ui-create-number-series.md).
4. I fältet för **Typ**, välj **Person**.
5. Fyll i övriga fält på kontaktkortet.

**Obs!** Innehållet i de fält du markerat i avsnittet **Arv** i fönstret **Marknadsföringsinställningar** kopieras från företaget till personerna i företaget.

## <a name="see-also"></a>Se även
[Ställa in Kundhantering](marketing-setup-marketing.md)  
[Tilldela utskicksgrupp till en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Konfigurera arbetsansvar för kontakter](marketing-job-responsibilities.md)  
[Skapa befattningsnivåer för kontaktpersoner](marketing-organizational-levels.md)  
[Synkronisera kontakter med kunder, leverantörer och bankkonton](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Arbeta med Financials](ui-work-product.md)  


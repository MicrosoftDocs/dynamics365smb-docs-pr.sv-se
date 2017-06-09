---
title: "Ställa in Affärsrelationer för kontakter | Microsoft Docs"
description: "Beskriver affärsrelationer för kontakter i Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6719ac45f298d6c952427c871eaf818cb7480c3
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-business-relations-on-contact-companies"></a>Ställa in affärsrelationer på kontaktföretag
Affärsrelationer används för att visa vilket affärsförhållande du har till kontakterna, till exempel spekulant, bank, konsult eller serviceleverantör.

Att använda affärsrelationer på kontakter är en två-stegsprocess. Först definierar du affärsrelationskoden. Du måste bara utföra den här steget en gång för varje affärsrelation. När du har en affärsrelation kan du börja koppla koden till kontaktföretag.

**Obs!** Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.

## <a name="to-define-a-business-relation-code"></a>Definiera en affärsrelationskod
Affärsrelationkoden definierar en kategori eller en typ av affärsrelation, till exempel BANK eller LAG. Du kan ha flera affärsrelationskoder. För att definiera affärsrelationen använder du fönstret **affärsrelationer**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Affaärsrelationer**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="AssignBusRelContact"></a> Så här tilldelar du affärsrelationer till kontakter
Du kan inte tilldela affärsrelationer till en kontaktperson, endast företag.

1. Öppna kontakten .
2. Välj åtgärden **företag** och sedan **affärsrelationer**.

    Fönstret **Kontakt affärsrelationer** öppnas.
3. I fältet **Affärsrelationskod**, markera den affärsrelation du vill tilldela.

Upprepa stegen för varje affärsrelation du vill tilldela. Affärsrelationer kan också tilldelas i Kontaktlista på samma sätt.

Antalet affärsrelationer som du har tilldelat kontakter anges automatiskt i fältet **Antal affärsrelationer** på avsnittet **Segmentering** på **Kontakt**-fönstret.

När du har tilldelat kontakterna affärsrelationer kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


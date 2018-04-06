---
title: "Definiera affärsrelationskode för kontakter | Microsoft Docs"
description: "Använd affärsrelationer i Business Central för att hjälpa till med marknadsföring och för att visa vilket affärsförhållande du har till potentiella kunder eller kunder, till exempel en bank eller serviceleverantör."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879d933822e061913975c1dbac2bf883ad9bbc1
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Ställa in affärsrelationer på kontaktföretag
Affärsrelationer används för att visa vilket affärsförhållande du har till kontakterna, till exempel spekulant, bank, konsult eller serviceleverantör.

Att använda affärsrelationer på kontakter är en två-stegsprocess. Först definierar du affärsrelationskoden. Du måste bara utföra den här steget en gång för varje affärsrelation. När du har en affärsrelation kan du börja koppla koden till kontaktföretag.

> [!NOTE]  
>   Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.

## <a name="to-define-a-business-relation-code"></a>Definiera en affärsrelationskod
Affärsrelationkoden definierar en kategori eller en typ av affärsrelation, till exempel BANK eller LAG. Du kan ha flera affärsrelationskoder. För att definiera affärsrelationen använder du fönstret **affärsrelationer**.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Affärsrelationer** och välj sedan relaterad länk.
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
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


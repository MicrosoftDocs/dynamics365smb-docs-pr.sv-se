---
title: Skapa en kund eller leverantör från en kontakt | Microsoft Docs
description: Du kan registrera en befintlig kontakt som en kund, leverantör eller bankkonto med befintliga data och ange en affärsrelation.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ccddaa5d1c1a5a31c6b82b99520b90bb28fe64dd
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238400"
---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Skapa en kund, leverantör eller bankkonto från en kontakt
Du vill kanske registrera några av dina befintliga kontakter som kunder, leverantörer eller bankkonton. Skapa en kund, en leverantör eller ett bankkonto från en kontakt låter dig använda befintliga data. När du skapar en kund, leverantör eller ett bankkonto på detta sätt, synkroniseras den med kontakten. Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.

Innan du kan registrera kontakterna på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer på sidan **Marknadsföringsinställningar**. Om du vill registrera kontakter som bankkonton måste du även ange nummerserien för bankkonton på sidan **Redovisningsinställningar**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
2. Välj kontakten du vill skapa som en kund, en leverantör eller ett bankkonto.
3. Välj åtgärden **Skapa som** och välj sedan antingen **Kund**, **Leverantör** eller **Bank**.
4. Bekräfta det följande meddelandet.

Kontaktinformationen överförs från kortet **Kontakt** kortet **Bankkonto**, **Kund** eller **Leverantörens**. Du kanske vill lägga till specifik information på varje kort, t.ex fakturering och betalningsinformation.

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Synkronisera kontakter med kunder, leverantörer och bankkonton](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Så här länkar du kontakter med befintliga kunder, leverantörer och bankkonton](marketing-how-link-contact.md)  
[Så här tilldelar du affärsrelationer till kontakter](marketing-business-relations.md#AssignBusRelContact)  
[Arbeta med Business Central](ui-work-product.md)

---
title: "Skapa en kund eller leverantör från en kontakt | Microsoft Docs"
description: "Du kan registrera en befintlig kontakt som en kund, leverantör eller bankkonto med befintliga data och ange en affärsrelation."
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
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 142c1649438ad31b604767d6b6f35a1caeb3f9e4
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Så här: Skapa en kund, leverantör eller bankkonto från en kontakt
Du vill kanske registrera några av dina befintliga kontakter som kunder, leverantörer eller bankkonton. Skapa en kund, en leverantör eller ett bankkonto från en kontakt låter dig använda befintliga data. När du skapar en kund, leverantör eller ett bankkonto på detta sätt, synkroniseras den med kontakten. Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.

Innan du kan registrera kontakterna på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer i fönstret **Marknadsföringsinställningar**. Om du vill registrera kontakter som bankkonton måste du även ange nummerserien för bankkonton i fönstret **Redovisningsinställningar**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontakter** och välj sedan relaterad länk.
2. Välj kontakten du vill skapa som en kund, en leverantör eller ett bankkonto.
3. Välj åtgärden **Skapa som** och välj sedan antingen **Kund**, **Leverantör** eller **Bank**.
4. Bekräfta det följande meddelandet.

Kontaktinformationen överförs från kortet **Kontakt** kortet **Bankkonto**, **Kund** eller **Leverantörens**. Du kanske vill lägga till specifik information på varje kort, t.ex fakturering och betalningsinformation.

## <a name="see-also"></a>Se även
[Så här skapar du kontaktföretag](marketing-create-contact-companies.md)  
[Så här skapar du kontaktpersoner](marketing-create-contact-persons.md)  
[Ställa in Kundhantering](marketing-setup-marketing.md)  
[Synkronisera kontakter med kunder, leverantörer och bankkonton](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Så här länkar du kontakter med befintliga kunder, leverantörer och bankkonton](marketing-how-link-contact.md)  
[Så här tilldelar du affärsrelationer till kontakter](marketing-business-relations.md#AssignBusRelContact)  
[Arbeta med Financials](ui-work-product.md)


---
title: "Skapa en kund, leverantör eller bankkonto från en kontakt | Microsoft Docs"
description: "Beskriver hur du skapar en kund, leverantör eller ett bankkonto från en kontakt i Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6ecbc24e447917e6316b0579fa8c3ee046e73915
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Skapa en kund, leverantör eller bankkonto från en kontakt
Du vill kanske registrera några av dina befintliga kontakter som kunder, leverantörer eller bankkonton. Skapa en kund, en leverantör eller ett bankkonto från en kontakt låter dig använda befintliga data. När du skapar en kund, leverantör eller ett bankkonto på detta sätt, synkroniseras den med kontakten. Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.

Innan du kan registrera kontakterna på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer i fönstret **Marknadsföringsinställningar**. Om du vill registrera kontakter som bankkonton måste du även ange nummerserien för bankkonton i fönstret **Redovisningsinställningar**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kontakter**, och välj sedan relaterad länk.
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


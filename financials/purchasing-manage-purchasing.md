---
title: "Översikt över uppgifter för hantering av inköp | Microsoft Docs"
description: "Beskriver uppgifter för hantering av inköp eller inköpsprocesser, inklusive hur inköpsfakturor och inköpsorder fungerar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 653cd9b5e9651f2039ab18f3e7a26b299238d817
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="purchasing"></a>Inköp
Du skapar en inköpsfaktura eller inköpsorder för att registrera kostnaden för inköp och för att spåra leverantörsskulder. Om du vill kontrollera ett lager används inköpsfakturor också för att uppdatera lagernivåer dynamiskt, så att du kan minimera lagerkostnader och ge bättre service. Inköpskostnaderna, inklusive serviceutgifter och lagervärden som kommer från bokföring av inköpsfakturor bidrar till vinstsiffror och övriga ekonomiska nyckeltal på din startsida.

Du måste använda inköpsorder om din inköpsprocess kräver att du t.ex. kan registrera delleveranser av en orderkvantitet eftersom hela kvantiteten inte var tillgänglig hos leverantören. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda inköpsorder. För mer information finns i [Så här gör du Direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar inköpsorder på samma sätt som inköpsfakturor.

Du kan låta inköpsfakturor skapas automatiskt, genom att använda OCR-tjänsten (optisk teckenigenkänning) för att konvertera PDF-fakturor från leverantörer till elektroniska dokument, som sedan omvandlas till inköpsfakturor av ett arbetsflöde. För att kunna använda den här funktionen måste du först utföra registrera dig för OCR-tjänsten och därefter utföra olika inställningar. Mer information finns i [Så här bearbetar du inkommande dokument](across-process-income-documents.md).      

Produkter kan vara både lagerartiklar och tjänster. Mer information finns i [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).

För alla inköpsprocesser kan du t.ex. inkludera ett arbetsflöde för godkännande för att kräva att stora inköp godkänns av redovisningschefen. Mer information finns i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs. Uppgifterna anges i den ordning de vanligen utförs.

| Om du vill | Gå till |
| --- | --- |
| Skapa en inköpsfaktura för att registrera en överenskommelse med en leverantör om att köpa produkter till vissa leverans- och betalningsvillkor. |[Så här registrerar du inköp](purchasing-how-record-purchases.md) |
| Skapa en inköpsfaktura för alla eller valda rader på en försäljningsfaktura. |[Så här köper du artiklar för en försäljning](purchasing-how-purchase-products-sale.md) |
| Utför en åtgärd på en obetald bokförd inköpsfaktura som automatiskt skapar en kreditnota och antingen annullerar inköpsfakturan eller skapar den på nytt, så att du kan göra korrigeringar. |[Så här rättar eller makulerar du obetalda försäljningsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Skapa en inköpskreditnota för att återföra en särskild bokförd inköpsfaktura för att visa produkter som du returnerar till leverantören, och vilka belopp som du ska inkassera. |[Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-register-new-vendors.md) |
| Skapa ett leverantörskort för varje leverantör som du har köpt av. |[Så här registrerar du nya leverantörer](purchasing-how-register-new-vendors.md) |

## <a name="see-also"></a>Se även
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Hantera projekt](projects-manage-projects.md)    
[Logistik](madeira-supply-chain.md)      
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

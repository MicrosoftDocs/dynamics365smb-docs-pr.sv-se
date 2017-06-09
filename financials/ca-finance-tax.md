---
title: "Omsättningsskatt och moms på varor och tjänster i Kanada | Microsoft Docs"
description: "Lära dig mer om GST och HST."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Omsättningsskatt och moms på varor och tjänster i Kanada
I Kanada när en leverantör inte har en företagsnärvaro i regionen som inköpet görs i, debiteras leverantören endast för moms på varor och tjänster (GST) eller harmoniserad försäljningsmoms HST). Men om landskapet har en provinsiell omsättningsskatt (PST), måste köparen fortfarande beräkna PST och betala den direkt till regionen. När en skatteområdeskod för regionen markeras använder [!INCLUDE[d365fin](includes/d365fin_md.md)] den för att beräkna PST och bokföra den så att det finns en skatteskuld både i redovisningen och i skattetransaktionsposten. Därför bör skatteområdeskoden som markeras här vara en med endast PST och inte GST.  

Mer information om omsättningsskatt finns i [Omsättningsskatt och skattegrupper i USA och Kanada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Skicka GST-/HST-filen
Skatteinformationen i inköpsdokument används för att generera en GST-/HST-onlinefilöverföring som du måste tillhandahålla till skattemyndigheterna. Den här filen inkluderar moms för varor och tjänster (GST) och harmoniserad försäljningsmoms HST). Arkivet skapas i ett .tax-filformat, som kan överföras online.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Omsättningsskatt och momsgrupper i USA och Kanada](us-finance-sales-tax.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


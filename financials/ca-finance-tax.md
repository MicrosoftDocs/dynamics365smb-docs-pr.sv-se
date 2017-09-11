---
title: Moms i Kanada | Microsoft Docs
description: "Lär dig om omsättningsskatt och moms på varor och tjänster i Kanada."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="9a82b-103">Rapportera omsättningsskatt och moms på varor och tjänster i Kanada</span><span class="sxs-lookup"><span data-stu-id="9a82b-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="9a82b-104">I Kanada när en leverantör inte har en företagsnärvaro i regionen som inköpet görs i, debiteras leverantören endast för moms på varor och tjänster (GST) eller harmoniserad försäljningsmoms (HST).</span><span class="sxs-lookup"><span data-stu-id="9a82b-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="9a82b-105">Men om landskapet har en provinsiell omsättningsskatt (PST), måste köparen fortfarande beräkna PST och betala den direkt till regionen.</span><span class="sxs-lookup"><span data-stu-id="9a82b-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="9a82b-106">När en skatteområdeskod för regionen markeras använder [!INCLUDE[d365fin](includes/d365fin_md.md)] den för att beräkna PST och bokföra den så att det finns en skatteskuld både i redovisningen och i skattetransaktionsposten.</span><span class="sxs-lookup"><span data-stu-id="9a82b-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="9a82b-107">Därför bör skatteområdeskoden som markeras här vara en med endast PST och inte GST.</span><span class="sxs-lookup"><span data-stu-id="9a82b-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="9a82b-108">Mer information om omsättningsskatt finns i [Omsättningsskatt och skattegrupper i USA och Kanada](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="9a82b-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="9a82b-109">Skicka GST-/HST-filen</span><span class="sxs-lookup"><span data-stu-id="9a82b-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="9a82b-110">Skatteinformationen i inköpsdokument används för att generera en GST-/HST-onlinefilöverföring som du måste tillhandahålla till skattemyndigheterna.</span><span class="sxs-lookup"><span data-stu-id="9a82b-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="9a82b-111">Den här filen inkluderar moms för varor och tjänster (GST) och harmoniserad försäljningsmoms (HST).</span><span class="sxs-lookup"><span data-stu-id="9a82b-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="9a82b-112">Arkivet skapas i ett .tax-filformat, som kan överföras online.</span><span class="sxs-lookup"><span data-stu-id="9a82b-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a82b-113">Se även</span><span class="sxs-lookup"><span data-stu-id="9a82b-113">See Also</span></span>
[<span data-ttu-id="9a82b-114">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="9a82b-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="9a82b-115">Ställa in Finance</span><span class="sxs-lookup"><span data-stu-id="9a82b-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="9a82b-116">Omsättningsskatt och momsgrupper i USA och Kanada</span><span class="sxs-lookup"><span data-stu-id="9a82b-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="9a82b-117">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9a82b-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


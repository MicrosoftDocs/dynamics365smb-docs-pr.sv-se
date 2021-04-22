---
title: Designdetaljer – Bokföringsgränssnittsstruktur | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de globala procedurerna i bokföringsgränssnittsstruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b852d6e5d7f96cfba64de219ca414de60cea3a31
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777606"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="8d2fa-103">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="8d2fa-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="8d2fa-104">I gränssnittstrukturen för bokföring i [!INCLUDE[prod_short](includes/prod_short.md)] finns det flera globala processer som använder samma struktur:</span><span class="sxs-lookup"><span data-stu-id="8d2fa-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="8d2fa-105">RunWithCheck och RunWithoutCheck anropar procedurkod – generiskt bokföringsgränssnitt för</span><span class="sxs-lookup"><span data-stu-id="8d2fa-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="8d2fa-106">standardredovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="8d2fa-106">Jnl Line.</span></span>  
* <span data-ttu-id="8d2fa-107">CustPostApplyCustLedgEntry – bokför kundapplikation, anropad från kodmodul 226 CustEntry – koppla bokförda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="8d2fa-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="8d2fa-108">VendPostApplyVendLedgEntry – bokför koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="8d2fa-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="8d2fa-109">UnapplyCustLedgEntry – bokför borttagning av koppling av kundapplikation, anropad från kodmodul 226 CustEntry – koppla bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="8d2fa-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="8d2fa-110">UnapplyVendLedgEntry – bokför borttagning av koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="8d2fa-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d2fa-111">Se även</span><span class="sxs-lookup"><span data-stu-id="8d2fa-111">See Also</span></span>  
[<span data-ttu-id="8d2fa-112">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="8d2fa-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
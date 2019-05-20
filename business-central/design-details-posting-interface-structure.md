---
title: Designdetaljer - Bokföringsgränssnittsstruktur | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de globala procedurerna i bokföringsgränssnittsstruktur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5905a16341dc487aaf624810d691ac4628ac2e30
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239527"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="b54cb-103">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="b54cb-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="b54cb-104">I gränssnittstrukturen för bokföring i [!INCLUDE[d365fin](includes/d365fin_md.md)] finns det flera globala processer som använder samma struktur:</span><span class="sxs-lookup"><span data-stu-id="b54cb-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="b54cb-105">RunWithCheck och RunWithoutCheck anropar procedurkod – generiskt bokföringsgränssnitt för standardredovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="b54cb-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="b54cb-106">CustPostApplyCustLedgEntry – bokför kundapplikation, anropad från kodmodul 226 CustEntry - koppla bokförda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="b54cb-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="b54cb-107">VendPostApplyVendLedgEntry – bokför koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="b54cb-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="b54cb-108">UnapplyCustLedgEntry – bokför borttagning av koppling av kundapplikation, anropad från kodmodul 226 CustEntry - koppla bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="b54cb-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="b54cb-109">UnapplyVendLedgEntry – bokför borttagning av koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry - koppla bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="b54cb-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b54cb-110">Se även</span><span class="sxs-lookup"><span data-stu-id="b54cb-110">See Also</span></span>  
[<span data-ttu-id="b54cb-111">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="b54cb-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
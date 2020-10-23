---
title: Designdetaljer - Bokföringsgränssnittsstruktur | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de globala procedurerna i bokföringsgränssnittsstruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 231148c304c5f2dabba5c69c442dfd0cfdc6397d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921948"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="846c5-103">Designdetaljer: Bokföringsgränssnittsstruktur</span><span class="sxs-lookup"><span data-stu-id="846c5-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="846c5-104">I gränssnittstrukturen för bokföring i [!INCLUDE[d365fin](includes/d365fin_md.md)] finns det flera globala processer som använder samma struktur:</span><span class="sxs-lookup"><span data-stu-id="846c5-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="846c5-105">RunWithCheck och RunWithoutCheck anropar procedurkod – generiskt bokföringsgränssnitt för</span><span class="sxs-lookup"><span data-stu-id="846c5-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="846c5-106">standardredovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="846c5-106">Jnl Line.</span></span>  
* <span data-ttu-id="846c5-107">CustPostApplyCustLedgEntry – bokför kundapplikation, anropad från kodmodul 226 CustEntry - koppla bokförda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="846c5-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="846c5-108">VendPostApplyVendLedgEntry – bokför koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner.</span><span class="sxs-lookup"><span data-stu-id="846c5-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="846c5-109">UnapplyCustLedgEntry – bokför borttagning av koppling av kundapplikation, anropad från kodmodul 226 CustEntry - koppla bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="846c5-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="846c5-110">UnapplyVendLedgEntry – bokför borttagning av koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry - koppla bokförda transaktioner</span><span class="sxs-lookup"><span data-stu-id="846c5-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="846c5-111">Se även</span><span class="sxs-lookup"><span data-stu-id="846c5-111">See Also</span></span>  
[<span data-ttu-id="846c5-112">Designdetaljer: Bokföringsmotorstruktur</span><span class="sxs-lookup"><span data-stu-id="846c5-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
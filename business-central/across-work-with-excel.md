---
title: Visa och redigera i Excel från Business Central | Microsoft-dokument
description: Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 71b4e5b7124f929255f1374b38cfbe28c9f12d2b
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692806"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="f413b-103">Visa och redigera i Excel från Business Central</span><span class="sxs-lookup"><span data-stu-id="f413b-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="f413b-104">Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f413b-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="f413b-105">För att göra detta har du två alternativ.</span><span class="sxs-lookup"><span data-stu-id="f413b-105">To do this, you have two options.</span></span> <span data-ttu-id="f413b-106">Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan.</span><span class="sxs-lookup"><span data-stu-id="f413b-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="f413b-107">Skillnaden mellan de två åtgärderna beskrivs nedan:</span><span class="sxs-lookup"><span data-stu-id="f413b-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="f413b-108">Öppna i Excel</span><span class="sxs-lookup"><span data-stu-id="f413b-108">Open in Excel</span></span>

- <span data-ttu-id="f413b-109">Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="f413b-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="f413b-110">Detta innebär att Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f413b-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="f413b-111">Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f413b-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="f413b-112">Du kan bara spara ändringarna till Excel-filen på datorn.</span><span class="sxs-lookup"><span data-stu-id="f413b-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="f413b-113">Den här åtgärden fungerar både i Windows och macOS.</span><span class="sxs-lookup"><span data-stu-id="f413b-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="f413b-114">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard.</span><span class="sxs-lookup"><span data-stu-id="f413b-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="f413b-115">Om du däremot ställer in [!INCLUDE [prodshort](includes/prodshort.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.</span><span class="sxs-lookup"><span data-stu-id="f413b-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="f413b-116">Redigera i Excel</span><span class="sxs-lookup"><span data-stu-id="f413b-116">Edit in Excel</span></span>

- <span data-ttu-id="f413b-117">Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="f413b-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="f413b-118">Detta innebär att Excel-arbetsboken innehåller nästan samma poster och kolumner.</span><span class="sxs-lookup"><span data-stu-id="f413b-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="f413b-119">Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="f413b-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="f413b-120">Det fungerar endast i Windows. inte macOS.</span><span class="sxs-lookup"><span data-stu-id="f413b-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="f413b-121">Detta utökades i 2019 års version, våg 2.</span><span class="sxs-lookup"><span data-stu-id="f413b-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="f413b-122">Mer information finns i [Förbättringar av Excel-integrering](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="f413b-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="f413b-123">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören.</span><span class="sxs-lookup"><span data-stu-id="f413b-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="f413b-124">För administratörer, om du vill veta hur du installerar Excel-tillägg, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="f413b-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="f413b-125">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är den här funktionen är endast tillgänglig för webbklienten.</span><span class="sxs-lookup"><span data-stu-id="f413b-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="f413b-126">Se skillnaden mellan alternativen</span><span class="sxs-lookup"><span data-stu-id="f413b-126">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="f413b-127">Se även</span><span class="sxs-lookup"><span data-stu-id="f413b-127">See Also</span></span>
[<span data-ttu-id="f413b-128">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="f413b-128">Working with Business Central</span></span>](ui-work-product.md)  

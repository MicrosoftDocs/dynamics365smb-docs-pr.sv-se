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
ms.date: 12/07/2018
ms.author: jswymer
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807430"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="5f79f-103">Visa och redigera i Excel från Business Central</span><span class="sxs-lookup"><span data-stu-id="5f79f-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="5f79f-104">Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5f79f-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="5f79f-105">För att göra detta har du två alternativ.</span><span class="sxs-lookup"><span data-stu-id="5f79f-105">To do this, you have two options.</span></span> <span data-ttu-id="5f79f-106">Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan.</span><span class="sxs-lookup"><span data-stu-id="5f79f-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="5f79f-107">Skillnaden mellan de två åtgärderna beskrivs nedan:</span><span class="sxs-lookup"><span data-stu-id="5f79f-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="5f79f-108">Öppna i Excel</span><span class="sxs-lookup"><span data-stu-id="5f79f-108">Open in Excel</span></span>

-    <span data-ttu-id="5f79f-109">Med den här åtgärden respekterar Excel eventuella filter på sidan gränsen på poster som visas.</span><span class="sxs-lookup"><span data-stu-id="5f79f-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="5f79f-110">Detta innebär att Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5f79f-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="5f79f-111">Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5f79f-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="5f79f-112">Du kan bara spara ändringarna till Excel-filen på datorn.</span><span class="sxs-lookup"><span data-stu-id="5f79f-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="5f79f-113">Den här åtgärden fungerar både i Windows och macOS.</span><span class="sxs-lookup"><span data-stu-id="5f79f-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="5f79f-114">För [!INCLUDE[prodshort](includes/prodshort.md)] lokal, är åtgärden **Öppen i Excel** inte tillgänglig om åtgärden **redigera i Excel** är.</span><span class="sxs-lookup"><span data-stu-id="5f79f-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="5f79f-115">Redigera i Excel</span><span class="sxs-lookup"><span data-stu-id="5f79f-115">Edit in Excel</span></span>

-    <span data-ttu-id="5f79f-116">Med den här åtgärden respekterar Excel-arbetsboken inte filter på sidan gränsen på poster som visas.</span><span class="sxs-lookup"><span data-stu-id="5f79f-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="5f79f-117">Detta innebär att Excel-arbetsboken innehåller alla tillgängliga poster och kolumner, oavsett vad som ska visas på sidan.</span><span class="sxs-lookup"><span data-stu-id="5f79f-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="5f79f-118">Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5f79f-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="5f79f-119">Det fungerar endast i Windows. inte macOS.</span><span class="sxs-lookup"><span data-stu-id="5f79f-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="5f79f-120">För [!INCLUDE[prodshort](includes/prodshort.md)] lokal, är åtgärden **redigera i Excel** endast tillgänglig om Excel-tillägget har installerats av administratören.</span><span class="sxs-lookup"><span data-stu-id="5f79f-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="5f79f-121">För administratörer, om du vill veta hur du installerar Excel-tillägg, se [ställa in Excel-tillägget](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="5f79f-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f79f-122">Se även</span><span class="sxs-lookup"><span data-stu-id="5f79f-122">See Also</span></span>

[<span data-ttu-id="5f79f-123">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="5f79f-123">Working with Business Central</span></span>](ui-work-product.md)  

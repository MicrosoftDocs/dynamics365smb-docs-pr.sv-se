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
ms.date: 01/13/2020
ms.author: jswymer
ms.openlocfilehash: 9fd5c6c242932d75addcfa5c1811bdd1aff99a94
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953058"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="13dd8-103">Visa och redigera i Excel från Business Central</span><span class="sxs-lookup"><span data-stu-id="13dd8-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="13dd8-104">Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="13dd8-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="13dd8-105">För att göra detta har du två alternativ.</span><span class="sxs-lookup"><span data-stu-id="13dd8-105">To do this, you have two options.</span></span> <span data-ttu-id="13dd8-106">Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan.</span><span class="sxs-lookup"><span data-stu-id="13dd8-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="13dd8-107">Skillnaden mellan de två åtgärderna beskrivs nedan:</span><span class="sxs-lookup"><span data-stu-id="13dd8-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="13dd8-108">Öppna i Excel</span><span class="sxs-lookup"><span data-stu-id="13dd8-108">Open in Excel</span></span>

- <span data-ttu-id="13dd8-109">Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="13dd8-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="13dd8-110">Detta innebär att Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="13dd8-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="13dd8-111">Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="13dd8-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="13dd8-112">Du kan bara spara ändringarna till Excel-filen på datorn.</span><span class="sxs-lookup"><span data-stu-id="13dd8-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="13dd8-113">Den här åtgärden fungerar både i Windows och macOS.</span><span class="sxs-lookup"><span data-stu-id="13dd8-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="13dd8-114">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard.</span><span class="sxs-lookup"><span data-stu-id="13dd8-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="13dd8-115">Om du däremot ställer in [!INCLUDE [prodshort](includes/prodshort.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.</span><span class="sxs-lookup"><span data-stu-id="13dd8-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="13dd8-116">Redigera i Excel</span><span class="sxs-lookup"><span data-stu-id="13dd8-116">Edit in Excel</span></span>

- <span data-ttu-id="13dd8-117">Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="13dd8-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="13dd8-118">Detta innebär att Excel-arbetsboken innehåller nästan samma poster och kolumner.</span><span class="sxs-lookup"><span data-stu-id="13dd8-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="13dd8-119">Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="13dd8-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="13dd8-120">Det fungerar endast i Windows. inte macOS.</span><span class="sxs-lookup"><span data-stu-id="13dd8-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="13dd8-121">Detta utökades i 2019 års version, våg 2.</span><span class="sxs-lookup"><span data-stu-id="13dd8-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="13dd8-122">Mer information finns i [Förbättringar av Excel-integrering](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="13dd8-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="13dd8-123">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören.</span><span class="sxs-lookup"><span data-stu-id="13dd8-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="13dd8-124">För administratörer, om du vill veta hur du installerar Excel-tillägg, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="13dd8-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="13dd8-125">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är den här funktionen är endast tillgänglig för webbklienten.</span><span class="sxs-lookup"><span data-stu-id="13dd8-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="13dd8-126">Se skillnaden mellan alternativen</span><span class="sxs-lookup"><span data-stu-id="13dd8-126">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a><span data-ttu-id="13dd8-127">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="13dd8-127">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="13dd8-128">Se även</span><span class="sxs-lookup"><span data-stu-id="13dd8-128">See Also</span></span>
[<span data-ttu-id="13dd8-129">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="13dd8-129">Working with Business Central</span></span>](ui-work-product.md)  

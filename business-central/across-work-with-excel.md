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
ms.date: 07/03/2020
ms.author: jswymer
ms.openlocfilehash: f782b3ce19baa29d9268f3fdf742d2aa6112957f
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534603"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="4141e-103">Visa och redigera i Excel från Business Central</span><span class="sxs-lookup"><span data-stu-id="4141e-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="4141e-104">Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4141e-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="4141e-105">För att göra detta har du två alternativ.</span><span class="sxs-lookup"><span data-stu-id="4141e-105">To do this, you have two options.</span></span> <span data-ttu-id="4141e-106">Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan.</span><span class="sxs-lookup"><span data-stu-id="4141e-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="4141e-107">Skillnaden mellan de två åtgärderna beskrivs nedan:</span><span class="sxs-lookup"><span data-stu-id="4141e-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="4141e-108">Öppna i Excel</span><span class="sxs-lookup"><span data-stu-id="4141e-108">Open in Excel</span></span>

- <span data-ttu-id="4141e-109">Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="4141e-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="4141e-110">Detta innebär att Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4141e-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="4141e-111">Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4141e-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4141e-112">Du kan bara spara ändringarna till Excel-filen på datorn.</span><span class="sxs-lookup"><span data-stu-id="4141e-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="4141e-113">Den här åtgärden fungerar både i Windows och macOS.</span><span class="sxs-lookup"><span data-stu-id="4141e-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="4141e-114">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard.</span><span class="sxs-lookup"><span data-stu-id="4141e-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="4141e-115">Om du däremot ställer in [!INCLUDE[prodshort](includes/prodshort.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.</span><span class="sxs-lookup"><span data-stu-id="4141e-115">However, if you set up [!INCLUDE[prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="4141e-116">Redigera i Excel</span><span class="sxs-lookup"><span data-stu-id="4141e-116">Edit in Excel</span></span>

- <span data-ttu-id="4141e-117">Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="4141e-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="4141e-118">Detta innebär att Excel-arbetsboken innehåller nästan samma poster och kolumner.</span><span class="sxs-lookup"><span data-stu-id="4141e-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="4141e-119">Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4141e-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="4141e-120">Det fungerar endast i Windows. inte macOS.</span><span class="sxs-lookup"><span data-stu-id="4141e-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="4141e-121">Du kan växla företaget som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4141e-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="4141e-122">Det gör du genom att välja ikonen **Alternativ** ![Inställningar för Excel-tillägg](media/cogwheel.png "Alternativ för Excel-tillägg") i Excel-tilläggsfönstret och sedan markera företaget i fältet **Företag**.</span><span class="sxs-lookup"><span data-stu-id="4141e-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="4141e-123">Kontrollera att fältet **Miljö** fältet inte är tomt när du byter företag.</span><span class="sxs-lookup"><span data-stu-id="4141e-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="4141e-124">Om så är fallet gör du det till ett av de tillgängliga alternativen, annars kommer tillägget inte att fungera korrekt.</span><span class="sxs-lookup"><span data-stu-id="4141e-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="4141e-125">Om du gör ändringar i tillägget måste du ladda det på nytt för att kunna uppdatera anslutningen.</span><span class="sxs-lookup"><span data-stu-id="4141e-125">If you make changes to the add-in, you must reload it in order to update the connection.</span></span> <span data-ttu-id="4141e-126">Om du vill läsa in på nytt använder du ![menyn tilläggsprogram för Excel](media/excel-addin-menu.png "Meny Excel tillägg") i det övre högra hörnet i tillägget.</span><span class="sxs-lookup"><span data-stu-id="4141e-126">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span>

> [!NOTE]
> <span data-ttu-id="4141e-127">För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören, och det är då endast tillgängligt för webbklienten.</span><span class="sxs-lookup"><span data-stu-id="4141e-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="4141e-128">För administratörer, om du vill veta hur du installerar Excel-tillägg, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="4141e-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="4141e-129">Se skillnaden mellan alternativen</span><span class="sxs-lookup"><span data-stu-id="4141e-129">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="4141e-130">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="4141e-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="4141e-131">Se även</span><span class="sxs-lookup"><span data-stu-id="4141e-131">See Also</span></span>

[<span data-ttu-id="4141e-132">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="4141e-132">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="4141e-133">Förbättringar av Excel-integrering i 2019 utgivningsplan, våg 2</span><span class="sxs-lookup"><span data-stu-id="4141e-133">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  

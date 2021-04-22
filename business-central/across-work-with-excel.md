---
title: Visa och redigera i Excel från Business Central
description: Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786938"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="b55e2-103">Visa och redigera i Excel från Business Central</span><span class="sxs-lookup"><span data-stu-id="b55e2-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="b55e2-104">Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b55e2-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="b55e2-105">För att göra detta har du två alternativ.</span><span class="sxs-lookup"><span data-stu-id="b55e2-105">To do this, you have two options.</span></span> <span data-ttu-id="b55e2-106">Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan.</span><span class="sxs-lookup"><span data-stu-id="b55e2-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="b55e2-107">Skillnaden mellan de två åtgärderna beskrivs nedan:</span><span class="sxs-lookup"><span data-stu-id="b55e2-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="b55e2-108">Öppna i Excel</span><span class="sxs-lookup"><span data-stu-id="b55e2-108">Open in Excel</span></span>

- <span data-ttu-id="b55e2-109">Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas.</span><span class="sxs-lookup"><span data-stu-id="b55e2-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="b55e2-110">Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b55e2-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="b55e2-111">Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b55e2-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b55e2-112">Du kan bara spara ändringarna till Excel-filen på datorn.</span><span class="sxs-lookup"><span data-stu-id="b55e2-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="b55e2-113">Den här åtgärden fungerar både i Windows och macOS.</span><span class="sxs-lookup"><span data-stu-id="b55e2-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="b55e2-114">För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard.</span><span class="sxs-lookup"><span data-stu-id="b55e2-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="b55e2-115">Om du däremot ställer in [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.</span><span class="sxs-lookup"><span data-stu-id="b55e2-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="b55e2-116">Redigera i Excel</span><span class="sxs-lookup"><span data-stu-id="b55e2-116">Edit in Excel</span></span>

- <span data-ttu-id="b55e2-117">Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar posterna som visas, varför Excel-arbetsboken kommer att innehålla nästan samma poster och kolumner.</span><span class="sxs-lookup"><span data-stu-id="b55e2-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="b55e2-118">Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b55e2-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="b55e2-119">Det fungerar endast i Windows. inte macOS.</span><span class="sxs-lookup"><span data-stu-id="b55e2-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="b55e2-120">Du kan växla företaget som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b55e2-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="b55e2-121">För att byta företag väljer du ikonen **Alternativ** ![Inställningar för Excel-tillägg](media/cogwheel.png "Alternativ för Excel-tillägg") i Excel-tilläggsfönstret och markerar sedan företaget i fältet **Företag**.</span><span class="sxs-lookup"><span data-stu-id="b55e2-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="b55e2-122">Kontrollera att fältet **Miljö** fältet inte är tomt när du byter företag.</span><span class="sxs-lookup"><span data-stu-id="b55e2-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="b55e2-123">Om så är fallet gör du det till ett av de tillgängliga alternativen, annars kommer tillägget inte att fungera korrekt.</span><span class="sxs-lookup"><span data-stu-id="b55e2-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="b55e2-124">Om du gör ändringar i tillägget måste du ladda det på nytt för att uppdatera anslutningen.</span><span class="sxs-lookup"><span data-stu-id="b55e2-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="b55e2-125">Om du vill läsa in på nytt använder du ![menyn tilläggsprogram för Excel](media/excel-addin-menu.png "Meny Excel tillägg") i det övre högra hörnet i tillägget.</span><span class="sxs-lookup"><span data-stu-id="b55e2-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="b55e2-126">Om du inte kan läsa in tillägget, kontakta administratören.</span><span class="sxs-lookup"><span data-stu-id="b55e2-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="b55e2-127">Om du är administratör, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="b55e2-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="b55e2-128">För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören, och det är då endast tillgängligt för webbklienten.</span><span class="sxs-lookup"><span data-stu-id="b55e2-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="b55e2-129">För administratörer: Om du vill veta hur du installerar Excel-tillägget, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="b55e2-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="b55e2-130">Se skillnaden mellan alternativen</span><span class="sxs-lookup"><span data-stu-id="b55e2-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b55e2-131">Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="b55e2-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="b55e2-132">Se även</span><span class="sxs-lookup"><span data-stu-id="b55e2-132">See Also</span></span>

[<span data-ttu-id="b55e2-133">Analysera bokslut i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="b55e2-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="b55e2-134">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="b55e2-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="b55e2-135">Förbättringar av Excel-integrering i 2019 utgivningsplan, våg 2</span><span class="sxs-lookup"><span data-stu-id="b55e2-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
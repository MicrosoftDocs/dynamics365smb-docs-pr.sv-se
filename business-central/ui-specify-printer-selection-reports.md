---
title: Skapa rapporter som ska skrivas ut på en viss skrivare | Microsoft Docs
description: Lär dig att ange en skrivare för en rapport och använda sidan Skrivarval.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: ea713fe831ce0d4befc81825531d3210f755a4cd
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247842"
---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="a02cc-103">Ange skrivarval för rapporter</span><span class="sxs-lookup"><span data-stu-id="a02cc-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="a02cc-104">Den här sidan är tom eftersom du inte har lagt upp särskilda skrivare för specifika rapporter.</span><span class="sxs-lookup"><span data-stu-id="a02cc-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="a02cc-105">Vi arbetar på att lösa detta.</span><span class="sxs-lookup"><span data-stu-id="a02cc-105">We are working on solving this.</span></span>

<span data-ttu-id="a02cc-106">Under tiden när du vill skriva ut en rapport måste du hämta rapporten som ett PDF-dokument först genom att välja knappen **skicka till**.</span><span class="sxs-lookup"><span data-stu-id="a02cc-106">In the meantime, when you want to print a report, you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="a02cc-107">Sedan väljer du vilken typ av fil du vill ladda ner rapporten som, och här bör du välja **PDF-dokument**.</span><span class="sxs-lookup"><span data-stu-id="a02cc-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="a02cc-108">Nu kan du antingen öppna det PDF-dokumentet på en gång och skriva ut det, eller spara det och skriva ut det senare.</span><span class="sxs-lookup"><span data-stu-id="a02cc-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** page to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a><span data-ttu-id="a02cc-109">Se även</span><span class="sxs-lookup"><span data-stu-id="a02cc-109">See Also</span></span>
<span data-ttu-id="a02cc-110">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a02cc-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a02cc-111">Kör batchjobb</span><span class="sxs-lookup"><span data-stu-id="a02cc-111">Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="a02cc-112">Skicka dokument som e-post</span><span class="sxs-lookup"><span data-stu-id="a02cc-112">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  

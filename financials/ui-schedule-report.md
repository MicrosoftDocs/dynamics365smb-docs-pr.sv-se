---
title: "Schemalägga en rapport att köras vid ett visst datum och tider | Microsoft Docs"
description: "Lär dig mer om att skriva en rapport i en jobbkö och schemalägga den att behandlas vid en viss tidpunkt."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, job queue
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0b97a5e48c4b339375ca9ad8cbe8388c5d47bb44
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="schedule-a-report-to-run"></a><span data-ttu-id="c6ecc-103">Så här schemalägger du en rapportkörning</span><span class="sxs-lookup"><span data-stu-id="c6ecc-103">Schedule a Report to Run</span></span>
<span data-ttu-id="c6ecc-104">Du kan schemalägga en rapport att köras vid ett visst datum och tider.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-104">You can schedule a report to run at a specific date and time.</span></span> <span data-ttu-id="c6ecc-105">Planerade rapporter anges i jobbkön och behandlas vid den planerade tid, på liknande sätt som andra jobb.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-105">Scheduled reports are entered in the job queue and processed at the scheduled time, similar to other jobs.</span></span> <span data-ttu-id="c6ecc-106">Du kan välja att spara den behandlade rapporten till en fil, t.ex en Excel-, Word- eller PDF-fil, skriva ut den till en viss skrivare eller bara behandlar rapporten.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-106">You can choose to save the processed report to a file, such as an Excel, Word, or PDF, print it to a selected printer, or process the report only.</span></span> <span data-ttu-id="c6ecc-107">Om du väljer att spara rapporten till en fil skickas den bearbetade rapporten till området **Rapportinkorg**, på din startsida där du kan visa den.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-107">If you choose to save the report to a file, then the processed report is sent to the **Report Inbox** area on your Home page, where you can view it.</span></span>

<span data-ttu-id="c6ecc-108">Du kan schemalägga en rapport när du öppnar en rapport.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-108">You can schedule a report when you open a report.</span></span> <span data-ttu-id="c6ecc-109">Du väljer åtgärden **schema** och sedan anger du information som t.ex. skrivare och tid och datum.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-109">You choose the **Schedule** action and then you enter information such as printer, and time and date.</span></span> <span data-ttu-id="c6ecc-110">Rapporten läggs sedan till jobbkön och körs vid den angivna tidpunkten.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-110">The report is then added to the job queue and will be run at the specified time.</span></span> <span data-ttu-id="c6ecc-111">När rapporten behandlas tas artikeln bort från jobbkön.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-111">When the report is processed, the item will be removed from the job queue.</span></span> <span data-ttu-id="c6ecc-112">Om du har sparat den bearbetade rapporten till en fil, kommer den att vara tillgänglig i området **Rapportinkorg**.</span><span class="sxs-lookup"><span data-stu-id="c6ecc-112">If you saved the processed report to a file, it will be available in the **Report Inbox** area.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6ecc-113">Se även</span><span class="sxs-lookup"><span data-stu-id="c6ecc-113">See Also</span></span>
[<span data-ttu-id="c6ecc-114">Ange skrivarval för rapporter</span><span class="sxs-lookup"><span data-stu-id="c6ecc-114">Specify Printer Selection for Reports</span></span>](ui-specify-printer-selection-reports.md)  
<span data-ttu-id="c6ecc-115">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c6ecc-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


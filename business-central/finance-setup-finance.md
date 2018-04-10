---
title: "Ställa in Financialsprocesser | Microsoft Docs"
description: "Få mer information om uppgifterna för att ställa in Finance i ditt företag som passar alla behov av redovisning, granskning eller bokföring."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 12/20/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d365f86ae25098927b827c1add48aa3400e52ff9
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-finance"></a><span data-ttu-id="509b9-103">Ställa in ekonomi</span><span class="sxs-lookup"><span data-stu-id="509b9-103">Setting Up Finance</span></span>
<span data-ttu-id="509b9-104">För att komma igång snabbare innehåller [!INCLUDE[d365fin](includes/d365fin_md.md)] standardkonfigurationer för de flesta ekonomiska processer.</span><span class="sxs-lookup"><span data-stu-id="509b9-104">To help you get going quickly, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="509b9-105">Om du behöver ändra konfigurationen så att de passar din verksamhet kan du fortsätta direkt.</span><span class="sxs-lookup"><span data-stu-id="509b9-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="509b9-106">Från Rollcenter kan du exempelvis använda en assisterad konfigurationsguide som hjälper dig att konfigurera momssatsen för din plats.</span><span class="sxs-lookup"><span data-stu-id="509b9-106">For example, from the Role Center, you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="509b9-107">Det finns dock några saker som du måste konfigurera själv.</span><span class="sxs-lookup"><span data-stu-id="509b9-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="509b9-108">Om du till exempel vill använda dimensioner som grund för business intelligence.</span><span class="sxs-lookup"><span data-stu-id="509b9-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="509b9-109">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="509b9-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="509b9-110">Om du vill</span><span class="sxs-lookup"><span data-stu-id="509b9-110">To</span></span> | <span data-ttu-id="509b9-111">Gå till</span><span class="sxs-lookup"><span data-stu-id="509b9-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="509b9-112">Välj hur du betalar leverantörerna.</span><span class="sxs-lookup"><span data-stu-id="509b9-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="509b9-113">Definiera betalningssätt</span><span class="sxs-lookup"><span data-stu-id="509b9-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="509b9-114">Ange bokföringsmallar mappar enheter som t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="509b9-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="509b9-115">Ställa in bokföringsmallar</span><span class="sxs-lookup"><span data-stu-id="509b9-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="509b9-116">Ställa in en tolerans genom vilken systemet stänger en faktura, även om betalningen, inklusive rabatt, inte helt täcker fakturabeloppet.</span><span class="sxs-lookup"><span data-stu-id="509b9-116">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="509b9-117">Arbeta med betalningstoleranser och kassarabattstoleranser</span><span class="sxs-lookup"><span data-stu-id="509b9-117">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="509b9-118">Ställa in räkenskapsperioder.</span><span class="sxs-lookup"><span data-stu-id="509b9-118">Set up fiscal periods.</span></span> |[<span data-ttu-id="509b9-119">Så här öppnar du ett nytt räkenskapsår:</span><span class="sxs-lookup"><span data-stu-id="509b9-119">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="509b9-120">Definiera hur du rapporterar belopp för moms som du har lagrat för försäljning till skattemyndigheterna.</span><span class="sxs-lookup"><span data-stu-id="509b9-120">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="509b9-121">Så här: rapportera moms till skattemyndigheterna</span><span class="sxs-lookup"><span data-stu-id="509b9-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="509b9-122">Ange funktioner för försäljning och inköp till att hantera betalningar i utländsk valuta.</span><span class="sxs-lookup"><span data-stu-id="509b9-122">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="509b9-123">Aktivera koppling av kundreskontratransaktioner till olika valutor</span><span class="sxs-lookup"><span data-stu-id="509b9-123">Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="509b9-124">Lägga till nya konton i den befintliga kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="509b9-124">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="509b9-125">Ställa in kontoplanen</span><span class="sxs-lookup"><span data-stu-id="509b9-125">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="509b9-126">Ställa in business intelligence (BI)-diagram för att analysera betalningen.</span><span class="sxs-lookup"><span data-stu-id="509b9-126">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="509b9-127">Ställa in analysvy för kassaflöde</span><span class="sxs-lookup"><span data-stu-id="509b9-127">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="509b9-128">Aktivera fakturering av en kund som inte har angetts i systemet.</span><span class="sxs-lookup"><span data-stu-id="509b9-128">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="509b9-129">Så här skapar du Kontantkunder</span><span class="sxs-lookup"><span data-stu-id="509b9-129">Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="509b9-130">Ställa in Intrastat-rapporten och skicka rapporten till en myndighet</span><span class="sxs-lookup"><span data-stu-id="509b9-130">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="509b9-131">Skapa och rapportera Intrastat</span><span class="sxs-lookup"><span data-stu-id="509b9-131">Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="509b9-132">Se även</span><span class="sxs-lookup"><span data-stu-id="509b9-132">See Also</span></span>
[<span data-ttu-id="509b9-133">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="509b9-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="509b9-134">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="509b9-134">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="509b9-135">Arbeta med dimensioner</span><span class="sxs-lookup"><span data-stu-id="509b9-135">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="509b9-136">Importera verksamhetsdata från andra finanssystem</span><span class="sxs-lookup"><span data-stu-id="509b9-136">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="509b9-137">Analysera kassaflödet i företaget</span><span class="sxs-lookup"><span data-stu-id="509b9-137">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="509b9-138">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="509b9-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

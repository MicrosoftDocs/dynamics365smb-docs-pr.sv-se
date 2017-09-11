---
title: Rapportering av 1099-transaktioner i USA | Microsoft Docs
description: "IRS kräver skatteformuläret 1099 för betalning till leverantörer och du kan ange att ett inköpsdokument är 1099 skattepliktigt och ange koden 1099 för leverantören."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a><span data-ttu-id="24047-103">Rapportering av skattepliktiga 1099-transaktioner i USA</span><span class="sxs-lookup"><span data-stu-id="24047-103">Reporting Transactions as 1099 Liable in the US</span></span>

<span data-ttu-id="24047-104">Det amerikanska skatteverket (IRS) kräver en eller flera versioner av 1099-skatteblanketten för betalningar till leverantörer.</span><span class="sxs-lookup"><span data-stu-id="24047-104">The Internal Revenue Service (IRS) requires one or more versions of the 1099 tax form for payments to vendors.</span></span> <span data-ttu-id="24047-105">Kopior av dessa blanketter måste skickas årligen till leverantörer på eller före den sista dagen i januari.</span><span class="sxs-lookup"><span data-stu-id="24047-105">Copies of these forms must be sent to vendors annually on or before the last day of January.</span></span> <span data-ttu-id="24047-106">I dina inköpsdokument kan du ställa in att dokumentet gäller under 1099, och du kan dessutom ställa in 1099-koden för leverantören.</span><span class="sxs-lookup"><span data-stu-id="24047-106">On your purchase documents, you can specify that the document is 1099 liable, and you can specify the 1099 code for the vendor.</span></span>  

## <a name="1099-codes"></a><span data-ttu-id="24047-107">1099-koder</span><span class="sxs-lookup"><span data-stu-id="24047-107">1099 codes</span></span>
<span data-ttu-id="24047-108">I [!INCLUDE[d365fin](includes/d365fin_md.md)] är de vanligaste 1099-koderna förinställda åt dig, så att du omgående kan skapa de rapporter som behövs.</span><span class="sxs-lookup"><span data-stu-id="24047-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the most common 1099 codes are already set up for you so you are ready to generate the required reports.</span></span> <span data-ttu-id="24047-109">Koderna ställa in i fönstret **IRS 1099-blankettruta**, där du också kan lägga till nya 1099-koder.</span><span class="sxs-lookup"><span data-stu-id="24047-109">The codes are defined in the **IRS 1099 Form Box** window where you can also add new 1099 codes.</span></span> <span data-ttu-id="24047-110">För varje skattepliktig leverantör kan du sedan ställa in relevant 1099-kod på snabbfliken **Betalningar** på leverantörskortet.</span><span class="sxs-lookup"><span data-stu-id="24047-110">For each tax liable vendor, you can then specify the relevant 1099 code on the **Payments** FastTab on the Vendor card.</span></span>  

<span data-ttu-id="24047-111">Med rapporten **1099-information för leverantören** kan du granska 1099-transaktioner som betalats under en viss tidsperiod.</span><span class="sxs-lookup"><span data-stu-id="24047-111">With the **Vendor 1099 Information** report, you can review 1099 transactions paid during a specified period.</span></span> <span data-ttu-id="24047-112">I slutet av året kan du skriva ut 1099-transaktioner på förtryckta blanketter.</span><span class="sxs-lookup"><span data-stu-id="24047-112">At the end of the year, you can print 1099 transactions on preprinted forms.</span></span>  

## <a name="printing-1099-tax-forms"></a><span data-ttu-id="24047-113">Utskrift av 1099-skatteblanketter</span><span class="sxs-lookup"><span data-stu-id="24047-113">Printing 1099 tax forms</span></span>
<span data-ttu-id="24047-114">Via fönstret **IRS 1099-blankettruta** får du åtkomst till följande skatteblanketter:</span><span class="sxs-lookup"><span data-stu-id="24047-114">From the **IRS 1099 Form Box** window, you can access the following tax forms:</span></span>  

* <span data-ttu-id="24047-115">Leverantörens 1099-Div</span><span class="sxs-lookup"><span data-stu-id="24047-115">Vendor 1099 Div</span></span>  

  <span data-ttu-id="24047-116">Skriver ut den federala blanketten 1099-DIV för utdelning och distribution.</span><span class="sxs-lookup"><span data-stu-id="24047-116">Prints the federal form 1099-DIV for dividends and distribution.</span></span> <span data-ttu-id="24047-117">Du kan skriva ut alla eller specifika 1099-DIV-blanketter.</span><span class="sxs-lookup"><span data-stu-id="24047-117">You can print all or specific 1099-DIV forms.</span></span> <span data-ttu-id="24047-118">Rapporten använder koder som gäller för DIV-blankettens belopprutor från fönstret **IRS 1099-blankettruta**.</span><span class="sxs-lookup"><span data-stu-id="24047-118">The report uses the codes that apply to the DIV form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="24047-119">Leverantörens 1099 Int</span><span class="sxs-lookup"><span data-stu-id="24047-119">Vendor 1099 Int</span></span>  

  <span data-ttu-id="24047-120">Skriver ut den federala blanketten 1099-INT för ränteintäkter.</span><span class="sxs-lookup"><span data-stu-id="24047-120">Prints the federal form 1099-INT for interest income.</span></span> <span data-ttu-id="24047-121">Du kan skriva ut alla eller specifika 1099-INT-blanketter.</span><span class="sxs-lookup"><span data-stu-id="24047-121">You can print all or specific 1099-INT forms.</span></span> <span data-ttu-id="24047-122">Rapporten använder de koder som gäller för INT-blankettens belopprutor från fönstret **IRS 1099-blankettruta**.</span><span class="sxs-lookup"><span data-stu-id="24047-122">The report uses the codes that apply to the INT form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="24047-123">Leverantörens 1099 Misc - diverse intäkter</span><span class="sxs-lookup"><span data-stu-id="24047-123">Vendor 1099 Misc - Miscellaneous income</span></span>  

  <span data-ttu-id="24047-124">Skriver ut den federala blanketten 1099-MISC för diverse intäkter.</span><span class="sxs-lookup"><span data-stu-id="24047-124">Prints the federal form 1099-MISC for miscellaneous income.</span></span> <span data-ttu-id="24047-125">Du kan skriva ut alla eller specifika 1099-MISC-blanketter.</span><span class="sxs-lookup"><span data-stu-id="24047-125">You can print all or specific 1099-MISC forms.</span></span> <span data-ttu-id="24047-126">Rapporten använder koder som gäller för MISC-blankettens belopprutor från fönstret **IRS 1099-blankettruta**.</span><span class="sxs-lookup"><span data-stu-id="24047-126">The report uses the codes that apply to the MISC form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  

<span data-ttu-id="24047-127">Lagstadgade ändringar som påverkar den här rapporten och tabelldatan administreras vanligtvis i uppdateringar i slutet av året.</span><span class="sxs-lookup"><span data-stu-id="24047-127">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="24047-128">Det kan vara till hjälp att köra rapporten **1099-information för leverantören** när du vill granska informationen innan du skriver ut blanketterna.</span><span class="sxs-lookup"><span data-stu-id="24047-128">It may be helpful to run the **Vendor 1099 Information** report to review the data before printing the forms.</span></span>

## <a name="submitting-1099-tax-forms-electronically"></a><span data-ttu-id="24047-129">Skicka 1099-skatteblankett elektroniskt</span><span class="sxs-lookup"><span data-stu-id="24047-129">Submitting 1099 tax forms electronically</span></span>
<span data-ttu-id="24047-130">Om du vill skicka 1099-skatteblanketterna elektroniskt, använd då rapporten **1099-magnetiska medier för leverantören**.</span><span class="sxs-lookup"><span data-stu-id="24047-130">To submit the 1099 tax forms electronically, use the **Vendor 1099 Magnetic Media** report.</span></span> <span data-ttu-id="24047-131">Anger de 1099-blanketter som kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="24047-131">Specifies the 1099 forms that can be exported.</span></span> <span data-ttu-id="24047-132">Blankettinformationen som exporteras av den här rapporten är densamma som de rapporter som skriver ut 1099-blanketter som beskrivs i föregående avsnitt.</span><span class="sxs-lookup"><span data-stu-id="24047-132">The form information exported by this report is the same as the reports that print 1099 forms that are described in the previous section.</span></span>  

<span data-ttu-id="24047-133">Rapporten använder koder som gäller för blankettens belopprutor från fönstret **IRS 1099-blankettruta**.</span><span class="sxs-lookup"><span data-stu-id="24047-133">The report uses the codes that apply to the form amount boxes from the **IRS 1099 Form-Box** window.</span></span> <span data-ttu-id="24047-134">Koderna är kopplade till blankettrutorna i rapportens fillayouter, och därför måste tabelldata och rapportversion för ett visst taxeringsår överensstämma.</span><span class="sxs-lookup"><span data-stu-id="24047-134">The codes are mapped to the form boxes in the file layouts of this report, therefore the table data and report version for a particular tax year must be in agreement.</span></span> <span data-ttu-id="24047-135">Om anpassade koder läggs till i tabellen måste dessa mappas till blankettrutorna i detta objekt.</span><span class="sxs-lookup"><span data-stu-id="24047-135">If any custom codes are added to the table these must be mapped to the form boxes inside this object.</span></span>  

<span data-ttu-id="24047-136">Lagstadgade ändringar som påverkar den här rapporten och tabelldatan administreras vanligtvis i uppdateringar i slutet av året.</span><span class="sxs-lookup"><span data-stu-id="24047-136">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="24047-137">Det kan vara till hjälp att köra rapporten **1099-information för leverantören** när du vill granska informationen innan du skapar den elektroniska filen.</span><span class="sxs-lookup"><span data-stu-id="24047-137">It may be helpful to run the **Vendor 1099 Information** report to review the data before generating the electronic file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="24047-138">Se även</span><span class="sxs-lookup"><span data-stu-id="24047-138">See Also</span></span>
[<span data-ttu-id="24047-139">Så här registrerar du nya leverantörer</span><span class="sxs-lookup"><span data-stu-id="24047-139">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="24047-140">Så här registrerar du inköp</span><span class="sxs-lookup"><span data-stu-id="24047-140">How to: Record Purchase</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="24047-141">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="24047-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  


---
title: Anpassa visuella signaler om en stack-ikons aktivitet | Microsoft Docs
description: "Skapa en färgindikator på en stack-ikon för att ge en anpassad visuell signal på stack-ikonens aktivitet."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c93bd33d972b030ede02ad7b24a8127ff2174141
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="6d9e3-103">Skapa en färglagd indikator på stack-ikoner</span><span class="sxs-lookup"><span data-stu-id="6d9e3-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="6d9e3-104">Du kan skapa stack-ikoner som visas på **Startsidan** för att inkludera en indikator som ändrar färg baserat på datavärdena i stack-ikonerna.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-104">You can set up Cues that appear on the **Home** page to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="6d9e3-105">Indikatorn visas som en kulört stapel längs den övre kanten på stack-ikon-panelen.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="6d9e3-106">Den ger en visuell signal över statusen för stack-ikonaktivitet, som kan ange gynnsamma eller ofördelaktiga förhållanden för att meddela användaren att vidta åtgärd.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="6d9e3-107">Om t.ex. en stack-ikon visar pågående försäljningsfakturor kan du ställa in indikatorn för att visa grönt (positivt) när totala antalet pågående försäljningsfakturor är under 10, och röd (negativt) när antalet är större än 20.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="6d9e3-108">Från fönstret **Inställning av stack-ikon** ställer du in indikatorer för alla stack-ikoner som är tillgängliga i företagsdatabasen.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="6d9e3-109">För att ställa in indikatorn, anger du upp till två tröskelvärden som definierar tre intervall av datavärden (låg, medel och hög) som du kan koppla en annan färg (eller stil).</span><span class="sxs-lookup"><span data-stu-id="6d9e3-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="6d9e3-110">Så här ställer du in kulörta indikatorer på stack-ikoner</span><span class="sxs-lookup"><span data-stu-id="6d9e3-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="6d9e3-111">Under **Aktiviteter** på din **Startsida** väljer du **Inställning av stack-ikon**.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-111">Under **Activities** on your **Home** page, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="6d9e3-112">Fönstret **Inställning av stack-ikon** visas.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="6d9e3-113">I fönstret anges indikatorerna som för närvarande är inställda på stack-ikoner.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="6d9e3-114">För att ändra en indikator redigerar du fälten och för att ändra till exempel,värdena för de olika trösklarna.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="6d9e3-115">Efterföljande tabeller listar de bakgrundsfärger som motsvarar alternativen för fälten **Lågt intervallformat**, **Medelintervallformat** och **Högt intervallformat**.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="6d9e3-116">Alternativ</span><span class="sxs-lookup"><span data-stu-id="6d9e3-116">Option</span></span> | <span data-ttu-id="6d9e3-117">Färg</span><span class="sxs-lookup"><span data-stu-id="6d9e3-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="6d9e3-118">**Ingen**</span><span class="sxs-lookup"><span data-stu-id="6d9e3-118">**None**</span></span> |<span data-ttu-id="6d9e3-119">Ingen färg (samma färg som stack-ikonen)</span><span class="sxs-lookup"><span data-stu-id="6d9e3-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="6d9e3-120">**Positiv**</span><span class="sxs-lookup"><span data-stu-id="6d9e3-120">**Favorable**</span></span> |<span data-ttu-id="6d9e3-121">Grön</span><span class="sxs-lookup"><span data-stu-id="6d9e3-121">Green</span></span> |
| <span data-ttu-id="6d9e3-122">**Negativ**</span><span class="sxs-lookup"><span data-stu-id="6d9e3-122">**Unfavorable**</span></span> |<span data-ttu-id="6d9e3-123">Röd</span><span class="sxs-lookup"><span data-stu-id="6d9e3-123">Red</span></span> |
| <span data-ttu-id="6d9e3-124">**Tvetydigt**</span><span class="sxs-lookup"><span data-stu-id="6d9e3-124">**Ambiguous**</span></span> |<span data-ttu-id="6d9e3-125">Gul</span><span class="sxs-lookup"><span data-stu-id="6d9e3-125">Yellow</span></span> |
| <span data-ttu-id="6d9e3-126">**Underordnad**</span><span class="sxs-lookup"><span data-stu-id="6d9e3-126">**Subordinate**</span></span> |<span data-ttu-id="6d9e3-127">Grått</span><span class="sxs-lookup"><span data-stu-id="6d9e3-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="6d9e3-128">Se även</span><span class="sxs-lookup"><span data-stu-id="6d9e3-128">See Also</span></span>
<span data-ttu-id="6d9e3-129">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d9e3-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

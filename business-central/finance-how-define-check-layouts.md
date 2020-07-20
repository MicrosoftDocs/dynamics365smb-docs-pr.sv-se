---
title: Ange layouten för en kontroll | Microsoft Docs
description: Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8346e8a868f73d3de729a56e86530048c58229aa
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/17/2020
ms.locfileid: "3458934"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="26ed8-103">Välj en checklayout</span><span class="sxs-lookup"><span data-stu-id="26ed8-103">Select a Check Layout</span></span>
<span data-ttu-id="26ed8-104">Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna.</span><span class="sxs-lookup"><span data-stu-id="26ed8-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="26ed8-105">Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.</span><span class="sxs-lookup"><span data-stu-id="26ed8-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="26ed8-106">Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.</span><span class="sxs-lookup"><span data-stu-id="26ed8-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="26ed8-107">Välj en checklayout genom att</span><span class="sxs-lookup"><span data-stu-id="26ed8-107">To select a check layout</span></span>
1. <span data-ttu-id="26ed8-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rapportval - bankkonto** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="26ed8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="26ed8-109">På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.</span><span class="sxs-lookup"><span data-stu-id="26ed8-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="26ed8-110">Välj något av följande rapport-ID:</span><span class="sxs-lookup"><span data-stu-id="26ed8-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="26ed8-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="26ed8-111">Report ID</span></span> | <span data-ttu-id="26ed8-112">Rapportnamn</span><span class="sxs-lookup"><span data-stu-id="26ed8-112">Report Name</span></span> | <span data-ttu-id="26ed8-113">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="26ed8-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="26ed8-114">1401</span><span class="sxs-lookup"><span data-stu-id="26ed8-114">1401</span></span> |<span data-ttu-id="26ed8-115">Check</span><span class="sxs-lookup"><span data-stu-id="26ed8-115">Check</span></span> |<span data-ttu-id="26ed8-116">Detta är standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="26ed8-116">This is the default report.</span></span> |
| <span data-ttu-id="26ed8-117">10411</span><span class="sxs-lookup"><span data-stu-id="26ed8-117">10411</span></span> |<span data-ttu-id="26ed8-118">Check (checktalong/checktalong/check)</span><span class="sxs-lookup"><span data-stu-id="26ed8-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="26ed8-119">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check.</span><span class="sxs-lookup"><span data-stu-id="26ed8-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="26ed8-120">10412</span><span class="sxs-lookup"><span data-stu-id="26ed8-120">10412</span></span> |<span data-ttu-id="26ed8-121">Check (checktalong/check/checktalong)</span><span class="sxs-lookup"><span data-stu-id="26ed8-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="26ed8-122">Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/check/checktalong.</span><span class="sxs-lookup"><span data-stu-id="26ed8-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="26ed8-123">10413</span><span class="sxs-lookup"><span data-stu-id="26ed8-123">10413</span></span> |<span data-ttu-id="26ed8-124">Tre checkar per sida</span><span class="sxs-lookup"><span data-stu-id="26ed8-124">Three Checks per Page</span></span> |<span data-ttu-id="26ed8-125">Den här rapporten är utformad för att skriva ut tre checkar på varje sida.</span><span class="sxs-lookup"><span data-stu-id="26ed8-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="26ed8-126">När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**.</span><span class="sxs-lookup"><span data-stu-id="26ed8-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="26ed8-127">Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="26ed8-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="26ed8-128">Om du vill ändra en av dessa standardlayouter använder du antingen Word- eller RDLC-integrering.</span><span class="sxs-lookup"><span data-stu-id="26ed8-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="26ed8-129">Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="26ed8-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="using-micr-and-security-fonts"></a><span data-ttu-id="26ed8-130">Använda MICR och säkerhetsteckensnitt</span><span class="sxs-lookup"><span data-stu-id="26ed8-130">Using MICR and Security Fonts</span></span>
<span data-ttu-id="26ed8-131">Online-versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller förinstallerade teckensnitt på de servrar som kan användas för att definiera kontrollera layouter.</span><span class="sxs-lookup"><span data-stu-id="26ed8-131">The online version of [!INCLUDE[d365fin](includes/d365fin_md.md)] contains pre-installed fonts on the servers that can be used when defining check layouts.</span></span> <span data-ttu-id="26ed8-132">I följande text konturer finns tillgängliga teckensnitt som innehåller länkar till detaljerad information om de olika leverantörerna av teckensnitten från tredje part.</span><span class="sxs-lookup"><span data-stu-id="26ed8-132">The following outlines which fonts are available and has links to detailed information by the 3rd-party suppliers of the fonts.</span></span>

> [!Important]
> <span data-ttu-id="26ed8-133">MICR och kontrollera säkerhetsteckensnitt i Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] licensieras i ett teckensnittspaket från IDAutomation.com, Inc. Dessa produkter får endast användas som en del av och i samband med Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="26ed8-133">MICR and check security fonts in Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] are licensed in a font package from IDAutomation.com, Inc. These products may only be used as part of and in connection with Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="26ed8-134">I uppdatering 15.3 och nyare installeras magnetiskt bläcktecken igenkänningsteckensnitt (MICR) och de kan användas.</span><span class="sxs-lookup"><span data-stu-id="26ed8-134">In update 15.3 and newer, Magnetic Ink Character Recognition (MICR) fonts are installed and available to use.</span></span> <span data-ttu-id="26ed8-135">Både E-13B och CMC-7 standarden stöds.</span><span class="sxs-lookup"><span data-stu-id="26ed8-135">Both the E-13B and the CMC-7 standards are supported.</span></span> <span data-ttu-id="26ed8-136">Förutom MICR-teckensnitt finns speciella säkerhetsteckensnitt som du kan använda för att skapa text, namn, belopp och valutasymboler, euro, pund och yen som du kan manipulera med när en kontroll har skrivits ut.</span><span class="sxs-lookup"><span data-stu-id="26ed8-136">In addition to MICR fonts, special security fonts are available to generate text, names, amounts, and the currency symbols Dollar, Euro, Pound, and Yen, which are hard to tamper with once a check has been printed.</span></span>

> [!NOTE]
> <span data-ttu-id="26ed8-137">Av säkerhetsskäl kan du inte överföra anpassade teckensnitt till [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljön.</span><span class="sxs-lookup"><span data-stu-id="26ed8-137">For security and legal reasons, you cannot upload custom fonts to the [!INCLUDE[d365fin](includes/d365fin_md.md)] environment.</span></span>

### <a name="micr-e-13b-specifications"></a><span data-ttu-id="26ed8-138">MICR E-13B specifikationer</span><span class="sxs-lookup"><span data-stu-id="26ed8-138">MICR E-13B Specifications</span></span>
<span data-ttu-id="26ed8-139">I följande avsnitt sammanfattas specifikationerna för de MICR-E-13B teckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.</span><span class="sxs-lookup"><span data-stu-id="26ed8-139">The following summarizes specifications for the MICR E-13B fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="26ed8-140">![MICR E-13B specifikationer](media/font_MICR_E-13B_Specifications.png "MICR E-13B specifikationer")</span><span class="sxs-lookup"><span data-stu-id="26ed8-140">![MICR E-13B Specifications](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="26ed8-141">Avgränsningstecken</span><span class="sxs-lookup"><span data-stu-id="26ed8-141">Delimiter characters</span></span>
<span data-ttu-id="26ed8-142">![Avgränsningstecken](media/font-micr-letters.png "Avgränsningstecken")</span><span class="sxs-lookup"><span data-stu-id="26ed8-142">![Delimiter characters](media/font-micr-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="26ed8-143">Den fullständiga specifikationen av MICR E-13B teckensnitt finns i leverantörens dokumentation här: (https://www.idautomation.com/micr-fonts/e13b/).</span><span class="sxs-lookup"><span data-stu-id="26ed8-143">The full specification of MICR E-13B fonts can be found in the supplier's documentation here: (https://www.idautomation.com/micr-fonts/e13b/).</span></span>

### <a name="micr-cmc-7-specifications"></a><span data-ttu-id="26ed8-144">MICR CMC-7 specifikationer</span><span class="sxs-lookup"><span data-stu-id="26ed8-144">MICR CMC-7 Specifications</span></span>
<span data-ttu-id="26ed8-145">Följande CMC-7 teckensnitt finns tillgängliga [!INCLUDE[d365fin](includes/d365fin_md.md)] online:</span><span class="sxs-lookup"><span data-stu-id="26ed8-145">The following CMC-7 fonts are available in [!INCLUDE[d365fin](includes/d365fin_md.md)] online:</span></span>

- <span data-ttu-id="26ed8-146">IDAutomationCMC7</span><span class="sxs-lookup"><span data-stu-id="26ed8-146">IDAutomationCMC7</span></span>
- <span data-ttu-id="26ed8-147">IDAutomationCMC7n10</span><span class="sxs-lookup"><span data-stu-id="26ed8-147">IDAutomationCMC7n10</span></span>
- <span data-ttu-id="26ed8-148">IDAutomationCMC7n25</span><span class="sxs-lookup"><span data-stu-id="26ed8-148">IDAutomationCMC7n25</span></span>
-   <span data-ttu-id="26ed8-149">IDAutomationCMC7n40</span><span class="sxs-lookup"><span data-stu-id="26ed8-149">IDAutomationCMC7n40</span></span>

<span data-ttu-id="26ed8-150">I följande avsnitt sammanfattas specifikationerna för de MICR CMC-7 teckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.</span><span class="sxs-lookup"><span data-stu-id="26ed8-150">The following summarizes specifications for the MICR CMC-7 fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="26ed8-151">![MICR CMC-7 specifikationer](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 specifikationer")</span><span class="sxs-lookup"><span data-stu-id="26ed8-151">![MICR CMC-7 Specifications](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="26ed8-152">Avgränsningstecken</span><span class="sxs-lookup"><span data-stu-id="26ed8-152">Delimiter characters</span></span>
<span data-ttu-id="26ed8-153">![Avgränsningstecken](media/font-cmc7-letters.png "Avgränsningstecken")</span><span class="sxs-lookup"><span data-stu-id="26ed8-153">![Delimiter characters](media/font-cmc7-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="26ed8-154">Den fullständiga specifikationen av MICR CMC-7 teckensnitt finns i leverantörens dokumentation här: (http://www.idautomation.com/micr-fonts/cmc7/).</span><span class="sxs-lookup"><span data-stu-id="26ed8-154">The full specification of MICR CMC-7 fonts can be found in the supplier's documentation here: (http://www.idautomation.com/micr-fonts/cmc7/).</span></span>

### <a name="secure-font-specifications"></a><span data-ttu-id="26ed8-155">Specifikationer för säkra teckensnitt</span><span class="sxs-lookup"><span data-stu-id="26ed8-155">Secure Font Specifications</span></span>
<span data-ttu-id="26ed8-156">I följande avsnitt sammanfattas specifikationerna för kontrollera säkerhetsteckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.</span><span class="sxs-lookup"><span data-stu-id="26ed8-156">The following summarizes specifications for check security fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="26ed8-157">![Kontrollera specifikationer för säkerhetsteckensnitt](media/font_check-security-font_Specifications.png "Kontrollera specifikationer för säkerhetsteckensnitt")</span><span class="sxs-lookup"><span data-stu-id="26ed8-157">![Check Security Font Specifications](media/font_check-security-font_Specifications.png "Check Security Font Specifications")</span></span>

<span data-ttu-id="26ed8-158">Den fullständiga specifikationen av kontrollera säkerhetsteckensnitt finns i leverantörens dokumentation här: (https://www.idautomation.com/security-fonts/).</span><span class="sxs-lookup"><span data-stu-id="26ed8-158">The full specification of check security fonts can be found in the supplier's documentation here: (https://www.idautomation.com/security-fonts/).</span></span>

<span data-ttu-id="26ed8-159">Det finns också teckensnitt för andra syften i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="26ed8-159">Fonts for other purposes are also available in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="26ed8-160">Mer information finns i [tillgängliga teckensnitt](ui-fonts.md)</span><span class="sxs-lookup"><span data-stu-id="26ed8-160">For more information, see [Available Fonts](ui-fonts.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="26ed8-161">Se även</span><span class="sxs-lookup"><span data-stu-id="26ed8-161">See Also</span></span>
[<span data-ttu-id="26ed8-162">Skapa och ändra anpassade rapportlayouter</span><span class="sxs-lookup"><span data-stu-id="26ed8-162">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="26ed8-163">Teckensnitt i Business Central</span><span class="sxs-lookup"><span data-stu-id="26ed8-163">Fonts in Business Central</span></span>](ui-fonts.md)  
[<span data-ttu-id="26ed8-164">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="26ed8-164">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="26ed8-165">[Stämma av bankkonton](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="26ed8-165">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="26ed8-166">Slutföra periodslutsprocesser</span><span class="sxs-lookup"><span data-stu-id="26ed8-166">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="26ed8-167">[Arbeta med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26ed8-167">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="26ed8-168">Allmänna affärsfunktioner</span><span class="sxs-lookup"><span data-stu-id="26ed8-168">General Business Functionality</span></span>](ui-across-business-areas.md)

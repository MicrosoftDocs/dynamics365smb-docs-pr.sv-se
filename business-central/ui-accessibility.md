---
title: Hjälpmedelsfunktioner
description: Kortkommandon och andra hjälpmedelsfunktioner.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c303c39850e22d3df375838d42703133428b4c7d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772360"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="300fa-103">Hjälpmedel och kortkommandon</span><span class="sxs-lookup"><span data-stu-id="300fa-103">Accessibility and Keyboard Shortcuts</span></span>

<span data-ttu-id="300fa-104">Det här avsnittet innehåller information om de funktioner som gör [!INCLUDE[prod_short](includes/prod_short.md)] tillgängligt för användare med funktionshinder.</span><span class="sxs-lookup"><span data-stu-id="300fa-104">This topic provides information about the features that make [!INCLUDE[prod_short](includes/prod_short.md)] readily available to people with disabilities.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="300fa-105">stöder följande hjälpmedelsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="300fa-105">supports the following accessibility features:</span></span>  

- <span data-ttu-id="300fa-106">Kortkommandon</span><span class="sxs-lookup"><span data-stu-id="300fa-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="300fa-107">Mer information finns i [Kortkommandon](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="300fa-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

- <span data-ttu-id="300fa-108">Navigering</span><span class="sxs-lookup"><span data-stu-id="300fa-108">Navigation</span></span>  

- <span data-ttu-id="300fa-109">Rubriker</span><span class="sxs-lookup"><span data-stu-id="300fa-109">Headings</span></span>  

- <span data-ttu-id="300fa-110">Alternativ text för bilder och länkar</span><span class="sxs-lookup"><span data-stu-id="300fa-110">Alternative text for images and links</span></span>  

- <span data-ttu-id="300fa-111">Stöd för vanliga hjälpmedel</span><span class="sxs-lookup"><span data-stu-id="300fa-111">Support for common assistive technologies</span></span>  

- <span data-ttu-id="300fa-112">Använd kortkommandon för att zooma in och ut på vilken sida som helst</span><span class="sxs-lookup"><span data-stu-id="300fa-112">Use keyboard shortcuts to zoom in or out on any page</span></span>

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[prod_short](includes/prod_short.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

## <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="300fa-113">Navigering</span><span class="sxs-lookup"><span data-stu-id="300fa-113">Navigation</span></span>  
 <span data-ttu-id="300fa-114">Du kan bläddra mellan flikar och åtgärder i menyfliksområdet, element i navigeringsbalken och andra kontroller i [!INCLUDE[prod_short](includes/prod_short.md)]-sidor och -rapporter med hjälp av tangentbordet.</span><span class="sxs-lookup"><span data-stu-id="300fa-114">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[prod_short](includes/prod_short.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="300fa-115">Om du vill flytta fokus från en flik, åtgärd eller kontroll till en annan, trycker du på Tabb-tangenten för att gå vidare.</span><span class="sxs-lookup"><span data-stu-id="300fa-115">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="300fa-116">Tryck på Shift+Tabb för att flytta bakåt.</span><span class="sxs-lookup"><span data-stu-id="300fa-116">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="300fa-117">Med tabbordningen kan du också växla mellan den primära webbläsarsidan och dialogrutor som begär exempelvis bekräftelse eller inloggningssidan.</span><span class="sxs-lookup"><span data-stu-id="300fa-117">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

## <a name="headings-in-content"></a><a name="Headings"></a> <span data-ttu-id="300fa-118">Rubriker i innehåll</span><span class="sxs-lookup"><span data-stu-id="300fa-118">Headings in Content</span></span>
 
 <span data-ttu-id="300fa-119">HTML-källan för [!INCLUDE[prod_short](includes/prod_short.md)]-innehåll använder taggar för att hjälpa användare av tekniska hjälpmedel för att förstå sidans struktur och innehåll.</span><span class="sxs-lookup"><span data-stu-id="300fa-119">The HTML source for [!INCLUDE[prod_short](includes/prod_short.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="300fa-120">På listsidor definieras exempelvis kolumnerna i TH-taggar, och kolumnrubrikerna anges med attributet TITLE inuti taggen.</span><span class="sxs-lookup"><span data-stu-id="300fa-120">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="300fa-121">Rubriker för element, till exempel snabbflikar, faktaboxar och fält ingår i rubriktaggarna (H1, H2, H3 och H4).</span><span class="sxs-lookup"><span data-stu-id="300fa-121">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

## <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="300fa-122">Bilder och länkar</span><span class="sxs-lookup"><span data-stu-id="300fa-122">Image and Links</span></span>

 <span data-ttu-id="300fa-123">En beskrivande text för bilder anges med attributet ALT i IMG-taggen.</span><span class="sxs-lookup"><span data-stu-id="300fa-123">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="300fa-124">En beskrivande text för hyperlänkar anges med rubrikattributet inuti A-taggen.</span><span class="sxs-lookup"><span data-stu-id="300fa-124">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="300fa-125">Hjälpmedel</span><span class="sxs-lookup"><span data-stu-id="300fa-125">Assistive Technologies</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="300fa-126">stöder olika hjälpmedel, till exempel hög kontrast, skärmläsare och program för röstigenkänning.</span><span class="sxs-lookup"><span data-stu-id="300fa-126">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="300fa-127">Vissa hjälpmedel fungerar kanske inte tillsammans med vissa element på [!INCLUDE[prod_short](includes/prod_short.md)]-sidor.</span><span class="sxs-lookup"><span data-stu-id="300fa-127">Some assistive technologies may not work well with certain elements in [!INCLUDE[prod_short](includes/prod_short.md)] pages.</span></span>  

## <a name="zoom"></a><a name="zoom"></a> <span data-ttu-id="300fa-128">Zooma</span><span class="sxs-lookup"><span data-stu-id="300fa-128">Zoom</span></span>

<span data-ttu-id="300fa-129">I de flesta webbläsare används vanliga kortkommandon för att zooma in och ut på den aktuella sidan.</span><span class="sxs-lookup"><span data-stu-id="300fa-129">Most browsers use standard keyboard shortcuts to zoom in and out on the current page.</span></span> <span data-ttu-id="300fa-130">Dessa kortkommandon är inte specifika för [!INCLUDE [prod_short](includes/prod_short.md)], men de fungerar när du använder [!INCLUDE [prod_short](includes/prod_short.md)] i en webbläsare.</span><span class="sxs-lookup"><span data-stu-id="300fa-130">These keyboard shortcuts are not specific to [!INCLUDE [prod_short](includes/prod_short.md)], but they work when you use [!INCLUDE [prod_short](includes/prod_short.md)] in a browser.</span></span> <span data-ttu-id="300fa-131">En lista över vilka kortkommandon som stöds finns i [Kortkommandon för att zooma in och ut](keyboard-shortcuts.md#zoomshortcuts).</span><span class="sxs-lookup"><span data-stu-id="300fa-131">For a list of supported keyboard shortcuts, see [Keyboard Shortcuts for Zooming In and Out](keyboard-shortcuts.md#zoomshortcuts).</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="300fa-132">Mer information om hjälpmedel</span><span class="sxs-lookup"><span data-stu-id="300fa-132">For more accessibility information</span></span>

<span data-ttu-id="300fa-133">Du hittar mer information om åtkomst via Microsofts produkter och hjälpmedel på webbplatsen för [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="300fa-133">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="300fa-134">Se även</span><span class="sxs-lookup"><span data-stu-id="300fa-134">See Also</span></span>

[<span data-ttu-id="300fa-135">Gör dig redo att göra affärer</span><span class="sxs-lookup"><span data-stu-id="300fa-135">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="300fa-136">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="300fa-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="300fa-137">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="300fa-137">Frequently Asked Questions</span></span>](across-faq.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
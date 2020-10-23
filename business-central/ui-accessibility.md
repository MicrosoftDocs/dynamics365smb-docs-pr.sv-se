---
title: Hjälpmedelsfunktioner
description: Kortkommandon och andra hjälpmedelsfunktioner.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 69b1dccc88750dca2e2f406554db34357bd8d6db
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912777"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="edea4-103">Hjälpmedel och kortkommandon</span><span class="sxs-lookup"><span data-stu-id="edea4-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="edea4-104">Det här avsnittet innehåller information om de funktioner som gör [!INCLUDE[d365fin](includes/d365fin_md.md)] tillgängligt för användare med funktionshinder.</span><span class="sxs-lookup"><span data-stu-id="edea4-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="edea4-105">stöder följande hjälpmedelsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="edea4-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="edea4-106">Kortkommandon</span><span class="sxs-lookup"><span data-stu-id="edea4-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="edea4-107">Mer information finns i [Kortkommandon](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="edea4-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="edea4-108">Navigering</span><span class="sxs-lookup"><span data-stu-id="edea4-108">Navigation</span></span>  

-   <span data-ttu-id="edea4-109">Rubriker</span><span class="sxs-lookup"><span data-stu-id="edea4-109">Headings</span></span>  

-   <span data-ttu-id="edea4-110">Alternativ text för bilder och länkar</span><span class="sxs-lookup"><span data-stu-id="edea4-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="edea4-111">Stöd för vanliga hjälpmedel</span><span class="sxs-lookup"><span data-stu-id="edea4-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

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

##  <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="edea4-112">Navigering</span><span class="sxs-lookup"><span data-stu-id="edea4-112">Navigation</span></span>  
 <span data-ttu-id="edea4-113">Du kan bläddra mellan flikar och åtgärder i menyfliksområdet, element i navigeringsbalken och andra kontroller i [!INCLUDE[d365fin](includes/d365fin_md.md)]-sidor och -rapporter med hjälp av tangentbordet.</span><span class="sxs-lookup"><span data-stu-id="edea4-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="edea4-114">Om du vill flytta fokus från en flik, åtgärd eller kontroll till en annan, trycker du på Tabb-tangenten för att gå vidare.</span><span class="sxs-lookup"><span data-stu-id="edea4-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="edea4-115">Tryck på Shift+Tabb för att flytta bakåt.</span><span class="sxs-lookup"><span data-stu-id="edea4-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="edea4-116">Med tabbordningen kan du också växla mellan den primära webbläsarsidan och dialogrutor som begär exempelvis bekräftelse eller inloggningssidan.</span><span class="sxs-lookup"><span data-stu-id="edea4-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="headings"></a><a name="Headings"></a> <span data-ttu-id="edea4-117">Rubriker</span><span class="sxs-lookup"><span data-stu-id="edea4-117">Headings</span></span>  
 <span data-ttu-id="edea4-118">HTML-källan för [!INCLUDE[d365fin](includes/d365fin_md.md)]-innehåll använder taggar för att hjälpa användare av tekniska hjälpmedel för att förstå sidans struktur och innehåll.</span><span class="sxs-lookup"><span data-stu-id="edea4-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="edea4-119">På listsidor definieras exempelvis kolumnerna i TH-taggar, och kolumnrubrikerna anges med attributet TITLE inuti taggen.</span><span class="sxs-lookup"><span data-stu-id="edea4-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="edea4-120">Rubriker för element, till exempel snabbflikar, faktaboxar och fält ingår i rubriktaggarna (H1, H2, H3 och H4).</span><span class="sxs-lookup"><span data-stu-id="edea4-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="edea4-121">Bilder och länkar</span><span class="sxs-lookup"><span data-stu-id="edea4-121">Image and Links</span></span>  
 <span data-ttu-id="edea4-122">En beskrivande text för bilder anges med attributet ALT i IMG-taggen.</span><span class="sxs-lookup"><span data-stu-id="edea4-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="edea4-123">En beskrivande text för hyperlänkar anges med rubrikattributet inuti A-taggen.</span><span class="sxs-lookup"><span data-stu-id="edea4-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="edea4-124">Hjälpmedel</span><span class="sxs-lookup"><span data-stu-id="edea4-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="edea4-125">stöder olika hjälpmedel, till exempel hög kontrast, skärmläsare och program för röstigenkänning.</span><span class="sxs-lookup"><span data-stu-id="edea4-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="edea4-126">Vissa hjälpmedel fungerar kanske inte tillsammans med vissa element på [!INCLUDE[d365fin](includes/d365fin_md.md)]-sidor.</span><span class="sxs-lookup"><span data-stu-id="edea4-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="edea4-127">Mer information om hjälpmedel</span><span class="sxs-lookup"><span data-stu-id="edea4-127">For more accessibility information</span></span>  
<span data-ttu-id="edea4-128">Du hittar mer information om åtkomst via Microsofts produkter och hjälpmedel på webbplatsen för [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="edea4-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="edea4-129">Se även</span><span class="sxs-lookup"><span data-stu-id="edea4-129">See Also</span></span>
[<span data-ttu-id="edea4-130">Komma igång</span><span class="sxs-lookup"><span data-stu-id="edea4-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="edea4-131">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edea4-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="edea4-132">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="edea4-132">Frequently Asked Questions</span></span>](across-faq.md)  

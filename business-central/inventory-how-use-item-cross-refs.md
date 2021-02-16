---
title: Använd artikeltvärreferenser
description: Skapa referenser mellan de beskrivningar som du och din leverantör använder för en artikel så att du kan infoga leverantörens artikelbeskrivning på inköpsdokument.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 7d670f6553a1bd70dcc3d97f90436f36c6627c56
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013798"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="4a987-103">Använd artikeltvärreferenser</span><span class="sxs-lookup"><span data-stu-id="4a987-103">Use Item Cross References</span></span>
<span data-ttu-id="4a987-104">Om du har skapat en tvärreferens mellan den artikelbeskrivning som du använder för en artikel och den beskrivning som används för leverantören som levererar den artikeln och leverantörens artikelbeskrivning infogas automatiskt på inköpsdokument för en leverantör när du fyller i fältet **Tvärreferensnr**</span><span class="sxs-lookup"><span data-stu-id="4a987-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="4a987-105">.</span><span class="sxs-lookup"><span data-stu-id="4a987-105">field.</span></span> <span data-ttu-id="4a987-106">Samma sak gäller för kundens artikelnummer i försäljningsdokument.</span><span class="sxs-lookup"><span data-stu-id="4a987-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="4a987-107">I följande procedurer beskrivs hur du använder artikelns tvärreferens på inköpssidan.</span><span class="sxs-lookup"><span data-stu-id="4a987-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="4a987-108">Momenten är liknande för försäljningssidan.</span><span class="sxs-lookup"><span data-stu-id="4a987-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="4a987-109">Det blir allt vanligare för artikelidentifierare som GTIN eller GUID som innehåller 30 eller fler tecken, vilket är mer än den aktuella funktionen för korsreferenser kan hanteras.</span><span class="sxs-lookup"><span data-stu-id="4a987-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="4a987-110">Om du behöver använda referenser som innehåller fler än 30 tecken kan administratören aktivera funktionen **Skriv längre artikelreferenser** på sidan [Funktionshantering](https://businesscentral.dynamics.com/?page=2610) (länken kräver att du har en [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation).</span><span class="sxs-lookup"><span data-stu-id="4a987-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="4a987-111">Hur du använder referenser ändras inte, men namn på sådant som sidor och knappar gör det.</span><span class="sxs-lookup"><span data-stu-id="4a987-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="4a987-112">Exempelvis kommer sidan **Transaktioner för korsreferens av artikel** att bli sidan **Transaktioner för artikelreferens**.</span><span class="sxs-lookup"><span data-stu-id="4a987-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="4a987-113">Så här skapar du en artikeltvärreferens för en leverantörs artikelbeskrivning</span><span class="sxs-lookup"><span data-stu-id="4a987-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="4a987-114">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4a987-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4a987-115">Öppna kortet för en artikel som du vill skapa en korsreferens till för den artikelbeskrivning som leverantören använder för artikeln.</span><span class="sxs-lookup"><span data-stu-id="4a987-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="4a987-116">Välj åtgärd **tvärreferenser**.</span><span class="sxs-lookup"><span data-stu-id="4a987-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="4a987-117">Om du inte hittar åtgärden **Korsreferenser** väljer du om du vill visa fler alternativ och sedan söker du under **Relaterat** > **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="4a987-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="4a987-118">På en ny rad på sidan **Artikel tvärreferenstrans**, fyll i fälten efter behov.</span><span class="sxs-lookup"><span data-stu-id="4a987-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="4a987-119">.</span><span class="sxs-lookup"><span data-stu-id="4a987-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="4a987-120">Ange leverantörens artikelbeskrivning på en inköpsorder</span><span class="sxs-lookup"><span data-stu-id="4a987-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="4a987-121">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4a987-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4a987-122">Skapa en inköpsorder för leverantören som du ställer in en artikeltvärreferens för ovan.</span><span class="sxs-lookup"><span data-stu-id="4a987-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="4a987-123">Skapa en inköpsorderrad för artikeln som du ställer in en artikeltvärreferens för ovan.</span><span class="sxs-lookup"><span data-stu-id="4a987-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="4a987-124">I **Tvärreferensnummer**</span><span class="sxs-lookup"><span data-stu-id="4a987-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="4a987-125">välj artikeln artikelkorsreferens som du har skapat och välj sedan knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a987-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="4a987-126">Fältet **beskrivning** på raden skrivs över med leverantörens artikelbeskrivning som ställs in på korsreferensartikelns transaktion.</span><span class="sxs-lookup"><span data-stu-id="4a987-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a987-127">Se även</span><span class="sxs-lookup"><span data-stu-id="4a987-127">See Also</span></span>
[<span data-ttu-id="4a987-128">Registrera nya artiklar</span><span class="sxs-lookup"><span data-stu-id="4a987-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="4a987-129">Lager</span><span class="sxs-lookup"><span data-stu-id="4a987-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4a987-130">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a987-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

---
title: Lägg till ytterligare rader när du definierar utökade beskrivningar
description: Du kan lägga till ytterligare rader om du vill utöka standardtexten som beskriver en artikel, ett redovisningskonto och andra data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: sgroespe
ms.openlocfilehash: 0b611a4f2bcabec7cda408790ab659c6cf3f8e97
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542573"
---
# <a name="add-extended-text"></a><span data-ttu-id="ac935-103">Lägg till extratext</span><span class="sxs-lookup"><span data-stu-id="ac935-103">Add Extended Text</span></span>

<span data-ttu-id="ac935-104">Du kan utöka beskrivningen av artiklar, lagerhållningsenheter, redovisningskonton och resurser genom att lägga till extra rader som extratext.</span><span class="sxs-lookup"><span data-stu-id="ac935-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="ac935-105">Du kan också ange villkor för hur de extra raderna ska användas.</span><span class="sxs-lookup"><span data-stu-id="ac935-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="ac935-106">I följande avsnitt beskrivs hur du lägger till extratext i en beskrivning av en artikel.</span><span class="sxs-lookup"><span data-stu-id="ac935-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="ac935-107">Men samma steg gäller för lager enheter, redovisningskonton och resurser.</span><span class="sxs-lookup"><span data-stu-id="ac935-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="ac935-108">Om du vill definiera extratexten för en beskrivning</span><span class="sxs-lookup"><span data-stu-id="ac935-108">To define extended text for an description</span></span>

1. <span data-ttu-id="ac935-109">Öppna kortet för en artikel som du vill lägga till extratext på, och välj sedan åtgärden **Extratext**.</span><span class="sxs-lookup"><span data-stu-id="ac935-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="ac935-110">Fyll i fälten **Kod** och **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="ac935-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="ac935-111">Välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ac935-111">Choose the **New**.</span></span>
4. <span data-ttu-id="ac935-112">Fyll i fältet **Språkkod** eller markera kryssrutan **Alla språkkoder** om du vill använda språkkoder.</span><span class="sxs-lookup"><span data-stu-id="ac935-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="ac935-113">Fyll i fältet **Startdatum** och fältet **Slutdatum** om du vill begränsa den period under vilken extratexten ska användas.</span><span class="sxs-lookup"><span data-stu-id="ac935-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="ac935-114">I fältet **Text** anger du den extra texten.</span><span class="sxs-lookup"><span data-stu-id="ac935-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="ac935-115">Markera relevanta kryssrutor för dokumenttyperna där du vill att extratexten ska skrivas ut.</span><span class="sxs-lookup"><span data-stu-id="ac935-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="ac935-116">Stäng sidan.</span><span class="sxs-lookup"><span data-stu-id="ac935-116">Close the page.</span></span>

<span data-ttu-id="ac935-117">Nu kan du lägga till den utökade texten i dokument.</span><span class="sxs-lookup"><span data-stu-id="ac935-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="ac935-118">I proceduren nedan beskrivs hur du lägger till extratext på en försäljningsorder, men samma steg gäller för andra dokument som du har angett för den extratext.</span><span class="sxs-lookup"><span data-stu-id="ac935-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="ac935-119">För att lägga till en utökad artikeltext på en försäljningsorderrad.</span><span class="sxs-lookup"><span data-stu-id="ac935-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="ac935-120">Öppna en försäljningsorder med en försäljningsrad för en artikel som har förlängd text som har definierats.</span><span class="sxs-lookup"><span data-stu-id="ac935-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="ac935-121">Mer information finns i [Sälja produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="ac935-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="ac935-122">Markera den aktuella raden och välj sedan åtgärden **Infoga förl. text**.</span><span class="sxs-lookup"><span data-stu-id="ac935-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac935-123">Se även</span><span class="sxs-lookup"><span data-stu-id="ac935-123">See Also</span></span>

[<span data-ttu-id="ac935-124">Ställa in lager</span><span class="sxs-lookup"><span data-stu-id="ac935-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="ac935-125">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac935-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

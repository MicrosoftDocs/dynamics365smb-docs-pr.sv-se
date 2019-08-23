---
title: Bokföra försäljningsdokument | Microsoft Docs
description: Lära dig olika bokföringsfunktioner för att bokföra försäljningsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 01e831ddddeffe6a64c6de24b4cd8c1b94bad9c3
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796901"
---
# <a name="posting-sales"></a><span data-ttu-id="265b9-103">Bokföra försäljning</span><span class="sxs-lookup"><span data-stu-id="265b9-103">Posting Sales</span></span>
<span data-ttu-id="265b9-104">I **Bokföringsgrupp** i ett försäljningsdokument kan du välja mellan följande bokföringsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="265b9-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="265b9-105">**Bokföra**</span><span class="sxs-lookup"><span data-stu-id="265b9-105">**Post**</span></span>
* <span data-ttu-id="265b9-106">**Testa rapport**</span><span class="sxs-lookup"><span data-stu-id="265b9-106">**Test Report**</span></span>
* <span data-ttu-id="265b9-107">**Bokför och skicka**</span><span class="sxs-lookup"><span data-stu-id="265b9-107">**Post and Send**</span></span>
* <span data-ttu-id="265b9-108">**Bokför och skriv ut**</span><span class="sxs-lookup"><span data-stu-id="265b9-108">**Post and Print**</span></span>
* <span data-ttu-id="265b9-109">**Bokför och e-posta**</span><span class="sxs-lookup"><span data-stu-id="265b9-109">**Post and Email**</span></span>
* <span data-ttu-id="265b9-110">**Bokför batch-jobb**</span><span class="sxs-lookup"><span data-stu-id="265b9-110">**Post Batch**</span></span>
* <span data-ttu-id="265b9-111">**Förhandsgranska bokföring**</span><span class="sxs-lookup"><span data-stu-id="265b9-111">**Preview Posting**</span></span>

<span data-ttu-id="265b9-112">När du har fyllt i alla raderna och skrivit in all information på försäljningsordern kan du bokföra den.</span><span class="sxs-lookup"><span data-stu-id="265b9-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="265b9-113">Här skapas en leverans och en faktura.</span><span class="sxs-lookup"><span data-stu-id="265b9-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="265b9-114">När en försäljningsorder bokförs, uppdateras kundens konto, redovisningen och artikeltransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="265b9-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="265b9-115">För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="265b9-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="265b9-116">Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="265b9-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="265b9-117">Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet.</span><span class="sxs-lookup"><span data-stu-id="265b9-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="265b9-118">Huruvida rabattransaktionen bokförs eller inte beror på innehållet i fältet **Rabattbokföring** på sidan **Försäljningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="265b9-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="265b9-119">För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto).</span><span class="sxs-lookup"><span data-stu-id="265b9-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="265b9-120">Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.</span><span class="sxs-lookup"><span data-stu-id="265b9-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="265b9-121">När du bokför en order kan du skapa både en utleverans och en faktura.</span><span class="sxs-lookup"><span data-stu-id="265b9-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="265b9-122">Detta kan göras samtidigt eller oberoende av varandra.</span><span class="sxs-lookup"><span data-stu-id="265b9-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="265b9-123">Du kan också skapa en delutleverans och en delfaktura genom att fylla i fältet **Ant. att utleverera** och **Ant. att fakturera** på de enskilda försäljningsorderraderna innan du bokför.</span><span class="sxs-lookup"><span data-stu-id="265b9-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="265b9-124">Observera att du inte kan skapa en faktura för något som inte har utlevererats.</span><span class="sxs-lookup"><span data-stu-id="265b9-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="265b9-125">D.v.s. innan du kan fakturera måste du ha registrerat en leverans alternativt välja att leverera och fakturera samtidigt.</span><span class="sxs-lookup"><span data-stu-id="265b9-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="265b9-126">När bokföringen är slutförd tas de bokförda försäljningsraderna bort från ordern.</span><span class="sxs-lookup"><span data-stu-id="265b9-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="265b9-127">Du får ett meddelande när bokföringen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="265b9-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="265b9-128">Sedan kan du se de bokförda transaktionerna på de olika sidorna som innehåller bokförda transaktioner, t.ex. sidorna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktion**, **Bokförda försäljningsutleveranser** och **Bokförda försäljningsfakturor**.</span><span class="sxs-lookup"><span data-stu-id="265b9-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

## <a name="see-also"></a><span data-ttu-id="265b9-129">Se även</span><span class="sxs-lookup"><span data-stu-id="265b9-129">See Also</span></span>

[<span data-ttu-id="265b9-130">Försäljning</span><span class="sxs-lookup"><span data-stu-id="265b9-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="265b9-131">Skicka dokument som e-post</span><span class="sxs-lookup"><span data-stu-id="265b9-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="265b9-132">Korrigera eller makulera obetalda försäljningsfakturor</span><span class="sxs-lookup"><span data-stu-id="265b9-132">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="265b9-133">Med hjälp av Berätta för att hitta funktioner och Information</span><span class="sxs-lookup"><span data-stu-id="265b9-133">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="265b9-134">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="265b9-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

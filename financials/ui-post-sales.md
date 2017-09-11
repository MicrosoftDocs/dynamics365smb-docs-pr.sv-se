---
title: "Förstå hur du bokför försäljningsdokument | Microsoft Docs"
description: "Få mer information om de olika bokföringsfunktionerna för att bokföra försäljningsdokument."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 106102d07761673461bc28bbf6452ed05f926112
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="posting-sales"></a><span data-ttu-id="637c0-103">Bokföra försäljning</span><span class="sxs-lookup"><span data-stu-id="637c0-103">Posting Sales</span></span>
<span data-ttu-id="637c0-104">I **Bokföringsgrupp** i ett försäljningsdokument kan du välja mellan följande bokföringsfunktioner:</span><span class="sxs-lookup"><span data-stu-id="637c0-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="637c0-105">**Bokföra**</span><span class="sxs-lookup"><span data-stu-id="637c0-105">**Post**</span></span>
* <span data-ttu-id="637c0-106">**Testa rapport**</span><span class="sxs-lookup"><span data-stu-id="637c0-106">**Test Report**</span></span>
* <span data-ttu-id="637c0-107">**Bokför och skicka**</span><span class="sxs-lookup"><span data-stu-id="637c0-107">**Post and Send**</span></span>
* <span data-ttu-id="637c0-108">**Bokför och skriv ut**</span><span class="sxs-lookup"><span data-stu-id="637c0-108">**Post and Print**</span></span>
* <span data-ttu-id="637c0-109">**Bokför och e-posta**</span><span class="sxs-lookup"><span data-stu-id="637c0-109">**Post and Email**</span></span>
* <span data-ttu-id="637c0-110">**Bokför batch-jobb**</span><span class="sxs-lookup"><span data-stu-id="637c0-110">**Post Batch**</span></span>
* <span data-ttu-id="637c0-111">**Förhandsgranska bokföring**</span><span class="sxs-lookup"><span data-stu-id="637c0-111">**Preview Posting**</span></span>

<span data-ttu-id="637c0-112">När du har fyllt i alla raderna och skrivit in all information på försäljningsordern kan du bokföra den.</span><span class="sxs-lookup"><span data-stu-id="637c0-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="637c0-113">Här skapas en leverans och en faktura.</span><span class="sxs-lookup"><span data-stu-id="637c0-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="637c0-114">När en försäljningsorder bokförs, uppdateras kundens konto, redovisningen och artikeltransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="637c0-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="637c0-115">För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="637c0-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="637c0-116">Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="637c0-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="637c0-117">Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet.</span><span class="sxs-lookup"><span data-stu-id="637c0-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="637c0-118">Huruvida rabattransaktionen bokförs eller inte beror på innehållet i fältet **Rabattbokföring** i fönstret **Försäljningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="637c0-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="637c0-119">För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto).</span><span class="sxs-lookup"><span data-stu-id="637c0-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="637c0-120">Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.</span><span class="sxs-lookup"><span data-stu-id="637c0-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="637c0-121">När du bokför en order kan du skapa både en utleverans och en faktura.</span><span class="sxs-lookup"><span data-stu-id="637c0-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="637c0-122">Detta kan göras samtidigt eller oberoende av varandra.</span><span class="sxs-lookup"><span data-stu-id="637c0-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="637c0-123">Du kan också skapa en delutleverans och en delfaktura genom att fylla i fältet **Ant. att utleverera** och **Ant. att fakturera** på de enskilda försäljningsorderraderna innan du bokför.</span><span class="sxs-lookup"><span data-stu-id="637c0-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="637c0-124">Observera att du inte kan skapa en faktura för något som inte har utlevererats.</span><span class="sxs-lookup"><span data-stu-id="637c0-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="637c0-125">D.v.s. innan du kan fakturera måste du ha registrerat en leverans alternativt välja att leverera och fakturera samtidigt.</span><span class="sxs-lookup"><span data-stu-id="637c0-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="637c0-126">När bokföringen är slutförd tas de bokförda försäljningsraderna bort från ordern.</span><span class="sxs-lookup"><span data-stu-id="637c0-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="637c0-127">Du får ett meddelande när bokföringen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="637c0-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="637c0-128">Sedan kan du se de bokförda transaktionerna i de olika fönstren som innehåller bokförda transaktioner, t.ex. fönsterna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktion**, **Bokförda försäljningsutleveranser** och **Bokförda försäljningsfakturor**.</span><span class="sxs-lookup"><span data-stu-id="637c0-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="637c0-129">Se även</span><span class="sxs-lookup"><span data-stu-id="637c0-129">See Also</span></span>
[<span data-ttu-id="637c0-130">Försäljning</span><span class="sxs-lookup"><span data-stu-id="637c0-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="637c0-131">Så här skickar du dokument som e-post</span><span class="sxs-lookup"><span data-stu-id="637c0-131">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="637c0-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="637c0-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>



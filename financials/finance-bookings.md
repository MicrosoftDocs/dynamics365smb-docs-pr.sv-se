---
title: Fakturera din bokningar i Dynamics 365 | Microsoft Docs
description: "Lär dig hur du bulkfakturerar från Microsoft Bookings i Dynamics 365 Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 154a4719cdd0e28280c5b0a5de85479beb0b9262
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="e4cfd-103">Bulkfakturering för Microsoft Bookings i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4cfd-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="e4cfd-104">Om företaget använder appen Bookings i Office 365  kan du göra bulkfakturering för avtalade tider.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="e4cfd-105">SIdan **Ofakturerade bokningar** i [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller en lista över företagets slutförda bokningar.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="e4cfd-106">Du kan snabbt markera avtalade tider som du vill fakturera och skapa fakturor för utkast för tjänsterna på den här sidan.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="e4cfd-107">Anslut till Bookings</span><span class="sxs-lookup"><span data-stu-id="e4cfd-107">Connect to Bookings</span></span>
<span data-ttu-id="e4cfd-108">För att ansluta ditt [!INCLUDE[d365fin](includes/d365fin_md.md)] med Bookings, måste du ange ditt Bookings-företag, vad som ska synkroniseras med Bookings, hur ofta du vill synkronisera och vilka mallar du vill använda.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="e4cfd-109">Du kan ställa in informationen i den **Inställningar av Bookings-synkning** som du kan starta från sidan **Inställningar för Exchange-synkning** som du hittar genom [söka](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="e4cfd-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="e4cfd-110">Till exempel om du vill synkronisera kunder mellan Bookings och [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange standardmallen för att lägga till nya kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] baserat på kunder i ditt Bookings-företag.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="e4cfd-111">Fakturera möten</span><span class="sxs-lookup"><span data-stu-id="e4cfd-111">Invoice Appointments</span></span>
<span data-ttu-id="e4cfd-112">När det är dags att skicka fakturor för slutförda bokningar kan du gå till sidan **Ofakturerade bokningar**.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="e4cfd-113">Beroende på hur ofta informationen är synkroniserad, är listan lång eller kort.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="e4cfd-114">Du kan skapa fakturor för alla bokningar i listan eller en bokning i taget.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="e4cfd-115">Du kan markera en eller flera poster i listan och fakturera sådana.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="e4cfd-116">Stöd för faktureringsmöten från Bookings är enklare än det fullständiga arbetsflödet för att arbeta med offerter, försäljningsorder och försäljningsfakturor.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="e4cfd-117">Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="e4cfd-117">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="e4cfd-118">Du kan välja att sälja tjänsterna med hjälp av [!INCLUDE[d365fin](includes/d365fin_md.md)] eller använda Bookings, beroende på dina behov.</span><span class="sxs-lookup"><span data-stu-id="e4cfd-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4cfd-119">Se även</span><span class="sxs-lookup"><span data-stu-id="e4cfd-119">See Also</span></span>
[<span data-ttu-id="e4cfd-120">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="e4cfd-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="e4cfd-121">Så här fakturerar du försäljning</span><span class="sxs-lookup"><span data-stu-id="e4cfd-121">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="e4cfd-122">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="e4cfd-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="e4cfd-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="e4cfd-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  


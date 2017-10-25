---
title: "Så här skapar du kontantkunder | Microsoft Docs"
description: "Det här avsnittet beskriver hur du skapar en kund som betalar kontant."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6826c574bf63de70d76a29b45968c68c0b2e2d1f
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cash-customers"></a><span data-ttu-id="4e866-103">Så här skapar du kontantkunder</span><span class="sxs-lookup"><span data-stu-id="4e866-103">How to: Set Up Cash Customers</span></span>
<span data-ttu-id="4e866-104">Det går inte att skapa fakturor utan kundnummer.</span><span class="sxs-lookup"><span data-stu-id="4e866-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="4e866-105">Det gäller även vid kontantförsäljning då det inte finns något att registrera på kundkonton.</span><span class="sxs-lookup"><span data-stu-id="4e866-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="4e866-106">Så här skapar du en kontantkund</span><span class="sxs-lookup"><span data-stu-id="4e866-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="4e866-107">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kund** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="4e866-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4e866-108">Skapa ett nytt kort för **Kund**.</span><span class="sxs-lookup"><span data-stu-id="4e866-108">Create a new **Customer** card.</span></span> <span data-ttu-id="4e866-109">Mer information finns i [Så här registrerar du nya kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="4e866-109">For more information, see [How to: Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="4e866-110">I fältet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4e866-110">In the **No.**</span></span> <span data-ttu-id="4e866-111">ange t.ex. **Kassa**.</span><span class="sxs-lookup"><span data-stu-id="4e866-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="4e866-112">Skriv till exempel **Kontanförsäljning** i fältet **Namn**.</span><span class="sxs-lookup"><span data-stu-id="4e866-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="4e866-113">I snabbfliken **Fakturering** fyller du i fälten **Kundbokföringsmall** och **Gen. rörelsebokföringsmall**.</span><span class="sxs-lookup"><span data-stu-id="4e866-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="4e866-114">Nu har du skapat en kund som innehåller tillräckliga uppgifter för fakturering.</span><span class="sxs-lookup"><span data-stu-id="4e866-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4e866-115">Du har kanske valt en bokföringsmall som också används vid inhemsk kreditförsäljning.</span><span class="sxs-lookup"><span data-stu-id="4e866-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="4e866-116">Om du vill underhålla särskilda data om kontantförsäljning, t.ex. genom särskilda konton för försäljning eller kundkrediter, kan du skapa en extra bokföringsmall för detta ändamål.</span><span class="sxs-lookup"><span data-stu-id="4e866-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="4e866-117">Du måste ange ett nummer i bokföringsmallen för kundkreditkontot, även om saldot på detta alltid kommer att vara 0 när du har bokfört fakturor.</span><span class="sxs-lookup"><span data-stu-id="4e866-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4e866-118">Se även</span><span class="sxs-lookup"><span data-stu-id="4e866-118">See Also</span></span>
[<span data-ttu-id="4e866-119">Hantera kundreskontra</span><span class="sxs-lookup"><span data-stu-id="4e866-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="4e866-120">[Så här registrerar du nya kunder](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="4e866-120">[How to: Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="4e866-121">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="4e866-121">Finance</span></span>](finance.md)  



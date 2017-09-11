---
title: "Skapa en kund eller leverantör från en kontakt | Microsoft Docs"
description: "Du kan registrera en befintlig kontakt som en kund, leverantör eller bankkonto med befintliga data och ange en affärsrelation."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 142c1649438ad31b604767d6b6f35a1caeb3f9e4
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="bf424-103">Så här: Skapa en kund, leverantör eller bankkonto från en kontakt</span><span class="sxs-lookup"><span data-stu-id="bf424-103">How to: Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="bf424-104">Du vill kanske registrera några av dina befintliga kontakter som kunder, leverantörer eller bankkonton.</span><span class="sxs-lookup"><span data-stu-id="bf424-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="bf424-105">Skapa en kund, en leverantör eller ett bankkonto från en kontakt låter dig använda befintliga data.</span><span class="sxs-lookup"><span data-stu-id="bf424-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="bf424-106">När du skapar en kund, leverantör eller ett bankkonto på detta sätt, synkroniseras den med kontakten.</span><span class="sxs-lookup"><span data-stu-id="bf424-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="bf424-107">Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.</span><span class="sxs-lookup"><span data-stu-id="bf424-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="bf424-108">Innan du kan registrera kontakterna på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer i fönstret **Marknadsföringsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="bf424-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="bf424-109">Om du vill registrera kontakter som bankkonton måste du även ange nummerserien för bankkonton i fönstret **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="bf424-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="bf424-110">Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här</span><span class="sxs-lookup"><span data-stu-id="bf424-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="bf424-111">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontakter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="bf424-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="bf424-112">Välj kontakten du vill skapa som en kund, en leverantör eller ett bankkonto.</span><span class="sxs-lookup"><span data-stu-id="bf424-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="bf424-113">Välj åtgärden **Skapa som** och välj sedan antingen **Kund**, **Leverantör** eller **Bank**.</span><span class="sxs-lookup"><span data-stu-id="bf424-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="bf424-114">Bekräfta det följande meddelandet.</span><span class="sxs-lookup"><span data-stu-id="bf424-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="bf424-115">Kontaktinformationen överförs från kortet **Kontakt** kortet **Bankkonto**, **Kund** eller **Leverantörens**.</span><span class="sxs-lookup"><span data-stu-id="bf424-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="bf424-116">Du kanske vill lägga till specifik information på varje kort, t.ex fakturering och betalningsinformation.</span><span class="sxs-lookup"><span data-stu-id="bf424-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf424-117">Se även</span><span class="sxs-lookup"><span data-stu-id="bf424-117">See Also</span></span>
[<span data-ttu-id="bf424-118">Så här skapar du kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="bf424-118">How to: Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="bf424-119">Så här skapar du kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="bf424-119">How to: Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="bf424-120">Ställa in Kundhantering</span><span class="sxs-lookup"><span data-stu-id="bf424-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="bf424-121">Synkronisera kontakter med kunder, leverantörer och bankkonton</span><span class="sxs-lookup"><span data-stu-id="bf424-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="bf424-122">Så här länkar du kontakter med befintliga kunder, leverantörer och bankkonton</span><span class="sxs-lookup"><span data-stu-id="bf424-122">How to: Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="bf424-123">Så här tilldelar du affärsrelationer till kontakter</span><span class="sxs-lookup"><span data-stu-id="bf424-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="bf424-124">Arbeta med Financials</span><span class="sxs-lookup"><span data-stu-id="bf424-124">Working with Financials</span></span>](ui-work-product.md)


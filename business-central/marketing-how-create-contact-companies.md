---
title: "Skapa kontaktföretag | Microsoft Docs"
description: "Beskriver hur du skapar en kontakt för varje nytt företag eller potentiellt företag som du interagerar med eller har en relation med."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 932ae29ff302390962bf9ca4dc48d2d76fce1ca2
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="5309a-103">Skapa kontaktföretag</span><span class="sxs-lookup"><span data-stu-id="5309a-103">Create Contact Companies</span></span>
<span data-ttu-id="5309a-104">Du kan skapa en kontakt för varje nytt företag som du har förbindelse med, till exempel kund, leverantör, spekulant, bank, jurist, konsult och så vidare.</span><span class="sxs-lookup"><span data-stu-id="5309a-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="5309a-105">Det finns två sätt att skapa en kontakt: från noll eller från en befintlig kund, leverantör eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="5309a-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="5309a-106">Innan du skapar en kontakt kan du kontrollera inställningarna på sidan **Affärsstödsinställning**.</span><span class="sxs-lookup"><span data-stu-id="5309a-106">Before creating a contact, you may want to check the settings on the **Marketing Setup** page.</span></span> <span data-ttu-id="5309a-107">Mer information finns i [Ställa in e-postmeddelanden](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="5309a-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="5309a-108">Skapa en företagskontakt från noll</span><span class="sxs-lookup"><span data-stu-id="5309a-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="5309a-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5309a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="5309a-110">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5309a-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="5309a-111">Skriv numret på den artikel som har beställts i fältet **Nr**.</span><span class="sxs-lookup"><span data-stu-id="5309a-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="5309a-112">Om du har definierat en nummerserie för kontakter på sidan **Affärsstödsinställning** kan du i stället trycka på Retur så anges nästa tillgängliga kontaktnummer automatiskt.</span><span class="sxs-lookup"><span data-stu-id="5309a-112">Alternatively, if you have set up a number series for contacts on the **Marketing Setup** page, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="5309a-113">Ange **Typ** till **Företag**.</span><span class="sxs-lookup"><span data-stu-id="5309a-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="5309a-114">Fyll i övriga fält enligt behov.</span><span class="sxs-lookup"><span data-stu-id="5309a-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="5309a-115">Skapa en företagskontakt från en kund, en leverantör eller ett bankkonto</span><span class="sxs-lookup"><span data-stu-id="5309a-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="5309a-116">Om du redan har lagt upp flera kunder, leverantörer eller bankkonton kan du skapa kontakter baserat på befintliga uppgifter.</span><span class="sxs-lookup"><span data-stu-id="5309a-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="5309a-117">När du skapar en kontakt på detta sätt, synkroniseras kontaktinformationen med kunden, leverantören eller bankkontotinformationen.</span><span class="sxs-lookup"><span data-stu-id="5309a-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5309a-118">Innan du kan skapa kontaktföretag på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer på sidan **Marknadsföringsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="5309a-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="5309a-119">Om du vill skapa kontakter från bankkonton måste du även ange nummerserien för bankkonton på sidan **Redovisningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="5309a-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts on the **General Ledger Setup** page.</span></span>

1. <span data-ttu-id="5309a-120">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), gå till ett av följande beroende på varifrån du vill skapa kontakter välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="5309a-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="5309a-121">**Skapa kontakter från kunder**</span><span class="sxs-lookup"><span data-stu-id="5309a-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="5309a-122">**Skapa kontakter från leverantörer**</span><span class="sxs-lookup"><span data-stu-id="5309a-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="5309a-123">**Skapa kontakter från bankkonton**</span><span class="sxs-lookup"><span data-stu-id="5309a-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="5309a-124">På batch-jobbsidan som öppnas i avsnittet **Kund**, **Leverantör** eller **Bankkonto** kan du ställa in filter om du endast vill skapa kontakter från vissa kunder, leverantörer eller bankkonton.</span><span class="sxs-lookup"><span data-stu-id="5309a-124">In the batch job page that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="5309a-125">Klicka på **OK** för att börja skapa kontakter.</span><span class="sxs-lookup"><span data-stu-id="5309a-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="5309a-126">Nästa kontaktnummer i nummerserien kopplas till de nya kontakterna.</span><span class="sxs-lookup"><span data-stu-id="5309a-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="5309a-127">De nyskapade kontakterna tilldelas den affärsrelation för leverantörer som angetts på sidan **Affärsstödsinställning**.</span><span class="sxs-lookup"><span data-stu-id="5309a-127">The business relation for vendors that is specified on the **Marketing Setup** page is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="5309a-128">Du kan också skapa en kund, en leverantör eller ett bankkonto från en kontakt.</span><span class="sxs-lookup"><span data-stu-id="5309a-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="5309a-129">Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto från en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="5309a-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5309a-130">Se även</span><span class="sxs-lookup"><span data-stu-id="5309a-130">See Also</span></span>
[<span data-ttu-id="5309a-131">Synkronisera kontakter med kunder, leverantörer och bankkonton</span><span class="sxs-lookup"><span data-stu-id="5309a-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="5309a-132">Så här tilldelar du affärsrelationer till kontakter</span><span class="sxs-lookup"><span data-stu-id="5309a-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="5309a-133">Så här tilldelar du industrigrupper till en kontakt</span><span class="sxs-lookup"><span data-stu-id="5309a-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="5309a-134">Tilldela utskicksgrupp till en kontakt</span><span class="sxs-lookup"><span data-stu-id="5309a-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="5309a-135">Skapa kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="5309a-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="5309a-136">Arbeta med Business Central</span><span class="sxs-lookup"><span data-stu-id="5309a-136">Working with Business Central</span></span>](ui-work-product.md)


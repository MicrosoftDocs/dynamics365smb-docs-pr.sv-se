---
title: "Synkronisera kontakter med kunder och leverantörer | Microsoft Docs"
description: "Du kan koppla eller synkronisera kontaktinformation för kontakter som också är kunder, leverantörer eller bankkonton, så att du bara uppdaterar informationen på ett ställe."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2018
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 736d1329b3d3c2e9367972c2a2fb9e2af0080c85
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="3bf1e-103">Synkronisera kontakter med kunder, leverantörer och bankkonton</span><span class="sxs-lookup"><span data-stu-id="3bf1e-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="3bf1e-104">Om några av kontakterna också är kund-, leverantörs- och/eller bankkonton kan du synkronisera deras kontaktinformation med relaterade kund-, leverantörs- och bankkonton.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="3bf1e-105">Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

<span data-ttu-id="3bf1e-106">Innan du kan synkronisera kontakterna med kund-, leverantörs- och/eller bankkonton måste du ange en affärsrelationskod för dessa på sidan **Marknadsföringsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-106">Before you can synchronize your contacts with customers, vendors, or bank accounts, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="3bf1e-107">Mer information finns i [Ställa in e-postmeddelanden](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="3bf1e-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="3bf1e-108">Olika sätt att synkronisera kontakter med kunder, leverantörer och bankkonton</span><span class="sxs-lookup"><span data-stu-id="3bf1e-108">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="3bf1e-109">Du kan synkronisera kontakterna med kunder, leverantörer eller bankkonton på tre olika sätt:</span><span class="sxs-lookup"><span data-stu-id="3bf1e-109">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="3bf1e-110">Länka kontakterna till befintliga kunder, leverantörer eller bankkonton från kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-110">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="3bf1e-111">Mer information finns i [Länka kontakter med kunder, leverantörer och bankkonton](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="3bf1e-111">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="3bf1e-112">Skapa kunder, leverantörer och bankkonton från kontakten.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-112">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="3bf1e-113">Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto från en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="3bf1e-113">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="3bf1e-114">Skapa kontakter från kunder, leverantörer eller bankkonton.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-114">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="3bf1e-115">Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="3bf1e-115">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="3bf1e-116">Konsekvenser för synkroniseringen</span><span class="sxs-lookup"><span data-stu-id="3bf1e-116">Consequences of Synchronization</span></span>
<span data-ttu-id="3bf1e-117">När kontaken har synkroniserats med kund-, leverantörs- eller bankkontot:</span><span class="sxs-lookup"><span data-stu-id="3bf1e-117">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="3bf1e-118">Du behöver bara uppdatera uppgifterna på ett ställe.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-118">You only have to update information in one place.</span></span> <span data-ttu-id="3bf1e-119">Om du till exempel ändrar telefonnumret på kontakten uppdateras telefonnumret med samma ändring på kund-, leverantörs- eller bankkontot.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-119">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="3bf1e-120">Om du har angett nummerserie för kontakter när du skapar kund-, leverantörs- eller bankkontokort, skapas automatiskt ett kontaktkort för kunder, leverantörer eller bankkonton.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-120">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="3bf1e-121">Du kan skapa förs.offerter och försäljningsorder, inköpsofferter och inköpsorder från kontakten.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-121">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="3bf1e-122">Dina interaktioner kan registreras när du utför vissa åtgärder som att skriva ut order eller avropsorder, skapa försäljningsserviceorder, skicka e-post osv.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-122">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="3bf1e-123">Om du raderar en kontakt som är länkad till en kund, leverantör eller bank är det bara kontakten som tas bort från programmet.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-123">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="3bf1e-124">Kunden, leverantören eller bankkontot återstår.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-124">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="3bf1e-125">Om du raderar en kontakt som är länkad till en kund, leverantör eller ett bankkonto är det bara kontakten som återstår.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-125">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="3bf1e-126">Vissa detaljer, t.ex fakturering och bokföringsdetaljer, visas inte på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-126">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="3bf1e-127">Följaktligen kan du behöva lägga till dem manuellt på kund-, leverantörs- och bankkontokort, när du skapar kontakter som kunder, leverantörer eller bankkonton.</span><span class="sxs-lookup"><span data-stu-id="3bf1e-127">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bf1e-128">Se även</span><span class="sxs-lookup"><span data-stu-id="3bf1e-128">See Also</span></span>
[<span data-ttu-id="3bf1e-129">Hantera kontakter</span><span class="sxs-lookup"><span data-stu-id="3bf1e-129">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="3bf1e-130">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3bf1e-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


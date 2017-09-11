---
title: "Sår här: Ställ in tillägget GetAddress.io för postnummer i Storbritannien | Microsoft Docs"
description: "Beskriver de allmänna funktionerna som du använder för att arbeta med data i Financials, ange värden, sortera data och ändra vyer."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: sv-se
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="1ce31-103">Så här: Ställ in tillägget GetAddress.io för postnummer i Storbritannien</span><span class="sxs-lookup"><span data-stu-id="1ce31-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="1ce31-104">Det här tillägget gör det enkelt att ange adresser i Storbritannien för enheter som kunder, kontakter, anställda, leverantörer, bankkonton och så vidare.</span><span class="sxs-lookup"><span data-stu-id="1ce31-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="1ce31-105">Tillägget GetAddress.io för postnummer i Storbritannien använder getAddress API för att hitta adresser i postnummer i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="1ce31-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="1ce31-106">Om du vill använda tillägget, måste du ha en plan och en API-nyckel för för getAddress API.</span><span class="sxs-lookup"><span data-stu-id="1ce31-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="1ce31-107">Det är enkelt och vi hjälper dig att göra detta när du ställer in tillägget GetAddress.io för postnummer i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="1ce31-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="1ce31-108">Planer baseras på användning eller vilka som ibland kallas samtal.</span><span class="sxs-lookup"><span data-stu-id="1ce31-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="1ce31-109">Ett samtal är i detta fall när [!INCLUDE[d365fin](includes/d365fin_md.md)] visar en lista med adresser i ett postnummer.</span><span class="sxs-lookup"><span data-stu-id="1ce31-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="1ce31-110">Välj det schema som passar dig bäst beroende på hur ofta du vill lägga till adresser.</span><span class="sxs-lookup"><span data-stu-id="1ce31-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="1ce31-111">Om du väljer **få API-nyckel** på sidan ska du använda planen **gratis** som låter dig lägga till 20 adresser per dag och är endast giltig i 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="1ce31-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="1ce31-112">Ställ in tillägget GetAddress.io för postnummer i Storbritannien</span><span class="sxs-lookup"><span data-stu-id="1ce31-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="1ce31-113">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anslutningar till tjänst** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="1ce31-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1ce31-114">I fönstret **Anslutningar till tjänst** väljer du **Storbritannien postnummertjänst**.</span><span class="sxs-lookup"><span data-stu-id="1ce31-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="1ce31-115">På sidan **Postnummerproviderkonfiguration** väljer du **inaktiverad**.</span><span class="sxs-lookup"><span data-stu-id="1ce31-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="1ce31-116">I fönstret **Val av postnummertjänst** väljer du **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="1ce31-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="1ce31-117">I fönstret **GetAddress.io konfiguration** väljer du **hämta API-nyckeln** för att öppna sidan **planer** på webbplatsen för getAddress API.</span><span class="sxs-lookup"><span data-stu-id="1ce31-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="1ce31-118">Du kanske måste tillåta popup-fönster i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="1ce31-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="1ce31-119">Köp en plan eller välj **få API-nyckeln**, och ange din e-postadress.</span><span class="sxs-lookup"><span data-stu-id="1ce31-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="1ce31-120">Öppna e-postmeddelandet från getAddress.io och kopiera API-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="1ce31-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="1ce31-121">Nyckeln är under rubriken **din API-nyckel**.</span><span class="sxs-lookup"><span data-stu-id="1ce31-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="1ce31-122">I fönstret **GetAddress.io konfig** klistrar du in API-nyckel i fältet **API-nyckel** och väljer sedan **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ce31-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="1ce31-123">På sidan **Tjänstanslutningar** kontrollerar du att fältet **adressleverantör** visar **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="1ce31-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="1ce31-124">Om det gör detta är tjänsten aktiverad.</span><span class="sxs-lookup"><span data-stu-id="1ce31-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ce31-125">Se även</span><span class="sxs-lookup"><span data-stu-id="1ce31-125">See Also</span></span>
<span data-ttu-id="1ce31-126">[GetAddress.io brittiska postnr](ui-extensions-getaddressio.md)
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1ce31-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="1ce31-127">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ce31-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

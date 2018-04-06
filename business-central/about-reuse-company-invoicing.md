---
title: "Använd Invoicing och Business Central | Microsoft Docs"
description: "Lösning för att komma åt Microsoft Invoicing när du har registrerat dig för Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7c23fdd29b8fa4da0d5eb4d86e244bd847e9e9fb
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="fb1f5-103">Använda samma Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] och Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="fb1f5-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="fb1f5-104">När du registrerar dig för en provversion av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fb1f5-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fb1f5-105">Om du loggar in i Office-portalen kommer du i samtliga fall att se en flik som heter **Business center** och klicka på den.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="fb1f5-106">Detta ingår i Office 365 Business Premium-prenumerationen, så det är inte alla som får se fliken i Office-Portalen.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="fb1f5-107">Om du öppnar Business center visas avsnittet **Invoicing**.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="fb1f5-108">Om du öppnar detta avsnitt visas ett meddelande om att du inte har åtkomst till Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fb1f5-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="fb1f5-109">Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="fb1f5-110">Lösning</span><span class="sxs-lookup"><span data-stu-id="fb1f5-110">Workaround</span></span>
<span data-ttu-id="fb1f5-111">Invoicing och [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delad plattform.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="fb1f5-112">Det innebär att du identifieras som en befintlig användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du klickar på Invoicing i Business center.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="fb1f5-113">Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fb1f5-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="fb1f5-114">Du måste därför logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] och döpa om ditt befintliga företag och sedan skapa ett nytt företag som du kan använda i Invoicing.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="fb1f5-115">Inga data flyttas eller skrivs över i samband med denna lösning.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="fb1f5-116">Byta namn på ditt företag</span><span class="sxs-lookup"><span data-stu-id="fb1f5-116">To rename your company</span></span>
1.  <span data-ttu-id="fb1f5-117">Logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fb1f5-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="fb1f5-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Företag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="fb1f5-119">I fönstret **Företag** väljer du knappen **Redigera lista**.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="fb1f5-120">Byt namn på posten *Mitt företag* till något annat.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="fb1f5-121">Vänta några minuter.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-121">Wait a number of minutes.</span></span> <span data-ttu-id="fb1f5-122">Vi kommer att genomföra ett antal ändringar i den underliggande databasen, och det tar ett tag.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="fb1f5-123">När systemet är redo igen väljer du knappen **Skapa nytt företag**.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="fb1f5-124">I dialogrutan som visas anger du namnet som *Mitt företag* och väljer sedan alternativet **Produktion – endast konfigurationsdata**.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="fb1f5-125">Detta tar återigen några minuter.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-125">This again takes a number of minutes.</span></span> <span data-ttu-id="fb1f5-126">När processen är klar kommer du att få åtkomst till Invoicing som en del av din Office 365 Business Premium-upplevelse.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="fb1f5-127">Om mina data</span><span class="sxs-lookup"><span data-stu-id="fb1f5-127">What about my data?</span></span>
<span data-ttu-id="fb1f5-128">När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-data om, men själva informationen ändras inte.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="fb1f5-129">Om du använder såväl Invoicing som [!INCLUDE[d365fin](includes/d365fin_md.md)] lagras datan i två olika behållare (de två företagen).</span><span class="sxs-lookup"><span data-stu-id="fb1f5-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="fb1f5-130">Inget delas, så du måste hantera kunder och artiklar i båda företagen.</span><span class="sxs-lookup"><span data-stu-id="fb1f5-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb1f5-131">Se även</span><span class="sxs-lookup"><span data-stu-id="fb1f5-131">See Also</span></span>
[<span data-ttu-id="fb1f5-132">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="fb1f5-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="fb1f5-133">Installation och administration</span><span class="sxs-lookup"><span data-stu-id="fb1f5-133">Setup and Administration</span></span>](admin-setup-and-administration.md)  


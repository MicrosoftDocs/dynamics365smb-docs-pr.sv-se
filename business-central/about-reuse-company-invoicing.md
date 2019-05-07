---
title: Använd Invoicing och Business Central | Microsoft Docs
description: Lösning för att komma åt Microsoft Invoicing när du har registrerat dig för Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0173d64e140cfea91bf7f08d821c2d30cf0eb7b3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "911274"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="ca875-103">Använda samma Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] och Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="ca875-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="ca875-104">När du registrerar dig för en provversion av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ca875-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ca875-105">Om du loggar in i Office-portalen kommer du i samtliga fall att se en flik som heter **Microsoft Invoicing** och klicka på den.</span><span class="sxs-lookup"><span data-stu-id="ca875-105">In all cases, if you sign in to the Office Portal, you might see a tile called **Microsoft Invoicing** and click it.</span></span> <span data-ttu-id="ca875-106">Detta ingår i Office 365 Business Premium-prenumerationen, så det är inte alla som får se fliken i Office-Portalen.</span><span class="sxs-lookup"><span data-stu-id="ca875-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="ca875-107">Om du öppnar Microsoft Invoicing visas ett meddelande om att du inte har åtkomst till Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ca875-107">If you access Microsoft Invoicing, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="ca875-108">Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.</span><span class="sxs-lookup"><span data-stu-id="ca875-108">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="ca875-109">Lösning</span><span class="sxs-lookup"><span data-stu-id="ca875-109">Workaround</span></span>
<span data-ttu-id="ca875-110">Invoicing och [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delad plattform.</span><span class="sxs-lookup"><span data-stu-id="ca875-110">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="ca875-111">Det innebär att du identifieras som en befintlig användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du klickar på Fakturering i Office-portalen.</span><span class="sxs-lookup"><span data-stu-id="ca875-111">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Office Portal.</span></span> <span data-ttu-id="ca875-112">Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ca875-112">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="ca875-113">Du måste därför logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] och döpa om ditt befintliga företag och sedan skapa ett nytt företag som du kan använda i Fakturering.</span><span class="sxs-lookup"><span data-stu-id="ca875-113">So you will have to sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="ca875-114">Inga data flyttas eller skrivs över i samband med denna lösning.</span><span class="sxs-lookup"><span data-stu-id="ca875-114">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="ca875-115">Byta namn på ditt företag</span><span class="sxs-lookup"><span data-stu-id="ca875-115">To rename your company</span></span>
1. <span data-ttu-id="ca875-116">Logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ca875-116">Sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
2. <span data-ttu-id="ca875-117">I det övre högra hörnet väljer du ikonen **inställningar** ![inställningar](media/ui-experience/settings_icon_small.png "ikonen för inställningar för rollcenter"), och välj **Mina inställningar**.</span><span class="sxs-lookup"><span data-stu-id="ca875-117">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose **My Settings**.</span></span>
3. <span data-ttu-id="ca875-118">I fältet **företag** väljer du ett annat företag.</span><span class="sxs-lookup"><span data-stu-id="ca875-118">In the **Company** field, choose a different company.</span></span>
4. <span data-ttu-id="ca875-119">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Företag** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="ca875-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
5. <span data-ttu-id="ca875-120">På sidan **Företag** väljer du knappen **Redigera lista**.</span><span class="sxs-lookup"><span data-stu-id="ca875-120">On the **Companies** page, choose **Edit List**.</span></span>  
6. <span data-ttu-id="ca875-121">Byt namn på posten *Mitt företag* till något annat.</span><span class="sxs-lookup"><span data-stu-id="ca875-121">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="ca875-122">Vänta några minuter.</span><span class="sxs-lookup"><span data-stu-id="ca875-122">Wait a number of minutes.</span></span> <span data-ttu-id="ca875-123">Vi kommer att genomföra ett antal ändringar i den underliggande databasen, och det tar ett tag.</span><span class="sxs-lookup"><span data-stu-id="ca875-123">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
7.  <span data-ttu-id="ca875-124">När systemet är redo igen väljer du knappen **Skapa nytt företag**.</span><span class="sxs-lookup"><span data-stu-id="ca875-124">When the system is ready again, choose the **Create New Company** button.</span></span>  
8.  <span data-ttu-id="ca875-125">I dialogrutan som visas anger du namnet som *Mitt företag* och väljer sedan alternativet **Produktion – endast konfigurationsdata**.</span><span class="sxs-lookup"><span data-stu-id="ca875-125">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="ca875-126">Detta tar återigen några minuter.</span><span class="sxs-lookup"><span data-stu-id="ca875-126">This again takes a number of minutes.</span></span> <span data-ttu-id="ca875-127">När processen är klar kommer du att få åtkomst till Invoicing som en del av din Office 365 Business Premium-upplevelse.</span><span class="sxs-lookup"><span data-stu-id="ca875-127">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="ca875-128">Om mina data</span><span class="sxs-lookup"><span data-stu-id="ca875-128">What about my data?</span></span>
<span data-ttu-id="ca875-129">När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-data om, men själva informationen ändras inte.</span><span class="sxs-lookup"><span data-stu-id="ca875-129">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="ca875-130">Om du använder såväl Invoicing som [!INCLUDE[d365fin](includes/d365fin_md.md)] lagras datan i två olika behållare (de två företagen).</span><span class="sxs-lookup"><span data-stu-id="ca875-130">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="ca875-131">Inget delas, så du måste hantera kunder och artiklar i båda företagen.</span><span class="sxs-lookup"><span data-stu-id="ca875-131">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca875-132">Se även</span><span class="sxs-lookup"><span data-stu-id="ca875-132">See Also</span></span>
[<span data-ttu-id="ca875-133">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="ca875-133">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="ca875-134">Administration</span><span class="sxs-lookup"><span data-stu-id="ca875-134">Administration</span></span>](admin-setup-and-administration.md)  

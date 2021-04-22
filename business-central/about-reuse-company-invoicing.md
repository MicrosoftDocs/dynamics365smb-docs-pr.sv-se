---
title: Använd Invoicing och Business Central | Microsoft Docs
description: Lösning för att komma åt Microsoft Invoicing när du har registrerat dig för Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Microsoft 365
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 38d4a9be0c801d595ea390780296c7cb920fd003
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776353"
---
# <a name="using-the-same-microsoft-365-account-in-prod_short-and-microsoft-invoicing"></a><span data-ttu-id="62d67-103">Använda samma Microsoft 365-konto i [!INCLUDE[prod_short](includes/prod_long.md)] och Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="62d67-103">Using the same Microsoft 365 Account in [!INCLUDE[prod_short](includes/prod_long.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="62d67-104">När du registrerar dig för en testversion av [!INCLUDE[prod_short](includes/prod_short.md)] kan du byta till en 30 dagar lång utvärderingsfas, starta en prenumeration eller sluta använda [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62d67-104">When you sign up for a trial with [!INCLUDE[prod_short](includes/prod_short.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="62d67-105">Ibland kan det hända att du har sett något som kallas **Microsoft Invoicing** och klickat på den.</span><span class="sxs-lookup"><span data-stu-id="62d67-105">In all cases, you may at some point have seen something called **Microsoft Invoicing** and clicked it.</span></span> <span data-ttu-id="62d67-106">Det här var en app som ingick i Microsoft 365 Business Standard och tidigare kallades för Microsoft 365 Business Premium-prenumeration, så det är inte alla som har sett den panelen i sin Microsoft 365-upplevelse.</span><span class="sxs-lookup"><span data-stu-id="62d67-106">This was an app that was part of what is now Microsoft 365 Business Standard and was formerly known as Microsoft 365 Business Premium subscription, so not everyone will have seen that tile in their Microsoft 365 experience.</span></span>  

<span data-ttu-id="62d67-107">Microsoft Invoicing är inte längre tillgängligt, men om du behöver logga in på fakturering för att hämta data kanske du får ett meddelande om att du inte kan komma åt Microsoft Invoicing eftersom ditt konto används i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62d67-107">Microsoft Invoicing is no longer available, but if you need to sign into Invoicing to retrieve your data, you might see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="62d67-108">Ett liknande meddelande visas om du installerar det mobila programmet för Invoicing.</span><span class="sxs-lookup"><span data-stu-id="62d67-108">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="62d67-109">Lösning</span><span class="sxs-lookup"><span data-stu-id="62d67-109">Workaround</span></span>
<span data-ttu-id="62d67-110">Invoicing och [!INCLUDE[prod_short](includes/prod_short.md)] har en delad plattform.</span><span class="sxs-lookup"><span data-stu-id="62d67-110">Invoicing and [!INCLUDE[prod_short](includes/prod_short.md)] have a shared platform.</span></span> <span data-ttu-id="62d67-111">Det innebär att du identifieras som en befintlig användare i [!INCLUDE[prod_short](includes/prod_short.md)] när du klickar på fakturering i Microsoft 365 administratörscenter.</span><span class="sxs-lookup"><span data-stu-id="62d67-111">That means that you are recognized as an existing user of [!INCLUDE[prod_short](includes/prod_short.md)] when you click Invoicing in the Microsoft 365 admin center.</span></span> <span data-ttu-id="62d67-112">Det beror på att Invoicing inte kan använda samma företag som [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62d67-112">The reason is that Invoicing cannot use the same company as [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="62d67-113">Du måste därför logga in på [!INCLUDE[prod_short](includes/prod_short.md)] och döpa om ditt befintliga företag och sedan skapa ett nytt företag som du kan använda i Fakturering.</span><span class="sxs-lookup"><span data-stu-id="62d67-113">So you will have to sign in to [!INCLUDE[prod_short](includes/prod_short.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="62d67-114">Inga data flyttas eller skrivs över i samband med denna lösning.</span><span class="sxs-lookup"><span data-stu-id="62d67-114">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="62d67-115">Byta namn på ditt företag</span><span class="sxs-lookup"><span data-stu-id="62d67-115">To rename your company</span></span>
1. <span data-ttu-id="62d67-116">Logga in på [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62d67-116">Sign in to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
2. <span data-ttu-id="62d67-117">I det övre högra hörnet väljer du ikonen **Inställningar** ![Inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan **Mina inställningar**.</span><span class="sxs-lookup"><span data-stu-id="62d67-117">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose **My Settings**.</span></span>
3. <span data-ttu-id="62d67-118">I fältet **företag** väljer du ett annat företag.</span><span class="sxs-lookup"><span data-stu-id="62d67-118">In the **Company** field, choose a different company.</span></span>
4. <span data-ttu-id="62d67-119">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Företag** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="62d67-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
5. <span data-ttu-id="62d67-120">På sidan **Företag** väljer du knappen **Redigera lista**.</span><span class="sxs-lookup"><span data-stu-id="62d67-120">On the **Companies** page, choose **Edit List**.</span></span>  
6. <span data-ttu-id="62d67-121">Byt namn på posten *Mitt företag* till något annat.</span><span class="sxs-lookup"><span data-stu-id="62d67-121">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="62d67-122">Vänta några minuter.</span><span class="sxs-lookup"><span data-stu-id="62d67-122">Wait a number of minutes.</span></span> <span data-ttu-id="62d67-123">Vi kommer att genomföra ett antal ändringar i den underliggande databasen, och det tar ett tag.</span><span class="sxs-lookup"><span data-stu-id="62d67-123">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
7.  <span data-ttu-id="62d67-124">När systemet är redo igen väljer du knappen **Skapa nytt företag**.</span><span class="sxs-lookup"><span data-stu-id="62d67-124">When the system is ready again, choose the **Create New Company** button.</span></span>  
8.  <span data-ttu-id="62d67-125">I dialogrutan som visas anger du namnet som *Mitt företag* och väljer sedan alternativet **Produktion – endast konfigurationsdata**.</span><span class="sxs-lookup"><span data-stu-id="62d67-125">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="62d67-126">Detta tar återigen några minuter.</span><span class="sxs-lookup"><span data-stu-id="62d67-126">This again takes a number of minutes.</span></span> <span data-ttu-id="62d67-127">När processen är klar kommer du att få åtkomst till Invoicing som en del av din Microsoft 365 Business Standard-upplevelse.</span><span class="sxs-lookup"><span data-stu-id="62d67-127">When the process completes, you will be able to access Invoicing as part of your Microsoft 365 Business Standard experience.</span></span> <span data-ttu-id="62d67-128">Men endast för export av data eftersom faktureringsprogrammet är föråldrat.</span><span class="sxs-lookup"><span data-stu-id="62d67-128">but only to export data since the Invoicing app is deprecated.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="62d67-129">Om mina data</span><span class="sxs-lookup"><span data-stu-id="62d67-129">What about my data?</span></span>
<span data-ttu-id="62d67-130">När du byter namn på det ursprungliga Mitt företag döps de databastabeller som lagrar dina befintliga [!INCLUDE[prod_short](includes/prod_short.md)]-data om, men själva informationen ändras inte.</span><span class="sxs-lookup"><span data-stu-id="62d67-130">When you rename the original My Company, the database tables that store your existing [!INCLUDE[prod_short](includes/prod_short.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="62d67-131">Om du använder såväl Invoicing som [!INCLUDE[prod_short](includes/prod_short.md)] lagras datan i två olika behållare (de två företagen).</span><span class="sxs-lookup"><span data-stu-id="62d67-131">If you use both Invoicing and [!INCLUDE[prod_short](includes/prod_short.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="62d67-132">Inget delas, så du måste hantera kunder och artiklar i båda företagen.</span><span class="sxs-lookup"><span data-stu-id="62d67-132">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="62d67-133">Se även</span><span class="sxs-lookup"><span data-stu-id="62d67-133">See Also</span></span>
[<span data-ttu-id="62d67-134">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="62d67-134">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="62d67-135">Administration</span><span class="sxs-lookup"><span data-stu-id="62d67-135">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
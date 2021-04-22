---
title: Arbeta med Business Central-data i Microsoft Teams| Microsoft Docs
description: Lär dig att använda Business Central-appen för Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786888"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="6c4a1-103">Arbeta med Business Central-data i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6c4a1-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="6c4a1-104">[!INCLUDE [prod_short](includes/prod_short.md)] erbjuder en app som ansluter Microsoft Teams till dina affärsdata i [!INCLUDE [prod_short](includes/prod_short.md)], så att du snabbt kan dela information mellan teammedlemmar och reagera snabbare på frågor.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="6c4a1-105">I den här artikeln lär du dig hur du använder appen för att dela [!INCLUDE [prod_short](includes/prod_short.md)]-data med kollegor i en Team-konversation.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="6c4a1-106">Översikt</span><span class="sxs-lookup"><span data-stu-id="6c4a1-106">Overview</span></span>

<span data-ttu-id="6c4a1-107">I [!INCLUDE [prod_short](includes/prod_short.md)]-appen kan du:</span><span class="sxs-lookup"><span data-stu-id="6c4a1-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="6c4a1-108">Kopiera en länk till en Business Central-post och klistra in den i en Teams-konversation så att den kan delas med dina medarbetare.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="6c4a1-109">Appen kommer sedan att utöka länken till ett kompakt, interaktivt kort som visar information om posten.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="6c4a1-110">När ni väl befinner er i konversationen kan du och dina medarbetare visa mer information om posten, redigera data och vidta åtgärder &mdash; utan att lämna Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="6c4a1-111">[![Team-integrering med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6c4a1-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c4a1-112">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="6c4a1-112">Prerequisites</span></span>

- <span data-ttu-id="6c4a1-113">Du har tillgång till Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="6c4a1-114">Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Team.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="6c4a1-115">Mer information finns i [Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c4a1-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="6c4a1-116">Alla deltagare i en Team-konversation kommer att kunna se kort för Business Central-poster som du skickar till konversationen.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="6c4a1-117">Men för att visa mer information om poster med hjälp av knapparna **Detaljer** eller **Öppna** på ett kort, behöver de tillgång till [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4a1-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c4a1-118">Mer information finns i [Hantera Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="6c4a1-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="6c4a1-119">Ta med ett Business Central-kort i en Team-konversation</span><span class="sxs-lookup"><span data-stu-id="6c4a1-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="6c4a1-120">Logga in på [!INCLUDE [prod_short](includes/prod_short.md)] genom webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="6c4a1-121">Öppna posten som du vill dela.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="6c4a1-122">Appen är utformad för att visa sidor med korttypen från [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4a1-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c4a1-123">Öppna en sida som visar en enskild post, t. ex. en artikel, kund eller försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="6c4a1-124">Du kan inte använda den för rollcenter eller sidor som visar flera poster i en lista.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="6c4a1-125">Kopiera hela URL-adressen från webbläsarens adressfält.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopiera URL-adress för Business Central från webbläsare](media/teams-url-v2.png)
4. <span data-ttu-id="6c4a1-127">Gå till Team och starta en konversation, som kan vara chatt med en person, en grupp personer eller en teamkanal.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="6c4a1-128">Klistra in URL-adressen i meddelanderutan där du skriver ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Klistra in Business Central-URL i Team](media/teams-paste-url-v2.png)
6. <span data-ttu-id="6c4a1-130">Första gången du klistrar in en länk i en konversation ombeds du logga in på [!INCLUDE [prod_short](includes/prod_short.md)] och ge appen tillstånd att hämta data.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="6c4a1-131">Följ bara instruktionerna på skärmen.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c4a1-132">Du behöver bara utföra detta steg en enda gång.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="6c4a1-133">Vänta ett tag medan ett kort genereras i meddelanderutan.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="6c4a1-134">När kortet visas granskar du innehållet på kortet noggrant för känslig information innan du skickar meddelandet.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="6c4a1-135">Det här steget är viktigt eftersom alla i konversationen kan se kortet när du har skickat meddelandet.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="6c4a1-136">Om kortet verkar vara bra väljer du **Skicka** för att skicka det till konversationen.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="6c4a1-137">När kortet visas och innan du väljer **Skicka** kan du ta bort den inklistrade URL:en om du vill.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="6c4a1-138">Om du vill visa mer information om eller ändra den post somvisas på kortet väljer du **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="6c4a1-139">Mer information finns i nästa avsnitt.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="6c4a1-140">Visa kortinformation</span><span class="sxs-lookup"><span data-stu-id="6c4a1-140">View card details</span></span>

<span data-ttu-id="6c4a1-141">När ett kort har skickats till en konversation kan alla deltagare med [rätt behörighet](admin-teams-integration.md#permissions) välja **Detaljer** för att öppna ett fönster som visar mer information om posten &mdash; och eventuellt ändra posten.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="6c4a1-142">Det spelar ingen roll om du är den som skickar kortet eller den som tar emot det.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="6c4a1-143">Funktionen **Detaljer** är särskilt användbar för mottagare eftersom den snabbt förser dem med koncis, riktad information om posten, i stället för att behöva söka igenom hela posten.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="6c4a1-144">Fönstret Detaljer liknar det du ser i [!INCLUDE [prod_short](includes/prod_short.md)] posten.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="6c4a1-145">Men informationen är något nedtrimmad för Team.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="6c4a1-146">När du är klar med att visa och göra ändringar kan du stänga fönstret och återgå till Team-konversationen.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="6c4a1-147">Här följer några saker som du bör tänka på när du arbetar med kortinformationen:</span><span class="sxs-lookup"><span data-stu-id="6c4a1-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="6c4a1-148">För att kunna öppna kortinformationen måste en användare ha behörighet till sidan och dess data i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4a1-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="6c4a1-149">Korten i Teams-chattar uppdateras inte automatiskt till ändringar.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="6c4a1-150">Ändringar som du sparar i en post i informationsfönstret sparas i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4a1-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c4a1-151">Kortet i Teams visar emellertid inte ändringarna i konverteringen förrän du klistrar in länken igen.</span><span class="sxs-lookup"><span data-stu-id="6c4a1-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="6c4a1-152">Mer information om hur du arbetar med kort och kortinformation finns i [Vanliga frågor och svar om Teams](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="6c4a1-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c4a1-153">Se även</span><span class="sxs-lookup"><span data-stu-id="6c4a1-153">See Also</span></span>

[<span data-ttu-id="6c4a1-154">Översikt över Business Central- och Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="6c4a1-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="6c4a1-155">[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c4a1-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="6c4a1-156">Vanliga frågor och Svar om Teams</span><span class="sxs-lookup"><span data-stu-id="6c4a1-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="6c4a1-157">Felsöka Teams</span><span class="sxs-lookup"><span data-stu-id="6c4a1-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="6c4a1-158">Utveckling för Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="6c4a1-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
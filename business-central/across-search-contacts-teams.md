---
title: Söka efter kontakter från Microsoft Teams
description: Mer information om hur du upprättar Business Central kunder, leverantörer och andra kontakter från Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 77108cab69a05165616ad5e1a44f1a3ddc9d4cd9
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882503"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="56a7c-103">Söka efter kunder, leverantörer och andra kontakter från Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="56a7c-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="56a7c-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="56a7c-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="56a7c-105">Infört i 2021 utgivningscykel 1.</span><span class="sxs-lookup"><span data-stu-id="56a7c-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="56a7c-106">[!INCLUDE [prod_short](includes/prod_short.md)] har ett omfattande system för hantering av affärskontakt som är väsentligt för användare i försäljning, operationer eller andra avdelningsroller.</span><span class="sxs-lookup"><span data-stu-id="56a7c-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="56a7c-107">Om du är en användare i en av dessa roller behöver du ofta slå upp, möta eller starta en konversation med leverantörerna, kunderna och andra kontakter.</span><span class="sxs-lookup"><span data-stu-id="56a7c-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="56a7c-108">Med [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams kan du utföra de här uppgifterna direkt från Teams utan att behöva växla till [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="56a7c-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="56a7c-109">I Teams kan du:</span><span class="sxs-lookup"><span data-stu-id="56a7c-109">From within Teams, you can:</span></span>

- <span data-ttu-id="56a7c-110">Slå upp [!INCLUDE [prod_short](includes/prod_short.md)] kontakter från Teams-kommandorutan eller från meddelandeområdet.</span><span class="sxs-lookup"><span data-stu-id="56a7c-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="56a7c-111">Kontakter kan inkludera potentiella kunder, leverantörer, kunder eller andra affärsrelationer.</span><span class="sxs-lookup"><span data-stu-id="56a7c-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="56a7c-112">Dela en kontakt som ett kort i en Teams-konversation.</span><span class="sxs-lookup"><span data-stu-id="56a7c-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="56a7c-113">Visa information om kontaktinformation, interaktionshistorik och andra insikter som utestående betalningar eller öppna dokument.</span><span class="sxs-lookup"><span data-stu-id="56a7c-113">View details about contact information, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56a7c-114">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="56a7c-114">Prerequisites</span></span>

- <span data-ttu-id="56a7c-115">Du har tillgång till Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="56a7c-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="56a7c-116">Du har installerat [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Team.</span><span class="sxs-lookup"><span data-stu-id="56a7c-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="56a7c-117">Mer information finns i [Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="56a7c-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="56a7c-118">Du har ett [!INCLUDE [prod_short](includes/prod_short.md)]-konto som har tillgång till kontakter i minst ett företag.</span><span class="sxs-lookup"><span data-stu-id="56a7c-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="56a7c-119">Oavsett om du söker från kommandorutan eller meddelanderutan, kan du uppmanas att logga in eller ställa in appen första gången.</span><span class="sxs-lookup"><span data-stu-id="56a7c-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="56a7c-120">Det här steget måste du söka efter kontakter på rätt Business Central-företag.</span><span class="sxs-lookup"><span data-stu-id="56a7c-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="56a7c-121">Information om hur du ställer in appen för att välja företag finns i [ändra företag och andra inställningar i Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="56a7c-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="56a7c-122">Slå upp kontakter från kommandorutan</span><span class="sxs-lookup"><span data-stu-id="56a7c-122">Look up contacts from the command box</span></span>

<span data-ttu-id="56a7c-123">Kommandorutan visas högst upp på varje skärm i Teams.</span><span class="sxs-lookup"><span data-stu-id="56a7c-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="56a7c-124">Du kan söka, ta snabb åtgärder eller starta appar, som [!INCLUDE [prod_short](includes/prod_short.md)]-appen.</span><span class="sxs-lookup"><span data-stu-id="56a7c-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="56a7c-125">Sökning från kommandorutan är praktiskt när du snabbt vill söka efter kontakter och relaterade data för egen användning.</span><span class="sxs-lookup"><span data-stu-id="56a7c-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="56a7c-126">Anta att du vill slå upp en e-postadress till en leverantör för att skapa ett kalendermöte.</span><span class="sxs-lookup"><span data-stu-id="56a7c-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="56a7c-127">Eller kanske vill du slå upp interaktionshistorik under ett möte med en kund.</span><span class="sxs-lookup"><span data-stu-id="56a7c-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="56a7c-128">I kommandorutan, skriv **@Business Central** och välj sedan Business Central-appen från resultatet.</span><span class="sxs-lookup"><span data-stu-id="56a7c-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Öppna Business Central-app för att söka efter kontakter från kommandorutan](media/teams-contacts-command-1.png)

2. <span data-ttu-id="56a7c-130">I rutan **Business Central**, börja skriva söktext, som ett namn, adress eller telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="56a7c-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="56a7c-131">När du skriver visas matchande resultat.</span><span class="sxs-lookup"><span data-stu-id="56a7c-131">As you type, matching results will appear.</span></span>

    ![Sök Business Central-kontakter från Teams-kommandorutan](media/teams-contacts-command-2.png)
3. <span data-ttu-id="56a7c-133">Välj en kontakt från resultatet.</span><span class="sxs-lookup"><span data-stu-id="56a7c-133">Select a contact from the results.</span></span>

    <span data-ttu-id="56a7c-134">Kontaktkortet visas under kommandorutan.</span><span class="sxs-lookup"><span data-stu-id="56a7c-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="56a7c-135">Om du vill lägga till kontaktkortet i en konversation går du till det övre högra hörnet på kortet, väljer **... (Fler alternativ)** > **Kopierar**.</span><span class="sxs-lookup"><span data-stu-id="56a7c-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="56a7c-136">Klistra sedan in kopian i meddelanderutan i en konversation.</span><span class="sxs-lookup"><span data-stu-id="56a7c-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="56a7c-137">Mer allmän information om kommandorutan i Teams finns i [Teams - Använd kommandorutan](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="56a7c-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="56a7c-138">Slå upp kontakter från meddelanderutan</span><span class="sxs-lookup"><span data-stu-id="56a7c-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="56a7c-139">Fördelen med att använda meddelanderutan är att du kan lägga till ett kontaktkort direkt till en konversation så att andra kan se det.</span><span class="sxs-lookup"><span data-stu-id="56a7c-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="56a7c-140">Nedanför meddelandeskrivningen, välj ikonen **Business Central** för att starta appen.</span><span class="sxs-lookup"><span data-stu-id="56a7c-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="56a7c-141">Om du inte ser ikonen **Business Central**, välj **... (Meddelandenstillägg)**.</span><span class="sxs-lookup"><span data-stu-id="56a7c-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Öppna Business Central-app för att söka efter kontakter från meddelanderutan](media/teams-contacts-message-box.png)

2. <span data-ttu-id="56a7c-143">I rutan **Business Central**, börja skriva söktext, som ett namn, adress eller telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="56a7c-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="56a7c-144">När du skriver visas matchande resultat.</span><span class="sxs-lookup"><span data-stu-id="56a7c-144">As you type, matching results will appear.</span></span>

    ![Sök Business Central-kontakter från meddelanderutan](media/teams-contacts-5.png)
3. <span data-ttu-id="56a7c-146">Välj en kontakt från resultatet.</span><span class="sxs-lookup"><span data-stu-id="56a7c-146">Select a contact from the results.</span></span>

    <span data-ttu-id="56a7c-147">Kontaktkortet visas i meddelanderutan.</span><span class="sxs-lookup"><span data-stu-id="56a7c-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56a7c-148">Kontaktkortet skickas inte till konversationen direkt för andra att se.</span><span class="sxs-lookup"><span data-stu-id="56a7c-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="56a7c-149">Du har möjlighet att granska innehållet på kortet och lägga till text före eller efter det du vill.</span><span class="sxs-lookup"><span data-stu-id="56a7c-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="56a7c-150">Skicka sedan meddelandet till chatten när det är klart.</span><span class="sxs-lookup"><span data-stu-id="56a7c-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="56a7c-151">Det finns också ett annat sätt</span><span class="sxs-lookup"><span data-stu-id="56a7c-151">Here's another way</span></span>

1. <span data-ttu-id="56a7c-152">I stället för att använda **Business Central**-ikonen skriver du **@Business Central** direkt i meddelanderutan.</span><span class="sxs-lookup"><span data-stu-id="56a7c-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="56a7c-153">Ange dina söktermer i rutan.</span><span class="sxs-lookup"><span data-stu-id="56a7c-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="56a7c-154">Välj en kontakt med upp- och nedpilarna på tangentbordet och tryck sedan på retur.</span><span class="sxs-lookup"><span data-stu-id="56a7c-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="56a7c-155">Visa information om kontaktkort</span><span class="sxs-lookup"><span data-stu-id="56a7c-155">Viewing contact card details</span></span>

<span data-ttu-id="56a7c-156">Kontakt kortet i Teams ger dig en snabb överblick över kunden, leverantören eller kontakten.</span><span class="sxs-lookup"><span data-stu-id="56a7c-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="56a7c-157">Kortet är interaktivt &mdash;vilket innebär att du kan visa mer information eller till och med ändra en kontakt med hjälp av knapparna **Detaljer** eller **Öppna i nytt fönster**.</span><span class="sxs-lookup"><span data-stu-id="56a7c-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="56a7c-158">Knappen **Detaljer** öppnas ett fönster i Teams som visar mer information om kontakten, men inte så mycket som visas i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="56a7c-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="56a7c-159">Om du vill se all information om en kontakt i [!INCLUDE [prod_short](includes/prod_short.md)] väljer du **Öppna i nytt fönster**.</span><span class="sxs-lookup"><span data-stu-id="56a7c-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="56a7c-160">Kontaktkortet fungerar precis som kort för poster, t.ex. artiklar, kunder eller försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="56a7c-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="56a7c-161">Mer information om kort finns i [Visa kortdetaljer](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="56a7c-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="56a7c-162">Alla deltagare i en Team-konversation kommer att kunna se kort för Business Central-kontakt som du skickar till konversationen.</span><span class="sxs-lookup"><span data-stu-id="56a7c-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="56a7c-163">Men för att visa mer information om poster med hjälp av knapparna **Detaljer** eller **Öppna** på ett kort, behöver de tillgång till [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="56a7c-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="56a7c-164">Mer information finns i [Hantera Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="56a7c-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="56a7c-165">Se även</span><span class="sxs-lookup"><span data-stu-id="56a7c-165">See Also</span></span>

[<span data-ttu-id="56a7c-166">Översikt över Business Central- och Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="56a7c-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="56a7c-167">[Installera [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="56a7c-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="56a7c-168">Vanliga frågor och Svar om Teams</span><span class="sxs-lookup"><span data-stu-id="56a7c-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="56a7c-169">Felsöka Teams</span><span class="sxs-lookup"><span data-stu-id="56a7c-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="56a7c-170">Utveckling för Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="56a7c-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
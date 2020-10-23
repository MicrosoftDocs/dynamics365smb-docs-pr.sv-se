---
title: Ställa in e-postloggning | Microsoft Docs
description: Lär dig hur du kan omvandla e-postinteraktioner mellan säljare och kunder till verkliga affärsmöjligheter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923626"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="41041-103">Spåra utbyte av e-postmeddelanden mellan säljare och kontakter</span><span class="sxs-lookup"><span data-stu-id="41041-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="41041-104">Få ut mer av kommunikationen mellan säljare och dina befintliga eller potentiella kunder genom att följa upp e-postutbyten och sedan omvandla dem till olika affärsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="41041-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="41041-105">kan tillsammans med Exchange Online spara en logg över de inkommande och utgående meddelandena.</span><span class="sxs-lookup"><span data-stu-id="41041-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="41041-106">Du kan visa och analysera innehållet i varje meddelande på sidan **Interaktionslogg**.</span><span class="sxs-lookup"><span data-stu-id="41041-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="41041-107">Konfigurera gemensamma mappar och regler för e-postloggning i Exchange Online</span><span class="sxs-lookup"><span data-stu-id="41041-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="41041-108">Därefter ansluter du [!INCLUDE[prodshort](includes/prodshort.md)] med Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="41041-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="41041-109">Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)] för att logga e-postmeddelanden</span><span class="sxs-lookup"><span data-stu-id="41041-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="41041-110">Kom igång med e-postloggning i två enkla steg:</span><span class="sxs-lookup"><span data-stu-id="41041-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="41041-111">Anslut [!INCLUDE[d365fin](includes/d365fin_md.md)] till Exchange Online för din Microsoft 365-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="41041-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Microsoft 365 subscription.</span></span> <span data-ttu-id="41041-112">Exchange Online hanterar dina e-postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="41041-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="41041-113">Detta steg är enkelt att utföra med hjälp av en guide för assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="41041-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="41041-114">Du behöver bara ha administratörsbehörigheter för ditt administratörskonto i Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="41041-114">You just need your administrator credentials for your administrator account in Microsoft 365.</span></span> <span data-ttu-id="41041-115">Du startar guiden genom att gå till **Assisterad konfiguration** och sedan välja **Konfigurera e-postloggning**.</span><span class="sxs-lookup"><span data-stu-id="41041-115">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span>  

2. <span data-ttu-id="41041-116">Kontrollera att du har angett giltiga e-postadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] för dina säljare och kontakter, beroende på om de är potentiella eller befintliga kunder.</span><span class="sxs-lookup"><span data-stu-id="41041-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="41041-117">Det gör du genom att för varje kund eller säljare öppna kortet **Kontakt** eller **Säljare/Inköpare** och titta i fältet **E-post**.</span><span class="sxs-lookup"><span data-stu-id="41041-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="41041-118">När du har slutfört stegen i guiden kan du kontrollera om kopplingen har lyckats.</span><span class="sxs-lookup"><span data-stu-id="41041-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="41041-119">Sök efter **Marknadsföringsinställningar**, välj **Process**, sedan **Funktioner** och därefter **Validera konfiguration för e-postloggning**.</span><span class="sxs-lookup"><span data-stu-id="41041-119">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="41041-120">Visa e-postutbyten i interaktionsloggen</span><span class="sxs-lookup"><span data-stu-id="41041-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="41041-121">skapar en transaktion på sidan **Interaktionslogg** varje gång en säljare och en kontakt utbyter e-postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="41041-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="41041-122">Om du vill visa interaktionsloggen öppnar du kortet **Kontakt** eller **Säljare/Inköpare** för den personen och väljer sedan **Historik** och därefter **Interaktionslogg**.</span><span class="sxs-lookup"><span data-stu-id="41041-122">To view the interaction log, open the **Contact** or **Salesperson Purchaser** card for the person, and then choose **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="41041-123">Det finns några saker som du kan göra med posterna i loggen, till exempel:</span><span class="sxs-lookup"><span data-stu-id="41041-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="41041-124">Visa innehållet i e-postmeddelandet som utbytts genom att klicka på åtgärden **Visa bilagor**.</span><span class="sxs-lookup"><span data-stu-id="41041-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="41041-125">Omvandla ett e-postutbyte till en affärsmöjlighet - Om en transaktion verkar lovande kan du omvandla den till en affärsmöjlighet och sedan hantera förloppet fram till en försäljning.</span><span class="sxs-lookup"><span data-stu-id="41041-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="41041-126">Välj posten och välj sedan åtgärden **Skapa affärsmöjlighet**.</span><span class="sxs-lookup"><span data-stu-id="41041-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="41041-127">Mer information finns i [Hantera försäljningsmöjligheter](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="41041-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="41041-128">Se även</span><span class="sxs-lookup"><span data-stu-id="41041-128">See Also</span></span>
[<span data-ttu-id="41041-129">Hantera relationer</span><span class="sxs-lookup"><span data-stu-id="41041-129">Managing Relationships</span></span>](marketing-relationship-management.md)


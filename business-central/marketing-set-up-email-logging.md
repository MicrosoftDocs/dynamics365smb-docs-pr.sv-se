---
title: Ställa in e-postloggning | Microsoft Docs
description: Lär dig hur du kan omvandla e-postinteraktioner mellan säljare och kunder till verkliga affärsmöjligheter.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: e325cce98256b723c6fcfdf4d16068f852a2b032
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308746"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="54dab-103">Spåra utbyte av e-postmeddelanden mellan säljare och kontakter</span><span class="sxs-lookup"><span data-stu-id="54dab-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>
<span data-ttu-id="54dab-104">Få ut mer av kommunikationen mellan säljare och dina befintliga eller potentiella kunder genom att följa upp e-postutbyten och sedan omvandla dem till olika affärsmöjligheter.</span><span class="sxs-lookup"><span data-stu-id="54dab-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="54dab-105">kan tillsammans med Exchange Online spara en logg över de inkommande och utgående meddelandena.</span><span class="sxs-lookup"><span data-stu-id="54dab-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="54dab-106">Du kan visa och analysera innehållet i varje meddelande på sidan **Interaktionslogg**.</span><span class="sxs-lookup"><span data-stu-id="54dab-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a><span data-ttu-id="54dab-107">Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)] för att logga e-postmeddelanden</span><span class="sxs-lookup"><span data-stu-id="54dab-107">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>
<span data-ttu-id="54dab-108">Kom igång med e-postloggning i två enkla steg:</span><span class="sxs-lookup"><span data-stu-id="54dab-108">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="54dab-109">Anslut [!INCLUDE[d365fin](includes/d365fin_md.md)] till Exchange Online för din Office 365-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="54dab-109">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="54dab-110">Exchange Online hanterar dina e-postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="54dab-110">Exchange Online handles your email messages.</span></span> <span data-ttu-id="54dab-111">Detta steg är enkelt att utföra med hjälp av en guide för assisterad konfiguration.</span><span class="sxs-lookup"><span data-stu-id="54dab-111">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="54dab-112">Du behöver bara ha administratörsbehörigheter för ditt administratörskonto i Office 365.</span><span class="sxs-lookup"><span data-stu-id="54dab-112">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="54dab-113">Du startar guiden genom att gå till **Assisterad konfiguration** och sedan välja **Konfigurera e-postloggning**.</span><span class="sxs-lookup"><span data-stu-id="54dab-113">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span> 
2. <span data-ttu-id="54dab-114">Kontrollera att du har angett giltiga e-postadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] för dina säljare och kontakter, beroende på om de är potentiella eller befintliga kunder.</span><span class="sxs-lookup"><span data-stu-id="54dab-114">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="54dab-115">Det gör du genom att för varje kund eller säljare öppna kortet **Kontakt** eller **Säljare/Inköpare** och titta i fältet **E-post**.</span><span class="sxs-lookup"><span data-stu-id="54dab-115">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="54dab-116">När du har slutfört stegen i guiden kan du kontrollera om kopplingen har lyckats.</span><span class="sxs-lookup"><span data-stu-id="54dab-116">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="54dab-117">Sök efter **Marknadsföringsinställningar**, välj **Process**, sedan **Funktioner** och därefter **Validera konfiguration för e-postloggning**.</span><span class="sxs-lookup"><span data-stu-id="54dab-117">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="54dab-118">Visa e-postutbyten i interaktionsloggen</span><span class="sxs-lookup"><span data-stu-id="54dab-118">Viewing Email Message Exchanges in the Interaction Log</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="54dab-119">skapar en transaktion på sidan **Interaktionslogg** varje gång en säljare och en kontakt utbyter e-postmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="54dab-119">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="54dab-120">Om du vill visa interaktionsloggen öppnar du kortet **Kontakt** eller **Säljare/Inköpare** för den personen och väljer sedan **Navigera**, **Historik** och därefter **Interaktionslogg**.</span><span class="sxs-lookup"><span data-stu-id="54dab-120">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="54dab-121">Det finns några saker som du kan göra med posterna i loggen, till exempel:</span><span class="sxs-lookup"><span data-stu-id="54dab-121">There are a few things we can do with each entry in the log, for example:</span></span>

* <span data-ttu-id="54dab-122">Visa innehållet i e-postmeddelandet som utbytts genom att klicka på åtgärden **Visa bilagor**.</span><span class="sxs-lookup"><span data-stu-id="54dab-122">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
* <span data-ttu-id="54dab-123">Omvandla ett e-postutbyte till en affärsmöjlighet - Om en transaktion verkar lovande kan du omvandla den till en affärsmöjlighet och sedan hantera förloppet fram till en försäljning.</span><span class="sxs-lookup"><span data-stu-id="54dab-123">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="54dab-124">Välj posten och välj sedan åtgärden **Skapa affärsmöjlighet**.</span><span class="sxs-lookup"><span data-stu-id="54dab-124">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="54dab-125">Mer information finns i [Hantera försäljningsmöjligheter](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="54dab-125">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="54dab-126">Se även</span><span class="sxs-lookup"><span data-stu-id="54dab-126">See Also</span></span>
[<span data-ttu-id="54dab-127">Hantera relationer</span><span class="sxs-lookup"><span data-stu-id="54dab-127">Managing Relationships</span></span>](marketing-relationship-management.md)


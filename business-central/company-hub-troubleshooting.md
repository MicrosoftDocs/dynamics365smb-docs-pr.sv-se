---
title: Felsöka företagsnavet
description: Lär dig mer om hur du kringgår eventuella problem när du kör företagsnavet i Dynamics 365 Business Central för att hantera arbete i flera olika företag.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fc015058079e30b2db6989b246dc38498cd7a1f4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786518"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="07e56-103">Felsöka företagsnavet</span><span class="sxs-lookup"><span data-stu-id="07e56-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="07e56-104">Lägga till företag på instrumentpanelen för företagsnavet är också lätt, men den här artikeln innehåller lösningar på problem som kan uppstå på vägen.</span><span class="sxs-lookup"><span data-stu-id="07e56-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="07e56-105">Kontrollera fel</span><span class="sxs-lookup"><span data-stu-id="07e56-105">Check errors</span></span>

<span data-ttu-id="07e56-106">Använd åtgärden **Kontrollera fel** om du vill visa en lista över de senaste felen.</span><span class="sxs-lookup"><span data-stu-id="07e56-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="07e56-107">Du kan visa ytterligare information om varje fel och rensa loggen genom att ta bort äldre poster.</span><span class="sxs-lookup"><span data-stu-id="07e56-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="07e56-108">Anslutning misslyckades</span><span class="sxs-lookup"><span data-stu-id="07e56-108">Connection failed</span></span>

<span data-ttu-id="07e56-109">Det kan finnas en par olika orsaker till att du inte kan ansluta till ett företag, däribland följande:</span><span class="sxs-lookup"><span data-stu-id="07e56-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="07e56-110">URL i fältet **Miljölänk** är inte giltig</span><span class="sxs-lookup"><span data-stu-id="07e56-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="07e56-111">Gå till sidan **Miljölänkar**, öppna den miljö som du inte kan ansluta till och välj sedan åtgärden **Testa anslutningen**.</span><span class="sxs-lookup"><span data-stu-id="07e56-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="07e56-112">Klientens företag är offline, till exempel om den uppgraderas</span><span class="sxs-lookup"><span data-stu-id="07e56-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="07e56-113">I instrumentpanelen, väljer du menyposten **verktyg** och väljer **kontrollera fel**.</span><span class="sxs-lookup"><span data-stu-id="07e56-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="07e56-114">Då öppnas en lista med teknisk information, så du kanske vill kontakta administratören om du ser fel.</span><span class="sxs-lookup"><span data-stu-id="07e56-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="07e56-115">Felmeddelandet ”*Servern godkände inte klientens referenser*” innebär till exempel att du inte har tillgång.</span><span class="sxs-lookup"><span data-stu-id="07e56-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="07e56-116">Du har inte tillgång till alla företag i miljön som du försöker ansluta till</span><span class="sxs-lookup"><span data-stu-id="07e56-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="07e56-117">I [!INCLUDE [prod_short](includes/prod_short.md)] kan en organisation ha flera affärsenheter som kallas företag, och du kanske inte har tillgång till alla företag.</span><span class="sxs-lookup"><span data-stu-id="07e56-117">In [!INCLUDE [prod_short](includes/prod_short.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="07e56-118">Arbeta med administratören eller klienten för att se till att du har tillgång till företagen som du arbetar i.</span><span class="sxs-lookup"><span data-stu-id="07e56-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="07e56-119">Data uppdateras inte</span><span class="sxs-lookup"><span data-stu-id="07e56-119">Data does not refresh</span></span>

<span data-ttu-id="07e56-120">När du lägger till ett företag eller begär en uppdatering av data hämtar [!INCLUDE [prod_short](includes/prod_short.md)] data.</span><span class="sxs-lookup"><span data-stu-id="07e56-120">When you add a company or request a refresh of the data, [!INCLUDE [prod_short](includes/prod_short.md)] fetches the data.</span></span> <span data-ttu-id="07e56-121">Men du måste uppdatera sidan, till exempel om du väljer åtgärden **Läs in alla företag igen**, uppdatera webbläsarsidan, navigera från instrumentpanelen och sedan tillbaka igen, eller liknande.</span><span class="sxs-lookup"><span data-stu-id="07e56-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="07e56-122">Om du har lagt till ett företag men det inte visas i listan kan du också använda åtgärden **Läs in alla företag igen** för att uppdatera listan.</span><span class="sxs-lookup"><span data-stu-id="07e56-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="07e56-123">Se även</span><span class="sxs-lookup"><span data-stu-id="07e56-123">See also</span></span>

[<span data-ttu-id="07e56-124">Hantera arbete i flera företag med företagsnavet</span><span class="sxs-lookup"><span data-stu-id="07e56-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="07e56-125">Lägg till företag till företagsnavet</span><span class="sxs-lookup"><span data-stu-id="07e56-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="07e56-126">Revisorlösningar i Business Central</span><span class="sxs-lookup"><span data-stu-id="07e56-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
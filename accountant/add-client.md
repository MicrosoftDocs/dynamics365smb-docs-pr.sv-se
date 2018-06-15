---
title: "Hämta klienter till Dynamics 365 revisorsupplevelse | Microsoft Docs"
description: "Lär dig hur du lägger till befintliga klienter i Accountant Hub för Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8b8d92e114733d87b1866d66ee3111208e233ad3
ms.contentlocale: sv-se
ms.lasthandoff: 05/15/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a><span data-ttu-id="19648-103">Lägga till klienter i instrumentpanelen i [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="19648-103">Add Clients to Your Dashboard in [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="19648-104">Du kan lägga till en klient med hjälp av fönstret **klienter** som du öppnar genom att välja åtgärd **hantera klienter** i menyfliksområdet.</span><span class="sxs-lookup"><span data-stu-id="19648-104">You can add a client by using the **Clients** window, which you can open by choosing the **Manage Clients** action in the ribbon.</span></span> <span data-ttu-id="19648-105">Välj bara **Ny** och fyll sedan i relevanta fält.</span><span class="sxs-lookup"><span data-stu-id="19648-105">Simply choose **New** and then fill in the fields.</span></span>  

![Lägg till en klient](./media/accountant-add-client/manage-client.png)

<span data-ttu-id="19648-107">Datan i ett kort för varje klient som anges av dig och du kan ändra den efter behov.</span><span class="sxs-lookup"><span data-stu-id="19648-107">The data in the card for each client is specified by you, and you can change it as needed.</span></span> <span data-ttu-id="19648-108">Men fältet **klient-URL** är kritiskt – detta är hur du får tillgång till varje klients [!INCLUDE [d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="19648-108">However, the **Client URL** field is critical - this is how you can access each client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="19648-109">Använd åtgärdem **Testa klient-URL** i menyfliksområdet för att kontrollera att du har angett rätt länk.</span><span class="sxs-lookup"><span data-stu-id="19648-109">Use the **Test Client URL** action in the ribbon to test that you entered the right link.</span></span> <span data-ttu-id="19648-110">Den måste du ange URL-adressen pekar på klientens [!INCLUDE [d365fin](includes/d365fin_md.md)], såsom *<https://mybusiness.financials.dynamics.com>*.</span><span class="sxs-lookup"><span data-stu-id="19648-110">The URL that you must enter points at the client's [!INCLUDE [d365fin](includes/d365fin_md.md)], such as *<https://mybusiness.financials.dynamics.com>*.</span></span> <span data-ttu-id="19648-111">Denna URL används sedan när du väljer menyobjektet **Gå till företag** på instrumentpanelen [!INCLUDE [d365acc](includes/d365acc_md.md)].</span><span class="sxs-lookup"><span data-stu-id="19648-111">This URL is then used when you choose the **Go To Company** menu item in the [!INCLUDE [d365acc](includes/d365acc_md.md)] dashboard.</span></span>  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a><span data-ttu-id="19648-112">Bli inbjuden till en klients [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="19648-112">Get Invited to a Client's [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="19648-113">Ett företag som använder [!INCLUDE [d365fin](includes/d365fin_md.md)]kan bjuda in dig till [!INCLUDE [d365fin](includes/d365fin_md.md)]som deras extern revisor.</span><span class="sxs-lookup"><span data-stu-id="19648-113">A company who use [!INCLUDE [d365fin](includes/d365fin_md.md)] can invite you to [!INCLUDE [d365fin](includes/d365fin_md.md)] as their external accountant.</span></span> <span data-ttu-id="19648-114">För att bli inbjuden måste du du ge det e-postmeddelande som du använder med [!INCLUDE [d365acc](includes/d365acc_md.md)], såsom <em>me@accountant.com</em>. Kundens administratör kan sedan lägga till dig i sina system genom att köra guiden **bjuda in extern revisor**.</span><span class="sxs-lookup"><span data-stu-id="19648-114">To get invited, you must give them the email that you use with [!INCLUDE [d365acc](includes/d365acc_md.md)], such as <em>me@accountant.com</em>. Your client's administrator can then add you to their system by running the **Invite External Accountant** wizard.</span></span>  

<span data-ttu-id="19648-115">Därför får du e-post från en klient med länkar till deras [!INCLUDE [d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="19648-115">As a result, you will receive email from your client with links to their [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="19648-116">Den första länken är en inbjudan för att få tillgång till företaget – öppna länken och acceptera stegen som lägger till klienternas [!INCLUDE [d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="19648-116">The first link is an invitation to get access to their company - open the link and accept the steps that adds you to your client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="19648-117">Den andra länken är för att lägga till den här klienten till instrumentpanelen i [!INCLUDE [d365acc](includes/d365acc_md.md)] som beskrivs ovan.</span><span class="sxs-lookup"><span data-stu-id="19648-117">The second link is for adding this client to your dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] as described above.</span></span>  

<span data-ttu-id="19648-118">När du har accepterat inbjudan kan du har loggat in och kan komma åt den klientens ekonomiska data från rollcentret **Revisor**.</span><span class="sxs-lookup"><span data-stu-id="19648-118">When you have accepted the invitation, you are logged in and can access the client's financial data from the **Accountant** Role Center.</span></span> <span data-ttu-id="19648-119">Mer information finns i [Revisorupplevelse i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).</span><span class="sxs-lookup"><span data-stu-id="19648-119">For more information, see [Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).</span></span>  

## <a name="see-also"></a><span data-ttu-id="19648-120">Se även</span><span class="sxs-lookup"><span data-stu-id="19648-120">See Also</span></span>
<span data-ttu-id="19648-121">[Komma igång med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="19648-121">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="19648-122">[Felsökning [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="19648-122">[Troubleshooting [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span></span>  


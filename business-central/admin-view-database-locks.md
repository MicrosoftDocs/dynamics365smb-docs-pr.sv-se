---
title: Visa databaslås
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: abee0f31d66f648f4b0be567d8599b31c536a193
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324108"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="7cfbd-102">Visa databaslås</span><span class="sxs-lookup"><span data-stu-id="7cfbd-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="7cfbd-103">Om lås</span><span class="sxs-lookup"><span data-stu-id="7cfbd-103">About Locks</span></span>

<span data-ttu-id="7cfbd-104">Databaslåsning styr åtkomsten för flera användare till samma data samtidigt.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="7cfbd-105">Om du vill skydda en transaktion mot att andra transaktioner ändrar samma data kommer den första transaktionen att låsa datan.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="7cfbd-106">Låset förblir aktiverat tills transaktionen är klar.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="7cfbd-107">Användare kan hindras från att slutföra transaktioner på den låsta datan.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="7cfbd-108">Oftast visas ett meddelande som anger låsstatusen.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="7cfbd-109">För att visa databaslås</span><span class="sxs-lookup"><span data-stu-id="7cfbd-109">To view database locks</span></span>

<span data-ttu-id="7cfbd-110">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **Databaslås** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="7cfbd-111">Sidan **Databaslås** ger en översiktsbild av alla aktuella databaslås.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="7cfbd-112">Mer information om hur du låser databasen finns i [Övervaka databaslås](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjälpavsnittet för Business Central-utvecklare och IT-proffs.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cfbd-113">Se även</span><span class="sxs-lookup"><span data-stu-id="7cfbd-113">See Also</span></span>

[<span data-ttu-id="7cfbd-114">Övervaka databaslås</span><span class="sxs-lookup"><span data-stu-id="7cfbd-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
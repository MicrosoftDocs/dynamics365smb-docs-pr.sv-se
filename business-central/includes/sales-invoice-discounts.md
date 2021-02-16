---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035797"
---
<span data-ttu-id="3f337-101">När alla artiklar har angetts på försäljningsorderraderna kan du beräkna försäljningsdokuments totala fakturarabatt genom att välja åtgärden **Beräkna fakturarabatt**.</span><span class="sxs-lookup"><span data-stu-id="3f337-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="3f337-102">Om fältet **Berk. fakturarabatt** väljs i fönstret **Försäljningsinställningar** kommer fakturarabatten att beräknas automatiskt när du gör något av följande i ett säljdokument:</span><span class="sxs-lookup"><span data-stu-id="3f337-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="3f337-103">Visa statistik</span><span class="sxs-lookup"><span data-stu-id="3f337-103">View statistics</span></span>
* <span data-ttu-id="3f337-104">Visa en testrapport</span><span class="sxs-lookup"><span data-stu-id="3f337-104">View a test report</span></span>
* <span data-ttu-id="3f337-105">Skriv ut</span><span class="sxs-lookup"><span data-stu-id="3f337-105">Print</span></span>
* <span data-ttu-id="3f337-106">Post</span><span class="sxs-lookup"><span data-stu-id="3f337-106">Post</span></span>

<span data-ttu-id="3f337-107">Rabatten fördelas på alla försäljningsdokumentets rader för artiklar där fältet **Tillåt fakturarabatt** på försäljningsorderraden innehåller **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3f337-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="3f337-108">Detta är den förvalda inställningen för artiklar.</span><span class="sxs-lookup"><span data-stu-id="3f337-108">This is the default setting for items.</span></span>

<span data-ttu-id="3f337-109">Villkoren för fakturarabatt definieras på sidan **Anp. fakturarabatter** för att beräkna fakturarabatten.</span><span class="sxs-lookup"><span data-stu-id="3f337-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="3f337-110">Valutakoden i försäljningsdokumentet används för att hitta villkoren för fakturarabatt i motsvarande valuta.</span><span class="sxs-lookup"><span data-stu-id="3f337-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="3f337-111">Om inga fakturarabatter har definierats för utländska valutor används villkoren för fakturarabatt som definieras på sidan **Anp. fakturarabatter** med belopp i din lokala valuta, och valutakursen på bokföringsdatumet i säljdokumentet används för att beräkna fakturarabatten i den utländska valutan.</span><span class="sxs-lookup"><span data-stu-id="3f337-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>

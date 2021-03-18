---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470293"
---
<span data-ttu-id="e718c-101">När alla artiklar har angetts på försäljningsraderna kan du beräkna fakturarabatten för hela dokumentet genom att välja åtgärden **Beräkna fakturarabatt**.</span><span class="sxs-lookup"><span data-stu-id="e718c-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="e718c-102">Rabatten beräknas baserat på alla försäljningsdokumentets rader för artiklar där fältet **Tillåt fakturarabatt** på försäljningsorderraden innehåller **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e718c-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="e718c-103">Detta är den förvalda inställningen för artiklar.</span><span class="sxs-lookup"><span data-stu-id="e718c-103">This is the default setting for items.</span></span> <span data-ttu-id="e718c-104">Rader med artikelomkostnader ingår till exempel inte i beräkningen av fakturarabatten.</span><span class="sxs-lookup"><span data-stu-id="e718c-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="e718c-105">Om du vill tillämpa en rabatt på sådana rader måste du ange fältet **Radrabatt %** på de relevanta raderna.</span><span class="sxs-lookup"><span data-stu-id="e718c-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="e718c-106">Om fältet **Beräkn. fakturarabatt** väljs på sidan **Försäljningsinställningar** kommer fakturarabatten att beräknas automatiskt när du gör något av följande i ett säljdokument:</span><span class="sxs-lookup"><span data-stu-id="e718c-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="e718c-107">Visa statistik</span><span class="sxs-lookup"><span data-stu-id="e718c-107">View statistics</span></span>
> * <span data-ttu-id="e718c-108">Visa en testrapport</span><span class="sxs-lookup"><span data-stu-id="e718c-108">View a test report</span></span>
> * <span data-ttu-id="e718c-109">Skriv ut</span><span class="sxs-lookup"><span data-stu-id="e718c-109">Print</span></span>
> * <span data-ttu-id="e718c-110">Post</span><span class="sxs-lookup"><span data-stu-id="e718c-110">Post</span></span>

<span data-ttu-id="e718c-111">Villkoren för fakturarabatt för en kund definieras på sidan **Kundfakturarabatter** för kunden.</span><span class="sxs-lookup"><span data-stu-id="e718c-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="e718c-112">Valutakoden i försäljningsdokumentet används för att hitta villkoren för fakturarabatt i motsvarande valuta.</span><span class="sxs-lookup"><span data-stu-id="e718c-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="e718c-113">Om inga fakturarabatter har definierats för utländska valutor används villkoren för fakturarabatt som definieras på sidan **Anp. fakturarabatter** med belopp i din lokala valuta, och valutakursen på bokföringsdatumet i säljdokumentet används för att beräkna fakturarabatten i den utländska valutan.</span><span class="sxs-lookup"><span data-stu-id="e718c-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>

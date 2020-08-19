---
title: Så här ställer du in inköpstransaktioner för tredje part från EU-land
description: EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0da964d4f03cdbd847c4fb0081c6e10ce6468d7b
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676746"
---
# <a name="set-up-eu-third-party-purchase-transactions"></a><span data-ttu-id="8611f-103">Ställa in treparts EU-inköpstransaktioner</span><span class="sxs-lookup"><span data-stu-id="8611f-103">Set Up EU Third-Party Purchase Transactions</span></span>
<span data-ttu-id="8611f-104">EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera Sverige.</span><span class="sxs-lookup"><span data-stu-id="8611f-104">European Union (EU) third-party trade occurs when you receive a purchase invoice from a customer in one EU country/region and the products are sent to a different EU country/region without entering Sweden.</span></span> <span data-ttu-id="8611f-105">Transaktionsbeloppet måste identifieras och rapporteras separat i enlighet med de svenska reglerna för momsrapportering och kraven för systemet för utbyte av mervärdesskattedata (VAT Information Exchange System, VIES).</span><span class="sxs-lookup"><span data-stu-id="8611f-105">The transaction amount must be identified and reported separately to comply with Swedish VAT reporting and VAT Information Exchange System (VIES) requirements.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="8611f-106">omfattar en svensk tilläggsfunktionalitet så att inköpstransaktioner kan ställas in som EU trepartshandel.</span><span class="sxs-lookup"><span data-stu-id="8611f-106">includes Swedish enhancements that allow purchase transactions to be set up as EU third-party trade.</span></span> <span data-ttu-id="8611f-107">Bokförda EU trepartstransaktioner kan då filtreras i momsrapporter och exkluderas från beloppet i kolumnen **Försäljning till kund** i rapporten **Moms- och kvartalsredovisning**.</span><span class="sxs-lookup"><span data-stu-id="8611f-107">Posted EU third-party transactions can then be filtered in VAT statements and excluded from the amount in the **Sales to Customer** column in the **VAT- VIES Declaration Tax Auth** report.</span></span>  

## <a name="to-set-up-eu-third-party-purchase-transactions"></a><span data-ttu-id="8611f-108">Så här ställer du in EU trepartsinköpstransaktioner</span><span class="sxs-lookup"><span data-stu-id="8611f-108">To set up EU third-party purchase transactions</span></span>  

1.  <span data-ttu-id="8611f-109">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](../../media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="8611f-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8611f-110">Välj en befintlig inköpsfakturan eller åtgärden **Nytt** för att skapa en ny.</span><span class="sxs-lookup"><span data-stu-id="8611f-110">Select an existing purchase invoice, or choose the **New** action to create a new one.</span></span>  
3.  <span data-ttu-id="8611f-111">I snabbfliken **Fakturadetaljer** markerar du kryssrutan **Treparts EU-handel**.</span><span class="sxs-lookup"><span data-stu-id="8611f-111">On the **Invoice Details** FastTab, select the **EU 3-Party Trade** check box.</span></span>  
4.  <span data-ttu-id="8611f-112">Välj knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="8611f-112">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8611f-113">Se även</span><span class="sxs-lookup"><span data-stu-id="8611f-113">See Also</span></span>  
 <span data-ttu-id="8611f-114">[Rapportera moms till skattemyndigheterna](../../finance-how-report-vat.md) </span><span class="sxs-lookup"><span data-stu-id="8611f-114">[Report VAT to Tax Authorities](../../finance-how-report-vat.md) </span></span>  
 [<span data-ttu-id="8611f-115">Lokal funktionalitet för Sverige</span><span class="sxs-lookup"><span data-stu-id="8611f-115">Sweden Local Functionality</span></span>](sweden-local-functionality.md)

---
title: Validera ett momsregistrerings nummer | Microsoft Docs
description: Validera ett momsregistreringsnummer
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 07/21/2020
ms.author: andregu
ms.openlocfilehash: 9624a51f040ae6231d9d0354cb0c571287ccd3e8
ms.sourcegitcommit: e22666f90262c7d2084ca6c74ca7d66652fc6df6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617294"
---
# <a name="validate-a-vat-registration-number"></a><span data-ttu-id="150e4-103">Validera ett momsregistreringsnummer</span><span class="sxs-lookup"><span data-stu-id="150e4-103">Validate a VAT Registration Number</span></span>

<span data-ttu-id="150e4-104">Det är viktigt att momsregistreringsnummer för kunder, leverantörer och kontakter är giltiga.</span><span class="sxs-lookup"><span data-stu-id="150e4-104">It is important that the VAT registration numbers you have for customers, vendors, and contacts are valid.</span></span> <span data-ttu-id="150e4-105">Till exempel ändrar företag sin skatteskuldstatus och i vissa länder kan skattemyndigheterna be dig lämna rapporter som t.ex. EG-försäljningslisterapport som anger de momsregistreringsnummer som du använder när du gör affärer.</span><span class="sxs-lookup"><span data-stu-id="150e4-105">For example, companies sometimes change their tax liability status, and in some countries tax authorities might ask you to provide reports, such as the EC Sales List report, that list the VAT registration numbers you use when you do business.</span></span>

<span data-ttu-id="150e4-106">Europeiska kommissionen har en tjänst för VIES momsnummervalidering på sin webbplats som är offentlig och kostnadsfri.</span><span class="sxs-lookup"><span data-stu-id="150e4-106">The European Commission provides the VIES VAT Number Validation service on its website, which is public and free.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="150e4-107">kan spara dig det steget och låter dig använda VIES-tjänsten för verifiering och spåra momsregistreringsnummer för kunder, leverantörer och kontakter direkt från kund-, leverantörs- och kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="150e4-107">can save you a step and let you use the VIES service to validate and track VAT numbers for customers, vendors, and contacts straight from the customer, vendor, and contact cards.</span></span> <span data-ttu-id="150e4-108">Tjänsten i [!INCLUDE[d365fin](includes/d365fin_md.md)] heter **Valideringstjänst för EU momsreg.nr.**.</span><span class="sxs-lookup"><span data-stu-id="150e4-108">The service in [!INCLUDE[d365fin](includes/d365fin_md.md)] is named **EU VAT Reg. No. Validation Service**.</span></span> <span data-ttu-id="150e4-109">Den är tillgänglig på sidan **Anslutningar till tjänst**, och du kan börja använda den direkt.</span><span class="sxs-lookup"><span data-stu-id="150e4-109">The service is available on the **Service Connections** page, and you can start using it right away.</span></span> <span data-ttu-id="150e4-110">Registrering behövs inte och tjänsten är gratis.</span><span class="sxs-lookup"><span data-stu-id="150e4-110">The service connection is free, and signup is not required.</span></span>

## <a name="to-verify-vat-registration-numbers"></a><span data-ttu-id="150e4-111">Kontrollera momsregistreringsnummer</span><span class="sxs-lookup"><span data-stu-id="150e4-111">To verify VAT registration numbers</span></span>

<span data-ttu-id="150e4-112">För att aktivera **Valideringstjänst för EU momsreg.nr.** öppnar du posten på sidan **Anslutning till tjänst**.</span><span class="sxs-lookup"><span data-stu-id="150e4-112">In order to enable the **EU VAT Reg. No. Validation Service** open the entry in the **Service Connection** page.</span></span> <span data-ttu-id="150e4-113">Fältet **Tjänstslutpunkt** ska redan vara ifyllt.</span><span class="sxs-lookup"><span data-stu-id="150e4-113">The **Service Endpoint** field should already be populated.</span></span> <span data-ttu-id="150e4-114">Om så inte är fallet kan du använda åtgärden **Ställ in standardslutpunkt**.</span><span class="sxs-lookup"><span data-stu-id="150e4-114">If not, you can use the **Set Default Endpoint** action.</span></span> <span data-ttu-id="150e4-115">Ange sedan fältet **Aktiverad** och du är redo att sätta igång.</span><span class="sxs-lookup"><span data-stu-id="150e4-115">Then set the **Enabled** field and you are good to go.</span></span>

> [!NOTE]
> <span data-ttu-id="150e4-116">Om du vill aktivera valideringstjänsten</span><span class="sxs-lookup"><span data-stu-id="150e4-116">To enable the EU VAT Reg. No.</span></span> <span data-ttu-id="150e4-117">för EU momsreg.nr. måste du ha administratörsrättigheter.</span><span class="sxs-lookup"><span data-stu-id="150e4-117">Validation Service, you must have administrator permissions.</span></span>

<span data-ttu-id="150e4-118">När du använder vår tjänst registrerar vi en historik över momsregistreringsnummer och kontroller för varje kund, leverantör eller kontakt i **momsregistreringslogga**, så att du enkelt kan spåra dem.</span><span class="sxs-lookup"><span data-stu-id="150e4-118">When you use our service connection, we record a history of VAT numbers and verifications for each customer, vendor, or contact, in the **VAT Registration Log**, so you can easily track them.</span></span> <span data-ttu-id="150e4-119">Loggen är unik för varje kund.</span><span class="sxs-lookup"><span data-stu-id="150e4-119">The log is specific to each customer.</span></span> <span data-ttu-id="150e4-120">Loggen är användbar för att verifierat att det aktuella momsregistreringsnumret är korrekt.</span><span class="sxs-lookup"><span data-stu-id="150e4-120">For example, the log is useful for proving that you have verified that the current VAT number is correct.</span></span> <span data-ttu-id="150e4-121">När du verifierar ett momsregistreringsnummer kommer kolumnen **begär ID** i loggen att visa att du har vidtagit åtgärder.</span><span class="sxs-lookup"><span data-stu-id="150e4-121">When you verify a VAT number, the **Request Identifier** column in the log will reflect that you have taken action.</span></span>

<span data-ttu-id="150e4-122">Du kan se momsregistreringsloggen på kund-, leverantör- eller kontaktkorten på snabbfliken **fakturering** genom att välja sökknappen i **Momsregistreringsnr.**</span><span class="sxs-lookup"><span data-stu-id="150e4-122">You can view the VAT Registration log on the Customer, Vendor, or Contact cards, on the **Invoicing** FastTab, by choosing the lookup button in the **VAT Registration No.** field.</span></span>  

<span data-ttu-id="150e4-123">Tjänsten kan också spara tid när du skapar en kund eller leverantör.</span><span class="sxs-lookup"><span data-stu-id="150e4-123">Our service can also save you time when you create a customer or vendor.</span></span> <span data-ttu-id="150e4-124">Om du känner till kundens momsregistreringsnummer kan du ange det i fältet **Momsregistreringsnr** på korten för kunden eller leverantören, och vi ska fylla i kundens namn åt dig.</span><span class="sxs-lookup"><span data-stu-id="150e4-124">If you know the customer's VAT number, you can enter it in the **VAT Registration No.** field on the Customer or Vendor cards, and we will fill out the customer name for you.</span></span> <span data-ttu-id="150e4-125">Vissa länder har dessutom företagsadresser i ett strukturerat format.</span><span class="sxs-lookup"><span data-stu-id="150e4-125">Some countries also provide company addresses in a structured format.</span></span> <span data-ttu-id="150e4-126">I dessa länder fyller vi även i addressen.</span><span class="sxs-lookup"><span data-stu-id="150e4-126">In those countries, we fill in the address too.</span></span>  

<span data-ttu-id="150e4-127">Det finns ett par saker att komma ihåg om tjänsten VIES momsnummervalidering:</span><span class="sxs-lookup"><span data-stu-id="150e4-127">There are a couple of things to note about the VIES VAT Number Validation service:</span></span>

* <span data-ttu-id="150e4-128">Den här tjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.</span><span class="sxs-lookup"><span data-stu-id="150e4-128">The service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  
* <span data-ttu-id="150e4-129">Det kan uppstå avbrott för den här tjänsten som inte Microsoft ansvarar för.</span><span class="sxs-lookup"><span data-stu-id="150e4-129">You may experience downtime for this service for which Microsoft is not responsible.</span></span> <span data-ttu-id="150e4-130">Tjänsten är en del av ett omfattande EU-nätverk av nationella register för moms.</span><span class="sxs-lookup"><span data-stu-id="150e4-130">The service is part of a broad EU network of national VAT registers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="150e4-131">Det är ditt ansvar att kontrollera att alla data är giltiga.</span><span class="sxs-lookup"><span data-stu-id="150e4-131">It is your responsibility to check that the data is valid.</span></span> <span data-ttu-id="150e4-132">Ibland returneras data med fel av tjänsten VIES momsnummervalidering.</span><span class="sxs-lookup"><span data-stu-id="150e4-132">On occasion, data with errors is returned by the VIES VAT Number Validation service.</span></span> <span data-ttu-id="150e4-133">Om valideringen misslyckas validerar du momsregistreringsnumren på [webbplatsen](https://ec.europa.eu/taxation_customs/vies/), skriver ut resultatet eller sparar det på en delad plats och lägger sedan till länken till posten för kunden, leverantören eller kontakten.</span><span class="sxs-lookup"><span data-stu-id="150e4-133">If validation fails, validate the VAT registration numbers on the [web site](https://ec.europa.eu/taxation_customs/vies/), print the result or save it to a shared location, and then add the link to the record for your customer, vendor, or contact.</span></span> <span data-ttu-id="150e4-134">För mer information, se [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="150e4-134">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="150e4-135">Se även</span><span class="sxs-lookup"><span data-stu-id="150e4-135">See Also</span></span>

[<span data-ttu-id="150e4-136">Ställa in moms</span><span class="sxs-lookup"><span data-stu-id="150e4-136">Set Up Value-Added Tax</span></span>](finance-setup-vat.md)  
[<span data-ttu-id="150e4-137">Ställa in orealiserad mervärdesskatt</span><span class="sxs-lookup"><span data-stu-id="150e4-137">Setting Up Unrealized Value Added Tax</span></span>](finance-setup-unrealized-vat.md)  
[<span data-ttu-id="150e4-138">Rapportera moms till skattemyndigheterna</span><span class="sxs-lookup"><span data-stu-id="150e4-138">Report VAT to a Tax Authority</span></span>](finance-how-report-vat.md)  
[<span data-ttu-id="150e4-139">Arbeta med moms på försäljning och inköp</span><span class="sxs-lookup"><span data-stu-id="150e4-139">Work with VAT on Sales and Purchases</span></span>](finance-work-with-vat.md)  
[<span data-ttu-id="150e4-140">Lokal funktionalitet i Business Central</span><span class="sxs-lookup"><span data-stu-id="150e4-140">Local functionality in Business Central</span></span>](about-localization.md)  
---
title: Skapa bankkonton | Microsoft Docs
description: "Du kan stämma av bankkonton i Financials med utdrag från banken."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bank-accounts"></a><span data-ttu-id="d53e3-103">Så här skapar du bankkonton</span><span class="sxs-lookup"><span data-stu-id="d53e3-103">How to: Set Up Bank Accounts</span></span>
<span data-ttu-id="d53e3-104">Du använder bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att hålla reda på dina banktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="d53e3-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="d53e3-105">Konton kan definieras i den lokala valutan eller i en utländsk valuta.</span><span class="sxs-lookup"><span data-stu-id="d53e3-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="d53e3-106">När du har skapat bankkonton kan du också använda funktionen för utskrift av checkar.</span><span class="sxs-lookup"><span data-stu-id="d53e3-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="d53e3-107">Så här skapar du bankkonton</span><span class="sxs-lookup"><span data-stu-id="d53e3-107">To set up bank accounts</span></span>
1. <span data-ttu-id="d53e3-108">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d53e3-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d53e3-109">I fönstret **Bankkonton** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d53e3-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="d53e3-110">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="d53e3-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="d53e3-111">Så här skapar du ett bankkonto för import eller export av bankfilerna</span><span class="sxs-lookup"><span data-stu-id="d53e3-111">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="d53e3-112">Fälten på snabbfliken **Överför** i fönstret **Bankkontokort** är relaterade till import och export av bankfeeds och filer.</span><span class="sxs-lookup"><span data-stu-id="d53e3-112">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="d53e3-113">Mer information finns i [Så här skapar du tjänsten för Bankdatakonvertering](bank-how-setup-bank-data-conversion-service.md) och [Så här ställer du in tjänsten bankdatakonvertering](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="d53e3-113">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="d53e3-114">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d53e3-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d53e3-115">Öppna kortet för ett bankkonto som du ska exportera eller importera bankfiler.</span><span class="sxs-lookup"><span data-stu-id="d53e3-115">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="d53e3-116">I snabbfliken **Överför** fyller du i nödvändiga fält.</span><span class="sxs-lookup"><span data-stu-id="d53e3-116">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="d53e3-117">Andra filexporttjänster och deras format kräver olika inställningsvärden i fönstret **bankkontokort**.</span><span class="sxs-lookup"><span data-stu-id="d53e3-117">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="d53e3-118">Du får information om vilka inställningsvärden som är fel eller saknas när du försöker exportera filen.</span><span class="sxs-lookup"><span data-stu-id="d53e3-118">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="d53e3-119">Så läs de korta beskrivningarna av fälten eller se relaterad procedur i närliggande ämnen.</span><span class="sxs-lookup"><span data-stu-id="d53e3-119">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="d53e3-120">Till exempel exportera en betalningsfil för nordamerikansk elektronisk överföring kräver att både fältet **Sista kundremissnr.** och fältet **Transitnr.** fylls i.</span><span class="sxs-lookup"><span data-stu-id="d53e3-120">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.** field and the **Transit No.** field are filled in.</span></span> <span data-ttu-id="d53e3-121">Mer information finns i [Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="d53e3-121">For more information, see [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="d53e3-122">Så här skapar du leverantörsbankkonto för export av bankfiler</span><span class="sxs-lookup"><span data-stu-id="d53e3-122">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="d53e3-123">Fälten på snabbfliken **Överför** i fönstret **Leveraqntörsbankkontokort** är relaterade till export av bankfeeds och filer.</span><span class="sxs-lookup"><span data-stu-id="d53e3-123">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="d53e3-124">Mer information finns i [Så här skapar du tjänsten för Bankdatakonvertering](bank-how-setup-bank-data-conversion-service.md) och [Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="d53e3-124">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="d53e3-125">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d53e3-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="d53e3-126">Öppna kortet för en leverantör vars bankkonto som du ska exportera betalningsbankfiler till.</span><span class="sxs-lookup"><span data-stu-id="d53e3-126">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="d53e3-127">Välj åtgärden **bankkonton**.</span><span class="sxs-lookup"><span data-stu-id="d53e3-127">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="d53e3-128">I fönstret**Leverantörsbankkontokort** på snabbfliken **Överför** fyller du sedan de fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="d53e3-128">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="d53e3-129">Se även</span><span class="sxs-lookup"><span data-stu-id="d53e3-129">See Also</span></span>
[<span data-ttu-id="d53e3-130">Ställa in bankverksamhet</span><span class="sxs-lookup"><span data-stu-id="d53e3-130">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="d53e3-131">Hantera bankkonton</span><span class="sxs-lookup"><span data-stu-id="d53e3-131">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="d53e3-132">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d53e3-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


---
title: "Gör betalningar med tjänsten för bankdatakonvertering eller SEPA Kreditöverföring | Microsoft Docs"
description: "Behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformation från på journalraderna."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 0760b5480b3c2de9bc370526bd87da2c9a492d92
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="a72e7-103">Göra betalningar med tjänsten för bankdatakonvertering eller SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="a72e7-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="a72e7-104">I fönstret **Betalningsjournal** kan du behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformation från på journalraderna.</span><span class="sxs-lookup"><span data-stu-id="a72e7-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="a72e7-105">Du kan sedan överföra filen till den elektroniska banken där relaterade pengaöverföringar bearbetas.</span><span class="sxs-lookup"><span data-stu-id="a72e7-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a72e7-106"> stödjer SEPA kreditöverföringar-format, men andra format för elektroniska betalningar i ditt land/din region kan finnas.</span><span class="sxs-lookup"><span data-stu-id="a72e7-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="a72e7-107">Om du vill aktivera SEPA-kreditöverföringar måste du först lägga upp ett bankkonto, en leverantör och redovisningsjournalen som utbetalningsjournalen baseras på.</span><span class="sxs-lookup"><span data-stu-id="a72e7-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="a72e7-108">Sedan förbereder du betalningar till leverantörer genom att automatiskt fylla i fönstret **Betalningsjournal** med förfallna betalningar med angivna bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="a72e7-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a72e7-109">När du har verifierat att betalningarna har behandlats korrekt av banken kan du fortsätta att bokföra utbetalningsjournalraderna.</span><span class="sxs-lookup"><span data-stu-id="a72e7-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="a72e7-110">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="a72e7-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="a72e7-111">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="a72e7-111">**To**</span></span>|<span data-ttu-id="a72e7-112">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="a72e7-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="a72e7-113">Aktivera funktionen för bankdatakonvertering om du vill få en eventuell bankutdragsfil konverterad till ett format som du kan importera eller få dina exporterad betalningfiler konverterade till det format som din bank kräver.</span><span class="sxs-lookup"><span data-stu-id="a72e7-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="a72e7-114">Så här ställer du in tjänsten bankdatakonvertering</span><span class="sxs-lookup"><span data-stu-id="a72e7-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="a72e7-115">Skapa ett bankkonto, en leverantör och en utbetalningsjournal för SEPA-kreditöverföring.</span><span class="sxs-lookup"><span data-stu-id="a72e7-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="a72e7-116">Så här: Skapar SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="a72e7-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="a72e7-117">Fyll i betalningsjournalen med rader för förfallna betalningar till leverantörer, med alternativet att infoga bokföringsdatum som baseras på förfallodatumet för de relaterade inköpsdokumenten.</span><span class="sxs-lookup"><span data-stu-id="a72e7-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="a72e7-118">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="a72e7-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="a72e7-119">Exportera utbetalningsjournalraderna till en fil i formatet SEPA Krediteringsöverföring.</span><span class="sxs-lookup"><span data-stu-id="a72e7-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="a72e7-120">Så här exporterar du betalningar till en bankfil</span><span class="sxs-lookup"><span data-stu-id="a72e7-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="a72e7-121">Bokför betalningarna när den elektroniska betalningen har behandlats utan problem av banken.</span><span class="sxs-lookup"><span data-stu-id="a72e7-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="a72e7-122">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="a72e7-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="a72e7-123">Se även</span><span class="sxs-lookup"><span data-stu-id="a72e7-123">See Also</span></span>  
[<span data-ttu-id="a72e7-124">Så här ställer du in tjänsten bankdatakonvertering</span><span class="sxs-lookup"><span data-stu-id="a72e7-124">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="a72e7-125">Så här: Skapar SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="a72e7-125">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="a72e7-126">[Hantera Leverantörsreskontra](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="a72e7-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="a72e7-127">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="a72e7-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="a72e7-128">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="a72e7-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   


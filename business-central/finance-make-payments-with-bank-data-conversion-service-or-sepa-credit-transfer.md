---
title: "Gör betalningar med tjänsten för bankdatakonvertering eller SEPA Kreditöverföring | Microsoft Docs"
description: "Behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformation från på journalraderna."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 99277cb2daf37fbce4548cf637e8967fa6688dbc
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="dbdde-103">Göra betalningar med tjänsten för bankdatakonvertering eller SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="dbdde-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="dbdde-104">I fönstret **Betalningsjournal** kan du behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformation från på journalraderna.</span><span class="sxs-lookup"><span data-stu-id="dbdde-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="dbdde-105">Du kan sedan överföra filen till den elektroniska banken där relaterade pengaöverföringar bearbetas.</span><span class="sxs-lookup"><span data-stu-id="dbdde-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="dbdde-106"> stödjer SEPA kreditöverföringar-format, men andra format för elektroniska betalningar i ditt land/din region kan finnas.</span><span class="sxs-lookup"><span data-stu-id="dbdde-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="dbdde-107">Om du vill aktivera SEPA-kreditöverföringar måste du först lägga upp ett bankkonto, en leverantör och redovisningsjournalen som utbetalningsjournalen baseras på.</span><span class="sxs-lookup"><span data-stu-id="dbdde-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="dbdde-108">Sedan förbereder du betalningar till leverantörer genom att automatiskt fylla i fönstret **Betalningsjournal** med förfallna betalningar med angivna bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="dbdde-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dbdde-109">När du har verifierat att betalningarna har behandlats korrekt av banken kan du fortsätta att bokföra utbetalningsjournalraderna.</span><span class="sxs-lookup"><span data-stu-id="dbdde-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="dbdde-110">I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.</span><span class="sxs-lookup"><span data-stu-id="dbdde-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="dbdde-111">**Om du vill**</span><span class="sxs-lookup"><span data-stu-id="dbdde-111">**To**</span></span>|<span data-ttu-id="dbdde-112">**Gå till**</span><span class="sxs-lookup"><span data-stu-id="dbdde-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="dbdde-113">Aktivera funktionen för bankdatakonvertering om du vill få en eventuell bankutdragsfil konverterad till ett format som du kan importera eller få dina exporterad betalningfiler konverterade till det format som din bank kräver.</span><span class="sxs-lookup"><span data-stu-id="dbdde-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="dbdde-114">Ställa in konverteringstjänsten för bankdata</span><span class="sxs-lookup"><span data-stu-id="dbdde-114">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="dbdde-115">Skapa ett bankkonto, en leverantör och en utbetalningsjournal för SEPA-kreditöverföring.</span><span class="sxs-lookup"><span data-stu-id="dbdde-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="dbdde-116">Konfigurera SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="dbdde-116">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="dbdde-117">Fyll i betalningsjournalen med rader för förfallna betalningar till leverantörer, med alternativet att infoga bokföringsdatum som baseras på förfallodatumet för de relaterade inköpsdokumenten.</span><span class="sxs-lookup"><span data-stu-id="dbdde-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="dbdde-118">Hantera Leverantörsreskontra</span><span class="sxs-lookup"><span data-stu-id="dbdde-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="dbdde-119">Exportera utbetalningsjournalraderna till en fil i formatet SEPA Krediteringsöverföring.</span><span class="sxs-lookup"><span data-stu-id="dbdde-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="dbdde-120">Exportera betalningar till en bankfil</span><span class="sxs-lookup"><span data-stu-id="dbdde-120">Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="dbdde-121">Bokför betalningarna när den elektroniska betalningen har behandlats utan problem av banken.</span><span class="sxs-lookup"><span data-stu-id="dbdde-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="dbdde-122">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="dbdde-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="dbdde-123">Se även</span><span class="sxs-lookup"><span data-stu-id="dbdde-123">See Also</span></span>  
[<span data-ttu-id="dbdde-124">Ställa in konverteringstjänsten för bankdata</span><span class="sxs-lookup"><span data-stu-id="dbdde-124">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="dbdde-125">Konfigurera SEPA-kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="dbdde-125">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="dbdde-126">[Hantera Leverantörsreskontra](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="dbdde-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="dbdde-127">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="dbdde-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="dbdde-128">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="dbdde-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

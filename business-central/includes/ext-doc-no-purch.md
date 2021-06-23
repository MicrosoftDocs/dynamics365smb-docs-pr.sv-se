---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116006"
---
<span data-ttu-id="8bd0e-101">I inköpsdokument och journaler kan du ange ett dokumentnummer som refererar till leverantörens nummersystem.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="8bd0e-102">Använd det här fältet för att registrera numret som leverantören har tilldelat ordern, fakturan eller kreditnotan.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="8bd0e-103">Sedan kan du använda numret om du av någon anledning behöver söka efter den bokförda posten med hjälp av detta nummer.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="8bd0e-104">Fältet **Ext. Dok.nr obligatoriskt** på sidan **Konfiguration av inköp och leverantörsreskontra** anger om det är obligatoriskt att ange ett externt dokumentnummer i följande situationer:</span><span class="sxs-lookup"><span data-stu-id="8bd0e-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="8bd0e-105">I fältet **Leverantörens fakturanr**, fältet **Leverantörens ordernr**</span><span class="sxs-lookup"><span data-stu-id="8bd0e-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="8bd0e-106">eller fältet **Leverantörens kreditnotanr**</span><span class="sxs-lookup"><span data-stu-id="8bd0e-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="8bd0e-107">i ett inköpshuvud</span><span class="sxs-lookup"><span data-stu-id="8bd0e-107">field on a purchase header</span></span>

* <span data-ttu-id="8bd0e-108">I fältet **Externt dokumentnr** på en redovisningsjournalrad, där fältet **Dokumenttyp** är inställt på *Faktura*, *Kreditnota* eller *Räntefaktura* och fältet **Kontotyp** är inställt på *Leverantör*.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="8bd0e-109">Om du markerar det här fältet kommer det inte att vara möjligt att bokföra en faktura, en kreditnota eller den typ av journalrad som beskrivits ovan utan ett externt dokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="8bd0e-110">Det externa dokumentnumret inkluderas i de bokförda dokumenten där du kan söka på det aktuella numret.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="8bd0e-111">Du kan även söka med hjälp av det externa dokumentnumret när du navigerar i leverantörsreskontratransaktioner.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="8bd0e-112">Olika sätt att hantera externa dokumentnummer är att använda fältet **Din referens**.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="8bd0e-113">Om du använder fältet **Din referens** inkluderas numret i bokförda dokument, och du kan söka efter det på samma sätt som för värden från fälten **Externt dokumentnr**.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="8bd0e-114">Fältet är dock inte tillgängligt på journalrader.</span><span class="sxs-lookup"><span data-stu-id="8bd0e-114">But the field is not available on journal lines.</span></span>

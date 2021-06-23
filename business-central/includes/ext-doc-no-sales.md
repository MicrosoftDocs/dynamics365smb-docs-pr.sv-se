---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116009"
---
<span data-ttu-id="82db1-101">I försäljningsdokument och journaler kan du ange ett dokumentnummer som refererar till kundens nummersystem.</span><span class="sxs-lookup"><span data-stu-id="82db1-101">On sales documents and journals, you can specify a document number that refers to the customer's numbering system.</span></span> <!--You can enter a maximum of ten characters, both numbers and letters.--> <span data-ttu-id="82db1-102">Använd det här fältet för att registrera numret som kunden har tilldelat ordern, fakturan eller kreditnotan.</span><span class="sxs-lookup"><span data-stu-id="82db1-102">Use this field to record the number that the customer assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="82db1-103">Sedan kan du använda numret om du av någon anledning behöver söka efter den bokförda posten med hjälp av detta nummer.</span><span class="sxs-lookup"><span data-stu-id="82db1-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>  

<span data-ttu-id="82db1-104">Fältet **Ext. Dok.nr obligatoriskt** på sidan **Konfiguration av försäljning och kundreskontra** anger om det är obligatoriskt att ange ett externt dokumentnummer i fältet **Externt dokumentnr** i ett försäljningshuvud och fältet **Externt dokumentnr** på en redovisningsjournalrad.</span><span class="sxs-lookup"><span data-stu-id="82db1-104">The **Ext. Doc. No. Mandatory** field on the **Sales & Receivables Setup** page specifies whether it is mandatory to enter an external document number in the **External Document No.** field on a sales header and the **External Document No.** field on a general journal line.</span></span>

<span data-ttu-id="82db1-105">Om du markerar det här fältet kommer det inte att vara möjligt att bokföra en faktura eller en redovisningsjournalrad utan ett externt verifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="82db1-105">If you select this field, it will not be possible to post an invoice or a general journal line without an external document number.</span></span>

<span data-ttu-id="82db1-106">Det externa dokumentnumret inkluderas i de bokförda dokumenten där du kan söka på det aktuella numret.</span><span class="sxs-lookup"><span data-stu-id="82db1-106">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="82db1-107">Du kan även söka med hjälp av det externa dokumentnumret när du navigerar i kundreskontratransaktioner.</span><span class="sxs-lookup"><span data-stu-id="82db1-107">You can also search using the external document number when navigating on customer ledger entries.</span></span>

<span data-ttu-id="82db1-108">Olika sätt att hantera externa dokumentnummer är att använda fältet **Din referens**.</span><span class="sxs-lookup"><span data-stu-id="82db1-108">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="82db1-109">Om du använder fältet **Din referens** inkluderas numret i bokförda dokument, och du kan söka efter det på samma sätt som för värden från fälten **Externt dokumentnr**.</span><span class="sxs-lookup"><span data-stu-id="82db1-109">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="82db1-110">Fältet är dock inte tillgängligt på journalrader.</span><span class="sxs-lookup"><span data-stu-id="82db1-110">But the field is not available on journal lines.</span></span>

---
title: "Konfigurera föredragna metoder för att skicka försäljningsdokument | Microsoft Docs"
description: "Beskriver hur du ställer in varje kunds standardmetod för att skicka dokument, till exempel, e-post, PDF, elektroniska dokument och så vidare."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c18edefc22d96f2c4037f7f51cca488e04c35d92
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="d2c93-103">Skapa dokumentutskicksprofiler</span><span class="sxs-lookup"><span data-stu-id="d2c93-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="d2c93-104">Du kan skapa varje kund med en föredragen metod för att skicka försäljningsdokument så att du inte behöver välja alternativ varje gång som du väljer åtgärden **Bokför och skicka**.</span><span class="sxs-lookup"><span data-stu-id="d2c93-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="d2c93-105">I fönstret **Dokumentutskicksprofiler** konfigurerar du olika utskicksprofiler som du kan välja bland i fältet **Dokumentutskicksprofil** på ett kundkort.</span><span class="sxs-lookup"><span data-stu-id="d2c93-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="d2c93-106">Du kan markera kryssrutan **Standard** om du vill ange att dokumentutskicksprofilen är standardprofilen för alla kunder förutom för kunder som har fältet **Dokumentutskicksprofil** ifyllt med en annan utskicksprofil.</span><span class="sxs-lookup"><span data-stu-id="d2c93-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="d2c93-107">När du väljer åtgärden **Bokför och skicka** i ett försäljningsdokument visar dialogrutan **Bekräftelse för bokför och utskick** den utskicksprofil som använts, antingen den som angetts för kunden eller standardinställningen för alla kunder.</span><span class="sxs-lookup"><span data-stu-id="d2c93-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="d2c93-108">I dialogrutan kan du ändra utskicksprofilen för det specifika försäljningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="d2c93-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="d2c93-109">Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="d2c93-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="d2c93-110">Så här konfigurerar du en dokumentutskicksprofil</span><span class="sxs-lookup"><span data-stu-id="d2c93-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="d2c93-111">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Dokumentutskicksprofiler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2c93-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2c93-112">I fönstret **Dokumentutskicksprofiler** väljer du åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d2c93-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="d2c93-113">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="d2c93-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="d2c93-114">Så här anger du en utskicksprofil på ett kundkort</span><span class="sxs-lookup"><span data-stu-id="d2c93-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="d2c93-115">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kunder** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="d2c93-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2c93-116">Öppna kortet för kunden som du vill skapa en utskicksprofil för.</span><span class="sxs-lookup"><span data-stu-id="d2c93-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="d2c93-117">I fältet **Dokumentutskicksprofil** väljer du en profil som du har konfigurerat enligt beskrivningen i föregående procedur.</span><span class="sxs-lookup"><span data-stu-id="d2c93-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2c93-118">Se även</span><span class="sxs-lookup"><span data-stu-id="d2c93-118">See Also</span></span>
[<span data-ttu-id="d2c93-119">Konfigurera försäljning</span><span class="sxs-lookup"><span data-stu-id="d2c93-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="d2c93-120">Försäljning</span><span class="sxs-lookup"><span data-stu-id="d2c93-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d2c93-121">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2c93-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


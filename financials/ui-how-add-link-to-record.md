---
title: "Så här: Länka från poster till extern information eller program | Microsoft Docs"
description: "Koppla en hyperlänk till ett dokument eller en webbplats till en viss post, till exempel en kund eller ett dokument."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3ccedd0f5bede5dc692b1fec89d87e708047a622
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="a1d44-103">Lägga till länkar till webbplatser, dokument och program på poster</span><span class="sxs-lookup"><span data-stu-id="a1d44-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="a1d44-104">För en viss post, till exempel kund, dokument eller försäljningsorder, kan du lägga till en länk till ett externt dokument, webbplatser eller program.</span><span class="sxs-lookup"><span data-stu-id="a1d44-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="a1d44-105">Eller så kanske du vill ha en länk som öppnar ett nytt, tomt e-postmeddelande till en viss mottagare när du klickar på den.</span><span class="sxs-lookup"><span data-stu-id="a1d44-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="a1d44-106">Kortsidan för vissa kort, till exempel kund- och leverantörskorten, innehåller fältet **Hemsida** där en Internettadress (URL) kan anges.</span><span class="sxs-lookup"><span data-stu-id="a1d44-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="a1d44-107">Om du vill infoga andra länkar kan du använda den metod som beskrivs i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="a1d44-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="a1d44-108">Ett annat exempel är när du får utskrivna fakturor från leverantörer.</span><span class="sxs-lookup"><span data-stu-id="a1d44-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="a1d44-109">Du kan skanna in dem och spara dem som PDF-filer på en SharePoint-webbplats.</span><span class="sxs-lookup"><span data-stu-id="a1d44-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="a1d44-110">Därefter kan du skapa en länk från en inköpsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] till motsvarande faktura på SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a1d44-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="a1d44-111">Du kan också skapa en länk från ett artikelkort till motsvarande sida i leverantörens onlinekatalog.</span><span class="sxs-lookup"><span data-stu-id="a1d44-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>
  
## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="a1d44-112">Så här lägger du till en länk på en post:</span><span class="sxs-lookup"><span data-stu-id="a1d44-112">To add a link on a record</span></span>   
  
1.  <span data-ttu-id="a1d44-113">Öppna posten som du vill bifoga länken till, till exempel ett kundkort eller en försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="a1d44-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="a1d44-114">Om du vill bifoga länken till en specifik rad, till exempel till en journalrad, markerar du raden.</span><span class="sxs-lookup"><span data-stu-id="a1d44-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  
  
2.  <span data-ttu-id="a1d44-115">Välj åtgärden **länkar** för att öppna fönstret **länkar** som visar de aktuella länkarna som du lägger till posten.</span><span class="sxs-lookup"><span data-stu-id="a1d44-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="a1d44-116">För att lägga till en ny länk väljer du **+ny**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-116">To add a new link, choose **+new**.</span></span> 
  
4.  <span data-ttu-id="a1d44-117">I fältet **länkar** anger du</span><span class="sxs-lookup"><span data-stu-id="a1d44-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="a1d44-118">Om du vill länka till en fil på datorn eller i nätverket, anger du den fullständiga sökvägen och filnamnet som **C:My Documentsinvoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="a1d44-119">Länka till en webbplats genom att ange Internet-adressen (URL) som **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span> 
    -   <span data-ttu-id="a1d44-120">Länka till en webbplats genom att ange Internet-adressen (URL) som **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span> 
    -   <span data-ttu-id="a1d44-121">Länka till ett program genom att ange en sträng för att öppna programmet.</span><span class="sxs-lookup"><span data-stu-id="a1d44-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="a1d44-122">Om du vill starta OneNote med en viss sida skriver du **onenote:///C:My Documentstest.one**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="a1d44-123">Eller om du vill öppna Outlook med ett nytt, tomt e-postmeddelande till ett visst alias skriver du **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  
  
5.  <span data-ttu-id="a1d44-124">Ange information om länken i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-124">Fill in the **Description** field with information about the link.</span></span>  
  
6.  <span data-ttu-id="a1d44-125">Klicka på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-125">Choose the **Save** button.</span></span>  
  
## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="a1d44-126">Så här tar du bort en länk från en post:</span><span class="sxs-lookup"><span data-stu-id="a1d44-126">To delete a link from a record</span></span>  
  
<span data-ttu-id="a1d44-127">För att ta bort en länk kan du i fönstret **länkar** du ange **...** och **Ta bort**.</span><span class="sxs-lookup"><span data-stu-id="a1d44-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="a1d44-128">Om du tar bort en enstaka post (till exempel en försäljningsorderrad, en försäljningsorder eller ett kundkort) tas postens alla bifogade länkar bort.</span><span class="sxs-lookup"><span data-stu-id="a1d44-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="a1d44-129">Om användaren däremot tar bort poster med hjälp av ett batch-jobb **Ta bort fakturerade förs.order** sparas länkarna i databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d44-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="a1d44-130">Kör kodmodulen **Ta bort tomma postlänkar** för att ta bort länkarna från databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d44-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="a1d44-131">För att öppna denna sida väljer du ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rappor"), ange **Ta bort tomma postlänkar**, och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a1d44-131">To do this, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   
  
<!-- ### To run delete orphaned record links  
  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  
  
2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->
  
## <a name="see-also"></a><span data-ttu-id="a1d44-132">Se även</span><span class="sxs-lookup"><span data-stu-id="a1d44-132">See Also</span></span>  
<span data-ttu-id="a1d44-133">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1d44-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
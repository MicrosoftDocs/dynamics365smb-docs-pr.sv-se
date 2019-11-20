---
title: Skapa XML-portar som baseras på XML-scheman | Microsoft Docs
description: Använda XML-scheman för att ange ramverket för datautbyte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0d028206d1e17c7a1093cf2b93da02894909deb5
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554452"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="50235-103">Använda XML-scheman för att förbereda dataintegrationsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="50235-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="50235-104">Om du vill aktivera importera/exportera av data i XML-filer via ramverket för datautbyte i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du använda XML-schema för att definiera vilka dataelement du vill utbyta med [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50235-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50235-105">Du utför det här arbetet på sidan **Visningsprogram för XML-schema** genom att läsa in XML-schemafilen, välja de relevanta dataelementen och sedan att initialisera antingen en definition för datautbyte eller en XMLport.</span><span class="sxs-lookup"><span data-stu-id="50235-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="50235-106">När du har definierat vilka dataelement som ska ingå baserat på XML-schemat, kan du använda åtgärden **Generera XMLport** för att skapa ett XMLport-objekt.</span><span class="sxs-lookup"><span data-stu-id="50235-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="50235-107">Alternativt kan du använda åtgärden **Generera datautbytesdefinition** för att initialisera en definition för datautbyte som baseras på de valda dataelementen, som du sedan fyller i i ramverket för datautbyte.</span><span class="sxs-lookup"><span data-stu-id="50235-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="50235-108">Det skapar en post på sidan **Definitioner för bokföringsbyte** där du fortsätter genom att ange vilka element i filen som mappas till vilka fält i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50235-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50235-109">Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="50235-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="50235-110">Det här avsnittet innehåller följande procedurer:</span><span class="sxs-lookup"><span data-stu-id="50235-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="50235-111">Så här läser du in en XML-schemafil</span><span class="sxs-lookup"><span data-stu-id="50235-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="50235-112">Så här markerar eller avmarkerar du noder i ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="50235-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="50235-113">Så här skapar du en definition för datautbyte baserat på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="50235-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="50235-114">Så här skapar du en XMLport för filen som baseras på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="50235-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="50235-115">Så här importerar du en XMLport till Object Designer</span><span class="sxs-lookup"><span data-stu-id="50235-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="50235-116">Så här läser du in en XML-schemafil</span><span class="sxs-lookup"><span data-stu-id="50235-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="50235-117">Se till att den relevanta XML-schemafilen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="50235-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="50235-118">Filnamnstillägget är .xsd.</span><span class="sxs-lookup"><span data-stu-id="50235-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="50235-119">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **XML-scheman** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="50235-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="50235-120">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="50235-120">Choose the **New** action.</span></span>  

4.  <span data-ttu-id="50235-121">Fyll i fälten enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="50235-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="50235-122">Fält</span><span class="sxs-lookup"><span data-stu-id="50235-122">Field</span></span>|<span data-ttu-id="50235-123">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="50235-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="50235-124">**Kod**</span><span class="sxs-lookup"><span data-stu-id="50235-124">**Code**</span></span>|<span data-ttu-id="50235-125">Ange en kod som identifierar XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="50235-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="50235-126">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="50235-126">**Description**</span></span>|<span data-ttu-id="50235-127">Ange beskrivningen av XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="50235-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="50235-128">Fältet **Målnamnrymd** anger ett namnområde i XML-schemafilen som har laddats för raden.</span><span class="sxs-lookup"><span data-stu-id="50235-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="50235-129">Välj **Läs in schema**-åtgärden och välj sedan XML-schemafilen.</span><span class="sxs-lookup"><span data-stu-id="50235-129">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="50235-130">När filen har fylls i fylls resten av fälten på raden i med information från filen, och kryssrutan **Schemat är inläst** markeras.</span><span class="sxs-lookup"><span data-stu-id="50235-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="50235-131">Trädet med det inlästa xml-schemat är komprimerat som standard.</span><span class="sxs-lookup"><span data-stu-id="50235-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="50235-132">Du expanderar varje nod genom att välja **+** på noden.</span><span class="sxs-lookup"><span data-stu-id="50235-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="50235-133">Välj **Expandera alla** på menyfliken om du vill expandera alla noder.</span><span class="sxs-lookup"><span data-stu-id="50235-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="50235-134">Så här markerar eller avmarkerar du noder i ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="50235-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="50235-135">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Visningsprogram för XML-schema** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="50235-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="50235-136">Fyll i fälten i huvudet enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="50235-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="50235-137">Fält</span><span class="sxs-lookup"><span data-stu-id="50235-137">Field</span></span>|<span data-ttu-id="50235-138">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="50235-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="50235-139">**XML-schemakod**</span><span class="sxs-lookup"><span data-stu-id="50235-139">**XML Schema Code**</span></span>|<span data-ttu-id="50235-140">Ange den XML schemafil som du läste in i steg 5 i avsnittet ”Ladda XML-schemafilen”.</span><span class="sxs-lookup"><span data-stu-id="50235-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="50235-141">**Ny XMLport Nr.**</span><span class="sxs-lookup"><span data-stu-id="50235-141">**New XMLport No.**</span></span>|<span data-ttu-id="50235-142">Ange numret på den XMLport som skapas från XML-schemat när du väljer åtgärden **GenereraXMLport**.</span><span class="sxs-lookup"><span data-stu-id="50235-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="50235-143">Raderna fylls nu i med noder som representerar alla element i XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="50235-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="50235-144">Noder för element som är obligatoriska i överensstämmelse med XML-schemat markeras som standard.</span><span class="sxs-lookup"><span data-stu-id="50235-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="50235-145">På den första raden, i kolumnen **Nodnamn**, expanderar du noden **Dokument** och expandera sedan gradvis underliggande noder som du vill granska.</span><span class="sxs-lookup"><span data-stu-id="50235-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="50235-146">Högerklicka på en nod och välj sedan **Expandera alla**.</span><span class="sxs-lookup"><span data-stu-id="50235-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="50235-147">Välj någon av följande åtgärder för att ändra vilka noder som visas.</span><span class="sxs-lookup"><span data-stu-id="50235-147">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="50235-148">**Åtgärd**</span><span class="sxs-lookup"><span data-stu-id="50235-148">**Action**</span></span>|<span data-ttu-id="50235-149">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="50235-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="50235-150">**Visa alla**</span><span class="sxs-lookup"><span data-stu-id="50235-150">**Show All**</span></span>|<span data-ttu-id="50235-151">Alla noder visas.</span><span class="sxs-lookup"><span data-stu-id="50235-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="50235-152">**Dölj ej obligatoriska**</span><span class="sxs-lookup"><span data-stu-id="50235-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="50235-153">Endast noder som representerar element som krävs enligt XML-schemat visas.</span><span class="sxs-lookup"><span data-stu-id="50235-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="50235-154">Dessa noder har anges vanligtvis med **1** i fältet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="50235-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="50235-155">Välj **Visa alla** för att återföra vyn.</span><span class="sxs-lookup"><span data-stu-id="50235-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="50235-156">**Dölj ej valda**</span><span class="sxs-lookup"><span data-stu-id="50235-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="50235-157">Endast noder där kryssrutan **Vald** är markerad visas.</span><span class="sxs-lookup"><span data-stu-id="50235-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="50235-158">Välj **Visa alla** för att återföra vyn.</span><span class="sxs-lookup"><span data-stu-id="50235-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="50235-159">Välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="50235-159">Choose the **Edit** action.</span></span>  

6.  <span data-ttu-id="50235-160">I kryssrutan **Vald** anger du för varje nod om du vill att elementet ska stödjas i definitionen för datautbyte för den relaterade SEPA-bankfilen.</span><span class="sxs-lookup"><span data-stu-id="50235-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="50235-161">När du markerar en obligatorisk underordnad nod markeras även alla överordnade noder ovanför den.</span><span class="sxs-lookup"><span data-stu-id="50235-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="50235-162">Välj åtgärden **Markera alla obligatoriska element** för att välja alla noder igen som representerar element som är obligatoriska enligt XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="50235-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="50235-163">Välj åtgärden **Avmarkera alla** för att rensa alla val.</span><span class="sxs-lookup"><span data-stu-id="50235-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="50235-164">Fältet **Val** anger att noden har två eller fler syskonnoder som fungerar som alternativ.</span><span class="sxs-lookup"><span data-stu-id="50235-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="50235-165">Så här skapar du en definition för datautbyte baserat på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="50235-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="50235-166">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **XML-scheman** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="50235-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="50235-167">Välj relevant XML-schema och välj sedan åtgärden **Öppna XML-schemavisare**.</span><span class="sxs-lookup"><span data-stu-id="50235-167">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="50235-168">Se till att de relevanta noderna har markerats.</span><span class="sxs-lookup"><span data-stu-id="50235-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="50235-169">Mer information finns i avsnittet ”Så här markerar eller avmarkerar du noder i ett XML-schema”.</span><span class="sxs-lookup"><span data-stu-id="50235-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="50235-170">På sidan **Öppna XML-schemavisare** väljer du åtgärden **Generera datautbytesdefinition**.</span><span class="sxs-lookup"><span data-stu-id="50235-170">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="50235-171">Datautbytesdefinitionen skapas på sidan **Definitioner för bokföringsbyte** som du kan fylla i genom att ange vilka element i filen som ska mappas till respektive fält i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50235-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50235-172">Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="50235-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="50235-173">Du kan också använda funktionen **Hämta filstruktur** från sidan **Definitioner för bokföringsbyte** som använder funktionen på sidan **Visningsprogram för XML-schema** för att autofylla snabbfliken **Kolumndefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="50235-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="50235-174">Så här skapar du en XMLport som baseras på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="50235-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="50235-175">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **XML-scheman** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="50235-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="50235-176">Välj relevant XML-schema och välj sedan åtgärden **Öppna XML-schemavisare**.</span><span class="sxs-lookup"><span data-stu-id="50235-176">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="50235-177">I fältet **Ny XMLport Nr.**</span><span class="sxs-lookup"><span data-stu-id="50235-177">In the **New XMLport No.**</span></span> <span data-ttu-id="50235-178">anger du numret som den nya XMLport-artikeln ska få när den skapas.</span><span class="sxs-lookup"><span data-stu-id="50235-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="50235-179">Se till att de relevanta noderna har markerats.</span><span class="sxs-lookup"><span data-stu-id="50235-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="50235-180">Mer information finns i avsnittet ”Så här markerar eller avmarkerar du noder i ett XML-schema”.</span><span class="sxs-lookup"><span data-stu-id="50235-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="50235-181">Välj åtgärden **Generera XMLport** och spara objektet som en .txt-fil på lämplig plats.</span><span class="sxs-lookup"><span data-stu-id="50235-181">Choose the **Generate XMLport** action, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="50235-182">Importera nya XMLport i [!INCLUDE[d365fin](includes/d365fin_md.md)] utvecklingsmiljö och kompilera den.</span><span class="sxs-lookup"><span data-stu-id="50235-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="50235-183">Se även</span><span class="sxs-lookup"><span data-stu-id="50235-183">See Also</span></span>  
<span data-ttu-id="50235-184">[Skapa dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="50235-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="50235-185">[Exportera betalningar till en bankfil](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="50235-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="50235-186">[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="50235-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="50235-187">Om ramverket för datautbyte</span><span class="sxs-lookup"><span data-stu-id="50235-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)

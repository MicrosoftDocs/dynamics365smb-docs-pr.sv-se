---
title: Använda XML-scheman för att förbereda dataintegreringsdefinitioner
description: Använd XML-scheman för att konfigurera ramverket för dokumentbyten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70e80403175c6a77d120a3b405b1b5758410c227
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781368"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="3bc62-103">Använd XML-scheman för att förbereda definitioner för databyten</span><span class="sxs-lookup"><span data-stu-id="3bc62-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="3bc62-104">Om du vill aktivera importera/exportera av data i XML-filer via ramverket för datautbyte i [!INCLUDE[prod_short](includes/prod_short.md)], kan du använda XML-schema för att definiera vilka dataelement du vill utbyta med [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3bc62-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3bc62-105">Du utför detta arbete på sidan **XML-schemavisning** genom att ladda XML-schemafilen, välja tillhörande dataelement samt därefter initialisera en definition för databyte.</span><span class="sxs-lookup"><span data-stu-id="3bc62-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="3bc62-106">När du har definierat vilka dataelement som sa inkluderas baserat på XML-schemat kan du använda åtgärden **Generera definition för databyte** för att initialisera en definition för databyte baserat på valda dataelement som du sedan slutför i ramverket för databyten.</span><span class="sxs-lookup"><span data-stu-id="3bc62-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="3bc62-107">Det skapar en post på sidan **Definitioner för bokföringsbyte** där du fortsätter genom att ange vilka element i filen som mappas till vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3bc62-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3bc62-108">Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="3bc62-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="3bc62-109">Det här avsnittet innehåller följande procedurer:</span><span class="sxs-lookup"><span data-stu-id="3bc62-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="3bc62-110">Så här läser du in en XML-schemafil</span><span class="sxs-lookup"><span data-stu-id="3bc62-110">To load an XML schema file</span></span>  

- <span data-ttu-id="3bc62-111">Så här markerar eller avmarkerar du noder i ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="3bc62-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="3bc62-112">Så här skapar du en definition för datautbyte baserat på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="3bc62-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="3bc62-113">Så här läser du in en XML-schemafil</span><span class="sxs-lookup"><span data-stu-id="3bc62-113">To load an XML schema file</span></span>

1. <span data-ttu-id="3bc62-114">Se till att den relevanta XML-schemafilen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="3bc62-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="3bc62-115">Filnamnstillägget är .xsd.</span><span class="sxs-lookup"><span data-stu-id="3bc62-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="3bc62-116">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **XML-scheman** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3bc62-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="3bc62-117">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="3bc62-118">Fyll i fälten enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="3bc62-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="3bc62-119">Fält</span><span class="sxs-lookup"><span data-stu-id="3bc62-119">Field</span></span>|<span data-ttu-id="3bc62-120">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3bc62-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3bc62-121">**Kod**</span><span class="sxs-lookup"><span data-stu-id="3bc62-121">**Code**</span></span>|<span data-ttu-id="3bc62-122">Ange en kod som identifierar XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="3bc62-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="3bc62-123">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="3bc62-123">**Description**</span></span>|<span data-ttu-id="3bc62-124">Ange beskrivningen av XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="3bc62-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="3bc62-125">Fältet **Målnamnrymd** anger ett namnområde i XML-schemafilen som har laddats för raden.</span><span class="sxs-lookup"><span data-stu-id="3bc62-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="3bc62-126">Välj **Läs in schema**-åtgärden och välj sedan XML-schemafilen.</span><span class="sxs-lookup"><span data-stu-id="3bc62-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="3bc62-127">När filen har fylls i fylls resten av fälten på raden i med information från filen, och kryssrutan **Schemat är inläst** markeras.</span><span class="sxs-lookup"><span data-stu-id="3bc62-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="3bc62-128">Trädet med det inlästa xml-schemat är komprimerat som standard.</span><span class="sxs-lookup"><span data-stu-id="3bc62-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="3bc62-129">Du expanderar varje nod genom att välja **+** på noden.</span><span class="sxs-lookup"><span data-stu-id="3bc62-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="3bc62-130">Välj **Expandera alla** på menyfliken om du vill expandera alla noder.</span><span class="sxs-lookup"><span data-stu-id="3bc62-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="3bc62-131">Så här markerar eller avmarkerar du noder i ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="3bc62-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="3bc62-132">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **XML-schemavisare** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3bc62-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="3bc62-133">Fyll i fälten i huvudet enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="3bc62-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="3bc62-134">Fält</span><span class="sxs-lookup"><span data-stu-id="3bc62-134">Field</span></span>|<span data-ttu-id="3bc62-135">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3bc62-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="3bc62-136">**XML-schemakod**</span><span class="sxs-lookup"><span data-stu-id="3bc62-136">**XML Schema Code**</span></span>|<span data-ttu-id="3bc62-137">Ange den XML-schemafil som du laddade i steg 5 i avsnittet "För att ladda en XML-schemafil".</span><span class="sxs-lookup"><span data-stu-id="3bc62-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="3bc62-138">**Ny XMLport Nr.**</span><span class="sxs-lookup"><span data-stu-id="3bc62-138">**New XMLport No.**</span></span>|<span data-ttu-id="3bc62-139">Ange numret på den XMLport som skapas från XML-schemat när du väljer åtgärden **GenereraXMLport**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="3bc62-140">Raderna fylls nu i med noder som representerar alla element i XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="3bc62-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="3bc62-141">Noder för element som är obligatoriska i överensstämmelse med XML-schemat markeras som standard.</span><span class="sxs-lookup"><span data-stu-id="3bc62-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="3bc62-142">På den första raden, i kolumnen **Nodnamn**, expanderar du noden **Dokument** och expandera sedan gradvis underliggande noder som du vill granska.</span><span class="sxs-lookup"><span data-stu-id="3bc62-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="3bc62-143">Högerklicka på en nod och välj sedan **Expandera alla**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="3bc62-144">Välj någon av följande åtgärder för att ändra vilka noder som visas.</span><span class="sxs-lookup"><span data-stu-id="3bc62-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="3bc62-145">**Åtgärd**</span><span class="sxs-lookup"><span data-stu-id="3bc62-145">**Action**</span></span>|<span data-ttu-id="3bc62-146">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3bc62-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="3bc62-147">**Visa alla**</span><span class="sxs-lookup"><span data-stu-id="3bc62-147">**Show All**</span></span>|<span data-ttu-id="3bc62-148">Alla noder visas.</span><span class="sxs-lookup"><span data-stu-id="3bc62-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="3bc62-149">**Dölj ej obligatoriska**</span><span class="sxs-lookup"><span data-stu-id="3bc62-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="3bc62-150">Endast noder som representerar element som krävs enligt XML-schemat visas.</span><span class="sxs-lookup"><span data-stu-id="3bc62-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="3bc62-151">Dessa noder har anges vanligtvis med **1** i fältet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="3bc62-152">Välj **Visa alla** för att återföra vyn.</span><span class="sxs-lookup"><span data-stu-id="3bc62-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="3bc62-153">**Dölj ej valda**</span><span class="sxs-lookup"><span data-stu-id="3bc62-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="3bc62-154">Endast noder där kryssrutan **Vald** är markerad visas.</span><span class="sxs-lookup"><span data-stu-id="3bc62-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="3bc62-155">Välj **Visa alla** för att återföra vyn.</span><span class="sxs-lookup"><span data-stu-id="3bc62-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="3bc62-156">Välj åtgärden **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="3bc62-157">I kryssrutan **Vald** anger du för varje nod om du vill att elementet ska stödjas i definitionen för datautbyte för den relaterade SEPA-bankfilen.</span><span class="sxs-lookup"><span data-stu-id="3bc62-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="3bc62-158">När du markerar en obligatorisk underordnad nod markeras även alla överordnade noder ovanför den.</span><span class="sxs-lookup"><span data-stu-id="3bc62-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="3bc62-159">Välj åtgärden **Markera alla obligatoriska element** för att välja alla noder igen som representerar element som är obligatoriska enligt XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="3bc62-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="3bc62-160">Välj åtgärden **Avmarkera alla** för att rensa alla val.</span><span class="sxs-lookup"><span data-stu-id="3bc62-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="3bc62-161">Fältet **Val** anger att noden har två eller fler syskonnoder som fungerar som alternativ.</span><span class="sxs-lookup"><span data-stu-id="3bc62-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="3bc62-162">Så här skapar du en definition för datautbyte baserat på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="3bc62-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="3bc62-163">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **XML-scheman** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="3bc62-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="3bc62-164">Välj relevant XML-schema och välj sedan åtgärden **Öppna XML-schemavisare**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="3bc62-165">Se till att de relevanta noderna har markerats.</span><span class="sxs-lookup"><span data-stu-id="3bc62-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="3bc62-166">Mer information finns i avsnittet "För att välja eller rensa noder i XML-schema".</span><span class="sxs-lookup"><span data-stu-id="3bc62-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="3bc62-167">På sidan **Öppna XML-schemavisare** väljer du åtgärden **Generera datautbytesdefinition**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="3bc62-168">Datautbytesdefinitionen skapas på sidan **Definitioner för bokföringsbyte** som du kan fylla i genom att ange vilka element i filen som ska mappas till respektive fält i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3bc62-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3bc62-169">Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="3bc62-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="3bc62-170">Du kan också använda funktionen **Hämta filstruktur** från sidan **Definitioner för bokföringsbyte** som använder funktionen på sidan **Visningsprogram för XML-schema** för att autofylla snabbfliken **Kolumndefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="3bc62-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="3bc62-171">Under 2019 års utgivningsvåg 1 kunde du generera en XMLport baserat på schemat och sedan importera denna i din lösning.</span><span class="sxs-lookup"><span data-stu-id="3bc62-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="3bc62-172">Detta stöds inte längre.</span><span class="sxs-lookup"><span data-stu-id="3bc62-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bc62-173">Se även</span><span class="sxs-lookup"><span data-stu-id="3bc62-173">See Also</span></span>

[<span data-ttu-id="3bc62-174">Skapa dataintegreringsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="3bc62-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="3bc62-175">Exportera betalningar till en bankfil</span><span class="sxs-lookup"><span data-stu-id="3bc62-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="3bc62-176">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="3bc62-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="3bc62-177">Om ramverket för datautbyte</span><span class="sxs-lookup"><span data-stu-id="3bc62-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
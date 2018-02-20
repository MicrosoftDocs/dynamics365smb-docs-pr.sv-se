---
title: "Skapa XML-portar som baseras på XML-scheman | Microsoft Docs"
description: "Använda XML-scheman för att ange ramverket för datautbyte."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 06e0de9409fa26d18f051d84b39d021227a55191
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="a1cee-103">Använda XML-scheman för att förbereda dataintegrationsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="a1cee-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="a1cee-104">Om du vill aktivera importera/exportera av data i XML-filer via ramverket för datautbyte i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du använda XML-schema för att definiera vilka dataelement du vill utbyta med [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a1cee-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a1cee-105">Du utför det här arbetet i fönstret **Visningsprogram för XML-schema** genom att läsa in XML-schemafilen, välja de relevanta dataelementen och sedan att initiera antingen en definition för datautbyte eller en XMLport.</span><span class="sxs-lookup"><span data-stu-id="a1cee-105">You perform this work in the **XML Schema Viewer** window by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="a1cee-106">När du har definierat vilka dataelement som ska ingå baserat på XML-schemat, kan du använda åtgärden **Generera XMLPort** för att skapa ett XMLport-objekt.</span><span class="sxs-lookup"><span data-stu-id="a1cee-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="a1cee-107">Alternativt kan du använda åtgärden **Generera datautbytesdefinition** för att initiera en definition för datautbyte som baseras på de valda dataelementen, som du sedan fyller i i ramverket för datautbyte.</span><span class="sxs-lookup"><span data-stu-id="a1cee-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="a1cee-108">Det skapar en post i fönstret **Definitioner för bokföringsbyte** där du fortsätter genom att ange vilka element i filen som mappas till vilka fält i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a1cee-108">This creates a record in the **Posting Exchange Definition** window where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a1cee-109">Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a1cee-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="a1cee-110">Det här avsnittet innehåller följande procedurer:</span><span class="sxs-lookup"><span data-stu-id="a1cee-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="a1cee-111">Så här läser du in en XML-schemafil</span><span class="sxs-lookup"><span data-stu-id="a1cee-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="a1cee-112">Så här markerar eller avmarkerar du noder i ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="a1cee-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="a1cee-113">Så här skapar du en definition för datautbyte baserat på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="a1cee-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="a1cee-114">Så här skapar du en XMLport för filen som baseras på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="a1cee-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="a1cee-115">Så här importerar du en XMLport till Object Designer</span><span class="sxs-lookup"><span data-stu-id="a1cee-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="a1cee-116">Så här läser du in en XML-schemafil</span><span class="sxs-lookup"><span data-stu-id="a1cee-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="a1cee-117">Se till att den relevanta XML-schemafilen är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="a1cee-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="a1cee-118">Filnamnstillägget är .xsd.</span><span class="sxs-lookup"><span data-stu-id="a1cee-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="a1cee-119">I rutan **Sök** anger du **XML-scheman** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a1cee-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="a1cee-120">På fliken **Start** i gruppen **Ny** väljer du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="a1cee-121">Fyll i fälten enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="a1cee-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a1cee-122">Fält</span><span class="sxs-lookup"><span data-stu-id="a1cee-122">Field</span></span>|<span data-ttu-id="a1cee-123">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a1cee-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a1cee-124">**Kod**</span><span class="sxs-lookup"><span data-stu-id="a1cee-124">**Code**</span></span>|<span data-ttu-id="a1cee-125">Ange en kod som identifierar XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="a1cee-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="a1cee-126">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="a1cee-126">**Description**</span></span>|<span data-ttu-id="a1cee-127">Ange beskrivningen av XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="a1cee-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="a1cee-128">Fältet **Målnamnrymd** anger ett namnområde i XML-schemafilen som har laddats för raden.</span><span class="sxs-lookup"><span data-stu-id="a1cee-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="a1cee-129">Välj **Läs in schema** på fliken **Start** i gruppen **Process** och välj sedan XML-schemafilen.</span><span class="sxs-lookup"><span data-stu-id="a1cee-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="a1cee-130">När filen har fylls i fylls resten av fälten på raden i med information från filen, och kryssrutan **Schemat är inläst** markeras.</span><span class="sxs-lookup"><span data-stu-id="a1cee-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a1cee-131">Trädet med det inlästa xml-schemat är komprimerat som standard.</span><span class="sxs-lookup"><span data-stu-id="a1cee-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="a1cee-132">Du expanderar varje nod genom att välja **+** på noden.</span><span class="sxs-lookup"><span data-stu-id="a1cee-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="a1cee-133">Välj **Expandera alla** på menyfliken om du vill expandera alla noder.</span><span class="sxs-lookup"><span data-stu-id="a1cee-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="a1cee-134">Så här markerar eller avmarkerar du noder i ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="a1cee-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="a1cee-135">I rutan **Sök** anger du **Visningsprogram för XML-schema** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a1cee-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a1cee-136">Fyll i fälten i huvudet enligt beskrivningen i följande tabell.</span><span class="sxs-lookup"><span data-stu-id="a1cee-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="a1cee-137">Fält</span><span class="sxs-lookup"><span data-stu-id="a1cee-137">Field</span></span>|<span data-ttu-id="a1cee-138">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a1cee-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a1cee-139">**XML-schemakod**</span><span class="sxs-lookup"><span data-stu-id="a1cee-139">**XML Schema Code**</span></span>|<span data-ttu-id="a1cee-140">Ange den XML schemafil som du läste in i steg 5 i avsnittet ”Ladda XML-schemafilen”.</span><span class="sxs-lookup"><span data-stu-id="a1cee-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="a1cee-141">**Nytt XML-portnr**</span><span class="sxs-lookup"><span data-stu-id="a1cee-141">**New XMLport No.**</span></span>|<span data-ttu-id="a1cee-142">Ange numret på den XMLport som skapas från XML-schemat när du väljer åtgärden **Generera XMLport** i fönstret .</span><span class="sxs-lookup"><span data-stu-id="a1cee-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="a1cee-143">Raderna fylls nu i med noder som representerar alla element i XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="a1cee-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="a1cee-144">Noder för element som är obligatoriska i överensstämmelse med XML-schemat markeras som standard.</span><span class="sxs-lookup"><span data-stu-id="a1cee-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="a1cee-145">På den första raden, i kolumnen **Nodnamn**, expanderar du noden **Dokument** och expandera sedan gradvis underliggande noder som du vill granska.</span><span class="sxs-lookup"><span data-stu-id="a1cee-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="a1cee-146">Högerklicka på en nod och välj sedan **Expandera alla**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="a1cee-147">På fliken **Hem** i gruppen **Visa** väljer du någon av följande åtgärder för att ändra vilka noder som visas.</span><span class="sxs-lookup"><span data-stu-id="a1cee-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="a1cee-148">**Åtgärd**</span><span class="sxs-lookup"><span data-stu-id="a1cee-148">**Action**</span></span>|<span data-ttu-id="a1cee-149">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a1cee-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="a1cee-150">**Visa alla**</span><span class="sxs-lookup"><span data-stu-id="a1cee-150">**Show All**</span></span>|<span data-ttu-id="a1cee-151">Alla noder visas.</span><span class="sxs-lookup"><span data-stu-id="a1cee-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="a1cee-152">**Dölj ej obligatoriska**</span><span class="sxs-lookup"><span data-stu-id="a1cee-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="a1cee-153">Endast noder som representerar element som krävs enligt XML-schemat visas.</span><span class="sxs-lookup"><span data-stu-id="a1cee-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="a1cee-154">Dessa noder har anges vanligtvis med **1** i fältet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="a1cee-155">Välj **Visa alla** för att återföra vyn.</span><span class="sxs-lookup"><span data-stu-id="a1cee-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="a1cee-156">**Dölj ej valda**</span><span class="sxs-lookup"><span data-stu-id="a1cee-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="a1cee-157">Endast noder där kryssrutan **Vald** är markerad visas.</span><span class="sxs-lookup"><span data-stu-id="a1cee-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="a1cee-158">Välj **Visa alla** för att återföra vyn.</span><span class="sxs-lookup"><span data-stu-id="a1cee-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="a1cee-159">På fliken **Start** i gruppen **Hantera** väljer du **Redigera**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="a1cee-160">I kryssrutan **Vald** anger du för varje nod om du vill att elementet ska stödjas i definitionen för datautbyte för den relaterade SEPA-bankfilen.</span><span class="sxs-lookup"><span data-stu-id="a1cee-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a1cee-161">När du markerar en obligatorisk underordnad nod markeras även alla överordnade noder ovanför den.</span><span class="sxs-lookup"><span data-stu-id="a1cee-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="a1cee-162">Välj åtgärden **Markera alla obligatoriska element** för att välja alla noder igen som representerar element som är obligatoriska enligt XML-schemat.</span><span class="sxs-lookup"><span data-stu-id="a1cee-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="a1cee-163">Välj åtgärden **Avmarkera alla** för att rensa alla val.</span><span class="sxs-lookup"><span data-stu-id="a1cee-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="a1cee-164">Fältet **Val** anger att noden har två eller fler syskonnoder som fungerar som alternativ.</span><span class="sxs-lookup"><span data-stu-id="a1cee-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="a1cee-165">Så här skapar du en definition för datautbyte baserat på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="a1cee-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="a1cee-166">I rutan **Sök** anger du **XML-scheman** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a1cee-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a1cee-167">Markera ett lämpligt XML-schema och välj **Öppna XML-schemavisare** på fliken **Hem** i gruppen **Behandla**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="a1cee-168">Se till att de relevanta noderna har markerats.</span><span class="sxs-lookup"><span data-stu-id="a1cee-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="a1cee-169">Mer information finns i avsnittet ”Så här markerar eller avmarkerar du noder i ett XML-schema”.</span><span class="sxs-lookup"><span data-stu-id="a1cee-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="a1cee-170">I fönstret **Visningsprogram för XML-schema** på fliken **Start** i gruppen **Process** väljer du **Generera datautbytesdefinition**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-170">In the **XML Schema Viewer** window, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="a1cee-171">Datautbytesdefinitionen skapas i fönstret **Definitioner för bokföringsbyte** som du kan fylla i genom att ange vilka element i filen som ska mappas till respektive fält i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a1cee-171">A data exchange definition is created in the **Posting Exchange Definition** window, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a1cee-172">Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a1cee-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a1cee-173">Du kan också använda funktionen **Hämta filstruktur** från fönstret **Definitioner för bokföringsbyte** som använder funktionen i fönstret **Visningsprogram för XML-schema** för att autofylla snabbfliken **Kolumndefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** window, which uses the functionality of the **XML Schema Viewer** window to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="a1cee-174">Så här skapar du en XMLport som baseras på ett XML-schema</span><span class="sxs-lookup"><span data-stu-id="a1cee-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="a1cee-175">I rutan **Sök** anger du **XML-scheman** och väljer sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="a1cee-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="a1cee-176">Markera ett lämpligt XML-schema och välj **Öppna XML-schemavisare** på fliken **Hem** i gruppen **Behandla**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="a1cee-177">I fältet **Nytt XML-portnr**</span><span class="sxs-lookup"><span data-stu-id="a1cee-177">In the **New XMLport No.**</span></span> <span data-ttu-id="a1cee-178">anger du numret som den nya XMLport-artikeln ska få när den skapas.</span><span class="sxs-lookup"><span data-stu-id="a1cee-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="a1cee-179">Se till att de relevanta noderna har markerats.</span><span class="sxs-lookup"><span data-stu-id="a1cee-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="a1cee-180">Mer information finns i avsnittet ”Så här markerar eller avmarkerar du noder i ett XML-schema”.</span><span class="sxs-lookup"><span data-stu-id="a1cee-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="a1cee-181">Välj **Generera XMLport** och spara objektet som en TXT-fil på ett lämpligt lagerställe på fliken **Hem** i gruppen **Bearbeta**.</span><span class="sxs-lookup"><span data-stu-id="a1cee-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="a1cee-182">Importera nya XML-porten till den [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment och kompilera.</span><span class="sxs-lookup"><span data-stu-id="a1cee-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1cee-183">Se även</span><span class="sxs-lookup"><span data-stu-id="a1cee-183">See Also</span></span>  
<span data-ttu-id="a1cee-184">[Skapa dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="a1cee-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="a1cee-185">[Exportera betalningar till en bankfil](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="a1cee-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="a1cee-186">[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="a1cee-186">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="a1cee-187">Om ramverket för datautbyte</span><span class="sxs-lookup"><span data-stu-id="a1cee-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)


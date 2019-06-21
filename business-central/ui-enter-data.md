---
title: Hur du anger du data i fält | Microsoft Docs
description: Lär dig mer om allmänna funktioner som hjälper dig att ange data i fälten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/03/2019
ms.author: jswymer
ms.openlocfilehash: d0fac96313b41a0e41ea96ab4fedd25565498f12
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621166"
---
# <a name="entering-data"></a><span data-ttu-id="02979-103">Ange data</span><span class="sxs-lookup"><span data-stu-id="02979-103">Entering Data</span></span>

<span data-ttu-id="02979-104">Det finns många allmänna funktioner som hjälper dig att ange data lättare, snabbare och mer exakt.</span><span class="sxs-lookup"><span data-stu-id="02979-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="02979-105">Dessa allmänna funktioner för dataregistrering beskrivs i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="02979-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="02979-106">Kortkommandon</span><span class="sxs-lookup"><span data-stu-id="02979-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="02979-107">Det finns flera kortkommandon som gör att du kan arbeta ”utan mus” och snabba på din datainmatning, särskilt med storskaliga och återkommande textinmatningsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="02979-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="02979-108">Mer information om genvägar finns i [Kortkommandon](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="02979-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="02979-109">I den här artikeln beskrivs några genvägar.</span><span class="sxs-lookup"><span data-stu-id="02979-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="02979-110">Påskynda datainmatning med snabbinmatning</span><span class="sxs-lookup"><span data-stu-id="02979-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="02979-111">Snabbinmatning är en funktion som skapats för datainmatning vid användning av tangentbordet.</span><span class="sxs-lookup"><span data-stu-id="02979-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="02979-112">Snabbinmatning fungerar på fält (t.ex. på kortsidorna) och i listor (rader och kolumner).</span><span class="sxs-lookup"><span data-stu-id="02979-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="02979-113">Det är bra när återkommande textinmatningsuppgifter utförs som behöver skapa flera poster i taget, till exempel en uppsättning försäljningsorder eller registrering av nya artiklar.</span><span class="sxs-lookup"><span data-stu-id="02979-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="02979-114">Du kanske redan känner till att använda Tabb-tangenten för att gå från ett fält på en sida till nästa redigerbara fält.</span><span class="sxs-lookup"><span data-stu-id="02979-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="02979-115">Nackdelen med att använda Tabb-tangenten är att det alltid går sekventiellt till nästa fält.</span><span class="sxs-lookup"><span data-stu-id="02979-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="02979-116">Snabbinmatning låter dig ändra den här sökvägen.</span><span class="sxs-lookup"><span data-stu-id="02979-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="02979-117">Med snabbinmatning använder du Retur-knappen för att navigera i de fält som du är intresserad av, hoppar över skrivskyddade fält och fält som du vanligtvis inte fyller i.</span><span class="sxs-lookup"><span data-stu-id="02979-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="02979-118">Du kanske redan har upptäckt denna funktion på vissa sidor.</span><span class="sxs-lookup"><span data-stu-id="02979-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="02979-119">Detta beror på att programmet redan anger vilka fält som ska inkluderas när du trycker på Retur och vilka som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="02979-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="02979-120">Du kan anpassa snabbinmatning genom att anpassa arbetsytan och optimera hur du anger data på varje sida.</span><span class="sxs-lookup"><span data-stu-id="02979-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="02979-121">Hur snabbinmatning fungerar</span><span class="sxs-lookup"><span data-stu-id="02979-121">How Quick Entry Works</span></span>

<span data-ttu-id="02979-122">Varje fält kan markeras som antingen *inkluderas i snabbinmatning* eller *exkluderas från snabbinmatning*.</span><span class="sxs-lookup"><span data-stu-id="02979-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="02979-123">Som inkluderas i snabbinmatning inkluderas i sökvägen när du trycker på Retur. fält som exkluderas från snabbinmatning kommer inte att göra detta.</span><span class="sxs-lookup"><span data-stu-id="02979-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="02979-124">När du är klar med att ange data i ett fält trycker du bara på Retur för att bekräfta ändringarna och gå till nästa fält.</span><span class="sxs-lookup"><span data-stu-id="02979-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="02979-125">Om du vill byta riktning och fortsätter till föregående fält trycker du på Shift + Retur.</span><span class="sxs-lookup"><span data-stu-id="02979-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="02979-126">Mer information om genvägar finns i [kortkommandon på tangentbord för snabbinmatning för fält](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="02979-126">For more information about shortcuts, see [Quick Entry Keyboard Shortcuts for Fields](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="02979-127">Tips och råd</span><span class="sxs-lookup"><span data-stu-id="02979-127">Tips and tricks</span></span>
<span data-ttu-id="02979-128">Nedan finns användbar information om hur du använder snabbinmatning.</span><span class="sxs-lookup"><span data-stu-id="02979-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="02979-129">Den är tillgänglig för alla fält som kan redigeras.</span><span class="sxs-lookup"><span data-stu-id="02979-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="02979-130">Den fungerar även i kolumner och rader.</span><span class="sxs-lookup"><span data-stu-id="02979-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="02979-131">Den hindrar inte från att komma åt andra element på en sida, till exempel åtgärder.</span><span class="sxs-lookup"><span data-stu-id="02979-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="02979-132">Dessa är tillgängliga genom att använda Tabb och Shift + Tabb.</span><span class="sxs-lookup"><span data-stu-id="02979-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="02979-133">Snabbflikarna behöver inte expanderas för att snabbinmatning ska fungera.</span><span class="sxs-lookup"><span data-stu-id="02979-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="02979-134">Om nästa snabbinmatningsfält finns i en komprimerad snabbflik kommer den snabbfliken automatiskt expandera och fokusera på det tilldelade fältet.</span><span class="sxs-lookup"><span data-stu-id="02979-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="02979-135">Snabbinmatning fungerar oavsett om fälten är obligatoriska.</span><span class="sxs-lookup"><span data-stu-id="02979-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="02979-136">Så det är en bra idé att kontrollera att obligatoriska fält är inkluderade i snabbinmatning.</span><span class="sxs-lookup"><span data-stu-id="02979-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="02979-137">Som standard inkluderas de flesta fält i snabbinmatning.</span><span class="sxs-lookup"><span data-stu-id="02979-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="02979-138">Så i början kommer uppgiften troligen att utesluta fält från snabbinmatning.</span><span class="sxs-lookup"><span data-stu-id="02979-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="02979-139">Så här ändrar du snabbinmatningsfält</span><span class="sxs-lookup"><span data-stu-id="02979-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="02979-140">Om du vill ändra vilka fält som ska inkluderas eller exkluderas i snabbinmatning på en sida, kan du använda anpassning.</span><span class="sxs-lookup"><span data-stu-id="02979-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="02979-141">Starta anpassning genom att välja ikonen ![inställningar](media/ui-experience/settings_icon_small.png "ikonen inställningar för rollcenter") och sedan **anpassa**.</span><span class="sxs-lookup"><span data-stu-id="02979-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="02979-142">Välj ett fält som du vill ändra, eller i listor, väljer du motsvarande kolumnrubrik eller väljer antingen **inkludera i snabbinmatning** eller **exkludera snabbinmatning**.</span><span class="sxs-lookup"><span data-stu-id="02979-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="02979-143">Mer information om anpassning finns i [Anpassa arbetsyta](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="02979-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="02979-144">Obligatoriska fält</span><span class="sxs-lookup"><span data-stu-id="02979-144">Mandatory Fields</span></span>

<span data-ttu-id="02979-145">När du anger data på sidor markeras vissa fält med en röd asterisk.</span><span class="sxs-lookup"><span data-stu-id="02979-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="02979-146">Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.</span><span class="sxs-lookup"><span data-stu-id="02979-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="02979-147">Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan.</span><span class="sxs-lookup"><span data-stu-id="02979-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="02979-148">Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.</span><span class="sxs-lookup"><span data-stu-id="02979-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="02979-149">Söka efter data allt eftersom du skriver</span><span class="sxs-lookup"><span data-stu-id="02979-149">Finding Data As You Type</span></span>

 <span data-ttu-id="02979-150">När du börjar skriva tecken i ett fält visas en listruta med möjliga fältvärden.</span><span class="sxs-lookup"><span data-stu-id="02979-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="02979-151">Listan ändras allt eftersom du skriver fler tecken, och du kan välja rätt värde när det visas.</span><span class="sxs-lookup"><span data-stu-id="02979-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="02979-152">Många fält har en nedpil-knapp som du kan välja.</span><span class="sxs-lookup"><span data-stu-id="02979-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="02979-153">Du kan välja pilen om du vill visa en lista med data som är tillgängliga för fältet.</span><span class="sxs-lookup"><span data-stu-id="02979-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="02979-154">Knappen har två funktioner beroende på typen av fält:</span><span class="sxs-lookup"><span data-stu-id="02979-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="02979-155">Sökning – Visar information från en annan tabell som du kan infoga i fältet.</span><span class="sxs-lookup"><span data-stu-id="02979-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="02979-156">Du kan bara välja en i taget.</span><span class="sxs-lookup"><span data-stu-id="02979-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="02979-157">Lista – Visar den uppsättning alternativ (fasta val) som finns för fältet.</span><span class="sxs-lookup"><span data-stu-id="02979-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="02979-158">Du kan bara markera ett av alternativen.</span><span class="sxs-lookup"><span data-stu-id="02979-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="02979-159">Kopiera och klistra in fält och rader</span><span class="sxs-lookup"><span data-stu-id="02979-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="02979-160">Du kan kopiera en eller flera rader i en lista eller ett enda fält på en sida och klistra in det du kopierade till samma sida, en annan sida eller ett externt dokument (såsom Microsoft Excel och Outlook e-post).</span><span class="sxs-lookup"><span data-stu-id="02979-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="02979-161">Kortfattat, för att kopiera trycker du på CTRL + C (cmd + C i macOS) på tangentbordet.</span><span class="sxs-lookup"><span data-stu-id="02979-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="02979-162">Klistra in genom att trycka på CTRL + V (cmd + V i macOS).</span><span class="sxs-lookup"><span data-stu-id="02979-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="02979-163">I en lista kopierar du fältet i samma kolumn i raden ovanför och klistra in den i den aktuella raden, tryck bara på F8.</span><span class="sxs-lookup"><span data-stu-id="02979-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="02979-164">Mer information finns i [Kopiera och klistra in i Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="02979-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="02979-165">Fokusera på radartiklar</span><span class="sxs-lookup"><span data-stu-id="02979-165">Focusing on Line Items</span></span>

<span data-ttu-id="02979-166">När du arbetar med dokument som innehåller en radartikeldel, som en försäljningsorder eller en fakturasida kan du växla vyn till att fokusera på poster, i huvudsak expandera radartikeldelen så att den upptar nästan hela arbetsytan, dölja andra delar av den sidan förutom åtgärder överst.</span><span class="sxs-lookup"><span data-stu-id="02979-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="02979-167">Detta ger dig en bättre översikt över radobjekten och ger mer plats att arbeta med dem.</span><span class="sxs-lookup"><span data-stu-id="02979-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="02979-168">Detta är speciellt viktigt när du arbetar med stora radposter och snabb dataregistrering önskas.</span><span class="sxs-lookup"><span data-stu-id="02979-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="02979-169">En annan fördel är den även ger avancerade filtreringsfunktioner, precis som i andra listor, så bläddra och söka igenom radposter blir ännu enklare.</span><span class="sxs-lookup"><span data-stu-id="02979-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switching-the-focus-on-and-off"></a><span data-ttu-id="02979-170">Aktivera och inaktivera fokus</span><span class="sxs-lookup"><span data-stu-id="02979-170">Switching the Focus On and Off</span></span>

<span data-ttu-id="02979-171">För att fokusera på radartiklar väljer du var som helst i radartikeldelen och välj ![ikonen Fokusläge](media/focus-mode.png "ikonen Fokusläge") i övre högra hörnet eller tryck på Ctrl + Shift + F12.</span><span class="sxs-lookup"><span data-stu-id="02979-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="02979-172">Om du vill växla tillbaka till normal vy, väljer ![ikonen Fokusläge](media/focus-mode.png "ikonen Fokusläge") eller tryck på Ctrl + Shift + F12 igen.</span><span class="sxs-lookup"><span data-stu-id="02979-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="02979-173">Filtrera radposter</span><span class="sxs-lookup"><span data-stu-id="02979-173">Filtering the Line Items</span></span>

<span data-ttu-id="02979-174">För att starta filtrering, välj ![Filterrutaikon](media/open-filter-pane-icon.png "Filterrutaikon") högst upp i listan eller tryck på **Shift+F3** för att öppna filterrutan.</span><span class="sxs-lookup"><span data-stu-id="02979-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="02979-175">Du kan arbeta med filterrutan som på vilken lista som helst.</span><span class="sxs-lookup"><span data-stu-id="02979-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="02979-176">Mer information finns i [Filtrering](ui-enter-criteria-filters.md#Filtering).</span><span class="sxs-lookup"><span data-stu-id="02979-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="02979-177">Filtrering är särskilt användbart när du visar och analyserar längre dokument.</span><span class="sxs-lookup"><span data-stu-id="02979-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="02979-178">Anta att du öppnar en bokförd försäljningsfaktura och filtrerar radposter för att visa alla radposter som har en enskild rabatt på mer än 5 % eller ett filter för att visa endast cykeltillbehör med "proffs" i namnet.</span><span class="sxs-lookup"><span data-stu-id="02979-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="02979-179">Ange antal genom beräkning</span><span class="sxs-lookup"><span data-stu-id="02979-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="02979-180">När du skriver siffror i antalsfält, till exempel fältet **Antal** för en artikeljournalrad, kan du skriva formeln i stället för summan.</span><span class="sxs-lookup"><span data-stu-id="02979-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="02979-181">Exempel</span><span class="sxs-lookup"><span data-stu-id="02979-181">Examples</span></span>  

-   <span data-ttu-id="02979-182">Om du skriver 19+19 beräknas fältet till 38.</span><span class="sxs-lookup"><span data-stu-id="02979-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="02979-183">Om skriver 41-9 beräknas fältet till 32.</span><span class="sxs-lookup"><span data-stu-id="02979-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="02979-184">Om du skriver 12\*4 beräknas fältet till 48.</span><span class="sxs-lookup"><span data-stu-id="02979-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="02979-185">Om du skriver 12/4 beräknas fältet till 3.</span><span class="sxs-lookup"><span data-stu-id="02979-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="02979-186">Ange negativa antal</span><span class="sxs-lookup"><span data-stu-id="02979-186">Entering Negative Numbers</span></span>

<span data-ttu-id="02979-187">Du kan ange negativa antal på två sätt.</span><span class="sxs-lookup"><span data-stu-id="02979-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="02979-188">Numret -20,5 som kan anges:</span><span class="sxs-lookup"><span data-stu-id="02979-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="02979-189">-20.5</span><span class="sxs-lookup"><span data-stu-id="02979-189">-20.5</span></span>  

    <span data-ttu-id="02979-190">eller</span><span class="sxs-lookup"><span data-stu-id="02979-190">or</span></span>
-   <span data-ttu-id="02979-191">20.5-</span><span class="sxs-lookup"><span data-stu-id="02979-191">20.5-</span></span>  

 <span data-ttu-id="02979-192">I båda fallen registreras beloppet som -20,5.</span><span class="sxs-lookup"><span data-stu-id="02979-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="02979-193">Om det sista tecknet i uttrycket är **+** eller **-**, kommer hela uttrycket registreras med det tecknet.</span><span class="sxs-lookup"><span data-stu-id="02979-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="02979-194">Ett exempel, **10-20+**, ska leda till 10 och inte -10.</span><span class="sxs-lookup"><span data-stu-id="02979-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="02979-195">Ange datum och tider</span><span class="sxs-lookup"><span data-stu-id="02979-195">Entering Dates and Times</span></span>

<span data-ttu-id="02979-196">Du kan ange datum och tider i alla datumfält.</span><span class="sxs-lookup"><span data-stu-id="02979-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="02979-197">Du kan skriva datum med eller utan avgränsare.</span><span class="sxs-lookup"><span data-stu-id="02979-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="02979-198">Hur du anger datum och klockslag beror på dina **region**-inställningar.</span><span class="sxs-lookup"><span data-stu-id="02979-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="02979-199">Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="02979-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="02979-200">Ange datum</span><span class="sxs-lookup"><span data-stu-id="02979-200">Entering Dates</span></span>

<span data-ttu-id="02979-201">För datumfält kan du antingen använda dataväljaren som låter dig välja ett datum från en kalender eller så kan du ange datumen manuellt.</span><span class="sxs-lookup"><span data-stu-id="02979-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="02979-202">Det här avsnittet innehåller en kort översikt över hur du anger datum.</span><span class="sxs-lookup"><span data-stu-id="02979-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="02979-203">Mer information finns i [arbeta med kalenderdatum och tider](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="02979-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="02979-204">För manuell datainmatning kan du skriva in två, fyra, sex eller åtta siffror.</span><span class="sxs-lookup"><span data-stu-id="02979-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="02979-205">Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="02979-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="02979-206">Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="02979-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="02979-207">Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.</span><span class="sxs-lookup"><span data-stu-id="02979-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="02979-208">Du kan också skriva ett datum som en veckodag följt av veckonumret och (valfritt) ett år (exempelvis Mån25, eller mån25 betyder måndagen i vecka 25).</span><span class="sxs-lookup"><span data-stu-id="02979-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="02979-209">I stället för att skriva in ett visst datum kan du skriva in någon av dessa koder.</span><span class="sxs-lookup"><span data-stu-id="02979-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="02979-210">Kod</span><span class="sxs-lookup"><span data-stu-id="02979-210">Code</span></span>|<span data-ttu-id="02979-211">Resultat</span><span class="sxs-lookup"><span data-stu-id="02979-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="02979-212">d</span><span class="sxs-lookup"><span data-stu-id="02979-212">t</span></span>|<span data-ttu-id="02979-213">Det här anger dagens datum (detta är datorns systemdatum).</span><span class="sxs-lookup"><span data-stu-id="02979-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="02979-214">p</span><span class="sxs-lookup"><span data-stu-id="02979-214">p</span></span>|<span data-ttu-id="02979-215">Det här anger en bokföringsperiod där `p`innebär att den första bokföringsperiod, `p2` innebär det andra kontot, och så vidare.</span><span class="sxs-lookup"><span data-stu-id="02979-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="02979-216">a</span><span class="sxs-lookup"><span data-stu-id="02979-216">w</span></span>|<span data-ttu-id="02979-217">Detta anger arbetsdatumet som har lagts upp i programmet.</span><span class="sxs-lookup"><span data-stu-id="02979-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="02979-218">Om du vill ändra arbetsdatumet, [ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="02979-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="02979-219">Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.</span><span class="sxs-lookup"><span data-stu-id="02979-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="02979-220">c</span><span class="sxs-lookup"><span data-stu-id="02979-220">c</span></span>|<span data-ttu-id="02979-221">Detta anger att datumet efter `c`är ett avslutsdatum, till exempel `C123101`.</span><span class="sxs-lookup"><span data-stu-id="02979-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="02979-222">Ange tider</span><span class="sxs-lookup"><span data-stu-id="02979-222">Entering Times</span></span>

<span data-ttu-id="02979-223">När du anger tider kan du infoga vilken avgränsare du vill mellan enheterna. Detta är dock inte obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="02979-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="02979-224">Du behöver inte skriva minuter, sekunder eller AM/PM.</span><span class="sxs-lookup"><span data-stu-id="02979-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="02979-225">I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.</span><span class="sxs-lookup"><span data-stu-id="02979-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="02979-226">Transaktion</span><span class="sxs-lookup"><span data-stu-id="02979-226">Entry</span></span>|<span data-ttu-id="02979-227">Tolkning</span><span class="sxs-lookup"><span data-stu-id="02979-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="02979-228">5</span><span class="sxs-lookup"><span data-stu-id="02979-228">5</span></span>|<span data-ttu-id="02979-229">05:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-229">05:00:00</span></span>|  
|<span data-ttu-id="02979-230">5:30</span><span class="sxs-lookup"><span data-stu-id="02979-230">5:30</span></span>|<span data-ttu-id="02979-231">05:30:00</span><span class="sxs-lookup"><span data-stu-id="02979-231">05:30:00</span></span>|  
|<span data-ttu-id="02979-232">0530</span><span class="sxs-lookup"><span data-stu-id="02979-232">0530</span></span>|<span data-ttu-id="02979-233">05:30:00</span><span class="sxs-lookup"><span data-stu-id="02979-233">05:30:00</span></span>|  
|<span data-ttu-id="02979-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="02979-234">5:30:5</span></span>|<span data-ttu-id="02979-235">05:30:05</span><span class="sxs-lookup"><span data-stu-id="02979-235">05:30:05</span></span>|  
|<span data-ttu-id="02979-236">053005</span><span class="sxs-lookup"><span data-stu-id="02979-236">053005</span></span>|<span data-ttu-id="02979-237">05:30:05</span><span class="sxs-lookup"><span data-stu-id="02979-237">05:30:05</span></span>|  
|<span data-ttu-id="02979-238">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="02979-238">5:30:5,50</span></span>|<span data-ttu-id="02979-239">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="02979-239">05:30:05.5</span></span>|  
|<span data-ttu-id="02979-240">053005050</span><span class="sxs-lookup"><span data-stu-id="02979-240">053005050</span></span>|<span data-ttu-id="02979-241">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="02979-241">05:30:05.05</span></span>|  

 <span data-ttu-id="02979-242">Du måste ange två siffror för varje tidsenhet om du inte använder någon avgränsare.</span><span class="sxs-lookup"><span data-stu-id="02979-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="02979-243">Ange datum och tid</span><span class="sxs-lookup"><span data-stu-id="02979-243">Entering Datetimes</span></span>

<span data-ttu-id="02979-244">När du anger datum och tid måste du ange ett blanksteg mellan datumet och tiden.</span><span class="sxs-lookup"><span data-stu-id="02979-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="02979-245">Listan nedan innehåller de olika sätt som du kan ange datum och tid på och en förklaring av hur de ska tolkas.</span><span class="sxs-lookup"><span data-stu-id="02979-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="02979-246">Transaktion</span><span class="sxs-lookup"><span data-stu-id="02979-246">Entry</span></span>|<span data-ttu-id="02979-247">Tolkning</span><span class="sxs-lookup"><span data-stu-id="02979-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="02979-248">021213 132455</span><span class="sxs-lookup"><span data-stu-id="02979-248">131202 132455</span></span>|<span data-ttu-id="02979-249">02-12-13 13:24:55</span><span class="sxs-lookup"><span data-stu-id="02979-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="02979-250">02-12-1 10</span><span class="sxs-lookup"><span data-stu-id="02979-250">1-12-02 10</span></span>|<span data-ttu-id="02979-251">02-12-01 10:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="02979-252">02.12.1 5</span><span class="sxs-lookup"><span data-stu-id="02979-252">1.12.02 5</span></span>|<span data-ttu-id="02979-253">02-12-01 05:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="02979-254">02.12.1</span><span class="sxs-lookup"><span data-stu-id="02979-254">1.12.02</span></span>|<span data-ttu-id="02979-255">02-12-01 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="02979-256">11 12</span><span class="sxs-lookup"><span data-stu-id="02979-256">11 12</span></span>|<span data-ttu-id="02979-257">11-innevarande månad-innevarande år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="02979-258">11 12 12</span><span class="sxs-lookup"><span data-stu-id="02979-258">1112 12</span></span>|<span data-ttu-id="02979-259">11-12-innevarande år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="02979-260">d eller dagens datum</span><span class="sxs-lookup"><span data-stu-id="02979-260">t or today</span></span>|<span data-ttu-id="02979-261">dagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="02979-262">d tid</span><span class="sxs-lookup"><span data-stu-id="02979-262">t time</span></span>|<span data-ttu-id="02979-263">dagens datum aktuell tid</span><span class="sxs-lookup"><span data-stu-id="02979-263">today's date actual time</span></span>|  
|<span data-ttu-id="02979-264">d 10:30</span><span class="sxs-lookup"><span data-stu-id="02979-264">t 10:30</span></span>|<span data-ttu-id="02979-265">dagens datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="02979-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="02979-266">d 03:03:03</span><span class="sxs-lookup"><span data-stu-id="02979-266">t 3:3:3</span></span>|<span data-ttu-id="02979-267">dagens datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="02979-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="02979-268">a eller arbetsdagens datum</span><span class="sxs-lookup"><span data-stu-id="02979-268">w or workdate</span></span>|<span data-ttu-id="02979-269">arbetsdagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="02979-270">m eller måndag</span><span class="sxs-lookup"><span data-stu-id="02979-270">m or Monday</span></span>|<span data-ttu-id="02979-271">måndag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-272">ti eller tisdag</span><span class="sxs-lookup"><span data-stu-id="02979-272">tu or Tuesday</span></span>|<span data-ttu-id="02979-273">tisdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-274">on eller onsdag</span><span class="sxs-lookup"><span data-stu-id="02979-274">we or Wednesday</span></span>|<span data-ttu-id="02979-275">onsdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-276">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="02979-276">th or Thursday</span></span>|<span data-ttu-id="02979-277">torsdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-278">fr eller fredag</span><span class="sxs-lookup"><span data-stu-id="02979-278">f or Friday</span></span>|<span data-ttu-id="02979-279">fredag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-280">lö eller lördag</span><span class="sxs-lookup"><span data-stu-id="02979-280">s or Saturday</span></span>|<span data-ttu-id="02979-281">lördag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-282">sö eller söndag</span><span class="sxs-lookup"><span data-stu-id="02979-282">su or Sunday</span></span>|<span data-ttu-id="02979-283">söndag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="02979-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="02979-284">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="02979-284">tu 10:30</span></span>|<span data-ttu-id="02979-285">tisdag i innevarande vecka 10:30:00</span><span class="sxs-lookup"><span data-stu-id="02979-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="02979-286">ti 03:03:03</span><span class="sxs-lookup"><span data-stu-id="02979-286">tu 3:3:3</span></span>|<span data-ttu-id="02979-287">tisdag i innevarande vecka 03:03:03</span><span class="sxs-lookup"><span data-stu-id="02979-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="02979-288">Ange varaktighet</span><span class="sxs-lookup"><span data-stu-id="02979-288">Entering Duration</span></span>

<span data-ttu-id="02979-289">Du anger varaktigheten som en siffra följd av en enhet.</span><span class="sxs-lookup"><span data-stu-id="02979-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="02979-290">Här följer några exempel.</span><span class="sxs-lookup"><span data-stu-id="02979-290">Here are some examples.</span></span>  

|<span data-ttu-id="02979-291">Varaktighet</span><span class="sxs-lookup"><span data-stu-id="02979-291">Duration</span></span>|<span data-ttu-id="02979-292">Måttenhet\*\*</span><span class="sxs-lookup"><span data-stu-id="02979-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="02979-293">2t</span><span class="sxs-lookup"><span data-stu-id="02979-293">2h</span></span>|<span data-ttu-id="02979-294">2 timmar</span><span class="sxs-lookup"><span data-stu-id="02979-294">2 hrs</span></span>|  
|<span data-ttu-id="02979-295">6t 30m</span><span class="sxs-lookup"><span data-stu-id="02979-295">6h 30 m</span></span>|<span data-ttu-id="02979-296">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="02979-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="02979-297">6,5t</span><span class="sxs-lookup"><span data-stu-id="02979-297">6.5h</span></span>|<span data-ttu-id="02979-298">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="02979-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="02979-299">90m</span><span class="sxs-lookup"><span data-stu-id="02979-299">90m</span></span>|<span data-ttu-id="02979-300">1 timme 30 minuter</span><span class="sxs-lookup"><span data-stu-id="02979-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="02979-301">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="02979-301">2d 6h 30m</span></span>|<span data-ttu-id="02979-302">2 dagar 6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="02979-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="02979-303">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="02979-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="02979-304">2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder</span><span class="sxs-lookup"><span data-stu-id="02979-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="02979-305">Du kan även ange en siffra som automatiskt konverteras till en varaktighet.</span><span class="sxs-lookup"><span data-stu-id="02979-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="02979-306">Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.</span><span class="sxs-lookup"><span data-stu-id="02979-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="02979-307">Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.</span><span class="sxs-lookup"><span data-stu-id="02979-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="02979-308">Numret 5 konverteras till 5 timmar om enheten är timmar.</span><span class="sxs-lookup"><span data-stu-id="02979-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="02979-309">Se även</span><span class="sxs-lookup"><span data-stu-id="02979-309">See Also</span></span>  
 [<span data-ttu-id="02979-310">Sortera, söka och filtrera listor</span><span class="sxs-lookup"><span data-stu-id="02979-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="02979-311">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="02979-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

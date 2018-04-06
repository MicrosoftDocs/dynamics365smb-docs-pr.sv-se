---
title: "Hur du anger du data i fält | Microsoft Docs"
description: "Det finns många allmänna funktioner som gör det snabbt och enkelt att registrera data. Dessa funktioner för dataregistrering beskrivs i det här avsnittet."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 5f95efb5cad24db9848752035172bc7bb76db716
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="entering-data"></a><span data-ttu-id="954af-104">Ange data</span><span class="sxs-lookup"><span data-stu-id="954af-104">Entering Data</span></span>
<span data-ttu-id="954af-105">Det finns många allmänna funktioner som gör det snabbt och enkelt att registrera data.</span><span class="sxs-lookup"><span data-stu-id="954af-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="954af-106">Dessa funktioner för dataregistrering beskrivs i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="954af-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="954af-107">I exemplen nedan används demonstrationsdata.</span><span class="sxs-lookup"><span data-stu-id="954af-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="954af-108">Obligatoriska fält</span><span class="sxs-lookup"><span data-stu-id="954af-108">Mandatory Fields</span></span>
<span data-ttu-id="954af-109">När du anger data på sidor markeras vissa fält med en röd asterisk.</span><span class="sxs-lookup"><span data-stu-id="954af-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="954af-110">Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.</span><span class="sxs-lookup"><span data-stu-id="954af-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="954af-111">Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan.</span><span class="sxs-lookup"><span data-stu-id="954af-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="954af-112">Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.</span><span class="sxs-lookup"><span data-stu-id="954af-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="954af-113">Söka efter data allt eftersom du skriver</span><span class="sxs-lookup"><span data-stu-id="954af-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="954af-114">När du börjar skriva tecken i ett fält visas en listruta med möjliga fältvärden.</span><span class="sxs-lookup"><span data-stu-id="954af-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="954af-115">Listan ändras allt eftersom du skriver fler tecken, och du kan välja rätt värde när det visas.</span><span class="sxs-lookup"><span data-stu-id="954af-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="954af-116">Många fält har en nedpil-knapp som du kan välja.</span><span class="sxs-lookup"><span data-stu-id="954af-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="954af-117">Du kan välja pilen om du vill visa en lista med data som är tillgängliga för fältet.</span><span class="sxs-lookup"><span data-stu-id="954af-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="954af-118">Knappen har två funktioner beroende på typen av fält:</span><span class="sxs-lookup"><span data-stu-id="954af-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="954af-119">Sökning – Visar information från en annan tabell som du kan infoga i fältet.</span><span class="sxs-lookup"><span data-stu-id="954af-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="954af-120">Du kan bara välja en i taget.</span><span class="sxs-lookup"><span data-stu-id="954af-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="954af-121">Lista – Visar den uppsättning alternativ (fasta val) som finns för fältet.</span><span class="sxs-lookup"><span data-stu-id="954af-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="954af-122">Du kan bara markera ett av alternativen.</span><span class="sxs-lookup"><span data-stu-id="954af-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="954af-123">Ange antal genom beräkning</span><span class="sxs-lookup"><span data-stu-id="954af-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="954af-124">När du skriver siffror i antalsfält, till exempel fältet **Antal** för en artikeljournalrad, kan du skriva formeln i stället för summan.</span><span class="sxs-lookup"><span data-stu-id="954af-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="954af-125">Exempel</span><span class="sxs-lookup"><span data-stu-id="954af-125">Examples</span></span>  

-   <span data-ttu-id="954af-126">Om du skriver 19+19 beräknas fältet till 38.</span><span class="sxs-lookup"><span data-stu-id="954af-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="954af-127">Om skriver 41-9 beräknas fältet till 32.</span><span class="sxs-lookup"><span data-stu-id="954af-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="954af-128">Om du skriver 12\*4 beräknas fältet till 48.</span><span class="sxs-lookup"><span data-stu-id="954af-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="954af-129">Om du skriver 12/4 beräknas fältet till 3.</span><span class="sxs-lookup"><span data-stu-id="954af-129">If you enter 12/4, the field is calculated to 3.</span></span>  

# <a name="entering-negative-numbers"></a><span data-ttu-id="954af-130">Ange negativa antal</span><span class="sxs-lookup"><span data-stu-id="954af-130">Entering Negative Numbers</span></span>
<span data-ttu-id="954af-131">Du kan ange negativa antal på två sätt.</span><span class="sxs-lookup"><span data-stu-id="954af-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="954af-132">Numret -20,5 som kan anges:</span><span class="sxs-lookup"><span data-stu-id="954af-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="954af-133">-20.5</span><span class="sxs-lookup"><span data-stu-id="954af-133">-20.5</span></span>  

    <span data-ttu-id="954af-134">eller</span><span class="sxs-lookup"><span data-stu-id="954af-134">or</span></span>
-   <span data-ttu-id="954af-135">20.5-</span><span class="sxs-lookup"><span data-stu-id="954af-135">20.5-</span></span>  

 <span data-ttu-id="954af-136">I båda fallen registreras beloppet som -20,5.</span><span class="sxs-lookup"><span data-stu-id="954af-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="954af-137">Om det sista tecknet i uttrycket är **+** eller **-**, kommer hela uttrycket registreras med det tecknet.</span><span class="sxs-lookup"><span data-stu-id="954af-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="954af-138">Ett exempel, **10-20+**, ska leda till 10 och inte -10.</span><span class="sxs-lookup"><span data-stu-id="954af-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="954af-139">Ange datum och tider</span><span class="sxs-lookup"><span data-stu-id="954af-139">Entering Dates and Times</span></span>
<span data-ttu-id="954af-140">Du kan ange datum och tider i alla datumfält.</span><span class="sxs-lookup"><span data-stu-id="954af-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="954af-141">Du kan skriva datum med eller utan avgränsare.</span><span class="sxs-lookup"><span data-stu-id="954af-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="954af-142">Hur du anger datum och klockslag beror på dina **region**-inställningar.</span><span class="sxs-lookup"><span data-stu-id="954af-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="954af-143">Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="954af-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="954af-144">Ange datum</span><span class="sxs-lookup"><span data-stu-id="954af-144">Entering Dates</span></span>  
 <span data-ttu-id="954af-145">I ett datumfält kan du skriva in två, fyra, sex eller åtta siffror.</span><span class="sxs-lookup"><span data-stu-id="954af-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="954af-146">Om du bara skriver in två siffror tolkas de som dag. Programmet lägger till månaden och året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="954af-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="954af-147">Om du skriver in fyra siffror tolkas de som dagen och månaden. Programmet lägger till året från arbetsdatumet.</span><span class="sxs-lookup"><span data-stu-id="954af-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="954af-148">Om det datum du vill ange ligger inom intervallet 1930-01-01 t.o.m. 2029-12-31 kan du ange året med två siffror, annars måste du ange det med fyra siffror.</span><span class="sxs-lookup"><span data-stu-id="954af-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="954af-149">Du kan också skriva ett datum som en veckodag följt av veckonumret och (valfritt) ett år (exempelvis Mån25, eller mån25 betyder måndagen i vecka 25).</span><span class="sxs-lookup"><span data-stu-id="954af-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="954af-150">I stället för att skriva in ett visst datum kan du skriva in någon av de två koderna nedan.</span><span class="sxs-lookup"><span data-stu-id="954af-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="954af-151">Kod</span><span class="sxs-lookup"><span data-stu-id="954af-151">Code</span></span>|<span data-ttu-id="954af-152">Resultat</span><span class="sxs-lookup"><span data-stu-id="954af-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="954af-153">d</span><span class="sxs-lookup"><span data-stu-id="954af-153">t</span></span>|<span data-ttu-id="954af-154">Det här är dagens datum (detta är datorns systemdatum).</span><span class="sxs-lookup"><span data-stu-id="954af-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="954af-155">a</span><span class="sxs-lookup"><span data-stu-id="954af-155">w</span></span>|<span data-ttu-id="954af-156">Detta är arbetsdatumet som har lagts upp i programmet.</span><span class="sxs-lookup"><span data-stu-id="954af-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="954af-157">Om du vill ändra arbetsdatumet, [ändra grundläggande inställningar](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="954af-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="954af-158">Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.</span><span class="sxs-lookup"><span data-stu-id="954af-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="954af-159">Ange tider</span><span class="sxs-lookup"><span data-stu-id="954af-159">Entering Times</span></span>  
 <span data-ttu-id="954af-160">När du anger tider kan du infoga vilken avgränsare du vill mellan enheterna. Detta är dock inte obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="954af-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="954af-161">Du behöver inte skriva minuter, sekunder eller AM/PM.</span><span class="sxs-lookup"><span data-stu-id="954af-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="954af-162">I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.</span><span class="sxs-lookup"><span data-stu-id="954af-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="954af-163">Transaktion</span><span class="sxs-lookup"><span data-stu-id="954af-163">Entry</span></span>|<span data-ttu-id="954af-164">Tolkning</span><span class="sxs-lookup"><span data-stu-id="954af-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="954af-165">5</span><span class="sxs-lookup"><span data-stu-id="954af-165">5</span></span>|<span data-ttu-id="954af-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-166">05:00:00</span></span>|  
|<span data-ttu-id="954af-167">5:30</span><span class="sxs-lookup"><span data-stu-id="954af-167">5:30</span></span>|<span data-ttu-id="954af-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="954af-168">05:30:00</span></span>|  
|<span data-ttu-id="954af-169">0530</span><span class="sxs-lookup"><span data-stu-id="954af-169">0530</span></span>|<span data-ttu-id="954af-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="954af-170">05:30:00</span></span>|  
|<span data-ttu-id="954af-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="954af-171">5:30:5</span></span>|<span data-ttu-id="954af-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="954af-172">05:30:05</span></span>|  
|<span data-ttu-id="954af-173">053005</span><span class="sxs-lookup"><span data-stu-id="954af-173">053005</span></span>|<span data-ttu-id="954af-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="954af-174">05:30:05</span></span>|  
|<span data-ttu-id="954af-175">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="954af-175">5:30:5,50</span></span>|<span data-ttu-id="954af-176">05:30:050,5</span><span class="sxs-lookup"><span data-stu-id="954af-176">05:30:05.5</span></span>|  
|<span data-ttu-id="954af-177">053005050</span><span class="sxs-lookup"><span data-stu-id="954af-177">053005050</span></span>|<span data-ttu-id="954af-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="954af-178">05:30:05.05</span></span>|  

 <span data-ttu-id="954af-179">Du måste ange två siffror för varje tidsenhet om du inte använder någon avgränsare.</span><span class="sxs-lookup"><span data-stu-id="954af-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="954af-180">Ange datum och tid</span><span class="sxs-lookup"><span data-stu-id="954af-180">Entering Datetimes</span></span>  
 <span data-ttu-id="954af-181">När du anger datum och tid måste du ange ett blanksteg mellan datumet och tiden.</span><span class="sxs-lookup"><span data-stu-id="954af-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="954af-182">Listan nedan innehåller de olika sätt som du kan ange datum och tid på och en förklaring av hur de ska tolkas.</span><span class="sxs-lookup"><span data-stu-id="954af-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="954af-183">Transaktion</span><span class="sxs-lookup"><span data-stu-id="954af-183">Entry</span></span>|<span data-ttu-id="954af-184">Tolkning</span><span class="sxs-lookup"><span data-stu-id="954af-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="954af-185">021213 132455</span><span class="sxs-lookup"><span data-stu-id="954af-185">131202 132455</span></span>|<span data-ttu-id="954af-186">02-12-13 13:24:55</span><span class="sxs-lookup"><span data-stu-id="954af-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="954af-187">02-12-1 10</span><span class="sxs-lookup"><span data-stu-id="954af-187">1-12-02 10</span></span>|<span data-ttu-id="954af-188">02-12-01 10:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="954af-189">02.12.1 5</span><span class="sxs-lookup"><span data-stu-id="954af-189">1.12.02 5</span></span>|<span data-ttu-id="954af-190">02-12-01 05:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="954af-191">02.12.1</span><span class="sxs-lookup"><span data-stu-id="954af-191">1.12.02</span></span>|<span data-ttu-id="954af-192">02-12-01 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="954af-193">11 12</span><span class="sxs-lookup"><span data-stu-id="954af-193">11 12</span></span>|<span data-ttu-id="954af-194">11-innevarande månad-innevarande år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="954af-195">11 12 12</span><span class="sxs-lookup"><span data-stu-id="954af-195">1112 12</span></span>|<span data-ttu-id="954af-196">11-12-innevarande år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="954af-197">d eller dagens datum</span><span class="sxs-lookup"><span data-stu-id="954af-197">t or today</span></span>|<span data-ttu-id="954af-198">dagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="954af-199">d tid</span><span class="sxs-lookup"><span data-stu-id="954af-199">t time</span></span>|<span data-ttu-id="954af-200">dagens datum aktuell tid</span><span class="sxs-lookup"><span data-stu-id="954af-200">today's date actual time</span></span>|  
|<span data-ttu-id="954af-201">d 10:30</span><span class="sxs-lookup"><span data-stu-id="954af-201">t 10:30</span></span>|<span data-ttu-id="954af-202">dagens datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="954af-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="954af-203">d 03:03:03</span><span class="sxs-lookup"><span data-stu-id="954af-203">t 3:3:3</span></span>|<span data-ttu-id="954af-204">dagens datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="954af-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="954af-205">a eller arbetsdagens datum</span><span class="sxs-lookup"><span data-stu-id="954af-205">w or workdate</span></span>|<span data-ttu-id="954af-206">arbetsdagens datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="954af-207">m eller måndag</span><span class="sxs-lookup"><span data-stu-id="954af-207">m or Monday</span></span>|<span data-ttu-id="954af-208">måndag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-209">ti eller tisdag</span><span class="sxs-lookup"><span data-stu-id="954af-209">tu or Tuesday</span></span>|<span data-ttu-id="954af-210">tisdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-211">on eller onsdag</span><span class="sxs-lookup"><span data-stu-id="954af-211">we or Wednesday</span></span>|<span data-ttu-id="954af-212">onsdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-213">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="954af-213">th or Thursday</span></span>|<span data-ttu-id="954af-214">torsdag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-215">fr eller fredag</span><span class="sxs-lookup"><span data-stu-id="954af-215">f or Friday</span></span>|<span data-ttu-id="954af-216">fredag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-217">lö eller lördag</span><span class="sxs-lookup"><span data-stu-id="954af-217">s or Saturday</span></span>|<span data-ttu-id="954af-218">lördag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-219">sö eller söndag</span><span class="sxs-lookup"><span data-stu-id="954af-219">su or Sunday</span></span>|<span data-ttu-id="954af-220">söndag i innevarande vecka 00:00:00</span><span class="sxs-lookup"><span data-stu-id="954af-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="954af-221">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="954af-221">tu 10:30</span></span>|<span data-ttu-id="954af-222">tisdag i innevarande vecka 10:30:00</span><span class="sxs-lookup"><span data-stu-id="954af-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="954af-223">ti 03:03:03</span><span class="sxs-lookup"><span data-stu-id="954af-223">tu 3:3:3</span></span>|<span data-ttu-id="954af-224">tisdag i innevarande vecka 03:03:03</span><span class="sxs-lookup"><span data-stu-id="954af-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="954af-225">Ange varaktighet</span><span class="sxs-lookup"><span data-stu-id="954af-225">Entering Duration</span></span>  
 <span data-ttu-id="954af-226">Du anger varaktigheten som en siffra följd av en enhet.</span><span class="sxs-lookup"><span data-stu-id="954af-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="954af-227">Här följer några exempel.</span><span class="sxs-lookup"><span data-stu-id="954af-227">Here are some examples.</span></span>  

|<span data-ttu-id="954af-228">Varaktighet</span><span class="sxs-lookup"><span data-stu-id="954af-228">Duration</span></span>|<span data-ttu-id="954af-229">Måttenhet**</span><span class="sxs-lookup"><span data-stu-id="954af-229">Unit of measure**</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="954af-230">2t</span><span class="sxs-lookup"><span data-stu-id="954af-230">2h</span></span>|<span data-ttu-id="954af-231">2 timmar</span><span class="sxs-lookup"><span data-stu-id="954af-231">2 hrs</span></span>|  
|<span data-ttu-id="954af-232">6t 30m</span><span class="sxs-lookup"><span data-stu-id="954af-232">6h 30 m</span></span>|<span data-ttu-id="954af-233">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="954af-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="954af-234">6,5t</span><span class="sxs-lookup"><span data-stu-id="954af-234">6.5h</span></span>|<span data-ttu-id="954af-235">6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="954af-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="954af-236">90m</span><span class="sxs-lookup"><span data-stu-id="954af-236">90m</span></span>|<span data-ttu-id="954af-237">1 timme 30 minuter</span><span class="sxs-lookup"><span data-stu-id="954af-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="954af-238">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="954af-238">2d 6h 30m</span></span>|<span data-ttu-id="954af-239">2 dagar 6 timmar 30 minuter</span><span class="sxs-lookup"><span data-stu-id="954af-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="954af-240">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="954af-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="954af-241">2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder</span><span class="sxs-lookup"><span data-stu-id="954af-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="954af-242">Du kan även ange en siffra som automatiskt konverteras till en varaktighet.</span><span class="sxs-lookup"><span data-stu-id="954af-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="954af-243">Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.</span><span class="sxs-lookup"><span data-stu-id="954af-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="954af-244">Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.</span><span class="sxs-lookup"><span data-stu-id="954af-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="954af-245">Numret 5 konverteras till 5 timmar om enheten är timmar.</span><span class="sxs-lookup"><span data-stu-id="954af-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a><span data-ttu-id="954af-246">Använda datumformler</span><span class="sxs-lookup"><span data-stu-id="954af-246">Using Date Formulas</span></span>  
 <span data-ttu-id="954af-247">En datumformel är en kort kombination av förkortningar med bokstäver och siffror som anger hur datum ska beräknas.</span><span class="sxs-lookup"><span data-stu-id="954af-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="954af-248">Du kan ange datumformler i olika beräkningsfält för datum och i fält för återkomstfrekvens i återkommande journaler.</span><span class="sxs-lookup"><span data-stu-id="954af-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="954af-249">I alla dataformulärfält inkluderas automatiskt en dag att täcka i dag som dagen när perioden börjar.</span><span class="sxs-lookup"><span data-stu-id="954af-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="954af-250">Därefter om du anger, till exempel 1 vecka, är perioden faktiskt åtta dagar eftersom idag inkluderas.</span><span class="sxs-lookup"><span data-stu-id="954af-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="954af-251">För att ange en period av sju dagar (en exakt vecka) inklusive perioden för startdatum måste du ange 6 dagar eller 1 vecka minus 1 dag.</span><span class="sxs-lookup"><span data-stu-id="954af-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="954af-252">Här följer några exempel på hur datumformler kan användas:</span><span class="sxs-lookup"><span data-stu-id="954af-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="954af-253">Datumformeln i fält för återkommande frekvens i återkommande journaler bestämmer hur ofta posten på journalraden ska bokföras.</span><span class="sxs-lookup"><span data-stu-id="954af-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="954af-254">Datumformeln i fältet Betalningsfrist för en viss påminnelsenivå bestämmer vilken tidsperiod som ska förflyta från förfallodatumet (eller från den föregående påminnelsen) innan en påminnelse ska skapas.</span><span class="sxs-lookup"><span data-stu-id="954af-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="954af-255">Datumformeln i fältet Förfallodatumformel bestämmer hur förfallodatumet på påminnelsen beräknas.</span><span class="sxs-lookup"><span data-stu-id="954af-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="954af-256">Formeln för datumberäkning kan bara omfatta högst 20 tecken, både siffror och bokstäver.</span><span class="sxs-lookup"><span data-stu-id="954af-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="954af-257">Du kan använda följande bokstäver som förkortningar för tidsangivelser.</span><span class="sxs-lookup"><span data-stu-id="954af-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="954af-258">L</span><span class="sxs-lookup"><span data-stu-id="954af-258">C</span></span>|<span data-ttu-id="954af-259">Löpande (innevarande)</span><span class="sxs-lookup"><span data-stu-id="954af-259">Current</span></span>|  
|<span data-ttu-id="954af-260">D</span><span class="sxs-lookup"><span data-stu-id="954af-260">D</span></span>|<span data-ttu-id="954af-261">Dag/dagar</span><span class="sxs-lookup"><span data-stu-id="954af-261">Day(s)</span></span>|  
|<span data-ttu-id="954af-262">V</span><span class="sxs-lookup"><span data-stu-id="954af-262">W</span></span>|<span data-ttu-id="954af-263">Vecka/veckor</span><span class="sxs-lookup"><span data-stu-id="954af-263">Week(s)</span></span>|  
|<span data-ttu-id="954af-264">M</span><span class="sxs-lookup"><span data-stu-id="954af-264">M</span></span>|<span data-ttu-id="954af-265">Månad/månader</span><span class="sxs-lookup"><span data-stu-id="954af-265">Month(s)</span></span>|  
|<span data-ttu-id="954af-266">K</span><span class="sxs-lookup"><span data-stu-id="954af-266">Q</span></span>|<span data-ttu-id="954af-267">Kvartal</span><span class="sxs-lookup"><span data-stu-id="954af-267">Quarter(s)</span></span>|  
|<span data-ttu-id="954af-268">Å</span><span class="sxs-lookup"><span data-stu-id="954af-268">Y</span></span>|<span data-ttu-id="954af-269">År</span><span class="sxs-lookup"><span data-stu-id="954af-269">Year(s)</span></span>|  

 <span data-ttu-id="954af-270">Du kan bygga upp en datumformel på tre sätt.</span><span class="sxs-lookup"><span data-stu-id="954af-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="954af-271">Följande exempel visar hur aktuell plus en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="954af-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="954af-272">LV</span><span class="sxs-lookup"><span data-stu-id="954af-272">CW</span></span>|<span data-ttu-id="954af-273">Löpande (innevarande) vecka</span><span class="sxs-lookup"><span data-stu-id="954af-273">Current week</span></span>|  
|<span data-ttu-id="954af-274">LM</span><span class="sxs-lookup"><span data-stu-id="954af-274">CM</span></span>|<span data-ttu-id="954af-275">Löpande (innevarande) månad</span><span class="sxs-lookup"><span data-stu-id="954af-275">Current month</span></span>|  

 <span data-ttu-id="954af-276">Följande exempel visar hur ett antal och en tidsenhet.</span><span class="sxs-lookup"><span data-stu-id="954af-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="954af-277">Ett nummer får inte vara högre än 9 999.</span><span class="sxs-lookup"><span data-stu-id="954af-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="954af-278">10D</span><span class="sxs-lookup"><span data-stu-id="954af-278">10D</span></span>|<span data-ttu-id="954af-279">Tio dagar från dagens datum.</span><span class="sxs-lookup"><span data-stu-id="954af-279">10 days from today</span></span>|  
|<span data-ttu-id="954af-280">2V</span><span class="sxs-lookup"><span data-stu-id="954af-280">2W</span></span>|<span data-ttu-id="954af-281">Två veckor från dagens datum</span><span class="sxs-lookup"><span data-stu-id="954af-281">2 weeks from today</span></span>|  

 <span data-ttu-id="954af-282">Följande exempel visar hur en tidsenhet och ett antal.</span><span class="sxs-lookup"><span data-stu-id="954af-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="954af-283">D10</span><span class="sxs-lookup"><span data-stu-id="954af-283">D10</span></span>|<span data-ttu-id="954af-284">Den tionde dagen varje månad.</span><span class="sxs-lookup"><span data-stu-id="954af-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="954af-285">VD4</span><span class="sxs-lookup"><span data-stu-id="954af-285">WD4</span></span>|<span data-ttu-id="954af-286">Den nästa fjärde dagen i en vecka (torsdag)</span><span class="sxs-lookup"><span data-stu-id="954af-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="954af-287">Följande exempel visar hur du kombinera dessa tre metoder om så behövs.</span><span class="sxs-lookup"><span data-stu-id="954af-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="954af-288">LM+10D</span><span class="sxs-lookup"><span data-stu-id="954af-288">CM+10D</span></span>|<span data-ttu-id="954af-289">Löpande månad + 10 dagar</span><span class="sxs-lookup"><span data-stu-id="954af-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="954af-290">Följande exempel visar hur du använder ett minustecken för att ange ett datum i det förflutna.</span><span class="sxs-lookup"><span data-stu-id="954af-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="954af-291">-1Å</span><span class="sxs-lookup"><span data-stu-id="954af-291">-1Y</span></span>|<span data-ttu-id="954af-292">1 år sedan från idag</span><span class="sxs-lookup"><span data-stu-id="954af-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="954af-293">Se även</span><span class="sxs-lookup"><span data-stu-id="954af-293">See Also</span></span>  
 [<span data-ttu-id="954af-294">Söka, filtrera och sortera data</span><span class="sxs-lookup"><span data-stu-id="954af-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="954af-295">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="954af-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


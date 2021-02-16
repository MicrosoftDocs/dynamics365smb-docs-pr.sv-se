---
title: Profiler för klassificering av kontakter
description: Konfigurera profilfrågeformulär för att klassificera dina affärskontakter
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2020
ms.openlocfilehash: 65c27bee86d273c467709f1e238b996829d73f37
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755448"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="990ce-103">Använda profilfrågeformulär för att klassificera affärskontakter</span><span class="sxs-lookup"><span data-stu-id="990ce-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="990ce-104">Du kan skapa profilfrågeformulär som du vill använda när du anger uppgifter om kontakternas profiler.</span><span class="sxs-lookup"><span data-stu-id="990ce-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="990ce-105">I varje frågeformulär kan du skapa frågor som du vill ställa till kontakterna.</span><span class="sxs-lookup"><span data-stu-id="990ce-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="990ce-106">Du kan också köra frågeformuläret när du automatiskt vill besvara några av frågorna på grundval av kontakt, kund eller leverantör.</span><span class="sxs-lookup"><span data-stu-id="990ce-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="990ce-107">Lägga till profilfrågeformulär så här</span><span class="sxs-lookup"><span data-stu-id="990ce-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="990ce-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Enkätsinställningar** och välj sedan tillhörande länk.</span><span class="sxs-lookup"><span data-stu-id="990ce-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="990ce-109">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="990ce-109">Choose the **New** Action.</span></span>  
3.  <span data-ttu-id="990ce-110">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="990ce-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="990ce-111">Lägga till frågor till ett frågeformulär</span><span class="sxs-lookup"><span data-stu-id="990ce-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="990ce-112">Välj relevant profilfrågeformulär och välj åtgärden **Redigera inställningar för frågeformulär**.</span><span class="sxs-lookup"><span data-stu-id="990ce-112">Choose the relevant profile questionnaire, and then choose the **Edit Questionnaire Setup** action.</span></span>  
2.  <span data-ttu-id="990ce-113">På den första tomma raden väljer du **Fråga** i fältet **Typ** och skriver frågan i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="990ce-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="990ce-114">Fyll i de övriga fälten på raden.</span><span class="sxs-lookup"><span data-stu-id="990ce-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="990ce-115">På nästa tomma rad väljer du **Svar** i fältet **Radtyp** och skriver svaret i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="990ce-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="990ce-116">I fältet **Prioritet** väljer du önskad prioritet.</span><span class="sxs-lookup"><span data-stu-id="990ce-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="990ce-117">I fälten **Från värde** och **Till värde** definierar du ett poängintervall.</span><span class="sxs-lookup"><span data-stu-id="990ce-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="990ce-118">De kontakter som får poäng inom det angivna intervallet får svaret.</span><span class="sxs-lookup"><span data-stu-id="990ce-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="990ce-119">Upprepa stegen och ange alla frågor och svar i profilfrågeformuläret.</span><span class="sxs-lookup"><span data-stu-id="990ce-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="990ce-120">När du har skapat ett frågeformulär, måste du skapa kontaktgraderingar för att klassificera kontakterna.</span><span class="sxs-lookup"><span data-stu-id="990ce-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="990ce-121">Du kan också skapa frågor som klassas automatiskt baserat på informationen på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="990ce-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="990ce-122">När du anger en fråga som ska besvaras automatiskt väljer du <STRONG>Rad</STRONG> och sedan <STRONG>Frågedetaljer</STRONG>. Ange därefter kriterier som ska användas när den besvaras.</span><span class="sxs-lookup"><span data-stu-id="990ce-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="990ce-123">Den automatiska klassificeringen av kontakter</span><span class="sxs-lookup"><span data-stu-id="990ce-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="990ce-124">Du kan klassificeras dina kontakter automatiskt efter kunder, leverantörer och kontaktuppgifter genom att automatiskt besvarade profilfrågor skapas på sidan **Profil frågeformulär inst.**.</span><span class="sxs-lookup"><span data-stu-id="990ce-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="990ce-125">Det är bara kontakter som registrerats som kunder eller leverantörer som kan tilldelas klassificering baserad på kund- respektive leverantörsdata.</span><span class="sxs-lookup"><span data-stu-id="990ce-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="990ce-126">Den automatiska klassificeringen uppdateras inte automatiskt.</span><span class="sxs-lookup"><span data-stu-id="990ce-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="990ce-127">Följaktligen kan du behöva uppdatera profilfrågeformulären när du har uppdaterat de kund-, leverantörs- eller kontaktdata som de grundas på.</span><span class="sxs-lookup"><span data-stu-id="990ce-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="990ce-128">Om du tilldelar kontakter profilfrågeformulär, som innehåller de automatiskt besvarade profilfrågor som du har skapat, tilldelar [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt de rätta svaren för kontakterna.</span><span class="sxs-lookup"><span data-stu-id="990ce-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[prod_short](includes/prod_short.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="990ce-129">Exempel</span><span class="sxs-lookup"><span data-stu-id="990ce-129">Example</span></span>
<span data-ttu-id="990ce-130">Du kan klassificera kontakterna efter hur mycket de har köpt från dig:</span><span class="sxs-lookup"><span data-stu-id="990ce-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="990ce-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="990ce-132"><strong>Kopplas till</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="990ce-133">A</span><span class="sxs-lookup"><span data-stu-id="990ce-133">A</span></span></p></td>
<td><p><span data-ttu-id="990ce-134">kontakter som har köpt för 500 000 SEK eller mer</span><span class="sxs-lookup"><span data-stu-id="990ce-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="990ce-135">B</span><span class="sxs-lookup"><span data-stu-id="990ce-135">B</span></span></p></td>
<td><p><span data-ttu-id="990ce-136">kontakter som har köpt för 100 000 upp till 499 999 SEK</span><span class="sxs-lookup"><span data-stu-id="990ce-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="990ce-137">S</span><span class="sxs-lookup"><span data-stu-id="990ce-137">C</span></span></p></td>
<td><p><span data-ttu-id="990ce-138">kontakter som har köpt för 99 999 SEK eller mindre</span><span class="sxs-lookup"><span data-stu-id="990ce-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="990ce-139">Det gör du genom att fylla i sidan **Profil frågeformulär inst.** så här:</span><span class="sxs-lookup"><span data-stu-id="990ce-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="990ce-140"><strong>Radtyp</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="990ce-141"><strong>Beskrivning</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="990ce-142"><strong>Automatisk klassificering</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="990ce-143"><strong>Från värde</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="990ce-144"><strong>Till värde</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="990ce-145">Fråga</span><span class="sxs-lookup"><span data-stu-id="990ce-145">Question</span></span></p></td>
<td><p><span data-ttu-id="990ce-146">ABC-klassificering</span><span class="sxs-lookup"><span data-stu-id="990ce-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="990ce-147">Klicka för att markera</span><span class="sxs-lookup"><span data-stu-id="990ce-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="990ce-148">Svar</span><span class="sxs-lookup"><span data-stu-id="990ce-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="990ce-149">A</span><span class="sxs-lookup"><span data-stu-id="990ce-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="990ce-150">500,000</span><span class="sxs-lookup"><span data-stu-id="990ce-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="990ce-151">Svar</span><span class="sxs-lookup"><span data-stu-id="990ce-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="990ce-152">B</span><span class="sxs-lookup"><span data-stu-id="990ce-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="990ce-153">100,000</span><span class="sxs-lookup"><span data-stu-id="990ce-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="990ce-154">499,999</span><span class="sxs-lookup"><span data-stu-id="990ce-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="990ce-155">Svar</span><span class="sxs-lookup"><span data-stu-id="990ce-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="990ce-156">S</span><span class="sxs-lookup"><span data-stu-id="990ce-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="990ce-157">99.999</span><span class="sxs-lookup"><span data-stu-id="990ce-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="990ce-158">Fyll sedan i sidan **Profilfrågedetaljer** så här:</span><span class="sxs-lookup"><span data-stu-id="990ce-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="990ce-159"><strong>Fält</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="990ce-160"><strong>Värde</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="990ce-161"><strong>Kundklassificeringsfält</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="990ce-162"><emphasis>Försäljning (BVA)</emphasis></span><span class="sxs-lookup"><span data-stu-id="990ce-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="990ce-163"><strong>Klassificeringsmetod</strong></span><span class="sxs-lookup"><span data-stu-id="990ce-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="990ce-164"><emphasis>Definierat värde</emphasis></span><span class="sxs-lookup"><span data-stu-id="990ce-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="990ce-165">När du tilldelar en kontakt profilfrågeformulär som innehåller denna fråga anges automatiskt relevant svar för kontakten på profilraderna på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="990ce-165">When you assign the profile questionnaire containing this question to a contact, application automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="990ce-166">Se även</span><span class="sxs-lookup"><span data-stu-id="990ce-166">See Also</span></span>
[<span data-ttu-id="990ce-167">Skapar kontakter</span><span class="sxs-lookup"><span data-stu-id="990ce-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  

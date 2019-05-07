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
ms.date: 04/01/2019
ms.openlocfilehash: fe02153a89ad5f63855cff5eec5344d601c8663a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934448"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="04a67-103">Använda profilfrågeformulär för att klassificera affärskontakter</span><span class="sxs-lookup"><span data-stu-id="04a67-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="04a67-104">Du kan skapa profilfrågeformulär som du vill använda när du anger uppgifter om kontakternas profiler.</span><span class="sxs-lookup"><span data-stu-id="04a67-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="04a67-105">I varje frågeformulär kan du skapa frågor som du vill ställa till kontakterna.</span><span class="sxs-lookup"><span data-stu-id="04a67-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="04a67-106">Du kan också köra frågeformuläret när du automatiskt vill besvara några av frågorna på grundval av kontakt, kund eller leverantör.</span><span class="sxs-lookup"><span data-stu-id="04a67-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="04a67-107">Lägga till profilfrågeformulär så här</span><span class="sxs-lookup"><span data-stu-id="04a67-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="04a67-108">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Frågeformulärsinställningar** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="04a67-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04a67-109">På fliken **Start** i gruppen **Ny** väljer du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="04a67-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="04a67-110">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="04a67-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="04a67-111">Lägga till frågor till ett frågeformulär</span><span class="sxs-lookup"><span data-stu-id="04a67-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="04a67-112">Välj relevant profilfrågeformulär och välj **Redigera inställningar för frågeformulär** på fliken **Start** i gruppen **Process**.</span><span class="sxs-lookup"><span data-stu-id="04a67-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="04a67-113">På den första tomma raden väljer du **Fråga** i fältet **Typ** och skriver frågan i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="04a67-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="04a67-114">Fyll i de övriga fälten på raden.</span><span class="sxs-lookup"><span data-stu-id="04a67-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="04a67-115">På nästa tomma rad väljer du **Svar** i fältet **Radtyp** och skriver svaret i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="04a67-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="04a67-116">I fältet **Prioritet** väljer du önskad prioritet.</span><span class="sxs-lookup"><span data-stu-id="04a67-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="04a67-117">I fälten **Från värde** och **Till värde** definierar du ett poängintervall.</span><span class="sxs-lookup"><span data-stu-id="04a67-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="04a67-118">De kontakter som får poäng inom det angivna intervallet får svaret.</span><span class="sxs-lookup"><span data-stu-id="04a67-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="04a67-119">Upprepa stegen och ange alla frågor och svar i profilfrågeformuläret.</span><span class="sxs-lookup"><span data-stu-id="04a67-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="04a67-120">När du har skapat ett frågeformulär, måste du skapa kontaktgraderingar för att klassificera kontakterna.</span><span class="sxs-lookup"><span data-stu-id="04a67-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="04a67-121">Du kan också skapa frågor som klassas automatiskt baserat på informationen på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="04a67-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="04a67-122">När du anger en fråga som ska besvaras automatiskt väljer du <STRONG>Rad</STRONG> och sedan <STRONG>Frågedetaljer</STRONG>. Ange därefter kriterier som ska användas när den besvaras.</span><span class="sxs-lookup"><span data-stu-id="04a67-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="04a67-123">Den automatiska klassificeringen av kontakter</span><span class="sxs-lookup"><span data-stu-id="04a67-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="04a67-124">Du kan klassificeras dina kontakter automatiskt efter kunder, leverantörer och kontaktuppgifter genom att automatiskt besvarade profilfrågor skapas på sidan **Profil frågeformulär inst.**.</span><span class="sxs-lookup"><span data-stu-id="04a67-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="04a67-125">Det är bara kontakter som registrerats som kunder eller leverantörer som kan tilldelas klassificering baserad på kund- respektive leverantörsdata.</span><span class="sxs-lookup"><span data-stu-id="04a67-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="04a67-126">Den automatiska klassificeringen uppdateras inte automatiskt.</span><span class="sxs-lookup"><span data-stu-id="04a67-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="04a67-127">Följaktligen kan du behöva uppdatera profilfrågeformulären när du har uppdaterat de kund-, leverantörs- eller kontaktdata som de grundas på.</span><span class="sxs-lookup"><span data-stu-id="04a67-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="04a67-128">Om du tilldelar kontakter profilfrågeformulär, som innehåller de automatiskt besvarade profilfrågor som du har skapat, tilldelar [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt de rätta svaren för kontakterna.</span><span class="sxs-lookup"><span data-stu-id="04a67-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="04a67-129">Exempel</span><span class="sxs-lookup"><span data-stu-id="04a67-129">Example</span></span>
<span data-ttu-id="04a67-130">Du kan klassificera kontakterna efter hur mycket de har köpt från dig:</span><span class="sxs-lookup"><span data-stu-id="04a67-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04a67-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="04a67-132"><strong>Kopplas till</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04a67-133">A</span><span class="sxs-lookup"><span data-stu-id="04a67-133">A</span></span></p></td>
<td><p><span data-ttu-id="04a67-134">kontakter som har köpt för 500 000 SEK eller mer</span><span class="sxs-lookup"><span data-stu-id="04a67-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04a67-135">B</span><span class="sxs-lookup"><span data-stu-id="04a67-135">B</span></span></p></td>
<td><p><span data-ttu-id="04a67-136">kontakter som har köpt för 100 000 upp till 499 999 SEK</span><span class="sxs-lookup"><span data-stu-id="04a67-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04a67-137">S</span><span class="sxs-lookup"><span data-stu-id="04a67-137">C</span></span></p></td>
<td><p><span data-ttu-id="04a67-138">kontakter som har köpt för 99 999 SEK eller mindre</span><span class="sxs-lookup"><span data-stu-id="04a67-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04a67-139">Det gör du genom att fylla i sidan **Profil frågeformulär inst.** så här:</span><span class="sxs-lookup"><span data-stu-id="04a67-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


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
<th><span data-ttu-id="04a67-140"><strong>Radtyp</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="04a67-141"><strong>Beskrivning</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="04a67-142"><strong>Automatisk klassificering</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="04a67-143"><strong>Från värde</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="04a67-144"><strong>Till värde</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04a67-145">Fråga</span><span class="sxs-lookup"><span data-stu-id="04a67-145">Question</span></span></p></td>
<td><p><span data-ttu-id="04a67-146">ABC-klassificering</span><span class="sxs-lookup"><span data-stu-id="04a67-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="04a67-147">Klicka för att markera</span><span class="sxs-lookup"><span data-stu-id="04a67-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04a67-148">Svar</span><span class="sxs-lookup"><span data-stu-id="04a67-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="04a67-149">A</span><span class="sxs-lookup"><span data-stu-id="04a67-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04a67-150">500,000</span><span class="sxs-lookup"><span data-stu-id="04a67-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04a67-151">Svar</span><span class="sxs-lookup"><span data-stu-id="04a67-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="04a67-152">B</span><span class="sxs-lookup"><span data-stu-id="04a67-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04a67-153">100,000</span><span class="sxs-lookup"><span data-stu-id="04a67-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="04a67-154">499,999</span><span class="sxs-lookup"><span data-stu-id="04a67-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04a67-155">Svar</span><span class="sxs-lookup"><span data-stu-id="04a67-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="04a67-156">S</span><span class="sxs-lookup"><span data-stu-id="04a67-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="04a67-157">99.999</span><span class="sxs-lookup"><span data-stu-id="04a67-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04a67-158">Fyll sedan i sidan **Profilfrågedetaljer** så här:</span><span class="sxs-lookup"><span data-stu-id="04a67-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04a67-159"><strong>Fält</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="04a67-160"><strong>Värde</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04a67-161"><strong>Kundklassificeringsfält</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="04a67-162"><emphasis>Försäljning (BVA)</emphasis></span><span class="sxs-lookup"><span data-stu-id="04a67-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04a67-163"><strong>Klassificeringsmetod</strong></span><span class="sxs-lookup"><span data-stu-id="04a67-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="04a67-164"><emphasis>Definierat värde</emphasis></span><span class="sxs-lookup"><span data-stu-id="04a67-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="04a67-165">När du tilldelar en kontakt profilfrågeformulär som innehåller denna fråga anges automatiskt relevant svar för kontakten på profilraderna på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="04a67-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="04a67-166">Se även</span><span class="sxs-lookup"><span data-stu-id="04a67-166">See Also</span></span>
[<span data-ttu-id="04a67-167">Skapar kontakter</span><span class="sxs-lookup"><span data-stu-id="04a67-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  

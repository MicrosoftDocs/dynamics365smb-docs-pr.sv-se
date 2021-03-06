---
title: Profiler för klassificering av kontakter
description: Konfigurera profilfrågeformulär för att klassificera dina affärskontakter
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2021
ms.openlocfilehash: 31321ce4cafd17efc8a7732c81e874df1a1d763a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785504"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Använda profilfrågeformulär för att klassificera affärskontakter
Du kan skapa profilfrågeformulär som du vill använda när du anger uppgifter om kontakternas profiler. I varje frågeformulär kan du skapa frågor som du vill ställa till kontakterna.  

Du kan också köra frågeformuläret när du automatiskt vill besvara några av frågorna på grundval av kontakt, kund eller leverantör.  

## <a name="to-add-a-profile-questionnaire"></a>Lägga till profilfrågeformulär så här
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Enkätsinställningar** och välj sedan tillhörande länk.  
2.  Välj åtgärden **Ny**.  
3.  Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Lägga till frågor till ett frågeformulär
1.  Välj relevant profilfrågeformulär och välj åtgärden **Redigera inställningar för frågeformulär**.  
2.  På den första tomma raden väljer du **Fråga** i fältet **Typ** och skriver frågan i fältet **Beskrivning**. Fyll i de övriga fälten på raden.  
3.  På nästa tomma rad väljer du **Svar** i fältet **Radtyp** och skriver svaret i fältet **Beskrivning**.  
4.  I fältet **Prioritet** väljer du önskad prioritet. I fälten **Från värde** och **Till värde** definierar du ett poängintervall. De kontakter som får poäng inom det angivna intervallet får svaret.  

Upprepa stegen och ange alla frågor och svar i profilfrågeformuläret.

När du har skapat ett frågeformulär, måste du skapa kontaktgraderingar för att klassificera kontakterna. Du kan också skapa frågor som klassas automatiskt baserat på informationen på kontaktkortet.  

> [!NOTE]
> När du anger en fråga som ska besvaras automatiskt väljer du <STRONG>Rad</STRONG> och sedan <STRONG>Frågedetaljer</STRONG>. Ange därefter kriterier som ska användas när den besvaras.

## <a name="the-automatic-classification-of-contacts"></a>Den automatiska klassificeringen av kontakter
Du kan klassificeras dina kontakter automatiskt efter kunder, leverantörer och kontaktuppgifter genom att automatiskt besvarade profilfrågor skapas på sidan **Profil frågeformulär inst.**.  

> [!NOTE]
> Det är bara kontakter som registrerats som kunder eller leverantörer som kan tilldelas klassificering baserad på kund- respektive leverantörsdata. Den automatiska klassificeringen uppdateras inte automatiskt. Följaktligen kan du behöva uppdatera profilfrågeformulären när du har uppdaterat de kund-, leverantörs- eller kontaktdata som de grundas på.  

Om du tilldelar kontakter profilfrågeformulär, som innehåller de automatiskt besvarade profilfrågor som du har skapat, tilldelar [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt de rätta svaren för kontakterna.  

## <a name="example"></a>Exempel
Du kan klassificera kontakterna efter hur mycket de har köpt från dig:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Svar</strong></th>
<th><strong>Kopplas till</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>kontakter som har köpt för 500 000 SEK eller mer</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>kontakter som har köpt för 100 000 upp till 499 999 SEK</p></td>
</tr>
<tr class="odd">
<td><p>S</p></td>
<td><p>kontakter som har köpt för 99 999 SEK eller mindre</p></td>
</tr>
</tbody>
</table>

Det gör du genom att fylla i sidan **Profil frågeformulär inst.** så här:


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
<th><strong>Radtyp</strong></th>
<th><strong>Beskrivning</strong></th>
<th><strong>Automatisk klassificering</strong></th>
<th><strong>Från värde</strong></th>
<th><strong>Till värde</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fråga</p></td>
<td><p>ABC-klassificering</p></td>
<td><p>Klicka för att markera</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Svar</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>S</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99.999</p></td>
</tr>
</tbody>
</table>

Fyll sedan i sidan **Profilfrågedetaljer** så här:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Fält</strong></th>
<th><strong>Värde</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Kundklassificeringsfält</strong></td>
<td><emphasis>Försäljning (BVA)</emphasis></td>
</tr>
<tr>
<td><strong>Klassificeringsmetod</strong></td>
<td><emphasis>Definierat värde</emphasis></td>
</tr>
</tbody>
</table>

När du tilldelar en kontakt profilfrågeformulär som innehåller denna fråga anges automatiskt relevant svar för kontakten på profilraderna på kontaktkortet.

## <a name="see-also"></a>Se även
[Skapar kontakter](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
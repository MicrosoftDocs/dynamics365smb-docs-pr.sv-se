---
title: Profiler för klassificering av kontakter
description: Läs om hur du ställer in profil frågeformulär för att hjälpa till att klassificera affärskontakternas profiler.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 6ce13672651a5b6b65712928b764ad11b3db514d
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588532"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Använda profilfrågeformulär för att klassificera affärskontakter
Du kan skapa profilfrågeformulär som du vill använda när du anger uppgifter om kontakternas profiler. I varje frågeformulär kan du skapa frågor som du vill ställa till kontakterna.  

Du kan också köra frågeformuläret när du automatiskt vill besvara några av frågorna på grundval av kontakt, kund eller leverantör.  

## <a name="to-add-a-profile-questionnaire"></a>Lägga till profilfrågeformulär så här
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Profil frågeformulär inst.** och väljer sedan relaterad länk.  
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

|Svar|Kopplas till|
|--- |--- |
|A|kontakter som har köpt för 500 000 SEK eller mer|
|B|kontakter som har köpt för 100 000 upp till 499 999 SEK|
|S|kontakter som har köpt för 99 999 SEK eller mindre|

Det gör du genom att fylla i sidan **Profil frågeformulär inst.** så här:

| Typ     | Beskrivning        | Automatisk klassificering     | Från värde | Till värde |
|----------|--------------------|------------------------------|------------|----------|
| Fråga | ABC-klassificering | Klicka för att markera |            |          |
| Svar   | A                  |                              | 500,000    |          |
| Svar   | B                  |                              | 100,000    | 499,999  |
| Svar   | S                  |                              |            | 99.999   |

Fyll sedan i sidan **Profilfrågedetaljer** så här:

| Fält                         | Värde         |
|-------------------------------|---------------|
| Kundklassificeringsfält | Försäljning (BVA)   |
| Klassificeringsmetod         | Definierat värde |

När du tilldelar en kontakt profilfrågeformulär som innehåller denna fråga anges automatiskt relevant svar för kontakten på profilraderna på kontaktkortet.

## <a name="see-also"></a>Se även

[Skapar kontakter](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
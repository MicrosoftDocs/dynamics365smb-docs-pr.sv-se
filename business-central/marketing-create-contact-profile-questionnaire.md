---
title: Profiler för klassificering av kontakter
description: Läs om hur du ställer in profil frågeformulär för att hjälpa till att klassificera affärskontakternas profiler.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.search.form: 5109, 5110
ms.author: edupont
ms.date: 05/20/2022
ms.openlocfilehash: 135ca390dbf00e46deefbe6e195acfbcf11b959c
ms.sourcegitcommit: 93f30ce3349233cbcd03f300e74b654b49fa5518
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/24/2022
ms.locfileid: "8799670"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Använda profilfrågeformulär för att klassificera affärskontakter

Genom att gradera presumtiva kunder kan du identifiera vilka som en försäljningskampanj helst bör riktas mot. Du kan skapa profilfrågeformulär som du vill använda när du anger uppgifter om kontakternas profiler. I varje frågeformulär kan du skapa frågor som du vill ställa till kontakterna. På så sätt kan du gruppera kontakterna så att dina kampanjer blir mer sannolika för att ge rätt personer till gång till de kriterier som du anger med hjälp av frågeformulären.  

Med rätt frågeformulär, kan du gradera de presumtiva kunderna och gruppera dem i kategorier. Du kan använda befintliga frågor och svar och kombinera dem med nya frågor och svar som du använder som grund för graderingen. Varje svar i graderingen ges ett poängvärde och, beroende på vilket intervall du skapar för kategorierna (*Från värde* och *Till värde*), grupperas kontakterna i de kategorier som du har definierat. Det kan till exempel vara kunder som graderas med *ABC*, *Hög/Låg lojalitet* hos leverantörer eller presumtiva kunder med graderingen *Platina/Guld/Silver*.  

Du kan också köra frågeformuläret när du automatiskt vill besvara några av frågorna på grundval av kontakt, kund eller leverantör.  

## <a name="to-add-a-profile-questionnaire"></a>Lägga till profilfrågeformulär så här

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Profil frågeformulär inst.** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Lägga till frågor till ett frågeformulär

1. Välj relevant profilfrågeformulär och välj åtgärden **Redigera inställningar för frågeformulär**.  
2. På den första tomma raden väljer du **Fråga** i fältet **Typ** och skriver frågan i fältet **Beskrivning**. Fyll i de övriga fälten på raden.  

    Du kan också lägga till information i frågan.

    1. Välj raden med frågan och välj sedan menyn **Rad** och välj sedan **Frågedetaljer**.  

    2. Markera fältet **Auto. kontaktklassificering** på sidan **Gruppering** välj **Profil frågedetaljer**.  

    3. I fältet **Kontakten kontaktklass.fält. Fältet**, markera alternativet **Gradering**.  

    4. Fyll i fältet **Min. besvarade frågor %**. Standardvärdet är **0**.  

        Anger det antal frågor (i procent) som måste besvaras för att den här graderingen ska beräknas.

    5. På fliken **Åtgärder** i gruppen **Sida** väljer du **Svarspoäng**. Ange hur många poäng du vill ge varje svar i sidan **Svarspoäng**.

        Om du vill ha en översikt över de poäng som du har gett varje svar väljer du **Svarspoäng** åtgärd.

    6. Om du vill köra en uppdatering går du tillbaka till sidan inställningar för **profilfrågeformulär**. Välj **Uppdatera klassificering** i gruppen **Funktioner** på fliken **Åtgärder**.

    På sidan **Profil frågeformulär inst.** visas antalet kontakter som uppfyller det villkor som visas i fältet **Antal kontakter** samt i **Kontaktkort** för varje kontakt.

3. På nästa tomma rad väljer du **Svar** i fältet **Radtyp** och skriver svaret i fältet **Beskrivning**.  
4. I fältet **Prioritet** väljer du önskad prioritet. I fälten **Från värde** och **Till värde** definierar du ett poängintervall. De kontakter som får poäng inom det angivna intervallet får svaret.  

Upprepa stegen och ange alla frågor och svar i profilfrågeformuläret.

När du har skapat ett frågeformulär kan du använda det för att betygsätta och klassificera dina kontakter. Du kan också skapa frågor som klassas automatiskt baserat på informationen på kontaktkortet.  

> [!NOTE]
> När du anger en fråga som ska besvaras automatiskt väljer du **Rad** och sedan **Frågedetaljer**. Ange därefter kriterier som ska användas när den besvaras.

## <a name="apply-questionnaires-to-contacts"></a>Använd enkäter för kontakter

Du kan koppla dina enkäter till kontakter manuellt. Öppna bara det relevanta kontaktkortet och välj sedan åtgärden **Profil**. När du sedan har använt de enkäter som du vill använda kan du börja använda kategorierna i dina kampanjer.  

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
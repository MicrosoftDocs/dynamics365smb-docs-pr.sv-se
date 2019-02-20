---
title: "Ställ in Information för kontakter | Microsoft Docs"
description: "Beskriver uppgifterna om du vill ange information och koder, till exempel om befintliga branschgrupper och affärsrelationer, innan du skapar kontakter."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Ställa in kontakter
När du skapar kontakter kan du ange särskild information, till exempel vilken bransch kontaktens företag tillhör och vilken affärsrelation du har med kontakten.

Innan du skapar kontakter och registrerar uppgifter om affärsrelationerna, måste du skapa olika koder som du använder för att tilldela informationen till kontaktföretagen och -personerna. Du kan skapa koder för utskicksgrupper, branschgrupper, affärsrelationer, webbadresser, befattningsnivåer och arbetsansvar.

Om du ställer in den här information kan du skapa kontakterna på ett mer organiserat sätt och att söka efter kontakterna utifrån en viss grupp blir mer effektivt. Varje grupp på företaget kan hitta den här informationen och därför blir kommunikationen med kontakterna mer framgångsrik.

I samband med att du konfigurerar dina kontakter måste du ställa in de affärsrelationer du har med kontakterna, t.ex. presumtiv kund, bank, konsult eller tjänstleverantör. Mer information finns i [ställa in affärsrelationer på kontaktföretag](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Ställa in Branschgrupper för kontaktföretag
Branschgrupper används för att visa vilken bransch kontakterna tillhör, exempelvis detaljhandel eller bilBransch.

Att använda Branschgrupper på kontakter är en två-stegsprocess. Först definierar du Branschgruppkoden. Du måste bara utföra den här steget en gång för varje Branschgrupp. När du har en Branschgrupp kan du börja koppla koden till kontaktföretag.

> [!NOTE]  
>   Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.

### <a name="to-define-an-industry-group-code"></a>Definiera en Branschgruppskod
Koden för branschgruppen definierar typen eller kategorin för den gruppen, till exempel ANNONS för annonsering eller PRESS för TV och radio. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du sidan **branschgrupper**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Branschgrupper** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

### <a name="AssignIndustryGroupContact"></a> Så här tilldelar du industrigrupper till en kontakt
Du kan inte tilldela branschgrupper till en kontaktperson, endast företag.

1. Öppna kontakten .
2. Välj åtgärden **företag** och sedan **branschgrupper**. Sidan **Kontakt branschgrupper** öppnas.
3. I fältet **branschgruppkod**, markera den branschgrupp du vill tilldela.

Upprepa stegen för varje branschgrupp du vill skapa. Branschgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet branschgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal branschgrupper** på avsnittet **Segmentering** på **Kontakt**-sidan.

När du har tilldelat kontakterna branschgrupper kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Ställa in utskicksgrupper för kontakter
Utskicksgrupper används för att definiera kontaktgrupper som du vill ge samma information. Du kan till exempel skapa en utskicksgrupp med de kontakter du vill skicka flyttkort till eller en annan grupp för att skicka julklappar.

Att använda utskicksgrupper på kontakter är en två-stegsprocess. Först definierar du utskicksgruppkoden. Du måste bara utföra den här steget en gång för varje utskicksgrupp. När du har en utskicksgrupp kan du börja koppla koden till kontaktföretag.

### <a name="to-define-mailing-group-codes"></a>Definiera utskicksgruppkoder
Utskicksgruppkoden definierar typen eller kategorin för den gruppen, till exempel FLYTTA för kontorsflyttning eller GÅVA för julklappar. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du sidan **Utskicksgrupper**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utskicksgrupper** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

### <a name="AssignMailGroupContact"></a> Så här tilldelar du utskicksgrupp till en kontakt
1. Öppna kontakten .
2. Välj åtgärden **Utskicksgrupper**. Sidan **Kontakt Utskicksgrupper** öppnas.
3. I fältet **Utskicksgruppskod**, markera den utskicksgrupp du vill tilldela.

Upprepa stegen för varje utskicksgrupp du vill tilldela. Utskicksgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet utskicksgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal utskicksgrupper** på avsnittet **Segmentering** på **Kontakt**-sidan.

När du har tilldelat kontakterna utskicksgrupp kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Ställa in alternativa adresser för en kontakt
Du kan tilldela kontakterna alternativa adresser som är aktuella ibland för e-post och meddelanden, till exempel deras sommarbostäder. Du kan tilldela varje alternativ adress ett eller flera datumintervall som du har angett för kontakterna för att visa när adresserna gäller.

### <a name="to-assign-an-alternate-address"></a>Så här tilldelar du alternativa adresser
1. Öppna kontakten .
2. Välj åtgärden **Alternativ adress** och välj sedan **Kort**. Sidan **Kontakt alt. adress lista** öppnas.
3. Ange en ny alternativ adress och fyll i fälten på sidan för **kontaktens adresskort för alternativ adress**.

Upprepa stegen för varje alternativ adress du vill tilldela. För varje alternativ adress kan du ange ett eller flera datumintervall.

Alternativa adresser kan också tilldelas från sidan Kontaktlista på samma sätt.

### <a name="to-assign-an-alternate-address-date-range"></a>Så här tilldelar du datumintervall för alternativa adresser
1. Öppna kontakten .
2. Välj åtgärden **Alternativ adress** och välj sedan **Datumintervall**. Sidan **Kontakt alt. adr. datuminterv.** öppnas.
3. Välj åtgärden **Ny**.
4. I fältet **Kontakt alt. adresskod**, välj en alternativ adress för den här kontakten och fyll sedan i fälten **startdatum** och **slutdatum**.

Upprepa stegen för varje datumintervall du vill tilldela.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Ställa in arbetsansvar för kontaktpersonerna.
Du kan lägga till information om arbetsansvar för kontaktpersoner för att ange vad kontaktpersonen ansvarar för i företaget, till exempel IT, ledning eller produktion. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

Att använda arbetsansvar på kontakter är en två-stegsprocess. Först definierar du arbetsansvarkoden. Du måste bara utföra den här steget en gång för varje arbetsansvar. När du har en arbetsansvarkod kan du börja koppla koden till kontaktpersoner.

### <a name="to-define-a-job-responsibility-code"></a>Så här definierar du en arbetsansvarskod
Arbetsansvarkoden definierar typen eller kategorin för projektet, som t.ex. MARKNADSFÖRING eller KÖP. Du kan ha flera arbetsansvarkoder. Att definiera arbetsansvaret använder du sidan **Arbetsansvar**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arbetsansvar** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Så här tilldelar du arbetsansvar till en kontaktperson
Du kan inte tilldela arbetsansvar till kontaktföretag.

1. Öppna kontaktperson.
2. Välj åtgärden **Person** och sedan **Arbetsansvar**. Sidan **Kontakt arbetsansvar** öppnas.
3. I fältet **Arbetsansvarskod**, markera det arbetsansvar du vill tilldela.

Upprepa stegen för varje arbetsansvar du vill tilldela. Arbetsansvar kan också tilldelas i kontaktlista på samma sätt.

Antalet arbetsansvar som du har tilldelat kontakter anges automatiskt i fältet **Antal arbetsansvar** i avsnittet **Segmentering** på sidan **Kontakt**.

När du har tilldelat arbetsansvar till kontakterna kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Skapa befattningsnivåer för kontaktpersoner
Du kan använda befattningsnivåer på kontakterna om du vill ange vilken befattningsnivå de har i företaget, t.ex. företagsledning. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

Att använda befattningsnivåer på kontakter är en två-stegsprocess. Först definierar du befattningsnivåkoden. Du måste bara utföra den här steget en gång för varje befattningsnivå. När du har en befattningsnivåkod kan du börja koppla koden till kontaktpersoner.

### <a name="to-define-an-organizational-level-code"></a>För att definiera en befattningsnivåkod
Befattningsnivåkoden anger typen eller kategorin av befattningsnivån, som t.ex. VD eller CFO. Du kan ha flera befattningsnivåkoder. För att definiera befattningsnivån använder du sidan **Befattningsnivåer**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Befattningsnivåer** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>För att tilldela befattningsnivåer till en kontaktperson
Du kan endast tilldela befattningsnivåer till kontaktpersoner, inte kontaktföretag. Du kan endast tilldela en befattningsnivå per kontakt.

1. Öppna kontakten .
2. I fältet **Befattningsnivåer** väljer du den kod som du vill tilldela.

När du har fördelat befattningsnivåer till kontakterna kan du använda informationen för att skapa segment.

När du har tilldelat arbetsansvar till kontakterna kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Ställa in Webbadresser för kontaktföretag
Du kan använda webbadresser med dina kontaktföretag för att t.ex. identifiera sökmotorer och webbplatser på Internet som du vill använda för att söka efter information om kontakterna. När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

Att använda webbadresser på kontakter är en två-stegsprocess. Först definierar du webbadresskoden. Du måste bara utföra den här steget en gång för varje webbadress. När du har en webbadresskod kan du börja koppla koden till kontaktpersoner.

### <a name="to-define-a-web-source-code"></a>För att definiera en webbadresskod
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Webbadresser** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten **Kod**, **Beskrivning** och **URL**.

    Skriv %1 i fältet **URL** för att infoga en platshållare för ett sökord i URL:en. När du startar webbadress från en kontakt ersätts %1 med sökordet (till exempel namnet på företaget) som du har angett på sidan **Kontakt webbadresser**.

Upprepa stegen för varje webbkälla du vill skapa.

### <a name="to-assign-web-sources-to-a-contact-company"></a>För att tilldela webbadresser till ett kontaktföretag
När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

1. Öppna kontakten .
2. Välj åtgärden **företag** och sedan **webbadresser**. Sidan **Kontakt webbadresser** öppnas.
3. I fältet **webbadresskod**, välj webbadressen som du vill tilldela.
4. Skriv i fältet **Sökord** det sökord som ska användas för att hitta informationen.

Upprepa stegen för varje webbkälla du vill skapa.

Webbadresser kan också tilldelas på sidan **Kontaktlista** på samma sätt.

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
title: Ställ in Information för kontakter | Microsoft Docs
description: Beskriver uppgifterna om du vill ange information och koder, till exempel om befintliga branschgrupper och affärsrelationer, innan du skapar kontakter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed9a7b84798ac7b0bf103329c9e06ea0468aa03b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788083"
---
# <a name="set-up-contacts"></a>Ställa in kontakter
När du skapar kontakter kan du ange särskild information, till exempel vilken bransch kontakten tillhör och vilken affärsrelation du har med kontakten.

Innan du skapar kontakter och registrerar uppgifter om affärsrelationerna, måste du skapa olika koder som du använder för att tilldela informationen till kontaktföretagen och -personerna. Du kan skapa koder för utskicksgrupper, branschgrupper, affärsrelationer, webbadresser, befattningsnivåer och arbetsansvar. Du kan skapa dessa genom att välja åtgärden **nytt** när du söker i listor från kontaktkortet.  

Om du ställer in den här information kan du skapa kontakterna på ett mer organiserat sätt och att söka efter kontakterna utifrån en viss grupp blir mer effektivt. Varje grupp på företaget kan hitta den här informationen och därför blir kommunikationen med kontakterna mer framgångsrik.

## <a name="to-assign-industry-groups-to-a-contact"></a> Så här tilldelar du industrigrupper till en kontakt
Branschgrupper används för att visa vilken bransch kontakterna tillhör, exempelvis detaljhandel eller bilBransch.

> [!NOTE]
> Detta är endast tillåtet för kontakter av typen **företag**.

Koden för branschgruppen definierar typen eller kategorin för den gruppen, till exempel ANNONS för annonsering eller PRESS för TV och radio. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du sidan **branschgrupper**.

1. Öppna relevant kontaktkort.
2. Välj åtgärden **företag** och sedan **branschgrupper**. Sidan **Kontakt branschgrupper** öppnas.
3. I fältet **branschgruppkod**, markera den branschgrupp du vill tilldela.

Upprepa stegen för varje branschgrupp du vill skapa. Branschgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet branschgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal branschgrupper** på avsnittet **Segmentering** på **Kontaktkort**-sidan.

När du har tilldelat kontakterna branschgrupper kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="to-assign-mailing-groups-to-a-contact"></a> Så här tilldelar du utskicksgrupp till en kontakt
Utskicksgrupper används för att definiera kontaktgrupper som du vill ge samma information. Du kan till exempel skapa en utskicksgrupp med de kontakter du vill skicka flyttkort till eller en annan grupp för att skicka julklappar.

Utskicksgruppkoden definierar typen eller kategorin för den gruppen, till exempel FLYTTA för kontorsflyttning eller GÅVA för julklappar. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du sidan **Utskicksgrupper**.

1. Öppna relevant kontaktkort.
2. Välj åtgärden **Utskicksgrupper**. Sidan **Kontakt Utskicksgrupper** öppnas.
3. I fältet **Utskicksgruppskod**, markera den utskicksgrupp du vill tilldela.

Upprepa stegen för varje utskicksgrupp du vill tilldela. Utskicksgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet utskicksgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal utskicksgrupper** på avsnittet **Segmentering** på **Kontaktkort**-sidan.

När du har tilldelat kontakterna utskicksgrupp kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="to-define-a-contacts-alternate-address"></a>Så här definierar du en kontakts alternativa adress
Du kan tilldela en alternativ adress där din kontakt ibland får post och information, till exempel deras sommarbostäder. Du kan tilldela varje alternativ adress ett eller flera datumintervall som du har angett för kontakterna för att visa när adresserna gäller.

1. Öppna relevant kontaktkort.
2. Välj åtgärden **Alternativ adress** och välj sedan åtgärden **Kort**.

    Om du vill ange att den alternativa adressen gäller under en viss tidsperiod, kan du välja åtgärden **datumintervall** i stället.
3. På sidan **Kontakt alt. adress lista** anger du en alternativ adress och fyll i fälten på sidan **kontaktens alternativa adress**.

Upprepa stegen för varje alternativ adress du vill tilldela. För varje alternativ adress kan du ange ett eller flera datumintervall.

## <a name="to-assign-job-responsibilities-to-a-contact"></a>Så här tilldelar du kontakter arbetsansvar
Du kan lägga till information om arbetsansvar för kontaktpersoner för att ange vad kontaktpersonen ansvarar för i företaget, till exempel IT, ledning eller produktion. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

> [!NOTE]
> Detta är endast tillåtet för kontakter av typen **Person**.

Arbetsansvarkoden definierar typen eller kategorin för projektet, som t. ex. MARKNADSFÖRING eller KÖP. Du kan ha flera arbetsansvarkoder. Att definiera arbetsansvaret använder du sidan **Arbetsansvar**.

1. Öppna relevant kontaktkort.
2. Välj åtgärden **Person** och sedan **Arbetsansvar**. Sidan **Kontakt arbetsansvar** öppnas.
3. I fältet **Arbetsansvarskod**, markera det arbetsansvar du vill tilldela.

Upprepa stegen för varje arbetsansvar du vill tilldela. Arbetsansvar kan också tilldelas i kontaktlista på samma sätt.

Antalet arbetsansvar som du har tilldelat kontakter anges automatiskt i fältet **Antal arbetsansvar** i avsnittet **Segmentering** på sidan **Kontakt**.

När du har tilldelat arbetsansvar till kontakterna kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="to-assign-organizational-levels-to-a-contact"></a>För att tilldela befattningsnivåer till en kontakt
Du kan använda befattningsnivåer på kontakterna om du vill ange vilken befattningsnivå de har i företaget, t. ex. företagsledning. Du kan använda den här informationen, när du anger uppgifter om kontakterna.

> [!NOTE]
> Detta är endast tillåtet för kontakter av typen **Person**.

Befattningsnivåkoden anger typen eller kategorin av befattningsnivån, som t. ex. VD eller CFO. Du kan ha flera befattningsnivåkoder. För att definiera befattningsnivån använder du sidan **Befattningsnivåer**.

1. Öppna relevant kontaktkort.
2. I fältet **Befattningsnivåer** väljer du den kod som du vill tilldela.

När du har fördelat befattningsnivåer till kontakterna kan du använda informationen för att skapa segment.

När du har tilldelat arbetsansvar till kontakterna kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="to-assign-web-sources-to-a-contact"></a>För att tilldela webbadresser till en kontakt
Du kan använda webbadresser med dina kontaktföretag för att t. ex. identifiera sökmotorer och webbplatser på Internet som du vill använda för att söka efter information om kontakterna. När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

> [!NOTE]
> Detta är endast tillåtet för kontakter av typen **företag**.

När du tilldelar webbadresser anger du vilken sökmotor och vilket sökord som ska användas för att hitta önskad information.

1. Öppna relevant kontaktkort.
2. Välj åtgärden **företag** och sedan **webbadresser**. Sidan **Kontakt webbadresser** öppnas.
3. I fältet **webbadresskod**, välj webbadressen som du vill tilldela.
4. Skriv i fältet **Sökord** det sökord som ska användas för att hitta informationen.

Upprepa stegen för varje webbkälla du vill skapa.

## <a name="to-assign-business-relations-to-a-contact"></a> Så här tilldelar du affärsrelationer till kontakter
Affärsrelationer används för att visa vilket affärsförhållande du har till kontakterna, till exempel spekulant, bank, konsult eller serviceleverantör.

> [!NOTE]
> Detta är endast tillåtet för kontakter av typen **företag**.

1. Öppna relevant kontaktkort.
2. Välj åtgärden **företag** och sedan **affärsrelationer**.
3. På sidan **Kontaktens affärsrelationer** i fältet **affärsrelationskod**, markerar du den affärsrelation du vill tilldela.

Upprepa stegen för varje affärsrelation du vill tilldela.

Antalet affärsrelationer som du har tilldelat kontakter anges automatiskt i fältet **Antal affärsrelationer** på avsnittet **Segmentering** på **Kontakt**-sidan.

När du har tilldelat kontakterna affärsrelationer kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Automatisk kopiering av särskild information från kontaktföretag till kontaktpersoner
Vissa uppgifter om kontaktföretag är helt identiska med uppgifter om kontaktpersoner som arbetar i dessa företag, till exempel adresser. På snabbfliken **Arv** i fönstret **Marknadsföringsinställningar** kan du ange vilka fält på kontaktkortet för ett företag som kopieras till kontaktkortet för en person varje gång du skapar en kontaktperson för ett kontaktföretag.

När du ändrar i något av dessa fält på kontaktföretagskortet ändras motsvarande fält på kontaktpersonskortet (om du inte har ändrat fälten på detta manuellt).

Mer information finns i [Skapa kontakter](marketing-create-contact-companies.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Använd fördefinierade standardinställningar på nya kontakter
Du kan ange att särskild språkkod, distriktskod, säljarkod och lands-/regionkod automatiskt ska tilldelas av programmet som standard på varje ny kontakt som du skapar. Du kan också ange standardförsäljningscykelkod som automatiskt ska tilldelas varje ny affärsmöjlighet som du skapar. Du ställer in detta på snabbfliken **Standard** på sidan **Marknadsföringsinställning**

Värden i övertagna fält ersätter de standardvärden som du har angett. Om du exempelvis har angett engelska som standardspråk men företagets språk är tyska, tilldelas tyska automatiskt som språkkod för de kontaktpersoner som är registrerade på det företaget.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisera kontakter med kunder, leverantörer och bankkonton
För att synkronisera kontaktkort med länkade kund-, leverantörs- eller bankkontokort måste du fylla i motsvarande fält i avsnittet **Affärsrelationskod för** på snabbfliken **interaktioner** på sidan **Marknadsföringsinställning**.  

Mer information finns i [Så här synkroniserar du kontakter med kunder, leverantörer och bankkonton](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

## <a name="searching-for-duplicate-contacts"></a>Söka efter dubbelkontakter
Du kan välja automatisk sökning efter kopior varje gång du skapar en kontakt eller söka manuellt när du har skapat kontakter. Du kan också välja automatisk uppdatering av söksträngar varje gång du ändrar uppgifter om kontakter eller skapar kontakter. Du kan bestämma procentuell överensstämmelse för sökningar, det vill säga hur många procents överensstämmelse det måste vara mellan två kontakter för att de ska anses vara kopior. Du ställer in detta på snabbfliken **Dubbletter** på sidan **Marknadsföringsinställning**

När du har hittat dubbelkontakter kan du använda sidan **Koppla dubblett** för att koppla den till en befintlig kontaktpost som du vill behålla. Mer information finns i [Koplla dubblettposter](sales-how-merge-duplicate-records.md).

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Skapa kontakter](marketing-create-contact-companies.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
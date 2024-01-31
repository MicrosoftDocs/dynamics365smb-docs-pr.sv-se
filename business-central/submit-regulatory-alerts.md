---
title: Skicka regelnotifieringar
description: Du kan följa den här guiden om du vill skicka en andra varning till produktteamet om du vet om nya bestämmelser som kräver stöd för funktionen i Business Central.
author: sorenfriisalexandersen
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: null
ms.date: 12/07/2023
ms.author: soalex
ms.service: dynamics-365-business-central
---

# Skicka notifieringar om lands-/regionspecifika regleringsfunktioner

Vi inbjuder dig till att använda Microsoft Dynamics Lifecycle Services (LCS) för att skicka regelnotifieringar Dynamics tjänst för att skicka regelnotifieringar.  

## Att skicka regelnotifiering i LCS

1. Gå till [Lifecycle Services](https://lcs.dynamics.com) och logga in.  

    Du visas de projekt som du har tillgång till.

2. Välj projektet **regleringsnotifieringar – globalt**.

    Då öppnas projektet och en mängd olika saker som rör projektet visas.

3. Markera tjänsten **Notifieringstjänst** på höger sida under avsnittet **fler verktyg**.

    En lista över aviseringar visas med rubriken **Dynamics skicka regelnotifieringar**.

4. Du kan lägga till en ny avisering genom att klicka på plustecknet **(+)** längst upp i listan.

    Då visas en 4-stegs-guide där du kan skapa aviseringen. Guiden har följande steg:
    - Sök efter befintliga objekt.

        Sök efter all information som du tycker är relevant för notifieringen som du ska skapa. Om det inte finns några relevanta sökresultat kan du välja knappen **Skicka regelnotifiering** längst ned på sidan om du vill fortsätta med att skicka notifieringen.
    - Bifoga affärsprocesser.

        Denna del gäller inte för Dynamics 365 Business Central. Välj **hoppa över** för att gå vidare till nästa steg.
    - Beskriv notifieringen.

        Ange information om notifieringen i lämpligt fält. En röd asterisk (\*) i guiden anger de fält som krävs.

        |Fält        |Beskrivning                               |
        |-------------|------------------------------------------|
        |Rubrik  | Ange en beskrivande rubrik för att identifiera berört område. Till exempel anger du *Ändringar i dokument från och med 1 juli 2019*. |
        |Beskrivning  | Ange en kort översikt över lagstiftningen. Beskrivningen bör fokusera på frågor som är relevanta för resursplanering inom företag (ERP), så att användare kan förstå kraven på en hög nivå utan att behöva läsa lagstiftningen först.|
        |Land  | Ange landet/regionen som lagstiftningen gäller för.|
        |Bransch| Ange vilken bransch om kravet bara gäller för specifika branscher. Välj till exempel **Offentliga sektorn**, **Butik** eller **Produktion**.|
        |Funktionsreferens  | Detta gäller inte för Business Central, men du kan ange en referens till en funktion om du känner till den. Listan med funktioner för ett visst land/region finns i [lokaliseringsportal](/dynamics/s-e/) på webbplatsen CustomerSource. |
        |Datum för tillämpning av lagen  | Ange det datum då berörda kunder måste börja följa lagen.|
        |Datum när myndigheten tillkännagav meddelandet  | Ange det datum då myndigheten meddelade ändringen.|
        |Senaste arkiveringsdatum  | Välj deadline för den första överföringen av nya eller ändrade rapporten.|
        |Länka till lagstiftning  | Ange en eller flera länkar till offentliggjorda lagar, tolkningsriktlinjer, genomföranderiktlinjer eller annan användbar dokumentation som hjälper användare att förstå och implementera kraven.|
        |Företagsnamn  | Ange namnet på företaget för den person som skickar meddelandet.|
        |Kontaktnamn  | Ange namnet på den person som skickar meddelandet. |
        |E-postkontakt  | E-postadressen på den person som skickar meddelandet.|
        |Affärsprocess  | De affärsprocesser som du har valt via guiden **skicka notifiering**|
        |Kommentarer  | Ange eventuell ytterligare information som kan hjälpa användare att förstå och implementera kraven. Välj **Skicka** om du vill spara kommentarerna. Flera kommentarer kan läggas till och ska skickas separat. Kommentarer sparas i den ordning de har lagts till. |
        |Bilagor  | Välj knappen **överför** och bläddra för att välja en fil som ska läggas till som bilaga. När du har markerat filen överförs och visas den som en länkad fil. Du kan lägga till upp till tre filer med storleken 5 MB var. För att ta bort filer, välj **Ta bort** under rubriken på filen. Bilagor måste vara allmänt tillgängligt material. De får inte vara ägda eller kundspecifika/partnerspecifika.|

        Välj **skicka** för att spara och skicka meddelandet.

        Om du inte har all information som krävs, eller om du inte är redo att skicka meddelandet, kan du spara en delvis slutförd notifiering.

    - Inlämningsbekräftelse.

      När du har skickat meddelandet får du en bekräftelse på att meddelandet har skickats till Microsoft.

## Se även

[Lokal funktionalitet i [!INCLUDE[prod_long](includes/prod_long.md)]](about-localization.md)  
[Byta språk och plats](about-locale-language.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Välkommen till Business Central](welcome.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
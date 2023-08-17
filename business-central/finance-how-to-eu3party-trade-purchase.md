---
title: Tredje partens EU-inköpstransaktioner
description: I den här artikeln beskrivs hur du ställer in och använder tredjeparts EU-inköpstransaktioner.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
---

# <a name="eu-third-party-purchase-transactions"></a>Tredje partens EU-inköpstransaktioner

EU trepartshandel sker när du tar emot en inköpsfaktura från en kund som finns i ett land eller en region inom EU och produkterna skickas till ett annat land eller en annan region inom EU utan att passera landet. Transaktionsbeloppet kan identifieras och rapporteras separat i enlighet med de visa EU-länder/regioners momsrapportering och kraven för systemet för utbyte av mervärdesskattedata (VAT Information Exchange System, VIES). Med Microsoft Dynamics 365 Business Central kan inköpstransaktioner ställas in som EU trepartshandel. Bokförda EU trepartstransaktioner kan då filtreras i momsrapporter och exkluderas från beloppet i kolumnen **Försäljning till kund** i rapporten **Moms- och kvartalsredovisning**.

Även om funktionen är förinstallerad som ett tillägg aktiveras den inte som standard. Följ dessa steg för att aktivera funktionen.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du arbetsyta **Funktionshantering** och väljer sedan relaterad länk.
2. Hitta och välj i listan **Funktionsuppdatering: Ersätt den befintliga funktionen för inköp via EU trepartshandel med det nya tillägget för inköp via EU trepartshandel**.
3. I kolumnen **Aktivera för** väljer du **Alla användare**.

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Aktivera EU-handelsfunktioner från tredjepartsleverantörer för ett inköp

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsinställningar** och väljer sedan relaterad länk.
2. På sidan **momsinställningar**, markera fältet **Aktivera EU 3-partens inköp**.

## <a name="use-eu-third-party-trade-functionality"></a>Använd funktionen EU trepartshandel

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Inköpsfaktura** (eller ett annat inköpsdokument) och välj sedan den relaterade länken.
2. Välj en befintlig inköpsfakturan eller välj **Nytt** för att skapa en ny.
3. I snabbfliken **Fakturadetaljer** markerar du kryssrutan **Treparts EU-handel**.
4. Välj **OK**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Inkludera eller exkludera transaktioner för EU trepartshandel i momsrapporten

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **momsrapport** och väljer sedan relaterad länk.
2. På sidan **momsrapport** väljer du ett av följande alternativ för att visa transaktioner för EU trepartshandel i med fältet **Filter för EU trepartshandel**.

    | Alternativ | Description |
    |--------|-------------|
    | Alla | Visa alla poster, oavsett om fältet **EU trepartshandel** i dokument var markerat. |
    | EU3 | Visa endast poster där fältet **EU trepartshandel** i dokument var markerat. |
    | Ej EU3 | Visa endast poster där fältet **EU trepartshandel** i dokument inte var markerat. |


## <a name="see-also"></a>Se även
[Ekonomihantering](finance.md)  
[Arbeta med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

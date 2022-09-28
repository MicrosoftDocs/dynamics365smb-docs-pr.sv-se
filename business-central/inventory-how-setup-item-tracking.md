---
title: Ställa in artikelspårning med serie-, parti- eller paketnummer
description: Ställa in artikelspårning med serie-, parti- eller paketnummer
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/31/2021
ms.author: edupont
ms.openlocfilehash: c298903d62da4cfd346a46ff1978ab91644fb13f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533274"
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Ställa in artikelspårning med serie-, parti- eller paketnummer

Håll reda på lagerartiklar även i komplexa lagerkonfigurationer med tal som är specifika för varje artikel, antingen som ett enskilt objekt, som ett parti eller som ett paket. Med artikelspårning kan du spåra artiklar över interna lagerrörelser och utgående och inkommande dokument.

Artiklar med serienr och partinr som kan spåras, antingen framåt eller bakåt i en försörjningskedja. Detta är användbart för allmän kvalitetssäkring och återkallade produkter. Mer information finns i [Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> I utgivningscykel 1 för 2021 och senare, slå på funktionsuppdateringen på *Använd spårning på paketnummer i boknings- och spårningssystemet* om du vill arbeta med paketnummer samt serienummer och partinummer. Mer information finns i [Aktivera kommande funktioner i förväg](admin-feature-management.md). När funktionen är påslagen kan du tilldela paketnummer till utgående och inkommande dokument som liknar hur du kan arbeta med partinummer.  

## <a name="numbers-and-item-tracking"></a>Nummer och artikelspårning

Som en del av dina lagerprocesser kan du bunta ditt lager i paket, lådor, behållare och så vidare. Men för att hålla reda på artiklarna tilldelar du unika nummer som identifiering. Du tillverkar och säljer till exempel en stol som har artikelnummer *1900-S*. Varje enskild stol har ett serienummer *1001*, men du lägger också ihop fyra stolar i *LOT0001* och du levererar stolar i en behållare med paketnummer *CONTAINER010* som också innehåller andra föremål, till exempel *LOT0100* med sidobord och *LOT200* med lampor.  

Beroende på din konfiguration använder du dessa olika nummer för att hålla reda på lagret [!INCLUDE [prod_short](includes/prod_short.md)] i de olika stadierna av inköp, försäljning, lageroperationer och så vidare.

## <a name="to-set-up-item-tracking-codes"></a>Så här skapar du en artikelspårningskoder

Artikelspårningskoden reflekterar ett företags olika regler i samband med användningen av serie- och partinummer för artiklar som flyttas i lagret.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelspårningskoder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. På **serienr.**, **partinr.** och **paketnr.** definieras principer för artikelspårning efter serie-, parti- och paketnummer.  

> [!NOTE]  
> Om du vill spåra specifika artiklar eller specifika partier under hela sin livstid, måste du välja fälten **SN specifik spårning** och **Parti specifik spårning** respektive. Därför när du arbetar med en utgående enhet av en artikel till den här artikelspårningskoden måste du alltid ange vilket befintligt serienummer eller vilket befintligt partinummer som ska hanteras. Detta innebär att när en enhet av artikeln säljs, måste den kopplas till en specifik grupp med serienummer i lagret eller ett specifikt partinummer i lagret. Det serienummer eller partinummer som är kopplat till artikeln vid införseln i lagret måste således vara oförändrat för artikeltypen vid utförseln ur lagret.

Eftersom det här inställningsfältet omfattar alla möjliga transaktioner med artikeln, markeras även de enskilda fälten för inkommande/utgående. Dessa individuella fält för inkommande/utgående har emellertid inget att göra med kopplingar i lagret, utan definierar bara företagets arbetsflöde i fråga om när artikelspårningsnummer ska kopplas.  

> [!NOTE]  
>  För att tilldela artikelspårningsnummer i distributionslageraktiviteter måste fälten **SN dist.lager spårning** och **Parti dist.lager spårning.** markeras på artikelns kort för artikelspårningskoden.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Så här skapar du utgångsregler för serie-/partinummer

För vissa artiklar kanske du vill definiera särskilda förfallodatum och -regler i artikelspårningskoden. På så sätt kan du hålla reda på när olika serie-/partinummer går ut.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelspårningskoder** och väljer sedan relaterad länk.
2. Välj en befintlig artikelspårningskod och välj sedan åtgärden **redigera**.  
3. Markera följande fält på snabbfliken **Div.**.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Endast utgångsbokföring**|Anger att ett förfallodatum som tilldelades artikelspårningsnumret när artikeln fördes in i lagret måste respekteras vid lagerdisposition.|  
    |**Kräv inmatning av utgångsdatum**|Anger att du manuellt måste ange ett förfallodatum på artikelspårningsraden.|  
    |**Använd utgångsdatum**|Anger att du vill beräkna utgångsdatum. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Så här skapar du garantier för serie-/partinummer

För vissa artiklar kanske du vill definiera specifika garantier i artikelspårningskoden. På så sätt kan du hålla reda på när garantierna för särskilda serie- eller partinummer i lagret går ut.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelspårningskoder** och väljer sedan relaterad länk.  
2. Välj en befintlig artikelspårningskod och välj sedan åtgärden **redigera**.  
3. Fyll i fältet **Garanti datumformel** och markera fälten på snabbfliken **Div.**:  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Garanti datumformel**|Anger garantins sista dag för artikeln.|  
    |**Kräv inmatning av garantidatum**|Anger att du manuellt måste ange ett garantidatum på artikelspårningsraden.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Så här ställer du in artiklar för spårning med rätt artikelspårningskoder

Om du vill aktivera artikelspårning måste du först tilldela artikelspårningskoder till en artikel. Det finns två sätt att lägga till artikelspårningskoder, genom att välja koden från en fördefinierad lista eller genom att tilldela en ny unik kod. Placera markören över fälten om du vill läsa en kort beskrivning.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikel** och väljer sedan relaterad länk.
2. Markera en befintlig artikel i listan och öppna sidan **Artikelkort**.  
3. På snabbfliken **Artikelspårning** tilldelar du lämpliga artikelspårningskoder och väljer **Artikelspårningskod**, **Serienr** och **Partinr**.
    1. Alternativt kan du också skapa en ny artikelspårningskod genom att välja åtgärden **Ny**.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/prepare-item-tracking/)

## <a name="see-also"></a>Se även

[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

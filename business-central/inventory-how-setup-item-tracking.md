---
title: 'Konfigurera artikelspårning med serie-, parti- eller paketnummer'
description: 'Ställa in artikelspårning med serie-, parti- eller paketnummer'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Konfigurera artikelspårning med serie-, parti- eller paketnummer

Håll reda på lagerartiklar även i komplexa lagerkonfigurationer med tal som är specifika för varje artikel, antingen som ett enskilt objekt, som ett parti eller som ett paket. Med artikelspårning kan du spåra artiklar över interna lagerrörelser och utgående och inkommande dokument.

Artiklar med serienr och partinr som kan spåras, antingen framåt eller bakåt i en försörjningskedja. Detta är användbart för allmän kvalitetssäkring och återkallade produkter. Mer information finns i [Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md).  

## <a name="numbers-and-item-tracking"></a>Nummer och artikelspårning

Som en del av dina lagerprocesser kan du bunta ditt lager i paket, lådor, behållare och så vidare. Men för att hålla reda på artiklarna tilldelar du unika nummer som identifiering. Du tillverkar och säljer till exempel en stol som har artikelnummer *1900-S*. Varje enskild stol har ett serienummer *1001*, men du lägger också ihop fyra stolar i *LOT0001* och du levererar stolar i en behållare med paketnummer *CONTAINER010* som också innehåller andra föremål, till exempel *LOT0100* med sidobord och *LOT200* med lampor.  

Beroende på din konfiguration använder du dessa olika nummer för att hålla reda på lagret [!INCLUDE [prod_short](includes/prod_short.md)] i de olika stadierna av inköp, försäljning, lageroperationer och så vidare.

## <a name="to-set-up-item-tracking-codes"></a>Så här skapar du en artikelspårningskoder

Artikelspårningskoden reflekterar ett företags olika regler i samband med användningen av serie- och partinummer för artiklar som flyttas i lagret.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelspårningskoder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. På snabbflikarna **Serienr**, **Partinr** **och Paketspårning** definierar du principer för artikelspårning efter serienummer, partinummer respektive kollinummer.  

> [!NOTE]  
> Om du vill spåra specifika artiklar eller specifika partier under hela sin livstid, måste du välja fälten **SN specifik spårning**, **Parti specifik spårning** och **Parti specifik spårning** respektive. Därför när du arbetar med en utgående enhet av en artikel till den här artikelspårningskoden måste du alltid ange vilket befintligt serienummer eller vilket befintligt partinummer som ska hanteras. Detta innebär att när en enhet av artikeln säljs, måste den kopplas till en specifik grupp med serienummer i lagret eller ett specifikt partinummer i lagret. Eller med andra ord, ett serie-, parti- eller paketnummer är kopplat till artikeln vid införseln i lagret måste således vara oförändrat för artikeltypen vid utförseln ur lagret.

Eftersom dessa inställningsfält täcker alla möjliga transaktioner med artikeln, väljs de individuella inkommande/utgående fälten. De enskilda ankommande/utgående fälten har emellertid inget att göra med program i lagret. De definierar bara ditt företags arbetsflöde när artikelspårningsnummer tilldelas.  

> [!NOTE]  
> För att tilldela artikelspårningsnummer i distributionslageraktiviteter måste fälten **SN dist.lager spårning** och **Parti dist.lager spårning.** markeras på artikelns kort för artikelspårningskoden.  

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

Om du vill aktivera artikelspårning måste du först tilldela artikelspårningskoderna till en artikel. Det finns två sätt att lägga till artikelspårningskoder, genom att välja koden från en fördefinierad lista eller genom att tilldela en ny unik kod. Placera markören över fälten om du vill läsa en kort beskrivning.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikel** och väljer sedan relaterad länk.
2. Markera en befintlig artikel i listan och öppna sidan **Artikelkort**.  
3. På snabbfliken **Artikelspårning** tilldelar du lämpliga artikelspårningskoder och väljer **Artikelspårningskod**, **Serienr** och **Partinr**.
    1. Alternativt kan du också skapa en ny artikelspårningskod genom att välja åtgärden **Ny**.

## <a name="to-specify-opening-balances-for-the-items-you-track"></a>Om du vill ange ingående balanser för artiklarna spårar du

Du kan skapa ingående saldo för de artiklar som du spårar. Eftersom du kan välja olika inställningar för distributionslager finns det två alternativ:

* Aktivera specifika journaler på sidan **Artikeljournal** för att låta användarna ange serie-, parti- och paketdata direkt på journalraderna.
* För platser där växlingsknappen **Dirigerad art.inf. och plock.** aktiveras, använd sidan **Inventeringslista för distributionslager** för att göra alla artikelspårningsfält tillgängliga. Fälten som är tillgängliga inkluderar fälten **garantidatum** och **utgångsdatum**.

### <a name="item-journals"></a>Artikeljournaler

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikeljournaler** och väljer sedan relaterad länk.
2. Välj fälten **Namn** för att öppna en lista med redovisningsjournaler.
3. Välj **Ny** för att skapa en ny batch och slå sedan på **Artikelspårning på rader**.
4. Välj **OK** för att välja den batch du skapat.
5. Fyll i fälten på artikeljournalraden vid behov. Lägg märke till att fälten **Partinr.**, **Serienr.**, **Utgångsdatum**, **Garantidatum** och **Paketnr.** Fält är tillgängliga (om funktionen är aktiverad).
6. Välj åtgärden **Bokför** för att justera lagret.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] visar ett fåtal mindre verifieringssätt när du skriver eller importerar data. En mer omfattande kontroll sker när du bokför eller överför data från Journal rader till sidan **fönstret Artikelspårning**. Det senare sker automatiskt när du öppnar sidan **Artikelspårning** från artikeljournalraden eller om du väljer åtgärden **Uppdatera artikelspårningsrader**.

### <a name="warehouse-physical-inventory-journal-for-locations-where-directed-pick-and-put-away-is-turned-on"></a>Lagerjournal för fysisk inventering för platser där riktad plockning och borttagning är aktiverad

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inventeringslista för distributionslager** och väljer sedan relaterad länk.
2. Fyll i fälten på artikeljournalraden vid behov. Lägg märke till att fälten **Partinr.**, **Serienr.**, **Utgångsdatum**, **Garantidatum** och **Paketnr.** Fält är tillgängliga (om funktionen är aktiverad).
3. Välj åtgärden **Registrera** för att justera lagret. Kom ihåg att du måste synkronisera justerade lagertransaktioner med tillhörande artikeltransaktioner Om du vill ha mer information går du till [synkronisera de justerade lagertransaktionerna](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

För massimportera använder du konfigurationspaket för att importera data till journalerna.

> [!NOTE]
> Du kan inte använda **Redigera i Excel** för att skapa journalrader med uppföljningsinformation.

## <a name="see-also"></a>Se även

[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

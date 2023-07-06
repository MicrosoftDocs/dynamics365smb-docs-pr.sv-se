---
title: Ställ in och använd tjänstdeklarationstillägget
description: Lär dig hur du ställer in och använder funktioner för tjänstdeklaration (Intrastat för tjänster) för att rapportera tjänstehandel med företag i andra EU-länder.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# <a name="the-service-declaration-extension"></a><a name="the-service-declaration-extension"></a><a name="the-service-declaration-extension"></a>Tjänstdeklarationstillägget

I vissa EU-länder kräver myndigheterna att företagen rapporterar exporten av tjänster till andra EU-länder. Med **tjänst deklaration** tillägget kan du samla in information om tjänsthandeln i EU och rapportera den till myndigheterna. Även om den har namnet **tjänstdeklaration** kan du även använda den som **Intrastat för tjänst**. Det här tillägget är tillgängligt för alla EU-länder som en W1-version, och det kan användas som det är i Belgien. För andra länder krävs en tilldelad landsökning. Om ett land behöver ett annat format kan du använda rapport konfigurationen i **Ramverk för dataintegration** för att ändra formatet.

## <a name="enable-the-service-declaration-extension"></a><a name="enable-the-service-declaration-extension"></a><a name="enable-the-service-declaration-extension"></a>Aktivera tjänstdeklarationstillägget

När du har installerat tillägget i din miljö måste du aktivera det.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Funktionshantering** och väljer sedan relaterad länk.
2. Sök **funktion: Aktivera användning av tjänstdeklaration (Intrastat för tjänster)** och i fältet **Aktiverad för** välj **Alla användare**. Lär dig mer om funktionshantering på [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrationsinnehållet.
3. När du aktiverar funktionen bör du följa stegen i installationsprocessen i installationsguiden. De flesta fält är konfigurerade som standard.
4. Lägg endast **Typer av tjänstetransaktioner** i det andra steget genom att välja alternativet **Öppna sidan för tjänstetransaktionstyper för att ange listan med koder**.
5. Innan du börjar bör du kontrollera **totala antalet koder** för att förstå hur många tjänsttransaktionstyper som redan har angetts.
6. Slutför konfigurationen genom att klicka **Slutför** i det sista steget.

## <a name="set-up-the-service-declaration-extension"></a><a name="set-up-the-service-declaration-extension"></a><a name="set-up-the-service-declaration-extension"></a>Ställ in tjänstdeklarationstillägget

Du kan ställa in tillägget manuellt, eller genom att använda en rapporteringsfil i datautbytesdefinition.

### <a name="to-set-up-service-declaration-manually"></a><a name="to-set-up-service-declaration-manually"></a><a name="to-set-up-service-declaration-manually"></a>Ställ in tjänstedeklarationen manuellt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Konfigurera tjänstdeklaration** och väljer sedan relaterad länk.
2. Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**:

    |Fält  |Description  |
    |---------|---------|
    |**Nummerserie för deklaration**     | Anger den nummerserie som ska användas för att tilldela nya poster ID.        |
    |**Rapportera artikelomkostnader**  | Anger om artikelomkostnader måste rapporteras. När den är aktiverad kontrollerar [!INCLUDE [prod_short](includes/prod_short.md)] tjänsttransaktionskoden för artikelomkostnader och inkluderar dem i tjänstdeklarationer.        |
    |**Försäljningskundnr/faktureringskundnr**     | Anger vilken kund som ska användas för att jämföra landskoden med landskoden på sidan **företagsinformation**. Endast dokument där dessa två koder är olika kommer att tas med i tjänstdeklarationen.<br><br>* **Fakturera till.**: Använd landskoden från **Fakturera till kund** <br<br>* **Sälja till.**: Använd landskoden från **Sälja till kund**.        |
    |**Inköpsleverantörsnr/betalningsleverantörsnr**  | Anger vilken leverantör som ska användas för att jämföra landskoden med landskoden på sidan **företagsinformation**. Endast dokument där dessa två koder är olika kommer att tas med i tjänstdeklarationen.<br><br> * **Köpa från.**: Använd landskoden från **Köpa från leverantören**. <br><br> * **Betala till.**: Använd landskoden från **Betala till leverantör**.         |
    |**Def.kod för datautbyte**  | Anger koden för datautbytesdefinitionen som används för att generera den exporterade filen för tjänstedeklarationen.        |
    |**Aktivera momsregistreringsnummer**     |  Anger om **momsregistreringsnumret** har aktiverats för tjänstedeklarationen.       |

3. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Typer av tjänstetransaktioner** och väljer sedan relaterad länk.
4. På raderna ange **Koder** och **beskrivningar** för de typer av tjänstetransaktioner du vill använda på raderna.

### <a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a>Konfigurera en rapporteringsfil

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Datautbytesdefinition** och välj relaterad länk.
2. Välj åtgärden **Ny**.
3. På snabbfliken **Allmänt** beskriver du datautbytesdefinitionen, datafiltypen, kolumnavgränsaren, relaterade codeunits, XMLport och andra fält genom att fylla i fälten.
4. På snabbfliken **Raddefinitioner** beskriver du formateringen för raderna i datafilen genom att fylla i fälten baserat på fältet **Radtyp** och där du behöver definiera antalet kolumner för den här raden.
5. På snabbfliken **Kolumndefinitioner** fyller du i raden för varje planerad kolumn.
6. Välj åtgärden **Fältmappning** på snabbfliken **Raddefinitioner** för att öppna sidan **Fältmappning**.
7. Skapa den nya transaktionen och på snabbfliken **Allmänt** väljer du **tabell-ID** (för **Rad för tjänstedeklaration**, välj **5024**) och fyll i fält:
   1. I fältet **nyckelindex**, ange nyckelindexet att sortera källposterna efter innan du exporterar.
   2. Välj **mappnings-codeunit**.
8. På snabbfliken **Fältmappning** lägger du till kolumner som du tidigare konfigurerat i snabbfliken **Kolumndefinitioner** och lägger sedan till följande:
   1. Ange **fält-ID** för varje kolumn.
   2. Ange **omvandlingsregeln** för varje kolumn som du behöver den för. Ange regeln för att omvandla importerad text till ett värde som stöds innan det kan mappas till det angivna fältet [!INCLUDE[prod_short](includes/prod_short.md)]. När du väljer ett värde i det här fältet anges det exakta värdet i fältet **Omvandlingsregel** i **Mappningsbuff. för datautbytesfält** och vice versa.
9. Om du vill gruppera transaktioner baserat på vissa kolumner väljer du de fält som du vill använda för gruppering på snabbfliken **Fältgruppering**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] levereras med den förinställda datautbytesdefinitionen för **Tjänstedeklarationsnr** för alla lokaliserade länder. Läs mer om att skapa en ny datautbytesdefinition i [Ställa in datautbytesdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

## <a name="other-related-configurations"></a><a name="other-related-configurations"></a><a name="other-related-configurations"></a>Andra relaterade konfigurationer

Innan du använder tjänstdeklarationstillägget konfigurerar du vissa fält för artiklar, resurser och artikelomkostnader.

### <a name="items"></a><a name="items"></a><a name="items"></a>Artiklar

Ställ in information om tjänstdeklaration på artikelkortsidor:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Markera det objekt som du vill konfigurera.
3. Expandera snabbfliken **Artikel** och konfigurera följande fält:
   1. I fältet **Typ** väljer du **Tjänst**.
   2. I fältet **Kod för typ av tjänstetransaktion** ange koden för **Typ av tjänstetransaktion**.
   3. Om du inte vill ta med service artikeln i tjänstdeklarationer väljer du fältet **Undanta från tjänstedeklaration**.

### <a name="resources"></a><a name="resources"></a><a name="resources"></a>Resurser

Ställ in information om tjänstdeklaration på resurskortsidor:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.
2. Markera den resurs som du vill konfigurera.
3. Expandera snabbfliken **Allmänt** och konfigurera följande fält:
   1. I fältet **Kod för typ av tjänstetransaktion** ange koden för **Typ av tjänstetransaktion**.
   2. Om du inte vill ta med resursen i tjänstdeklarationer väljer du fältet **Undanta från tjänstedeklaration**.

### <a name="item-charges"></a><a name="item-charges"></a><a name="item-charges"></a>Artikelkostnader

Ställ in information om tjänstdeklaration för artikelomkostnad:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **artikelomkostnader** och väljer sedan relaterad länk.
2. Markera den artikelomkostnad som du vill konfigurera.
3. I fältet **Kod för typ av tjänstetransaktion** ange koden för **Typ av tjänstetransaktion**.
4. Om du inte vill ta med artikelomkostnad i tjänstdeklarationer väljer du fältet **Undanta från tjänstedeklaration**.

## <a name="create-new-service-declaration"></a><a name="create-new-service-declaration"></a><a name="create-new-service-declaration"></a>Skapa en ny tjänstdeklaration

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tjänstdeklaration** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På snabbfliken **Allmänt** fyller du i fälten:
    1. I fältet **Konfigurationskod** anger du konfigurations koden som används för att föreslå rader och skapa filer. Du måste välja en som **tjänstdeklaration**.
    2. I fältet **Startdatum** och **Slutdatum** anger du start- och slutdatum för den period som ska tas med i tjänstdeklarationen.
4. Välj **Föreslå rader** för att starta ett batchjobb som samlar in rader från dokument och fyller i tjänstdeklarationsraderna.

När du kör batch-jobbet hämtas alla transaktioner från relevanta inköps- och försäljningsdokument under den period som krävs och läggs till på tjänstdeklarationsraderna. Placera markören över fälten i rader om du vill läsa en kort beskrivning.

## <a name="modify-a-service-declaration"></a><a name="modify-a-service-declaration"></a><a name="modify-a-service-declaration"></a>Ändra en tjänstedeklaration

Om det behövs kan du ändra raderna eller lägga till nya.

1. På sidan **Tjänstdeklaration** väljer du åtgärden **Ny rad** i snabbfliken **Rader**.
2. I fältet **dokumenttyp** välj det alternativ som är relaterat till det dokument du vill använda.
3. Baserat på **Dokumenttyp**, fyll i fältet **Dokumentnr.**.
4. Fyll i resterande fält.

## <a name="overview-the-service-declaration-lines"></a><a name="overview-the-service-declaration-lines"></a><a name="overview-the-service-declaration-lines"></a>Översikt över tjänstedeklarationrader

När du har skapat en tjänstdeklaration använder du åtgärd **översikt** för att få en överblick över tjänstdeklarationsraderna. Du kan gruppera och sammanfatta raderna på samma sätt som den exporterade filen. Du kan också öppna raderna i Excel.

## <a name="report-service-declaration-in-a-file"></a><a name="report-service-declaration-in-a-file"></a><a name="report-service-declaration-in-a-file"></a>Rapportera tjänstdeklaration i en fil

Du kan skicka tjänstdeklaration som en fil baserad på olika lokala myndigheters behov. Så här skapar du en fil:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **tjänstdeklaration** och väljer sedan relaterad länk.
2. Välj den tjänstdeklaration som du vill rapportera som en fil.
3. Om du inte redan har gjort det fyll i tjänstdeklaration manuellt eller genom att välja åtgärden **Föreslå rader**.
4. Välj åtgärden **Skapa fil**.
5. Tjänstdeklaration-filen sparas i det format som krävs.

## <a name="other-considerations"></a><a name="other-considerations"></a><a name="other-considerations"></a>Övrigt att tänka på

När du använder **tjänstdeklaration** tillägget finns det några saker du bör tänka på. Det är till exempel viktigt att grupperna överensstämmer med kraven från utfärdare. Det är också viktigt att tjänst tas med på rätt sätt på försäljnings- och inköpsdokument.

### <a name="grouping-lines"></a><a name="grouping-lines"></a><a name="grouping-lines"></a>Gruppera rader

På tjänstdeklarationsrader finns det ingen gruppering utifrån något fält. Alla transaktioner kopieras från original dokumentet som en källa.

Gruppering som krävs av myndigheterna kommer att lämnas i den exporterade filen. Du måste konfigurera grupper i **Datautbytesdefinitionen** som är helt konfigurerbar. Läs mer i [Så här skapar du datautbytesdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="using-services-in-document-lines"></a><a name="using-services-in-document-lines"></a><a name="using-services-in-document-lines"></a>Använda tjänster på dokumentrader

När du skapar en inköps-, försäljnings- eller servicefaktura hittar du två fält som är relaterade till tjänstdeklarationer på deras rader. Båda fälten fylls i automatiskt med standardvärdena från artikel-, resurs- eller artikel omkostnaden som ställts in.

- **Kod för typ av tjänstetransaktion** – ange koden för typ av tjänstetransaktion.
- **Tillämplig för tjänstedeklaration** – Anger om en artikel eller resurs är tillämplig för en tjänstedeklaration.

Du kan ändra värdena i dessa fält, men om du väljer fältet **Tillämplig för tjänstedeklaration** måste du ange ett värde **Kod för typ av tjänstetransaktion**. Om du inte gör det kan du inte bokföra dokumentet.

Om du anger ett värde i fältet **Kod för typ av tjänstetransaktion** men inte väljer **Gäller för tjänstdeklaration** kan du bokföra dokumentet men raden kommer inte att beräknas när du gör det.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Ställ in Intrastat-rapportering](finance-how-setup-report-intrastat.md)
[Intrastat-rapport i Business Central](finance-how-report-intrastat.md)  
[Ekonomihantering](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

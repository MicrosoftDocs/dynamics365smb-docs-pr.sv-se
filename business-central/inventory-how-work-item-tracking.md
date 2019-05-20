---
title: Tilldela serienummer och partinummer till artiklar för spårning | Microsoft Docs
description: Du kan lägga till serie- och partinummer till alla avgående och ankommande dokument och visa de bokförda artikelspårningstransaktionerna i de associerade artikeltransaktionerna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c7a5aa7d768a4fe2fae111b04ffc1fdab65d07dc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240378"
---
# <a name="work-with-serial-and-lot-numbers"></a>Arbeta med serienummer och partinummer
Du kan tilldela serie- och partinummer till alla avgående och ankommande dokument och visa de bokförda artikelspårningstransaktionerna i de associerade artikeltransaktionerna. Du utför arbetet på sidan **Artikelspårningsrader** som du öppnar från ett inkommande eller utgående dokument.

I matrisen med antalsfält längst upp på fönstret **Artikelspårningsrader** visas antalen och summorna för artikelspårningsnummer som anges på raderna i fönstret. Antalen måste stämma överens med antalen på dokumentraden, som anges med 0 i fälten **Odefinierad**.

För att ge bättre prestanda samlas tillgänglighetsinformationen på sidan **Artikelspårningsrader** endast en gång när du öppnar sidan. Detta innebär att informationen om tillgänglighet inte uppdateras under tiden som sidan är öppen, även om ändringar sker i lagret eller i andra dokument.

Artiklar med serienr eller partinr som kan spåras, antingen framåt eller bakåt i en försörjningskedja. Detta är användbart för allmän kvalitetssäkring och återkallade produkter. Mer information finns i [Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Så här plockar du specifika serie-/partinummer i distributionslagret
Avgående hantering av serie- eller partinummer är en vanlig uppgift i olika lagerprocesser.  

I vissa processer har inte lagerartiklarna serie- eller partinummer och lagerarbetaren måste tilldela nya under den avgående hantering, vanligtvis från en fördefinierade nummerserier.

I enkla processer har lagerartiklarna redan serie- eller partinummer, t.ex. tilldelade under införsel, och dessa nummer överförs automatiskt via alla avgående lageraktiviteter utan interaktioner av lagerarbetare.

I vissa situationer i lager med serie - eller partinummer definieras specifika serie- eller partinummer i källdokumentet, till exempel försäljningsorder, som lagerarbetaren måste respektera under den avgående lagerhanteringen. Det kan bero på att kunden valde ett visst parti under orderprocessen. När lagerplockningen eller dokumentet för dist.lager plockning skapas från ett utgående källdokument där serie- eller partinummer redan är definierade, är alla fält på sidan **Artikelspårningsrader** under lagerplockningen skrivskyddade, utom fältet **Ant. att hantera**. I detta fall anger lagerplockningsraderna artikelspårningsnumren på enskilda ta- och placerarader. Kvantiteten är redan uppdelad på unika kombinationer av serienummer eller partinummer eftersom de artikelspårningsnummer som ska levereras är specificerade på försäljningsordern.  

## <a name="item-tracking-availability"></a>Disposition av artikelspårning
När du arbetar med parti- eller serienummer beräknar [!INCLUDE[d365fin](includes/d365fin_md.md)] dispositionsinformationen för parti- och serienumren på de olika artikelspårningssidorna. På så sätt kan du visa hur mycket av ett parti- eller serienummer som för närvarande används i andra dokument. Det minskar fel och osäkerhet som orsakas av dubbla fördelningar.

På sidan **Artikelspårningsrader** visas en varningsikon i fälten **Disposition, partinr** eller **Disposition, serienr** om en del av eller hela antalet som har valts redan används i andra dokument eller om parti- eller serienumret inte är disponibelt.

På sidorna **partinummer-/serienummerlista**, **partinummer-/serienummerdisposition** och **Artikelspårning - Markera transaktioner** finns information om hur stor del av en artikels antal som utnyttjas. Följande information inkluderas.

|Fält|Description|
|-----|-----------|  
|**Totalt antal**|Det totala antalet artiklar som för närvarande finns i lager.|
|**Totalt begärt antal**|Det totala antalet artiklar som har begärts i det här dokumentet och i andra dokument.|
|**Aktuellt pågående antal**|Antalet artiklar som har begärts i det aktuella dokumentet, men som ännu inte har allokerats till databasen.|
|**Aktuellt begärt antal**|Antalet artiklar som har begärts i det aktuella dokumentet.|
|**Totalt disponibelt antal**|Det totala antalet artiklar i lager, minus artikelantalet som har begärts i det här dokumentet och i andra dokument (totalt begärt antal) och minus antalet som har begärts, men ännu inte allokerats, i det här dokumentet (aktuellt pågående antal).|

Om du arbetar på sidan **Artikelspårningsrader** under en lång tidsperiod eller om det pågår mycket aktivitet för den artikel som du arbetar med kan du välja åtgärden **Uppdatera tillgänglighet**. Dispositionen för artikeln kontrolleras automatiskt på nytt när sidan stängs, så att eventuella dispositionsproblem kan upptäckas.

## <a name="to-set-up-item-tracking-codes"></a>Så här skapar du en artikelspårningskoder
Artikelspårningskoden reflekterar ett företags olika regler i samband med användningen av serie- och partinummer för artiklar som flyttas i lagret.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelspårningskoder** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. På snabbflikarna **Serienr** och **Partinr** definieras principer för artikelspårning efter serie- respektive partinummer.  

> [!NOTE]  
>  Om du vill spåra specifika artiklar eller specifika partier under hela sin livstid, måste du välja fälten **SN specifik spårning** och **Parti specifik spårning** respektive. Därför när du arbetar med en avgående enhet av en artikel till den här artikelspårningskoden måste du alltid ange vilket befintligt serienummer eller vilket befintligt partinummer som ska hanteras. Detta innebär att när en enhet av artikeln säljs, måste den kopplas till en specifik grupp med serienummer i lagret eller ett specifikt partinummer i lagret. Det serienummer eller partinummer som är kopplat till artikeln vid införseln i lagret måste således vara oförändrat för artikeltypen vid utförseln ur lagret.

Eftersom det här inställningsfältet omfattar alla möjliga transaktioner med artikeln, markeras även de enskilda fälten för ankommande/avgående. Dessa individuella fält för ankommande/avgående har emellertid inget att göra med kopplingar i lagret, utan definierar bara företagets arbetsflöde i fråga om när artikelspårningsnummer ska kopplas.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Så här skapar du utgångsregler för serie-/partinummer  
För vissa artiklar kanske du vill definiera särskilda förfallodatum och -regler i artikelspårningskoden. På så sätt kan du hålla reda på när olika serie-/partinummer går ut.

1. Välj en befintlig artikelspårningskod och välj sedan åtgärden **redigera**.  
2.  Markera följande kryssrutor på snabbfliken **Div.**.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Endast utgångsbokföring**|Anger att ett förfallodatum som tilldelades artikelspårningsnumret när artikeln fördes in i lagret måste respekteras vid lagerdisposition.|  
    |**Utgångsdatum ska anges**|Anger att du manuellt måste ange ett förfallodatum på artikelspårningsraden.|  
    |**Ignorera utgångsdatum**|Anger att du inte vill beräkna slutdatum. |  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Så här skapar du garantier för serie-/partinummer  
För vissa artiklar kanske du vill definiera specifika garantier i artikelspårningskoden. På så sätt kan du hålla reda på när garantierna för särskilda serie- eller partinummer i lagret går ut.        
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelspårningskoder** och välj sedan relaterad länk.  

1. Välj en befintlig artikelspårningskod och välj sedan åtgärden **redigera**.  
2.  Fyll i fältet **Garanti datumformel** och markera kryssrutorna på snabbfliken **Diverse** .  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Garanti datumformel**|Anger garantins sista dag för artikeln.|  
    |**Garantidatum ska anges.**|Anger att du manuellt måste ange ett garantidatum på artikelspårningsraden.|  

## <a name="to-record-serial-or-lot-number-information"></a>Så här registrerar du information om serie- eller partinummer  
Om du behöver koppla särskild information till ett visst artikelspårningsnummer, till exempel för kvalitetssäkring, kan du göra det på ett informationskort för serienummer eller partinummer.

1. Öppna ett dokument som har serie-/partinummer tilldelas.
2. Öppna sidan **Artikelspårningsrader** för dokumentet.
3. Välj till exempel åtgärden **serienr. informationskort**.  

    Fälten **Serienr** och **Partinr** fylls i på förhand med information från artikelspårningsraden.  
4. Ange kortfattad information i fältet **Beskrivning**, t.ex. om villkoret för artikeln.  
5. Välj åtgärden **Kommentar** för att skapa en separat kommentarspost.  
6. Markera kryssrutan **Spärrad** om du vill utesluta serie- eller partinummer från alla transaktioner.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Så här ändras befintlig information om serie-/partinummer  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.  
2. Markera en artikel som har en artikelspårningskod och serienr eller partinr information.
3. Från sidan **artikelkort** väljer du åtgärden **transaktioner** och väljer **transaktioner**.
4. Välj fältet **Partinr** , eller **Serienr**. Om information för artikelspårningsnumret finns öppnas sidan **Lista med partinr.information** eller **Lista med serienr.information**.  
5. Välj ett kort och välj sedan åtgärden **Partinrinfo.kort/Serienr informationskort**.  
6. Ändra den korta beskrivningstexten, kommentarsposten eller fältet **Spärrad**.  

Du kan inte ändra serie- eller partinummer eller antal. För att kunna göra det måste du gruppera artikeltransaktionen i fråga. Mer information finns i [Omgruppera parti- eller serienummer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Så här tilldelar du serie-/partinummer vid ankommande transaktioner  
Ibland vill man i ett företag kunna spåra artiklar från det ögonblick då de ankommer till företaget. I detta fall utgör ofta inköpsordern det centrala dokumentet, även om du kan hantera artikelspårning från vilket ankommande dokument som helst och visa dokumentets bokförda transaktioner i de associerade artikeltransaktionerna.  

De exakta reglerna för hantering av artikelspårningsnummer i företaget avgörs av inställningarna för sidan **Artikelspårning kodkort**.  

> [!NOTE]  
>  För att kunna använda artikelspårningsnummer i distributionslageraktiviteter måste inställningsfälten **Parti dist.lager spårning** och **SN dist.lager spårning** väljas eftersom de definierar vilka regler som ska gälla för serienummer eller partinummer för distributionslageraktiviteterna.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsorder** och välj sedan relaterad länk.  
2.  Markera önskad dokumentrad och klicka på snabbfliken **Rader**, välj åtgärden **Rad** och sedan åtgärden **Artikelspårningsrader**.  

    Du kan tilldela serie- eller partinummer på följande sätt:  

    -   Automatiskt, genom att välja **Tilldela serienr** eller **Tilldela partinr** så att serie-/partinummer tilldelas utifrån fördefinierade nummerserier.  
    -   Automatiskt, genom att välja **Skapa anpassat SN** så att serie-/partinummer tilldelas utifrån nummerserier som du specifikt definierar för de ankommande artiklarna.  
    -   Manuellt, genom att ange serie- eller partinummer direkt, t.ex. leverantörens nummer.  
    -   Manuellt, genom att ange ett särskilt nummer för varje artikelenhet.  

3. Tilldela automatiskt genom att välja åtgärden **skapa anpassad SN**.  
4. I fältet **Anpassat SN** anger du startnumret för en beskrivande serienummerserie, till exempel **S/N-Vend0001**.  
5. I fältet **Öka** skriver du 1 för att ange att varje påföljande nummer ökar med ett.  

    Fältet **Antal att skapa** innehåller radantalet som standard, men detta går att ändra.  

6. Markera kryssrutan **Skapa nytt partinr** för att ordna in de nya serienumren i ett annat parti.  
7. Välj knappen **OK**.  

Nu skapas ett partinummer som innehåller enskilda serienummer enligt artikelantalet på dokumentraden, med början från **S/N-Vend0001**.  

I matrisen med antalsfält i huvudet visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalen måste stämma överens med antalen på dokumentraden, som anges med 0 i fälten **Odefinierad**.  

När dokumentet bokförs överförs artikelspårningstransaktionerna till de associerade artikeltransaktionerna.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Så här tilldelar du serie- eller partinummer vid avgående transaktioner  
Det finns två sätt att lägga till serie- och partinummer på utgående transaktioner:  

-   Välja bland befintliga serie- eller partinummer. Detta gäller om artikelspårningsnummer redan har tilldelats vid en ankommande transaktion. För mer information, se [Så här väljer du bland befintliga serie-/partinummer](inventory-how-work-item-tracking.md#to-select-from-existing-serial-or-lot-numbers)
-   Tilldela nya serie- eller partinummer vid avgående transaktioner. Detta gäller om artikelspårningsnummer inte ska tilldelas till artiklar förrän de säljs och är klara för utleverans.  

De olika reglerna för artikelspårningsnummer anges på sidan **Artikelspårning kodkort**.  

> [!NOTE]  
>  För att tilldela artikelspårningsnummer i distributionslageraktiviteter måste kryssrutorna **SN dist.lager spårning** och **Parti dist.lager spårning.** markeras på artikelns kort för artikelspårningskoden.    

1. Markera önskad dokumentrad och klicka på snabbfliken **Rader**, välj åtgärden **Order** och sedan åtgärden **Artikelspårningsrader**.  

    Du kan tilldela artikelspårningsnummer på följande sätt:  
    -   Automatiskt utifrån fördefinierade nummerserier: gå till fliken **Tilldela serienr** eller **Tilldela partinr.**.  
    -   Automatiskt, baserat på parametrar du definierar särskilt för den utgående artikeln: Välj åtgärden **Skapa anpassat SN**.  
    -   Manuellt, genom att ange serie- eller partinummer oberoende av nummerserierna.  

2.  Tilldela ett serienummer automatiskt genom att välja **Tilldela serienr**för den här proceduren  

    Fältet **Antal att skapa** innehåller radantalet som standard, men detta går att ändra.  
3.  Markera fältet **Skapa nytt partinr** för att ordna in de nya serienumren i ett annat parti.  
4.  Klicka på **OK** om du vill att ett partinummer och nya, enskilda serienummer ska skapas enligt "antal att hantera" på den associerade dokumentraden.  

I matrisen med antalsfält längst upp visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalet måste stämma överens med antalet på dokumentraden, som anges med **0** i fälten **Odefinierad**.  

När dokumentet bokförs överförs artikelspårningstransaktionerna till de associerade artikeltransaktionerna.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Så här väljer du bland befintliga serie-/partinummer  
Vanligtvis måste redan befintliga parti- eller serienummer i lagret väljas för artiklarna som kräver artikelspårning. Denna regel gäller även när avgående transaktioner skapas, d.v.s. när artiklarna tas bort ur lagret.  

 De exakta reglerna för hantering av artikelspårningsnummer i företaget avgörs av inställningarna för tabellen **Artikelspårningskod**.  

> [!NOTE]  
>  För att kunna hantera artikelspårningsnummer i distributionslageraktiviteter måste artikeln läggas upp med SN/Parti dist.lager spårning. Det är det som anger vilka regler som ska gälla för serienummer och partinummer i distributionslagret.

1.  I avgående dokument ska den rad markeras som serie- eller partinummer ska väljas för.  
2.  På snabbfliken **Rader**, välj åtgärden **Åtgärder**, **Rad** eller **Artikel** och sedan åtgärden **Artikelspårningsrader**.  
3.  På sidan **Artikelspårningsrader** finns det tre alternativ för att ange parti- eller serienummer:  

    -   Välj fältet **Partinr** eller **Serienr** och välj sedan ett nummer på sidan **Artikelspårning sammandrag**.  
    -   Välj åtgärden **Välj transaktioner**. På sidan **Markera transaktioner** visas alla parti - eller serienummer tillsammans med den tillgängliga informationen.

4. I fältet **Valt antal** anger du antalet av varje parti - eller serienummer som du vill använda.   
5. Klicka på **OK** så överförs den valda artikelspårningsinformationen till sidan **Artikelspårningsrader**.  
6. Ange eller skanna in artikelspårningsnumret.

I matrisen med antalsfält i huvudet visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalet måste stämma överens med antalet på dokumentraden, som anges med **0** i fälten **Odefinierad**.  

 När dokumentraden bokförs överförs artikelspårningsinformationen till de associerade artikeltransaktionerna.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Så här hanterar du serie-/partinummer på överföringsorder  
Rutinerna för hantering av serie- och partinummer som överförs mellan olika lagerställen påminner om procedurerna vid artikelinköp och -försäljning.  

Överföringsordern är emellertid unik eftersom både utleveransen och inleveransen utförs från samma överföringsrad, vilket innebär att samma instans på sidan **Artikelspårningsrader** används. Detta innebär också att artikelspårningsnummer som levereras från ett lagerställe måste inlevereras oförändrade till det andra lagerstället.  

 De exakta reglerna för hantering av artikelspårningsnummer i företaget avgörs av inställningarna för tabellen  **Artikelspårningskod**.    
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Överföringsorder** och välj sedan relaterad länk.  
2.  Öppna den order som du vill bearbeta. På snabbfliken **Rader** välj åtgärden **Rad**, **Artikelspårningsrader** och sedan **Utleverans**.  
3.  På sidan **Artikelspårningsrader** tilldelar eller väljer du serie-/partinummer för eventuella övriga avgående artikeltransaktioner.  

    Vid hanteringen av serie- och partinummer för överföringsartiklar, har artiklarna vanligtvis redan tilldelats nummer. Förloppet består därför oftast bara av att du väljer bland befintliga serie- eller partinummer.  

4.  Bokför överföringsordern, först ut- och sedan inleverans, för att ange att artiklarna överförs med artikelspårningstransaktionerna.  

Sidan **Artikelspårningsrader** är skrivskyddat under överföringen.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Så här hanterar du serie- och partinummer när du hämtar inleveransrader från en inköpsfaktura  
När du använder funktionen för att hämta bokförd inleverans, eller utleveransrader från relaterade fakturor eller kreditnotor, överförs artikelspårningsrader i distributionslagerdokumenten automatiskt. Men de behandlas på ett speciellt sätt.

Funktionen stöder följande processer för ankommande:  
-   **Hämta inleveransrader** – från en inköpsfaktura.  
-   **Hämta returleveransrader** – från en inköpskreditnota.  

Funktionen stöder följande processer för avgående:  
-   **Hämta leveransrader** – från en försäljningsfaktura eller kombinerade utleveranser.  
-   **Hämta returinleveransrader** – från en försäljningskreditnota.  

I de här situationerna kopieras befintliga artikelspårningsrader automatiskt till fakturan eller kreditnotan, men på sidan **Artikelspårningsrader** tillåts inga ändringar av serienummer eller partinummer. Endast kvantiteter kan ändras.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsfakturor** och välj sedan relaterad länk.  
2.  Öppna en inköpsfaktura för artiklar som är inköp med serie- eller partinummer.  
3.  Från en inköpsfaktura på snabbfliken **Rader** väljer du **Hämta inleveransrader**.  
4.  Välj inleveransrader, som har artikelspårningsrader, och välj sedan **OK** på sidan **Hämta inleveransrader**.  

    Källdokumentet kopieras till inköpsfakturan som en ny rad och artikelspårningsraderna kopieras till den underliggande sidan **Artikelspårningsrader**.  

5.  Välj den överförda inleveransraden i inköpsfakturan.  
6.  Klicka på **Rad** och välj **Artikelspårningsrader** på snabbfliken **Rader** om du vill visa de överförda artikelspårningsraderna.  

Innehållet i fälten **Serienr** Och **Partinr** går inte att redigera. Du kan dock ta bort hela rader eller ändra kvantiteten så att den stämmer med de ändringar som görs av ursprungsraden.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Gruppera parti- eller serienummer  
Att gruppera artikelspårningen för en artikel innebär att ett parti- eller serienummer ändras till ett nytt parti- eller serienummer eller att utgångsdatumet ändras till ett nytt utgångsdatum. Vid arbete med partier går det även att koppla flera partier till ett enda. De här aktiviteterna utförs med hjälp av artikelgrupperingsjournalen.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelgrupp.journal** och välj sedan relaterad länk.  
2.  Fyll i raden med relevant information. Mer information finns i [Beräkna lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md) eller [Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).
3.  Välj åtgärden **artikelspårningsrader**.  
4.  I fälten **Serienr** eller **Partinr** väljer du aktuellt serie- eller partinummer.  
5.  Om ett nytt artikelspårningsnummer behöver anges kan fälten **Nytt serienr** eller **Nytt partinr** användas. Det går även att koppla ett eller flera partier till ett nytt parti eller ett befintligt parti.  

    > [!NOTE]  
    >  Observera att när utgångsdatum grupperas föreslås artiklarna med de tidigaste utgångsdatumen för de avgående transaktionerna först. Mer information finns i [Plocka enligt FEFO](warehouse-picking-by-fefo.md).  

5.  Om ett nytt utgångsdatum behöver anges för serie- eller partinumret kan fältet **Nytt utgångsdatum** användas.  

    > [!IMPORTANT]  
    >  Om ett parti grupperas till samma partinummer, men med ett annat utgångsdatum, måste hela partiet grupperas på en artikelgrupperingsjournalrad. Om mer än ett parti grupperas till ett nytt partinummer, d.v.s. att mer än ett parti kopplas till ett nytt parti, måste samma nya utgångsdatum anges för samtliga partier. Om ett befintligt parti grupperas till ett annat befintligt parti, som inte har samma utgångsdatum, måste utgångsdatumet för det andra partiet användas. Om inga värden anges i fältet **Nytt utgångsdatum** grupperas parti- eller serienumret med ett tomt utgångsdatum.  

6.  Om det finns befintlig information om det gamla serie- eller partinumret går det att kopiera informationen till det nya serie- eller partinumret.  

    1.  På sidan **Artikelspårningsrader**, välj **Ny serienr-information** eller **Ny partinr-information**.  
    2.  Om du vill kopiera information från det gamla parti- eller serienumret väljer du åtgärden **Kopiera info**.  
    3.  Klicka på knappen **OK** när det parti- eller serienummer har valts som informationen ska kopieras ifrån. Detta görs i på sidan med informationslistor.  

7.  Genom att registrera information om parti- eller serienummer kan den befintliga informationen om parti- eller serienumret ändras.  
8.  Bokför journalen för att koppla de nya artikelspårningsnumren eller utgångsdatumen till den associerade artikeltransaktionen.

## <a name="see-also"></a>Se även
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)   
[Lagersaldo](inventory-manage-inventory.md)  
[Detaljer: Artikelspårning](design-details-item-tracking.md)
[Designdetaljer - artikelspårning och reservationer](design-details-item-tracking-and-reservations.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

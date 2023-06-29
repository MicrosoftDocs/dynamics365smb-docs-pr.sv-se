---
title: Arbeta med dimensioner för att spåra och analysera data
description: 'Använd dimensioner för att kategorisera poster, till exempel efter avdelning eller projekt, så att du enklare kan spåra och analysera data för att hjälpa dig att fatta bra affärsbeslut.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# <a name="work-with-dimensions"></a><a name="work-with-dimensions"></a>Arbeta med dimensioner

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis försäljningsorder. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

Så i stället för att skapa separata redovisningskonton för varje avdelning och projekt kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad kontoplan. Läs mer i [Business Intelligence](bi.md).

Ett annat exempel är att ställa in en dimension kallad *Avdelning* och sedan använda denna dimension när du bokför försäljningsdokument. På så sätt kan du använda business intelligence-verktyg för att visa vilken avdelning som sålt vilka artiklar. Ju fler dimensioner du använder, desto mer detaljerade är rapporterna som du baserar dina affärsbeslut på. Faktum är att en enda försäljningstransaktion kan innehålla information från olika dimensioner, t.ex.:  

* Kontot som artikelförsäljningen bokfördes till.  
* Var artikeln såldes.
* Vem som sålde den.
* Vilken kund som köpte den.

## <a name="analyzing-by-dimensions"></a><a name="analyzing-by-dimensions"></a>Analys per dimension

Dimensioner spelar en viktig roll inom affärsstöd, exempelvis när du definierar analysvyer. Läs mer i [Analysera data efter dimensioner](bi-how-analyze-data-dimension.md).

> [!TIP]
> Ett snabbt sätt att analysera transaktionsdata genom dimensioner är att använda åtgärden **Ange dimensionsfilter** för att filtrera summor efter dimensioner i kontoplanen samt på transaktionssidor.

> [!NOTE]
> I analysvyer används ofta data från dimensioner. Om du upptäcker att en felaktig dimension har använts på bokförda redovisningstransaktioner kan du korrigera dimensionsvärdena och uppdatera analysvyerna. Det hjälper till att hålla dina finansiella rapporter och analyser korrekta. Läs mer i [Felsökning och korrigering av dimensioner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets"></a><a name="dimension-sets"></a>Dimensionsuppsättningar

En dimensionsuppsättning en är en unik kombination av dimensionsvärden. De lagras som dimensionsuppsättningstransaktioner i databasen. Varje dimensionsuppsättningstransaktion representerar ett enstaka dimensionsvärde. Dessutom identifieras varje dimensionsuppsättning och dimensionsuppsättningstransaktion av ett gemensamt dimensionsuppsättnings-ID.  

När du skapar en journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden. I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.  

## <a name="setting-up-dimensions"></a><a name="setting-up-dimensions"></a>Lägga upp dimensioner

Du kan ange dimensioner och dimensionsvärden för att kategorisera journaler och dokument, till exempel försäljningsorder och inköpsorder. Du ställer in dimensioner på sidan **Dimensioner** där du skapar en rad för varje dimension som t. ex. *Projekt*, *Avdelning*, *Område* och *Säljare*.

Du kan också ställa in värden för dimensioner. Tänk dig att värden representerar ditt företags avdelningar. Dimensionsvärden kan anges i en hierarkisk struktur som liknar kontoplanen. Det innebär att data kan brytas ned i olika nivåer av granularitet och delmängder av dimensionsvärden kan summeras. Du kan definiera så många dimensioner och dimensionsvärden som behövs och alla i företaget kan använda dem.

När dimensioner och värden har konfigurerats kan du definiera globala dimensioner och kortdimensioner på sidan **Redovisningsinställningar**. Dessa dimensioner kan du alltid välja som fält på journal- och dokumentrader, och transaktioner utan att först öppna sidan **Dimensioner**. Läs mer i avsnittet [Att ställa in globala och genvägsdimensioner](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globala dimensioner** används som filter, till exempel i rapporter, batch-jobb och XMLports. Du kan använda två globala dimensioner, så välj dimensionerna som du ofta använder.
* **Genvägsdimensioner** finns tillgängliga som fält i journaler samt i journal- och redovisningstransaktioner. Du kan skapa upp till åtta av dessa.  

> [!NOTE]
> När du har använt en ny dimension i någon post, till exempel en rad eller en ny post, kan du inte radera dimensionen, även om du inte bokför posten. Detta beror på att [!INCLUDE[prod_short](includes/prod_short.md)] omedelbart skapar en dimensionsuppsättning för raden eller posten omedelbart. Läs mer i avsnittet [Dimensionsuppsättningar](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a><a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Konfigurera standarddimensioner för kunder, leverantörer och andra konton

Du kan tilldela en standarddimension för ett enskilt konto. Dimensionen kopieras till journal eller dokument när du anger numret på en rad, men du kan ta bort eller ändra koden på raden om det behövs. Du kan också kräva en dimension för att bokföra en transaktion i en viss typ av konto. > 

> [!NOTE]
> Standarddimensionens prioriteter är öppna för scenarier i försäljning och inköp som du kanske vill betala för särskild uppmärksamhet. När du använder standarddimensionens prioritet för försäljnings- och inköpsdokument, [!INCLUDE [prod_short](includes/prod_short.md)] beaktar alltid dimensionerna i rubriken som kommer från kunden eller leverantören. Det gäller dimensioner som du anger manuellt eller som standard och är särskilt relevant när du använder standarddimensioner på lagerställen och artiklar men inte på kunder eller leverantörer.
>
> **Exempel**
>
> Du har ett scenario med följande dimensionsinställningar:
>
> * En kund utan standarddimensioner
> * Ett objekt med ADM som dimensionsvärde för dimensionen AVDELNING
> * Ett lagerställe med PROD som dimensionsvärde för dimensionen AVDELNING
> * Standarddimensionens prioritet anges som kund > artikel > lagerställe
>
> När du skapar ett nytt dokument i det här scenariot används dimensioner enligt följande:
>
> * Om du skapar ett nytt dokument och lägger till en plats, blir standardvärdet för nya rader PROD. När du lägger till rader med artiklar behåller [!INCLUDE [prod_short](includes/prod_short.md)] PROD eftersom den kommer från dokumentets huvud.
>
> * Om du skapar ett nytt dokument och lägger till objekt som har ADM-dimensionsvärdet och sedan anger ett lagerställe i dokumentets rubrik, [!INCLUDE [prod_short](includes/prod_short.md)] kommer att fråga om du vill skriva över de befintliga raderna eftersom det finns en konflikt.
>
> Vi rekommenderar att du testar standard dimensionsinställningarna, dimensionsprioriteterna och i vilken ordning du anger data i dokument.  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dimensioner** och väljer sedan relaterad länk.  
2. På sidan **Dimensioner** väljer du relevant dimension och sedan åtgärden **Standarddim. för kontotyp**.  
3. Fyll i en rad för varje ny standarddimension du vill ange. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Om du vill kräva en dimension men inte tilldela ett standardvärde till den, lämnar du fältet **Dimensionsvärdekod** tomt och markerar **Kod alltid** i fältet **Bokförs med**.  

> [!WARNING]  
> Om kontot ska användas i batch-jobbet **Justera valutakurser** eller i batch-jobbet **Bokför lagerkostnad i redov.konto**, välj då inte **Kod obligatoriskt** eller **Samma kod**. Det går inte att använda dimensionskoder i dessa batch-jobb.  

> [!NOTE]  
> Om ett konto måste ha en annan dimension än den standarddimension som har tilldelats kontotypen måste en ny standarddimension anges för kontot. På så sätt ersätter standarddimensionen för kontot standarddimensionen för kontotypen.  

### <a name="to-set-up-default-dimension-priorities"></a><a name="to-set-up-default-dimension-priorities"></a>Så här anger du standarddimensionsprioritet

Olika kontotyper, t.ex. ett kundkonto och ett artikelkonto, kan ha olika definierade standarddimensioner. Detta kan resultera i att en transaktion har fler än en föreslagen standarddimension. Du kan undvika att den här typen av konflikter uppstår genom att använda prioritetsregler för de olika källorna.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Standarddimensionsprioritet** och välj sedan relaterad länk.  
2. På sidan **Standarddimensionsprioritet** i fältet **Källkod** anger du ursprungskoden för den transaktionstabell som standarddimensionsprioriteten gäller.  
3. Fyll i en rad för varje standarddimensionsprioritet du vill ha för den valda ursprungskoden.
4. Upprepa proceduren för varje ursprungskod du vill ange standarddimensionsprioritet för.  

> [!IMPORTANT]  
> Om du definierar två tabeller med samma prioritet för samma ursprungskod väljer [!INCLUDE[prod_short](includes/prod_short.md)] alltid tabellen med lägst tabell-ID.  

### <a name="to-set-up-dimension-combinations"></a><a name="to-set-up-dimension-combinations"></a>Så här definierar du dimensionskombinationer

Du kan förhindra att transaktioner bokförs med oförenliga eller irrelevanta dimensioner genom att spärra eller begränsa vissa kombinationer av två dimensioner. En spärrad dimensionskombination innebär att du inte kan bokföra båda dimensionerna i samma transaktion, oberoende av dimensionsvärdena. En begränsad dimensionskombination innebär däremot att du kan bokföra båda dimensionerna i samma transaktion, men endast för vissa kombinationer av dimensionsvärden.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **dimensionskombinationer** och väljer sedan relaterad länk.  
2. På sidan **Dimensionskombinationer** väljer du det dimensionskombinationsfält som du vill ha från följande alternativ.  

    |Fält|Description|
    |----------------------------------|---------------------------------------|  
    |**Inga begränsningar**|Den här dimensionskombinationen har inga begränsningar. Alla dimensionsvärden är tillåtna.|  
    |**Begränsad**|Den här dimensionskombinationen är begränsad beroende på vilka dimensionsvärden som anges. Du definierar begränsningarna på sidan **Dimensionsvärdekombination**.|  
    |**Spärrad**|Den här dimensionskombinationen är inte tillåten.|  

3. Om du valde alternativet **Begränsad** måste du definiera vilka kombinationer av dimensionsvärden som är spärrade. Gör det genom att välja fältet för att definiera dimensionsvärdeskombinationen.  
4. Välj en dimensionsvärdekombination som är spärrad och ange **Spärrad** i fältet. Ett tomt fält innebär att dimensionsvärdekombinationen är tillåten. Upprepa i fall flera kombinationer är spärrade.  

> [!NOTE]  
> Samma dimensioner visas både på rader och i kolumner, vilket innebär att alla dimensionskombinationer visas två gånger. [!INCLUDE[prod_short](includes/prod_short.md)] visar inställningarna automatiskt i båda fälten. Du kan inte välja någonting i fälten från det övre vänstra hörnet och nedåt eftersom dessa fält har samma dimension både på rader och i kolumner.  
>
> Det alternativ du valt visas inte förrän markören flyttas ur fältet.  
>
> Om du vill visa namnet på dimensionerna i stället för koden markerar du fältet **Visa kolumnnamn**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a><a name="to-set-up-global-and-shortcut-dimensions"></a>För att ställa in globala och genvägsdimensioner

Globala och genvägsdimensioner kan användas som filter i [!INCLUDE[prod_short](includes/prod_short.md)], däribland i rapporter, batch-jobb, sidor för reskontratransaktioner och analysvyer. Globala och genvägsdimensioner kan läggas till direkt utan att du först öppnar sidan **Dimensioner**. På journal- och dokumentrader kan du välja globala dimensioner respektive genvägsdimensioner i ett fält på raden. Du kan också ställa in två globala dimensioner och åtta genvägsdimensioner. Välj de dimensioner som du oftast använder.

> [!IMPORTANT]
> Om du ändrar en global eller genvägsdimension krävs att alla transaktioner som har bokförts med dimensionen uppdateras. Om du vill ändra en global dimension kan du använda funktionen **Ändra globala dimensioner**, men detta kan ta lång tid och dessutom påverka prestandan, och tabeller kan vara låsta under uppdateringen. Se till att du väljer globala och genvägsdimensioner noga så att du inte behöver ändra dem senare. Använd åtgärden **Ändra dimensioner** för att ändra en genvägsdimension.
>
> Läs mer i avsnittet [Att ändra globala dimensioner](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> När du lägger till eller ändrar en global eller genvägsdimension loggas du automatiskt ut och in igen, så att det nya värdet förbereds för användning.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.
2. Fyll i fälten på snabbfliken **Dimensioner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a><a name="to-change-global-dimensions"></a>Ändra globala dimensioner

När du ändrar en global eller genvägsdimension uppdateras alla transaktioner som har bokförts med dimensionen. Eftersom den här metoden kan vara tids krävande och påverka prestanda kan två olika lägen anpassas till databasens storlek.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.
2. Välj åtgärden **Ändra globala dimensioner**.
3. Längst upp på sidan väljer du ett av följande två lägen för att köra batch-jobbet.

    |Alternativ|Description|
    |-|-|
    |**Sekventiell**|(Standard) Hela ändringen utförs i en transaktion som återställer alla poster till de dimensioner de hade före ändringen.<br /><br />Det här alternativet rekommenderas om företaget har relativt få bokförda transaktioner, i vilket fall batch-jobbet tar kortast möjliga tid att slutföra. Med den här metoden låses flera tabeller och andra användare blockeras tills den är klar. Observera att det kan hända att det inte går att processen i det här läget i stora databaser. Använd i så fall alternativet **parallellt**.|
    |**Parallell**|Dimensionsändringen sker i flera bakgrundssessioner och åtgärden delas upp i flera transaktioner. Aktivera reglaget för **Parallell bearbetning** om du vill använda detta alternativ. <br /><br />Vi rekommenderar detta alternativ för stora databaser eller företag med många bokförda poster eftersom det tar kortast tid att slutföra. Observera att uppdateringsförfarandet inte startar om det finns mer än en aktiv databassession i det här läget.|  

4. I fälten **Global dimension 1 kod** och/eller **Global dimension 2 kod** anger du de nya dimensionerna. De aktuella dimensionerna visas i grått bakom fälten.
5. Gör något av följande beroende på läget:
    * I läget **Sekventiellt** väljer du åtgärden **Starta**.
    * I läget **Parallellt** väljer du åtgärden **Förbered**.

    Fliken **Loggtransaktioner** fylls med information om de dimensioner som kommer att ändras.
6. Logga ut från [!INCLUDE[prod_short](includes/prod_short.md)] och logga sedan in igen.
7. Välj åtgärden **Starta** för att starta den parallella bearbetningen av dimensionsändringarna.

### <a name="example-of-dimension-setup"></a><a name="example-of-dimension-setup"></a>Exempel på dimensionsinställningarna

Anta att ditt företag vill spåra transaktioner utifrån organisationens struktur och geografiska platser. För att göra detta kan du ange två dimensioner på sidan **Dimensioner**:

* **OMRÅDE**  
* **AVDELNING**  

| Kod | Name | Kodledtext | Filterledtext |
| --- | --- | --- | --- |
| OMRÅDE |Område |Områdeskod |Analysfilter |
| AVDELNING |Avdelning |Avdelningskod |Avdelningsfilter |

För **OMRÅDE** lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| 10 |Amerika |Från-summa |
| 20 |Nordamerika |Standard |
| 30 |Stillahavsområdet |Standard |
| 40 |Sydamerika |Standard |
| 50 |Region Americas, hela |Till-summa |
| 60 |Europa |Från-summa |
| 70 |EU |Standard |
| 80 |Utanför EU |Standard |
| 90 |Europa totalt |Till-summa |

För de två huvudsakliga geografiska områdena, USA och Europa, lägger du till underkategorier för områden med indrag av dimensionsvärden. Då kan du rapportera på försäljning eller utgifter i områden och hämta summorna för de större geografiska områdena. Du kan även välja att använda länder, regioner, kommuner eller städer som dimensionsvärden, beroende på ditt företag.

> [!NOTE]  
> Om du vill upprätta en hierarki måste koderna vara i alfabetisk ordning. Det innefattar koderna för dimensionsvärdena som ges i [!INCLUDE[prod_short](includes/prod_short.md)].  

För **AVDELNING** lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| PROD |Produktion |Standard |
| FÖRS |FÖRS |Standard |

Med denna konfiguration kan du lägga till två dimensioner som de två globala dimensionerna på sidan **Redovisningsinställningar**. Det betyder att du kan använda OMRÅDE och AVDELNING som filter för redovisningstransaktioner, samt i alla rapporter. De båda globala dimensionerna blir dessutom automatiskt tillgängliga för att användas som genvägsdimensioner på transaktionsrader och i dokumenthuvuden.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a><a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Få en översikt över dimensioner som används flera gånger

Sidan **Standarddimensioner: Flera** anger hur en grupp konton använder dimensioner och dimensionsvärden. Du kan konfigurera detta genom att markera flera konton och sedan ange standarddimensioner och dimensionsvärden för dem. Därefter föreslår programmet dessa dimensioner och dimensionsvärden varje gång ett av dessa konton används, till exempel på en journalrad. På så sätt underlättas användarens arbete med att registrera transaktioner, detta eftersom dimensionsfälten fylls i automatiskt. Observera också att dimensionsvärdena som föreslås kan ändras, till exempel på en journalrad.

Sidan **Standarddimensioner: Flera** innehåller följande fält:

|Fält|Description|
|-----|-----------|  
|**Dimensionskod**|Visar alla dimensioner som har definierats som standarddimensioner för ett eller flera av de markerade kontona. Om du väljer det här fältet kan du se en lista över tillgängliga dimensioner. Om du väljer en dimension anges den dimensionen som standarddimension för alla markerade konton.|
|**Dimensionsvärdekod**|Visar antingen ett enstaka dimensionsvärde eller termen (Konflikt). Om ett dimensionsvärde visas i fältet har alla markerade konton samma standarddimensionsvärde för en dimension. Om termen (Konflikt) visas i fältet har inte alla markerade konton samma standarddimensionsvärde för en dimension. Om du väljer fältet **Dimensionskod** ser du en lista över alla tillgängliga dimensionsvärden för en dimension. Om du väljer ett dimensionsvärde definieras det som standarddimensionsvärde för alla markerade konton.|
|**Bokförs med**|Visar antingen en enstaka bokföringsregel eller termen (Konflikt). Om en bokföringsregel visas i fältet har alla markerade konton samma bokföringsregel för ett dimensionsvärde. Om termen (Konflikt) visas i fältet har inte alla markerade konton samma bokföringsregel för ett dimensionsvärde. Om du väljer fältet **Bokförs med** ser du en lista över bokföringsregler för en dimension. Om du markerar en bokföringsregel tillämpas den på alla markerade konton.|

## <a name="use-dimensions"></a><a name="use-dimensions"></a>Använda dimensioner

I ett dokument som t. ex. en försäljningsorder kan du lägga till dimensionsinformation för både en individuell dokumentrad och själva dokument. Så på sidan **Försäljningsorder** kan du ange dimensionsvärden för de två första genvägsdimensionerna på den individuella försäljningsraden och sedan lägga till ytterligare dimensionsinformation om du väljer knappen **Dimensioner**.  

Om du istället arbetar med en journal kan du lägga till dimensionsinformation i en transaktion om du har lagt upp genvägsdimensioner som fält direkt på journalraderna.  

Du kan också ställa in standarddimensioner för konton eller kontotyper, så att dimensioner och dimensionsvärden fylls i automatiskt.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a><a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Så här visar du globala dimensioner på transaktionssidor

Globala dimensioner är alltid definierade och namngivna utifrån företaget. Om du vill visa de globala dimensionerna för ditt företag öppnar du sidan **Redovisningsinställningar**.

Du kan se om det finns globala dimensioner för transaktionerna på en transaktionssida. De två globala dimensionerna skiljer sig från övriga dimensioner eftersom de kan användas som filter var som helst i [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kontoplan** och väljer sedan relaterad länk.  
2. På sidan **Kontoplan** väljer du åtgärden **Redovisningstransaktioner**.  
3. Om du bara vill visa relevanta transaktioner definierar du ett eller flera filter på sidan.  
4. Om du vill visa alla dimensioner för en transaktion markerar du transaktionen och väljer sedan åtgärden **Dimensioner**.  

> [!NOTE]  
> Sidan **Transaktionsdimensioner** visas dimensionerna för en transaktion i taget. När du bläddrar bland transaktionerna ändras innehållet på sidan **Transaktionsdimensioner** därefter.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

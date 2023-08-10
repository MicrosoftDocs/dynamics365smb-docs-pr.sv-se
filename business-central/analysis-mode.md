---
title: Analysera data i listsidor med hjälp av dataanalysläge
description: Lär dig hur du använder dataanalysläget i Business Central för att analysera data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/30/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-data-using-data-analysis-mode"></a>Analysera listdata med hjälp av dataanalysläge

I den här artikeln lär du dig hur du analyserar data från listsidor med *dataanalysläge*. I dataanalysläget kan du analysera data direkt från sidan, utan att behöva köra en rapport eller växla till ett annat program som Excel. Det är ett interaktivt och mångsidigt sätt att beräkna, sammanfatta och undersöka data. I stället för att köra rapporter med olika alternativ och filter kan du lägga till flera flikar som representerar olika uppgifter eller vyer för informationen. Exemplen kan vara "mina kunder", "följa upp poster", "nyligen tillagda leverantörer", "försäljningsstatistik" eller någon annan vy som du kan tänka på.

> [!TIP]
> En bra sak om dataanalysläget är att det inte ändrar någon av de underliggande data för listsidan eller sidans layout när den inte är i dataanalysläget. Det bästa sättet att lära sig mer om det du kan göra i dataanalysläget är att testa saker.

## <a name="prerequisite"></a>Förutsättningar

Dataanalysläget är för närvarande i förhandsgranskning, vilket innebär att en administratör måste aktivera den innan du kan använda den. Om du är administratör och vill aktivera dataanalysläget går du till sidan **Funktionshantering** och aktiverar **Funktionsuppdatering: Analysläge, snabbanalysera data direkt i Business Central**. Mer information om att aktivera eller inaktivera funktioner finns i [Funktionshantering](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="get-started"></a>Kom i gång

1. Öppna listsidan.

   Om du t.ex. vill arbeta med **Kundreskontratransaktioner** markerar du ![Förstoringsglas som öppnar funktionen Berätta](media/ui-search/search_small.png). ikon (<kbd>Alt</kbd>+<kbd>Q</kbd>), ange *kundreskontratransaktioner* och välj sedan relaterad länk.  
2. I åtgärdsfältet högst upp på sidan aktiverar du växlingen **Analys**.

    I dataanalysläge öppnas data i en upplevelse som är optimerad för dataanalys.  I dataanalysläge ersätts normalt åtgärdsfältet med ett speciellt fältet dataanalysläge. I bilden nedan visas de olika områdena på en sida i dataanalysläge.

   [![Visar en översikt över en sida i dataanalysläge](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Varje område förklaras i följande avsnitt.

3. Använd de olika områdena för att ändra, sammanfatta och analysera data. Se följande avsnitt för information.

4. När du vill avsluta analys läget stänger du av växlingsknappen **analys**.

   De analysvyer som du har lagt till finns kvar tills du tar bort dem. Om du återgår till dataanalysläget igen visas de exakt som du lämnade dem.

> [!NOTE]
> De data som visas i analysläget styrs av de filter eller vyer som anges på listsidan. På så sätt kan du förkonfigurera data innan du startar analysläget.

## <a name="work-with-data-analysis-mode"></a>Arbeta med dataanalysläge

I dataanalysläge delas sidan upp i två områden:

- Huvudområdet, som består av dataområdet (1), sammanfattningsfältet (2) och flikfältet (5)
- Datamanipuleringsområdet, som består av två rutor: kolumner (3) och analysfilter (4).

### <a name="data-area-1"></a>Dataområde (1)

Dataområdet är där raderna och kolumnerna på listsidan visas och data summeras. Dataområdet ger ett mångsidigt sätt att styra layouten på kolumner och ett snabbt sätt att få fram en sammanfattning av informationen. För kolumner som innehåller numeriska värden visas summan av alla värden i kolumnen på en sista rad, såvida du inte har definierat radgrupper. I det här fallet visas summorna som delsummor för grupperna.  

![Visar en översikt över dataområde på en sida i dataanalysläge](media/analysis-mode-data-area.png)

- Om du vill flytta en kolumn markerar du den och drar den till den plats som verkar vettig i analysen.
- Högerklicka på kolumnen eller hovra över den och välj menyikonen ![Visar ikonen i en kolumn i dataanalysläge som öppnar en meny med åtgärder](media/analysis-mode-column-menu-icon.png) För att komma åt flera åtgärder som du kan utföra på kolumner. Som exempel:

  - Om du vill fästa en kolumn till vänster eller höger om dataområdet så att den inte flyttas från skärmen när du bläddrar, markerar du ![Visar ikonen i en kolumn i dataanalysläge som öppnar en meny med åtgärder](media/analysis-mode-column-menu-icon.png) > **Fästa kolumn** > **Fästa vänster** kolumndelen.
  - Definiera datafilter direkt i kolumndefinitionen i stället för att gå till rutan **analysfilter**. Du kan fortfarande visa information om relaterade data och för varje rad och öppna kortet för att lära dig mer om en viss entitet.
- Använd dataområdet för att interagera med informationen. För kolumner som innehåller numeriska, summerbara värden kan du hämta beskrivande statistik för en fältuppsättning genom att markera dem. Statistiken visas i statusfältet (2) längs med sidans nederkant.
- Exportera data i Excel- eller csv-format. Du kan bara högerklicka på dataområdet eller en cellmarkering som du vill exportera.

### <a name="summary-bar-2"></a>Sammanfattningsfält (2)

Sammanfattningsfältet visas längs sidans nederkant och statistik visas över informationen i listan. När du interagerar med kolumner vars värden kan summeras, t.ex. om du markerar flera rader i en kolumn som visar belopp, kommer informationen att uppdateras.

![Visar en översikt över ett sammanfattningsfält i dataanalysläge](media/analysis-mode-totals-row.png)

I följande tabell beskrivs de olika nummer som visas i summa området:

|Nummer|Beskrivning|
|-|-|
|Rader|Antalet markerade rader som en del av det totala antalet tillgängliga rader. |
|Totalt antal rader|Antalet rader i den ofiltrerade listan.|
|Har filtrerats|Antalet rader som visas som ett resultat av de filter som tillämpas på listan.|
|Genomsnitt|Det genomsnittliga värdet i alla valda summeringsbara fält.|
|Antal|Antalet valda rader.|
|Min|Det minsta värdet i alla valda summeringsbara fält.|
|Max|Det högsta värdet i alla valda summeringsbara fält.|
|Summa|Total summan av alla värden i de valda summeringsbara fälten.|

### <a name="columns-3"></a>Kolumner (3)

 **Kolumnerna** är en av två fönsterrutor som samarbetar för att definiera analysen. Det andra området är rutan **Analysfilter**.  Rutan **kolumner** används för att summera data. Använd rutan **kolumner** för att definiera vilka kolumner som ska tas med i analysen.

![Visar en översikt över kolumnrutan i dataanalysläge](media/analysis-mode-columns-2.png)

|Områden|Beskrivning|
|-|-|
|Sök/markera eller avmarkera alla rutor|Söka efter kolumner. Markera kryssrutan om du vill välja/rensa alla kolumner.|
|Kryssrutor|I det här området finns en kryssruta för varje fält i källtabellen för listan. Använd det här området om du vill ändra vilka kolumner som ska visas i listan. Markera en kryssruta om du vill visa kolumnen för fältet på sidan. Avmarkera kryssrutan om du vill dölja kolumnen. |
|Radgrupper|Använd det här området om du vill gruppera och summera data efter ett eller flera fält. Du kan endast ta med icke-numeriska fält, t.ex. text, datum och tid. Radgrupper används ofta i pivotläge.|
|Värden|Använd det här området för att ange fält som du vill ha en total summa för. Du kan bara ta med fält som innehåller nummer som kan läggas samman. Det kan t.ex. inte vara text, datum eller tid.|

Om du vill flytta ett fält från ett område till ett annat väljer du ta bort ikon ![Visar en översikt över en sida i analysläge](media/column-grab-icon.png) bredvid kolumnen i listan ovan och dra till målområdet. Du kan inte flytta ett fält till ett område där det inte är tillåten.

### <a name="analysis-filters-4"></a>Analysfilter (4)

Med rutan **Analysfilter** kan du ange ytterligare datafilter för kolumner för att begränsa posterna i listan. Ange filter för kolumner om du vill begränsa antalet poster i listan och efterföljande summor till endast de transaktioner som du är intresserad av baserat på ett villkor som du definierar. Du kanske till exempel bara vill ha information om en viss kund eller försäljningsorder som överstiger ett visst belopp. Om du vill definiera ett filter markerar du kolumnen, väljer jämförelseåtgärden i listan (t.ex. **lika med** eller **börjar med**) och anger sedan värdet.

![Visar en översikt över filterrutan i analysläge](media/analysis-mode-filters.png)

> [!NOTE]
> De extra filtren gäller endast för den aktuella analysfliken. På så sätt kan du definiera exakt de extra datafilter som behövs för en viss analys.

### <a name="tabs-5"></a>Flikar (5)

På flikområdet kan du skapa olika konfigurationer (kolumner och analysfilter) på olika flikar, där du kan ändra data på flikarna oberoende av varandra. Det finns alltid minst en flik som kallas **Analys 1** som standard. Det kan vara bra att lägga till fler flikar för att spara ofta använda analysvyer i en datauppsättning. Du kan till exempel ha flikar för att analysera data i pivotläge och andra flikar som filtrerar till en delmängd av rader. Vissa flikar kan visa en detaljerad vy med många kolumner och andra bara visa några få nyckelkolumner.

Här följer några tips på hur du arbetar med flera analyser:

- För att lägga till en ny flik, välj det stora **+**-tecknet bredvid den sista analysfliken.
- Välj nedåtpilen på en flik för att komma åt en lista över åtgärder du kan göra på en flik, som att byta namn, duplicera, ta bort och flytta.

   - **Ta bort** tar bort den flik som för tillfället är öppen. **Ta bort alla** tar bort alla flikar som du lagt till utom fliken standard **analys 1**.
- Du kan inte ta bort **Analys 1** helt men du kan byta namn på den med åtgärden **Byt namn** och ta bort alla ändringar som du har gjort med **Ta bort** eller **Ta bort alla**.  

- De analysvyer som du har lagt till och konfigurerat finns kvar tills du tar bort dem. Om du återgår till dataanalysläget igen visas de exakt som du lämnade dem.

   > [!TIP]
   > Flikarna som du ställer in visas bara för dig. Andra användare kan bara se de flikar som de har ställt in.
- Du kan kopiera analysflikar. Kopiering kan vara användbart om du vill experimentera med att ändra en flik utan att ändra originalet, eller om du vill skapa olika varianter av samma analys.

## <a name="pivot-mode"></a>Pivotläge

Du kan använda pivotläge för att analysera stora mängder numeriska data, delsummera data efter kategorier och underkategorier. Pivotläge fungerar som [pivotregister i Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Aktivera och inaktivera pivotläge genom att dra skjutreglaget för **pivotläge** i rutan **kolumner** (3). När du slår på pivotläget, visas området **Kolumnetiketter** i rutan. Använd området **kolumnetikett** om du vill gruppera totala summor för rader i kategorier. Fält som du lägger till i området **kolumnetiketter** visas som kolumner i dataområdet (1).

Att bygga ut dataanalysen i pivotläge innebär att du flyttar fält till de tre områdena: **radgrupper**, **kolumnetiketter** och **värden**. I bilden nedan visas var fälten är mappade till dataområdet (1), där `sum` är beräknad data och även eventuellt **värden**.

<table>
<tr><th></th><th>Kolumnetikett</th><th></th><th>Kolumnetikett</th><th></th></tr>
<tr><th>Radgrupp</th><th>Värde</th><th>Värde</th><th>Värde</th><th>Värde</th></tr>
<tr><td>rad</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
<tr><td>rad</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
<tr><td>rad</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
<tr><td>rad</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
</table>

> [!TIP]
> Kolumner som bara har ett fåtal värden är de bästa kandidater för att använda i kolumnen **värden**.

## <a name="limitations"></a>Begränsningar

Analysvyn innehåller för närvarande gränsen 100 000 rader. Om du överskrider den här gränsen får du ett meddelande som talar om detta. För att undvika den här begränsningen anger du filtren på sidan innan du växlar till data analys läge om det är möjligt.  Du kanske vill analysera en viss grupp av kunder eller kanske du vill ha data från det aktuella året. Du kan också välja en fördefinierad vy om den skulle fungera för analysen.

## <a name="see-also"></a>Se även

[Ad hoc-dataanalys](reports-adhoc-analysis.md)  
[Visa och redigera i Excel](across-work-with-excel.md)  

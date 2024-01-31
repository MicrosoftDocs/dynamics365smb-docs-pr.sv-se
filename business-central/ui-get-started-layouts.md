---
title: Kom igång med att skapa layouter
description: 'Lär dig hur du kan skapa layouter för att personligt anpassa utseendet på rapporten när den visas, skrivs ut eller sparas.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Kom igång med att skapa rapportlayouter

Business Central levereras med många inbyggda layouter som du kan använda i dina rapporter. Andra layouter kan ha lagts till som en del av andra tillägg. Du kan också skapa egna rapporter antingen från början eller baserat på en befintlig layout.

> [!IMPORTANT]
> Du kan också använda rapportlayouter för att lägga till innehåll i e-postmeddelanden. Med hjälp av rapportlayout kan du spara tid och säkerställa konsekvens genom att återanvända samma innehåll när du kommunicerar med kunderna. Om du vill använda anpassade rapportlayout med e-post måste du ange en filtyp för layouten. Du kan inte använda filtypen RDLC. Mer information finns i [ställa in återanvändbara e-posttexter och layouter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Översikt

När du arbetar med layouter för rapporter är det bra att tänka på layouten som en fil som importeras och kopplas till en rapport. Oavsett vilken typ av layout som används, är det i princip hur du hanterar layouter i Business Central. Vanligt vis arbetar du med sidan **rapportlayout**. Den största skillnaden är hur du utformar layouten, som görs med hjälp av program varan som layouten bygger på, som Word, Excel eller SQL Server Report Builder.

Med det här konceptet i åtanke. Det finns huvudsakligen tre eller fyra uppgifter som du behöver för att skapa en layout i en rapport:

1. Bestäm typ av layout.
2. Exportera en kopia av en befintlig layout som ska användas som utgångs punkt.
3. Gör ändringar i layout filen i det aktuella programmet.
4. Lägg till den nya filen i rapporten.

> [!IMPORTANT]
> Du kan inte ändra eller ersätta en tilläggslayout, som är en layout som kommer från ett fil tillägg. Du kan bara ändra eller ersätta användardefinierade layouter. På sidan **rapportmallar** kan du se om layout är en utöknings- eller egendefinierad layout genom att titta på kolumnen **tillägg**. En tilläggslayout visar information om källtillägget i kolumnen. **Tillägg** kolumnen är tom för en användardefinierad layout.
>
> Information om skillnaden mellan olika tilläggsfunktioner och användardefinierade layouter finns i [layoutkälla](ui-manage-report-layouts.md#layout-sources).

## Kom igång

De faktiska uppgifterna varierar beroende på vad din situation innebär. Med hjälp av följande tabell kan du komma igång.

|Vad vill du göra?|Se...|
|-----------------------|------|
|Räkna ut vilken typ av layout som passar bäst för min situation|[Bestämma vilken typ av layout du vill ha](#decide)|
|Skapa en ny layout för en rapport som bygger på en befintlig layout och som behåller den befintliga layouten.|[Skapa en ny layout](#create)|
|Göra ändringar i en befintlig layout som används i en rapport|[Ändra en layout](#modify)|
|Jag har en ny version av en layoutfil för en rapport. Jag vill ersätta den befintliga layoutfilen.|[Ersätta en layout](#replace)|
|Ändra den layout som används av en rapport till en annan layout|[Ange layout för en rapport](ui-set-report-layout.md)|
|Ändra namn och beskrivning för en layout|[Ändra namn på en layout](#rename)|

## <a name="decide"></a>Bestämma vilken typ av layout du vill ha

Det första du ska när du skapar en layout är att bestämma vilken [layouttyp](ui-manage-report-layouts.md#layout-types) du vill ha. Du kan välja mellan Word, Excel eller RDLC. Vilken typ av layout som ska användas beror på hur du vill att den genererade rapporten ska se ut. Dessutom är det beroende av hur du använder program vara för att skapa layouterna, som Word, Excel och SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-layouter är oftast de enklaste att skapa och ändra eftersom funktionerna för att summera data, lägga till grafik och formatering är vanliga Excel-funktioner.

* Alla rapporter och dokument har inte en data mängd som är optimerad för att användas med en Excel-layout. Aggregeringar och komplexa beräkningar fungerar till exempel bäst med RDLC- eller Word-layouter. Detsamma gäller dokument.

* Om du bara gör format ändringar som teckensnitt, storlek och färg, är en Word-layout också ett bra alternativ.

* Att lägga till data fält eller ordna om data fält i Word-eller RDLC är mer avancerade än med Excel.

* Det går bra att använda Word- och RDLC-layouter för rapporter som ska skrivas ut.  

* De allmänna designbegreppen för Word- och RDLC-layouter är lika varandra. Däremot har varje typ vissa designfunktioner som påverkar hur den genererade rapporten visas i [!INCLUDE[prod_short](includes/prod_short.md)]. Samma rapport kan se olika ut när du använder Word-layouten jämfört med RDLC-layouten.

## <a name="create"></a>Skapa en ny layout

Det finns två sätt att skapa en ny layout utifrån en befintlig layout. Ett sätt är att spara den befintliga layouten i en kopia. Det andra sättet är att exportera den befintliga layouten.

## [Kopierar](#tab/copy)

Kopiera är ett snabbt sätt att skapa en ny layout som är samma som en befintlig layout. När du har kopierat en kopia kommer du att göra ändringar genom att exportera layouten. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Välj den layout som du vill ha som kopia av den nya layouten och välj sedan åtgärden **redigera information**.

    Om du har valt en tilläggslayout får du en fråga om du vill redigera en kopia. Om du vill fortsätta, välj **Ja**.

    > [!TIP]
    > För att hjälpa dig hitta layout, använd rutan **Sök**, **Filter** och kolumnsortering.
3. Ändra **Layoutnamn**.
4. Aktivera **Spara ändringar att kopiera** växla till **På**, välj **OK**

   Den nya layouten visas på sidan **rapportlayout**.
5. Om du vill göra ändringar i den nya layouten läser du [Ändra en befintlig layout](#modify).

### [Exportera/importera](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Välj den layout som du vill ha som kopia av den nya layouten och välj sedan åtgärden **Exportera layout**.

   Layoutfilen hämtas till enheten. 

    > [!TIP]
    > För att hjälpa dig hitta layout, använd rutan **Sök**, **Filter** och kolumnsortering.

3. Öppna filen i det aktuella programmet, som t.ex. Word (för en DOCX-fil) eller Excel (för en xlsx-fil).

   Mer information finns i:

   * [Arbeta med Word-layouter](ui-how-add-fields-word-report-layout.md)
   * [Arbeta med Excel-layouter](ui-excel-report-layouts.md)
   * [Arbeta med RDLC-layouter](ui-rdlc-report-layouts.md)

   Gör ändringar i filen och spara den.

4. Gå tillbaka till **rapportlayouter** genom att välja **ny layout**-åtgärden.
5. Fyll i följande fält:

   |Fält|Beskrivning|Obligatoriskt|
   |-----|-----------|---------|
   |Rapport-ID|Ange det ID som har tilldelats rapporten|ja|
   |Layoutnamn| Ange ett kort beskrivningsnamn för layouten så att du enkelt kan identifiera den.|ja|
   |Beskrivning| Skriv mer detaljerad information i layouten. |nej|
   |Formalternativ|Ange det här fältet som överensstämmer med layoutens typ, som t.ex. Word, Excel eller RDLC.|ja|

6. Välj **OK**, gör sedan ett av följande steg för att ladda upp layoutfilen för rapporten:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Den valda filen överförs till layouten och du kommer då tillbaka till sidan **rapportlayout**.

Om du vill se hur rapporten ser ut med den nya layouten markerar du layouten i listan och väljer **Kör rapport**.

---

## <a name="modify"></a>Ändra en layout

Följ de här stegen om du vill ändra en befintlig användardefinierad layout.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Markera layout som du vill ändra och välj åtgärden **Exportera layout**.

   Layoutfilen hämtas till enheten. 

   > [!TIP]
   > För att hjälpa dig hitta layout, använd rutan **Sök**, **Filter** och kolumnsortering.

3. Öppna filen i det aktuella programmet, som t.ex. Word (för en DOCX-fil) eller Excel (för en xlsx-fil).

   Mer information finns i:

   * [Arbeta med Word-layouter](ui-how-add-fields-word-report-layout.md)
   * [Arbeta med Excel-layouter](ui-excel-report-layouts.md)
   * [Arbeta med RDLC-layouter](ui-rdlc-report-layouts.md)

   Gör ändringar i filen och spara den.

4. Gå tillbaka på sidan **rapportmallar**, markera den befintliga layouten och välj åtgärden **Ersätt layout**.
5. Välj **OK** > **Välj** för att öppna Utforskaren på enheten.
6. Hitta och välj Excel-filen och välj sedan **Öppna**.

   Den valda filen överförs till layouten och du kommer då tillbaka till sidan **rapportlayout**.
7. Om du vill se hur rapporten ser ut med den nya layouten markerar du layouten i listan och väljer **Kör rapport**.

## <a name="replace"></a>Ersätta en layout

Följ de här stegen för att ersätta den befintliga användardefinierade layouttabellen med en ny fil.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Markera den befintliga layouten och välj sedan åtgärden **Ersätt layout**.
3. Välj **OK** > **Välj** för att öppna Utforskaren på enheten.
4. Hitta och välj Excel-filen och välj sedan **Öppna**.

   Den valda filen överförs till layouten och du kommer då tillbaka till sidan **rapportlayout**.
5. Om du vill se hur rapporten ser ut med den nya layouten markerar du layouten i listan och väljer **Kör rapport**.

## <a name="rename"></a>Ändra namn på en layout

Följ nedanstående instruktioner om du vill ändra namn på och beskrivning av en användardefinierad layout.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Markera layout som du vill byta namn på och välj åtgärden **Redigera information**.

    > [!TIP]
    > För att hjälpa dig hitta layout, använd rutan **Sök**, **Filter** och kolumnsortering.
3. Ändra **layoutnamn** och klicka sedan på **OK**.

## Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med Word-layouter](ui-how-add-fields-word-report-layout.md)  
[Arbeta med Excel-layouter](ui-excel-report-layouts.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

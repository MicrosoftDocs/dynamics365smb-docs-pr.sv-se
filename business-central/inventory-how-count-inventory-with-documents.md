---
title: Räkna och justera lager
description: Beskriver hur du räknar fysiskt lager och använder lagerdokument för att justera lagerbehållningen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Beräkna och justera lager med hjälp av dokument

Du kan göra en fysisk inventering av artiklar med hjälp av inventeringsorder och inventeringsregistreringsdokument. Sidan **inventeringsorder** används för att ordna de fullständiga inventeringar, till exempel en per lagerställe. Använd sidan **registrering av fysiskt lager** för att samla in och kommunicera den faktiska inventeringen av artiklar. Du kan skapa flera inspelningar av en order, till exempel för att fördela grupper av artiklar till olika medarbetare.

Du kan skriva ut rapporten **registrering av fysiskt lager** från varje inspelning och innehåller tomma antalsfält för att ange det inventerade faktiska lagersaldot. När en du gör inventering och kvantiteterna som anges på sidan **omkodning av fysiskt lager** väljer du åtgärden **Slutför**. Denna åtgärd överför kvantiteterna till dessa rader på sidan **inventeringsorder**. [!INCLUDE [prod_short](includes/prod_short.md)]säkerställer att du inte kan registrera ett artikelantal två gånger.  

> [!NOTE]
> Med dokumenten för att utföra en inventering som ger mer kontroll och stöder distribution av inventeringen till flera medarbetare. Du kan också utföra aktiviteten med hjälp av journaler, till exempel **Inventeringsjournaler** och **Dist.lager inventeringsjournaler**. Läs mer på [Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md). I den här artikeln beskrivs hur du utför en inventering med hjälp av dokument.
>
> Om du använder zoner i ditt lager kan du inte använda inventeringsorder. Använd istället sidan **Dist.lag. inventeringsjournal** för att räkna distributionslagertransaktionerna innan du synkroniserar dem med artikeltransaktionerna.

Inventering med dokument består av följande övergripande åtgärder:

1. Skapa en inventeringsorder med förväntade artikelkvantiteter som fylls i automatiskt.
2. Skapa minst en inventeringsregistrering från ordern.
3. Ange antalet räknade artiklar på registreringarna som anges på utskrifter, till exempel och anger värdet till **avslutad**.
4. Slutför och bokför inventeringsordern.

## Skapa en inventeringsorder

En inventeringsorder är ett fullständigt dokument som består av en inventering i orderhuvudet och vissa orderrader. Informationen i inventeringshuvudet beskriver hur du gör en inventering. Orderraderna innehåller information om artiklarna och var de finns.

Om du vill skapa inventeringsorderrader kan du använda åtgärden **beräkna rader** för att lägga till det aktuella lagret som rader på ordern. Du kan även använda åtgärden **Kopiera från dokument** för att fylla i raderna med innehållet i en annan ordning för öppna eller bokförda inventeringen. Nedan beskrivs endast hur du använder åtgärden **beräkna rader**.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokför inventeringsorder** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i de fält som krävs på snabbfliken **Allmänt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  **På fliken Åtgärder** i gruppen **Funktioner** väljer du **Annat** och sedan **Beräkna rader**.
5. Välj alternativ om det behövs.
6. Ange filter, till exempel för att endast ta med en delmängd av artiklar som ska beräknas med den första registreringen.

    > [!TIP]
    > Du kan planera för flera medarbetare att beräkna inventering genom att ange olika filter varje gång du använder åtgärden **beräkna rader** för att fylla i ordern med en delmängd av lagerartiklar som en användare registrerar. När du skapar flera registreringar för fysiskt lager för flera anställda minimerar du risken för att räkna artiklar två gånger. Mer information finns i [Så här skapar du en inventeringsregistrering](#to-create-a-physical-inventory-recording).

7. Välj **OK**.

En rad för varje artikel som finns på den valda platsen och ange filter och alternativ som lagts till ordern. För artiklar som har ställts in för artikelspårning markeras kryssrutan **använda artikelspårning** och information om den förväntade kvantiteten av serie- och partinummer finns genom att välja **rader** och **Artikelspårningsrader**. Mer information finns i [Hantera artikelspårning vid inventering](#handle-item-tracking-when-counting-inventory).

Du kan nu skapa en eller flera registreringar som är instruktioner till anställda som utför inventeringen.  

> [!NOTE]
> Om du använder paketspecifik spårning kan du även använda dokument för att räkna och justera lagret med paketnummer. Om du vill börja använda den här funktionen måste du aktivera **Funktionsuppdatering: Aktivera användning av paketspårning i inventeringsorder** på sidan **Funktionshantering**. Befintliga inventeringsorder uppdateras, men [!INCLUDE [prod_short](includes/prod_short.md)] kan inte fylla i **paketnumret.** . Du måste återskapa raderna med åtgärden **Beräkna rader** på sidan **Inventeringsorder**.
>
> Du kan ange kollinumret för artiklar där paketspårning behövs på sidan **Rader för inventeringsregistrering**. Välja **Avsluta** för att slutföra registreringen.
>
> När du har valt **Slutför** på sidan **Inventeringsorder** [!INCLUDE [prod_short](includes/prod_short.md)] beräknar du skillnader med avseende på paketet och annan artikelspårningsinformation och gör positiva eller negativa justeringar.

## Skapa en inventeringsregistrering

För varje inventeringsorder kan du skapa ett eller flera registreringsdokument för fysiskt lager där de anställda anger de inventerade kvantiteterna. Anställda kan ange kvantiteter antingen manuellt eller med en skanningsenhet.

Som standard skapas en registrering för alla rader på relaterad inventeringsorder. För att undvika att två anställda räknar samma artiklar om du distribuerar inventeringen fyller du gradvis i den fysiska lagerordern genom att ange filter för batch-jobbet **Beräkna rader**. Skapa sedan inventeringsregistreringen med kryssrutan **Bara rader som inte finns i registreringar** markerad. Den här inställningen säkerställer att varje ny registrering innehåller andra artiklar än de på andra registreringar.

Vid manuell beräkning, kan du skriva ut rapporten **Inventeringsregistrering** som har en tom kolumn där anställda vid distributionslagret kan skriva inventerade kvantiteter. När inventeringen är klar anger du kvantiteterna som är registrerade på rader på sidan **Inventeringsregistrering**. Slutligen kan du överföra registrerade kvantiteter till relaterade inventeringsordern genom att sätta status på **avslutad**.

1. På en **sida för en inventeringsorder** som innehåller rader för de artiklar som ska räknas i en inspelning måste du välja **åtgärden Skapa ny inspelning** .
1.  **På fliken Åtgärder** i **gruppen Funktioner** väljer du **Annat** och sedan **Skapa ny inspelning**.
1. Välj alternativ och ange filter efter behov.
1. Välj **OK**.
1. För varje uppsättning artiklar som ska inventeras, läs in dem på den relaterade inventeringsordern och upprepa steg 1 till 3 med kryssrutan **Bara rader som inte finns i registreringar** markerad.
1.  **På fliken Relaterad** väljer du **Order** och väljer **sedan åtgärden Inspelningar** för att öppna **sidan Inventeringsregistreringslista** .
1. Öppna relevant registrering.
1. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
1. För artiklar som använder artikelspårning skapar du ytterligare en rad för varje partinummer eller serienummer genom att välja åtgärd **funktion** och åtgärd **kopiera rad**. Mer information finns i [Hantera artikelspårning vid inventering](#handle-item-tracking-when-counting-inventory).  
1. Välj åtgärden **Skriv ut** för att förbereda fysiska dokumentet som anställda ska använda för att anteckna inventerade kvantiteter.

## Slutför en inventeringsregistrering

När de anställda har räknat kvantiteterna registrerar du kvantiteterna i [!INCLUDE [prod_short](includes/prod_short.md)].

1. Från sidan **Inventeringsregistreringslista** markera inventeringsregistrering som du vill slutföra och klicka på åtgärden **redigera**.
2. På snabbfliken **rader** fyller du i faktiska räknade kvantiteten i fältet **antal** för varje rad.
3. För artiklar med serie- eller partinummer (kryssrutan **använd artikelspårning** är markerad), anger du kvantiteterna på raderna för artikelns serienummer och partinummer respektive fråga. Mer information finns i [Hantera artikelspårning vid inventering](#handle-item-tracking-when-counting-inventory).
4. Markera kryssrutan **registrerad** på varje rad.
5. När du har angett alla data för en inventeringsregistrering, väljer du åtgärden **slutför**. Observera att alla rader måste ha kryssrutan **registrerad** markerad.

    > [!NOTE]
    > När du är klar med en inventeringsregistrering överförs varje rad till raden på relaterad inventeringsorder som exakt matchar det. För att matcha måste värdena i fälten **Artikelnr**, **Variantkod**, **Platskod** och **Lagerställekod** vara samma för registrering och orderraderna.>
    > 
    > Om det inte finns några matchande inventeringsorderrad och om kryssrutan **Tillåt registrering utan order** är markerad och en ny rad läggs till och kryssrutan **Registrerade utan order** markeras på den relaterade inventeringsorderraden. I annat fall visas ett felmeddelande och processen avbryts.> Om mer än en inventeringsregistreringsrad matchar en inventeringsorderrad, visas ett meddelande och processen avbryts. Om du av någon anledning har två identiska inventeringsrader på inventeringsordern använder du en åtgärd för att lösa problemet. Mer information finns i [Hitta dubbla inventeringsorderrader](#to-find-duplicate-physical-inventory-order-lines).

## Slutför en inventeringsorder

När du är klar med registreringen **av en inventering uppdateras fältet Inventerbart antal (bas)**  på den relaterade inventeringsordern med de räknade (registrerade) värdena och **kryssrutan På registreringsrader** markeras. Om ett beräknat antal skiljer sig från det förväntade antalet visas skillnaden i **fälten Pos ant. (bas)**  och **Neg ant. (bas).** 

För åtkomst till förväntade kvantiteter och alla registrerade avvikelser för artiklar med artikelspårning väljer du åtgärden **rader** och väljer sedan **Artikelspårningsrader** för att välja olika vyer för serienummer och partinummer i den inventeringen.

Du kan även välja differensen för **Differens för inventeringsorder** åtgärd för att visa eventuella skillnader mellan förväntat antal och inventerat antal.

### Hitta dubbla inventeringsorderrader

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokför inventeringsorder** och väljer sedan relaterad länk.
2. Öppna den inventeringsorder som du vill visa dubbla rader för.
1.  **På fliken Relaterad** väljer du **Annat** och sedan **Visa dubblettrader**.

Dubbla inventeringsorderraderna visas så att du kan ta bort dem och endast en rad med en unik uppsättning värden i fälten **Artikelnr**, **Variantkod**, **Platskod** och **Lagerställekod**.

### Bokför en inventeringsorder

När du har slutfört en inventeringsorder och ändrar dess status till **avslutad**, kan du bokföra den. Du kan bara ange produktionsorderstatusen från inventeringen till **avslutad** om följande villkor gäller:

- Alla relaterade inventeringsregistreringar har statusen **avslutad**.
- Varje inventeringsorderrad har inventerats av minst en inventeringsregistreringsrad.
- Kryssrutan **På registrerade rader** och **Beräknat förväntat antal** har markerats för alla inventeringsorderrader.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokför inventeringsorder** och väljer sedan relaterad länk.
2. Markera den inventeringsorder som du vill slutföra och välj sedan åtgärden **Redigera**.

    På sidan **inventeringsorder** visar du den kvantitet som finns i fältet **Ant. registrerade (bas)**.
3. Välj åtgärden **Slutför**.

    Värdet i fältet **Status** är **Avslutad**. Du kan nu bara ändra ordningen genom att välja åtgärden **Öppna igen**.
4. Välj åtgärden **Bokför** och välj sedan knappen **OK** för att bokföra ordern.

    Artikeltransaktionerna uppdateras tillsammans med alla relaterade artikelspårningstransaktionerna.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### För att visa bokförda inventeringsorder

När du har bokfört inventeringsordern kommer den att tas bort och du kan visa och utvärdera dokumentet som en bokförd inventeringsorder. Den bokförda ordern innehåller dess inventeringsregistreringar och eventuella kommentarer.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda inventeringsorder** och väljer sedan relaterad länk.
2. På sidan **Bokförda inventeringsorder** markera bokförda ordern som du vill visa och välj sedan åtgärden **visa**.
3.  **På fliken Relaterad** väljer du **Order** och sedan **åtgärden Inspelningar** för att visa en lista över relaterade fysiska inventeringsinspelningar.  

## Hantera artikelspårning vid inventering

Artikelspårning relaterar till serie- eller partinummer som har tilldelats artiklarna. Vid inventering av en artikel i lagret som, till exempel 10 olika partinummer ska den anställde kunna registrera vilka och hur många enheter av varje partinummer som finns i lager. Mer information finns i [Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md).

Kryssrutan **använda artikelspårning** på inventeringsorderrader väljs automatiskt om artikelspårningskoden har ställts in för artikeln. Du kan markera eller avmarkera kryssrutan manuellt.

### Exempel – Förbered en inventeringsregistrering för en artikelspårad artikel

Beakta inventeringsperioden för artikel A, som finns i lager som tio olika serienummer.

1. På registreringsraden för artikeln väljer du kryssrutan **använda artikelspårning**.
2. Välj fältet **serienr**, markera det första serienumret som finns i lager för artikeln och välj sedan knappen **OK**.

    Kopiera raden för den första artikelspårade artikeln för att infoga extra rader som motsvarar antalet serienummer i lagret.

3. Välj åtgärden **funktion** och sedan **kopia raden**.
4. På sidan **Kopiera inventeringsregistreringsrad**, ange **9** i fältet **Antal kopior** och välj sedan **OK**.
5. På första raden, i fältet **serienr** markerar du nästa serienumret för artikeln.
6. Upprepa steg 5 för de återstående åtta serienumren. Se till att du inte väljer samma nummer två gånger.
7. Välj åtgärden **Skriv ut** för att förbereda utskrifter som anställda ska använda för att anteckna inventerade artiklar och serie-/partinummer.

Observera att rapporten **Inventeringsregistrering** innehåller tio rader för artikel A, en för varje löpnummer.

### Exempel – registrera och bokföra inventerat partinummeravvikelser

En partispårad artikel lagras i lagret med ”PARTI”-nummerserien.

**Förväntat lagersaldo**:

|Partinr|Antal|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Totalt|120|

**Registrerade kvantiteter**:

|Partinr|Antal|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Totalt|112|

**Kvantiteter att bokföra**:

|Partinr|Förväntad kvantitet|Registrerad kvantitet|Kvantitet att bokföra|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Totalt|120|112|-8|

På sidan **inventeringsorder** innehåller fältet **Neg. antal (bas)** **8**. För den aktuella orderraden visar sidan **Artikelspårningslista för inventering** positiva eller negativa kvantiteter för varje partinummer.

## Inventariedokument

Följande typer av dokument är användbara för att hantera distributionslagret:

* Använd **lagerinleveranser** för att registrera positiva justeringar av artiklar baserat på kvalitet, kvantitet och kostnad.
* Använd **lagerutleveranser** för att skriva av saknade eller skadade varor.

Du kan skriva ut dokumenten när som helst, släppa och öppna dem igen och tilldela gemensamma värden, till exempel dimensioner, i huvudet. Om du vill skriva ut dokumenten igen efter att de har bokförts använder du sidorna **Bokförd lagerinleverans** och **Bokförd lagerutleverans**.

> [!NOTE]
> Innan du kan använda dessa dokument måste du ange en nummerserie för att skapa deras identifierare. Mer information finns i [Så här ställer du in numrering för lagerdokument](#to-set-up-numbering-for-inventory-documents).

### Så här ställer du in numrering för lagerdokument

I följande procedur beskrivs hur du ställer in numrering för inventeringsdokument.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerinställning** och väljer sedan relaterad länk.
2. På snabbfliken **Numrering** ange följande fält nummerserien för dokument:

   - **Invt. Inleverans nr.**  
   - **Postat Invt. Inleverans nr.**  
   - **Invt. Sändningsnummer**  
   - **Postat Invt. Sändningsnummer**  

### Så här skapar och bokför du ett lagerdokument

Följande procedur visar hur du skapar, skriver ut och bokför en lagerinleverans. Momenten är liknande för bokförda lagerutleveranser.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Lagerinleveranser** och väljer sedan relaterad länk.  
2. I huvudet på **Invt. På sidan Inleverans väljer du lagerstället i fältet** Lagerställekod **och** fyller sedan i de återstående fälten efter behov.
3. På snabbfliken **Rader** i fältet **Artikel** välj inventeringsartikel. Skriv det antal artiklar som ska läggas till i fältet **Kvantitet**.
4. Så här skriver du ut en **lagerinleveransrapport** från Invt **. På sidan Inleverans** väljer du **åtgärden Skriv ut** .

Följande funktioner finns på **Invt. Kvitto** sida:

- Välj åtgärderna **Frisläpp** eller **Öppna igen** för att ange status för nästa bearbetningssteg.  
- Välj åtgärden **Bokför** för att bokföra lagerinleveransen, eller välj **Bokför och skriv ut** för att bokföra inleveransen och skriva ut test rapporten.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Skriva ut lagerdokument

Du kan ange vilka rapporter som ska skrivas ut i olika etapper genom att välja något av följande alternativ i fältet **Användning** på sidan **Rapportval – lager**:

* Lagerinleverans
* Lagerutleverans
* Bokförd lagerinleverans
* Bokförd lagerutleverans

> [!NOTE]
> Vilka rapporter som finns kan variera beroende på landets/regionens lokalisering. Basprogrammet innehåller inga layouter.

## Se även

[Räkna, justera och gruppera om lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md)    
[Arbeta med serie- och partinummer](inventory-how-work-item-tracking.md)    
[Lagersaldo](inventory-manage-inventory.md)    
[Warehouse Management – översikt](design-details-warehouse-management.md)    
[Försäljning](sales-manage-sales.md)    
[Inköp](purchasing-manage-purchasing.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

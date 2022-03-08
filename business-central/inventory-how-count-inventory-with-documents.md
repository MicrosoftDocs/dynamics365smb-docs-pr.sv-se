---
title: Beräkna lager med dokumentbaserad funktion | Microsoft Docs
description: Beskriver hur du utför en cyklisk inventering av lagret med sidorna Inventeringsorder och Inventeringsregistrering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: ae40390d2aa095739154a635c0e4fdf77933e648
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782124"
---
# <a name="count-inventory-using-documents"></a>Beräkna lager med hjälp av dokument
Du kan göra en fysisk inventering av artiklar med hjälp av inventeringsorder och inventeringsregistreringsdokument. Sidan **inventeringsorder** används för att ordna de fullständiga inventeringar, till exempel en per lagerställe. Sidan **registrering av fysiskt lager** används för att kommunicera och samla in faktiska inventeringen av artiklar. Du kan skapa flera inspelningar av en order, till exempel för att fördela grupper av artiklar till olika medarbetare.

Rapporten **registrering av fysiskt lager** kan skrivas ut från varje inspelning och innehåller tomma antalsfält för att ange det inventerade faktiska lagersaldot. När en användare gör inventering och kvantiteterna som anges på sidan **omkodning av fysiskt lager** väljer du åtgärden **Slutför**. Detta överför kvantiteterna till dessa rader på sidan **inventeringsorder**. Funktionen garanterar att inget artikelantalet kan registreras två gånger.      

> [!NOTE]
> Den här proceduren beskriver hur du utför en inventering med dokument, en metod som ger mer kontroll och stöder distribution av inventeringen till flera medarbetare. Du kan också utföra aktiviteten med hjälp av journaler, sidorna **Inventeringsjournaler** och **Dist.lager inventeringsjournaler**. Mer information finns i [Inventera, justera och gruppera om lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).<br /><br />
> Observera att om du använder funktionen för lagerplatser eller zoner, får du inte använda inventeringsorder. Använd i stället **Sist.lag. inventeringsjournal** för att räkna distributionslagertransaktionerna innan du synkroniserar dem med artikeltransaktioner.

Inventering med dokument består av följande övergripande åtgärder:

1. Skapa en inventeringsorder med förväntade artikelkvantiteter som fylls i automatiskt.
2. Skapa minst en inventeringsregistrering från ordern.
3. Ange antalet räknade artiklar på registreringarna som anges på utskrifter, till exempel och anger värdet till **avslutad**.
4. Slutför och bokför inventeringsordern.

## <a name="to-create-a-physical-inventory-order"></a>Skapa en inventeringsorder
En inventeringsorder är ett fullständigt dokument som består av en inventering i orderhuvudet och vissa rader för orderinventering. Informationen i inventeringshuvudet beskriver hur du gör en inventering. Inventeringsorderraderna innehåller information om artiklarna och var de finns.

Om du vill skapa inventeringsorderrader kan du använda funktionen **beräkna rader** för att återspegla det aktuella lagret som rader på ordern. Alternativt kan du använda funktionen **Kopiera från dokument** för att fylla i raderna med innehållet i en annan öppen eller bokförd inventeringsorder. Nedan beskrivs endast hur du använder funktionen **beräkna rader**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventeringsorder** och välj sedan tillhörande länk.
2. Välj åtgärden **Ny**.
3. Fyll i de fält som krävs på snabbfliken **Allmänt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj åtgärden **Beräkna rader**.
5. Välj alternativ om det behövs.
6. Ange filter, till exempel för att endast ta med en delmängd av artiklar som ska beräknas med den första registreringen.

    > [!TIP]
    > Du kan planera för flera medarbetare att beräkna inventering genom att ange olika filter varje gång du använder åtgärden **beräkna rader** för att endast fylla i ordern med en delmängd av lagerartiklar som en användare kommer att registrera. När du skapar flera registreringar för fysiskt lager för flera anställda minimerar du risken för att räkna artiklar två gånger. Mer information finns i avsnittet "Så här skapar du en inventeringsregistrering".

7.  Välj **OK**.

En rad för varje artikel som finns på den valda platsen och ange filter och alternativ som skrivs på ordern. För artiklar som har ställts in för artikelspårning markeras kryssrutan **använda artikelspårning** och information om den förväntade kvantiteten av serie- och partinummer finns genom att välja åtgärden **rader** och **Artikelspårningsrader**. Mer information finns i avsnittet ”Hantera artikelspårning vid inventering”.

Du kan nu fortsätta med att skapa en eller flera registreringar som är instruktioner till anställda som utför den faktiska inventeringen.  

## <a name="to-create-a-physical-inventory-recording"></a>Skapa en inventeringsregistrering
För varje inventeringsorder kan du skapa en eller flera inventeringsregistreringsdokument där personalen anger inventerade kvantiteter manuellt eller genom en integrerad skanner.

Som standard skapas en registrering för alla rader på relaterad inventeringsorder. Undvika att två anställda räknar samma artiklar vid fördelad räkning, är det lämpligt att gradvis fylla i inventeringsordern genom att ange filter för batch-jobbet **beräkna rader** (se avsnittet ”om du vill skapa en inventeringsorder”) och sedan skapa det fysiska lagret, registrera medan du markerar kryssrutan **Bara rader som inte finns i registreringar**. Den här inställningen ser till att varje ny registrering du skapar endast innehåller olika artiklar än de på andra registreringar.

Vid manuell beräkning, kan du skriva ut en lista, rapporten **Inventeringsregistrering** som har en tom kolumn att skriva inventerade kvantiteter i. När inventeringen är klar anger du kvantiteterna som är registrerade på rader på sidan **Inventeringsregistrering**. Slutligen kan du överföra registrerade kvantiteter till relaterade inventeringsordern genom att sätta status på **avslutad**.

1. På sidan **inventeringsorder** som innehåller rader för artiklarna som ska räknas i en registrering väljer du åtgärden **göra nya registreringar**.
2. Välj alternativ och ange filter efter behov.
3. Välj **OK**.

    Ett inventeringsregistreringsdokument skapas.

4. För varje uppsättning artiklar som ska inventeras, läs in dem på den relaterade inventeringsordern och upprepa steg 1 till 3 med kryssrutan **Bara rader som inte finns i registreringar** markerad.

5. Välj åtgärden **registreringar** för att öppna sidan **Inventeringsregistreringslista**.
6. Öppna relevant registrering.
7. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
8. För artiklar som använder artikelspårning skapar du ytterligare en rad för varje partinummer eller serienummer genom att välja åtgärd **funktion** och åtgärd **kopiera rad**. Mer information finns i avsnittet ”Hantera artikelspårning vid inventering”.    
9. Välj åtgärden **Skriv ut** för att förbereda fysiska dokumentet som anställda ska använda för att anteckna inventerade kvantiteter.

## <a name="to-finish-a-physical-inventory-recording"></a>Slutför en inventeringsregistrering
När medarbetare har inventerat lagerkvantiteter, måste du förbereda att registrera dem i systemet.

1. Från sidan **Inventeringsregistreringslista** markera inventeringsregistrering som du vill slutföra och klicka på åtgärden **redigera**.
2. På snabbfliken **rader** fyller du i faktiska räknade kvantiteten i fältet **antal** för varje rad.
3. För artiklar med serie- eller partinummer (kryssrutan **använd artikelspårning** är markerad), anger du kvantiteterna på särskilda raderna för artikelns serienummer och partinummer respektive fråga. Mer information finns i avsnittet ”Hantera artikelspårning vid inventering”.
4. Markera kryssrutan **registrerad** på varje rad.
5. När du har angett alla data för en inventeringsregistrering, väljer du åtgärden **slutför**. Observera att alla rader måste ha kryssrutan **registrerad** markerad.

> [!NOTE]
> När du är klar med en inventeringsregistrering överförs varje rad till raden på relaterad inventeringsorder som exakt matchar det. För att matcha måste värdena i fälten **Artikelnr**, **Variantkod**, **Platskod** och **Lagerställekod** vara samma för registrering och orderraderna.<br /><br />
> Om det inte finns några matchande inventeringsorderrad och om kryssrutan **Tillåt registrering utan order** är markerad och en ny rad infogas automatiskt och kryssrutan **Registrerade utan order** markeras på den relateradeinventeringsorderraden. I annat fall visas ett felmeddelande och processen avbryts.<br /><br />
> Om mer än en inventeringsregistreringsrad matchar en inventeringsorderrad, visas ett meddelande och processen avbryts. Om du av någon anledning har två identiska inventeringsrader på inventeringsordern använder du en funktion för att lösa problemet. Mer information finns i avsnittet "Så här hittar du dubbla inventeringsorderrader".

## <a name="to-complete-a-physical-inventory-order"></a>Slutför en inventeringsorder
När du är klar med inventeringsregistrering uppdateras på fältet **inspelning av antal (bas)** på relaterade inventeringsordern med de inventerade (registrerade) värdena och kryssrutan **på registrera** är markerad. Om beräknade värdet skiljer sig från der förväntade visas skillnaden i fältet **Positivt antal (bas)** och **Negativt antal**.

För att visa förväntade kvantiteter och alla registrerade avvikelser för artiklar med artikelspårning väljer du åtgärden **rader** och väljer sedan åtgärden **Artikelspårningsrader** för att välja olika vyer för serienummer och partinummer i den inventeringen.

Du kan även välja differensen för **Differens för inventeringsorder** åtgärd för att visa eventuella skillnader mellan förväntat antal och inventerat antal.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Hitta dubbla inventeringsorderrader

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventeringsorder** och välj sedan tillhörande länk.
2. Öppna den inventeringsorder som du vill visa dubbla rader för.
3. Välj åtgärd **visa dubblettrader**.

Dubbla inventeringsorderraderna visas så att du kan ta bort dem och endast en rad med en unik uppsättning värden i fälten **Artikelnr**, **Variantkod**, **Platskod** och **Lagerställekod**.

### <a name="to-post-a-physical-inventory-order"></a>Bokför en inventeringsorder
När du har slutfört en inventeringsorder och ändrar dess status till **avslutad**, kan du bokföra den. Du kan bara ange produktionsorderstatusen från inventeringen till **avslutad** om följande gäller:

- Alla relaterade inventeringsregistreringar har statusen **avslutad**.
- Varje inventeringsorderrad har inventerats av minst en inventeringsregistreringsrad.
- Kryssrutan **På registrerade rader** och **Beräknat förväntat antal** har markerats för alla inventeringsorderrader.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inventeringsorder** och välj sedan tillhörande länk.
2. Markera den inventeringsorder som du vill slutföra och välj sedan åtgärden **Redigera**.

    På sidan **inventeringsorder** visar du den kvantitet som finns i fältet **Ant. registrerade (bas)**.
3. Välj åtgärden **Slutför**.

    Värdet i fältet **Status** ändras till **avslutad** och du kan nu bara ändra ordningen genom att först välja åtgärden **öppna igen**.
4. Välj åtgärden **Bokför** och välj sedan knappen **OK** för att bokföra ordern.

De involverade artikeltransaktionerna uppdateras tillsammans med alla relaterade artikelspårningstransaktionerna.

### <a name="to-view-posted-physical-inventory-orders"></a>För att visa bokförda inventeringsorder
När du har bokfört inventeringsordern kommer den att tas bort och du kan visa och utvärdera dokumentet som en bokförd inventeringsorder inklusive dess inventeringsregistreringar och eventuella kommentarer som har skapats.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda inventeringsorder** och välj sedan tillhörande länk.
2. På sidan **Bokförda inventeringsorder** markera bokförda ordern som du vill visa och välj sedan åtgärden **visa**.
3. För att visa en lista över relaterade inventeringsregistreringar väljer du åtgärden **registreringar**.

## <a name="handling-item-tracking-when-counting-inventory"></a>Hantera artikelspårning vid inventering
Artikelspårning tillhör serie- eller partinummer som har tilldelats artiklarna. Vid inventering av en artikel i lagret som, till exempel 10 olika partinummer ska den anställde kunna registrera vilka och hur många enheter av varje partinummer som finns i lager. Mer information om funktionen för artikelspårning finns i [Så här arbetar du med serienummer och partinummer](inventory-how-work-item-tracking.md).

Kryssrutan **använda artikelspårning** på inventeringsorderrader väljs automatiskt om artikelspårningskoden har ställts in för artikeln, men du kan också markera eller avmarkera den manuellt.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Exempel - Förbered en inventeringsregistrering för en artikelspårad artikel
Beakta inventeringsperioden för artikel A, som finns i lager som tio olika serienummer.
1. På registreringsraden för artikeln väljer du kryssrutan **använda artikelspårning**.
2.  Välj fältet **serienr**, markera det första serienumret som finns i lager för artikeln och välj sedan knappen **OK**.

    Fortsätt att kopiera raden för den första artikelspårade artikeln för att infoga extra rader som motsvarar antalet serienummer i lagret.

3. Välj åtgärd **funktion** och sedan åtgärd **kopia raden**.
4. På sidan **Kopiera inventeringsregistreringsrad**, ange 9 i fältet **Antal kopior** och välj sedan **OK**.
5. På första kopiaraderna väljer du fältet **serienr** och markerar nästa serienumret för artikeln.
6. Upprepa steg 5 för de återstående åtta serienummer, och se till att du inte väljer samma.
7. Välj åtgärden **Skriv ut** för att förbereda utskrifter som anställda ska använda för att anteckna inventerade artiklar och serie-/partinummer.

Observera att rapporten **Inventeringsregistrering** innehåller tio rader för artikel A, en för varje löpnummer.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Exempel – registrera och bokföra inventerat partinummeravvikelser
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

På sidan **inventeringsorder** innehåller fältet **Neg. antal (bas)** *8*. För den aktuella raden innehåller sidan **Artikelspårningslista för inventering** positiva eller negativa kvantiteter för det enskilda partinummer.

## <a name="see-also"></a>Se även
[Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md)  
[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)  
[Lager](inventory-manage-inventory.md)  
[Lagerstyrning](warehouse-manage-warehouse.md)    
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

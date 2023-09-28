---
title: Plocka artiklar för utleverans från dist.lager
description: Lära dig hur du använder distributionslagerplockdokument för att skapa och arbeta plocknings information innan du bokför distributionslagerutleveransen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment"></a>Plocka artiklar för utleverans från dist.lager

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du plocka och inleverera artiklar och använda någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|Utgående process|Begär plockning|Kräv utleverans|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument|Aktiverat||Grundläggande: Order för order|  
|A|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument||Aktiverat|Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument|Aktiverat|Aktiverat|Avancerat|  

Läs mer i [Avgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).

I denna artikel hänvisas till metod D i tabellen. För att lära dig mer om leverera artiklar, gå till [leverera artiklar](warehouse-how-ship-items.md).

När Lagerställe är inställt på att begära plockningsbearbetning så väl som utleveransbearbetning använder du plockningsdokumenten för att skapa och bearbeta plockningsinformationen innan du bokför Lagerutleveransen.  

Du kan inte skapa de distributionslagerplockdokument från början. Plockning är en del av ett arbetsflöde där en person som bearbetar order skapar dem med en pushmetod, eller som skapar lagerpersonalen på en pullmetod:

- För push-metoden där du använder åtgärden **Skapa plockning** på sidan **Distributionslagerutleverans**. Välj raderna att plockas och förbered plockningar genom att till exempel ange vilka fack som ska tas från och placeras i, och hur många enheter som ska hanteras. Lagerplatser kan fördefinieras för distributionslagerstället eller resurs.
- När du använder åtgärden **Frisläpp** på sidan **Distributionslagerutleverans** för att göra artiklarna tillgängliga för plockning. På sidan **Plockningskalkylark** kan distributionslagerpersonal använda åtgärden **Hämta dist.lager dokument** för att hämta sina tilldelade plockningar.

> [!NOTE]  
> Plockning för distributionslagerutleverans av artiklar som är monterade till försäljningsorder, följer samma steg för distributionslager för utleverans, enligt beskrivningen i den här artikeln. Numret på plockningsrader per antal som ska levereras kan vara många-till-en, eftersom plockning för distributionslager är för monteringskomponenter och inte för monteringsartikeln.  
>
> Distributionslagerplockningsrader skapas för värdet i fältet **Återstående antal** på raderna i monteringsorder som är kopplad till försäljningsorderraden som levereras. Alla komponenter kan plockas i en åtgärd. Läs mer på [Hantera artiklar för montering mot kundorder i distributionslagerutleveranser](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Information om hur du plockar komponenter för monteringsorder, inklusive situationer där monteringsartikeln inte är relaterad till en försäljningsutleverans, se [Plocka för montering eller projekt i avancerad distributionslagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Så här skapar du plockningsdokumenten i bulk med plockningskalkylarket

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Plockningskalkylark** och väljer sedan relaterad länk.  

2. Välj åtgärden **Hämta dist.lager dokument**.  

    Listan innehåller alla utleveranser som har släppts för plockning, inklusive de för vilka plockningsinstruktioner redan har skapats. Dokument med plockningsrader som är helt plockade och registrerade visas inte i den här listan.  
3. Välj de utleveranser som du vill förbereda en plockning för.

    > [!NOTE]  
    >  Om du försöker välja ett inleverans- eller internt plockningsdokument, som du redan har skapat instruktioner för, för alla dess rader får du ett meddelande att det inte finns någonting att hantera. För att kombinera plockningsinstruktioner för lagret som du redan har skapats måste du ta bort de enskilda distributionslagerplockningarna förs.

4. Fyll i fältet **Sorteringsmetod** för att sortera raderna.  

    > [!NOTE]  
    >  Hur raderna sorteras i förslaget överförs inte automatiskt till plockningsinstruktionen. Samma möjligheter till sortering och lagerplatsordning finns. Du kan enkelt återskapa radorder du planerar i kalkylbladet när du skapar plockningsinstruktionerna eller genom att sortera i plockningsinstruktionerna.

5. Fyll i fältet **Ant. att hantera** antingen manuellt eller genom att använda åtgärden **Fyll i auto. ant. att hantera**.  

    På sidan visas de tillgängliga kvantiteterna för lagerplatser för direktutleverans. Denna information är användbar när du planerar arbetstilldelningar i direktutleveranser. [!INCLUDE[prod_short](includes/prod_short.md)] föreslår alltid en plockning från en lagerplats för direktutleverans först.
6. Du kan redigera raderna efter behov. Du kan också ta bort rader för att skapa en välja mer effektivt. Om det till exempel finns rader med artiklar på lagerställen för direktutleveranser kanske du vill skapa en plockning för alla rader. Artiklarna för direktutleverans utlevereras med övriga artiklar i utleveransen, och lagerställena för direktutleveranser får därmed plats för fler inkommande artiklar.  

    > [!NOTE]  
    >  När du tar bort rader tas de bara bort från det här kalkylbladet. De tas inte bort från urvalslistan för plockning.  

7. Välj åtgärden **Skapa plockning**. Sidan **Skapa plockning** öppnas, där du kan lägga till mer information plockningen du skapar. Ange hur plockrader ska kombineras i plockdokumentet genom att välja ett av följande alternativ.  

    |Alternativ|Beskrivning|
    |-|-|
    |Per dist.lagerdokument Dokument|Skapa separata plockningsdokument för kalkylarksraderna med samma distributionslagerkälldokumentet.|
    |Per Kund/Lev./Lagerst.|Skapa separata plockningsdokument för varje kund (försäljningsorder), leverantören (inköpsreturorder) och lagerställe (överföringsorder).|
    |Per artikel|Skapa separata plockningsdokument för varje artikel i plockningsförslaget.|
    |Per från zon|Skapa separata plockningsdokument för varje zon som du tar artiklarna från.|
    |Per lagerplats|Skapa separata plockningsdokument för varje lagerplats som du tar artiklarna från.|
    |Per förfallodatum|Skapa separata plockningsdokument för källdokument som har samma förfallodatum.|

    Ange hur plockningsdokument skapas genom att välja bland följande alternativ.

    |Alternativ|Beskrivning|
    |-|-|
    |Max. Nr. av plockningsrader|Skapar plockningsdokument som inte har fler än radnummer än som ställts in i varje dokument.|
    |Max. Nr. av plock.källdok.|Skapar plockningsdokument som inte täcker fler än antalet källdokument som ställts in.|
    |Tilldelat användar-ID|Skapar plockningsdokument enbart för förslagsrader som tilldelats den valda lagerpersonalen.|
    |Sorteringsmetod för plock.rader|Välja bland de tillgängliga alternativen för att sortera rader i den nya plockningsdokumentet.|
    |Sätt brytenhetsfilter|Döljer mellanliggande plockningsrader för brytenheter när en större måttenhet konverteras till en mindre måttenhet och plockas helt.|
    |Fyll inte i ant. att hantera|Lämnar fältet Ant. att hantera tomt på de skapade plockningsraderna.|
    |Skriv ut plockning|Skriver ut plockningsdokumenten, när de skapas. Du kan även skriva ut från skapade plockningsdokumenten.|

8. Välj **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] skapar plockningen enligt dina val.  

## <a name="to-pick-items-for-a-warehouse-shipment"></a>Så här plocka artiklar för utleverans

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Distributionslagerplockningar** och väljer sedan relaterad länk.  

    Om du vill arbeta med en viss plockning väljer du plockningen från listan eller filtrerar listan för att söka efter de plockningar som specifikt har tilldelats dig. Öppna plockningskortet.  
2. Om **Tilldelat användar-ID** är tomt, anger du ID för att identifiera själv om det behövs.  
3. Plocka artiklar.  

    Om distributionslagret har konfigurerats att använda lagerställen, då artikelns standardlagerställen används för att föreslå var du vill hämta artiklar från. Instruktionerna innehåller minst två separata rader för Ta och placera-åtgärder.  

    Om lagret är distributionslager för att använda riktad borttagning och plockning, används lagerplatsordning för att beräkna de bästa lagerplatserna att plocka från. Dessa lagerplatser föreslås på plockningsraderna. Instruktionerna innehåller minst två separata rader för Ta och placera-åtgärder.  

    * Den första raden, med **Ta** i fältet **Åtgärdstyp**, anger var artiklarna finns i inleveransområdet. Om du skickar ett stort antal artiklar på en utleveransraden, kanske du måste plocka artiklarna i flera lagerplatser, så det finns en Ta-rad för varje lagerplats.
    * Nästa rad, med fältet **Plats** i **Åtgärdstyp**, anger var du måste placera artiklarna i distributionslager. Du kan inte ändra zon- och lagerplatsfältet på den här raden.

    > [!NOTE]
    > Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om den utsedda lagerplatsen är full, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.

4. När du har utfört plockningen och placerat artiklarna i utleveransområdet eller på lagerstället för utleveranser väljer du åtgärden **Registrera plockning**.  

Du kan nu ta artiklarna till leveransdockan och bokföra leveransen, inklusive relaterade källdokumentet, på sidan **Distributionslagerutleverans**. Läs mer på [utleverera artiklar](warehouse-how-ship-items.md).

## <a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

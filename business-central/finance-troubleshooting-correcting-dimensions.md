---
title: Felsökning och korrigering av dimensioner
description: Lär dig hur du felsöker vanliga dimensionsfel och hur du korrigerar dimensioner när de har använts på bokförda transaktioner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Felsökning och korrigering av dimensioner

Ekonomiska rapporter och analysvyer bygger ofta på data från dimensioner. Trots de säkerhetsåtgärder som finns tillgängliga inträffar ibland ett misstag som kan medföra felaktigheter. Den här artikeln beskriver några typiska fel och hur du korrigerar dimensionstilldelningar för bokförda transaktioner så att ekonomiska rapporter är korrekta.

## Felsökning av dimensionsfel

När du bokför dokument eller journalrader som innehåller dimensioner kan olika fel uppstå. De är emellertid vanligtvis relaterade till en felaktig dimensionsinställning eller tilldelning.

> [!NOTE]
> I följande lista över möjliga felmeddelanden fungerar *%X*-koder som platshållare för datavariabler som det faktiska meddelandet innehåller i användargränssnittet beroende på sammanhanget. Till exempel *%1 %2 är spärrad.* kan visas i användargränssnittet som ”dimensionskodsområde är spärrat”.  

|Problem|Felmeddelande|Möjlig lösning|
|-----|-------------|-----------------|
|Spärrad dimension|%1 %2 är spärrad.|-Sök efter icke-bokförda dokument som innehåller dimensionsuppsättningen med den spärrade dimensionen och lås upp den.<br />-Ta bort dimensionsuppsättningen för den spärrade dimensionen.|
|Borttagen dimension|%1 %2 kan inte hittas.|-Återställ den saknade dimensionen.<br />-Sök efter icke-bokförda dokument som innehåller dimensionsuppsättningen med den saknade dimensionen och lägg till den.<br />-Ta bort dimensionsuppsättningen för den saknade dimensionen.|
|Spärrat dimensionsvärde|%1 %2 – %3 är spärrad.|-Sök efter icke-bokförda dokument som innehåller dimensionsuppsättningen med det spärrade dimensionsvärdet och lås upp det.<br />-Ta bort dimensionsuppsättningsraden för det spärrade dimensionsvärdet.|
|Borttaget dimensionsvärde|    %1 för %2 saknas.|-Återställ det saknade dimensionsvärdet.<br />-Sök efter icke-bokförda dokument som innehåller dimensionsuppsättningen med det saknade dimensionsvärdet och lägg till det.<br />-Ta bort dimensionsuppsättningen för den saknade dimensionsvärdet.|
|Otillåtet dimensionsvärde|Dimensionsvärdetypen för %1 %2 – %3 får inte vara %4.|-Ändra fältet **dimensionsvärdetyp** på sidan **dimensionsvärden** till **Standard** eller **Från-summa**.<br />-Ta bort dimensionsuppsättningsraden för det spärrade dimensionsvärdet.|
|Blockerad dimensionskombination|Dimensioner %1 och %2 kan inte användas samtidigt.|-Sök efter icke-bokförda dokument som innehåller dimensionsuppsättningen med det spärrade dimensionskombinationen och lås upp det.<br />-Ändra någon av de motstridiga behörighetsuppsättningsraderna för dimensionskombinationen.|
|Blockerad dimensionskombination|Dimensionskombinationerna %1 – %2 och %3 – %4 kan inte användas samtidigt.|-Sök efter icke-bokförda dokument som innehåller dimensionsuppsättningen med det spärrade dimensionsvärdet och lås upp det.<br />-Ändra någon av de motstridiga behörighetsuppsättningsraderna för dimensionsvärdeskombinationen.|
|Tom dimensionsvärdekod för standarddimensionen när fältet **värdebokföring** innehåller **Kod alltid**|-Välj %1 för %2 %3.<br />-Välj %1 för %2 %3 till %4 %5.|-Ändra fältet **värdebokföring** på sidan **standarddimension**.<br />-Ange ett icke tomt dimensionsvärde för dimensionen som är i konflikt i dimensionsuppsättningen.|
|Fel dimensionsvärdekod för standarddimensionen när fältet **värdebokföring** innehåller **Samma kod**|-Välj %1 %2 för %3 %4.<br />-Välj %1 %2 för %3 %4 till %5 %6.|-Ändra fältet **värdebokföring** på sidan **standarddimension**.<br />-Ange krävt dimensionsvärde för dimensionen som är i konflikt i dimensionsuppsättningen.|
|Icke-tomt dimensionsvärdekod för tomma standarddimensionen när fältet **värdebokföring** innehåller **Samma kod**|-%1 %2 måste vara tom.<br />-%1 %2 måste vara tom för %3 %4.|-Ändra fältet **värdebokföring** på sidan **standarddimension**.<br />-Ange en icke tom dimensionsvärdekod för dimensionen som är i konflikt i dimensionsuppsättningen.|
|Oväntat dimensionsvärde för standarddimensionen när fältet **värdebokföring** innehåller **Ingen kod**|-%1 %2 får inte tas med.<br />.%1 %2 får inte tas med för %3 %4.|-Ändra fältet **värdebokföring** på sidan **standarddimension**.<br />-Ta bort raden i konflikt från dimensionsuppsättningen.|
|En dimensionskorrigering slutförs inte korrekt.||-Välj **Återställ** om du vill återställa korrigeringen till ett utkasttillstånd. Detta återställer ändringarna och du kan köra korrigeringen igen.|

## Ändra dimensionstilldelningar efter bokföring

Om du upptäcker att en felaktig dimension har använts på bokförda redovisningstransaktioner kan du korrigera dimensionsvärdena och uppdatera analysvyerna. Korrigeringen hjälper till att hålla dina ekonomiska rapporter och analyser korrekta.

> [!IMPORTANT]
> Funktionerna för att korrigera dimensioner är endast avsedda att hjälpa till att göra den ekonomiska rapporten korrekt. Dimensionskorrigeringar gäller bara för redovisningstransaktionerna. De ändrar inte de dimensioner som tilldelats poster i andra redovisningar för samma transaktion. De dimensioner som tilldelats i redovisningen och underredovisningarna visas som en avvikelse.

### Ställa in dimensionskorrigeringar

Det finns två saker att tänka på när du ställer in dimensionskorrigeringar:

* Finns det dimensioner som du inte vill tillåta att människor ändrar? På sidan **Inställningar för dimensionskorrigering** ange de dimensioner som du vill blockera för ändringar.
* Vem kan ändra globala dimensioner? Om du vill tillåta personer att göra ändringar tilldelar du behörigheten **D365 DIM CORRECTION** till användarna. Behörigheterna gör det möjligt för dem att skapa dimensionskorrigeringar, köra dem och ångra dem om det behövs. De kan också ange blockerade dimensioner. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md). 

### Korrigera en dimension

Du kan manuellt välja en eller flera redovisningstransaktioner eller använda filter för att välja uppsättningar med transaktioner. Om det behövs kan du också lägga till eller ta bort dimensioner. 

1. Om du vill starta en dimensionskorrigering använder du en av följande sidor:

    * På sidan **GL/Register** genom att välja ett register och sedan välja åtgärden **Korrigera dimensioner**. Denna åtgärd startar en korrigering av transaktionerna i den valda registret.
    * På sidan **Redovisningstransaktioner** genom att välja åtgärden **Dimensionskorrigering**. 

2. I fältet **Beskrivning**, ange information om ändringen. Andra personer kan använda den här informationen senare för att förstå vad som gjordes.
3. Välj snabbfliken **Valda transaktioner**, välj relevanta transaktioner.

    > [!IMPORTANT]
    > När du ändrar en markering återställs värdena på snabbfliken **Ändringar av dimensionskorrigering**. Markera därför alltid transaktionerna innan du anger ändringar av dimensionsvärde.

   Alternativen beskrivs i tabellen nedan.

   |Alternativ  |Beskrivning  |
   |---------|---------|
   |Lägg till relaterade transaktioner     |Lägg till redovisningstransaktioner som finns i samma redovisningsregister.|   
   |Lägg till efter filter     |Använd filtervillkor när du lägger till redovisningstransaktioner.|
   |Manuellt val     |Välj specifika redovisningstransaktioner.         |
   |Lägg till per dimensioner     |Filtrera redovisningstransaktioner efter dimensioner.         |
   |Ta bort poster     |Avmarkera redovisningstransaktioner         |
   |Hantera urvalskriterier     |Håll reda på urvalsprocessen och ångra markeringar om det behövs.         |

4. På snabbfliken **Ändringar av dimensionskorrigering** välj den dimension som du vill ändra fältet **Dimensionskod** och det nya värdet **Ny dimensionsvärdekod**.
5. Om du vill verifiera korrigeringen väljer du **Validera dimensionsändringar**. Mer information finns i [Validera dimensionskorrigeringar](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Välj **Kör**.

### Validera dimensionskorrigeringar

Innan du kör en korrigering är det en bra idé att validera den först. Valideringen söker efter begränsningar för värdebokföring för redovisningskontona, begränsningar för dimensioner och om dimensionsvärdena är blockerade. Under valideringen anges statusen för korrigeringen till **Validering i process**. När du har validerat en korrigering visas resultatet i fältet **Valideringsstatus**. Om fel hittades kan du använda åtgärden **Visa fel** för att undersöka dem. När du har korrigerat ett fel måste du använda åtgärden **Öppna igen** för att köra korrigeringen eller en ny validering.

Du kan antingen köra en korrigering omedelbart eller schemalägga den så att den körs en senare gång. Om du kör korrigeringar på en stor datauppsättning rekommenderar vi att du schemalägger den så att den körs utanför arbetstid. Mer information finns i [Dimensionskorrigeringar på stora datauppsättningar](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### Ångra en korrigering

När du har korrigerat en dimension kan du använda åtgärden **Ångra** om du inte gillar det du ser för att återställa föregående värde. Du kan dock bara ångra den senaste korrigeringen. Innan du ångrar en korrigering kan du validera de ändringar som kan resultera från åtgärden ångra. Validering är till exempel användbart om dimensionsbegränsningarna har ändrats efter korrigeringen.

Om Ångra-åtgärden inte är tillgänglig, till exempel för att du har gjort många korrigeringar, kan du använda åtgärden **Kopiera till utkast** för att starta en ny korrigering för samma poster.

### Dimensionskorrigeringar på stora datauppsättningar

Var försiktig när du korrigerar stora uppsättningar poster, till exempel uppsättningar som innehåller mer än 10 000 poster. Om du kan rekommenderar vi att du använder filtren för att köra korrigeringarna på mindre datauppsättningar. Det är också en bra idé att köra korrigeringar utanför de normala öppettiderna. 

### Använda analysvyer med dimensionskorrigeringar

Om **Uppdatera vid bokföring** är aktiverat för en analysvy, [!INCLUDE[prod_short](includes/prod_short.md)] kan uppdateringen visa när dokument och tidskrifter publiceras. Du kan också uppdatera vyer med den här inställningen aktiverad med resultat av dimensionskorrigeringar. Det gör du genom att aktivera växlingsknappen **Uppdatera analysvyer**. Uppdatering av analysvyer kan påverka prestanda, särskilt för stora datauppsättningar, så vi rekommenderar att du uppdaterar analysvyer endast för små datauppsättningar.  

### Visa historiska dimensionskorrigeringar

Om en redovisningstransaktion har korrigerats kan du undersöka ändringen med hjälp av åtgärden **Historik för dimensionskorrigeringar**.

### Hantera ofullständiga korrigeringar

Om en korrigering inte slutförs visas en varning på korrigeringskortet. Om detta inträffar kan du använda åtgärden **Återställning** för att återställa korrigeringen till ett utkast till status och ångra ändringarna. Du kan sedan köra korrigeringen igen.

> [!NOTE]
> Återställning av en ofullständig korrigering påverkar inte uppdateringar av analysvyer eftersom de sker i slutet av korrigeringsprocessen.

### Använda kostnadsredovisning med korrigerade redovisningstransaktioner

När du har korrigerat dimensioner kommer dina data för kostnadsredovisning inte att vara synkroniserade. Kostnadsredovisning använder dimensioner för att aggregera belopp för kostnadsställen och kostnadsbärare och för att köra kostnadsallokeringar. Om du ändrar dimensioner för redovisningstransaktioner innebär det förmodligen att du kör dina kostnadsredovisningsmodeller igen. Beroende på vilka data som har uppdaterats och hur dina funktioner för kostnadsredovisning har ställts in kan du behöva göra följande:

* Ta bara bort några kostnadsregister och kör om fördelningar.
* Ta bort allt och kör alla dina modeller igen.

Du miste manuellt identifiera var dimensionskorrigeringar kommer att påverka kostnadsredovisningen och var uppdateringar behövs. [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller för närvarande inte ett automatiserat sätt att göra det.

## Se även

[Arbeta med dimensioner](finance-dimensions.md)  
[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

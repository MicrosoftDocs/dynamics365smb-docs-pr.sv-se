---
title: 'Inleverera, artikelinförsel, flytta, plocka och leverera i avancerad lagerkonfiguration med dirigerad plockning och artikelinförsel'
description: Ankommande och avgående processer kan utföras på olika sätt beroende på lagerkomplexitetsnivå.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration-with-directed-put-away-and-pick"></a>Genomgång av ankommande och avgående flöde i avancerad distributionslagerkonfiguration med dirigerad artikelinförsel och plockning

Den här genomgången visar hur man slutför inkommande och utgående flöden i konfigurationen Avancerad: dirigerad artikelinförsel och plockning. Mer information finns i avsnittet [Översikt över olika konfigurationsalternativ](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Förutsättningar
För att slutföra denna genomgång måste du ange dig själv som distributionslagerpersonal på lagerstället *VIT* med de här stegen:  
1. Välj ![glödlampan som öppnar funktionen Berätta 1.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2. Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
3. Ange WHITE i fältet **Lagerställekod**.  
4. Aktivera **standard** växling.


## <a name="scenario"></a>Scenario
Ellen, lagerchefen använder funktionen för direktutleverera och lagerplatspåfyllning för att öka hastigheten på inleveranser och leveranstid.  

## <a name="steps"></a>Steg

1. Skapa distributionslagerutleverans.  

    1. Välj ![glödlampan som öppnar funktionen Berätta 2.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
    2. Välj order för kund 10000 för lagerstället VIT. Externt ordernr är *W-1*.
    3. Välj åtgärden **Skapa distributionslagerutleverans** för att skapa en distributionslagerutleverans för vald försäljningsorder.
    4. Välj åtgärden **Frisläpp** för att meddela lagret att försäljningsutleverans är klar för lagerhantering.  

2. Definiera lagerplatser för artikeln om du vill kontrollera var den är artikelinförsel 

    1.  Välj ![glödlampan som öppnar funktionen Berätta 3.](../../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.  
    2.  Välj *WRB-1000* och sedan åtgärden **lagerställesinnehåll**.  
    3.  Välj åtgärden **Ny**. Lägg till två rader.
    
    |Artikel|Lagerställekod|Lagerplatskod|Åtgärdat|Måttenhet|
    |----------|----------|---------|---|------|  
    |DIST-1000|VIT|D-05-0001|Ja|PÅSE|  
    |WRB-1000|VIT|D-05-0002|Ja|PÅSE|

3. Skapa dist.lager inleverans.  

    1. Välj ![glödlampan som öppnar funktionen Berätta 4.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
    2. Välj order från leverantör 10000 för lagerstället VIT. Leverantörens ordernr är *W-2*. Använd anpassningsverktygen om fältet **Leverantörens ordernr.** inte visas. Mer information finns i [Anpassa din arbetsyta](../../ui-personalization-user.md).
    3. Välj åtgärden **Skapa dist.lagerinleverans** för att skapa en dist.lagerinleverans för vald inköpsorder.


4. Kontrollera om det finns utgående order som behöver inlevererade artiklar och bokförd inleverans
    1. Välj åtgärden **Beräkna direktutleverans**. Detta fyller i kolumnen **Ant. för direktutlevns**.
    2. Ange 0 i fältet **Ant. för direktutlevns** på raden med artikel *WRB-1000* eftersom du inte tänker packa om på inleveransområdet.
    3. Välj åtgärden **Bokför inleverans**.

5. Registrera dist.lager artikelinförsel
    1. Med ![glödlampan som öppnar funktionen Berätta 5.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Lagerartikelinförsel** och väljer sedan relaterad länk.
    2. Leta upp dokumentet för dist.lager artikelinförsel som har skapats från dist.lager inleverans och öppna det
    3. På sidan **Dist.lager artikelinförsel** granska avsnittet **Rader**

    I det här skedet visas lagerplatsens kapacitetslogik. artikelinförselraderna kommer att ha tre rader för artikeln *WRB-1000*:
    - Ta rad för att flytta inlevererade rader från mottagande lagerstället (W-08-0001)
    - En plats linje som flyttar en PÅSE till en av de konfigurerade fasta lagerplatserna (W-05-0001)
    - En platsrad som flyttar en annan PÅSE till en annan fast lagerplats (W-05-0002). Det beror på att en fast lagerplats inte kan innehålla hela inleveranskvantiteten.

    Eftersom den här artikelinförseln innehåller rader för direktutleveranser visas tre rader för artikeln *WRB-1001*:
    -  Ta rad för att flytta inlevererade rader från mottagande lagerstället (W-08-0001)
    -  En platsrad för 2 på lagerplatsen för direktutleveranser
    -  En platsrad för den återstående kvantiteten på lagerplats

    4. Välj åtgärden **Registrera artikelinförsel**.


6. Definiera plocklagerplatser för artikeln om du vill kontrollera var den plockas från 

    1.  Välj ![glödlampan som öppnar funktionen Berätta 6.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
    2.  Öppna lagerställekortet *VIT*.  
    3.  Välj åtgärden **Lagerplats** på **Lagerställekort**
    4.  Välj lagerplats *W-02-0001* och sedan åtgärden **innehåll**.  
    5.  Välj åtgärden **Ny**.  
    6.  Aktivera **fast** växling.  
    7.  I fältet **Verifikationsnr.** anger du *WRB-1000*. 
    8.  I fältet **Min. ant.** ange *2*. 
    9.  I fältet **Max. ant.** ange *10*. 

    Använd anpassningsverktygen om fältet **Min. ant.** och **Max ant.** inte visas. Mer information finns i [Anpassa din arbetsyta](../../ui-personalization-user.md). 

7. Omorganisera distributionslager genom att flytta artiklar från området för masslagring till området för plockning för att optimera plockningstiden.

    1. Välj ![glödlampan som öppnar funktionen Berätta 7.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transportkalkylark** och väljer sedan relaterad länk
    2. Välj åtgärden **Beräkna lagerplatsåteranskaffning**. 

    Kalkylark för distributionslager med förslag på att flytta artikel *WRB-1000* från området för masslagring till plockningsområdet skapas.

    3. Välj åtgärden **Skapa transport** för att bekräfta att skapa dokumentet.
    4.  Välj ![glödlampan som öppnar funktionen Berätta 8.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagertransporter** och väljer sedan relaterad länk
    5.  Öppna den lagertransport som du har skapat, granska avsnittet **rader**

     I det här skedet visas funktionen för brytenhet. Fyra rader visas:
    - En rad som tar ut den ena PÅSEN från volymlagerplatsen
    - En rad för att placera 48 STYCK tillbaka i lagret på samma lagerplats. 
    - En rad som tar ut 10 STYCK från volymlagerplatsen
    - En rad för att placera 10 STYCK på plockningslagerplatsen

    6.  Välj åtgärden **Registrera transport**.

8. Skapa distributionslagerplockning

    1. Välj ![glödlampan som öppnar funktionen Berätta 9.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Plockningskalkylark** och väljer sedan relaterad länk
    2. Välj åtgärden **Hämta dist.lager dokument**, välj raden för försäljningsordern för kund 10000 och välj sedan knappen **OK** för att fylla i kalkylbladsrader enligt det valda dokumentet.

    3. Kontrollera fältet **Ant. på direktutlevns lagerplats**. 

    4. Välj åtgärden **Skapa plockning**.
    5. Bekräfta vilka plockningsinställningar som behövs, t.ex. växlingen **Per från zon**. Välj **OK**.
    
    Du får ett bekräftelsemeddelande med plockningsnumren. Det finns två plockningar som vissa artiklar i zonen för direktutleveranser, nära leveransområdet och det skulle verka vettigt att bearbeta dem separat.

9.  Registrera dist.lager plockning
    1. Välj ![glödlampan som öppnar funktionen Berätta 10.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Distributionslagerplockningar** och väljer sedan relaterad länk
    2. Leta upp de plockningar du har skapat och öppna den.
    3. Välj **Registrera plockning**.
    4. Upprepa för den andra plockningen

10. Bokför dist.lager utleverans
    
    1. Välj ![glödlampan som öppnar funktionen Berätta 11.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Distributionslagerutleverans** och väljer sedan relaterad länk.
    2. På sidan Distributionslagerutleverans granska avsnittet **Rader**. När lagerplockningen har registrerats uppdateras distributionslagerutleveransen med **Ant. att utleverera** ifylld.
    3. Välj åtgärden **Bokför utleverans**.
    4. Bekräfta alternativet **leverans**.


## <a name="results"></a>Resultat
- **Bokförda inleveranser till distributionslager** skapas
- **Registrerad artikelinförsel för distributionslager** skapas    
- **Bokförd inköpsinleverans** skapas    
- **Inköpsorder** har **Inlevererat antal** uppdaterats för raderna som inlevererats
- **Registrerad dist.lager transport** skapas
- **Registrerad distributionslagerplockning** skapas
- **Bokförd distributionslagerutleverans** skapas
- **Bokförd utleverans** skapades
- **Försäljningsorder** har **Utlevererat antal** uppdaterats för raderna som levererats
- Artikel **lager** ökas med eventuell påminnelse om inte levererats



## <a name="see-also"></a>Se även
[Ta emot artiklar](../../warehouse-how-receive-items.md) 
[Designdetaljer: Inkommande distributionslagerflöde](../../design-details-inbound-warehouse-flow.md) 
[Leverera artiklar](../../warehouse-how-ship-items.md) 
[Plocka artiklar för utleverans från dist.lager](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Designdetaljer: Utgående distributionslagerflöde](../../design-details-outbound-warehouse-flow.md) 
[Visa artikeldisposition](../../inventory-how-availability-overview.md) 

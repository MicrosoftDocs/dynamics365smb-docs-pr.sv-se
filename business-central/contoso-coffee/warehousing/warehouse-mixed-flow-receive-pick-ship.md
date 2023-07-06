---
title: 'Inleverera, artikelinförsel, plocka och leverera blandade distributionslagerkonfigurationer'
description: I Business Central kan de inkommande och utkommande processerna kan att utföras på olika sätt beroende på lagerkomplexitetsnivå.
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a><a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a><a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a>Genomgång av ankommande och avgående flöde i blandade distributionslagerkonfigurationer

Den här genomgången visar hur man slutför inkommande och utgående flöden i blandad konfiguration, där för inkommande flödeslager konfigureras som Grundläggande: order för order och för utgående flöde Avancerad konfiguration används. Mer information finns i avsnittet [Översikt över olika konfigurationsalternativ](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Förutsättningar
För att slutföra denna genomgång måste du ange dig själv som distributionslagerpersonal på lagerstället *GUL* med de här stegen:  
1. Välj ![glödlampan som öppnar funktionen Berätta 1.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2. Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
3. I fältet **Lagerställekod** ange *GUL*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a><a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a><a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Inkommande flöde: Inleverera och införa utflöde i grundläggande lagerkonfigurationer

I [!INCLUDE[prod_short](../../includes/prod_short.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Inleveranser|Artikelinförslar|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|INTER|||2|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument|||X|3|  
|L|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument||X||6-4-5|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](../../design-details-inbound-warehouse-flow.md).  

Efterföljande genomgången visar metod C i föregående tabellen.  

### <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Scenario
Alicia, inköpsagenten, skapar inköpsorder för olika rostade bönor som efterfrågan visas. När den kombinerade leveransen inlevereras till lagret tar Anders, lagerarbetaren emot artiklarna och för in artiklarna. När Anders bokför inleverans, bokförs artiklarna som inlevererade till lagret och som tillgängligt för försäljning eller andra behov.  

### <a name="steps"></a><a name="steps"></a><a name="steps"></a>Steg
1. Ställ in sidan **Lagerställekort** så att den definierar företagets inkommande lagerflöden.  

    1.  Välj ![glödlampan som öppnar funktionen Berätta 2.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
    2.  Öppna lagerställekortet *GUL*.  
    3.  Inaktivera växlingsknappen **Kräver artikelinförsel**.  

2. Frisläpp inköpsorder till lagret.  

    1. Välj ![glödlampan som öppnar funktionen Berätta 3.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
    2. Välj order från leverantör 10000 för lagerstället GUL. Leverantörsordernummer är *Y-1* och *Y-2*. Använd anpassningsverktygen om fältet **Leverantörens ordernr.** inte visas. Mer information finns i [Anpassa din arbetsyta](../../ui-personalization-user.md).
    3. Välj åtgärden **Frisläpp** för att meddela lagret att valda inköpsorder är klara för lagerhantering när leverans anländer.  

3. Skapa den distributionslagerinleverans som ska inlevereras och föras in
    1. Välj ![glödlampan som öppnar funktionen Berätta 4.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Dist.lager inleveranser** och väljer sedan relaterad länk.
    2. Välj åtgärden **Ny**
    3. På sidan dist. lager inleverans trycker du på Retur för att ange att ett lagerinleveransnummer har valts automatiskt
    4. Ange **Lagerställekod** som *GUL*.
    5. Välj **Hämta källdokument...** åtgärden
    6. Välj tidigare släppta inköpsorder från leverantör 10000 och välj **OK**.
        Raderna kommer att innehålla en ny transaktion för varje inköpsorderrad.

4. Justera kvantitet till inleverans baserat på Inlevererat antal och bokför dokument
    1. Välj rad med artikel  *WRB-1000*.
    2. Välj *OVERRCPT10* i fältet **Kod för överinleverans** och ändra värdet i **Antal att inleverera** från *100* till *110*.
    3. Välj rad med artikel  *WRB-1001* och 
    4. På andra raden, ändra värdet i fältet **Antal att inleverera** från *200* till *190*.
    5. Välj åtgärden **Bokför inleverans**.

### <a name="results"></a><a name="results"></a><a name="results"></a>Resultat
 - de rostade bönorna har nu registrerats som artikelinförsel
 - **Bokförda inleveranser till distributionslager** skapas
 - **Bokförd inköpsinleverans** skapas
 - inköpsorder har **Inlevererat antal** uppdaterats för raderna som inlevererats
 - artikel **lager** ökas med det valda antalet
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a><a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a><a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a>Utgående flöde: plockning och leverans i avancerade lagerkonfigurationer

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Plockningar|Utleveranser|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|INTER|||2|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument||X||3|  
|L|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument|||X|6-4-5|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: utgående distributionslagerflöde](../../design-details-outbound-warehouse-flow.md).  

Efterföljande genomgången visar metod D i föregående tabellen.

### <a name="scenario-1"></a><a name="scenario-1"></a><a name="scenario-1"></a>Scenario
Susan, orderhandläggaren, skapar försäljningsorder för olika rostade bönor och skickar den till lagerstället. Eftersom alla order kommer från samma kund, Ellen, kan lagerchefen leverera dem tillsammans. Anders, lagerarbetaren, måste kontrollera att leveransen förbereds och levereras till kunden.

### <a name="steps-1"></a><a name="steps-1"></a><a name="steps-1"></a>Steg
Detta är en fortsättning av [Inkommande flöde: Inleverera och införa utflöde i grundläggande lagerkonfigurationer](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Frisläpp försäljningsorder till lagret.  

    1. Välj ![glödlampan som öppnar funktionen Berätta 5.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
    2. Välj order för kund 10000 för lagerstället GUL. Externa ordernummer *Y-3*, *Y-4* och *Y-5*. Använd anpassningsverktygen om fältet **Externt ordernr.** inte visas. Mer information finns i [Anpassa din arbetsyta](../../ui-personalization-user.md).
    3. Välj åtgärden **Frisläpp** för att meddela lagret att valda försäljningsorder är klara för lagerhantering.  

2. För att leverera artiklar  
    1. Välj ![glödlampan som öppnar funktionen Berätta 6.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Distributionslagerutleverans** och väljer sedan relaterad länk.  
    2. Välj åtgärden **Ny**.  
    3. I fältet **Lagerställekod** ange *GUL*.  
    4. Välj åtgärden **Filter för att hämta urspr.dok.**.  
    5. I fältet **Kod** ange **CUST10000**.  
    6. I fältet **Beskrivning** ange **Kund 10000**.  
    7. Välj åtgärden **Ändra**.  
    8. På snabbfliken **Försäljning** i fältet **Förs.kundnrfilter** anger du *10000*.  
    9. Välj åtgärden **Kör**. 
    
    Distributionslagerutleverans är fylld med fyra rader som representerar försäljningsorderrader för de angivna kunderna. Fältet **Ant. att utleverera** är tomt, eftersom artiklar måste plockas först.

3. Skapa distributionslagerplockningen från distributionslagerutleveransen
    1. På sidan distributionslagerutleverans, välj åtgärden **Skapa plockning**.
    2. Bekräfta vilka plockningsinställningar som behövs, t.ex. markera *artikel* i fältet **Sorteringsmetod för aktivitetsrad** om du vill gruppera samma objekt tillsammans. Välj **OK**.
    3. Du får ett bekräftelsemeddelande med plockningsnummer. 

4. Öppna distributionslagerplockning
    1. Med ![glödlampan som öppnar funktionen Berätta 7.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Distributionslagerplockningar** och väljer sedan relaterad länk
    2. Leta upp de plockningar du har skapat och öppna den.
    3. Uppdatera **Ant. att hantera** vid behov.
    4. Välj **Registrera plockning**.
    5. Distributionslagerplockningen stängs och tas bort om alla kvantiteter hanteras.

5. Bokför dist.lager utleverans
   1. Välj ![glödlampan som öppnar funktionen Berätta 8.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Distributionslagerutleverans** och väljer sedan relaterad länk.  
   2. Leta upp de utleveranser du har skapat och öppna den.
    Lägg märke till att fältet **Ant. leverera** fylls i.
    3. Du kan uppdatera **Bokföringsdatum**, **Externt verifikationsnr.**, **Speditörkod**, **Leveransmetod** vid behov. Icke-tomma värden överförs till källdokument.
    4. Välj åtgärden **Bokför utleverans**.
    5. Bekräfta alternativet **leverans**.

### <a name="results-1"></a><a name="results-1"></a><a name="results-1"></a>Resultat
 - de rostade bönorna har nu registrerats som plockad 
 - **Registrerad distributionslagerplockning** skapas
 - **Bokförd distributionslagerutleverans** skapas
 - de tre **Bokförd utleverans** skapas
 - försäljningsorder har **Utlevererat antal** uppdaterats för raderna som levererats
 - artikel **lager** minskas med det valda antalet


## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även
[Ta emot artiklar](../../warehouse-how-receive-items.md)
[Konfigurera grundläggande distributionslager med verksamhetsområden](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Designdetaljer: Inkommande distributionslagerflöde](../../design-details-inbound-warehouse-flow.md)
[Leverera artiklar](../../warehouse-how-ship-items.md)
[Plocka artiklar för utleverans från dist.lager](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Designdetaljer: Utgående distributionslagerflöde](../../design-details-outbound-warehouse-flow.md)
[Visa artikeldisposition](../../inventory-how-availability-overview.md)

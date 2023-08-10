---
title: 'Inleverera, artikelinförsel, plocka och leverera grundläggande distributionslagerkonfigurationer'
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

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Genomgång av ankommande och avgående flöde i grundläggande distributionslagerkonfigurationer

Den här genomgången visar hur man slutför inkommande och utgående flöden i konfigurationen Grundläggande: order för order. Mer information finns i avsnittet [Översikt över olika konfigurationsalternativ](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Förutsättningar
För att slutföra denna genomgång måste du ange dig själv som distributionslagerpersonal på lagerstället *SILVER* med de här stegen:  
1. Välj ![glödlampan som öppnar funktionen Berätta 1.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2. Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
3. I fältet **Lagerställekod** ange *SILVER*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Inkommande flöde: Inleverera och införa utflöde i grundläggande lagerkonfigurationer

I [!INCLUDE[prod_short](../../includes/prod_short.md)], kan de inkommande processerna för att inleverera och lagerinföra utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Inleveranser|Artikelinförslar|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|INTER|||2|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument|||X|3|  
|L|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument||X||6-4-5|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: Ingående distributionslagerflöde](../../design-details-inbound-warehouse-flow.md).  

Efterföljande genomgången visar metod B i föregående tabellen.  

### <a name="scenario"></a>Scenario
Alicia, inköpsagenten, skapar inköpsorder för olika rostade bönor. När leveransen anländer till lagret, placerar Anders, lagerarbetaren, artiklarna på de lämpligaste lagerplatserna. När Anders bokför artikelinförseln bokförs artiklarna som inlevererade i lagret och är tillgängliga för försäljning eller för annat behov.  

### <a name="steps"></a>Steg
1. Ställ in sidan **Lagerställekort** så att den definierar företagets inkommande lagerflöden.  

    1.  Välj ![glödlampan som öppnar funktionen Berätta 2.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
    2.  Öppna lagerställekortet *SILVER*.  
    3.  Markera kryssrutan **Begär artikelinförsel**.  

2. Definiera standardlagerplats för artikeln om du vill kontrollera var den är artikelinförsel

    1.  Välj åtgärden **Lagerplats** på **Lagerställekort**
    2.  Markera den första raden för lagerplatsen *S-1-01*, och välj sedan åtgärden **innehåll**.  
    3.  Välj åtgärden **Ny**.  
    4.  Markera fälten **Fast** och **Standard**.  
    5.  I fältet **Verifikationsnr.** anger du *WRB-1000*.  

3. Skapa inköpsordern som är den vanligaste typen för inkommande källdokumentet.  

    1.  Välj ![glödlampan som öppnar funktionen Berätta 3.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
    2.  Välj åtgärden **Ny**.  
    3.  Skapa en inköpsorder för leverantör 10000 med följande inköpsorderrader. Använd anpassningsverktygen om ett fält för **Lagerplatskod** inte visas. Mer information finns i [Anpassa din arbetsyta](../../ui-personalization-user.md). 

    |Artikel|Lagerställekod|Lagerställeskod|Antal|  
    |----------|----------|---------|--------------|  
    |WRB-1000|SILVER|S-1-01|20|  
    |WRB-1001|SILVER||30|

    Lagerplatskoden i den första fylls i överensstämmelse med inställningen. Lagerplatskoden för den andra artikeln är tom eftersom den inte har standardvärden. Behåll det så här.  

    4.  Välj åtgärden **Frisläpp** för att meddela lagret att inköpsordern är klar för lagerhantering när leverans anländer.  

4. Skapa **lager, artikelinförsel** för att Inleverera och införa de levererade artiklarna  

    1. Välj ![glödlampan som öppnar funktionen Berätta 4.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lager, artikelinförsel** och väljer sedan relaterad länk.  
    2. Välj åtgärden **Ny**. 
    3. Välj *SILVER* i fältet **Lagerställekod**.
    4. Välj fältet **Källdokument** och sedan **Inköpsorder**.  
    5. Välj fältet **Källnr.**, välj raden för köpet från leverantör 10000 och välj sedan **OK** för att fylla i artikelinförselraderna i enlighet med det valda källdokumentet.

        Välj alternativt åtgärden **Hämta källdokument** och välj sedan inköpsordern.  

5. Ändra lagerartikelinförseln baserat på faktiskt införande av artiklar och bokför dokument

    När artiklar förs in på lagerplatser, plockas standardlagerplatsen redan till några artiklar, så han bestämde sig för att använda en annan lagerplats. Anders placerar också andra artiklar på nästa lagerplatser, eftersom Inlevererad kvantitet inte passar kapaciteten.

    1. På den första raden ändras **Lagerplatskod** från *S-1-01*, tsom kopierades från inköpsordern till *S-1-02*. 
    2.  Ange 20 i fältet **Ant. att hantera** på lagerartikelinförselraden med artikel WBR-1000.  
    3. På andra raden anger du 20 i fältet **Ant. att hantera** och väljer åtgärden **Dela rad**. Det visas en ny rad, som är en kopia av den ursprungliga raden, med den skillnaden att fältet **Ant. att hantera** innehåller det antal som du tog bort från den ursprungliga raden. 
    4. Fyll i lagerplatskoder för artikel WBR-1001:

    |Artikel|Lagerställeskod|Antal|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Välj åtgärden **bokför**, välj åtgärden **inleverera**, och välj sedan **OK**-knappen.  

### <a name="results"></a>Resultat
 - de rostade bönorna har nu registrerats som artikelinförsel på angivna lagerplatser
 - **Bokförd artikelinförsel i lager** skapas
 - **Bokförd inköpsinleverans** skapas
 - inköpsorder har **Inlevererat antal** uppdaterats för raderna som inlevererats
 - artikel **lager** ökas med det valda antalet
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Utgående flöde: Plockning och leverans i grundläggande lagerkonfiguration

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de utgående processerna för plockning och utleverans utföras på fyra sätt med hjälp av olika funktionaliteter beroende på lagerkomplexitetsnivån.  

|Metod|inkommande behandling|Lagerställen|Plockningar|Utleveranser|Nivå av komplexitet (Se [Designdetaljer: Lagerstyrningsinställning](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokföra plockning och utleverans från orderraden|INTER|||2|  
|B|Bokföra plockning och utleverans från ett lagerplockningdokument||X||3|  
|L|Bokföra plockning och utleverans från ett distributionslagerutleveransdokument|||X|6-4-5|  
|D|Bokföra plockning från ett distributionslagerplockningdokument och bokföra leveransen från ett distributionslagerutleveransdokument||INTER|INTER|6-4-5|  

Mer information finns i [Designdetaljer: utgående distributionslagerflöde](../../design-details-outbound-warehouse-flow.md).  

Efterföljande genomgången visar metod B i föregående tabellen.

### <a name="scenario-1"></a>Scenario
Susan, orderhandläggaren, skapar försäljningsorder för olika rostade bönor och skickar den till lagerstället. Anders, lagerarbetaren, måste kontrollera att leveransen förbereds och levereras till kunden. Anders hanterar alla uppgifter som är involverade på sidan **Lagerplockning** som automatiskt pekar på lagerställena där rostade bönor lagras.

### <a name="steps-1"></a>Steg
Detta är en fortsättning av [Inkommande flöde: Inleverera och införa utflöde i grundläggande lagerkonfigurationer](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Ställ in sidan **Lagerställekort** så att den definierar företagets inkommande lagerflöden.  

    1.  Välj ![glödlampan som öppnar funktionen Berätta 5.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
    2.  Öppna lagerställekortet *SILVER*.  
    3.  Markera kryssrutan **Begär plockning**.  

2. Skapa försäljningsorder som är den vanligaste typen för utgående källdokumentet.  

    1. Välj ![glödlampan som öppnar funktionen Berätta 6.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
    2. Välj åtgärden **Ny**.  
    3. Skapa en försäljningsorder för kunden 10000 med följande försäljningsorderrad.  

    |Artikel|Lagerställekod|Antal|  
    |----|-------------|--------|  
    |WRB-1000|SILVER|20|  
    |WRB-1001|SILVER|30|  

    Lagerplatskoderna fylls automatiskt i med standardlagerplatser.

    4. Välj åtgärden **Skapa lagerinförsel/plockning/rörelse**.
    5. Markera kryssrutan **Skapa lagerplockning**.  
    6. Välj **OK**. En ny lagerplockning skapas.

3. Plocka och utleverera artiklar

    1. Välj ![glödlampan som öppnar funktionen Berätta 7.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lagerplockning** och väljer sedan relaterad länk.  
    2. Välj lagerplockningen för försäljningen till kunden 10000
    
    Det skapade lagerplocket ignorerade lagerplats som definierats för artikeln *WRB-1000*, eftersom den inte innehåller inventering och använde en annan lagerplats. De andra raderna, med artikel *WRB-1001*, delades automatiskt upp för plockning från flera lagerplatser.
    
4. Välj åtgärden **Fyll i auto. ant. att hantera**.  

5. Välj åtgärden **bokför**, välj **leverera**, och välj sedan **OK**-knappen.  

### <a name="results-1"></a>Resultat
 - de rostade bönorna har nu registrerats som plockade från angivna lagerplatser
 - **Bokförd lagerplockning** skapas
 - **Bokförd utleverans** skapades
 - försäljningsorder har **Utlevererat antal** uppdaterats för raderna som levererats
 - artikel **lager** minskas med det valda antalet


## <a name="see-also"></a>Se även
[Införda artiklar med lagerinförslar](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Konfigurera grundläggande distributionslager med verksamhetsområden](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Designdetaljer: Inkommande distributionslagerflöde](../../design-details-inbound-warehouse-flow.md) 
[Plocka artiklar för utleverans från dist.lager](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Designdetaljer: Utgående distributionslagerflöde](../../design-details-outbound-warehouse-flow.md) 
[Visa artikeldisposition](../../inventory-how-availability-overview.md) 

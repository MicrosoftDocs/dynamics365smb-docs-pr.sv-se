---
title: Genomgång av servicekontrakt för serviceartiklar
description: I den här artikeln får du hjälp med olika scenarier som omfattar serviceartiklar och avtal.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Genomgång av servicekontrakt för serviceartiklar

Den här genomgången visar flera kärnprocesser:

- Skapa serviceartiklar via Försäljning
- Skapa och fakturera ett servicekontrakt
- Skapa en serviceorder för ett servicekontrakt
- Tilldela en resurs baserat på kompetens och zon
- Slutför tidsregistreringen för serviceordern
- Bokför och fakturera kontraktserviceordern

## <a name="creation-of-service-items"></a>Skapa serviceartiklar

### <a name="scenario"></a>Scenario

Orderhandläggaren Susan bokför en försäljningsorder som säljer en artikel som konfigurerats för att generera en serviceartikel.  

### <a name="steps"></a>Steg

1. Kontrollera att **Serviceartikelgrupp** har valts för **Artikel**.
   
    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.  
    2. Välj artikel *S-100* och öppna den.
    3. Kontrollera värdet i fältet **Serviceartikelgrupp**.
       
2. Bokför **försäljningsordern** för att skapa serviceartikeln för kunden.  

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
    2. Välj ordern för kund 10000. Externt ordernr är *SVC-1*.
    3. Välj åtgärden **Bokför** för att leverera artikeln till kunden.

### <a name="results"></a>Resultat

- En serviceartikel skapas för kund 10000

## <a name="invoicing-a-service-contract"></a>Fakturera ett servicekontrakt

### <a name="scenario-1"></a>Scenario

Servicechefen Charles skapar sedan ett servicekontrakt som ska faktureras för regelbundna underhållsbesök.

3. Skapa **Servicekontraktet** för den nya serviceartikeln
    1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk.
    2. Välj åtgärden **Ny**.  
    3. I bekräftelsedialogrutan väljer du **Ja** för att skapa kontrakt med hjälp av mall. 
    4. Välj *Ej förbetalt kontrakt – månadsvis*.
    5. På snabbfliken Service, i fältet **Serviceordertyp**, anger du **UNDERH.**
    6. På raderna anger du följande information:

    |Serviceartikelnr|Radvärde|  
    |----------------|----------|  
    |SV000001|6000|

    7. Välj åtgärden **Signera kontrakt** och bekräfta signaturen.
    8. Välj **Ja** för att bekräfta skapandet av en servicefaktura. Du får ett bekräftelsemeddelande med numret för servicefakturan.

3. Bokför servicefakturan
   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicefakturor** och väljer sedan relaterad länk.
   2. Leta upp servicefakturan och välj åtgärden **Bokför**.

### <a name="results-1"></a>Resultat

- Ett signerat servicekontrakt skapas, med transaktioner
- En bokförd servicefaktura skapas

## <a name="create-a-service-order-for-a-service-contract-and-assign-resources"></a>Skapa en serviceorder för ett servicekontrakt och tilldela resurser

### <a name="scenario-2"></a>Scenario

Servicechefen Charles skapar serviceorderna för regelbundna underhållsorder under Servicekontrakt och granskar sedan beordringstavlan för att tilldela dem.

### <a name="steps-1"></a>Steg

1. Kör de serviceorder som uppfyller skyldigheterna i aktiva servicekontrakt.
   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Skapa kontraktserviceorder** och väljer sedan relaterad länk.
   2. Ange månadens start- och slutdatum i fälten Startdatum och Slutdatum på snabbfliken Alternativ
   3. Välj **OK** för att bekräfta skapandet av serviceorder. Du får ett bekräftelsemeddelande med nummer för de serviceorder som skapats.

2. Granska de order som väntar på tilldelning via beordringstavlan
   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Beordringstavla** och väljer sedan relaterad länk.
   2. Beordringstavlan visar alla öppna serviceorder tillsammans med **antalet fördelningar** för att visa om serviceorderna har tilldelats till en resurs.
   3. Välj åtgärden **Visa dokument** för att öppna en serviceorder.  Du kommer att se att faktaboxen Serviceartikelrader visar vilka resurser som är skickliga på att arbeta med den här artikeln.

3. tilldela en resurs till servicerordern
   1. Välj serviceordern väljer du radåtgärden **Resursfördelningar**
   2. Ange följande information om resursfördelningen

    |Serviceartikelnr|Resursnr|Fördelningsdatum|Fördelade timmar|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|d|1|

    3. Fördelningens status ändras till Aktiv.
    4. Om du uppdaterar beordringstavlan visas att **Antal fördelningar** har ändrats från 0 till 1 för serviceordern.

### <a name="results-2"></a>Resultat

- Serviceorder skapas för servicekontrakten
- Serviceorderna fördelas till en resurs för att slutföra arbetet

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Slutför tidsregistreringen för serviceordern och bokför serviceordern

### <a name="scenario-3"></a>Scenario

Serviceteknikern registrerar sin tid direkt mot serviceordern och markerar sedan ordern som avslutad.

> [!NOTE]
> Tidsregistrering för serviceorder kan anges via tidrapporter. För mer information, se [länk till tidrapport om denna anteckning är meningsfull].

### <a name="steps-2"></a>Steg

1. Leta reda på serviceordern och ange tiden på serviceraden
   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.
   2. Hitta den serviceorder som du vill ange tid för.
   3. Välj radåtgärden **Servicerad**.
   4. Ange följande information:

    |Kontakttyp|Nr.|Kvantitet|Ant. att förbruka|
    |----|---|--------|--------|   
    |Resurs|RESOURCE1|2|2|

2. Bokför förbrukningen på serviceordern
   1. Välj åtgärden **Bokför** för att slutföra serviceordern, välj alternativet **Leverera och förbruka**, och välj sedan **OK**-knappen.

### <a name="results-3"></a>Resultat

- Servicetransaktioner skapas kopplade till serviceartikeln, servicekontraktet och resursen

## <a name="see-also"></a>Se även

[Introduktion till demonstrationsdata för Contoso Coffee](../../contoso-coffee/contoso-coffee-intro.md)  
[Om produktionsorder](../../production-about-production-orders.md)

---
title: Genomgång av serviceorder för serviceartiklar
description: I den här artikeln får du hjälp med flera kärnprocesser som omfattar serviceorder och artiklar.
author: andreipa
ms.author: andreipa
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# <a name="walkthrough-of-service-orders-for-service-items"></a>Genomgång av serviceorder för serviceartiklar

Den här genomgången visar flera kärnprocesser:

- Skapa en ad hoc-serviceorder och registrera reparation av artikeln
- Tillhandahåll en låneartikel till kunden under en reparationsperiod
- Bokför och fakturera serviceordern
    
## <a name="creating-a-service-order"></a>Skapa en serviceorder

### <a name="scenario"></a>Scenario

Servicechefen Charles skapar en serviceorder för ett reparationsscenario och lånar ut en låneartikel till kunden under reparationstiden.

### <a name="steps"></a>Steg

1. Skapa serviceordern manuellt för den artikel som behöver repareras.
   1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Serviceorder**
   2. Välj åtgärden **Ny**.
   3. Ange **10000** i kundnr. fält
   4. Välj **REPARERA** för fältet **Serviceordertyp**.
   5. På raderna väljer du **S-100** som **Artikelnr**.
2. Valfritt
   1. Välj raåtgärden **Felsökning** för att kontrollera möjliga lösningar.
   2. Välj radåtgärden **Relationer Fel/åtgärd.koder**
   3. Välj *LJUD* som **Symptomkod**
   4. Välj *5-2 Högt ljud under bryggning* som **Felkod** och stäng sidan. Felkod, åtgärdskod uppdateras på rader.
3. Låna ut en ersättningsartikel medan varan repareras
   1. På raderna väljer du **LÅNARE1** som Lånarnr. Bekräfta utfärdandet av låneartikeln genom att välja **Ja** för att låna ut låneartikeln. 
   2. Välj funktionsåtgärden **Hämta std.-servicekoder**, välj standardkoden associerad med servicegruppen och klicka på **OK**.
   
### <a name="results"></a>Resultat

- En serviceorder skapas för artikeln
- Serviceorderns servicedokumentlogg visar låneartikelns aktiviteter.
- Låneartikeln kommer att ha en transaktion som återspeglar utlåningen.
   

## <a name="regsiter-performed-work-mark-loaner-as-returned"></a>Regsiter utförde arbete - markera låneartikeln som returnerad.

### <a name="scenario-1"></a>Scenario

Serviceteknikern markerar låneartikeln som returnerad, registrerar utfört arbete.

### <a name="steps-1"></a>Steg

1. Hitta serviceuppgiften och registrera tid 
   1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
   2. Hitta den serviceorder som du vill ange tid för.
   3. Välj åtgärden **Artikelförslag**.
   4. Ange följande information:

    |Kontakttyp|Nr.|Kvantitet|
    |----|---|--------|  
    |Artikel|SER102|2|

   4. Välj *FÄRDIG* i fältet **Reparationsstatuskod**
    
2. Markera låneartikeln som returnerad
   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **låneartiklar** och väljer sedan relaterad länk.
   2. Hitta den låneartikel som ska markeras som returnerad.
   3. Välj åtgärden **Inleverans** 
   4. Bekräfta returnerandet av låneartikeln genom att välja **Ja** för att returnera låneartikeln.
      
### <a name="results-1"></a>Resultat

- Serviceorderns **servicedokumentlogg** visar låneartikelns aktiviteter.
- Låneartikeln kommer att ha en transaktion som återspeglar inleveransen.


### <a name="scenario-2"></a>Scenario

Servicechefen Charles bokför den färdiga serviceordern.

1. Hitta serviceordern 
   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.
   2. Hitta den serviceorder som du vill bokföra.

2. Bokför fakturan på serviceordern
   1. Välj åtgärden **Bokför** för att slutföra serviceordern, välj alternativet **Leverera och fakturera**, och välj sedan **OK**-knappen.
   2. Bekräfta öppnandet av den bokförda fakturan genom att välja **Ja**. 
### <a name="results-2"></a>Resultat

- **Bokförd servicefaktura** skapas.
- **Servicetransaktioner** associerade till artikel och resurs skapas

## <a name="see-also"></a>Se även

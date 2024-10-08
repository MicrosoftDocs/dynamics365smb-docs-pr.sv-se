---
title: Genomgång av grundläggande projekt
description: Den här artikeln vägleder dig genom flera kärnprocesser inom projektledning.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-of-basic-jobs"></a>Genomgång av grundläggande projekt

Den här genomgången visar flera kärnprocesser:

- Lägga till projektaktiviteter
- Registrera utgifter för tid och material till ett projekt
- Fakturera projekt

## <a name="adding-a-project-task"></a>Lägga till en projektuppgift

### <a name="scenario"></a>Scenario

Simon, projektledaren, vill lägga ner tid på att lära kunden hur man använder espressomaskinens produkt. Simon vill använda en separat uppgift i jobbet för att installera en kommersiell maskin på plats.

### <a name="steps"></a>Steg

1. Skapa projektuppgiften.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Projekt** och välj sedan relaterad länk.  
    2. Välj projektet *J00010*.
    3. I åtgärden **Aktiviteter** och ange åtgärden **Nya rad** och ange sedan följande värden:
 
    |Projektuppgiftsnr|Description|Typ av projektuppgift|
    |------------|-----------|-------------|  
    |220|Kundutbildning|Bokföra|

2. Dra in projektaktiviteter.
   1. I området Uppgift letar du upp åtgärden **Indrag av projektaktiviteter**.
   2. Bekräfta att du vill dra in uppgifter genom att välja **Ja**.

### <a name="results"></a>Resultat

 - Nu kan tid och utgifter registreras i den nya projektuppgiften

## <a name="record-time-and-material-expenses-to-a-project"></a>Registrera tids- och materialkostnader för ett projekt

### <a name="scenario-1"></a>Scenario

Edgin, teknikern som installerar maskinen, måste registrera sin tid och materialet som används under installationen till projektet för fakturering. Edgin har redan lagt till resor och material, och behöver nu lägga till tiden för att lära personalen hur man använder maskinen.

### <a name="steps-1"></a>Steg

1. Skapa de extra projektjournalraderna.

    1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projektjournaler** och väljer sedan relaterad länk.  
    2. Välj batchen *CONTOSO*. Du kommer att se flera rader med resurs- och artikeltyper som återspeglar den tid (för teknikern och fordonet) och det material (maskinen och förbrukningsartiklarna) som använts.
    3. Skapa en ny rad och ange sedan följande värden:
 
    |Projektnr|Projektuppgiftsnr|Kontakttyp|Nr.|Description|Kvantitet|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Resurs|EDGIN|Kundutbildning|1|

2. Bokför tid och utgift.
   1. Välj åtgärden **Bokföra**.
   2. Bekräfta att du vill bokföra raderna genom att välja **Ja**.

### <a name="results-1"></a>Resultat

- Projekttransaktioner och resurstransaktioner av typen *Förbrukning* skapas
- Artikeltransaktioner skapas för att justera lagret negativt.
- På projektkortet återspeglar kostnader och priser i området Uppgifter de nya saldon som väntar på att faktureras.
- På projektkortet visas summorna för priserna i faktaboxen projektdetaljer.

## <a name="creating-a-sales-invoice-for-a-project"></a>Så här skapar du en försäljningsfaktura för ett projekt

### <a name="scenario-2"></a>Scenario

Simon måste skapa och bokföra en faktura som ska skickas till kunden tillsammans med tiden och utgifterna för projektet.

### <a name="steps-2"></a>Steg

1. Skapa försäljningsfakturan.

    1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Projekt** och välj sedan relaterad länk.  
    2. I listan över projekt väljer du åtgärden **Skapa projektförsäljningsfaktura**.
    3. Ange **Projektnr.** filtrera till *J00010*.
    4. Välj **OK** för att generera försäljningsfakturan. Du får en bekräftelse på hur många fakturor som genereras.

2. Bokför fakturan för tid och utgift.

   1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.  
   2. Välj den sista fakturan för att öppna den för granskning.
   3. Välj åtgärden **Bokföra**.

### <a name="results-2"></a>Resultat

- Projekttransaktioner och resurstransaktioner av typen *Försäljning* skapas.
- På projektkortet återspeglar kostnader och priser i området Uppgifter nya, fakturerade saldon.
- På projektkortet visas prissummorna i faktaboxen Projektdetaljer i avsnittet för fakturerat pris.

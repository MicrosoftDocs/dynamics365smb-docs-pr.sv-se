---
title: XML-scheman för att förbereda definitioner för databyten
description: Använd XML-scheman för att ställa in ramverk för datautbyte för att definiera vilka data element som du vill skicka med.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Använd XML-scheman för att förbereda definitioner för databyten

Om du vill aktivera importera/exportera av data i XML-filer via ramverket för datautbyte i [!INCLUDE[prod_short](includes/prod_short.md)], kan du använda XML-schema för att definiera vilka dataelement du vill utbyta med [!INCLUDE[prod_short](includes/prod_short.md)]. Du utför detta arbete på sidan **XML-schemavisning** genom att ladda XML-schemafilen, välja tillhörande dataelement samt därefter initialisera en definition för databyte.  

 När du har definierat vilka dataelement som sa inkluderas baserat på XML-schemat kan du använda åtgärden **Generera definition för databyte** för att initialisera en definition för databyte baserat på valda dataelement som du sedan slutför i ramverket för databyten. Det skapar en post på sidan **Definitioner för bokföringsbyte** där du fortsätter genom att ange vilka element i filen som mappas till vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

 Det här avsnittet innehåller följande procedurer:  

- Så här läser du in en XML-schemafil  

- Så här markerar eller avmarkerar du noder i ett XML-schema  

- Så här skapar du en definition för datautbyte baserat på ett XML-schema  

## Så här läser du in en XML-schemafil

1. Se till att den relevanta XML-schemafilen är tillgänglig. Filnamnstillägget är .xsd.  

2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **XML-scheman** och väljer sedan relaterad länk.  

3. Välj åtgärden **Ny**.  

4. Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kod**|Ange en kod som identifierar XML-schemat.|  
    |**Beskrivning**|Ange beskrivningen av XML-schemat.|  

     Fältet **Målnamnrymd** anger ett namnområde i XML-schemafilen som har laddats för raden.  

5. Välj **Läs in schema**-åtgärden och välj sedan XML-schemafilen.  

     När filen har fylls i fylls resten av fälten på raden i med information från filen, och kryssrutan **Schemat är inläst** markeras.  

    > [!NOTE]  
    >  Trädet med det inlästa xml-schemat är komprimerat som standard. Du expanderar varje nod genom att välja **+** på noden. Välj **Expandera alla** på menyfliken om du vill expandera alla noder.  

### Så här markerar eller avmarkerar du noder i ett XML-schema  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Visningsprogram för XML-schema** och väljer sedan relaterad länk.  

2. Fyll i fälten i huvudet enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**XML-schemakod**|Ange den XML-schemafil som du laddade i steg 5 i avsnittet "För att ladda en XML-schemafil".|  
    |**Ny XMLport Nr.**|Ange numret på den XMLport som skapas från XML-schemat när du väljer åtgärden **GenereraXMLport**.|  

     Raderna fylls nu i med noder som representerar alla element i XML-schemat. Noder för element som är obligatoriska i överensstämmelse med XML-schemat markeras som standard.  

3. På den första raden, i kolumnen **Nodnamn**, expanderar du noden **Dokument** och expandera sedan gradvis underliggande noder som du vill granska.  

     Högerklicka på en nod och välj sedan **Expandera alla**.  

4. Välj någon av följande åtgärder för att ändra vilka noder som visas.  

    |**Åtgärd**|Beskrivning|  
    |----------------|---------------------------------------|  
    |**Visa alla**|Alla noder visas.|  
    |**Dölj ej obligatoriska**|Endast noder som representerar element som krävs enligt XML-schemat visas. Dessa noder har anges vanligtvis med **1** i fältet **MinOccurs**.<br /><br /> Välj **Visa alla** för att återföra vyn.|  
    |**Dölj ej valda**|Endast noder där kryssrutan **Vald** är markerad visas.<br /><br /> Välj **Visa alla** för att återföra vyn.|  

5. Välj åtgärden **Redigera**.  

6. I kryssrutan **Vald** anger du för varje nod om du vill att elementet ska stödjas i definitionen för datautbyte för den relaterade SEPA-bankfilen.  

    > [!NOTE]  
    >  När du markerar en obligatorisk underordnad nod markeras även alla överordnade noder ovanför den.  

7. Välj åtgärden **Markera alla obligatoriska element** för att välja alla noder igen som representerar element som är obligatoriska enligt XML-schemat.  

8. Välj åtgärden **Avmarkera alla** för att rensa alla val.  

     Fältet **Val** anger att noden har två eller fler syskonnoder som fungerar som alternativ.  

### Så här skapar du en definition för datautbyte baserat på ett XML-schema  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **XML-scheman** och väljer sedan relaterad länk.  

2. Välj relevant XML-schema och välj sedan åtgärden **Öppna XML-schemavisare**.  

3. Se till att de relevanta noderna har markerats. Mer information finns i avsnittet "För att välja eller rensa noder i XML-schema".  

4. På sidan **Öppna XML-schemavisare** väljer du åtgärden **Generera datautbytesdefinition**.  

 Datautbytesdefinitionen skapas på sidan **Definitioner för bokföringsbyte** som du kan fylla i genom att ange vilka element i filen som ska mappas till respektive fält i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
> Du kan också använda funktionen **Hämta filstruktur** från sidan **Definitioner för bokföringsbyte** som använder funktionen på sidan **Visningsprogram för XML-schema** för att autofylla snabbfliken **Kolumndefinitioner**.  

> [!NOTE]
> Under 2019 års utgivningsvåg 1 kunde du generera en XMLport baserat på schemat och sedan importera denna i din lösning. Detta stöds inte längre.

## Se även

[Skapa dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)  
[Om ramverket för datautbyte](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
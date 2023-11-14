---
title: Ställa in felrapportering i servicehantering
description: Felrapportering låter dig upprätta standarder för att registrera felinformation för serviceartiklar med felkoder etc.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# Konfigurera felrapportering
Felrapportering låter dig upprätta standarder för att registrera felinformation för serviceartiklar. Exempelvis kan du ange problemet, vilka problem som uppstår, orsaken till problemet och hur du löser det.  

Felkoder identifierar de olika serviceartikelfelen eller de åtgärder som vidtas för serviceartiklar. Beroende på felrapporteringsnivån på företaget kanske du måste skapa feltypskoder och symptomkoder innan du skapar felkoder. Felområden identifierar fel hos serviceartiklar. Felorsakskoder identifierar orsaken till serviceartikelfel och vid behov utesluter garanti- och kontraktsrabatter. Du kanske till exempel vill utesluta garanti- och kontraktsrabatt om kunden är ansvarig för felet på serviceartikeln. Du kan tilldela felorsakskoder för serviceorder. Mer information finns i [Så här arbetar du med tjänsteuppgifter](service-how-to-work-on-service-tasks.md).  

## Ange övergripandenivå av felrapportering
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceinställningar** och väljer sedan relaterad länk.
2. I fältet **Felrapporteringsnivå**, välj ett av alternativen som beskrivs i följande tabell.  

    |**Felnivå**|**Beskrivning**|  
    |------------|-------------|  
    |Ingen | Inga rapporteringskoder används.|  
    |Fel | Koder visas i tabellen **Felkoder**. Dessa koder kan identifiera fel på serviceartiklar eller åtgärder som ska vidtas. Du kan gruppera närliggande koder i grupper med **feltypskoder**.|  
    |Fel + Symptom | Du kan ange en kombination av koder i tabellerna **Felkoder** och **Symptomkoder**. Vanliga symptomkoder omfattar indikatorer som en kund kan använda för att beskriva ett problem, till exempel brus eller kvalitet.|  
    |Fel + Symptom + Typ | Använd koderna Fel, Symptom och Felområde som en implementering av IRIS (International Repair Coding System).|  

När du gör inställningar för felhantering kan du också ange vilka reparationer eller åtgärder som associeras med ett fel eller en defekt. Du ställer in detta på sidan **fel/åtgärd kodssamband** där du konfigurerar kombinationer av koder för serviceartikelgruppen på serviceartikeln som du har öppnat fönstret för och antalet förekomster av var och en.

## Så här skapar du fel- och åtgärdskodssamband
<!--this needs to go in a working with topic-->
Du måste bygga upp information om fel- och åtgärdskodssamband för att kunna se de vanligaste reparationsmetoderna för vissa artikelfel när du utför på artiklarna. Använd batch-jobbet **Infoga fel-/åtgärdssambandskoder** för sökning efter alla kombinationer av fel- och åtgärdskoder i bokförda serviceorder och registrera dem på sidan **Fel-/åtgärdssambandskoder**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du infoga **fel-åtgärdssambandskoder**, och välj sedan relaterad länk.  
2. Ange datum för att definiera den period som du vill inkludera i batch-jobbet.  
3. Markera kryssrutan **Relation baserad på serviceartikelgrupp** om du vill att relationen ska grupperas efter serviceartikelgrupp.  
4. Markera kryssrutan **Bibehåll manuellt infogade poster** om du vill behålla uppgifterna som du redan har infogat manuellt i fönstret **Fel- och åtgärdssamband koder**.  

## Se även
[Ställa in tjänstehantering](service-setup-service.md)  
[Servicehantering](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
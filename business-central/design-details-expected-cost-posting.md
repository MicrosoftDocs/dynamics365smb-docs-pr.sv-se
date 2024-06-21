---
title: Designdetaljer – Bokföring av förväntad kostnad
description: Förväntade kostnader representerar uppskattningen av exempelvis en inköpt artikels kostnad som du registrerar innan fakturan för artikeln erhålls.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/20/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designdetaljer: Bokföring av förväntad kostnad
Förväntade kostnader representerar uppskattningen av exempelvis en inköpt artikels kostnad som du registrerar innan fakturan för artikeln erhålls.  

 Du kan bokföra förväntade kostnader till lagret och redovisningen. När du bokför ett antal som bara har inlevererats eller levererats men inte fakturerats, skapas en värdetransaktion med den förväntade kostnaden. Den förväntade kostnaden påverkar lagervärdet men bokförs inte till redovisningen om du inte har ställt in systemet att göra det.  

> [!NOTE]  
>  Förväntade kostnader hanteras endast för artikeltransaktioner. Förväntade kostnader är inte för immateriella transaktionstyper, till exempel kapacitet och artikelomkostnader.  

 Om endast antalsdelen för en lagerökning har bokförts ändras lagervärdet inte i redovisningen, om du inte har markerat kryssrutan **Förväntad kost.bokf. i redov.** på sidan **Lagerinställningar**. I så fall bokförs förväntade kostnader på interimskonton vid tidpunkten för inleveransen. När inleveransen har fakturerats helt balanseras interimskontona och den faktiska kostnaden bokförs till lagerkontot.  

 För att stödja avstämning och spårbarhet visar den fakturerade värdetransaktionen det förväntade kostnadsbeloppet som har bokförts för att motkontera interimskontona.  

## Förutsättningar för bokföring av förväntade kostnader

För att du ska kunna bokföra förväntade kostnader måste du göra följande:
1. På sidan **Lagerinställningar** markerar du kryssrutan **Automatisk bokföring av kostnader** och kryssrutan **Förväntad kostnadsbokföring till redovisning**.
2. Ställ in vilka interimskonton som ska användas under den förväntade kostnadsbokföringsbehandlingen.  

  På sidan **Bokföringsinställning för lager** bekräftar du fälten **Lagerkonto** **Lagerkonto (interim)** för **Lagerställekod och Bokföringsinställningskod för lager** för den artikel du tänker köpa. Mer information om dessa konton finns i [Designinformation – konton i redovisningen](design-details-accounts-in-the-general-ledger.md).
3. På sidan **Allmänna bokföringsinställningar** bekräftar du fältet **Lagerbokf. (interim)** för den **Allm. rörelsebokföringsmall** och den **Allm. produktbokföringsmall** som du ska använda.
4. När du skapar en inköpsorder krävs som standard fältet **Leverantörens fakturanummer**. Du måste stänga av detta på sidan **Inställningar för inköp och skulder** genom att avmarkera fältet **Ext. Dok.nr obligatoriskt**.

## Exempel  

> [!NOTE]  
> De kontonummer som används i detta exempel gäller endast som referens och kommer att variera i systemet. Ställ in dem enligt anvisningarna ovan.

Du bokför en inköpsorder som mottagen. Förväntad kostnad är 95,00 BVA.  

 **Värdetransaktioner**  

|Bokföringsdatum|Transaktionstyp|Kost.belopp (förväntat)|Förväntad kost. bokf. i redov.|Förväntad kostnad|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Inköpskostnad|95.00|95.00|Ja|1|1|  

 **Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**  

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Redovisningstransaktioner**  

|Bokföringsdatum|Redovisningskonto|Kontonr. (En-US-demo)|Belopp|Löpnr|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Lagerkontoredovisning (interim)|5530|-95.00|2|  
|01-01-20|Lager (interim)|2131|95.00|1|  

 Du kan bokföra inköpsordern som fakturerad vid ett senare tillfälle. Fakturerad kostnad är 100,00 BVA.  

 **Värdetransaktioner**  

|Bokföringsdatum|Kost.belopp (aktuellt)|Kost.belopp (förväntat)|Kostnad bokförd i redov.|Förväntad kostnad|Artikeltrans.löpnr|Löpnr|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100,00|-95.00|100,00|Nej|1|2|  

 **Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**  

|Löpnr redovisning|Värdelöpnr|Bokf. redov.journalnr|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Redovisningstransaktioner**  

|Bokföringsdatum|Redovisningskonto|Kontonummer (endast exempel!)|Belopp|Löpnr|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Lagerkontoredovisning (interim)|5530|95.00|4|  
|01-15-20|Lager (interim)|2131|-95.00|3|  
|01-15-20|Direkt kostnad kopplad – konto|7291|-100|6|  
|01-15-20|Lagerkonto|2130|100|5|  

## Se även
 [Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
 [Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)   
 [Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md)   
 [Designdetaljer: Lagerbokföring](design-details-inventory-posting.md)   
 [Designdetaljer: Varians](design-details-variance.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)  
 [Ekonomi](finance.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

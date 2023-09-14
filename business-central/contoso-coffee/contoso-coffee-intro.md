---
title: Introduktion till demonstrationsdata för Contoso Coffee
description: Översikt över scenarier som kan vara till hjälp när demonstrationsdatan för Contoso Coffee ska hjälpa dig lära dig hur du använder funktionerna i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: brentholtorf
ms.author: bholtorf
---

# Introduktion till demonstrationsdata för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-apparna för Business Central lägger till demonstrationsdata som du kan använda för att lära dig använda funktionerna i Business Central.  


## Konfigurera data för Contoso Coffee

Om du vill använda demonstrationsdata för Contoso Coffee måste du installera två appar i det aktuella företaget i [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Demonstrationsdatauppsättning för Contoso Coffee**  

    Den här appen levererar demonstrationsdata för basprogrammet.  
- **Demonstrationsdatauppsättning för Contoso Coffee (lands-ID)**  

    Den här appen lägger till landsspecifika innehåll ovanpå basprogrammet.

Lägg till programmen i ett tomt företag i en betald prenumeration eller som en del av en utvärderingsversion. Du kan till exempel skapa ett nytt företag utan exempeldata från den assisterade konfigurationsguiden **Skapa nytt företag** som du kan öppna från listan **Företag**. Lägg sedan till programmen från [marknadsplatsen](../ui-extensions-install-uninstall.md#install) om de inte redan anges på sidan **Tilläggshantering**.  

Sedan ska du slutföra:
 - [Produktionsinställningar](manufacturing/contoso-coffee-manufacturing-intro.md) för att förbereda för användning av [Produktionsscenarier](#manufacturing-scenarios)
 - [Lagerstyrningsinställningar](warehousing/contoso-coffee-warehousing-intro.md) för att förbereda för användning av [Lagerstyrningsscenarier](#warehousing-scenarios)

## Produktionsscenarier

Demonstrationsdata för Contoso Coffee stöder för närvarande följande produktionsscenarier för test och utbildning:

1. [Skapa en ny produktionsstruktur och strukturversion](manufacturing/create-new-production-bom-version.md)  
2. [Skapa en ny operationsföljd](manufacturing/create-new-routing.md)  
3. [Skapa en fast planerad produktionsorder och ändra den](manufacturing/create-firm-planned-production-order-change.md)  
4. [Kombinera automatisk och manuell bokföring](manufacturing/combine-automatic-manual-flushing.md)  
5. [Använda orderplanering för att skapa och reservera leverans](manufacturing/order-planning-create-reserve-supply.md)  
6. [Ställ in och hantera en legotillverkningsoperation](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Skapa en ny kapacitet](manufacturing/set-up-new-capacity.md)  
8. [Prognostisera behov för artikelvarianter med olika strukturer tilldelade](manufacturing/variants.md)  

Läs stegen för respektive scenario i den relevanta artikeln.  

> [!IMPORTANT]
> Produktionsgenomgångar kräver att användarupplevelsen är inställd på *Premium* på sidan **Företagsinformation**.

## Lagerstyrningsscenarier

Demonstrationsdata för Contoso Coffee stöder för närvarande följande lagerstyrningsscenarier för test och utbildning:

1.  Konfigurera standardlagerplatser, inleverans- och artikelinförsel med lagerinförsel, plockning och leverans på orderbasis med [Genomgång av ankommande och avgående flöde i blandade distributionslagerkonfigurationer](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Inleverans och artikelinförsel av flera inkommande order samtidigt med lagerinleverans, skicka flera order samtidigt med distributionslagerutleverans, plocka med distributionslagerplockningar med [Genomgång av ankommande och avgående flöde i blandade distributionslagerkonfigurationer](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Konfigurera fasta lagerplatser för artikelmåttenhet, direktutleveranser för att minska fysiska transporter av varor, optimera placering av varor med lagerpåfyllning, dela upp stora måttenheter i mindre, fördela plockning bland lageranställda med plockförslag med [Genomgång av ankommande och avgående flöde i avancerad distributionslagerkonfiguration med dirigerad artikelinförsel och plockning](warehousing/warehouse-directed-flow.md)

Läs stegen för respektive scenario i den relevanta artikeln.
   
## Se även

[Produktion](../production-manage-manufacturing.md)  
[Lagerstyrning](../warehouse-manage-warehouse.md)  


---
title: Hantera lager | Microsoft Docs
description: Beskriver hur du hanterar fysiska varor som du handlar med, till exempel hantering av lager i distributionslagret.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a4c4788f7f262dee32f489095bf1ee303ea712c5
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2019
ms.locfileid: "939422"
---
# <a name="inventory"></a>Lagersaldo
För varje fysisk produkt som du handlar i måste du skapa ett artikelkort av typen **Lager**. Artiklar som du erbjuder till kunder men inte håller i lager kan du registrera som katalogartiklar, som du kan omvandla till lagerartiklar vid behov. Du kan öka eller minska kvantiteten för en artikel i lager, genom att bokföra direkt till artikeltransaktionerna, till exempel efter en fysisk inventering eller, om du inte vill registrera inköp.

Lagerökningar och lagerminskningar registreras även naturligtvis när du bokför inköps- och försäljningsdokument. Mer information finns i [Bokföra inköp](purchasing-how-record-purchases.md), [Sälja produkter](sales-how-sell-products.md) och [Fakturera försäljning](sales-how-invoice-sales.md). Överföringar mellan lagerställen ändrar lagrets kvantiteter över företagets distributionslager.   

För att öka en översikt av artiklar och för att söka efter dem kan du kategorisera artiklar och ge dem attribut för att söka och sortera förbi.

> [!NOTE]
> Den fysiska hanteringen av artiklar kallas lageraktiviteter. Mer information finns i [Lagerhantering](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Lageravstämning
När du bokför lagertransaktioner, till exempel försäljningsutleveranser, inköpsfakturor eller lagerjusteringar, registreras de ändrade artikelkostnaderna i artikelvärdesposter. För att återspegla denna förändring i lagervärde i din bokföring kommer lagerkostnaderna automatiskt att bokföras på relaterade lagerkonton i redovisningen. För varje lagertransaktion som bokförs, bokförs lämpliga värden på lagerkontot, justeringskontot och KSV-kontot i redovisningen. Mer information finns i [Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Även om lagerkostnaderna automatiskt bokförs i redovisningen måste du fortsatt säkerställa att varukostnader skickas vidare till relaterade avgående försäljningstransaktioner, i synnerhet när varorna säljs innan du har fakturerat inköpet av varorna. I programmet kallas detta för Kostnadsjustering. Artikelkostnader justeras automatiskt när du bokför artikeltransaktioner, men du kan också justera projektartikelkostnader manuellt. Mer information finns i [Justera artikelkostnader](inventory-how-adjust-item-costs.md).

|Till |Gå till |
|---|----|
|Skapa artikelkort för lagerartiklar som du handlar med.|[Registrera nya artiklar](inventory-how-register-new-items.md)|
|Strukturera de överordnade artiklar som du säljer som satser som består av komponenter som du monterar till order eller lager.|[Arbeta med strukturer](inventory-how-work-BOMs.md)|
|Att hålla en översikt över artiklar och hjälpa dig att hitta och sortera artiklar genom att ordna dem i kategorier.|[Kategorisera artiklar](inventory-how-categorize-items.md)|
|Tilldela artikelattribut med olika värdetyper till artiklarna för att hjälpa dig att sortera och hitta artiklar.|[Arbeta med artikelattribut](inventory-how-work-item-attributes.md)|
|Skapa artikelkort för vissa artiklar som du erbjuder till kunder, men inte håller i lager.|[Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md)|
|Utföra en fysisk inventering av lagret med sidorna **Inventeringsorder** och **Inventeringsregistrering**.|[Beräkna lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md)|
|Utför en fysisk inventering, göra negativa eller positiva justeringar och ändra information, till exempel plats eller partinumret i artikeltransaktionerna.|[Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md)|
|Visa tillgängligheten av artiklar per lagerställe, per period, per försäljning eller per inköpshändelse eller per deras användning av monterings- eller produktionsstrukturer.|[Visa artikeldisposition](inventory-how-availability-overview.md)|
|Överför lagerartiklar mellan lagerställen med överföringsorder, för att hantera lageraktiviteter, eller med artikelgrupperingsjournalen.|[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)|
|Reservera lager eller inkommande artiklar för försäljningsorder, inköpsorder, serviceorder, monteringsorder eller produktionsorder.|[Reservera artiklar](inventory-how-to-reserve-items.md)|
|Ställa in en leverantörs eller kundens egen beskrivning för ett objekt så att du enkelt kan infoga deras artikelbeskrivning i handelsdokument.|[Använd artikeltvärreferenser](inventory-how-use-item-cross-refs.md)|
|Tilldela serienummer/partinummer till några ankommande eller avgående dokument- eller journalrader, till exempel för att spåra objekt vid återkallning.|[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)|
|Ställa in en leverantörs eller kundens egen artikelbeskrivning för ditt artikelkort så att du snabbt kan infoga deras artikelbeskrivning i handelsdokument.|[Använd artikeltvärreferenser](inventory-how-use-item-cross-refs.md)|
|Sök var serie- eller partinummer har använts i dess försörjningskedja, till exempel i återkallningssituationer.|[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)|
|Spärra en artikel så att den inte kan registreras på försäljnings- eller inköpsrader eller bokföras i en transaktion.|[Spärra artiklar](inventory-how-block-items.md)|
|Hantera affärsverksamheten på försäljningskontor, inköpsavdelningar eller planeringskontor på flera platser.|[Arbeta med ansvarsenheter](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

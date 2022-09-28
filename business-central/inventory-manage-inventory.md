---
title: Hantera lager
description: I den här artikeln beskrivs hur du hanterar de fysiska produkter som du handlar med genom att skapa ett lagerartikelkort.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.search.forms: 5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 568ccee7e01aacb429e6ed2e2b69daf91f67b488
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530034"
---
# <a name="manage-inventory"></a>Hantera lager

För varje fysisk produkt som du handlar i måste du skapa ett artikelkort av typen **Lager**. Artiklar som du erbjuder till kunder men inte håller i lager kan du registrera som katalogartiklar, som du kan omvandla till lagerartiklar vid behov. Du kan öka eller minska kvantiteten för en artikel i lager, genom att bokföra direkt till artikeltransaktionerna, till exempel efter en fysisk inventering eller, om du inte vill registrera inköp.

Lagerökningar och lagerminskningar registreras även naturligtvis när du bokför inköps- och försäljningsdokument. Mer information finns i [Bokföra inköp](purchasing-how-record-purchases.md), [Sälja produkter](sales-how-sell-products.md) och [Fakturera försäljning](sales-how-invoice-sales.md). Överföringar mellan lagerställen ändrar lagrets kvantiteter över företagets distributionslager.

För att öka en översikt av artiklar och för att söka efter dem kan du kategorisera artiklar och ge dem attribut för att söka och sortera förbi.

> [!NOTE]
> Den fysiska hanteringen av artiklar kallas lageraktiviteter. Läs mer i [lagerstyrning](warehouse-manage-warehouse.md).

Planeringen av artiklar för att motsvara efterfrågan omfattas av funktionen för leveransplanering. Läs mer i [planering](production-planning.md).  

## <a name="inventory-reconciliation"></a>Lageravstämning

När du bokför lagertransaktioner, till exempel försäljningsutleveranser, inköpsfakturor eller lagerjusteringar, registreras de ändrade artikelkostnaderna i artikelvärdesposter. För att återspegla denna förändring i lagervärde i din bokföring kommer lagerkostnaderna automatiskt att bokföras på relaterade lagerkonton i redovisningen. För varje lagertransaktion som bokförs, bokförs lämpliga värden på lagerkontot, justeringskontot och KSV-kontot i redovisningen. Läs mer i [Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Även om lagerkostnaderna automatiskt bokförs i redovisningen måste du fortsatt säkerställa att varukostnader skickas vidare till relaterade utgående försäljningstransaktioner, i synnerhet när varorna säljs innan du har fakturerat inköpet av varorna. I programmet kallas detta för Kostnadsjustering. Artikelkostnader justeras automatiskt när du bokför artikeltransaktioner, men du kan också justera projektartikelkostnader manuellt. Läs mer i [Justera artikelkostnader](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Närliggande uppgifter

I följande tabell beskrivs relaterade uppgifter.

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
|Reservera lager eller inkommande artiklar för försäljningsorder, inköpsorder, serviceorder, monteringsorder, överföringsorder eller produktionsorder.|[Reservera artiklar](inventory-how-to-reserve-items.md)|
|Ställ in artikelspårning så att du kan spåra artiklars serienummer, till exempel för att spåra artiklar vid återkallelser.|[Ställa in artikelspårning med serie-, parti- eller paketnummer](inventory-how-setup-item-tracking.md)|
|Tilldela serienummer eller partinummer till alla utgående eller inkommande dokument- eller journalrader.|[Arbeta med serienummer och partinummer](inventory-how-work-item-tracking.md)|
|Sök var serie- eller partinummer har använts i dess försörjningskedja, till exempel i återkallningssituationer.|[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)|
|Ställa in en leverantörs eller kundens egen artikelbeskrivning för ditt artikelkort så att du snabbt kan infoga deras artikelbeskrivning i handelsdokument.|[Använd artikelreferenser](inventory-how-use-item-cross-refs.md)|
|Spärra en artikel så att den inte kan registreras på försäljnings- eller inköpsrader eller bokföras i en transaktion.|[Spärra artiklar](inventory-how-block-items.md)|
|Hantera affärsverksamheten på försäljningskontor, inköpsavdelningar eller planeringskontor på flera platser.|[Arbeta med ansvarsenheter](inventory-responsibility-centers.md)|
|Använd resurser med särskilda funktioner för olika tjänster och serviceartiklar.|[Så här skapar du resursfördelningar](service-how-setup-resource-allocation.md)|

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/get-started-inventory-management/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]

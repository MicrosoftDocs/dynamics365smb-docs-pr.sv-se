---
title: Hantera lager | Microsoft Docs
description: Beskriver hur du hanterar fysiska varor som du handlar med, till exempel hantering av lager i distributionslagret.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>Lagersaldo
För varje fysisk produkt som du handlar i måste du skapa ett artikelkort av typen **Lager**. Artiklar som du erbjuder till kunder men inte håller i lager kan du registrera som ej lagerförd artikel, som du kan omvandla till lagerartiklar vid behov. Du kan öka eller minska kvantiteten för en artikel i lager, genom att bokföra direkt till artikeltransaktionerna, till exempel efter en fysisk inventering eller, om du inte vill registrera inköp.

Lagerökningar och lagerminskningar registreras även naturligtvis när du bokför inköps- och försäljningsdokument. Mer information finns i [Så här bokför du inköp](purchasing-how-record-purchases.md), [Så här säljer du produkter](sales-how-sell-products.md) och [Så här fakturerar du försäljning](sales-how-invoice-sales.md). Överföringar mellan lagerställen ändrar lagrets kvantiteter över företagets distributionslager.   

För att öka en översikt av artiklar och för att söka efter dem kan du kategorisera artiklar och ge dem attribut för att söka och sortera förbi.

Du måste se till att kostnaderna för artiklarna vidarebefordras till den relaterade avgående försäljningstransaktionen, framför allt i situationer där du säljer varor innan du fakturerar inköpet av dessa artiklar. Detta kallas för kostnadsjustering, något som du kan utföra manuellt eller ställa in att ske automatiskt när du bokför en artikeltransaktion.

## <a name="inventory-reconciliation"></a>Lageravstämning
När du bokför lagertransaktioner, till exempel försäljningsutleveranser, inköpsfakturor eller lagerjusteringar, registreras de ändrade artikelkostnaderna i artikelvärdesposter. För att återspegla denna förändring i lagervärde i din bokföring kommer lagerkostnaderna automatiskt att bokföras på relaterade lagerkonton i redovisningen. För varje lagertransaktion som bokförs, bokförs lämpliga värden på lagerkontot, justeringskontot och KSV-kontot i redovisningen.

Även om lagerkostnaderna automatiskt bokförs i redovisningen måste du fortsatt säkerställa att varukostnader skickas vidare till relaterade avgående försäljningstransaktioner, i synnerhet när varorna säljs innan du har fakturerat inköpet av varorna. I programmet kallas detta för Kostnadsjustering. Artikelkostnader justeras automatiskt när du bokför artikeltransaktioner, men du kan också justera projektartikelkostnader manuellt. Mer information finns i Så här justerar du artikelkostnader.

|Till |Gå till |
|---|----|
|Skapa artikelkort för lagerartiklar som du handlar med.|[Så här registrerar du nya objekt](inventory-how-register-new-items.md)|
|Strukturera de överordnade artiklar som du säljer som satser som består av komponenter som du monterar till order eller lager.|[Så här arbetar du med strukturer](inventory-how-work-BOMs.md)|
|Att hålla en översikt över artiklar och hjälpa dig att hitta och sortera artiklar genom att ordna dem i kategorier.|[Så här kategoriserar du artiklar](inventory-how-categorize-items.md)|
|Tilldela artikelattribut med olika värdetyper till artiklarna för att hjälpa dig att sortera och hitta artiklar.|[Så här arbetar du med Artikelattribut](inventory-how-work-item-attributes.md)|
|Skapa artikelkort för vissa artiklar som du erbjuder till kunder, men inte håller i lager.|[Så här arbetar du med Ej lagerförda artiklar](inventory-how-work-nonstock-items.md)|
|Utför en fysisk inventering, göra negativa eller positiva justeringar och ändra information, till exempel plats eller partinumret i artikeltransaktionerna.|[Så här: Inventera, justera och gruppera lager](inventory-how-count-adjust-reclassify.md)|
|Visa tillgängligheten av artiklar per lagerställe, per period, per försäljning eller per inköpshändelse eller per deras användning av monteringsstrukturer.|[Så här visar du artikeldisposition](inventory-how-availability-overview.md)|
|Överför lagerartiklar mellan lagerställen med överföringsorder, för att hantera lageraktiviteter, eller med artikelgrupperingsjournalen.|[Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)|
|Uppskatta eller skriv av värdet av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.|[Så här omvärderar du lager](inventory-how-revalue-inventory.md)|
|Justera artikelkostnader, antingen automatiskt eller manuellt, för att vidarebefordra kostnadsförändringar från ingående transaktioner till deras relaterade utgående transaktioner.|[Så här justerar du artikelkostnader](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>Se även  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)    
[Logistik](madeira-supply-chain.md)  
[Arbeta med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

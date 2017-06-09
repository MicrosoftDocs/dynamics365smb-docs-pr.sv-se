---
title: Lager | Microsoft Docs
description: Beskriver hur du hanterar fysiska artiklar.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Lagersaldo
För varje fysisk produkt som du handlar i måste du skapa ett artikelkort av typen **Lager**. Artiklar som du erbjuder till kunder men inte håller i lager kan du registrera som ej lagerförd artikel, som du kan omvandla till lagerartiklar vid behov. Du kan öka eller minska kvantiteten för en artikel i lager, genom att bokföra direkt till artikeltransaktionerna, till exempel efter en fysisk inventering eller, om du inte vill registrera inköp.

Lagerökningar och lagerminskningar registreras även naturligtvis när du bokför inköps- och försäljningsdokument. Mer information finns i [Så här bokför du inköp](purchasing-how-record-purchases.md), [Så här säljer du produkter](sales-how-sell-products.md) och [Så här fakturerar du försäljning](sales-how-invoice-sales.md). Överföringar mellan lagerställen ändrar lagrets kvantiteter över företagets distributionslager.   

För att öka en översikt av artiklar och för att söka efter dem kan du kategorisera artiklar och ge dem attribut för att söka och sortera förbi.

Du måste se till att kostnaderna för artiklarna vidarebefordras till den relaterade avgående försäljningstransaktionen, framför allt i situationer där du säljer varor innan du fakturerar inköpet av dessa artiklar. Detta kallas för kostnadsjustering, något som du kan utföra manuellt eller ställa in att ske automatiskt när du bokför en artikeltransaktion.

Ändringar av lagervärdet från handel kopplas automatiskt till din finansiella anläggningstillgångar när du bokför artikeltransaktioner.

|Om du vill |Gå till |
|---|----|
|Skapa artikelkort för lagerartiklar som du handlar med.|[Så här registrerar du nya objekt](inventory-how-register-new-items.md)|
|Strukturera de överordnade artiklar som du säljer som satser som består av komponenter som du monterar till order eller lager.|[Så här arbetar du med strukturer](inventory-how-work-BOMs.md)|
|Att hålla en översikt över artiklar och hjälpa dig att hitta och sortera artiklar genom att ordna dem i kategorier.|[Så här kategoriserar du artiklar](inventory-how-categorize-items.md)|
|Tilldela artikelattribut med olika värdetyper till artiklarna för att hjälpa dig att sortera och hitta artiklar.|[Så här arbetar du med Artikelattribut](inventory-how-work-item-attributes.md)|
|Skapa artikelkort för vissa artiklar som du erbjuder till kunder, men inte håller i lager.|[Så här arbetar du med Ej lagerförda artiklar](inventory-how-work-nonstock-items.md)|
|Öka eller minska en artikels lagerkvantitet, till exempel efter en fysisk inventering eller som ett enkelt sätt att registrera inköpsinleveranser.|[Så här justerar du lager](inventory-how-adjust-inventory.md)|
|Visa tillgängligheten av artiklar per lagerställe, per period, per försäljning eller per inköpshändelse eller per deras användning av monteringsstrukturer.|[Så här skapar du en tillgänglighetsöversikt](inventory-how-availability-overview.md)|
|Överför lagerartiklar mellan lagerställen med överföringsorder, för att hantera lageraktiviteter, eller med artikelgrupperingsjournalen.|[Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)|
|Uppskatta eller skriv av värdet av en eller flera artiklar i lager genom att bokföra deras faktiska, beräknade värde.|[Så här omvärderar du lager](inventory-how-revalue-inventory.md)|
|Justera artikelkostnader, antingen automatiskt eller manuellt, för att vidarebefordra kostnadsförändringar från ingående transaktioner till deras relaterade utgående transaktioner.|[Så här justerar du artikelkostnader](inventory-how-adjust-item-costs.md)|
|Lär dig hur ändringar av lagervärdet från handel kopplas automatiskt till dina ekonomiska böcker.|[Avancerad: Lageravstämning](advanced-inventory-reconciliation.md).|

## <a name="see-also"></a>Se även  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)    
[Logistik](madeira-supply-chain.md)  
[Arbetar med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

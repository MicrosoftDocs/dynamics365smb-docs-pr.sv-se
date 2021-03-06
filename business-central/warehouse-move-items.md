---
title: Flytta artiklar | Microsoft Docs
description: När artiklarna finns i lagret kanske de måste flyttas enligt de lageraktiviteter som håller igång artikelflödet genom lagret. Alla transporter sker direkt i samband med intern operationer, till exempel en produktionsorder som behöver slutartiklar eller artikelinförsel av färdiga varor. Andra transporter sker pga platsbrist i distributionslagret eller som ad hoc-transporter till och från funktion.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66c2b9d191bc899de6ec2b6e6bbcd99d133448b7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784123"
---
# <a name="moving-items"></a>Flytta artiklar
Lageraktiviteten att flytta artiklar inom distributionslagret utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats. Hur komplex det är kan sträcka sig från inga lagerkonfigurationer, till grundläggande lagerstyrning med hantering av order för order i en eller flera aktiviteter samt avancerade konfigurationer där alla lageraktiviteter måste utförs i ett dirigerat arbetsflöde. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

När artiklarna finns i lagerstället kanske de måste flyttas enligt de lageraktiviteter som håller igång artikelflödet genom lagret. Alla transporter sker direkt i samband med intern operationer, till exempel en produktionsorder som behöver slutartiklar eller artikelinförsel av färdiga varor. Andra transporter sker pga platsbrist i distributionslagret eller som ad hoc-transporter till och från funktion.

Andra transportuppgifter är att regelbundet göra återanskaffningar för plockningslagerställen eller fabrikslagerställen och att ändra information om lagerställets innehåll.

Att flytta artiklar till andra platser påverkar artikeltransaktionerna och måste därför göras med en överföringsorder. Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).  

Lagerrelaterade uppgifter för inventering, justering och gruppering av artiklar kan omfatta lagerställeuppgifter som gäller för distributionslagertransaktionerna innan de kan synkroniseras med de associerade artikeltransaktionerna. Mer information finns i [Inventera, justera och gruppera om lager](inventory-how-count-adjust-reclassify.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Flytta artiklar mellan lagerställen i grundläggande distributionslagerkonfigurationer när som helst och utan källdokument.|[Flytta artiklar i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Använd dist.lagertransportkalkylarket för att flytta artiklar i avancerad distributionslagerkonfiguration, både för källdokument och för ad hoc.|[Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Ta med komponentartiklarna till interna operationer i grundläggande distributionslagerkonfigurationer, som begärs av källdokument för dessa operationer.|[Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planera vilka lagerställen som ska fyllas på eller tömmas för att uppnå ett effektivt flöde, till exempel tömma ett volymlager före en stor inleverans.|[Planera lagertransporter i kalkylark](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Uppdatera vilken frekvens lagerställen, till exempel plockningslagerställen, måste återfyllas med på grund av fluktuation i efterfrågan.|[Beräkna lagerplatsåteranskaffning](warehouse-how-to-calculate-bin-replenishment.md)|
|Omstrukturera distributionslagret med nya lagerställeskoder och nya lagerplatsegenskaper och flytta dem eventuellt runt.|[Omstrukturera lager](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
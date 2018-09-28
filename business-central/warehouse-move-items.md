---
title: Flytta artiklar | Microsoft Docs
description: "När artiklarna finns i lagret kanske de måste flyttas enligt de lageraktiviteter som håller igång artikelflödet genom lagret. Alla transporter sker direkt i samband med intern operationer, till exempel en produktionsorder som behöver slutartiklar eller artikelinförsel av färdiga varor. Andra transporter sker pga platsbrist i distributionslagret eller som ad hoc-transporter till och från funktion."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6efb709151ea98b5c8d89d67138b52bac5751c56
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="moving-items"></a>Flytta artiklar
Lageraktiviteten att flytta artiklar inom distributionslagret utförs på olika sätt beroende på hur lagerstyrningsfunktionerna har konfigurerats. Hur komplex det är kan sträcka sig från inga lagerkonfigurationer, till grundläggande lagerstyrning med hantering av order för order i en eller flera aktiviteter samt avancerade konfigurationer där alla lageraktiviteter måste utförs i ett dirigerat arbetsflöde. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).

När artiklarna finns i lagerstället kanske de måste flyttas enligt de lageraktiviteter som håller igång artikelflödet genom lagret. Alla transporter sker direkt i samband med intern operationer, till exempel en produktionsorder som behöver slutartiklar eller artikelinförsel av färdiga varor. Andra transporter sker pga platsbrist i distributionslagret eller som ad hoc-transporter till och från funktion.

Att flytta artiklar till andra platser påverkar artikeltransaktionerna och måste därför göras med en överföringsorder. Mer information finns i [Så här överför du lager mellan olika lagerställen](inventory-how-transfer-between-locations.md).  

Andra transportuppgifter är att regelbundet göra återanskaffningar för plockningslagerplatser eller fabrikslagerplatser och att ändra information om lagerplatsens innehåll.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Flytta artiklar mellan lagerplatser i grundläggande distributionslagerkonfigurationer när som helst och utan källdokument.|[Flytta artiklar i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Använd dist.lagertransportkalkylarket för att flytta artiklar i avancerad distributionslagerkonfiguration, både för källdokument och för ad hoc.|[Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Ta med komponentartiklarna till interna operationer i grundläggande distributionslagerkonfigurationer, som begärs av källdokument för dessa operationer.|[Flytta komponenter till ett verksamhetsområde i grundläggande lagerkonfigurationer](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planera vilka lagerplatser som ska fyllas på eller tömmas för att uppnå ett effektivt flöde, till exempel tömma ett volymlager före en stor inleverans.|[Planera lagertransporter i kalkylark](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Uppdatera vilken frekvens lagerplatser, till exempel plockningslagerplatser, måste återfyllas med på grund av fluktuation i efterfrågan.|[Beräkna lagerplatsåteranskaffning](warehouse-how-to-calculate-bin-replenishment.md)|
|Omstrukturera distributionslagret med nya lagerplatskoder och nya lagerplatsegenskaper och flytta dem eventuellt runt.|[Omstrukturera lager](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


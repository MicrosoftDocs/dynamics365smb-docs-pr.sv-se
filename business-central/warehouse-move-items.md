---
title: Flytta artiklar
description: Lära dig att flytta artiklar mellan lagerplatser i distributionslagret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: Conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345'
---
# Flytta artiklar

Du kan flytta artiklar i distributionslagret på olika sätt beroende på hur du har konfigurerat distributionslagret. Komplexiteten kan variera:

* Små lagerställen kan använda grundläggande distributions lagerkonfiguration för att hantera order individuellt i ett eller flera steg.
* Stora lagerställen kan använda avancerade konfigurationer där alla lageraktiviteter koordineras av ett dirigerat arbetsflöde. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).

Artiklar kan behöva flyttas mellan lagerplatser, t.ex. på grund av interna åtgärder:

* En produktionsorder behöver komponenter som levererats, eller så är det färdiga artiklar som artikelinförseln innehåller.
* En lagerchef vill optimera utrymmet.
* Oplanerade transporter till och från åtgärder.
* Fylla på plockningslagerställen eller fabrikslagerställen.
* Uppdaterar lagerställesinnehåll.

Inventering, justering och gruppering av artiklar kan omfatta lagerställeuppgifter som gäller för distributionslagertransaktionerna innan de kan synkroniseras med de associerade artikeltransaktionerna. Läs mer på [Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).  

 I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|  
|Flytta artiklar mellan lagerställen|[Överföra lager mellan olika lagerställen](inventory-how-transfer-between-locations.md)|
|Flytta artiklar mellan lagerställen i grundläggande distributionslagerkonfigurationer när som helst och utan källdokument.|[Flytta artiklar i grundläggande distributionslagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Använd dist.lagertransportkalkylarket, intern artikelinförsel och plockning för att flytta artiklar i avancerad distributionslagerkonfiguration med direktplockning och artikelinförsel.|[Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Omstrukturera distributionslagret med nya lagerställeskoder och nya lagerplatsegenskaper och flytta dem eventuellt runt.|[Omstrukturera lager](warehouse-how-to-restructure-warehouses.md)|  

## Se relaterad [Microsoft utbildning](/training/modules/manage-internal-warehouse-processes/)

## Se även

[Warehouse Management – översikt](design-details-warehouse-management.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

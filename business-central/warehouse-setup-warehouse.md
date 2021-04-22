---
title: Konfigurera lagerprocesser | Microsoft Docs
description: Ett företags distributionsstrategi återspeglas i konfigurationen av dess lagerprocesser. Detta omfattar att definiera hur olika artiklar hanteras på olika lagerställen, till exempel graden av styrning av lagerplats och omfattningen av arbetsflödet som krävs mellan lageraktiviteterna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6730e88bff36347a387bbbbb05b82ec67bac8cac
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778003"
---
# <a name="setting-up-warehouse-management"></a>Ställa in lagerstyrning
Ett företags distributionsstrategi återspeglas i konfigurationen av dess lagerprocesser. Detta omfattar att definiera hur olika artiklar hanteras på olika lagerställen, till exempel graden av styrning av lagerplats och omfattningen av arbetsflödet som krävs mellan lageraktiviteterna.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Få en översikt över möjligheterna med grundläggande och avancerade distributionslagerfunktioner.|[Designdetaljer: Översikt över distributionslager](design-details-warehouse-overview.md)|  
|Ställa in åtta olika typer av lagerplatstyper, till exempel Plockningslagerplats, för att definiera vilka flödesaktiviteter som gäller för respektive typ av lagerplats.|[Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md)|  
|Skapa lagerställen, antingen manuellt eller automatiskt med information, till exempel namn, nummerserie och kategori, enligt en lagerplatsmall.|[Skapa lagerställen](warehouse-how-to-create-individual-bins.md)|  
|Definiera vilka artiklar som du vill lagra på en viss lagerplats och ställa in reglerna som bestämmer när lagerstället ska fyllas med en särskild artikel.|[Skapa lagerställesinnehåll](warehouse-how-to-set-up-bin-contents.md)|  
|Ange att en artikel alltid placeras på en viss lagerplats.|[Tilldela standardlagerställen till artiklar](warehouse-how-to-assign-default-bins-to-items.md)|
|Skapa mallar som styr var och hur artiklar införs vid dirigerad artikelinförsel.|[Skapa artikelinförselmallar](warehouse-how-to-set-up-put-away-templates.md)|
|Ange användare som anställda vid distributionslager vid särskilda platser.|[Registrera distributionslagerpersonal](warehouse-how-to-set-up-warehouse-employees.md)|
|Definiera olika typer av lagerställen i lagret för att styra var artiklar placeras enligt typ, rangordning eller hanteringsnivå.|[Registrera lagerställen för att använda lagerställen](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Göra fler inställningar för ett befintligt lagerställe för att aktivera det för lageraktiviteter.|[Konvertera befintliga lagerställen till distributionslagerställen](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Aktivera plockning, flyttning och utflöde för monterings- eller produktionsorder i grundläggande distributionslagerkonfiguration.|[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Ställa in artiklar och lagerställen för den mest avancerade lagerstyrningen där alla aktiviteter måste följa ett strikt arbetsflöde.|[Registrera artiklar och platser för dirigerad artikelinförsel och plockning](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Definiera när och hur artiklar på lagerställen inventeras för underhålls- eller ekonomirapportering.|[Inventera, justera och omgruppera lager](inventory-how-count-adjust-reclassify.md)|
|Aktivera lagerarbetarna att dela upp en större enhet i mindre enheter för att uppfylla behoven hos källdokument.|[Aktivera automatisk volymnedbrytning med dirigerad artikelinförsel och plockning](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Ställa in lagret så att det alltid föreslår automatiskt att de artiklar som utgår först plockas först.|[Aktivera plockning med FEFO](warehouse-picking-by-fefo.md)|
|Få tips på hur du ordnar om lagerställen, lagerställen eller zoner för att få mer effektiva lageraktiviteter.|[Omstrukturera lager](warehouse-how-to-restructure-warehouses.md)|
|Integrera streckkodsläsare i lösningen för hantering av lager. Endast för installation på plats.|[Använda ADCS (Automatiskt datainsamlingssystems)](warehouse-use-automated-data-capture-systems-adcs.md)|
|Ange standardrapporter som ska användas för olika dokumenttyper.|[Rapportval i Business Central](across-report-selections.md)|

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
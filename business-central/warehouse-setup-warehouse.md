---
title: Konfigurera lagerprocesser | Microsoft Docs
description: Ett företags distributionsstrategi återspeglas i konfigurationen av dess lagerprocesser. Detta omfattar att definiera hur olika artiklar hanteras på olika lagerställen, till exempel graden av styrning av lagerplats och omfattningen av arbetsflödet som krävs mellan lageraktiviteterna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: afb9f2d21b0b343846b2f0ba7143ea090433a8aa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195973"
---
# <a name="setting-up-warehouse-management"></a>Ställa in lagerstyrning
Ett företags distributionsstrategi återspeglas i konfigurationen av dess lagerprocesser. Detta omfattar att definiera hur olika artiklar hanteras på olika lagerställen, till exempel graden av styrning av lagerplats och omfattningen av arbetsflödet som krävs mellan lageraktiviteterna.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Få en översikt över möjligheterna med grundläggande och avancerade distributionslagerfunktioner.|[Designdetaljer: Översikt över distributionslager](design-details-warehouse-overview.md)|  
|Ställa in åtta olika typer av lagerplatstyper, till exempel Plockningslagerplats, för att definiera vilka flödesaktiviteter som gäller för respektive typ av lagerplats.|[Skapa lagerplatstyper](warehouse-how-to-set-up-bin-types.md)|  
|Skapa lagerplatser, antingen manuellt eller automatiskt med information, till exempel namn, nummerserie och kategori, enligt en lagerplatsmall.|[Skapa lagerplatser](warehouse-how-to-create-individual-bins.md)|  
|Definiera vilka artiklar som du vill lagra på en viss lagerplats och ställa in reglerna som bestämmer när lagerplatsen ska fyllas med en särskild artikel.|[Skapa lagerplatsinnehåll](warehouse-how-to-set-up-bin-contents.md)|  
|Ange att en artikel alltid placeras på en viss lagerplats.|[Tilldela standardlagerplatser till artiklar](warehouse-how-to-assign-default-bins-to-items.md)|
|Skapa mallar som styr var och hur artiklar införs vid dirigerad artikelinförsel.|[Skapa artikelinförselmallar](warehouse-how-to-set-up-put-away-templates.md)|
|Ange användare som anställda vid distributionslager vid särskilda platser.|[Registrera distributionslagerpersonal](warehouse-how-to-set-up-warehouse-employees.md)|
|Definiera olika typer av lagerplatser i lagret för att styra var artiklar placeras enligt typ, rangordning eller hanteringsnivå.|[Registrera lagerställen för att använda lagerplatser](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Göra fler inställningar för ett befintligt lagerställe för att aktivera det för lageraktiviteter.|[Konvertera befintliga lagerställen till distributionslagerplatser](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Aktivera plockning, flyttning och utflöde för monterings- eller produktionsorder i grundläggande distributionslagerkonfiguration.|[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Ställa in artiklar och lagerställen för den mest avancerade lagerstyrningen där alla aktiviteter måste följa ett strikt arbetsflöde.|[Registrera artiklar och platser för dirigerad artikelinförsel och plockning](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Definiera när och hur artiklar på lagerställen inventeras för underhålls- eller ekonomirapportering.|[Inventera, justera och omgruppera lager](inventory-how-count-adjust-reclassify.md)|
|Aktivera lagerarbetarna att dela upp en större enhet i mindre enheter för att uppfylla behoven hos källdokument.|[Aktivera automatisk volymnedbrytning med dirigerad artikelinförsel och plockning](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Ställa in lagret så att det alltid föreslår automatiskt att de artiklar som utgår först plockas först.|[Aktivera plockning med FEFO](warehouse-picking-by-fefo.md)|
|Få tips på hur du ordnar om lagerställen, lagerplatser eller zoner för att få mer effektiva lageraktiviteter.|[Omstrukturera lager](warehouse-how-to-restructure-warehouses.md)|
|Integrera streckkodsläsare i lösningen för hantering av lager. Endast för installation på plats.|[Använda ADCS (Automatiskt datainsamlingssystems)](warehouse-use-automated-data-capture-systems-adcs.md)|

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

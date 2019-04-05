---
title: Definiera relationen mellan kostnadstyper och redovisningskonton | Microsoft Docs
description: Lär dig hur du skapar relationen mellan kostnadstypen och redovisningskontot.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: f80e9b6276d26adffb5e3208ffefbf98d7f7ff96
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807125"
---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definiera relationen mellan kostnadstyper och redovisningskonton
Relationen mellan kostnadstypen och redovisningskontot skapas i kostnadstypen och i redovisningskontot.  

* Fältet **Redovisningskontointervall** i tabellen **Kostnadstyp** bestämmer vilka redovisningskonton som tillhör en kostnadstyp.  
* Fältet **Kostnadstypsnr.** i kontoplanen bestämmer vilken kostnadstyp ett redovisningskonto tillhör.  

Dessa två fält fylls i automatiskt när du använder funktionen **Hämta kostnadstyper från kontoplan**.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Relationen mellan redovisningskonton och kostnadstyper  
Det finns en många till en-relation mellan kostnadstyper och redovisningskonton. Flera redovisningskonton kan tillhöra en kostnadstyp, men varje redovisningskonto tillhör endast en kostnadstyp. Tabellen nedan beskriver informationen i sambandet.  

|Samband|**Redovisningskontointervall**|**Kostnadstypsnr**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Ett redovisningskonto för varje kostnadstyp|Ett redovisningskonton|En kostnadstyp|  
|Flera redovisningskonton för en kostnadstyp|Redovisningskontointervall, exempelvis 7110..7193 för varje redovisningskonto|För varje redovisningskonto i intervallet finns det bara en kostnadstyp|  
|Kostnadstyper utan motsvarande redovisningskonton|<Empty>||  
|Redovisningskonton vars transaktioner inte kommer att överföras||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kostnadstyper utan en relation till redovisningen  
En kostnadstyp kan inte ha en koppling till redovisningskonton, om ett av följande villkor gäller:  

* Konton för rörelseredovisning, till exempel Beräkna ränta och avskrivning, tar endast kostnader från rörelseredovisningen.  
* Hjälpkostnadstyper, till exempel kostnadstyper 9901, 9902 och 9903 i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)] används som kredit- och debetkonton för fördelningar.  
* Hjälpkontot 9920 i databasen [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller faktiska periodiseringar som visar skillnaden mellan kostnader och utgifterna från redovisningen.  

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)  
[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
[Om kostnadsredovisning](finance-about-cost-accounting.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

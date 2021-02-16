---
title: Designdetaljer – Bokföringsgränssnittsstruktur | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de globala procedurerna i bokföringsgränssnittsstruktur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e306b0caeb58bfe7bd04f93ac64d8b593f70f695
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751261"
---
# <a name="design-details-posting-interface-structure"></a>Designdetaljer: Bokföringsgränssnittsstruktur
I gränssnittstrukturen för bokföring i [!INCLUDE[prod_short](includes/prod_short.md)] finns det flera globala processer som använder samma struktur:  
  
* RunWithCheck och RunWithoutCheck anropar procedurkod – generiskt bokföringsgränssnitt för standardredovisningsjournalrad.  
* CustPostApplyCustLedgEntry – bokför kundapplikation, anropad från kodmodul 226 CustEntry – koppla bokförda transaktioner.  
* VendPostApplyVendLedgEntry – bokför koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner.  
* UnapplyCustLedgEntry – bokför borttagning av koppling av kundapplikation, anropad från kodmodul 226 CustEntry – koppla bokförda transaktioner  
* UnapplyVendLedgEntry – bokför borttagning av koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Bokföringsmotorstruktur](design-details-posting-engine-structure.md)
---
title: Designdetaljer – Bokföringsgränssnittsstruktur
description: Det här avsnittet innehåller en översikt över de globala procedurerna och designdetaljer i bokföringsgränssnittsstruktur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: bholtorf
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

[!INCLUDE[footer-include](includes/footer-banner.md)]

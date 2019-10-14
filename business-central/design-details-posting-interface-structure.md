---
title: Designdetaljer - Bokföringsgränssnittsstruktur | Microsoft Docs
description: Det här avsnittet innehåller en översikt över de globala procedurerna i bokföringsgränssnittsstruktur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f484c6474c840b4c2d802494407f8d819256596c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306946"
---
# <a name="design-details-posting-interface-structure"></a>Designdetaljer: Bokföringsgränssnittsstruktur
I gränssnittstrukturen för bokföring i [!INCLUDE[d365fin](includes/d365fin_md.md)] finns det flera globala processer som använder samma struktur:  
  
* RunWithCheck och RunWithoutCheck anropar procedurkod – generiskt bokföringsgränssnitt för standardredovisningsjournalrad.  
* CustPostApplyCustLedgEntry – bokför kundapplikation, anropad från kodmodul 226 CustEntry - koppla bokförda transaktioner.  
* VendPostApplyVendLedgEntry – bokför koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry – koppla bokförda transaktioner.  
* UnapplyCustLedgEntry – bokför borttagning av koppling av kundapplikation, anropad från kodmodul 226 CustEntry - koppla bokförda transaktioner  
* UnapplyVendLedgEntry – bokför borttagning av koppling av leverantörsapplikation, anropad från kodmodul 227 VendEntry - koppla bokförda transaktioner  
  
## <a name="see-also"></a>Se även  
[Designdetaljer: Bokföringsmotorstruktur](design-details-posting-engine-structure.md)
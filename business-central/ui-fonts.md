---
title: Tillgängliga teckensnitt
description: Lär dig mer om de förinstallerade teckensnitt som du kan använda för externa rapporter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 11/30/2021
ms.author: edupont
ms.openlocfilehash: faa581a88a6c7503c34177db459345a24638a95a
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334963"
---
# <a name="available-fonts"></a>Tillgängliga teckensnitt

Online-versionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller förinstallerade teckensnitt på de servrar som kan användas för att genererar rapporter. I följande avsnitt visas en disposition över vilka teckensnitt som är tillgängliga.

> [!NOTE]
> Av säkerhetsskäl kan du inte överföra anpassade teckensnitt till [!INCLUDE[prod_short](includes/prod_short.md)]-miljön.

## <a name="document-fonts"></a>Dokumentteckensnitt

Följande teckensnitt är installerade och tillgängliga att använda i rapportlayouter för såväl Word som RDLC:

* Arial
* Consolas
* Courier New
* Lucida Console
* Segoe Print
* Segoe Script
* Segoe UI
* Segoe UI Light
* Segoe UI Semilight
* Times New Roman

## <a name="fonts-for-checks"></a>Teckensnitt för kontroller

Magnetiskt bläcktecken igenkänningsteckensnitt (MICR) och de kan användas. Både E-13B och CMC-7 standarden stöds.  

Förutom MICR-teckensnitt finns speciella säkerhetsteckensnitt som du kan använda för att skapa text, namn, belopp och valutasymboler, euro, pund och yen som du kan manipulera med när en kontroll har skrivits ut.  

Mer information finns i [Välj en checklayout](finance-how-define-check-layouts.md).  

## <a name="fonts-for-barcodes"></a>Teckensnitt för streckkoder
Teckensnitt för att generera streckkoder finns installerade och tillgängliga att använda i både Word- och RDLC-rapportlayouter.

Följande endimensionella streckkodssymboler stöds:
* Kod 3 av 9 (kod 39)
* Kod 128
* Kod 93
* Codabar
* MSI
* Interfolierade 2 av 5

Följande tvådimensionella streckkodssymboler stöds:
* Aztec
* Datamatris
* Maxicode
* PDF417
* QR

Mer information finns i avsnittet [Streckkodsteckensnitt med Business Central Online](/dynamics365/business-central/dev-itpro/developer/devenv-report-barcode-fonts).

## <a name="see-also"></a>Se även

[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Välj en kontrollayout](finance-how-define-check-layouts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
[Streckkodsteckensnitt med Business Central Online](/dynamics365/business-central/dev-itpro/developer/devenv-report-barcode-fonts)

[!INCLUDE[footer-include](includes/footer-banner.md)]

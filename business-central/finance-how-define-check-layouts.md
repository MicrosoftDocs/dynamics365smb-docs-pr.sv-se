---
title: Ange layouten för en kontroll | Microsoft Docs
description: Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 02/20/2020
ms.author: edupont
ms.openlocfilehash: df141f15eda20b1c3ce17e12e726f79a20532915
ms.sourcegitcommit: 35552b250b37c97772129d1cb9fd9e2537c83824
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "3097750"
---
# <a name="select-a-check-layout"></a>Välj en checklayout
Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna. Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.

Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.

## <a name="to-select-a-check-layout"></a>Välj en checklayout genom att
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Rapportval - bankkonto** och välj sedan relaterad länk.
2. På sidan **Rapportval - bankkonto** i fältet **Användning** väljer du **Check**.
3. Välj något av följande rapport-ID:

| Rapport-ID | Rapportnamn | Beskrivning |
| --- | --- | --- |
| 1401 |Check |Detta är standardrapporten. |
| 10411 |Check (checktalong/checktalong/check) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check. |
| 10412 |Check (checktalong/check/checktalong) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/check/checktalong. |
| 10413 |Tre checkar per sida |Den här rapporten är utformad för att skriva ut tre checkar på varje sida. |

När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**. Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).

Om du vill ändra en av dessa standardlayouter använder du antingen Word- eller RDLC-integration. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Använda MICR och säkerhetsteckensnitt
Online-versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller förinstallerade teckensnitt på de servrar som kan användas för att definiera kontrollera layouter. I följande text konturer finns tillgängliga teckensnitt som innehåller länkar till detaljerad information om de olika leverantörerna av teckensnitten från tredje part.

> [!Important]
> MICR och kontrollera säkerhetsteckensnitt i Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] licensieras i ett teckensnittspaket från IDAutomation.com, Inc. Dessa produkter får endast användas som en del av och i samband med Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].

I uppdatering 15.3 och nyare installeras magnetiskt bläcktecken igenkänningsteckensnitt (MICR) och de kan användas. Både E-13B och CMC-7 standarden stöds. Förutom MICR-teckensnitt finns speciella säkerhetsteckensnitt som du kan använda för att skapa text, namn, belopp och valutasymboler, euro, pund och yen som du kan manipulera med när en kontroll har skrivits ut.

> [!NOTE]
> Av säkerhetsskäl kan du inte överföra anpassade teckensnitt till [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljön.

### <a name="micr-e-13b-specifications"></a>MICR E-13B specifikationer
I följande avsnitt sammanfattas specifikationerna för de MICR-E-13B teckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.

![MICR E-13B specifikationer](media/font_MICR_E-13B_Specifications.png "MICR E-13B specifikationer")

Den fullständiga specifikationen av MICR E-13B teckensnitt finns i leverantörens dokumentation här: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7 specifikationer
Följande CMC-7 teckensnitt finns tillgängliga [!INCLUDE[d365fin](includes/d365fin_md.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
-   IDAutomationCMC7n40

I följande avsnitt sammanfattas specifikationerna för de MICR CMC-7 teckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.

![MICR CMC-7 specifikationer](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 specifikationer")

Den fullständiga specifikationen av MICR CMC-7 teckensnitt finns i leverantörens dokumentation här: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Specifikationer för säkra teckensnitt
I följande avsnitt sammanfattas specifikationerna för kontrollera säkerhetsteckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.

![Kontrollera specifikationer för säkerhetsteckensnitt](media/font_check-security-font_Specifications.png "Kontrollera specifikationer för säkerhetsteckensnitt")

Den fullständiga specifikationen av kontrollera säkerhetsteckensnitt finns i leverantörens dokumentation här: (https://www.idautomation.com/security-fonts/).

Det finns också teckensnitt för andra syften i [!INCLUDE[prodshort](includes/prodshort.md)]. Mer information finns i [tillgängliga teckensnitt](ui-fonts.md)

## <a name="see-also"></a>Se även
[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)  
[Teckensnitt i Business Central](ui-fonts.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Stämma av bankkonton](bank-manage-bank-accounts.md)   
[Slutföra periodslutsprocesser](year-how-complete-period-end-processes.md)  
[Arbeta med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

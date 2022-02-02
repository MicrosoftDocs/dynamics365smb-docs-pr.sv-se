---
title: Ange layouten för en kontroll
description: Du kan skapa och skriva ut dina checkar i flera olika format i överensstämmelse med standarder som anges av dina lokala myndigheter.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.search.form: 374, 404
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4278cb474440e8746bcc423c3dd10dbc209fdb9a
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971671"
---
# <a name="select-a-check-layout"></a>Välj en checklayout

Du kan designa dina checkar så att de uppfyller de normer som fastställts av de lokala myndigheterna. Checkbilder kan vara skrivna ut på engelska, franska, eller spanska.

Checkar har utformats för att skrivas ut i både amerikanska och kanadensiska checkbildformat i antingen check-checktalong-check-format eller checktalong-checktalong-check-format.

## <a name="to-select-a-check-layout"></a>Välj en checklayout genom att

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Rapportval, bankkonto** och väljer sedan relaterad länk.
2. På sidan **Rapportval – bankkonto** i fältet **Användning** väljer du **Check**.
3. Välj något av följande rapport-ID:

| Rapport-ID | Rapportnamn | Beskrivning |
| --- | --- | --- |
| 1401 |Check |Detta är standardrapporten. |
| 10411 |Check (checktalong/checktalong/check) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/checktalong/check. |
| 10412 |Check (checktalong/check/checktalong) |Den här rapporten är utformad för att skriva ut checkar i formatet checktalong/check/checktalong. |
| 10413 |Tre checkar per sida |Den här rapporten är utformad för att skriva ut tre checkar på varje sida. |

När du har upprättat checklayouter, kan du skriva ut checkar från sidan **utbetalningsjournal**. Mer information finns i [Arbeta med checkar](payables-how-work-checks.md).

Om du vill ändra en av dessa standardlayouter använder du antingen Word- eller RDLC-integrering. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Använda MICR och säkerhetsteckensnitt

Online-versionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller förinstallerade teckensnitt på de servrar som kan användas för att definiera kontrollera layouter. I följande text konturer finns tillgängliga teckensnitt som innehåller länkar till detaljerad information om de olika leverantörerna av teckensnitten från tredje part.

> [!Important]
> MICR och kontrollera säkerhetsteckensnitt i Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] licensieras i ett teckensnittspaket från IDAutomation.com, Inc. Dessa produkter får endast användas som en del av och i samband med Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].

I uppdatering 15.3 och nyare installeras magnetiskt bläcktecken igenkänningsteckensnitt (MICR) och de kan användas. Både E-13B och CMC-7 standarden stöds. Förutom MICR-teckensnitt finns speciella säkerhetsteckensnitt som du kan använda för att skapa text, namn, belopp och valutasymboler, euro, pund och yen som du kan manipulera med när en kontroll har skrivits ut.

> [!NOTE]
> Av säkerhetsskäl kan du inte överföra anpassade teckensnitt till [!INCLUDE[prod_short](includes/prod_short.md)]-miljön.

### <a name="micr-e-13b-specifications"></a>MICR E-13B specifikationer

I följande avsnitt sammanfattas specifikationerna för de MICR-E-13B teckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.

![MICR E-13B specifikationer.](media/font_MICR_E-13B_Specifications.png "MICR E-13B specifikationer")

### <a name="delimiter-characters"></a>Avgränsningstecken

![Avgränsningstecken.](media/font-micr-letters.png "Avgränsningstecken")

Den fullständiga specifikationen av MICR E-13B teckensnitt finns i leverantörens dokumentation här: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7 specifikationer

Följande CMC-7 teckensnitt finns tillgängliga [!INCLUDE[prod_short](includes/prod_short.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

I följande avsnitt sammanfattas specifikationerna för de MICR CMC-7 teckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.

![MICR CMC-7 specifikationer.](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 specifikationer")

### <a name="delimiter-characters"></a>Avgränsningstecken

![Avgränsningstecken för CMC-7.](media/font-cmc7-letters.png "Avgränsningstecken för CMC-7")

Den fullständiga specifikationen av MICR CMC-7 teckensnitt finns i leverantörens dokumentation här: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Specifikationer för säkra teckensnitt

I följande avsnitt sammanfattas specifikationerna för kontrollera säkerhetsteckensnitt som kan vara användbara när teckensnitt kalibreras för att kontrollera layouter med specifika MICR-skrivare.

![Kontrollera specifikationer för säkerhetsteckensnitt.](media/font_check-security-font_Specifications.png "Kontrollera specifikationer för säkerhetsteckensnitt")

Den fullständiga specifikationen av kontrollera säkerhetsteckensnitt finns i leverantörens dokumentation här: (https://www.idautomation.com/security-fonts/).

Det finns också teckensnitt för andra syften i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [tillgängliga teckensnitt](ui-fonts.md)

## <a name="see-also"></a>Se även

[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)  
[Teckensnitt i Business Central](ui-fonts.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Stämma av bankkonton](bank-manage-bank-accounts.md)   
[Slutföra periodslutsprocesser](year-how-complete-period-end-processes.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
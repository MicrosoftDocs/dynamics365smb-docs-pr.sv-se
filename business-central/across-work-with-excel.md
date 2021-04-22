---
title: Visa och redigera i Excel från Business Central
description: Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786938"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visa och redigera i Excel från Business Central

Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel. För att göra detta har du två alternativ. Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan. Skillnaden mellan de två åtgärderna beskrivs nedan:  

## <a name="open-in-excel"></a>Öppna i Excel

- Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas. Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prod_short](includes/prod_short.md)].

- Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bara spara ändringarna till Excel-filen på datorn.

- Den här åtgärden fungerar både i Windows och macOS.

> [!NOTE]
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard. Om du däremot ställer in [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.

## <a name="edit-in-excel"></a>Redigera i Excel

- Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar posterna som visas, varför Excel-arbetsboken kommer att innehålla nästan samma poster och kolumner.

- Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prod_short](includes/prod_short.md)].

- Det fungerar endast i Windows. inte macOS.

- Du kan växla företaget som du arbetar med. För att byta företag väljer du ikonen **Alternativ** ![Inställningar för Excel-tillägg](media/cogwheel.png "Alternativ för Excel-tillägg") i Excel-tilläggsfönstret och markerar sedan företaget i fältet **Företag**.  

    > [!IMPORTANT]
    > Kontrollera att fältet **Miljö** fältet inte är tomt när du byter företag. Om så är fallet gör du det till ett av de tillgängliga alternativen, annars kommer tillägget inte att fungera korrekt.  

Om du gör ändringar i tillägget måste du ladda det på nytt för att uppdatera anslutningen. Om du vill läsa in på nytt använder du ![menyn tilläggsprogram för Excel](media/excel-addin-menu.png "Meny Excel tillägg") i det övre högra hörnet i tillägget. Om du inte kan läsa in tillägget, kontakta administratören. Om du är administratör, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören, och det är då endast tillgängligt för webbklienten. För administratörer: Om du vill veta hur du installerar Excel-tillägget, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Se skillnaden mellan alternativen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med Business Central](ui-work-product.md)  
[Förbättringar av Excel-integrering i 2019 utgivningsplan, våg 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
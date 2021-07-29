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
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443487"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visa och redigera i Excel från Business Central

Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel. Beroende på sidan finns det två alternativ för att visa i Excel. Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan. I den här artikeln beskrivs skillnaderna mellan de två åtgärderna.

## <a name="open-in-excel"></a>Öppna i Excel

Med instruktionen **Öppna i Excel** kan du göra ändringar i posterna i Excel, men du kan inte publicera tillbaka ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bara spara ändringarna till Excel-filen på datorn.

- Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas. Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prod_short](includes/prod_short.md)].

- Den här åtgärden fungerar både i Windows och macOS.

- Från och med uppdatering 18.3 kan du även visa listor som visas i sid delar, till exempel raderna i en försäljningsorder. Denna funktion är en valfri funktion, som kräver att du aktiverar export av list delar till **Exportera valfri listdel till Excel** i **funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard. Om du däremot ställer in [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Redigera i Excel

Med instruktionen **Redigera i Excel** kan du göra ändringar i posterna i Excel, men du kan inte publicera tillbaka ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)].

- Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar posterna som visas, varför Excel-arbetsboken kommer att innehålla nästan samma poster och kolumner.

- Det fungerar endast i Windows. inte macOS.

- Du kan växla företaget som du arbetar med. Om du vill byta företag väljer du ikonen **alternativ** för ![Excel-tillägget.](media/cogwheel.png "Alternativ för Excel-tillägg") i fönstret Excel-tillägg markerar du företaget från fältet **företag**.  

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
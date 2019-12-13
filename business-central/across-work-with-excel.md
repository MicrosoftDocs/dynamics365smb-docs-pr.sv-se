---
title: Visa och redigera i Excel från Business Central | Microsoft-dokument
description: Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 99fe339426b755b70983d8ec9345858357043347
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808751"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visa och redigera i Excel från Business Central

Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel. För att göra detta har du två alternativ. Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan. Skillnaden mellan de två åtgärderna beskrivs nedan:  

## <a name="open-in-excel"></a>Öppna i Excel

- Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas. Detta innebär att Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prodshort](includes/prodshort.md)].

- Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan bara spara ändringarna till Excel-filen på datorn. 

- Den här åtgärden fungerar både i Windows och macOS. 

> [!NOTE]
> För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard. Om du däremot ställer in [!INCLUDE [prodshort](includes/prodshort.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.

## <a name="edit-in-excel"></a>Redigera i Excel

- Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar poster som visas. Detta innebär att Excel-arbetsboken innehåller nästan samma poster och kolumner.

- Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].

- Det fungerar endast i Windows. inte macOS.

Detta utökades i 2019 års version, våg 2. Mer information finns i [Förbättringar av Excel-integrering](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören. För administratörer, om du vill veta hur du installerar Excel-tillägg, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt är den här funktionen är endast tillgänglig för webbklienten.

### <a name="see-the-differences-between-the-options"></a>Se skillnaden mellan alternativen 
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Se även
[Arbeta med Business Central](ui-work-product.md)  

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
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 2474f83fd9fa137b40756a3d07ac025208f3ac6c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308266"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visa och redigera i Excel från Business Central 

Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du även visa posterna med hjälp av Microsoft Excel. För att göra detta har du två alternativ. Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan. Skillnaden mellan de två åtgärderna beskrivs nedan:  

## <a name="open-in-excel"></a>Öppna i Excel

-    Med den här åtgärden respekterar Excel eventuella filter på sidan gränsen på poster som visas. Detta innebär att Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prodshort](includes/prodshort.md)].

-    Du kan inte ändra posterna i Excel, men du kan inte publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan bara spara ändringarna till Excel-filen på datorn. 

-    Den här åtgärden fungerar både i Windows och macOS. 

>[!NOTE]
>För [!INCLUDE[prodshort](includes/prodshort.md)] lokal, är åtgärden **Öppen i Excel** inte tillgänglig om åtgärden **redigera i Excel** är.

## <a name="edit-in-excel"></a>Redigera i Excel

-    Med den här åtgärden respekterar Excel-arbetsboken inte filter på sidan gränsen på poster som visas. Detta innebär att Excel-arbetsboken innehåller alla tillgängliga poster och kolumner, oavsett vad som ska visas på sidan. 

-    Fördelen med åtgärden **redigera i Excel** är att du kan ändra poster i Excel och sedan publicera ändringarna tillbaka till [!INCLUDE[prodshort](includes/prodshort.md)].

-    Det fungerar endast i Windows. inte macOS.

>[!NOTE]
>För [!INCLUDE[prodshort](includes/prodshort.md)] lokal, är åtgärden **redigera i Excel** endast tillgänglig om Excel-tillägget har installerats av administratören. För administratörer, om du vill veta hur du installerar Excel-tillägg, se [ställa in Excel-tillägget](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Se skillnaden mellan alternativen 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Se även
[Arbeta med Business Central](ui-work-product.md)  

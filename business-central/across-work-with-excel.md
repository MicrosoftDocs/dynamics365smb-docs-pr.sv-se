---
title: "Visa och redigera i Excel från Business Central | Microsoft-dokument"
description: "Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.contentlocale: sv-se
ms.lasthandoff: 01/22/2019

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

## <a name="see-also"></a>Se även

[Arbeta med Business Central](ui-work-product.md)  


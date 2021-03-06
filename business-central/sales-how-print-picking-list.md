---
title: Skriva ut en lagerplockningslista från en försäljningsorder
description: Du kan skriva ut en lagerplocklista direkt från en försäljningsorder, försäljningsfaktura och andra utgående försäljningsdokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4cddce48df3be0a3fadaa74ed751b274ccce7f31
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115467"
---
# <a name="print-the-picking-list"></a>Skriv ut plocklistan

Du kan skriva ut en lagerplockningslista direkt från en försäljningsorder och andra dokument som inleder leverans av varor.

Den här rapporten används vanligtvis i företag utan dedikerad funktionalitet för lagerstyrning, så att en lager arbetare enkelt kan visa eller skriva ut plocklistan från det relaterade försäljningsdokumentet. I företag med högre volym eller mer komplexa processer planeras och utförs plockningen i dedikerade distributions lagerdokument. Mer information finns i [Plocka artiklar](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>För att skriva ut en plockningslista från en försäljningsorder

Följande procedur är baserad på en försäljningsorder. Stegen är liknande för alla andra dokument som kan användas för att initiera leverans av artiklar, såsom överföringsorder.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), ange **försäljningsorder** och välj sedan relaterad länk.  
2. Öppna en försäljningsorder som du vill plocka artiklar för.  
3. Välj åtgärden **Rapport** och sedan åtgärden **Plockningslista efter order**.  
4. Välj **Skriv ut** för att skriva ut plockningslistan eller välj **Förhandsgranska** på för att visa den på skärmen.

Du kan också spara plockningslistan som ett dokument, t. ex. skicka till någon eller lägga till en bilaga till försäljningsordern. För mer information, se [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).

> [!NOTE]
> Om du använde funktionen **Expandera struktur** på försäljningsordern visas bara komponenterna för den relaterade monteringsartikeln i rapporten. Mer information finns i [Arbeta med strukturer](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Se även

[Lager](inventory-manage-inventory.md)  
[Plocka artiklar](warehouse-pick-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Skriva ut en plockningslista från en försäljningsorder
description: 'Du kan skriva ut en lagerplocklista direkt från en försäljningsorder, försäljningsfaktura och andra utgående försäljningsdokument.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="print-the-picking-list" />Skriv ut plocklistan

Du kan skriva ut en lagerplockningslista direkt från en försäljningsorder och andra dokument som inleder leverans av varor.

Den här rapporten används vanligtvis i företag utan dedikerad funktionalitet för Warehouse Management, så att en lager arbetare kan visa eller skriva ut plocklistan från det relaterade försäljningsdokumentet. I företag med högre volym eller mer komplexa processer planeras och utförs leverans och plockning i dedikerade distributionslagerdokument. Läs mer i [Avgående distributionslagerflöde](design-details-outbound-warehouse-flow.md).

## <a name="to-print-a-picking-list-from-a-sales-order" />För att skriva ut en plockningslista från en försäljningsorder

Följande procedur är baserad på en försäljningsorder. Stegen är liknande för alla andra dokument som kan användas för att initiera leverans av artiklar, såsom överföringsorder.

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Öppna en försäljningsorder som du vill plocka artiklar för.  
3. Välj åtgärden **Rapport** och sedan åtgärden **Plockningslista efter order**.  
4. Välj **Skriv ut** för att skriva ut plockningslistan eller välj **Förhandsgranska** på för att visa den på skärmen.

Du kan också spara plockningslistan som ett dokument, t. ex. skicka till någon eller lägga till en bilaga till försäljningsordern. Se mer på [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).

> [!NOTE]
> Om du använde funktionen **Expandera struktur** på försäljningsordern visas bara komponenterna för den relaterade monteringsartikeln i rapporten. Mer information finns i [Arbeta med strukturer](inventory-how-work-BOMs.md).

## <a name="see-also" />Se även

[Lager](inventory-manage-inventory.md)  
[Avgående distributionslagerflöde](design-details-outbound-warehouse-flow.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

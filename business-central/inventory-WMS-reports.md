---
title: Lager- och distributionslagerrapporter och -analyser
description: Se vilka lager- och distributionslagerrapporter och -analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på din verksamhet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 04/13/2023
ms.custom: bap-template
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Lager- och distributionslagerrapporter och -analyser

Lager- och distributionslagerrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gör att lager- och affärspersonal få insikter och statistik om aktuella och tidigare lager- och distributionslageraktiviteter.  

## <a name="reports"></a>Rapporter

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Uppgifter

I följande artiklar beskrivs några av de viktigaste uppgifterna för att analysera verksamhetens tillstånd:

* [Skapa analysrapporter](bi-how-create-analysis-views-reports.md)  
* [Visa artikeldisposition](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Skriva ut och skanna streckkoder

Med hjälp av streckkoder kan du effektivisera dina inkommande, utgående och interna lagerprocesser. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

När du har installerat appen kan du använda åtgärden **Skriv ut etikett** för att skriva ut 1D- och 2D-streckkoder från sidorna i följande tabell.

|Sida  |Fältvärden som streckkoder kan innehålla  |
|---------|---------|
|Artiklar, artikelkort     |Artikelnummer, beskrivning och GTIN         |
|Artikelreferenslista, Artikelreferens     |Artikelnr., Beskrivning, Måttenhet och Referensnr.         |
|Parti nr. informationslista, partinr. etikett     |Artikelnr, Beskrivning och Partinummer       |
|SN-etikett     |Nr., Beskrivning och Serienummer         |

> [!NOTE]
> Vissa skrivare och streckkods-/QR-kodformat kräver en specifik implementering. Du kan behöva ladda upp en annan Word-mall eller klona rapporten för att skapa en egen anpassad version.

## <a name="see-also"></a>Se även

[Ställa in lager](inventory-setup-inventory.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Hantering av distributionslager – översikt](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

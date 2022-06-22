---
title: Rapportval i Business Central
description: Mer information om hur du ställer in de rapporter som du använder för att skriva ut olika typer av dokument i Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 03/11/2022
ms.author: edupont
ms.openlocfilehash: 9106b1ac3f6b179e26c8dfb01212b88e92b694fe
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950205"
---
# <a name="report-selection-in-business-central"></a>Rapportval i Business Central

Du kan ställa in standardrapporter som ska användas för att skriva ut dokument för försäljning och inköp, till exempel order, offerter och fakturor. Om du t. ex. har en särskild layout för försäljningsfakturor kan du ange rapporten på sidan **Rapporturval – Försäljning** så att den används för att skicka eller skriva ut försäljningsfakturor.  

Sidorna för **rapporturval** anger vilken rapport som ska skrivas ut i olika situationer. [!INCLUDE [prod_short](includes/prod_short.md)] tillhandahåller standardkonfigurationer, men du kan ändra dem om det behövs. Du kan också lägga till rapporter på sidorna för **Rapporturval** om du exempelvis vill skriva ut mer än en rapport per dokumenttyp.  

## <a name="available-report-selections"></a>Tillgängliga rapporturval

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller olika **Rapporturval**-sidor för olika områden. I följande tabeller beskrivs var du kan hitta information om de olika sidorna.  

|Område eller uppgift  |Läs mer|
|--------------|----------|
|Exempel på hur rapporturval fungerar (försäljning)|[Rapportval för försäljningsdokument](#example-report-selection-for-sales-documents)|
|Standardlayout för e-post med försäljnings- och inköpsdokument  |[Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definiera kontrollayouter     |[Välj en checklayout](finance-how-define-check-layouts.md) |
|Definiera rapporter för momsrapportering (Tyskland)|[Ställ in rapporter för moms och Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Ditt [!INCLUDE [prod_short](includes/prod_short.md)] kan lägga till ytterligare sidor för **Rapporturval**, beroende exempelvis på plats och bransch. Du kan alltid kontrollera inställningarna genom att välja den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Rapportval** och väljer sedan relaterad länk.

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller följande sidor om **Rapportavsnitt**:

* **Rapportval – Försäljning**  
* **Rapportval – Inköp**  
* **Rapportval – Lager**  
* **Rapportval – Kassaflöde**  
* **Rapportval – Distributionslager**  
* **Rapportval – Bankkonto**  
* **Rapportval – Påminnelse/ränta**  
* **Rapportval – Projekt**  

## <a name="example-report-selection-for-sales-documents"></a>Exempel: Rapportval för försäljningsdokument

Sidan **Rapportval – Försäljning** definierar de standardrapporter som ska användas i olika scenarier för varje relaterad dokumenttyp. Välj en dokumenttyp i fältet **Användning** och lägg sedan till eller granska rapportvalet. Du kan konfigurera mer än en rapport och i vilken ordning rapporterna ska skickas eller skrivas ut.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Vissa typer av dokument kan skickas som e-postbilagor, andra inte. Om en typ av dokument kan skickas med e-post kommer **Rapportval** att innehålla extra fält.  

På sidorna **Rapporturval – Försäljning** och **Rapporturval – Inköp** hjälper följande fält dig att konfigurera e-post:

|Fältnamn |Description  |
|-----------|-------------|
|**Använd till brödtext i e-post**| Infoga sammanfattad information, till exempel faktura nummer, förfallodatum och betalningstjänstlänk, i ett e-postmeddelande.        |
|**Använd till e-postbilaga**| Bifoga det relaterade dokumentet till e-postmeddelandet.|
|**Beskrivning av layouten på brödtext i e-post**|Ange vilken brödtext i e-post som ska användas. Layouten är oftast en egen layout för rapporter. |

## <a name="see-also"></a>Se även

[Ställ in återanvändbara e-posttexter och layouter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Välj en kontrollayout](finance-how-define-check-layouts.md)  
[Ställ in rapporter för moms och Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md)  
[Ställa in skrivare](ui-specify-printer-selection-reports.md)  
[Ekonomisk rapportering och analys i Business Central](finance-reports.md)  
[Kundreskontrarapporter och analyser i Business Central](receivables-reports.md) 
[Leverantörsreskontrarapporter och analyser i Business Central](payables-reports.md)  
[Rapporter och analyser för anläggningstillgångar i Business Central](fa-reports.md)  
[Projektrapporter och analyser i Business Central](project-reports.md)  
[Försäljningsrapporter och analyser i Business Central](sales-reports.md)  
[Inköpsrapporter och analyser i Business Central](purchase-reports.md)  
[Lager- och distributionslagerrapporter och -analyser i Business Central](inventory-WMS-reports.md)  
[Monteringsrapporter och analyser i Business Central](assembly-reports.md)  
[Produktionsrapporter och analyser i Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
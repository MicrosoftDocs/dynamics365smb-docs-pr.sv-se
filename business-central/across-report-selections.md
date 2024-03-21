---
title: Rapportval i Business Central
description: Mer information om hur du ställer in de rapporter som du använder för att skriva ut olika typer av dokument i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="report-selection-for-documents-in-business-central"></a>Rapporturval för dokument i Business Central

Du kan ställa in standardrapporter som ska användas för att skriva ut dokument för försäljning, inköp och service, till exempel order, offerter och fakturor. Om du t. ex. har en särskild layout för försäljningsfakturor kan du ange rapporten på sidan **Rapporturval – Försäljning** så att den används för att skicka eller skriva ut försäljningsfakturor.  

## <a name="available-report-selections"></a>Tillgängliga rapporturval

Sidorna för **rapporturval** anger vilken rapport som ska skrivas ut i olika situationer. [!INCLUDE [prod_short](includes/prod_short.md)] tillhandahåller standardkonfigurationer, men du kan ändra dem om det behövs. Du kan också lägga till rapporter på sidorna för **Rapporturval** om du exempelvis vill skriva ut mer än en rapport per dokumenttyp. 

I följande tabeller beskrivs var du kan hitta information om de olika sidorna.  

|Område eller uppgift  |Läs mer|
|--------------|----------|
|Exempel på hur rapporturval fungerar (försäljning)|[Rapporturval för försäljningsdokument](#example-report-selection-for-sales-documents) hittas nedan|
|Standardlayout för e-post med försäljnings- och inköpsdokument  |[Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definiera kontrollayouter     |[Välj en kontrollayout](finance-how-define-check-layouts.md) |
|Definiera rapporter för momsrapportering (Tyskland)|[Ställ in rapporter för moms och Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Ditt [!INCLUDE [prod_short](includes/prod_short.md)] kan lägga till ytterligare sidor för **Rapporturval**, beroende exempelvis på plats och bransch. Kontrollera konfigurationen genom att välja ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Rapporturval** och väljer sedan relaterad länk.

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller följande sidor om **Rapporturval**:

* **Rapportval – Försäljning**  
* **Rapportval – Inköp**  
* **Rapportval – Lager**  
* **Rapportval – Kassaflöde**  
* **Rapportval – Distributionslager**  
* **Rapportval – Bankkonto**  
* **Rapportval – Projekt**  
* **Rapportval - service**

## <a name="example-report-selection-for-sales-documents"></a>Exempel: Rapportval för försäljningsdokument

Sidan **Rapportval – Försäljning** erbjuder standardrapporter som ska användas i olika scenarier för varje relaterad dokumenttyp. Välj en dokumenttyp i fältet **Användning** och lägg sedan till eller granska rapporturvalet. Du kan konfigurera mer än en rapport och specificera den ordning rapporterna ska skickas eller skrivas ut.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Du kan inte skicka alla typer av dokument som e-postbilagor, För dem du kan det innehåller sidan **Rapporturval** extra fält.  

På sidorna **Rapporturval – Försäljning** och **Rapporturval – Inköp** hjälper följande fält dig att konfigurera e-post:

|Fältnamn |Description  |
|-----------|-------------|
|**Använd till brödtext i e-post**| Infoga sammanfattad information, till exempel fakturanummer, förfallodatum eller en länk till en betalningstjänst, i ett e-postmeddelande.        |
|**Använd till e-postbilaga**| Bifoga det relaterade dokumentet till e-postmeddelandet.|
|**Beskrivning av layouten på brödtext i e-post**|Ange vilken brödtext i e-post som ska användas. Oftast är det en egen layout för rapporter. |

## <a name="see-also"></a>Se även

[Ställ in återanvändbara e-posttexter och layouter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Välj en kontrollayout](finance-how-define-check-layouts.md)  
[Ställ in rapporter för moms och Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md)  
[Ställa in skrivare](ui-specify-printer-selection-reports.md)  
[Ekonomisk rapportering och analys i Business Central](finance-reports.md)  
[Kundreskontrarapporter och analys i Business Central](receivables-reports.md)  
[Leverantörsreskontrarapporter och analys i Business Central](payables-reports.md)  
[Rapporter och analyser för anläggningstillgångar i Business Central](fa-reports.md)  
[Projektrapporter och analyser i Business Central](project-reports.md)  
[Försäljningsrapporter och analyser i Business Central](sales-reports.md)  
[Inköpsrapporter och analyser i Business Central](purchase-reports.md)  
[Lager- och distributionslagerrapporter och -analyser i Business Central](inventory-WMS-reports.md)  
[Monteringsrapporter och analyser i Business Central](assembly-reports.md)  
[Produktionsrapporter och analyser i Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

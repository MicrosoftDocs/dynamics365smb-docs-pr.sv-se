---
title: Rapportval i Business Central
description: Mer information om hur du ställer in de rapporter som du använder för att skriva ut olika typer av dokument i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: 9d282ea35f7b4bdf317e818504f061d4145404bd
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379004"
---
# <a name="report-selection-in-business-central"></a>Rapportval i Business Central

Du kan konfigurera standardrapporter som ska användas för att skriva ut de olika dokumenten för försäljning och inköp, exempelvis order, offerter, fakturor och kreditnotor. Om du t. ex. har en särskild layout för försäljningsfakturor kan du ange rapporten på sidan **Rapporturval - Försäljning** så att den används för att skicka eller skriva ut försäljningsfakturor.  

Sidorna för **rapporturval** anger vilken rapport som ska skrivas ut i olika situationer. [!INCLUDE [prod_short](includes/prod_short.md)] innehåller standardkonfigurationer, men naturligtvis kan du ändra dessa standardvärden. Du kan också lägga till rapporter på sidorna för **Rapporturval** om du exempelvis vill skriva ut mer än en rapport per dokumenttyp.  

## <a name="available-report-selections"></a>Tillgängliga rapporturval

[!INCLUDE [prod_short](includes/prod_short.md)] innehåller olika **Rapporturval**-sidor för olika områden. I följande tabeller beskrivs var du kan hitta information om de olika sidorna.  

|Område eller uppgift  |Läs mer|
|--------------|----------|
|Exempel på hur rapporturval fungerar (försäljning)|[Rapportval för försäljningsdokument](#example-report-selection-for-sales-documents)|
|Standardlayout för e-post med försäljnings- och inköpsdokument  |[Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Definiera kontrollayouter     |[Välj en checklayout](finance-how-define-check-layouts.md) |
|Definiera rapporter för momsrapportering (Tyskland)|[Ställ in rapporter för moms och Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Ditt [!INCLUDE [prod_short](includes/prod_short.md)] kan lägga till ytterligare sidor för **Rapporturval**, beroende exempelvis på plats och bransch. Du kan alltid kontrollera inställningarna genom att välja ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Rapportera val** och sedan välja önskad länk.

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller följande sidor om **Rapportavsnitt**:

* **Rapportval - Försäljning**  
* **Rapportval - Inköp**  
* **Rapportval - Lager**  
* **Rapportval - Kassaflöde**  
* **Rapportval - Distributionslager**  
* **Rapportval - Bankkonto**  
* **Rapportval - Påminnelse/ränta**  

## <a name="example-report-selection-for-sales-documents"></a>Exempel: Rapportval för försäljningsdokument

Sidan **Rapportval - Försäljning** definierar de standardrapporter som ska användas i olika scenarier för varje relaterad dokumenttyp. Välj en dokumenttyp i fältet **Användning** och lägg sedan till eller granska rapportvalet. Du kan konfigurera mer än en rapport och i vilken ordning rapporterna ska skickas eller skrivas ut.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Vissa typer av dokument kan skickas som e-postbilagor, andra inte. Varje sida för **Rapporturval** visar ytterligare fält om typen stöder e-post direkt.  

På sidorna **Rapporturval - Försäljning** och **Rapporturval - Inköp** hjälper följande fält dig att konfigurera e-post:

|Fältnamn |Beskrivning  |
|-----------|-------------|
|**Använd till brödtext i e-post**| Anger att sammanfattad information, t. ex. fakturanummer, förfallodatum och betalningstjänstlänken, kommer att infogas i brödtexten i det e-postmeddelande du skickar.        |
|**Använd till e-postbilaga**| Anger att det relaterade dokumentet kommer att bifogas i e-postmeddelandet.|
|**Beskrivning av layouten på brödtext i e-post**|Anger den layout för e-postbrödtext som används, vanligtvis en anpassad rapportlayout. |

## <a name="see-also"></a>Se även

[Konfigurera återanvändbara e-posttexter och layouter för försäljnings- och inköpsdokument](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Välj en kontrollayout](finance-how-define-check-layouts.md)  
[Ställ in rapporter för moms och Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Definiera dokumentlayout för kunder och leverantörer](ui-define-customer-vendor-document-layouts.md)  
[Ställa in skrivare](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
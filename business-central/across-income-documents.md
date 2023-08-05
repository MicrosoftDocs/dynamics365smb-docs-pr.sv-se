---
title: Arbeta med inkommande dokument
description: 'Du kan hantera inkommande externa företagsdokument, som till exempel betalningsinleveranser eller PDF-filer, hantera OCR-uppgifter och konvertera filer till elektroniska dokument och poster.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# Inkommande dokument

Externa affärsdokument kan komma till ditt företag som en e-postbilaga eller papperskopia som du skannar för att spara. Det här scenariot är typiskt för inköp där sådana inkommande dokument representerar betalningkvitton för kostnader eller små inköp.

På sidan **Inkommande dokument** använder du olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.

## Användningsscenario

Du kan registrera filer och pappers kopior som tagits emot från dina handelspartner i [!INCLUDE[prod_short](includes/prod_short.md)] och skapa en dokument post. Till exempel en inköps- eller försäljningsfaktura, kreditnota eller en journalrad.

Överför de mottagna filerna eller använd enhetens kamera för att ta ett foto och skapa poster som representerar de externa dokumenten. Alternativt med PDF eller bildfiler kan du låta en extern OCR-tjänst (Optical Character Recognition) generera elektroniska dokument som därefter kan konverteras till poster inne i "[!INCLUDE[prod_short](includes/prod_short.md)]".

> [!NOTE]
> OCR-funktionen tillhandahålls av externa providers. Välj ett servicepaket som passar din organisation och/eller ditt land/din region. Sök efter tjänster som är kompatibla med [!INCLUDE[prod_short](includes/prod_short.md)] och information om tillgängliga funktioner på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

När du exempelvis tar emot en faktura i PDF-format från leverantören, kan du skicka den till OCR-tjänsten från sidan **Inkommande dokument**. Du kan också använda vissa OCR-providers om du vill behandla filer som vidarebefordras till en dedicerad e-postadress, som sedan automatiskt skapar en relaterad post för inkommande dokument. Efter några sekunder får du tillbaka filen från OCR-tjänsten som en elektronisk faktura som kan omvandlas till en inköpsfaktura för leverantören.

> [!TIP]
> Skapa inkommande dokument poster i [!INCLUDE[prod_short](includes/prod_short.md)] direkt från e-postmeddelanden som skickas av leverantörer med hjälp av Outlook-tillägget. Mer information finns i [Använda Business Central som din företagsinkorg i Outlook](work-outlook-addin.md).

## Funktioner för inkommande dokument

Processen för inkommande dokument består av följande huvudaktiviteter:

* Logga de externa dokumenten inne i [!INCLUDE[prod_short](includes/prod_short.md)] genom att skapa rader på sidan **Inkommande dokument** på något av följande sätt:
  * Manuellt antingen från en dator eller från en mobil enhet, på något av följande sätt:
    * Använd knappen **Skapa från fil** och ladda upp en fil och fyll relevanta fält på sidan **Inkommande dokument**.
    * Använd knappen **Nytt** och fyll sedan i relevanta fält på sidan **Inkommande dokument** och bifoga den relaterade filen manuellt.
    * Använd knappen **Skapa från kamera** för att skapa en ny inkommande dokumentpost och dokumentinspelning med enhetens inbyggda kamera.
  * Automatiskt genom att ta emot dokumentet från OCR-tjänsten som ett elektroniskt dokument, efter att du har skickat den relaterade PDF- eller bildfilen per e-post till OCR-tjänsten. Snabbfliken **Ekonomisk information** ifylls automatiskt på sidan **Inkommande dokument**.
* Använd en extern OCR-tjänsten för att omvandla PDF- eller bildfiler till elektroniska dokument som kan konverteras till dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].
* Skapa nya dokument eller redovisningsjournalrader för inkommande dokumentposter genom att registrera informationen när du läser den från den inkommande dokumentfiler.
* Koppla inkommande dokumentfiler till inköps- och försäljningsdokument med olika status. inklusive leverantören, kunden och de redovisningstransaktionerna från bokföringen.
* Visa inkommande dokumentposter och deras bilagor från alla inköps- och försäljningsdokument eller sök efter alla redovisningstransaktioner utan inkommande dokumentposter från sidan **Kontoplan**.

> [!NOTE]
> Filer som bifogas kort och dokument på fliken **Bifogade filer** finns inte på sidan **inkommande dokument**. För mer information, se [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).

| Till | Gå till |
| --- | --- |
| Ställa in funktionen för **inkommande dokument** och konfigurera OCR-tjänsten. |[Ställa in inkommande dokument](across-how-setup-income-documents.md) |
| Skapa inkommande dokumentposter manuellt eller automatiskt, genom att ta ett foto av t. ex. ett papperskvitto. |[Skapa inkommande dokumentposter](across-how-create-income-document-records.md) |
| Använd en OCR-tjänst för att göra PDF- och bildfiler till elektroniska dokument, som t. ex. kan omvandlas till inköpsfakturor i [!INCLUDE[prod_short](includes/prod_short.md)]. Utbilda OCR-tjänsten för att undvika fel nästa gång som den bearbetar liknande information. |[Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md) |
| Koppla eller ta bort inkommande dokumentposter för ett icke bokfört försäljnings- eller inköpsdokument och till en kund, leverantör eller redovisningstransaktion från dokumentet eller posten. |[Skapa inkommande dokumentposter direkt från dokument och transaktioner](across-how-connect-disconnect-income-document-records.md) |
| Från sidorna **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda dokument som inte har inkommande dokumentposter, och sedan länka dem till centralt befintliga poster eller skapa nya med bifogade dokumentfiler. |[Söka efter bokförda dokument utan inkommande dokumentposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få en bättre översikt genom att ange inkommande dokumentposter som *Bearbetade* för att ta bort dem från standardvyn. |[Hantera många inkommande dokumentposter](across-how-manage-many-income-document-records.md) |

## Se relaterad [Microsoft utbildning](/training/modules/incoming-documents-dynamics-365-business-central/)

## Se även

[Inköp](purchasing-manage-purchasing.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Utbyta data elektroniskt](across-data-exchange.md)  
[Business Central och OneDrive för företag-integration](across-onedrive-overview.md)  
[Använda Business Central som din företagsinkorg i Outlook](work-outlook-addin.md)  
[Skicka dokument och e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Arbeta med inkommande dokument | Microsoft Docs
description: Du kan hantera inkommande externa företagsdokument, som till exempel betalningsinleveranser eller PDF-filer, hantera OCR-uppgifter och konvertera filer till elektroniska dokument och poster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8e02cd4627219c7ea439155b2b91b61e03534dc2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788489"
---
# <a name="incoming-documents"></a>Inkommande dokument

Vissa affärstransaktioner registreras inte i [!INCLUDE[prod_short](includes/prod_short.md)] från början. I stället kommer ett externt affärsdokument till ditt företag som en e-postbilaga eller papperskopia som du skannar för att spara. Det här är typiskt för inköp där sådana inkommande dokument representerar betalningkvitton för kostnader eller små inköp.

Från PDF eller bildfiler som representerar inkommande dokument kan du låta en extern OCR-tjänst (Optical Character Recognition) generera elektroniska dokument som därefter kan konverteras till dokumentposter inne i "[!INCLUDE[prod_short](includes/prod_short.md)]". Välj ett servicepaket som passar din organisation och/eller ditt land/din region. Du kan också skapa transaktioner manuellt för att visa de externa dokumenten.  

På sidan **Inkommande dokument** använder du olika funktioner för att förhandsgranska utgiftskvitton, hantera OCR-uppgifter och konvertera inkommande dokumentfiler, manuellt eller automatiskt, till relevanta dokument eller journalrader i . De externa filerna kan kopplas till något processteg, inklusive till bokförda dokument och till resulterande leverantörs-, kund- och redovisningstransaktioner.

Processen för inkommande dokument består av följande huvudaktiviteter:

* Logga de externa dokumenten inne i [!INCLUDE[prod_short](includes/prod_short.md)] genom att skapa rader på sidan **Inkommande dokument** på något av följande sätt:
  * Manuellt med hjälp av enkla funktioner, antingen från en dator eller från en mobil enhet, på något av följande sätt:
    * Använd knappen **Skapa från fil** och fyll sedan i relevanta fält på sidan **Inkommande dokument**. Filen kopplas automatiskt.  
    * Använd knappen **Nytt** och fyll sedan i relevanta fält på sidan **Inkommande dokument** och bifoga den relaterade filen manuellt.
    * Använd knappen **Skapa från kamera** för att skapa en ny inkommande dokumentpost och sedan skicka bilden till ocr-servicen, till exempel.
  * Automatiskt genom att ta emot dokumentet från OCR-tjänsten som ett elektroniskt dokument, efter att du har skickat den relaterade PDF- eller bildfilen per e-post till OCR-tjänsten. Snabbfliken **Ekonomisk information** ifylls automatiskt på sidan **Inkommande dokument**.
* Använd OCR-tjänsten för att omvandla PDF- eller bildfiler till elektroniska dokument som kan konverteras till dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].
* Skapa nya dokument eller redovisningsjournalrader för inkommande dokumentposter genom att registrera informationen när du läser den från den inkommande dokumentfiler.
* Koppla inkommande dokumentfiler till inköps- och försäljningsdokument med olika status. inklusive leverantören, kunden och de redovisningstransaktionerna från bokföringen.
* Visa inkommande dokumentposter och deras bilagor från alla inköps- och försäljningsdokument eller sök efter alla redovisningstransaktioner utan inkommande dokumentposter från sidan **Kontoplan**.

| Till | Gå till |
| --- | --- |
| Ställa in funktionen för inkommande dokument och konfigurera OCR-tjänsten. |[Ställa in inkommande dokument](across-how-setup-income-documents.md) |
| Skapa inkommande dokumentposter, koppla filer, använda OCR för att omvandla PDF-filer till elektroniska dokument, omvänd elektroniska dokument till dokumentposter, granska inkommande dokumentposter bokförda för försäljnings- och inköpsdokument. |[Bearbeta inkommande dokument](across-process-income-documents.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
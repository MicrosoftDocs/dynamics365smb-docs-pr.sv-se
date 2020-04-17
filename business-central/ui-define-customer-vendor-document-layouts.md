---
title: Tilldela särskild dokumentlayout till kunder eller leverantörer | Microsoft Docs
description: När anpassade layouter för rapporter definieras kan du välja dem från kund- och leverantörskort för att ange att valda layouter ska användas för de dokument som du skapar för kunden eller leverantören i fråga.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: cc1317961be7896250a883da5c58d1f7eb5cf326
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194505"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definiera dokumentlayout för kunder och leverantörer
När anpassade layouter för rapporter definieras kan du välja dem från kund- och leverantörskort för att ange vilka layouter som ska användas för olika typer av dokument som du skapar för kunden eller leverantören i fråga. Värdet i fältet **Användning** definierar vilken bearbetning som dokumentlayouten ska användas för, t.ex. **påminnelse**, **utleverans** och **bekräftelse**.

Förutom att definiera vilka layouter som ska användas för vilket dokument, kan du spara tid när du skickar dokument till olika kund- eller leverantörskontakter genom att skapa specifika kontakters e-postadresser för särskilda dokument. Kundutdrag skickas till exempel till revisorkontakter, försäljningsorder till kundernas inköpare och inköpsorder till leverantörernas säljare eller kontoansvariga.

När du definierar en dokumentlayout för en kund eller leverantör kan du också ange e-postadressen till den kontaktperson som måste ta emot dokumentet. Du kan snabbt göra detta med funktionen **Välj e-post från kontakter**, som automatiskt filtrerar kontaktpersonens e-postadresser som registrerats för kunden eller leverantören i fråga.

Innan du kan definiera vilken dokumentlayout som ska användas för vilka processer och vilken kontakt som du vill skicka dokumentet till, måste du ladda alla tillgängliga rapporter (dokument) från sidan **rapportval**. Du kan snabbt göra detta med funktionen **kopiera från rapporturval**.

Nedan beskrivs hur du definierar olika layouter för försäljningsdokument från ett kundkort. Stegen är desamma för layouter för inköpsdokument från ett leverantörskort.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Så här aktiverar du alla tillgängliga försäljningsdokument för en kund
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Öppna kortet för den kund för vilken du vill definiera dokumentlayout per affärsprocedur.
3. På sidan **Kundkort** väljer du sidan **Dokumentlayouter**.
4. På sidan **Dokumentlayouter**, välj åtgärden **Kopiera från rapporturval**.

Sidan **Dokumentlayouter** för kunden i fråga är fylld med alla rapport layouter för försäljning som finns i systemet. Mer information om var de skapas finns i [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md).

Du kan nu fortsätta med att justera listan med egna rapportmallar eller e-postadresser till de kontakter som dokumenten ska skickas till.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Så här väljer du en anpassad rapportlayout som ska användas för layouter för försäljningsdokument
Om en eller flera av rapportlayouten som definierats på sidan **dokumentlayout** för en kund inte har någon egen definierad rapportlayout, kan du snabbt göra det.

1. På sidan **dokumentlayout** på raden för en rapportlayout som du vill använda en anpassad layout för, väljer du fältet **Anpassad layoutbeskrivning**. Du kan antingen fylla i fältet om kundlayout redan har valts eller är tom.
2. På sidan **Anpassade rapportlayouter**, välj den speciella dokumentlayout som du vill använda för försäljningsdokumenttyp i fråga. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Så här anger du vilken kontakt som får vilken dokumentlayout för en kund
Du kan spara tid när du skickar dokument till olika kund- eller leverantörskontakter genom att ange kontaktens e-postadresser på de olika raderna på sidan **dokumentlayouter**. Kundutdrag skickas till exempel till revisorkontakter, försäljningsorder till kundernas inköpare och inköpsorder till leverantörernas säljare eller kontoansvariga.

1. På sidan **dokumentlayouter** på raden för en rapportlayout som du vill skicka till en viss kontakt för kunden väljer du åtgärden **Välj e-post från kontakter**.
2. På sidan **Kontakter** väljer du rad för relevant kontakt och väljer sedan knappen **OK**.

E-postadressen till kontakten infogas nu på dokumentets layouttabell så att försäljningsdokumentet, t.ex. påminnelser, alltid skickas till den kontakten hos kundens företag.

## <a name="see-also"></a>Se även  
[Uppdatera anpassade rapportlayouter](ui-update-report-layouts.md)  
[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  

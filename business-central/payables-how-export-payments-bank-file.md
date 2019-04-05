---
title: Exportera betalningar till en elektronisk betalningsfil | Microsoft Docs
description: För att göra leverantörsbetalningar aktiverar du en bankdatakonverteringsservice, exporterae en bankfil och överför filen till elektroniska banken för att överföra medel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 14015c089e3cd6db19a12fe4eed72d523f3aefc5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807256"
---
# <a name="export-payments-to-a-bank-file"></a>Exportera betalningar till en bankfil
När du är redo att göra betalningar till dina leverantörer eller återföringar till dina anställda kan du exportera en fil med betalningsinformation på raderna på sidan **Betalningsjournal**. Du kan sedan överföra filen till banken för att bearbeta relaterade pengaöverföringar.

I den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)], ställs en global tjänstleverantör in och ansluts för att konvertera bankdata till valfritt filformat som din bank kräver. I Nordamerikanska versioner kan samma tjänst användas för att skicka betalningsfiler som elektronisk överföring (EFT), men med en något annorlunda process. Se steg 6 i avsnittet "att exportera betalningar till en bankfil".    

> [!NOTE]  
>   Innan du kan exportera betalningsfiler från betalningsjournalen måste du ange elektroniskt format för berörda adress och du måste aktivera tjänsten för bankdatakonvertering. Mer information finns i [Så här ställer du in bankkonton](bank-how-setup-bank-accounts.md) och [Så här ställer du in konverteringstjänsten för bankdata](bank-how-setup-bank-data-conversion-service.md). Dessutom måste du välja kryssrutan **Tillåt betalningsexport betalning** på sidan **redovisningsjournaler**. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).  

Du använder sidan **Kreditöverföringsregister** för att visa de betalningsfiler som har exporterats från betalningsjournalen. På den här sidan kan du också återexportera betalningfiler i händelse av tekniska fel, eller om filen ändras. Tänk på att exporterade EFT-filer inte visas på den här sidan och kan inte återexporteras.  

## <a name="to-export-payments-to-a-bank-file"></a>Exportera betalningar till en bankfil
Nedan beskrivs hur du betalar en leverantör med check. Stegen liknar återbetalning till en kund med check.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Betalningsjournal** och välj sedan relaterad länk.
2. Fyll i utbetalningsjournalraderna. Mer information finns i [Registrera betalningar och återbetalningar](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Om du använder EFT kan du välja mellan **elektronisk betalning** eller **elektronisk betalning – IAT** i fältet **Bankbetalningstyp**. Andra filexporttjänster och deras format kräver olika inställningsvärden på sidan **Bankkontokort** och **Leverantörsbankkontokort**. Du får information om vilka inställningsvärden som är fel eller saknas när du försöker exportera filen.

3. När du har gjort alla betalningsjournalrader, väljer du åtgärden **Exportera**.
4. På sidan **Exportera elektronisk betalning** fyller du i fälten efter behov.

    Felmeddelanden visas i faktaboxen **Fel i betalningsfil** där du kan även välja ett felmeddelande om du vill se detaljerad information. Du måste lösa alla fel innan betalningsfilen kan exporteras.

    > [!TIP]  
    >   När du använder tjänsten för bankdatakonvertering visas ett vanligt felmeddelande som berättar att bankkontonumret inte har den längd som din bank kräver. För att undvika eller lösa felet måste du ta bort värdet i fältet **IBAN** på sidan **Bankkontokort** och sedan i fältet **Bankkontonr** ange ett bankkontonummer i formatet som din bank kräver.

5. På sidan **Spara som** anger du var filen ska exporteras till och välj sedan **Spara**.

    > [!NOTE]  
    >   Om du använder EFT, sparar du det resulterande remissaformuläret för leverantör som Word-dokument eller välj att få det med e-post direkt till leverantören. Betalningarna läggs nu till på sidan **generera EFT-fil** där du kan skapa flera betalningsorder tillsammans för att spara kostnader för överföring. Mer information finns i följande steg:
6. På sidan **betalningsjournal** kan du välja åtgärden **generera EFT-fil**.

    På sidan **generera EFT-fil** listas alla betalningar som har ställts in för EFT som du har exporterat från utbetalningsjournalen för en angiven adress men som ännu inte har skapats på snabbfliken **rader**.
7. Välj åtgärder **generera EFT-fil** för att exportera en fil för EFT-betalningar.
8. På sidan **Spara som** anger du var filen ska exporteras till och välj sedan **Spara**.

Bankbetalningsfilen exporteras till den plats som du anger, och du kan fortsätta att föra över den till ditt elektroniska bankkonto och göra de faktiska beloppen. Du kan sedan bokföra de exporterade betalningsjournalraderna.

## <a name="to-plan-when-to-post-exported-payments"></a>Så här planerar du när du vill bokföra exporterad betalning
Om du inte vill bokföra en utbetalningsjournalrad för en exporterad betalning, till exempel eftersom du väntar på en bekräftelse att transaktionen har behandlats av banken, kan du bara ta bort journalraden. När du senare skapar en utbetalningsjournal för att betala återstående belopp på fakturan kan du i fältet **Totalt exporterat belopp** se hur mycket av beloppet som redan har exporterats. Du kan också söka efter detaljerad information om det exporterade totalbeloppet genom att välja knappen **Transaktioner i kreditöverföringsregister** för att visa detaljer om exporterade betalningsfiler.

Om du följer en process där du inte vill bokföra utbetalningar, tills du har bekräftelsemeddelande att de har behandlats i banken, kan du använda detta två sätt.

* I en utbetalningsjournal med föreslagna betalningsrader kan du sortera på antingen kolumnen **Exporterat till betalningsfil** eller **Totalt exporterat belopp** och sedan ta bort betalningsförslag för öppna fakturor för vilka betalningar som redan har gjorts och du inte vill göra betalningar för.
* På sidan **Betalningsförslag för lev.**, där du anger vilka betalningar som ska infogas i utbetalningsjournalen, kan du markera kryssrutan **Hoppa över exporterade betalningar** om du inte vill infoga journalrader för betalningar som redan har exporterats.

Om du vill visa information om exporterade betalningar väljer du åtgärden **Betalningsexporthistorik**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Så här återexporterar du betalningar till en bankfil
Du kan återexportera betalningsfiler till en bankfil från sidan **Kreditöverföringsregister**. Innan du tar bort eller bokför utbetalningsjournalrader kan du också återexportera betalningsfilen från sidan **Betalningsjournal** genom att helt enkelt exportera den på nytt. Om du har tagit bort eller bokfört rader i utbetalningsjournalen efter att du har exporterat dem kan du återexportera samma betalningsfil från sidan **Kreditöverföringsregister**. Markera raden för batchen med kreditöverföringar du vill återexportera och välj sedan åtgärden **Återexportera betalningar till fil**.

> [!NOTE]  
>   Exporterade EFT-filer visas inte på sidan **Kreditöverföringsregister** och kan inte återexporteras.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kreditöverföringsregister** och välj sedan relaterad länk.
2. Välj en betalningsexport som du vill återexportera och välj sedan åtgärden **Återexportera betalningar till fil**.

## <a name="see-also"></a>Se även
[Göra betalningar](payables-make-payments.md)  
[Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

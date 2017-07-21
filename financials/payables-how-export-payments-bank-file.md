---
title: Exportera betalningar till en elektronisk betalningsfil | Microsoft Docs
description: "För att göra leverantörsbetalningar aktiverar du en bankdatakonverteringsservice, exporterae en bankfil och överför filen till elektroniska banken för att överföra medel."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bb79c8df5b353239802f63fc3c268c83b6eb7859
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-export-payments-to-a-bank-file"></a>Så här exporterar du betalningar till en bankfil
När du är redo att göra betalningar till leverantörer med hjälp av **Betalningsjournal** fönster, kan du exportera en fil med betalningsinformation på journalraderna. Du kan sedan överföra filen till den elektroniska banken att bearbeta relaterade pengaöverföringar.

I den generiska versionen av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], ställs en global tjänstleverantör in och ansluts för att konvertera bankdata till valfritt filformat som din bank kräver. I Nordamerikanska versioner kan samma tjänst användas för att skicka betalningsfiler som elektronisk överföring (EFT), men med en något annorlunda process. Se steg 6 i avsnittet "att exportera betalningar till en bankfil".    

> [!NOTE]  
>   Innan du kan exportera betalningsfiler från betalningsjournalen måste du ange elektroniskt format för berörda adress och du måste aktivera tjänsten för bankdatakonvertering. Mer information finns i [Så här ställer du in bankkonton](bank-how-setup-bank-accounts.md) och [Så här ställer du in tjänsten bankdatakonvertering](bank-how-setup-bank-data-conversion-service.md). Dessutom måste du välja kryssrutan **Tillåt betalningsexport betalning** i fönstret **redovisningsjournaler**. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).  

Du använder fönstret **Kreditöverföringsregister** för att visa de betalningsfiler som har exporterats från betalningsjournalen. I det här fönstret kan du också återexportera betalningfiler i händelse av tekniska fel, eller om filen ändras. Tänk på att exporterade EFT-filer inte visas i det här fönstret och kan inte återexporteras.  

## <a name="to-export-payments-to-a-bank-file"></a>Exportera betalningar till en bankfil
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.
2. Fyll i betalningsjournalen med relevanta utbetalningar, till exempel genom att använda funktionen **Betalningsförslag för lev.**. Mer information finns i [Så här föreslår du leverantörsbetalningar](payables-how-suggest-vendor-payments.md).
3. Fyll i fälten på utbetalningsjournalraderna vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Om du använder EFT kan du välja mellan **elektronisk betalning** eller **elektronisk betalning – IAT** i fältet **Bankbetalningstyp**.

    Andra filexporttjänster och deras format kräver olika inställningsvärden i fönstren**Bankkontokort** och **Leverantörsbankkontokort**. Du får information om vilka inställningsvärden som är fel eller saknas när du försöker exportera filen.

4. När du har gjort alla betalningsjournalrader, väljer du åtgärden **Exportera**.
5. I fönstret **Exportera elektronisk betalning** fyller du i fälten efter behov.

    Felmeddelanden visas i faktaboxen **Fel i betalningsfil** där du kan även välja ett felmeddelande om du vill se detaljerad information. Du måste lösa alla fel innan betalningsfilen kan exporteras.

    > [!TIP]  
>   När du använder tjänsten för bankdatakonvertering visas ett vanligt felmeddelande som berättar att bankkontonumret inte har den längd som din bank kräver. För att undvika eller åtgärda felet, måste du ta bort värdet i fältet **IBAN** i fönstret **Bankkontokort** och sedan i **Bankkontonr.** anger du ett bankkonto i formatet som din bank krävs.

6. I fönstret **Spara som** anger du var filen ska exporteras till och välj sedan **Spara**.

    > [!NOTE]  
>   Om du använder EFT, sparar du det resulterande remissaformuläret för leverantör som Word-dokument eller välj att få det med e-post direkt till leverantören. Betalningarna läggs nu till i fönstret **generera EFT-fil** där du kan skapa flera betalningsorder tillsammans för att spara kostnader för överföring. Mer information finns i följande steg:
7. I fönstret **betalningsjournal** kan du välja åtgärden **generera EFT-fil**.

    I fönstret **generera EFT-fil** listas alla betalningar som har ställts in för EFT som du har exporterat från utbetalningsjournalen för en angiven adress men som ännu inte har skapats på snabbfliken **rader**.
8. Välj åtgärder **generera EFT-fil** för att exportera en fil för EFT-betalningar.
9. I fönstret **Spara som** anger du var filen ska exporteras till och välj sedan **Spara**.

Bankbetalningsfilen exporteras till den plats som du anger, och du kan fortsätta att föra över den till ditt elektroniska bankkonto och göra de faktiska beloppen. Du kan sedan bokföra de exporterade betalningsjournalraderna.

## <a name="to-export-payments-that-represent-customer-refunds"></a>För att exportera betalningar som motsvarar kundåterbetalningar
Nedan beskrivs en problemlösning för export av elektroniska återbetalningar.

> [!CAUTION]  
>   Den resulterande betalningjournalraden kan inte bokföras, raderas eller annulleras.
1. Konfigurera kunden som leverantör. Kalla den "Kunden X för återbetalning", t.ex. Mer information finns i [Så här registrerar du nya leverantörer](purchasing-how-register-new-vendors.md).
2. På utbetalningsjournalraden för kunden anger du fältet **kontotyp** till **kund**, och fältet **dokumenttyp** till **Återbetala**.
3. Utför de vanliga stegen för betalningsexport som beskrivs i avsnittet "Exportera betalningar till en bankfil".

## <a name="to-plan-when-to-post-exported-payments"></a>Så här planerar du när du vill bokföra exporterad betalning
Om du inte vill bokföra en utbetalningsjournalrad för en exporterad betalning, till exempel eftersom du väntar på en bekräftelse att transaktionen har behandlats av banken, kan du bara ta bort journalraden. När du senare skapar en utbetalningsjournal för att betala återstående belopp på fakturan kan du i fältet **Totalt exporterat belopp** se hur mycket av beloppet som redan har exporterats. Du kan också söka efter detaljerad information om det exporterade totalbeloppet genom att välja knappen **Transaktioner i kreditöverföringsregister** för att visa detaljer om exporterade betalningsfiler.

Om du följer en process där du inte vill bokföra utbetalningar, tills du har bekräftelsemeddelande att de har behandlats i banken, kan du använda detta två sätt.

* I en utbetalningsjournal med föreslagna betalningsrader kan du sortera på antingen kolumnen **Exporterat till betalningsfil** eller **Totalt exporterat belopp** och sedan ta bort betalningsförslag för öppna fakturor för vilka betalningar som redan har gjorts och du inte vill göra betalningar för.
* På liknande sätt kan du i batchjobbet **Betalningsförslag för lev.**, där du anger vilka betalningar som ska infogas i utbetalningsjournalen, markera kryssrutan **Hoppa över exporterade betalningar** om du inte vill infoga journalrader för betalningar som redan har exporterats.

Om du vill visa information om exporterade betalningar väljer du åtgärden **Betalningsexporthistorik**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Så här återexporterar du betalningar till en bankfil
Du kan återexportera betalningsfiler till en bankfil från fönstret **Kreditöverföringsregister**. Innan du tar bort eller bokför utbetalningsjournalrader kan du också återexportera betalningsfilen från fönstret **Betalningsjournal** genom att helt enkelt exportera den på nytt. Om du har tagit bort eller bokfört rader i utbetalningsjournalen efter att du har exporterat dem kan du återexportera samma betalningsfil från fönstret **Kreditöverföringsregister**. Markera raden för batchen med kreditöverföringar du vill återexportera och välj sedan åtgärden **Återexportera betalningar till fil**.

> [!NOTE]  
>   Exporterade EFT-filer visas inte i fönstret **Kreditöverföringsregister** och kan inte återexporteras.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.
2. Välj en betalningsexport som du vill återexportera och välj sedan åtgärden **Återexportera betalningar till fil**.

## <a name="see-also"></a>Se även
[Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

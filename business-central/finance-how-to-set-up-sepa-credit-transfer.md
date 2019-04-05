---
title: Ställ in SEPA Kreditöverföringar | Microsoft Docs
description: Lär dig hur du ställer in SEPA-kreditöverföring i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 6c35fdb6e5e37eb521b6d51050a552e52b66ec5d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807171"
---
# <a name="set-up-sepa-credit-transfer"></a>Konfigurera SEPA-kreditöverföring
Från sidan **Betalningsjournal** kan du exportera betalningar till en fil för överföring till din elektroniska bank för behandling av de relaterade pengaöverföringarna. [!INCLUDE[d365fin](includes/d365fin_md.md)] stödjer SEPA kreditöverföringar-format, men andra format för elektroniska betalningar i ditt land/din region kan finnas.  

Om du vill aktivera export av bankfilformat som inte stöds från början i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du konfigurera en datautbytesdefinition med ramverket för datautbyte. Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Innan du kan bearbeta betalning på elektronisk väg genom att exportera betalningsfiler i formatet SEPA Krediteringsöverföring, måste du utföra följande inställningssteg:  

* Skapa bankkontot i fråga för att hantera format för SEPA-kreditöverföringen.  
* Skapa leverantörskort för att behandla betalningar genom att exportera filer i formatet för SEPA-kreditöverföringen.  
* Ställ in den relaterade redovisningsjournal-batchen för att aktivera betalningsexporten från sidan **Betalningsjournal**  
* Så här kan du ansluta datautbytesdefinitionen för en eller flera betalningstyper till lämpliga betalningsmetoder  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Så här lägger du upp ett bankkonto för SEPA-kreditöverföring  
1. I rutan **Sök**, ange **Bankkonton** och välj sedan relaterad länk.  
2. Öppna kortet för det bankkonto som du ska exportera betalningsfiler från i formatet SEPA Kreditöverföring.  
3. På snabbfliken **överför**i fältet **Format för betalningsexport**, välj **SEPADD**.  
4. I fältet **SEPA CT Medd ID-nr serie** väljer du en nummerserie från vilken nummer tilldelas till SEPA-kreditöverföringsartiklar.  
5. Se till att fältet **IBAN** är ifyllt.  

    > [!NOTE]  
    >  Fältet **Valutakod** måste anges till **EUR**, eftersom SEPA-kreditöverföringar bara kan utföras i valutan EURO.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Så här lägger du upp ett leverantörskort för SEPA-kreditöverföring  
1. I rutan **Sök**, ange **Leverantörer** och välj sedan relaterad länk.  
2. Öppna kortet för den leverantör som du ska betala elektronisk genom att exportera betalningsfiler i formatet SEPA Kreditöverföring.  
3. På snabbfliken **Betalning** i fältet **Betalningsmetodkod** väljer du **BANK**.  
4. I fältet **Föredraget bankkonto** väljer du banken som pengarna ska överföras till när de har behandlat av din elektroniska bank.  

     Värdet i fältet **Föredraget bankkonto** kopieras till fältet **mottagarens bankkonto** på sidan **betalningsjournal**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Så här anger du utbetalningsjournalen för att exportera betalningsfiler  
1. I rutan **Sök**, ange **Utbetalningsjournaler** och välj sedan relaterad länk.  
2. Öppna utbetalningsjournalen som du använder för att behandla betalningar genom att exportera filer i formatet SEPA Kreditöverföring.  
3. I fältet **Journalnamn** väljer du listrute\-knappen.  
4. På sidan **Redovisningsjournaler** på fliken **Start** i gruppen **Hantera** väljer du **Redigera lista**.  
5. Markera kryssrutan **Tillåt betalningsexport** på raden för utbetalningsjournalen som du kommer att använda när du vill exportera betalningar.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Så här kan du ansluta datautbytesdefinitionen för en eller flera betalningstyper till lämpliga betalningsmetoder  
1. I rutan **Sök**, ange **Betalningssätt** och välj sedan relaterad länk.  
2. På sidan **Betalningsmetoder** väljer du det betalningssätt som används att exportera betalningar från och väljer sedan fältet **Definition för bet.exportrad**.  
3. På sidan **Definition för bet.exportrad** väljer du den kod som du har angett i fältet **Kod** på snabbfliken **Definitioner för rad** i steg 4 i avsnittet ”Beskriva layouten för rader och kolumner i filen” i förfarandet [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="see-also"></a>Se även  
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)  
[Skapa dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md)  
[Utbyta data elektroniskt](across-data-exchange.md).  

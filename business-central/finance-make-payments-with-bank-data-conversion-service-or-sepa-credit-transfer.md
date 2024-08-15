---
title: Göra betalningar med AMC banking (US) eller SEPA credit transfer (EU)
description: Behandla betalningar till dina leverantörer genom att exportera en fil (EFT) tillsammans med betalningsinformation från på journalraderna.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/17/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Gör betalningar med AMC banking 365 fundamentals extension eller SEPA kreditöverföring

På sidan **Utbetalningsjournaler** kan du behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformationen från journalraderna. Du kan sedan överföra filen till den elektroniska banken där relaterade pengaöverföringar bearbetas. [!INCLUDE[prod_short](includes/prod_short.md)] har stöd för formatet SEPA-kreditöverföring, men i ditt land/din region kan andra format för elektroniska betalningar vara tillgängliga.

> [!NOTE]
> I den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)], ställs en global tjänstleverantör in och ansluts för att konvertera bankdata till valfritt filformat som din bank kräver. I Nordamerikanska versioner kan samma service användas för att skicka betalningsfiler som EFT (Elektronisk överföring), t.ex. det ACH-nätverk som ofta används, men med en något annorlunda metod. Se steg 6 i [Att exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Om du vill aktivera SEPA-kreditöverföringar måste du först lägga upp ett bankkonto, en leverantör och redovisningsjournalen som utbetalningsjournalen baseras på. Därefter förbereder du betalningar till leverantörer genom att automatiskt fylla i **sidan Utbetalningsjournaler** med förfallna betalningar med angivna bokföringsdatum.  

> [!NOTE]  
> När du har verifierat att betalningarna har behandlats korrekt av banken kan du fortsätta att bokföra utbetalningsjournalraderna.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Konfigurera tillägget AMC Banking 365 Fundamentals

Aktivera tillägget AMC Banking 365 Fundamentals om du vill få en eventuell bankutdragsfil konverterad till ett format som du kan importera eller få dina exporterad betalningsfiler konverterade till det format som din bank kräver. Mer information finns i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Ställa in SEPA-kreditöverföring

Från sidan **Utbetalningsjournaler** kan du exportera betalningar till en fil för överföring till din elektroniska bank för behandling av relaterade penningöverföringar. [!INCLUDE[prod_short](includes/prod_short.md)] har stöd för formatet SEPA-kreditöverföring, men i ditt land/din region kan andra format för elektroniska betalningar vara tillgängliga.  

Om du vill aktivera export av ett bankfilformat som inte stöds direkt i [!INCLUDE[prod_short](includes/prod_short.md)] kan du konfigurera en definition för datautbyte med hjälp av ramverket för datautbyte. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Innan du kan bearbeta betalning på elektronisk väg genom att exportera betalningsfiler i formatet SEPA Krediteringsöverföring, måste du utföra följande inställningssteg:  

* Skapa bankkontot i fråga för att hantera format för SEPA-kreditöverföringen.  
* Skapa leverantörskort för att behandla betalningar genom att exportera filer i formatet för SEPA-kreditöverföringen.  
* Konfigurera den relaterade redovisningsjournalen för att aktivera betalningsexport från **sidan Utbetalningsjournaler**   
* Så här kan du ansluta datautbytesdefinitionen för en eller flera betalningstyper till lämpliga betalningsmetoder  

> [!NOTE]
> Business Central stöder både CT-smärta i SEPA-format.001.001.03 och CT-smärta.001.001.09. Du kan välja vilket format som helst på **sidan Bankkonto kort** .  
> [!TIP]
> Den här artikeln gäller för den allmänna versionen av [!INCLUDE [prod_short](includes/prod_short.md)]. I ditt land eller din region kan ytterligare obligatoriska fält läggas till på de olika sidorna. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Så här lägger du upp ett bankkonto för SEPA-kreditöverföring

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.  
2. Öppna kort för bankkontot som du ska exportera betalningsfiler från i formatet SEPA-kreditöverföring.  
3. Välj det **SEPA-format som du vill använda i** fältet Format för betalningsexport **på snabbfliken Kontoinnehavare** .  
4. På snabbfliken **Allmänt** i fältet **Nr-serie för kredittrans.med.** välj en nummerserie från vilken nummer tilldelas SEPA-kreditöverföringsposter.  
5. Se till att fältet **IBAN** är ifyllt.  

    > [!NOTE]  
    > Fältet **Valutakod** måste anges till **EUR**, eftersom SEPA-kreditöverföringar bara kan utföras i valutan EURO.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Så här lägger du upp ett leverantörskort för SEPA-kreditöverföring

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.  
2. Öppna kortet för den leverantör som du ska betala elektronisk genom att exportera betalningsfiler i formatet SEPA Kreditöverföring.  
3.  **På snabbfliken Betalningar** i fältet **Betalningssätt väljer** du **BANK.**  
4. I fältet **Önskat bankkonto** väljer du den bank som pengarna ska överföras till när de behandlas av din elektroniska bank.  

    Om du inte redan har skapat en bank för leverantören kan du göra det nu. Mer information finns i [Så här skapar du leverantörs bankkonton för export av bankfiler](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Värdet i fältet **Föredraget bankkonto** kopieras till fältet **mottagarens bankkonto** på sidan **betalningsjournal**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Så här anger du utbetalningsjournalen för att exportera betalningsfiler

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.  
2. I fältet **Journalnamn** väljer du listrute\-knappen.  
3. Välj åtgärden **Redigera lista** på sidan **Redovisningsjournaler**.  
4. På raden för betalningsjournalen som du använder för att exportera betalningar Välj **kryssrutan Tillåt betalningsexport** .  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Så här kan du ansluta datautbytesdefinitionen för en eller flera betalningstyper till lämpliga betalningsmetoder

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **betalningsmetoder** och väljer sedan relaterad länk.  
2. På sidan **Betalningsmetoder** väljer du det betalningssätt som används att exportera betalningar från och väljer sedan fältet **Definition för bet.exportrad**.  
3. På sidan **Definition för bet.exportrad** väljer du den kod som du har angett i fältet **Kod** på snabbfliken **Definitioner för rad** i steg 4 i avsnittet ”Beskriva layouten för rader och kolumner i filen” i förfarandet [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Förbereda utbetalningsjournalen

Fyll i betalningsjournalen med rader för förfallna betalningar till leverantörer, med alternativet att infoga bokföringsdatum som baseras på förfallodatumet för de relaterade inköpsdokumenten. Mer information finns i [Hantera leverantörsskulder](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Exportera betalningar till en bankfil

När du är redo att göra utbetalningar till leverantörer, eller ersättningar till anställda, kan du exportera en fil med betalningsinformationen på raderna på sidan **Utbetalningsjournaler** . Du kan sedan överföra filen till banken för att bearbeta relaterade pengaöverföringar.

I den allmänna versionen av [!INCLUDE[prod_short](includes/prod_short.md)] är tillägget AMC Banking 365 Fundamentals tillgängligt. I nordamerikanska versioner kan samma tillägg användas för att skicka betalningsfiler som elektronisk överföring (EFT), men med en något annorlunda process. Se steg 6 i [Att exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Innan du kan exportera betalningsfiler från betalningsjournalen måste du ange elektroniskt format för berört bankkonto och du måste aktivera tillägget AMC Banking 365 Fundamentals. Mer information finns i [Skapa bankkonton](bank-how-setup-bank-accounts.md) och [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md). Dessutom måste du välja kryssrutan **Tillåt betalningsexport betalning** på sidan **redovisningsjournaler**. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).  

Du använder sidan **Kreditöverföringsregister** för att visa de betalningsfiler som har exporterats från betalningsjournalen. På den här sidan kan du också återexportera betalningfiler i händelse av tekniska fel, eller om filen ändras. Observera dock att exporterade EFT-filer inte visas på den här sidan och inte kan exporteras igen.  

### <a name="to-export-payments-to-a-bank-file"></a>Exportera betalningar till en bankfil

Nedan beskrivs hur du betalar en leverantör med check. Stegen liknar återbetalning till en kund med check.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.
2. Fyll i utbetalningsjournalraderna. Mer information finns i [Registrera betalningar och återbetalningar](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Om du använder EFT kan du välja mellan **elektronisk betalning** eller **elektronisk betalning – IAT** i fältet **Bankbetalningstyp**. Andra filexporttjänster och deras format kräver olika inställningsvärden på sidan **Bankkontokort** och **Leverantörsbankkontokort**. Du får information om vilka inställningsvärden som är fel eller saknas när du försöker exportera filen.
    >
    > EFT-funktionen kan bara användas för bankkonton i lokal valuta. Den kan inte användas med en utländsk valuta, som anges med ett värde i fältet **Valutakod**. (Tomt fältvärde betyder lokal valuta.)

3. När du har gjort alla betalningsjournalrader, väljer du åtgärden **Exportera**.
4. På sidan **Exportera elektronisk betalning** fyller du i fälten efter behov.

    Felmeddelanden visas i faktaboxen **Fel i betalningsfil** där du kan även välja ett felmeddelande om du vill se detaljerad information. Du måste lösa alla fel innan betalningsfilen kan exporteras.

    > [!TIP]  
    > När du använder tillägget AMC Banking 365 Fundamentals visas ett vanligt felmeddelande som berättar att bankkontonumret inte har den längd som din bank kräver. För att undvika eller lösa felet måste du ta bort värdet i fältet **IBAN** på sidan **Bankkontokort** och sedan i fältet **Bankkontonr** ange ett bankkontonummer i formatet som din bank kräver.

5. På sidan **Spara som** anger du var filen ska exporteras till och välj sedan **Spara**.

    > [!NOTE]  
    > Om du använder EFT, sparar du det resulterande remissaformuläret för leverantör som Word-dokument eller välj att få det med e-post direkt till leverantören. Betalningarna läggs nu till på sidan **generera EFT-fil** där du kan skapa flera betalningsorder tillsammans för att spara kostnader för överföring. Mer information finns i följande steg:
6. På sidan **Utbetalningsjournaler** väljer du **åtgärden Generera EFT-fil** .

    På sidan **generera EFT-fil** listas alla betalningar som har ställts in för EFT som du har exporterat från utbetalningsjournalen för en angiven adress men som ännu inte har skapats på snabbfliken **rader**.
7. Välj åtgärder **generera EFT-fil** för att exportera en fil för EFT-betalningar.
8. På sidan **Spara som** anger du var filen ska exporteras till och välj sedan **Spara**.

Bankbetalningsfilen exporteras till den plats som du anger, och du kan fortsätta att föra över den till ditt elektroniska bankkonto och göra de faktiska beloppen. Du kan sedan bokföra de exporterade betalningsjournalraderna.

### <a name="to-plan-when-to-post-exported-payments"></a>Så här planerar du när du vill bokföra exporterad betalning

Om du inte vill bokföra en utbetalningsjournalrad för en exporterad betalning, till exempel för att du väntar på bekräftelse på att transaktionen har behandlats av banken, kan du bara ta bort journalraden. När du senare skapar en utbetalningsjournal för att betala återstående belopp på fakturan kan du i fältet **Totalt exporterat belopp** se hur mycket av beloppet som redan har exporterats. Du kan också söka efter detaljerad information om det exporterade totalbeloppet genom att välja knappen **Transaktioner i kreditöverföringsregister** för att visa detaljer om exporterade betalningsfiler.

Om du följer en process där du inte bokför betalningar förrän du har bekräftat att de har behandlats i banken kan du styra detta på två sätt.

* I en utbetalningsjournal med föreslagna betalningsrader kan du sortera efter kolumnen **Exporterat till betalningsfil** eller Totalt **exporterat belopp** och sedan ta bort betalningsförslag för öppna fakturor som du redan har betalat för och inte vill betala för.
*  **På sidan Betalningsförslag** för leverantör, där du anger vilka betalningar som ska infogas i utbetalningsjournalen, kan du Välj **kryssrutan Hoppa över exporterade betalningar** om du inte vill infoga journalrader för betalningar som redan har exporterats.

Om du vill visa information om exporterade betalningar väljer du åtgärden **Betalningsexporthistorik**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Så här återexporterar du betalningar till en bankfil

Du kan återexportera betalningsfiler till en bankfil från sidan **Kreditöverföringsregister**. Innan du tar bort eller bokför utbetalningsjournalrader kan du också exportera betalningsfilen på nytt från sidan **Utbetalningsjournaler** genom att exportera den igen. Om du tar bort eller bokför utbetalningsjournalraderna efter exporten kan du exportera samma betalningsfil på nytt från sidan **Kreditöverföringsregister** . Markera raden för batchen med kreditöverföringar du vill återexportera och välj sedan åtgärden **Återexportera betalningar till fil**.

> [!NOTE]  
> Exporterade EFT-filer visas inte på sidan **Kreditöverföringsregister** och kan inte återexporteras.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Kreditöverföringsregister** och välj sedan relaterad länk.
2. Välj en betalningsexport som du vill återexportera och välj sedan åtgärden **Återexportera betalningar till fil**.

## <a name="posting-the-payments"></a>Förhandsgranska betalningarna

Bokför betalningarna när den elektroniska betalningen har behandlats utan problem av banken. Mer information finns i [Gör betalningar](payables-make-payments.md).

## <a name="see-also"></a>Se även

[Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Ta betalt med SEPA-postförskott](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

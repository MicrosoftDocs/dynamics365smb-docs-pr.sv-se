---
title: Skapa bankkonton (innehåller video)
description: Läs om hur bankkonton används i Business Central och hur du kan stämma av belopp med din bank.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 01/24/2022
ms.author: edupont
---
# <a name="set-up-bank-accounts" />Skapa bankkonton

Du använder bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)] för att hålla reda på dina banktransaktioner. Konton kan definieras i den lokala valutan eller i en utländsk valuta. När du har skapat bankkonton kan du också använda funktionen för utskrift av checkar. Bankkontona innehåller extra funktionalitet för [betalningsavstämning](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankavstämning](bank-how-reconcile-bank-accounts-separately.md) och import och export av bankfiler. Bankkontona kan också inkluderas i transaktioner i redovisningsjournalerna. Varje bankkonto är länkat till ett konto i kontoplanen via den tilldelade bankkontobokföringsmallen. Om du använder ett bankkonto i en betalningstransaktion skapas automatiskt en transaktion på både bankkontot och det anslutna redovisningskontot.  

Bankkonton fungerar olika beroende på om en valutakod har angetts:

- Om valutakoden är tom

  Alla transaktioner på bankkontot sker i den lokala valutan (BVA) för det aktuella företaget. Om en transaktion görs till kontot i en annan valuta bokförs beloppen på kontot i BVA baserat på den aktuella valutakursen. Alla checkar som utfärdas från det här kontot måste utfärdas i BVA. Om bank kontot används i en journal kommer Journal raden automatiskt att ärva den tomma valuta koden.  
  
- Valutakoden anges

  Alla transaktioner som görs till och alla checkar som utfärdas från det här kontot måste vara i samma valuta som har angetts på kontot.

Du kan spara tid genom att göra ett bankkonto till det standardkonto som ska användas för den valuta som har angetts för kontot. Om du gör det kommer kontot att tilldelas försäljnings- och servicedokument som använder valutan. Om du vill att kontot ska vara standard för försäljnings- och servicedokument på sidan **Bankkontokort** aktiverar du reglaget **Använd som standard för valuta**. Om det behövs kan du välja ett annat konto när du arbetar med ett dokument.

Ett bankkonto är en viktig del av [!INCLUDE[prod_short](includes/prod_short.md)] och spelar en roll i många andra funktioner. Följande illustration visar de viktigaste relationerna:

![Illustration av bankkontorelationer.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Du kan se att skapandet av ett bankkonto gör det tillgängligt på alla platser som visas ovan och speglas i det aktuella redovisningskontot och på sidan **Företagsinformation**.

Ett bankkonto övervakas oftast dagligen för att säkerställa att alla nya betalningar från kunder registreras så snabbt som möjligt. Detta säkerställer att en kunds faktiska status återspeglas i [!INCLUDE[prod_short](includes/prod_short.md)]. Det ger säljare, revisorer och andra anställda tillgång till den mest relevanta och aktuella informationen så att de inte gör onödiga samtal till kunden om förfallna fakturor eller förseningar i leveranser.  

![Illustration av bankbetalning.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

En annan uppgift är att importera leverantörens valutabetalningar med faktiska valutakurser för att försäkra dig om att leverantörens faktiska status är aktuell. Att använda funktionen för [betalningsavstämning](receivables-apply-payments-auto-reconcile-bank-accounts.md) är det enklaste sättet att göra det. I **betalningsavstämningsjournal** kan du importera banktransaktioner direkt från ett bankprogram online och låta dem bokföras mer eller mindre automatiskt. Journalen identifierar och bokför automatiskt följande:  

- Direkt debitering av betalningar från kunder  
- Kundbetalningar av enstaka fakturor  
- Betalningar i klumpsumma från kunder.  
- Kundbetalningar i utländska valutor  
- Leverantörsbetalningar  
- Leverantörsbetalningar i utländska valutor  
- Återkommande leverantörsbetalningar och abonnemang  
- Bankavgifter och intressen  

Betalningsavstämningen ger en betydande tidsbesparing vid bokföring av inkommande och utgående betalningar. Transaktionerna på bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] anses dock inte vara 100 % riktiga förrän du kör en bankkontoavstämning.  

Bankkontoavstämningen är hur du ser till att bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] matchar det externa kontot hos banken.  

 ![Illustration av bankkontoavstämning.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

I bilden ovan representerar den vänstra sidan bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] och den högra sidan representerar de transaktioner som importerats från banken via bankprogrammet online. I diagrammet i mitten visas transaktionerna från båda sidorna, som är bankkontoavstämning.

Från bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] bör de flesta transaktionerna vara kända för den fysiska banken. De få undantagen är följande fall:  

- Korrigeringar som bokförts i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Utfärdade checkar som inte har registrerats ännu 
- Leverantörsbetalningar som inte har godkänts av banken  

Från det fysiska kontot i banken kommer transaktioner som inte har identifierats i betalningsavstämningsjournalen in hela tiden, till exempel följande:  

- Nya leverantörsabonnemang  
- Kundbetalningar utan beskrivning
- Bankens ränta
- Bankavgifter
- Kreditkortsavgifter ännu inte rapporterade

Ju bättre du är på att mappa information i betalningsavstämningsjournalen, desto fler transaktioner bokförs automatiskt och desto enklare blir den periodiska bankavstämningen.

I videoklippet under de grundläggande stegen visas hur du kan skapa ett bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Vissa fält kan innehålla känslig information, till exempel fälten **Bankfilialsnr.**, **Bankkontonr.**, **SWIFT-kod** och **IBAN-kod**. Läs mer i [Övervaka känsliga fält](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts" />Så här skapar du bankkonton

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. På sidan **Bankkonton** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ett exempel är fältet **Bokföringsmall för bank-konto** som kopplar bankkontot till det underliggande redovisningskontot i balansräkningen. Läs mer i [Så här skapar du bokföringsmallar](finance-posting-groups.md).

> [!TIP]
> Vissa fält är dolda tills du väljer åtgärden **Visa fler**, vanligen på grund av att de sällan används. Andra måste läggas till genom anpassning. Lär dig hur du [anpassar arbetsytan](ui-personalization-user.md).

Du kan skapa så många bankkonton som du behöver för ditt företag. För varje bankkonto måste du ange information som gör bankkontot unikt identifierbart. Den här informationen omfattar bankens geografiska adress, nummerserie för olika typer av transaktioner, till exempel direktdebitering och kreditöverföringar, valutan som anges i och information som används för import av bankutdrag. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance" />Ange ett ingående saldo

För att fylla i fältet **Saldo** med en ingående balans måste du bokföra en bankkontotransaktion med beloppet i fråga. Du kan göra detta genom att utföra en bankkontoavstämning. Läs mer på [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).  
>
> Alternativt kan du implementera den ingående balansen som en del av skapandet av allmänna data i nya företag med hjälp av guiden för assisterad konfiguration **Migrera affärsdata**. Lär dig mer på [Gör dig redo att göra affärer](ui-get-ready-business.md).  

> [!IMPORTANT]
> Bokför inte det ingående saldot direkt i redovisningen. När du har transaktioner på redovisningskontot som bokförts direkt till det, kan du normalt inte stämma av bankkontot. Med bankkonton i utländsk valuta innebär en sådan åtgärd att skillnaderna ackumuleras när du bokför fler bankavstämningar. Vanligtvis bokförs det ingående banksaldot direkt på bank-kontot och beloppet fylls sedan i på redovisningskontot. Du kan också ångra det senare mot det redovisningskonto som du använder för att balansera det öppna redovisningssaldot. I båda fallen måste du balansera eventuell direkt bokföring till redovisningskontot innan du börjar med den första bankkontoavstämningen&mdash;framför allt om bankkontot är i en utländsk valuta.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files" />Så här skapar du ett bankkonto för import eller export av bankfilerna

Fälten relaterade till import och export av bankfeeds och filer finns på snabbfliken **Överför** på sidan **Bankkontokort**. Läs mer i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) och [Konfigurera tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Välj ![glödlampan som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. Öppna kortet för bankkontot som du ska exportera eller importera bankfiler för.
3. I snabbfliken **Överför** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andra filexporttjänster och deras format kräver olika inställningsvärden på sidan **bankkontokort**. Du får information om vilka inställningsvärden som är fel eller saknas när du exporterar filen. Läs noga igenom de korta beskrivningarna av fälten eller se relaterad procedur i närliggande ämnen. Till exempel kräver export av en betalningsfil för nordamerikansk elektronisk överföring att både fältet **Sista kundremissnr.** och fältet **Transitnr.** fylls i. Läs mer i [Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Fälten på snabbfliken **Transit** på bankkontot har olika syften, beroende på om betalningen är inkommande eller utgående.

I bilden nedan visas flödet av ankommande betalningar (nummer i beskrivningen motsvarar värdena i bilden):

:::row:::
    :::column:::

1. Transaktionerna exporteras från bankkontot i ett läsbart CSV-format eller till bankens egna format.
2. *Datautbytesdefinition* mappar informationen i filen till fälten i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Så här skapar du dataintegration](across-set-up-data-exchange.md)
3. I *inställningarna för export/import av data* definieras exporten eller importen och länkar till datautbytesdefinitionen.
4. *Importformatet för bankutdrag* länkar importinställningarna till bankkontot.
5. Betalningarna importeras med hjälp av **Betalningsavstämningsjournal** eller från sidan **Bankkontoavstämning**.

  :::column-end:::
  :::column:::

        ![Illustration av betalningar som erhållits från banken till bankkonton.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Inkommande betalningar importeras alltid med hjälp av **Betalningsavstämningsjournal** eller direkt till sidan **Bankkontoavstämning**. Utgående betalningar kan däremot utgå från alla utbetalningsjournaler. Det enda som krävs är att fältet **Tillåt betalningsexport** i relevant betalningsjournal måste väljas.

I bilden nedan visas flödet av utgående betalningar (nummer i beskrivningen motsvarar värdena i bilden):

:::row:::
    :::column:::

6. Transaktionerna fylls i en utbetalningsjournal som har förberetts för export av betalningar till fil.
7. *Importformatet för bankutdrag* länkar importinställningarna till bankkontot.
8. I *inställningarna för export/import av data* definieras exporten eller importen och länkar till datautbytesdefinitionen.
9. *Datautbytesdefinition* mappar informationen i filen till fälten i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Så här skapar du dataintegration](across-set-up-data-exchange.md)
10. Betalningarna exporteras från utbetalningsjournalen och importeras till bankkontot.

  :::column-end:::
  :::column:::

        ![Illustration av betalningar från bankkonton som skickas till banken.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files" />Så här skapar du leverantörsbankkonto för export av bankfiler

Fälten på snabbfliken **Överför** på sidan **Leverantörsbankkontokort** är relaterade till exporten av bankfeeds och filer. Läs mer i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) och [Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account" />Ändra ditt bankkonto

För att använda ett annat bankkonto för företaget måste du skapa det nya bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)]. Vi rekommenderar att du inte bara ersätter informationen om det konto som du använder för tillfället, eftersom det kan orsaka felaktiga data. Den ingående balansen kan t.ex. vara felaktig eller också kan bankens flöde sluta fungera som det ska. Det är viktigt att du behåller det aktuella och nya kontot separat.

När du har skapat det nya bankkontot bör du också skapa en ny bokföringsmall och tilldela den till ett nytt redovisnings konto. Du kan återanvända en befintlig bokföringsmall och banktransaktioner bokförs på samma redovisningskonton som övriga bankkonton som delar bankens bokföringsmall. Vi rekommenderar dock att du skapar en ny bankbokföringsmall och ett redovisningskonto så att avstämningarna blir enklare att göra.

> [!NOTE]
> Tänk på att bankkontoinformationen på öppna försäljningsfakturor fortfarande visar det ursprungliga bankkontot. Därför kommer betalningar fortfarande att bokföras på det kontot. Vi rekommenderar att du håller båda kontona aktiva i en viss tidsperiod efter ändringen.

För att få en mer sammandragen bild av dina konton i den finansiella rapporteringen, använd kontona **Från-summa** och **Till-summa** i din kontoplan, raderna **Summeringsintervall** i ekonomiska rapporter eller redovisningskontokategorier. Läs mer i avsnittet [Business Intelligence och Financial Reporting](bi.md).

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Ställa in bankverksamhet](bank-setup-banking.md)  
[Ställa in bokföringsmallar](finance-posting-groups.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[SEPA-autogiro i Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Så här ställer du in ditt bankkonto för SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Så här lägger du upp ett bankkonto för SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Gör betalningar med tillägget AMC Banking 365 Fundamentals eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Betalningsavstämning](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Så här fungerar i redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

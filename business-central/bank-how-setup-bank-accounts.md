---
title: Skapa bankkonton (innehåller video)
description: Läs om hur bankkonton används i Business Central och hur du kan stämma av belopp med din bank.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: 922d80f054b2daea6c06b7c440ac3605fa0bd243
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529386"
---
# <a name="set-up-bank-accounts"></a>Skapa bankkonton

Du använder bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)] för att hålla reda på dina banktransaktioner. Konton kan definieras i den lokala valutan eller i en utländsk valuta. När du har skapat bankkonton kan du också använda funktionen för utskrift av checkar. Bankkontona innehåller extra funktionalitet för [betalningsavstämning](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankavstämningen](bank-how-reconcile-bank-accounts-separately.md) bankavstämning och import och export av bankfiler. Bankkontona kan också inkluderas i transaktioner i redovisningsjournalerna. Varje bankkonto är länkat till ett konto i kontoplanen via den tilldelade bankkontobokföringsmallen. Om du använder ett bankkonto i en betalningstransaktion skapas automatiskt en transaktion på både bankkontot och det anslutna redovisningskontot.  

Bankkonton fungerar olika beroende på om en valutakod har angetts:

- Valutakoden är tom

  Alla transaktioner på bankkontot kommer att ske i den lokala valutan (BVA) för det aktuella företaget. Om en transaktion görs till kontot i en annan valuta bokförs beloppen på kontot i BVA baserat på den aktuella valutakursen. Alla checkar som utfärdas från det här kontot måste utfärdas i BVA. Om bank kontot används i en journal kommer Journal raden automatiskt att ärva den tomma valuta koden.  
- Valutakoden anges

  Alla transaktioner som görs till det här kontot måste vara i samma valuta som har angetts på kontot. Alla checkar som utfärdas från det här kontot måste också ha denna valuta.  

Du kan spara tid genom att göra ett bankkonto till det standardkonto som ska användas för den valuta som har angetts för kontot. Om du gör det kommer kontot att tilldelas försäljnings- och servicedokument som använder valutan. Om du vill att kontot ska vara standard för försäljnings- och servicedokument på sidan **Bankkontokort** aktiverar du reglaget **Använd som standard för valuta**. Om det behövs kan du välja ett annat konto när du arbetar med ett dokument.

Ett bank konto är en integrerad del av [!INCLUDE[prod_short](includes/prod_short.md)] och spelar en roll i många andra funktioner. Följande illustration visar de viktigaste relationerna:

![Illustration av bankkontorelationer.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Det innebär att du skapar ett bankkonto, gör det tillgängligt på alla platser som visas ovan och speglas i för det aktuella redovisningskontot och på sidan **Företagsinformation**.

Ett bankkonto övervakas oftast dagligen för att säkerställa att alla nya betalningar från kunder registreras så snabbt som möjligt. På så sätt kan du se till att kundernas faktiska status återspeglas i [!INCLUDE[prod_short](includes/prod_short.md)] så att säljare, personer, revisorer och andra anställda har tillgång till relevant och aktuell information. På så sätt undviker de inte onödiga samtal till kunden om förfallna fakturor eller förseningar i försändelser.  

![Illustration av bankbetalning.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

En annan uppgift är att importera leverantörens valuta betalningar med faktiska valutakurser för att försäkra dig om att leverantörens faktiska status är aktuell. Det enklaste sättet att säkerställa att bankkontot uppdateras är att använda funktionen för [betalningsavstämning](receivables-apply-payments-auto-reconcile-bank-accounts.md). I **betalningsavstämningsjournal** kan du importera banktransaktioner direkt från ett bankprogram online och låta dem bokföras mer eller mindre automatiskt. Journalen identifierar och bokför automatiskt följande:  

- Direkt debitering av betalningar från kunder  
- Kundbetalningar av enstaka fakturor  
- Betalningar i klumpsumma från kunder.  
- Kundbetalningar i utländska valutor  
- Leverantörsbetalningar  
- Leverantörsbetalningar i utländska valutor  
- Återkommande leverantörsbetalningar och abonnemang  
- Bankavgifter och intressen  

Betalningsavstämningen ger en enorm tidsbesparing vid bokföring av inkommande och utgående betalningar. Transaktionerna på bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] anses dock inte vara 100 % riktigt förrän du kör en bankkontoavstämning.  

Bankkontoavstämningen är hur du ser till att bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] matchar det externa kontot hos banken.  

 ![Illustration av bankkontoavstämning.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

I bilden ovan representerar den vänstra sidan bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] och den högra sidan representerar de transaktioner som importerats från banken via bankprogrammet online. I diagrammet i mitten visas transaktionerna från båda sidorna, som är bankkontoavstämning.

Från bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)] bör de flesta transaktionerna vara kända för den fysiska banken. De enda undantagen är följande fall:  

- Korrigeringar som bokförts i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Utfärdade checkar som inte har registrerats ännu  
- Leverantörsbetalningar som inte har godkänts av banken  

Från det fysiska kontot i banken kommer okända transaktioner som inte har identifierats i betalningsavstämningsjournalen att tas med i tiden, till exempel följande:  

- Nya leverantörsabonnemang  
- Kundbetalningar utan beskrivning
- Bankens intressen
- Bankavgifter
- Kreditkortsdebitering som ännu inte har rapporterats

Den bättre mappningsinformation som du gör i betalningsavstämningsjournal, desto fler transaktioner bokförs automatiskt och desto enklare blir den periodiska bankavstämningen.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Vissa fält kan innehålla känslig information, till exempel fälten **Bankfilialsnr.**, **Bankkontonr.**, **SWIFT-kod** och **IBAN-kod**. Mer information finns i [Övervaka känsliga fält](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Så här skapar du bankkonton

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. På sidan **Bankkonton** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Till exempel kopplar fältet **Bokföringsmall för bank-konto** bank-kontot till det underliggande redovisningskontot i balansräkningen. Mer information finns i [Konfigurera bokföringsmallar](finance-posting-groups.md).

> [!TIP]
> Vissa fält är dolda tills du väljer **Visa fler** åtgärder, vanligen på grund av att de används sällan. Andra måste läggas till genom anpassning. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

Du kan skapa så många bankkonton som du behöver för ditt företag. För varje bankkonto måste du ange information som gör bankkontot unikt identifierbart. Den här informationen omfattar bankens geografiska adress, nummerserie för olika typer av transaktioner, till exempel direktdebitering och kreditöverföringar, valutan som anges i och information som används för import av bankutdrag. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->

## <a name="entering-an-opening-balance"></a>Ange ett ingående saldo

Så här fyller du i fältet **Saldo** med en ingående balans, du måste bokföra en bankkontotransaktion med beloppet i fråga. Du kan göra detta genom att utföra en bankkontoavstämning. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).  
>
> Alternativt kan du implementera den ingående balansen som en del av skapande av allmänna data i nya företag med hjälp av den assisterad inställningsguide **Migrera affärsdata**. Mer information finns i [Komma igång med att göra affärer](ui-get-ready-business.md).  

> [!IMPORTANT]
> Det är viktigt att du inte bokför det ingående saldot direkt i redovisningen. Om du har transaktioner på redovisningskontot som bokförs direkt till redovisningskontot kommer du normalt sett inte att kunna stämma av bankkontot eller – om det rör sig om bankkonton i utländsk valuta – leda till att differenser ackumuleras när du bokför fler bankavstämningar. Ofta bokförs det ingående banksaldot direkt på bank-kontot och beloppet fylls sedan i på redovisningskontot. Du kan också ångra det senare mot det redovisningskonto som du använder för att balansera det öppna redovisningssaldot. I båda fallen måste du balansera eventuell direkt bokföring till redovisningskontot innan du börjar med den första bankkontoavstämningen, framför allt om bankkontot är i en utländsk valuta.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Så här skapar du ett bankkonto för import eller export av bankfilerna

Fälten relaterade till import och export av bankfeeds och filer finns på snabbfliken **Överför** på sidan **Bankkontokort**. Mer information finns i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) och [Konfigurera tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. Öppna kortet för ett bankkonto som du ska exportera eller importera bankfiler.
3. I snabbfliken **Överför** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andra filexporttjänster och deras format kräver olika inställningsvärden på sidan **bankkontokort**. Du får information om vilka inställningsvärden som är fel eller saknas när du exporterar filen. Läs noga igenom de korta beskrivningarna av fälten eller se relaterad procedur i närliggande ämnen. Till exempel exportera en betalningsfil för nordamerikansk elektronisk överföring kräver att både fältet **Sista kundremissnr.** och fältet **Transitnr.** fylls i. Mer information finns i [Så här exporterar du betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Fälten på snabbfliken **Transit** på bankkontot har olika syften, beroende på om betalningen är inkommande eller utgående.

Bilden visar flödet av ankommande betalningar:

:::row:::
    :::column:::
        1. Transaktionerna exporteras från bankkontot i ett läsbart CSV-format eller till bankens egna format.
        <br><br>
2. *Datautbytesdefinition* mappar informationen i filen till fälten i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Ange Dataintegration](across-set-up-data-exchange.md)
<br><br>
3. I *inställningarna för export/import* av data definieras exporten eller importen och länkar till datautbytesdefinitionen.
<br><br>
4. *Importformatet för bankutdrag* länkar importinställningarna till bankkontot.
<br><br>
5. Betalningarna importeras med hjälp av **Betalningsavstämningsjournal** eller från sidan **Bankkontoavstämning**.
    :::column-end:::
    :::column:::
        ![Illustration av betalningar som erhållits från banken till bankkonton.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Inkommande betalningar importeras alltid med hjälp av **Betalningsavstämningsjournal** eller direkt på sidan **Bankkontoavstämning**. Utgående betalningar kan däremot utgå från alla utbetalningsjournaler. Det enda som krävs är att fältet **Tillåt betalningsexport** i relevant betalningsjournal måste väljas.

Bilden visar flödet av avgående betalningar:

:::row:::
    :::column:::
        6. Transaktionerna som fyllts i en utbetalningsjournal som har förberetts för export av betalningar till fil.
        <br><br>
        7. *Importformatet för bankutdrag* länkar importinställningarna till bankkontot
        <br><br>
        8. I *inställningarna för export/import* av data definieras exporten eller importen och länkar till datautbytesdefinitionen.
        <br><br>
        9. *Datautbytesdefinition* mappar informationen i filen till fälten i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Ange Dataintegration](across-set-up-data-exchange.md)
        <br><br>
        10. Betalningarna exporteras från utbetalningsjournalen och importeras till bankkontot
    :::column-end:::
    :::column:::
        ![Illustration av betalningar från bankkonton som skickas till banken.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Så här skapar du leverantörsbankkonto för export av bankfiler

Fälten på snabbfliken **Överför** på sidan **Leveraqntörsbankkontokort** är relaterade till export av bankfeeds och filer. Mer information finns i [Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) och [Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Ändra ditt bankkonto

Om du vill använda ett annat bankkonto för företaget måste du skapa det nya bankkontot i [!INCLUDE[prod_short](includes/prod_short.md)]. Vi rekommenderar att du inte bara ersätter informationen om det konto som du använder för tillfället, eftersom det kan orsaka felaktiga data. Den ingående balansen kan t.ex. vara felaktig eller också kan bankens flöde sluta fungera som det ska. Det är viktigt att du behåller det aktuella och nya kontot separat.

När du har skapat det nya bankkontot bör du också skapa en ny bokföringsmall och tilldela den till ett nytt redovisnings konto. Du kan återanvända en befintlig bokföringsmall och banktransaktioner bokförs på samma redovisningskonton som övriga bankkonton som delar bankens bokföringsmall. Vi rekommenderar dock att du skapar en ny bankbokföringsmall och ett redovisningskonto så att avstämningarna blir enklare att göra.

> [!NOTE]
> Tänk på att bankkontoinformationen på öppna försäljningsfakturor fortfarande visar det ursprungliga bankkontot. Därför kommer betalningar fortfarande att bokföras på det kontot. Vi rekommenderar att du håller båda kontona aktiva i en viss tidsperiod efter ändringen.

För att få en mer sammandragen bild av dina konton i den finansiella rapporteringen, använd kontona **Från-summa** och **Till-summa** i dina kontoplan, raderna **Summeringsintervall** i kontouppställningar eller kontokategorier. Mer information finns i avsnittet [Business Intelligence och Financial Reporting](bi.md).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

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

---
title: SEPA-autogiro i Business Central
description: Med kundens samtycke kan du samla in betalningar direkt från kundens bankkonto enligt SEPA-formatet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="collect-payments-with-sepa-direct-debit"></a>Samla in betalningar med SEPA-autogiro

Med kundens samtycke kan du samla in betalningar direkt från kundens bankkonto enligt SEPA-formatet.  

Först ställer du in exportformat för bankfilen som används av din bank för att utföra en autogiro. Därefter ställer du in kundens betalningssätt. Till sist ställ in medgivande för autogiro att återspegla ditt avtal med kunden för att samla in sina betalningar under en viss avtalsperiod.  

Om du vill instruera banken för att överföra betalningsbeloppet från kundens bankkonto till ditt företags konto skapar du en autogiroinsamlingpost som innehåller information om bankkonton, berörda försäljningsfakturor och medgivande för autogiro. Sedan kan du exportera en XML-fil som baseras på samlingstransaktionen som du skickar till din bank för bearbetning. Alla betalningar som inte kunde behandlas meddelas till dig av din bank och du måste sedan manuellt avvisa de aktuella autogiroinsamlingsposterna.  

Du kan ställa in standardiserade kundförsäljningskoder med metoden för autogirobetalning och obligatorisk information. Du kan sedan använda batch-jobbet **Skapa standard kundfakturor** för att generera flera försäljningsfakturor med direktdebiteringsinformationen ifylld automatiskt. Detta kan göras manuellt eller automatiskt enligt betalningens förfallodatum.  

När betalningar har behandlas enligt din bank, kan du bokföra betalningsinleveranser antingen direkt från sidan **Transaktioner för samlingar med autogiro** eller genom att flytta betalningsraderna i journalen när du bokför betalningsinleveranser, såsom sidan **Inbetalningsjournal**. Beroende på processen för hantering av kontanter, kan du också vänta och använda betalningarna som en del av bankavstämning.  

> [!NOTE]  
> För att samla in betalningar med hjälp av SEPA Autogiro måste valutan på försäljningsfakturan vara EURO.  

## <a name="setting-up-sepa-direct-debit"></a>Konfigurera SEPA Autogiro

Från sidan **Samlingar med autogiro** kan du exportera instruktioner till din Internetbank för autogirobetalning från kundens bankkonto till ditt bankkonto enligt formatet för SEPA-autogiro.

> [!NOTE]
> Den globala versionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder endast formatet SEPA Autogiro. I versionen för Sverige kan andra format för elektronisk betalning vara tillgängliga. Se under **Lokal funktionalitet** i innehållsförteckningen.  

Om du vill aktivera export av bankfilformat som inte stöds från början i [!INCLUDE[prod_short](includes/prod_short.md)], kan du konfigurera en datautbytesdefinition med ramverket för datautbyte. Mer information finns i [Så här konfigurerar du dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Innan du kan bearbeta kundbetalningar på elektronisk väg genom att exportera instruktioner om autogiro i formatet SEPA-autogiro måste du utföra följande inställningssteg:  

* Ställ in exportformat för bankfilen i syfte att instruera din bank att utföra en autogiroinsamling från kundens bankkonto till ditt bankkonto.  
* Ställ in kundens betalningssätt.  
* Ställ in medgivande för autogiro att återspegla ditt avtal med kunden för att samla in sina betalningar under en viss avtalsperiod.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Så här ställer du in ditt bankkonto för SEPA-autogiro

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.  
2. Öppna det bankkonto som du vill använda för autogiro.  
3. På snabbfliken **Överföring**, i fältet **Exp.format för SEPA-autogiro**, välj alternativet för SEPA-autogiro.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>För att ställa in kundens betalningssätt för SEPA-autogiro

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **betalningsmetoder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Så här anger du betalningssätt. Fyll i de specifika fälten för autogiro\-enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Autogiro**|Ange om betalningsmetoden används för SEPA-autogiroinsamling.|  
    |**Betalningsvillkorskod för autogiro**|Ange betalningsvillkor, till exempel BETALA INTE, som visas på försäljningsfakturor som betalas med SEPA-autogiro i syfte att visa kunden att betalningen kommer att överföras automatiskt. Du kan även lämna fältet tomt.|  

    > [!NOTE]  
    >  Ange inte ett värde i fältet **Motkonto.**  

4. Välj **OK** för att stänga sidan **Betalningssätt**.  
5. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.  
6. Öppna kortet för den kund som du vill ställa in för SEPA-autogiroinsamling.  
7. Välj **Betalningssätt**-fältet och välj sedan koden för betalningssätt som du angav i steg 3.  
8. Upprepa steg 6 till och med 7 för alla kunder som du vill ställa in för SEPA-autogiroinsamling.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Så här ställer du in medgivande för autogiro som representerar kundavtalet

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.  
2. Öppna kortet för den kund som du vill ställa in för SEPA-autogiro.  
3. Välj åtgärden **bankkonton**.  
4. På sidan **Kund bankkontolista** väljer du det kundbankkonto som ska använda autogiro och väljer sedan åtgärden **Autogiromedgivanden**.  
5. På sidan **SEPA Autogiromedgivanden** fyller du i fälten enligt instruktionerna i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kund bankkontokod**|Anger det bankkonto som\-autogirobetalningar samlas in från. Detta fält fylls i automatiskt.|  
    |**Giltig från**|Ange det datum när medgivande för\-autogiro startar.|  
    |**Giltig till**|Ange det datum när medgivande för\-autogiro upphör.|  
    |**Signeringsdatum**|Ange det datum när kunden signerade medgivande för\-autogiro.|  
    |**Typ av betalning**|Ange om avtalet omfattar flera (**återkommande**) eller en enda (**Enstaka**) autogiroinsamling.|  
    |**Förväntat antal debet**|Ange hur många autogiroinsamlingar som du förväntar dig att göra. Det här fältet gäller bara om du har valt **Återkommande** i fältet **Typ av betalning**.|  
    |**Antal debet**|Anger hur många autogiroinsamlingar som har gjorts med hjälp av medgivande\-av autogiro. Fältet uppdateras automatiskt.|  
    |**Spärrad**|Anger att autogiroinsamlingar inte kan göras med hjälp av medgivande av\-autogiro.|  

6. Upprepa steg 1 till och med 5 för alla kunder som du vill ställa in för SEPA-autogiro.  

 Medgivande för autogiro infogas automatiskt i fältet **Medgivande-ID för autogiro** när du skapar en försäljningsfaktura för den kund som du valde i steg 2. Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil

Om du vill instruera banken att överföra betalningsbeloppet från kundens bankkonto till ditt företags konto skapar du en autogirobetalning som innehåller information om kundens bankkonto, berörda försäljningsfakturor och medgivande för autogiro. Från direktdebitering-insamlingsposten som skapas kan du sedan exportera en XML-fil som du skickar eller överför till din elektroniska bank för bearbetning. Alla betalningar som inte kunde behandlas av banken meddelas till dig av din bank och du måste sedan manuellt avvisa de aktuella autogiroinsamlingsposterna.  

 > [!NOTE]  
 > För att samla in betalningar med hjälp av SEPA Autogiro måste valutan på försäljningsfakturan vara EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Skapa en direktdebitering-insamling

 1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Samlingar med autogiro** och väljer sedan relaterad länk.  
 2. På sidan **Samlingar med autogiro** väljer du åtgärden **Skapa samling med autogiro**.  
 3. På sidan **Skapa samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Från förfallodatum**|Ange tidigaste betalningsförfallodatumet på försäljningsfakturor som du vill skapa en direktdebitering-insamling för.|  
    |**Till förfallodatum**|Ange senaste betalningsförfallodatumet på försäljningsfakturor som du vill skapa en direktdebitering-insamling för.|  
    |**Partnertyp**|Anger om direktdebitering-insamlingen görs för kunder som är av typen **företag** eller **person**.|  
    |**Endast kunder med giltigt medgivande**|Ange om en autogiroinsamling skapas för kunder som har ett giltigt medgivande för autogiro. **Obs!**  En autogiroinsamling skapas även om fältet **Medgivande-ID för autogiro** inte fylls på försäljningsfakturan.|  
    |**Endast fakturor med giltigt medgivande**|Ange om en autogirering skapas för försäljningsfakturor endast om ett giltigt autogiromedgivande väljs i fältet **Medgivande-id för autogiro** på försäljningsfakturan.|  
    |**Bankkontonr.**|Ange vilka av ditt företags bankkonton som den insamlade betalningen ska överföras till från kundens bankkonto.|  
    |**Bankkontonamn**|Anger namnet på det bankkonto som du väljer i **Bankkontonr** fält. Detta fält fylls i automatiskt.|  

 4. Välj knappen **OK**.  

En autogiroinsamling läggs till på sidan **Autogiroinsamlingar** och en eller flera autogiroinsamlingsposter skapas.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Så här exporterar du direktdebeterings-insamlingposter till en bankfil

 1. På sidan **Samlingar med autogiro** väljer du åtgärden **Transaktioner för samlingar med autogiro**.  
 2. På sidan **Transaktioner för samlingar med autogiro** väljer du den post som du vill exportera och väljer sedan åtgärden **Skapa autogirofil**.  
 3. Spara exportfilen på den plats från vilken du skickar eller överför den till din elektroniska bank.  

      På sidan **Transaktioner för samlingar med autogiro** kan fältet **Status för autogirosamling** ändras till fil. På sidan **SEPA Autogiromedgivanden** kan fältet **Debet antal** uppdateras fältet med ett antal.  

 Om den exporterade filen inte kan behandlas, till exempel eftersom kunden är insolvent, kan du avvisa direktdebitering-insamlingsposten. Om den exporterade filen har bearbetats av banken, samlas automatiskt förfallna betalningar på de berörda försäljningsfakturorna från berörda kunder. I så fall kan du stänga samlingen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Avvisa en direktdebitering-insamlingspost

* På sidan **Transaktioner för samlingar med autogiro**, markera den post som inte behandlades korrekt, och välj åtgärden **Avvisa transaktion**.  

    Värdet i fältet **Status** på sidan **Transaktioner för samlingar med autogiro** ändras till **Avvisad**.  

### <a name="to-close-a-direct-debit-collection"></a>Stänga en direktdebitering-insamling

* På sidan **Transaktioner för samlingar med autogiro**, markera den post som behandlades korrekt, och välj åtgärden **Stäng samling**.  

    Relaterade direktdebitering-insamlingen är stängd.  

 Du kan nu fortsätta med att bokföra inleveranser för de berörda försäljningsfakturorna. Du kan göra detta om du ofta bokför betalningsinleveranser, som på sidan **Betalningsregistrering** eller också kan du bokföra de relaterade betalningsinleveranser direkt från sidan **Transaktioner för samlingar med autogiro**. Mer information finns i [kräva in betalningar med SEPA direktdebitering](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts"></a>Bokföra betalningsinleveranser för SEPA Autogiro

När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna. För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Du kan bokföra Betalningsinleverans direkt från sidan **Samlingar med autogiro** eller sidan **Transaktioner för samlingar med autogiro**. Alternativt kan du vidarebefordra arbetet till en annan användare genom att förbereda de relaterade journalraderna.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Så här bokför du ett betalningskvitto på sidan Samlingar med autogiro

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Samlingar med autogiro** och väljer sedan relaterad länk.  
2. Välj en rad för en autogiroinsamling som har exporterats till en bankfil och framgångsrikt bearbetats av banken.
3. Välj åtgärden **Bokför betalningsinleveranser**.  
4. På sidan **Bokför samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Autogirosamlingsnr.**|Ange autogiroinsamlingen som du vill bokföra betalningskvittot för.|  
    |**Redovisningsjournalmall**|Ange vilken redovisningsjournalmallen som ska användas för att bokföra betalningskvitto, t. ex. mall för inbetalningar.|  
    |**Redovisningsjournalnamn**|Ange vilka redovisningsjournalbatch som ska användas för att bokföra ett betalningskvitto.|  
    |**Skapa enbart journal**|Markera den här kryssrutan om du inte vill bokföra betalningskvittot när du väljer **OK** knappen. Betalningskvittot skall förberedas i den angivna journalen och bokförs inte förrän någon bokför journalraderna i fråga.|  

5. Välj **OK**.

## <a name="see-also"></a>Se även

[Hantera kundreskontra](receivables-manage-receivables.md)  
[Servicehantering](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

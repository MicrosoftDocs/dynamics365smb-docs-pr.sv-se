---
title: 'Ställa in och fakturera Förskottsbetaln., försäljning'
description: Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning

Denna genomgång visar hur du konfigurerar och använder förskottsbetalningar i [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Du kan till exempel skicka fler förskottsfakturor om fler artiklar läggs till i ordern.  

## <a name="about-this-walkthrough"></a>Om den här genomgången

Den här genomgången kommer att innehålla följande scenarion:  

- Lägga upp förskottsbetalningar  
- Skapa en order som kräver förskottsbetalning  
- Skapa en förskottsfaktura  
- Korrigera förskottsbetalningskrav för en order  
- Använda förskottsbetalningar för en order  
- Fakturera slutbeloppet på en order med en förskottsbetalning  

### <a name="roles"></a>Roller

Den här genomgången innehåller aktiviteter för följande roller:  

- Redovisningschef (Phyllis)  
- Orderhandläggare (Susan)  
- Kundreskontraadministratör (Arnie)  

## <a name="story"></a>Situation

 Phyllis är redovisningschef och fattar beslut om vilka kunder som måste betala en deposition innan artiklar tillverkas eller levereras. Phyllis lägger upp [!INCLUDE[prod_short](includes/prod_short.md)] för att beräkna förskottsbetalningar automatiskt.  

 Susan är försäljningsorderhandläggare. När en kund ringer in en order registrerar Susan ordern i systemet medan kunden är i telefon. På så sätt kan Susan verifiera priser och betalningsvillkor med kunden omedelbart, och hon kan göra ändringar i ordern medan hon förhandlar med kunden.  

 Arnie arbetar på kundreskontraavdelningen där han bokför fakturor och betalningar.  

 I det här scenariot lägger Phyllis upp förskottsbetalningskrav för kunden Service AB, baserat på deras kredithistorik. Phyllis ger Susans instruktioner för hur order ska hanteras.  

 När kunden ringer förhandlar Susan med kunden tills de når en överenskommelse och väljer sedan att beräkna förskottsbetalningen på flera olika sätt.  

 När Susan har skickat förskottsfakturan beställer kunden ytterligare en artikel. Susan uppdaterar order och skapar en förskottsfaktura.  

 Arnie registrerar kundens betalning och bokför den mot fakturorna och skickar sedan den sista fakturan.  

## <a name="set-up-prepayments"></a>Konfigurera förskottsbetalningar

Phyllis konfigurerar systemet för hantering av förskottsbetalningar från kunder.  

- Phyllis väljer att ha samma nummerserie för förskottsbetalningar som för fakturering av försäljning.  
- Phyllis konfigurerar programmet så att det kontrollerar om förskottsbetalningar krävs innan slutgiltig fakturering görs av en order.  
- Phyllis lägger upp standardvärden för hur stor del av fakturan som ska förskottsbetalas för särskilda artiklar och kunder.  

I följande procedurer beskrivs hur Phyllis uppgifter ska utföras:  

### <a name="to-set-up-number-series-for-prepayments"></a>Så här lägger du upp nummerserier för förskottsbetalningar

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.  
2. På sidan **Försäljningsinställningar** expanderar du snabbfliken **Nummerserier**.  
3. Kontrollera att nummerserien för bokförda förskottsfakturor i fältet **Försk.fakt.nr.serie (bokförd)** är samma som för bokförda försäljningsfakturor (**Fakturanr-serie (bokförd)**) och att nummerserien för bokförda förskottskreditnotor (**Försk.kredit.nr.serie (bokförd)**) är samma som för bokförda kreditnotor (**Kreditnotenr-serie (bokförd)**).  

### <a name="to-block-shipments-for-unpaid-prepayment"></a>Så här spärrar du utleveranser för obetalda förskottsbetalningar

1. På sidan **Försäljningsinställningar**, på snabbfliken **Allmänt**, markerar du kryssrutan **Kontrollera förskottsbet. vid bokföring**.

Nu kan du inte utleverera eller fakturera en order med ett obetalt förskottsbetalningsbelopp.  

Phyllis kräver att kunden 20000 ska faktureras 30 % i förskott för alla order. Därför anger Phyllis ett procentuellt standardvärde för förskottsbetalning.  

Phyllis kräver att alla kunder ska faktureras 20 % i förskott för artikel 1896-S. Kunden 20000 har dålig betalningshistorik så Phyllis kräver 40 % i förskottsbetalning från kund 20000 för artikel 1896-S. I följande exempel visas hur du lägger upp procentuella standardvärden för förskottsbetalningar.  

### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Så här tilldelar du kunder och artiklar procentuella standardvärden för förskottsbetalningar

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.  
2. Öppna kortet för kund 20000 (Trey Research).
3. På snabbfliken **Betalningar**, i fältet **Förskottsbetalning %**, anger du **30**.  
4. Välj åtgärden **Relaterat**, markera menyalternativet **Försäljning** och välj sedan menyalternativet **Procentsatser för förskottsbetalning**.  
5. Fyll i de två raderna på sidan **Procentandelar, förskottsbetalning för försäljning** enligt nedan:  

    |**Förs.typ**|**Förs.kod**|**Artikelnr**|**Förskottsbetalning %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Kund**|**20000**|**1896-S**|**40**|
    |**Kund**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Beroende på ditt land/din region måste du också ange en skattegruppskod på snabbfliken **Kostnader och bokföring** för artikel 1896-S. När du använder demonstrationsföretaget är det här fältet redan inställt.

6. Stäng alla sidor.  

### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Så här kan du skriva in ett konto för utgående förskottsbetalningar i bokföringsinställningarna

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Bokföringsinställningar** och välj sedan relaterad länk.  
2. Markera raden där fältet **Gen. rörelsebokföringsmall** anges till **INRIKES** och fältet **Produktbokföringsmall** anges till **ÅTERFÖRSÄLJNING**.  
3. I fältet **Förskottsbet.konto, försäljning** anges relevant konto. Ditt val sparas automatiskt.  

> [!TIP]
> Om fältet på sidan **Bokföringsinställningar** inte visas kan du använda den vågräta rullningslisten längst ned på sidan för att rulla åt höger.  

## <a name="create-an-order-that-requires-a-prepayment"></a>Skapa en order som kräver förskottsbetalning

 I följande scenario skapar Susan, orderhandläggaren, en order medan hon pratar med en kund. De artiklar som kunden beställer kräver en förskottsbetalning. Dessutom har kunden gjort sent betalningar tidigare. Susan har blivit instruerad att kräva ett fast belopp på **800** som förskottsbetalning för ordern.  

Kunden önskar betala 35 % vilket Susan går med på och ändrar ordern därefter.  

Susan skapar en förskottsfaktura och skickar den till kunden.  

### <a name="to-create-a-sales-order-with-a-prepayment"></a>Så här skapar du en försäljningsorder med förskottsbetalning

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Kundnamn** väljer du **Trey Research**.  
4. Stäng varningen för förfallet saldo som visas.  
5. Fyll i två försäljningsrader med följande information.  

    |**Radtyp**|**Nr**|**Antal**|  
    |--------------|-------------|------------------|  
    |**Artikel**|**1896-S**|**1**|  
    |**Artikel**|**1900-S**|**1**|

    Förskottsfälten på försäljningsraden är dolda som standard. Om du vill visa fälten måste du anpassa sidan. Mer information finns i [Så här börjar du anpassa en sida genom den anpassningsbanderollen](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Kontrollera att fältet **Förskottsbetalning %** på raden med artikel **1900-S** innehåller värdet **30**. Standardvärdet hämtades från försäljningshuvudet som kopierades från kundkortet.  

    Fältet **Förskottsbetalning %** på raden med artikel **1896-S** innehåller värdet **40**. 40 är den procentsats som du angav på sidan **Procentandelar, förskottsbetalning för försäljning** för artikel **1896-S** och kund **20000**.  

    Mer information finns i [Ange Förskottsbetalningar](finance-set-up-prepayments.md).  
7. I åtgärden **Order** väljer du **Statistik**.  
8. På snabbfliken **Förskottsbetalning** innehåller fältet **Förskottsbetalningsbelopp exkl. moms** värdet **458,16**. Om du skapar en förskottsbetalning för ordern nu, är 458,16 beloppet som visas på fakturan.  

    I det här scenariot har Susan blivit instruerad att föreslå en fullständig förskottsbetalning på **800** för ordern.  

    > [!IMPORTANT]  
    >  Beroende på ditt land/din region kan följande steg eventuellt inte utföras.  
9. Ändra värdet i fältet **Förskottsbetalning exkl. moms** till **800** och stäng sedan sidan.  
10. Kontrollera fältet **Förskottsbetalning %** på försäljningsraderna så ser du att det har ändrats till **67,02438** och **67,02282**.  

     Omräkningen inkluderar alla rader med en procentuell förskottsbetalning som är större än 0.  

     Nu frågar kunden om den procentuella förskottsbetalningen kan ändras till 35 %. Susans chef godkänner ändringen.
11. På sidan **Förs.order**, under snabbfliken **Förskottsbetalning**, i fältet **Förskottsbetalning %** anger du **35**.  
12. Välj **ja** för varningen som visas. En debitering på 35 % används som procentuell förskottsbetalning för hela ordern.  
13. Bekräfta att raderna har uppdaterats korrekt.  

## <a name="create-a-prepayment-invoice"></a>Skapa en förskottsfaktura

När Susan har angett korrekta värden för förskottsbetalning av ordern skapar hon förskottsfakturan och skickar den till kunden.  

### <a name="to-create-a-prepayment-invoice"></a>Så här skapar du en förskottsfaktura

1. På sidan **Försäljningsorder** väljer du **Åtgärder**, sedan **Bokföring**, sedan **Förskottsbetalning** och sedan **Bokför och skriv ut faktura för förskottsbetalning**
2. Klicka på **Ja** för att bokföra fakturan.  

> [!NOTE]  
> Susan skulle nu skicka fakturan till kunden.  

## <a name="create-an-additional-prepayment-invoice"></a>Skapa en ytterligare förskottsfaktura

Följande dag ringer kunden upp Susan och ändrar ordern. Kunden vill ha två stycken av artikel 1896-S. Susan öppnar ordern igen och uppdaterar den och skapar sedan ytterligare en förskottsfaktura för ordern och skickar den till kunden.  

### <a name="to-create-an-additional-prepayment-invoice"></a>Så här skapar du ytterligare en förskottsfaktura

1. På sidan **Försäljningsorder** väljer du åtgärden **Frisläpp** och sedan **Öppna igen**.  
2. På raden för artikel **1896-S** anger du **2** i fältet **Kvantitet**.  

    I åtgärden **Order** väljer du **Statistik**. Fältet **Förskottsbetalning exkl. moms** innehåller nu **768,04** och fältet **Förskottsbetalningsbelopp exkl. moms** innehåller **417,76**. Dessa värden visar att det finns ytterligare förskottsbelopp som ännu inte har fakturerats ännu.  
3. För att bokföra en faktura för extra förskottsbetalningsbelopp väljer du **Åtgärder**, sedan **Bokföring**, sedan **Förskottsbetalning** och sedan **Bokför och skriv ut faktura för förskottsbetalning**
4. Klicka på **Ja** för att bokföra fakturan.  

## <a name="apply-the-prepayments"></a>Använda förskottsbetalningar

Kunden betalar förskottsbeloppet. Arnie, från redovisningsavdelningen, registrerar betalningen och använder den på förskottsfakturorna.  

### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Så här bokför du betalningar mot förskottsfakturor

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inbetalningsjournaler** och väljer sedan relaterad länk.  
2. Fyll i journalraden med följande information.  

    |Fältnamn|Skriv in|  
    |----------------|-----------|  
    |**Dokumenttyp**|**Betalning**|  
    |**Kontotyp**|**Kund**|  
    |**Kontonr**|**20000**|  
3. Välj åtgärden **Process** och sedan **Tillämpa poster**.  
4. På sidan **Tillämpa kundposter** väljer du först faktura för förskottsbetalning och sedan åtgärden **Behandla**, innan du väljer åtgärden **Uppsättningens ID**.  
5. Upprepa det föregående steget för den andra förskottsbetalningen.  
6. Välj **OK**.  

    Fälten **Belopp** har nu fyllts i med summan av de två förstkottsbetalningsfakturorna.  

7. Om du vill bokföra journalen väljer du åtgärden **Bokför/skriv ut** och väljer sedan **Bokför**.
8. Välj **Ja**.

## <a name="invoice-the-remaining-amount"></a>Fakturera återstående belopp

Nu har Arnie blivit informerad om att artiklarna på ordern har levererats och att ordern är klar för fakturering. Arnie skapar fakturan för ordern.  

### <a name="to-invoice-the-remaining-amount"></a>Så här fakturerar du återstående belopp

1. Öppna försäljningsordern.
2. Välj åtgärden **Bokföring** och sedan **Bokför**.
3. Välj **Skicka och fakturera** och välj sedan knappen **OK**.
4. Om du vill förhandsgranska fakturan väljer du knappen **Ja**.

    > [!NOTE]  
    > Normalt har leveransavdelningen redan bokfört utleveransen.  

    Arnie kan visa historiken för att kontrollera att försäljningfakturan har skapats som avsett.

5. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda försäljningsfakturor** och väljer sedan relaterad länk.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Uppdatera statusen för förutbetalda order och fakturor automatiskt

Du kan påskynda bearbetningen av order och fakturor genom att lägga upp jobbkötransaktioner som automatiskt uppdaterar status för dessa dokument. När en förskotts faktura betalas kan jobbkötransaktionen automatiskt ändra dokument statusen från **Väntar på förskottsbetalning** till **släppt**. När du registrerar jobbkötransaktioner måste du använda de kodmoduler som är **383 Uppdatera väntande förskottsbetalning, försäljning** och **383 Uppdaterar väntande förskottsbetalning, inköp**. Vi rekommenderar att du schemalägger transaktionerna så att de körs ofta, till exempel varje minut. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="next-steps"></a>Gå vidare

Den här genomgången har gått igenom hur du konfigurerar [!INCLUDE[prod_short](includes/prod_short.md)] att hantera förskottsbetalningar. 

- Ställ in procentuella standardvärden för förskottsbetalningar för kunder och artiklar.
- Använd olika metoder för att beräkna förskottsbetalningar för en order.  
- Beräkna förskottsbetalningsbeloppet som en procentsats av summan på ordern.
- Tilldela ordern ett totalt förskottsbetalningsbelopp.  

Du har också bokfört en förskottsfaktura, skapat en andra förskottsfaktura när ordern har ändrats och bokfört slutfakturan för det återstående beloppet.  

Funktionerna för förskottsbetalning gör det enklare att lägga upp och använda förskottsbetalningsregler för kunder och artiklar. De ger dig också möjlighet att bokföra varje betalning mot en faktura.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Skapa förskottsfakturor
description: Hantera situationer där du eller din leverantör behöver förskottsbetalning. Använd standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 02/02/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices" />Skapa förskottsfakturor

Om du kräver att kunderna betalar innan du skickar deras beställning kan du använda förskottsbetalningsfunktionerna. Detsamma gäller om leverantören kräver att du betalar innan han/hon levererar en order till dig.  

När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura. Standard förskottsbetalningsprocent för en given artikel på beställningen, eller för kunden eller leverantören tas med i förskottsfakturan. Du kan också ange en procentandel för förskottsbetalning för hela dokumentet.

När du har skapat en försäljnings- eller inköpsorder kan du skapa en förskottsfaktura. Använd standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet. Du kan till exempel ange ett totalt belopp för hela ordern.  

I följande procedur beskrivs hur du fakturerar en förskottsbetalning för en försäljningsorder. Momenten är liknande för en inköpsorder.  

## <a name="to-create-a-prepayment-invoice" />Så här skapar du en förskottsfaktura

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Skapa en ny försäljningsorder för relevant kund. Mer information finns i [Sälja produkter](sales-how-sell-products.md).  

    På snabbfliken **Förskottsbetalning** i fältet **Förskottsbetalning %** anges den procentandel som ska användas för att beräkna förskottsbeloppet. Om det finns en standardprocentandel på kundkortet fylls fältet i automatiskt. Du kan ändra procentandelen. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Välj fältet **Komprimera förskottsbetalning** om du vill skapa rader på den förskottsfaktura som kombinerar rader från försäljningsordern om:  

    - De har samma redovisningskonto för förskottsbetalningar, enligt de allmänna bokföringsinställningarna.  
    - De har samma dimensioner.  

    Låt fältet vara tomt om du vill skapa en förskottsfaktura med en rad för varje försäljningsorderrad som det finns en procentandel för förskottsbetalning för, välj då inte fältet **Komprimera förskottsbetalning**.  

    Förfallodatumet för förskottsbetalningen beräknas automatiskt baserat på värdet i fältet **Betalningsvillkorskod för förskottsbetalning**.

    > [!NOTE]
    > När några rader på en faktura kräver 100 % förskottsbetalning och andra rader inte och det finns moms på kontot för förskottsbetalning, kan det avrundade beloppet orsaka ett fel när du skapar en förskottsfaktura. Felet beror på att förskottsfakturans belopp är högre än beloppen på dokumentraderna. Lös problemet genom att ändra beloppen på en eller alla rader som kräver förskottsbetalning på 100 %. Ändringen kommer att beräkna om det avrundade momsbeloppet och använda den ackumulerade avrundningsskillnaden på den senast ändrade raden.
    >
    > Ytterligare två sätt att åtgärda problemet är:
    >
    > * Skapa en separat bokföringsinställning för moms och en bokföringsinställning för moms med separat moms-ID och använda det för de artiklar eller rader som kräver 100 % förskottsbetalning. Avrundning görs för varje moms-ID, så en separat avrundning utförs för artiklar som är kopplade till bokföringsmallen för moms.
    > * Använd en separat faktura för artiklarna eller raderna som du vill och inte behöver 100 % förskottsbetalningar.

3. Fyll i försäljningsraderna.  

    Om du har angett en standard procentandel för förskottsbetalning för kunden eller på snabbfliken **förskottsbetalning** i det här dokumentet kopieras det här värdet till varje rad. Du kan ändra innehållet i fältet **Förskottsbetalning %** på raden.  

    > [!TIP]
    > Om du inte ser fältet **Förskottsbetalning %** kan du lägga till det med hjälp av anpassning.  Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

4. Visa det totala förskottsbeloppet genom att välja åtgärden **statistik**.

    Om du vill justera det totala förskottsbetalningsbeloppet för ordern kan du ändra innehållet i fältet **Förskottsbetalningsbelopp** på sidan **Förs.orderstatistik**.  

    Om fältet **Priser inkl. moms** är markerat, kan fältet **Förskottsbetalningsbelopp inkl moms** redigeras  

    Om du ändrar innehållet i fältet **Förskottsbetalningsbelopp** fördelas beloppet proportionellt på alla rader, förutom på de där värdet **0** i fältet **Förskottsbetalning %**.  

5. Du skriver ut en testrapport innan du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan välja åtgärden **Testrapport för förskottsbetalning**.  
6. Du bokför en förskottsfaktura genom att välja åtgärden **Förskottsbetalning** och sedan åtgärden **Bokför förskottsfaktura**.  

    Om du vill bokföra och skriva ut förskottsfakturan väljer du åtgärden **Bokför och skriv ut faktura på förskottsbet.**.  

Du kan skicka ut ytterligare förskottsfakturor för ordern. Om du vill utfärda en annan faktura höjer du förskottsbetalningsbeloppet på minst en rad, justerar dokumentdatumet om det behövs och bokför sedan förskottsfakturan. En ny faktura skapas för skillnaden mellan de förskottsbetalningsbelopp som hittills har fakturerats och det nya förskottsbetalningsbeloppet.  

> [!NOTE]  
> Om du befinner dig i Nordamerika kan ändra du inte procentandelen för förskottsbetalning när förskottsfakturan har bokförts. Detta förhindras i den amerikanska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] eftersom beräkning av moms på annat sätt blir felaktiga.  

 När du vill bokföra resten av fakturan bokför du den som en vanlig faktura. Förskottsbetalningsbeloppet dras automatiskt av från beloppet som ska betalas.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically" />Uppdatera statusen för förutbetalda order och fakturor automatiskt

Du kan påskynda bearbetningen av order och fakturor genom att lägga upp jobbkötransaktioner som automatiskt uppdaterar status för dessa dokument. När en förskotts faktura betalas kan jobbkötransaktionen automatiskt ändra dokument statusen från **Väntar på förskottsbetalning** till **släppt**. När du registrerar jobbkötransaktioner måste du använda de kodmoduler som är **383 Uppdatera väntande förskottsbetalning, försäljning** och **383 Uppdaterar väntande förskottsbetalning, inköp**. Vi rekommenderar att du schemalägger transaktionerna så att de körs ofta, till exempel varje minut. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="see-related-microsoft-trainingtrainingmodulesprepayment-invoices-dynamics--business-central" />Se relaterad [Microsoft utbildning](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Genomgång: Konfigurera och fakturera förskottsbetalning för försäljning](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Anpassa din arbetsyta](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Registrera inköp med inköpsfakturor (innehåller video)
description: 'Beskriver hur du köper lager, icke-lagerartiklar eller andra resurser genom att skapa och bokföra inköpsfakturor eller order.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="record-purchases-with-purchase-invoices-and-orders"></a>Registrera inköp med inköpsfakturor och order

Du skapar en inköpsfaktura eller inköpsorder för att registrera kostnaden för inköp och för att spåra leverantörsskulder. Inköpsfakturor eller inköpsorder också för att uppdatera lagernivåer dynamiskt, så att du kan minimera lagerkostnader och ge bättre service. Inköpskostnaderna, inklusive serviceutgifter, och lagervärde som kommer från bokföring av inköpsfakturor eller order bidrar till vinstsiffror och övriga ekonomiska KPI:er i rollcentret.

## <a name="record-purchases-with-purchase-invoices"></a>Registrera inköp med inköpsfakturor

När du tar emot lagerartiklarna, eller när den inköpta tjänsten avslutas, bokför du inköpsfakturan för att uppdatera lager och finansiella transaktioner, samt för att aktivera betalning till leverantören utifrån betalningsvillkoren. [Göra betalningar](payables-make-payments.md).

> [!CAUTION]  
> Bokför inte en inköpsfaktura för fysiska artiklar förrän du tar emot artiklarna och vet slutkostnaden för inköpet, inklusive eventuella extrakostnader. Annars kan lagervärdet och vinstsiffrorna ha oriktiga resultat.

### <a name="create-and-post-a-purchase-invoice"></a>Skapa och bokföra en inköpsfaktura

Följande steg beskriver hur du skapar en inköpsfaktura. Stegen för att skapa en inköpsorder är liknande. Den största skillnaden är att inköpsorder har några ytterligare fält och åtgärder för fysisk hantering av artiklar.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Ange namnet på en befintlig leverantör i fältet **Leverantörsnamn**.

    Andra fält på sidan **Inköpsfaktura** fylls nu i med standardinformation om den valda leverantören. Om leverantören inte är registrerad, gör så här:

    1. Ange namnet på en ny leverantör i fältet **leverantörsnamn**.
    2. Välj **ja** i dialogrutan om registrering av den nya leverantören.
    3. Mer information om hur du fyller i leverantörskortet finns i [Registrera nya leverantörer](purchasing-how-register-new-vendors.md).  
    4. Välj **OK** för att gå tillbaka till sidan **Inköpsfaktura**, när du har slutfört leverantörskortet.

3. På sidan **Inköpsfaktura** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Fortsätt nu med att fylla inköpsfakturaraderna med artiklar eller resurser som du har köpt från leverantören.

    > [!NOTE]  
    > Om du har ställt in återkommande inköpsrader för leverantöre, till exempel en månatlig återanskaffningsorder, kan du infoga dessa rader på fakturan, genom att välja knappen **Hämta återkommande inköpsrader**.
4. Ange numret på en lagerförd artikel eller service på snabbfliken **Rader** Snabbfliken, i **Artikelnr** fältet.
5. Ange hur många artiklar som ska införskaffas i fältet **Antal**.

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Inköpspris** multiplicerat med värdet i fältet **Kvantitet**.

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på leverantörskortet.

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

6. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms** längst ned på fakturan.

    > [!NOTE]  
    > Om du har ställt in fakturarabatter för leverantören, då infogas det angivna procentsatsvärdet automatiskt i fältet **Procentuell fakturarabatt för leverantör** om kriteriet uppfylls. Det relaterade beloppet infogas sedan i fältet **Fakturarabatt** .
7. Välj **Bokför** när du tar emot de beställda artiklarna eller tjänster.

Inköpet visas nu i lager, resurstransaktioner och ekonomiska transaktioner, och leverantörsbetalningen aktiveras. Inköpsfakturan tas bort från listan över inköpsfakturor och ersätts med ett nytt dokument i listan över bokförda inköpsfakturor.  Mer information om vad som händer när du bokför inköpsdokument finns i [ bokföra inköp](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.
>
> Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.

## <a name="posted-invoices"></a>Bokförda fakturor

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Det är enkelt att korrigera eller annullera en bokförd inköpsfaktura innan du betalar leverantören. Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen. Läs mer i [Korrigera eller makulera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). För att ångra ett köp av varor eller tjänster som anges på den bokförda inköpsfakturan som betalningen behandlas för måste du skapa en inköpskreditnota. Läs mer [Behandla inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

[Öppna listan **bokförda inköpsfakturor**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].


## <a name="purchasing-non-inventory-items"></a>Köpa artiklar som inte finns i lager

Raderna på en inköps faktura kan vara av typen **resurs** eller **artikel**. Artikelkort kan vidare klassificeras som av typen **Lager**, **Tjänst** eller **Inte i lager**, som anger om artikeln är en fysisk lagerenhet, en arbetstidsenhet (även tillämplig för resurser) eller en fysisk enhet som inte hålls i lager. Lär dig mer om att [Registrera nya artiklar](inventory-how-register-new-items.md). Inköpsfakturaprocessen är samma för alla nämnda typer.

> [!NOTE]
> Med inköpsradtypen **Resurs** kan du också köpa externa resurser, till exempel i syfte att fakturera en leverantör för utfört arbete. Läs mer i [Ställa in resurser](projects-how-setup-resources.md).
>
> Om du vill använda en inköpt resurs kan du komma att behöva ange resursens kapacitet och tilldela denna manuellt till ett projekt. När du köper en resurs skapas reskontratransaktion – reskontratransaktioner för resurs spåras emellertid inte för mängd och värde på samma sätt som för exempelvis artiklar. Om antals- och värdespårning krävs kan du använda andra radartikeltyper.

## <a name="when-to-use-purchase-orders"></a>När inköpsorder ska användas

Du måste använda inköpsorder om din inköpsprocess kräver att du t. ex. kan registrera delleveranser av en orderkvantitet eftersom hela kvantiteten inte var tillgänglig hos leverantören. Om du levererar sålda artiklar direkt från din leverantör till kunden, som en direktleverans, måste du även använda inköpsorder. Mer information finns i [skapa direktleveranser](sales-how-drop-shipment.md).

I alla andra aspekter fungerar inköpsorder på samma sätt som inköpsfakturor. Följande procedur är baserad på en inköpsfaktura. Momenten är liknande för en inköpsorder.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order"></a>Inleverera artiklar med en inköpsorder

Följande steg beskriver hur du inlevererar artiklar med en inköpsorder. 

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. Öppna en befintlig inköpsorder eller skapa en ny.
3. Ange hur många enheter som har inlevererats i fältet **Inlevereras antal**.

   > [!NOTE]
   > Om mottagen kvantitet överstiger den i inköpsordern, och om leverantören har godkänt överskridande inleveranser, kan du använda fältet **Överskr. inleverans** för att hantera överskottet. Mer information finns i avsnittet [Så här tar du emot fler artiklar än vad som beställts](purchasing-how-record-purchases.md#receive-more-items-than-ordered).
4. Välj åtgärden **Bokföra**.

  Värdet i fältet **Inlevererat antal** uppdateras i enlighet därmed. Om detta är en delinleverans och värdet är lägre än värdet i fältet **antal**.

> [!NOTE]
> Om du använder ett distributionslagerdokument kan du inte använda åtgärden **Bokföra** på inköpsordern för att bokföra inleveransen. Det beror på att en distributionslagerarbetare redan bokfört inköpsordermängden som inlevererad. Läs mer på [Designdetaljer – Inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-ordered"></a>Så här tar du emot fler artiklar än vad som beställts

När det kommer fler varor än vad som beställts vill du kanske ta emot dem i stället för att annullera inleveransen. Det kan t.ex. vara billigare att behålla överskottsartiklar på lagret än att returnera dem, eller så din leverantör erbjuda en rabatt för att behålla dem.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts"></a>Så här lägger du upp överinleveranser

Skapa koder för överinleverans för att definiera en procentsats med vilken en inlevererad kvantitet kan överskrida den beställda kvantiteten. Ange procentsatsen i fältet **Tolerans för överinleverans %**. Du kan sedan tilldela koden på sidorna artikelkort eller leverantörskort för artiklar och leverantörer.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Koder för överinleverans** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item"></a>Tilldela koden för överinleverans för en artikel

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Öppna **Artikelkort** för artikeln.
3. I fältet **överinleveranskod**, välj koden som innehåller den procentandel du vill tillåta för överinleveranser.

Koden för överinleverans tilldelas till artikeln. Inköpsorder eller distributionslagerinleverans för artikeln tillåter att du tar emot mer än det beställda antalet inom toleransprocenten för överinleverans.

> [!NOTE]
> Du kan ställa in ett arbetsflöde för godkännande för att kräva att överinleveranser måste godkännas innan de kan hanteras. Markera kryssrutan **Godkännande krävs** på sidan **Koder för överinleverans**. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).

### <a name="over-receive-an-order"></a>Överleverans av en order

På inköpsrader och distributionslagerrader används **Överinleveransmängd** för att registrera överlevererade kvantiteter, vilket innebär antal som överstiger värdet i fältet **Antal**, den beställda mängden.

När du hanterar ett överinleverans kan du antingen öka värdet i fältet **Ant. att inlevereras** till den faktiska inlevererade kvantiteten. Fältet **Överinleveranskvantitet** uppdateras för att visa överskjutande antal. Du kan också ange överskjutande antal i fältet **Överinleveranskvantitet**. Fältet **Ant. att inlevereras** uppdateras för att visa beställt antal plus överskjutande antal. Följande procedur beskriver hur du fyller i fältet **Ant. att inlevereras**.  

1. På en inköpsorder eller ett lagerinleveransdokument där inlevererad mängd överstiger den beställda anger du den faktiskt inlevererade mängden i fältet **Ant. att inlevereras**.

    Om ökningen ligger inom den tolerans som anges av den tilldelade koden för överinleverans uppdateras fältet **Överleveranskvantitet** för att visa det antal med vilket värdet i fältet **Antal** överskrids.

    Om ökningen överskrider toleransen är överinleverans inte tillåten. Undersök om en annan överinleveranskod tillåter det. Annars kan endast den beställda kvantiteten tas emot, och den överskjutande kvantiteten måste hanteras på annat sätt, till exempel genom att returnera den till leverantören.

2. Bokför inleveransen på samma sätt som andra inleveranser.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandlar inte ekonomiska aspekter av överinleveranser automatiskt. Du måste hantera detta manuellt i samråd med leverantören, till exempel genom att leverantören skickar en ny eller uppdaterad faktura.

## <a name="external-document-number"></a>Externt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases"></a>Bokföra inköp

I ett inköpsdokument kan du välja mellan följande bokföringsåtgärder:

* **Bokföra**
* **Förhandsgranska bokföring**
* **Bokför och skriv ut**
<!--* **Test Report**-->
* **Bokför batch-jobb**

När ett inköpdokument bokförs uppdateras leverantörens konto, redovisningen, artikeltransaktionstransaktionerna samt resurstransaktionstransaktionerna.

För respektive inköpsdokument skapas en inköpstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på leverantörens konto i tabellen **Lev.reskontratransaktion** och en redovisningstransaktion på det relevanta kontot för leverantörsskulder. Dessutom kan bokföring av inköpet resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Om rabattransaktionen är bokförd eller ej beror på innehållet i fältet **Rabattbokföring** på sidan **Inköpsinställningar**.

För varje inköpsrad, som tillämpligt, skapas poster i:

* Tabellen **Artikeltransaktion** om inköpsraden är av typen **Artikel**.
* Tabellen **Redovisningstransaktion** om inköpsraderna är av typen **Redovisningskonto**.
* Tabellen **Resurstransaktion** om inköpsraden är av typen **Resurs**.

Dessutom registreras inköpsdokument alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**.

Du kan alltid granska olika transaktioner som kommer att skapas i samband med bokföring. Välj **Förhandsgranska bokföring** för att validera dokument och granska förväntade transaktioner.


> [!IMPORTANT]  
> När du bokför en inköpsorder för artiklar kan du skapa både en inleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delinleverans och en delfaktura genom att fylla i fältet **Ant. att inlevereras** och **Ant. att fakturera** på de enskilda inköpsorderraderna innan du bokför. Observera att du inte kan skapa en inköpsfaktura från en inköpsorder för produkter eller tjänster som inte har tagits emot. Innan du kan fakturera måste du således ha registrerat en inleverans alternativt välja att inleverera och fakturera samtidigt.

Du kan bokföra eller bokföra och skriva ut. Om du väljer Bokför och Skriv ut, skrivs en rapport ut när ordern bokförs. Du kan även välja åtgärden **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Läs mer på [Bokföra flera dokument på samma gång](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visa reskontratransaktioner

När bokföringen är slutförd tas de bokförda inköpsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Du kan därefter se bokförda transaktioner på de sidor som innehåller bokförda transaktioner, inklusive sidorna **Lev.reskontratransaktioner**, **Redovisningstransaktioner**, **Artikeltransaktioner**, **resurstransaktioner**, **Inköpsleveranser** samt **Bokförda inköpsfakturor**.

I de flesta fall kan du öppna reskontratransaktioner från det berörda kortet eller dokumentet. Välj till exempel åtgärden **Transaktioner** på sidan **Leverantörskort**.

## <a name="editing-ledger-entries"></a>Redigera reskontratransaktioner

Du kan redigera vissa fält i bokförda inköpsdokument, till exempel fältet **Betalningsreferens**. Mer information finns i [Redigera bokförda dokument](across-edit-posted-document.md). För mer kritiska fält som påverkar granskningsspåret måste du återföra eller ångra bokföring. Läs mer på [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Se även

[Begära offerter](purchasing-how-request-quotes.md)  
[Köpa artiklar för en försäljning](purchasing-how-purchase-products-sale.md)  
[Förbereda direktutleveranser](sales-how-drop-shipment.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Konfigurera resurser](projects-how-setup-resources.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Bokföra flera dokument på samma gång](ui-batch-posting.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

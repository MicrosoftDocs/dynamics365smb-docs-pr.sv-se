---
title: Fakturaförsäljning
description: Beskriver hur du skapar en pantförskrivning eller försäljningsfaktura eller försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.search.form: 43, 48, 9301
ms.date: 09/01/2022
ms.author: edupont
ms.openlocfilehash: d9c62e76239880b65237319a809d251ae71e8bb7
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461190"
---
# <a name="invoice-sales"></a>Fakturaförsäljning

Du kan vanligtvis skapa antingen en försäljningsorder eller försäljningsfaktura för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.  

Du måste dock använda en försäljningsorder i stället för en försäljningsfaktura om du:  

* Du behöver skicka en del av en orderkvantitet, till exempel eftersom den fullständiga kvantiteten inte är tillgänglig.  
* Leverera produkter efter att du har bokfört motsvarande fakturor.
* Sälj artiklar som leverantören levererar direkt till kunden, kallat direktleverans. Mer information finns i [skapa direktleveranser](sales-how-drop-shipment.md).  

I alla andra situationer fungerar försäljningsorder och försäljningsfakturor på samma sätt. Mer information om hur du använder försäljningsorder finns i [Sälj produkter](sales-how-sell-products.md).

Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsfaktura när du instämmer om försäljningen. Se mer i [Gör försäljningsofferter](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Skapa försäljningsfakturor

Om kunden bestämmer sig att köpa kan du bokföra fakturan för att skapa relaterade kvantitet- och värdetransaktioner. När du bokför försäljningsfakturan, kan du också e-posta den som en PDF-bilaga. Du kan använda ifylld e-postbrödtext med en sammanfattning av fakturan och betalningsinformationen, till exempel en länk till PayPal. Läs mer på [Skicka dokument via e-post](ui-how-send-documents-email.md). När kunden sedan betalar fakturan, kan du registrera den betalningen på olika sätt, beroende på storlek och önskade arbetsflöden för din organisation. Läs mer i avsnittet [registrera betalningar](#registering-payments).  

Artikelkort kan vara av typen **Lager**, **Service**, eller **Inte i lager** för att ange om artikeln är en fysisk inventeringsenhet, en arbetstidsenhet eller en fysisk enhet som inte hålls i inventeringen. Lär dig mer om att [Registrera nya artiklar](inventory-how-register-new-items.md). Försäljningsfakturaprocessen är samma för alla tre artikeltyper.

Du kan fylla i kundfälten på försäljningsfakturan på ett av två sätt, beroende på om kunden redan har registrerats. Se steg 2 i följande procedur.

### <a name="to-create-a-sales-invoice"></a>Så här skapar du en försäljningsfaktura

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.  
2. Ange namnet på en befintlig kund i fältet **Kund**. Om kunden däremot är ny och därför inte registrerad, följer du dessa steg för att fylla i standard kundinformationen på sidan **försäljningsfaktura**.

    1. Ange namnet på en ny kund i fältet **Kundnamn**.
    2. Välj **ja** i dialogrutan om registrering av den nya kunden.
    3. Välj en mall det nya kundkortet ska baseras på sidan **Välj en mall för en ny kund** och välj sedan **OK**.
    4. Ett nytt kundkort visar information från den markerade kundmallen. Fyll i resterande fält. Lär dig mer om att [registrera nya kunder](sales-how-register-new-customers.md).  
    5. Välj **OK** för att gå tillbaka till sidan **Stäng**, när du har slutfört kundkortet.

   Flera fält i försäljningsfakturahuvudet är nu ifyllda med information som du har angett på det nya kundkortet.  
3. På sidan **Inkommande dokument** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Om du tillåter att kunden betalar direkt, till exempel via kontanter eller PayPal, fyll sedan i fältet **betalningssätt**. Betalningen registreras sedan när du bokför försäljningsfakturan som fakturerad. Om du väljer *kontant* registreras betalning på ett angivet motkonto.

    Du är nu klar att fylla i snabbfliken **Rad** med produkter som du säljer till kunden eller för en transaktion med den kund som du vill registrera en post i ett redovisningskonto.

4. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.
   * Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du återspegla det här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.
5. I fältet **Nr.** väljer du en post som ska bokföras enligt värdet i fältet **Typ**.

    Du lämnar fältet **Nr.** tomt i följande fall:

    * Om raden är avsedd för en kommentar. Skriv kommentaren i fältet **Beskrivning**.
    * Om raden är avsedd för en katalogartikel. Välj åtgärden **Markera katalogartiklar**. Mer information: [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

6. I fältet **Antal** anger du hur många enheter av produkt, kostnad eller transaktion som registreras på raden för kunden.  

    > [!NOTE]  
    > Om artikeln är av typen **Tjänst**, eller fältet **Typ** innehåller **Resurs**, är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden. Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md)

    Värdet i fältet **Radbelopp** beräknas som *enhetspris* × *antal*.  

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.  
7. Om du vill ge en rabatt kan du ange ett procenttal i fältet **radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.  

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på försäljningsraden automatiskt om de överenskomna prisvillkorna uppfylls. Läs mer på [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Upprepa moment 4 till 7 för varje produkt som du vill fakturera kunden för.

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

    > [!NOTE]
    > I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.<br /><br />Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.
9. I fältet **Fakturarabatt exkl. moms** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om rabattkriteriet uppfylls, och det relaterade beloppet infogas i fältet **Fakturarabatt exkl. moms**. Läs mer på [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

10. När försäljningsfakturaraderna slutförda väljer du åtgärden **Bokföra och skicka**.  

Dialogrutan **Bokför och skicka bekräftelse** visar kundens standardmetod för mottagning av dokument. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Läs mer: [Skapa dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

Relaterade artiklar och kundtransaktionerna skapas nu i systemet, och försäljningsfakturan matas ut som ett PDF-dokument. Försäljningsfakturan tas bort från listan över försäljningsfakturor och ersätts med ett nytt dokument i listan över bokförda försäljningsfakturor.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beräkna fakturarabatter på försäljning

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Bokförda fakturor

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Det är enkelt att korrigera eller annullera en bokförd försäljningsfaktura, innan den betalas. Det är användbart om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen. Läs mer i [Korrigera eller makulera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md). Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota för att återföra försäljningen. Läs mer [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).  

[Öppna listan **bokförda försäljningsfakturor**](https://businesscentral.dynamics.com/?page=143) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments"></a>Registrera betalningar

Beroende på ditt företagsbehov kan du få betalt och registrera den betalningen på olika sätt: manuellt, automatiskt eller via betalningstjänster.  

Du kan bearbeta betalningar direkt från kundkortet. Använd åtgärden **registrera kundbetalningar** för att få en översikt över obetalda fakturor för den kunden. Markera sedan fakturan som betald delvis eller helt. Denna betalningsavstämning behandlar dina kundbetalningar genom att matcha mottagna belopp på ditt bankkonto med relaterade obetalade försäljningsfakturor och sedan bokföra betalningarna. Mer information finns i avsnitt [Så här stämmer du av betalningar individuellt](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

I företagsmiljöer där kunden betalar en tid efter leveransdatum enligt betalningsvillkor, en bokförd försäljningsfaktura förblir öppen (obetalda) till Kundreskontraavdelningen verifierar att betalning tagits emot och gäller betalningen för den bokförda försäljningsfaktura. Detta kan göras manuellt eller automatiskt. Mer information finns i [Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner](receivables-how-apply-sales-transactions-manually.md) och [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).  

I företagsmiljöer där kunden betalar direkt, till exempel genom PayPal eller kontanter, betalningen bokförs direkt när du bokför försäljningsfakturan, d.v.s. stängs den bokförda försäljningsfakturan som i sin helhet. Du väljer relevant metod i fältet **Kod för betalningsmetod** på försäljningsordern. För elektroniska betalningar såsom PayPal, måste du även fylla i fältet **betalningstjänst**. Läs mer på [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).

Du kan även skapa direktbetalade fakturor för icke-registrerade kunder genom att definiera ett ”kontant” kundkort som du refererar till på försäljningsfakturan. Läs mer i [Så här skapar du Kontantkunder](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Om du vill skicka påminnelser om förfallna betalningar måste du först ange nivåer och villkor för betalningspåminnelser. Läs mer i [Konfigurera påminnelsevillkor och nivåer](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Externa dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index).

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skriv ut plocklistan](sales-how-print-picking-list.md)  
[Lager](inventory-manage-inventory.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Kräva in utestående saldon](receivables-collect-outstanding-balances.md)  
[Bulkfakturering från Microsoft Bookings i Business Central ](finance-bookings.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

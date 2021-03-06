---
title: Fakturaförsäljning
description: Beskriver hur du skapar en pantförskrivning eller försäljningsfaktura eller försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d0a48037123dee4a7c9282432cc2b357b335e794
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115571"
---
# <a name="invoice-sales"></a>Fakturaförsäljning

Du kan skapa en försäljningsfaktura eller försäljningsorder för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.  

Det finns två situationer där du måste använda en försäljningsorder i stället för en faktura:  

* Om du behöver skicka en del av en orderkvantitet, till exempel eftersom den fullständiga kvantiteten inte är tillgänglig.  
* Om du levererar produkter efter att du har bokfört motsvarande fakturor.
* Om du säljer artiklar som leverantören levererar direkt till kunden, kallat direktleverans. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md).  

I alla andra aspekter fungerar försäljningsorder och försäljningsfakturor på samma sätt. Mer information finns i [Sälja produkter](sales-how-sell-products.md).

Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsfaktura när du instämmer om försäljningen. Mer information finns i [Gör försäljningsoffert](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Skapa försäljningsfakturor

Om kunden bestämmer sig att köpa kan du bokföra fakturan för att skapa relaterade kvantitet- och värdetransaktioner. När du bokför försäljningsfakturan, kan du också e-posta dokument som en PDF-bilaga. Du kan använda ifylld e-postbrödtext med en sammanfattning av fakturan och betalningsinformationen, till exempel en länk till PayPal. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md). När kunden sedan betalar fakturan, kan du registrera den betalningen på olika sätt, beroende på storlek och önskade arbetsflöden för din organisation. Mer information finns i avsnittet [registrera betalningar](#registering-payments).  

Artikelkortet kan vara av typen **Lager**, **Service**, eller **Inte i lager** för att ange om artikeln är en fysisk inventeringsenhet, en arbetstidsenhet eller en fysisk enhet som inte hålls i inventeringen. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md). Försäljningsfakturaprocessen är samma för alla tre artikeltyper.

Du kan fylla i kundfälten på försäljningsfakturan på två sätt, beroende på om kunden redan har registrerats. Se steg 2 i följande procedur.

### <a name="to-create-a-sales-invoice"></a>Så här skapar du en försäljningsfaktura

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Försäljningsfakturor** och välj sedan relaterad länk.  
2. Ange namnet på en befintlig kund i fältet **Kund**.

   Andra fält på sidan **Försäljningsfaktura** innehåller standardinformation om den valda kunden. Om kunden inte är registrerad, gör så här:

    1. Ange namnet på en ny kund i fältet **Kund**.
    2. Välj knappen **ja** i dialogrutan om registrering av den nya kunden.
    3. Välj en mall det nya kundkortet ska baseras på sidan **Välj en mall för en ny kund** och välj sedan knappen **OK**.
    4. Ett nytt kundkort visar information från den markerade kundmallen. Fyll i resterande fält. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).  
    5. Välj **OK** för att gå tillbaka till sidan **Förs.faktura**, när du har slutfört kundkortet.

   Flera fält i försäljningsfakturahuvudet är nu ifyllda med information som du har angett på det nya kundkortet.  
3. På sidan **Inkommande dokument** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Om du tillåter att kunden betalar direkt, till exempel via kontanter eller PayPal, fyll sedan i fältet **betalningssätt**. Betalningen registreras sedan när du bokför försäljningsfakturan som fakturerad. Om du väljer kontant registreras betalning på ett angivet motkonto.

    Du är nu klar att fylla i försäljningsfakturaraderna för produkter som du säljer till kunden eller för en transaktion med den kund som du vill registrera en post i ett redovisningskonto.  

    Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.  
4. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.
5. I fältet **Nr.** väljer du en post som ska bokföras enligt värdet i fältet **Typ**.

    Du lämnar fältet **Nr.** tomt i följande fall:

    * Om raden är avsedd för en kommentar. Skriv kommentaren i fältet **Beskrivning**.
    * Om raden är avsedd för en katalogartikel. Välj åtgärden **Markera katalogartiklar**. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

6. I fältet **Antal** anger du hur många enheter av produkt, kostnad eller transaktion som registreras på raden för kunden.  

    > [!NOTE]  
    > Om artikeln är av typen **Tjänst**, eller fältet **Typ** innehåller **Resurs**, är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden. Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md).

    Värdet i fältet **Radbelopp** beräknas som *enhetspris* x *antal*.  

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.  
7. Om du vill ge en rabatt kan du ange ett procenttal i fältet **radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.  

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på försäljningsraden automatiskt om de överenskomna prisvillkorna uppfylls. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Upprepa moment 9 till 12 för varje produkt som du vill fakturera kunden för.  

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

    > [!NOTE]
    > I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.<br /><br />Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.
9. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).  
10. När försäljningsfakturaraderna slutförda väljer du åtgärden **Bokföra och skicka**.  

Dialogrutan **Bokför och skicka bekräftelse** visar kundens standardmetod för mottagning av dokument. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

Relaterade artiklar och kundtransaktionerna skapas nu i systemet, och försäljningsfakturan matas ut som ett PDF-dokument. Försäljningsfakturan tas bort från listan över försäljningsfakturor och ersätts med ett nytt dokument i listan över bokförda försäljningsfakturor.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beräkna fakturarabatter på försäljning

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Bokförda fakturor

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Det är enkelt att korrigera eller annullera en bokförd försäljningsfaktura, innan den betalas. Det är användbart om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen. Mer information finns i [Så här kan du korrigera eller annullera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md). Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota för att återföra försäljningen. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).  

[Öppna listan **bokförda försäljningsfakturor**](https://businesscentral.dynamics.com/?page=143) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments"></a>Registrera betalningar

Beroende på ditt företagsbehov kan du få betalt och registrera den betalningen på olika sätt: manuellt, automatiskt eller via betalningstjänster.  

Du kan bearbeta betalningar direkt från kundkortet. Använd åtgärden **registrera kundbetalningar** för att få en översikt över obetalda fakturor för den kunden. Markera sedan fakturan som betald delvis eller helt. Denna betalningsavstämning behandlar dina kundbetalningar genom att matcha mottagna belopp på ditt bankkonto med relaterade obetalade försäljningsfakturor och sedan bokföra betalningarna. Mer information finns i [Så här stämmer du av betalningar individuellt](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

I företagsmiljöer där kunden betalar en tid efter leveransdatum enligt betalningsvillkor, en bokförd försäljningsfaktura förblir öppen (obetalda) till Kundreskontraavdelningen verifierar att betalning tagits emot och gäller betalningen för den bokförda försäljningsfaktura. Detta kan göras manuellt eller automatiskt. Mer information finns i [Stäm av kundbetalningar med inbetalningsjournalen eller från kundreskontratransaktioner](receivables-how-apply-sales-transactions-manually.md) och [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).  

I företagsmiljöer där kunden betalar direkt, till exempel genom PayPal eller kontanter, betalningen bokförs direkt när du bokför försäljningsfakturan, d.v.s. stängs den bokförda försäljningsfakturan som i sin helhet. Du väljer relevant metod i fältet **Kod för betalningsmetod** på försäljningsordern. Se under steg 8. För elektroniska betalningar såsom PayPal, måste du även fylla i fältet **betalningstjänst**. Mer information finns i [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).  

Du kan även skapa direktbetalade fakturor för icke-registrerade kunder genom att definiera ett ”kontant” kundkort som du refererar till på försäljningsfakturan. Mer information finns i [Skapa kontantkunder](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Om du vill skicka påminnelser om förfallna betalningar måste du ange nivåer och villkor för betalningspåminnelser. Mer information finns i [Ange villkor och nivåer för påminnelser](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Externa dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index)

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
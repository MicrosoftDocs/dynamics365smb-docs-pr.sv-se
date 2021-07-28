---
title: Skapa en försäljningsorder och sälja produkter | Microsoft Docs
description: Beskriver hur du skapar en försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 67d7ad0d10ddc5c6065df482c7ceb4b98058d504
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436732"
---
# <a name="sell-products"></a>Sälja produkter

Du kan skapa en försäljningsorder eller försäljningsfaktura för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.

> [!NOTE]  
> Använd försäljningsorder om din försäljningsprocess kräver att du t. ex. kan leverera delar av en orderkvantitet eftersom hela kvantiteten inte är tillgängliga på en gång. Om du använder försäljningsfakturor [!INCLUDE [prod_short](includes/prod_short.md)] förutsätts det att du levererar hela kvantiteten när du bokför fakturan. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda försäljningsorder. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar försäljningsorder på samma sätt som försäljningsfakturor. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).

Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsorder när du instämmer om försäljningen. Mer information finns i [Gör försäljningsoffert](sales-how-make-offers.md).

När kunden har bekräftat avtalet, till exempel efter en offertprocess, skickar du en orderbekräftelse för att registrera dina åtagande att leverera produkterna enligt överenskomment.

När du har levererat produkterna, antingen helt eller delvis, bokför du försäljningsordern som levererade eller som levererade och fakturerade för att skapa kundreskontratransaktioner i systemet. När du bokför försäljningsorder, kan du också e-posta dokument som en PDF-bilaga. Du kan använda ifylld e-postbrödtext med en sammanfattning av ordern och betalningsinformationen, till exempel en länk till PayPal. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).

I företagsmiljöer där kunden betalar en tid efter leveransdatum enligt betalningsvillkor, en bokförd försäljningsfaktura förblir öppen (obetalda) till Kundreskontraavdelningen verifierar att betalning tagits emot och gäller betalningen för den bokförda försäljningsfaktura. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

I företagsmiljöer där kunden betalar direkt, till exempel genom PayPal eller kontanter, betalningen bokförs direkt när du bokför försäljningsordern som fakturerad, d.v.s. stängs den bokförda försäljningsfakturan som i sin helhet. Du väljer relevant metod i fältet **Kod för betalningsmetod** på försäljningsordern. Se under steg 8. För elektroniska betalningar såsom PayPal, måste du även fylla i fältet **betalningstjänst**. Mer information finns i [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).

Du kan även skapa direktbetalade order för icke-registrerade kunder genom att definiera ett ”kontant” kundkort som du refererar till på försäljningsorder. Mer information finns i [Skapa kontantkunder](finance-how-to-set-up-cash-customers.md).

Det är enkelt att rätta eller avbryta en bokförd försäljningsfaktura som härrör från en försäljningsorder, innan den har betalas. Det är användbart om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen. Mer information finns i [Så här kan du korrigera eller annullera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md). Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota för att återföra försäljningen. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).

Artikelkortet kan vara av typen **Lager**, **Service**, eller **Inte i lager** för att ange om artikeln är en fysisk inventeringsenhet, en arbetstidsenhet eller en fysisk enhet som inte hålls i inventeringen. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md). Försäljningsorderprocessen är samma för alla tre artikeltyper.

Du kan fylla i kundfälten på försäljningsorder på två sätt, beroende på om kunden redan har registrerats. Se steg 2 i följande procedur.

## <a name="to-create-a-sales-order"></a>Så här skapar du försäljningsorder

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Ange namnet på en befintlig kund i fältet **Kund**.

    Andra fält på sidan **Försäljningsorder** fylls nu i med standardinformation om den valda kunden.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]  

    Flera fält i Försäljningsorder är nu ifyllda med information som du har angett på det nya kundkortet.
3. På sidan **Förs.order** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Om du tillåter att kunden betalar direkt, till exempel via kreditkort eller PayPal, fyll sedan i fältet **betalningssätt**. Betalningen registreras sedan när du bokför försäljningsordern som fakturerad. Om du väljer kontant registreras betalning på ett angivet motkonto.

    Du är nu redo att fylla i Försäljningsorderraderna med lagerförda artiklar eller tjänster som du vill sälja till kunden.

    Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.
4. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.

5. I fältet **Nr.** anger du ett nummer för en lagerartikel eller tjänst.

    Du lämnar fältet **Nr.** tomt i följande fall:

    * Om raden är avsedd för en kommentar. Skriv kommentaren i fältet **Beskrivning**.
    * Om raden är avsedd för en katalogartikel. Välj åtgärden **Markera katalogartiklar**. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).
6. Skriv det antal artiklar som ska säljas i fältet **Kvantitet**.

    > [!NOTE]  
    > För artiklar av typen *Resurs* eller *Tjänst* är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden. Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md).

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Enhetspris** multiplicerat med värdet i fältet **Kvantitet**.

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.
7. Ange ett värde i procent, om du vill bevilja kunden en rabatt på produkten i fältet **Radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på offertraden automatiskt om de överenskomna prisvillkorna uppfylls. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).
8. Ange en text i fältet **Beskrivning** på en tom rad för att lägga till en kommentar om offertraden som kunden kan se på den utskrivna offerten.  
9. Upprepa moment 4 till 8 för varje artikel som du vill att sälja till kunden.

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

    > [!NOTE]
    > I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.
    >
    > Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.  

10. I fältet **Fakturarabatt** anger du (valfritt) ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).
11. Att enbart leverera en del av orderkvantiteten , anger denna kvantitet i **Ant. att utleverera**. Värdet kopieras till **Ant. att fakturera**.
12. För att enbart fakturera en del av den levererade kvantiteten , anger du denna kvantitet i **Ant. att fakturera**. Antalet kan inte vara högre än värdet i fältet **Ant. att utleverera**.  
13. När försäljningsorderraderna slutförda väljer du åtgärden **Bokföra och skicka**.

Dialogrutan **Bokför och skicka bekräftelse** visar kundens standardmetod för mottagning av dokument. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

Relaterade artiklar och kundtransaktionerna skapas nu i systemet, och försäljningsorder matas ut som ett PDF-dokument. När försäljningsordern bokförs helt tas den bort från listan över försäljningsorder och ersätts med nya dokument i listan över bokförda försäljningsfakturor och listan över bokförda försäljningsleveranser.  

## <a name="external-document-number"></a>Externt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skriv ut plocklistan](sales-how-print-picking-list.md)  
[Lager](inventory-manage-inventory.md)  
[Skicka dokument som e-transaktion](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
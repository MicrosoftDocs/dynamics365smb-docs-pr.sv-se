---
title: Skapa en kundförsäljningsreturorder och sälja produkter
description: Beskriver hur du skapar en försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, partial deliveries, customer sales order
ms.date: 09/24/2021
ms.author: edupont
ms.openlocfilehash: 7156684c2b12af7e5b3e8b51791a702566824009
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588507"
---
# <a name="sell-products-with-a-customer-sales-order"></a>Sälja produkter med en kundförsäljningsreturorder  

Artikeln ger vägledning till användare om när de ska använda kundförsäljningsorder i stället för bara faktura. Du kan använda försäljningsorder om din försäljningsprocess gör att du bara kan leverera delar av en orderkvantitet, exempelvis om hela kvantiteten inte är tillgänglig samtidigt.  

Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda försäljningsorder. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar försäljningsorder på samma sätt som försäljningsfakturor. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).

När du har levererat produkterna, antingen helt eller delvis, bokför du försäljningsordern som levererade eller som levererade och fakturerade för att skapa kundreskontratransaktioner i systemet. När du bokför försäljningsorder, kan du också e-posta dokument som en PDF-bilaga. Du kan använda ifylld e-postbrödtext med en sammanfattning av ordern och betalningsinformationen, till exempel en länk till PayPal. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).

I företagsmiljöer där kunden betalar direkt, till exempel genom PayPal eller kontanter, betalningen bokförs direkt när du bokför försäljningsordern som fakturerad, d.v.s. stängs den bokförda försäljningsfakturan som i sin helhet. Du väljer relevant metod i fältet **Kod för betalningsmetod** på försäljningsordern. Se under steg 8. För elektroniska betalningar såsom PayPal, måste du även fylla i fältet **betalningstjänst**. Mer information finns i [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).

Du kan även skapa direktbetalade order för icke-registrerade kunder genom att definiera ett ”kontant” kundkort som du refererar till på försäljningsorder. Mer information finns i [Skapa kontantkunder](finance-how-to-set-up-cash-customers.md).

## <a name="to-create-a-sales-order"></a>Så här skapar du försäljningsorder

> [!NOTE]  
> Följande procedur förutsätter att kunden redan har ställts in. Instruktioner om hur du gör det finns i [Registrera nya kunder](sales-how-register-new-customers.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Skapa en ny post genom att välja **Ny**.
3. Ange namnet på en befintlig kund i fältet **Kund**.

    Andra fält på sidan **Försäljningsorder** fylls nu i med standardinformation om den valda kunden.  

4. På sidan **Förs.order** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Om du tillåter att kunden betalar direkt, till exempel via kreditkort eller PayPal, fyll sedan i fältet **betalningssätt**. Betalningen registreras sedan när du bokför försäljningsordern som fakturerad. Om du väljer kontant registreras betalning på ett angivet motkonto.

    Du är nu redo att fylla i Försäljningsorderraderna med lagerförda artiklar eller tjänster som du vill sälja till kunden.

    Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.
5. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.

6. I fältet **Nr.** anger du ett nummer för en lagerartikel eller tjänst.

    Du lämnar fältet **Nr.** tomt i följande fall:

    * Om raden är avsedd för en kommentar. Skriv kommentaren i fältet **Beskrivning**.
    * Om raden är avsedd för en katalogartikel. Välj åtgärden **Markera katalogartiklar**. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).
7. Skriv det antal artiklar som ska säljas i fältet **Kvantitet**.

    > [!NOTE]  
    > För artiklar av typen *Resurs* eller *Tjänst* är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden. Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md).

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Enhetspris** multiplicerat med värdet i fältet **Kvantitet**.

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.
8. Ange ett värde i procent, om du vill bevilja kunden en rabatt på produkten i fältet **Radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på offertraden automatiskt om de överenskomna prisvillkorna uppfylls. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).
9. Gör en kommentar i fältet **Beskrivning** på en orderrad för att lägga till en kommentar om försäljningsorder som kunden kan se på den utskrivna offerten.  
10. Upprepa moment 5 till 9 för varje artikel som du vill att sälja till kunden.

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

    > [!NOTE]
    > I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.
    >
    > Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.  

11. I fältet **Fakturarabatt** anger du (valfritt) ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).
12. Att enbart leverera en del av orderkvantiteten , anger denna kvantitet i **Ant. att utleverera**. Värdet kopieras till **Ant. att fakturera**.
13. För att enbart fakturera en del av den levererade kvantiteten , anger du denna kvantitet i **Ant. att fakturera**. Antalet kan inte vara högre än värdet i fältet **Ant. att utleverera**.  
14. När försäljningsorderraderna slutförda väljer du åtgärden **Bokföra och skicka**.

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
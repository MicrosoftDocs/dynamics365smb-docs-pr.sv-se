---
title: Skapa en kundförsäljningsreturorder och sälja produkter
description: Beskriver hur du skapar en försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 09/02/2022
ms.author: edupont
---
# <a name="sell-products-with-a-customer-sales-order" />Sälja produkter med en kundförsäljningsreturorder

Artikeln ger vägledning till användare om du bör använda en kundorder utöver en faktura. Om din försäljningsprocess kräver att du bara skickar en del av en order, kanske för att hela kvantiteten inte är tillgänglig direkt, måste du bearbeta den försäljningen genom att göra en försäljningsorder.

Du måste också använda försäljningsorder om du säljer varor som levererar direkt från din leverantör till din kund, i det som kallas direktutleverans. Mer information finns i [skapa direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar försäljningsorder på samma sätt som försäljningsfakturor. Läs mer på [fakturaförsäljning](sales-how-invoice-sales.md).

När du har levererat produkterna, antingen helt eller delvis, bokför du försäljningsordern som levererade eller som levererade och fakturerade för att skapa kundreskontratransaktioner i systemet. När du bokför försäljningsorder, kan du också e-posta den som en PDF-bilaga. Du kan förifylla e-postbrödtext med en sammanfattning av ordern och betalningsinformationen, till exempel en länk till PayPal. Läs mer på [Leverera artiklar](warehouse-how-ship-items.md) och [Skicka dokument via e-post](ui-how-send-documents-email.md).

I företagsmiljöer där kunden betalar direkt, till exempel genom PayPal eller kontanter, betalningen bokförs direkt när du bokför försäljningsordern som fakturerad, d.v.s. stängs den bokförda försäljningsfakturan som i sin helhet. Du väljer relevant metod i fältet **Kod för betalningsmetod** på försäljningsordern. Se punkt 5 nedan. För elektroniska betalningar såsom PayPal, måste du även fylla i fältet **betalningstjänst**. Läs mer på [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).

Du kan även skapa direktbetalade order för icke-registrerade kunder genom att definiera ett ”kontant” kundkort som du refererar till på försäljningsorder. Läs mer i [Så här skapar du Kontantkunder](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order" />Skapa en försäljningsorder

> [!NOTE]  
> Följande procedur förutsätter att kunden redan har ställts in. Instruktioner om hur du gör det finns i [Registrera nya kunder](sales-how-register-new-customers.md).

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Skapa en ny post genom att välja **Ny**.
3. Ange namnet på en befintlig kund i fältet **Kund**.

    Andra fält på sidan **Försäljningsorder** fylls nu i med standardinformation om den valda kunden.  

4. På sidan **Förs.order** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Om du tillåter att kunden betalar direkt, till exempel via kreditkort eller PayPal, fyll sedan i fältet **betalningssätt**. Betalningen registreras sedan när du bokför försäljningsordern som fakturerad. Om du väljer *kontant* registreras betalning på ett angivet motkonto.

    Du är nu redo att fylla i Försäljningsorderraderna med lagerförda artiklar eller tjänster som du vill att kunden ska köpa.

    Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.
5. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.

6. I fältet **Nr.** anger du ett nummer för en lagerartikel eller tjänst.

    Du lämnar fältet **Nr.** är tomt om raden är för en:

    * Kommentera. Skriv kommentaren i fältet **Beskrivning**.
    * Katalogartikel. Välj åtgärden **Markera katalogartiklar**. Mer information: [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).
7. Skriv det antal artiklar som ska säljas i fältet **Kvantitet**.

    > [!NOTE]  
    > För artiklar av typen *Resurs* eller *Tjänst* är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden. Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md).

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Enhetspris** multiplicerat med talet fältet **Kvantitet**.

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.
8. Ange ett värde i procent, om du vill bevilja kunden en rabatt på produkten i fältet **Radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på offertraden automatiskt om de överenskomna prisvillkorna uppfylls. Läs mer på [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).
9. För att lägga till en kommentar om orderraden som kunden kan se på den utskrivna försäljningsordern, skriv en kommentar på en tom rad i fältet **Beskrivning**.  
10. Upprepa moment 5 till 9 för varje artikel du vill att kunden ska köpa.

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

    > [!NOTE]
    > I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.
    >
    > Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.  

11. I fältet **Fakturarabatt** anger du (valfritt) ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Läs mer på [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).
12. Att enbart leverera en del av orderkvantiteten , anger denna kvantitet i **Ant. att utleverera**. Värdet kopieras automatiskt till **Ant. att fakturera**.

    > [!NOTE]
    > Om fältet **Leveransråd** anges som **Slutfört** i snabbfliken **Leverans och fakturering** kan du inte bokföra del leveranser. Ta reda på mer på [Behandla delleveranser](sales-how-send-partial-shipments.md).
13. För att enbart fakturera en del av den levererade kvantiteten , anger du denna kvantitet i **Ant. att fakturera**. Antalet kan inte vara högre än värdet i fältet **Ant. att utleverera**.  
14. När försäljningsorderraderna slutförda väljer du åtgärden **Bokföra och skicka**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Dialogrutan **Bokför och skicka bekräftelse** visar kundens standardmetod för mottagning av dokument. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Läs mer: [Skapa dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

Relaterade artiklar och kundtransaktionerna skapas nu i systemet, och försäljningsorder matas ut som ett PDF-dokument. När försäljningsordern bokförs helt tas den bort från listan över försäljningsorder och ersätts med nya dokument i listan över bokförda försäljningsfakturor och listan över bokförda försäljningsleveranser.  

## <a name="external-document-number" />Externt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-trainingtrainingmodulescreate-sales-documents-dynamics--business-central" />Se relaterad [Microsoft utbildning](/training/modules/create-sales-documents-dynamics-365-business-central/).

## <a name="see-also" />Se även

[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Bokföra försäljning](ui-post-sales.md)  
[Leverera artiklar](warehouse-how-ship-items.md)  
[Skapa direktleveranser](sales-how-drop-shipment.md)  
[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skriv ut plocklistan](sales-how-print-picking-list.md)  
[Bearbeta delleveranser](sales-how-send-partial-shipments.md)  
[Lager](inventory-manage-inventory.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

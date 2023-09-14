---
title: Gör försäljningsofferter
description: Läs om hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden eller potentiell kund att sälja produkter under vissa villkor.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: bholtorf
---
# Gör försäljningsofferter

Du kan skapa en försäljningsoffert för att erbjuda en kund eller potentiell kund att sälja vissa produkter till vissa leverans- och betalningsvillkor. Du kan skicka försäljningsofferten till kunden för att meddela erbjudandet. Du kan e-posta dokument som en PDF-bilaga. Du kan också välja e-postbrödtexten förifylld med en sammanfattning av offerten. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).

Medan du förhandlar med kunden eller potentiell kund kan du ändra och skicka försäljningsofferten så mycket som behövs. När kunden accepterar offerten omvandlar du försäljningsofferten till en försäljningsfaktura eller försäljningsorder som du bearbetar försäljningen. Mer information finns i [Fakturera försäljning](sales-how-invoice-sales.md) eller [Sälja produkter](sales-how-sell-products.md).

I de flesta fall skickar du försäljningsoffert till potentiella kunder. Du har ofta en kontaktperson som du har förhandlat med. Om de accepterar erbjudandet slår du in försäljningsofferten i en order och registrerar den potentiella kunden som en kund i [!INCLUDE [prod_short](includes/prod_short.md)]. I följande procedur fokuserar vi på kontakter, men du kan också skicka offerter till befintliga kunder.  

## Så här skapar du en försäljningsoffert

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsofferter** och väljer sedan relaterad länk.
2. Ange den kontakt eller kund som du vill skicka försäljningsofferten till.

    - Om försäljningsofferten gäller en befintlig kontakt anger du namnet i fältet **Kontaktnr.** .  

        Om försäljningsofferten gäller en befintlig kund anger du kunden i fältet **kund**.
    - Om kontakten inte är registrerad, gör så här:

        1. I fältet **Kontaktnr.** välj sedan knappen Redigera :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. I dialogrutan där du väljer kontakten väljer du den **nya** åtgärden och fyller sedan i relevanta fält. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Mer information finns i [Skapa kontakter](marketing-create-contact-companies.md).  
        3. När du är klar med kontaktkortet markerar du den nyskapade kontakten i listan över kontakter och klickar sedan på OK för att gå tillbaka till förs. offerten.

        Flera fält i Försäljningsofferten är nu ifyllda med information som du har angett på det nya kontaktkortet.

        > [!NOTE]
        > Om du vill beräkna skatter och priser för en offert korrekt måste du välja den relevanta kundmallen i fältet **Kod för kundmall**. Mallen kommer att användas för att konvertera kontakten till en kund när offerten har konverterats till en försäljningsorder eller faktura.
    -  Om offerten är för en ny kund måste du lägga till kunden. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).  

3. På sidan **Förs.offert** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du är nu klar att fylla i försäljningsraderna för produkter som du säljer för en transaktion med den kund eller den potentiella kund som du vill registrera en post i ett redovisningskonto.  

    Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.  

4. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.
5. I fältet **Nr.** väljer du en post som ska bokföras enligt värdet i fältet **Typ**.

    Du lämnar fältet **Nr.** tomt i följande fall:
    - Om raden är avsedd för en kommentar. Skriv kommentaren i fältet **Beskrivning**.
    - Om raden är avsedd för en katalogartikel. Välj åtgärden **Markera katalogartiklar**. Mer information finns i [Arbeta med katalogartiklar](inventory-how-work-nonstock-items.md).

6. I fältet **Antal** anger du hur många enheter av produkt, kostnad eller transaktion som registreras på raden för kunden.

    > [!NOTE]  
    >  Om artikeln är av typen **Tjänst**, eller fältet **Typ** innehåller **Resurs**, är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden. Mer information finns i [Ställa in måttenheter](inventory-how-setup-units-of-measure.md).

    Värdet i fältet **Radbelopp** beräknas som *enhetspris* x *antal*.  

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.  
7. Om du vill ge en rabatt kan du ange ett procenttal i fältet **radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.  

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på försäljningsraden automatiskt om de överenskomna prisvillkorna uppfylls. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Upprepa moment 4 till 7 för varje produkt som du vill att erbjuda kontakten.

    Summorna under raderna beräknas automatiskt när du skapar eller ändrar rader.  
9. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > För att fylla i **Offertens giltighetsdatum** fylls i automatiskt med ett visst antal dagar efter att offerten har skapats, kan du fylla i **Beräkning av offertens giltighet** på sidan **Försäljning & kundreskontra**.

10. När försäljningsoffertraderna slutförda väljer du åtgärden **Skicka med e-post**.
11. På sidan **Skicka e-post** fyller du i återstående fält och granskar den inbäddade försäljningsofferten. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).
12. Om kontakten accepterar offerten väljer du åtgärden **skapa order**.  

    Alternativt kan du välja åtgärden **Gör faktura** om din organisation föredrar den processen.  
    > [!NOTE]
    > Om du har lagt till en kund i steg 2 ombeds du bekräfta konverteringen av offerten till en order.  
    >
    > Om du har lagt till en kontakt från en potentiell kund i steg 2 ombeds du utföra följande steg:
    >
    >  - Konvertera kontakten eller det potentiella kunden till en kund genom att välja någon av konverteringsmall för kontakt. Mer information finns i [Att skapa en kund, leverantör, anställd eller bankkonto från en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Bekräfta konverteringen av offerten till en order.

Konverteringen tar bort försäljningsofferten från databasen. En försäljningsfaktura eller försäljningsorder har skapats baserat på informationen i försäljningsofferten där du kan bearbeta försäljningen. I fältet **Offertnr** på försäljningsfakturan eller försäljningsordern kan du ange numret på försäljningsofferten som den har skapats från. Mer information finns i [Fakturera försäljning](sales-how-invoice-sales.md) eller [Sälja produkter](sales-how-sell-products.md).  

## Externt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## Se relaterad [Microsoft utbildning](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Arkivera dokument](across-how-to-archive-documents.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Skapa ett försäljningserbjudande till en kund
description: Beskriver hur du skapar ett försäljningserbjudande eller begäran om förslag (Offertförfrågan) för att registrera ditt erbjudande till kunden att sälja produkter under vissa villkor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: a538b7099521b10227bf5aeaefad0a9c60971068
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115546"
---
# <a name="make-sales-quotes"></a>Gör försäljningsofferter

Du kan skapa en försäljningsoffert för att erbjuda en kund att sälja vissa produkter till vissa leverans- och betalningsvillkor. Du kan skicka försäljningsofferten till kunden för att meddela erbjudandet. Du kan e-posta dokument som en PDF-bilaga. Du kan också välja e-postbrödtexten förifylld med en sammanfattning av offerten. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).

Medan du förhandlar med kunden kan du ändra och skicka försäljningsofferten så mycket som behövs. När kunden accepterar offerten omvandlar du försäljningsofferten till en försäljningsfaktura eller försäljningsorder som du bearbetar försäljningen. Mer information finns i [Fakturera försäljning](sales-how-invoice-sales.md) eller [Sälja produkter](sales-how-sell-products.md).

Du kan fylla i kundfälten på försäljningsofferten på två sätt, beroende på om kunden redan har registrerats. Se steg 2 och 3 i följande procedur.

## <a name="to-create-a-sales-quote"></a>Så här skapar du en försäljningsoffert

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **försäljningsofferter** och välj sedan tillhörande länk.
2. Ange namnet på en befintlig kund i fältet **Kund**.

   Andra fält på sidan **Försäljningsoffert** innehåller standardinformation om den valda kunden.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]

    Flera fält i Försäljningsofferten är nu ifyllda med information som du har angett på det nya kundkortet.  
3. På sidan **Förs.offert** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du är nu klar att fylla i försäljningsorderraderna för produkter som du säljer till kunden eller för en transaktion med den kund som du vill registrera en post i ett redovisningskonto.  

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
8. Upprepa moment 4 till 7 för varje produkt som du vill att erbjuda kunden.

    Summorna under raderna beräknas automatiskt när du skapar eller ändrar rader.  
9. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > För att fylla i **Offertens giltighetsdatum** fylls i automatiskt med ett visst antal dagar efter att offerten har skapats, kan du fylla i **Beräkning av offertens giltighet** på sidan **Försäljning & kundreskontra**.

10. När försäljningsoffertraderna slutförda väljer du åtgärden **Skicka med e-post**.
11. På sidan **Skicka e-post** fyller du i återstående fält och granskar den inbäddade försäljningsofferten. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).
12. Om kunden accepterar offerten väljer du åtgärden **Gör faktura** eller **Gör order**.

Försäljningsofferten tas bort från databasen. En försäljningsfaktura eller försäljningsorder har skapats baserat på informationen i försäljningsofferten där du kan bearbeta försäljningen. I fältet **Offertnr** på försäljningsfakturan eller försäljningsordern kan du ange numret på försäljningsofferten som den har skapats från. Mer information finns i [Fakturera försäljning](sales-how-invoice-sales.md) eller [Sälja produkter](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Externt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Tilldela dokumentets layouter för kunder eller leverantörer
description: Använd dokumentlayout för att styra utseende och format för dokument som fakturor och order som du skickar till kunder och leverantörer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definiera dokumentlayout för kunder och leverantörer

Med dokumentets layout används rapportlayout för att definiera hur många dokument du skickar till kunder och leverantörer. Business Central innehåller standardlayouter, men du kan också anpassa egna layouter för var och en av dina affärspartner. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md). Du väljer standard-och anpassade dokumentlayout från kund-och leverantörs korten genom att välja åtgärden **dokumentlayout**. Värdet i fältet **användning** definierar den procedur som dokumentlayouten används för. För kunder kan du till exempel använda **påminnelse**, **leverans** och **bekräftelse** typer för dokumentets layout.

Med dokumentlayout kan du också spara tid när du skickar dokument till kund- eller leverantörskontakter via e-post. För varje layout som du tilldelar kunden eller kontakten kan du ange en eller flera e-postadresser för kontakter. Du kan t. ex. skicka en faktura till kundens inköps- och distributionskontakter. Det är enkelt att lägga till kontaktens e-postadresser. På sidan **Dokumentlayouter** låter åtgärden **Välj e-post från kontakter** dig välja från en lista över kontaktadresser som du har registrerat för kunden eller leverantören. Du kan också lägga till e-postadresser manuellt. Om du anger flera adresser avgränsar du dem med semikolon, och lägger inte till några blanksteg mellan adresserna.

Innan du kan definiera vilken dokumentlayout som ska användas för vilka processer och vilken kontakt som du vill skicka dokumentet till, måste du ladda alla tillgängliga rapporter (dokument) från sidan **rapportval**. Du kan snabbt ladda dokumenten med hjälp av åtgärden **kopiera från rapporturval** på sidan **dokumentmallar**.

Stegen i följande avsnitt beskriver hur man definierar försäljningsdokumentlayouter från sidan **Kundkort**. För leverantörer är stegen desamma från sidan **leverantörskort**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Så här laddar du standardlayouter för dokument för försäljningsdokument för en kund

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna sidan **kundkort** för kunden och välj sedan åtgärden **dokumentlayout**.
3. På sidan **Dokumentlayouter**, välj åtgärden **Kopiera från rapporturval**.

På sidan **dokumentlayout** visas alla layouter som är tillgängliga för försäljningsdokument. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Så här väljer du en anpassad rapportlayout som ska användas för layouter för försäljningsdokument

Om du inte redan har skapat en egen rapportlayout för dokumenttypen måste du göra det först. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna sidan **kundkort** för kunden och välj sedan åtgärden **dokumentlayout**.
3. På sidan **dokumentlayout** på raden för en rapportlayout som du vill använda en anpassad layout för, väljer du fältet **Anpassad layoutbeskrivning**.
4. På sidan **Anpassade rapportlayouter**, välj den dokumentlayout som du vill använda för försäljningsdokumenttyp. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-will-receive-which-document-layout-for-a-customer"></a>Så här anger du vilken kontakt som får vilken dokumentlayout för en kund

Om du vill spara tid när du skickar dokument till kund- och leverantörskontakter via e-post, anger du deras e-postadresser på dokumentlayout. Du kan till exempel alltid skicka kundutdrag till deras revisorskontakter och försäljningsorder till deras köpare eller inköpsorder till säljare.

1. På sidan **dokumentlayouter** på raden för en rapportlayout som du vill skicka till en viss kontakt för kunden väljer du åtgärden **Välj e-post från kontakter**.
2. Välj en eller flera kontakter på sidan **kontakter** och klicka sedan på **OK**.

## <a name="see-also"></a>Se även

[Uppdatera anpassade rapportlayouter](ui-update-report-layouts.md)  
[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Arbeta med rapporter, batch-jobb och XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

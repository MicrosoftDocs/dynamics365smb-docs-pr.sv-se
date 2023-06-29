---
title: Bokföra koncerninterna dokument och journaler
description: Detta ämne förklarar hur du använder koncerninterna dokument eller journaler för att bokföra transaktioner med koncerninterna partner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals"></a><a name="work-with-intercompany-documents-and-journals"></a>Arbeta med koncerninterna dokument och journaler

Du använder koncerninterna dokument eller journaler för att bokföra transaktioner med koncerninterna partner. När du bokför ett koncerninternt dokument eller journalrad i företaget skapas, skapas ett motsvarande dokument eller journalrad i din koncerninterna utkorg. Du överför raden från Utkorgen till partnern. Partnern kan sedan bokföra den koncerninterna transaktionen i sitt företag utan att behöva registrera samma data på nytt.

För försäljnings- och inköpsdokument säkerställer den koncerninterna partnerkoden för kunden eller leverantören att alla beställningar och fakturor för transaktioner mellan partnerna kommer att producera motsvarande dokument i partnerföretagen. Företagets konton balanserar korrekt.

Detsamma gäller för koncerninterna redovisningsjournalrader. Du behöver inte specificera konton, du väljer själv partnerföretaget. Motsvarande koncerninterna redovisningsjournalrader skapas sedan i partnerföretaget.

## <a name="fill-in-and-send-an-intercompany-sales-order"></a><a name="fill-in-and-send-an-intercompany-sales-order"></a>Fyll i och skicka en koncernintern försäljningsorder

Du kan skicka försäljnings- och inköpsorder samt returorder före bokföring. Fakturor och kreditnotor kan inte skickas förrän de är bokförda.

Följande procedur beskriver hur du fyller i och skickar en koncernintern försäljningsorder. Samma steg gäller koncerninterna inköpsorder och returorder och till bokförda koncerninterna fakturor och kreditnotor.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.  
2. Välj **Ny** för att skapa en ny försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Se till att kunden är en koncernintern partner.
5. Om du vill skicka försäljningsordern innan du bokför den, väljer du åtgärden **skicka Koncerninterna försäljningsorder**.

> [!NOTE]
> Om du utför steg 5, går försäljningsordern till koncerninterna utkorgen där du kan skicka den senare. Om du vill veta mer om den koncerninterna inkorgen och utkorgen går du till [Hantera den koncerninterna inkorgen och utkorgen](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal"></a><a name="fill-in-and-post-an-intercompany-journal"></a>Fyll i och bokför koncerninterna journaler

När du bokför ett koncernintern redovisningsjournalsrad i företaget skapas, skapas ett motsvarande journalrad i din koncerninterna utkorg som du kan överföra till partnern. Med 2022 utgivningscykel 1 kan du också ställa in företaget för automatiskt skapande av mottagna koncerninterna transaktioner som partner bokförde i de koncerninterna redovisningsjournalerna. Partnern kan sedan bokföra den koncerninterna transaktionen i sitt företag utan att behöva registrera samma data på nytt.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Koncernintern redovisningsjournaler** och väljer sedan relaterad länk.  
2. Öppna journalerna. Mer information finns i [Arbeta med Skapa redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. I fältet **Redov.ktonr konc.int. partner** anger du det koncerninterna redovisningskontot som beloppet ska bokföras på i partnerns företag.

    > [!NOTE]
    > Fältet måste vara ifyllt på en rad med ett bankkonto eller redovisningskonto i antingen fältet **Kontonr.** eller **Motkonto**.  
5. Välj åtgärden **Bokföra**.

Transaktionerna bokförs i företaget och en journal med motsvarande transaktioner och skapas i koncerninterna utkorgen som du kan skicka till partnerföretaget.

## <a name="see-also"></a><a name="see-also"></a>Se även

[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

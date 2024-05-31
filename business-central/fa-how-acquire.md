---
title: Anskaffa anläggningstillgångar
description: 'Du kan ställa in en anläggningstillgång, tilldela en avskrivningsregel och registrera anläggningstillgångens anskaffningskostnad.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="acquire-fixed-assets"></a>Anskaffa anläggningstillgångar

 **Använd sidan Anläggningstillgångskort** för att ange information om en tillgång. Du kan ställa in byggnads- eller produktionsutrustning som en huvudtillgång med en komponentlista och du kan gruppera dem på olika sätt, till exempel efter klass, avdelning eller plats. Du måste upprätta och koppla en avskrivningsregel till varje anläggningstillgång innan du kan förvärva den.

När du har skapat en anläggningstillgång och tilldelat en avskrivningsregel måste du skaffa den. Om du vill anskaffa en anläggningstillgång, registrerar du dess anskaffningskostnad i relevant redovisningskonto, bankkonto eller leverantör genom att bokföra en förvärvtransaktion från sidan **Anl.tillg. redovisningsjournal**. Du kan använda sidan **Assisterad anskaffning av anläggningstillgång** för att skapa och bokföra de redovisningsjournalrader som behövs automatiskt.

Använd indexering för att justera värden för allmänna prisnivåändringar. Använd batch-jobbet **Indexera anläggningstillgångar** när du beräknar anskaffningskostnader och ersättningskostnader.

## <a name="add-a-fixed-asset-to-your-list-of-fixed-assets"></a>Lägga till en anläggningstillgång i listan över anläggningstillgångar

Innan du kan förvärva en anläggningstillgång måste du lägga till den i tillgångsförteckningen. Det finns flera sätt att lägga till anläggningstillgångar i listan:

* Ange information om tillgångarna **på sidan Anläggningstillgångskort** .
*  **Använd åtgärden Redigera i Excel** om du vill hämta listan över resurser till ett kalkylblad, lägga till nya resurser i listan och sedan publicera uppdateringen till [!INCLUDE [prod_short](includes/prod_short.md)].
* Använda en inköpsorder för att lägga till tillgångar.
* Använd åtgärden Kopiera anläggningstillgång **.** 

När du har lagt till anläggningstillgångar i listan är nästa steg att skaffa dem så att du kan använda dem i transaktioner. Läs mer i [Skaffa en anläggningstillgång](#acquire-fixed-assets).

### <a name="add-a-fixed-asset-on-the-fixed-asset-card-page"></a>Lägg till en anläggningstillgång på sidan Anläggningstillgångskort

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten på snabbfliken **Allmän** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I snabbfliken **Avskrivningsregelkort** fyller du i fälten efter behov. Dessa steg tilldelar en avskrivningsregel till anläggningstillgången.  
4. Om du vill använda mer än en avskrivningsregel till anläggningstillgången väljer du åtgärden **Lägg till flera avskrivningsregler**. Mer information finns i [Så här kopplar du en avskrivningsregel till en anläggningstillgång](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    När du har fyllt i de obligatoriska fälten visas knappen **Du är redo att förvärva anläggningstillgången.** Meddelandet visas högst upp på sidan. Om du är redo att förvärva tillgången nu väljer **du åtgärden Förvärva** . Följ stegen på sidan Assisterad anskaffning av **anläggningstillgångar** för att slutföra anskaffningen. Om du inte är redo kan du alltid förvärva tillgången senare.

### <a name="use-edit-in-excel-to-add-assets"></a>Använda Redigera i Excel för att lägga till resurser

Om du vill lägga till många anläggningstillgångar är Redigera i Excel ett bra verktyg att använda. Verktyget hämtar din aktuella lista över tillgångar i ett kalkylblad som innehåller de flesta fälten på sidan Anläggningstillgångskort. Du kan fylla i några eller alla fält på en rad för varje tillgång och publicera ändringarna så att de läggs till i [!INCLUDE [prod_short](includes/prod_short.md)] listan. Om du inte kan fylla i alla obligatoriska fält är det ok. Du kan uppdatera dem [!INCLUDE [prod_short](includes/prod_short.md)] när du är klar.

> [!NOTE]
> Om du vill använda åtgärden Redigera i Excel måste Office-tillägget vara Microsoft Dynamics installerat. Tillägget skapar kopplingen mellan Excel och [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Hämta Business Central-tillägget för Excel](admin-deploy-excel-addin.md).

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj ikonen :::image type="content" source="media/share-icon.png" alt-text="Dela den här sidan med andra användare eller appar."::: Och välj **sedan Redigera i Excel**.
3. Öppna den hämtade filen och ange information om de nya anläggningstillgångarna.

   > [!TIP]
   > Du behöver inte ange en identifierare i Nr **.** . När du publicerar uppdateringen [!INCLUDE [prod_short](includes/prod_short.md)]  tilldelas en identifierare baserat på den nummerserie du använder för anläggningstillgångar.

4. Om du vill uppdatera [!INCLUDE [prod_short](includes/prod_short.md)] väljer du **Microsoft Dynamics** Publicera **i** fönstret.

### <a name="add-a-fixed-asset-from-a-purchase-order-or-invoice"></a>Lägga till en anläggningstillgång från en inköpsorder eller faktura

Följande steg beskriver hur du lägger till en anläggningstillgång från en inköpsorder. Stegen är liknande för en inköpsfaktura.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. Välj **Ny** för att skapa en ny inköpsorder.
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4.  **Välj** Anläggningstillgång i **fältet**  **Typ på snabbfliken Rader**.
5. I fältet **Nr.** Väljer du antingen en befintlig anläggningstillgång om du vill lägga till en utgift eller Ny om du **vill** lägga till en ny tillgång.
6. När du har angett informationen om den nya tillgången och inköpsordern väljer **du Bokför**.

## <a name="acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal"></a>Skaffa en anläggningstillgång med hjälp av en redovisningsjournal för anläggningstillgångar

I följande procedur beskrivs hur du skaffar genom att skapa och bokföra de redovisningsjournalrader som krävs. Du kan också skapa och bokföra journalrader manuellt. Mer information finns i [Skaffa en anläggningstillgång med hjälp av en redovisningsjournal](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal) för anläggningstillgångar.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
1. Välj den tillgång som du vill förvärva och välj **sedan åtgärden Förvärva** .
1. Följ stegen på sidan Assisterad anskaffning av **anläggningstillgångar** för att slutföra anskaffningen.

> [!NOTE]  
> Du kan också bokföra anskaffningstransaktioner som krediteringar. I detta fall ska du komma ihåg att värdet i fältet **Anskaffningskostnad inkl. moms** måste vara med ett minustecken för att ange en kreditering.

När du väljer **Slutför** fylls fältet **Bokföringsvärde** på **sidan Anläggningstillgångskort** i, vilket anger att anläggningstillgången anskaffats till angiven anskaffningskostnad.  

## <a name="to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal"></a>Så här bokför du en anskaffning av anläggningstillgångar manuellt med en redovisningsjournal för anläggningstillgångar

Efterföljande procedur beskriver hur du anskaffar en anläggningstillgång manuellt, genom att skapa och bokföra rader på sidan **Anl.tillg. redovisningsjournal**. Du kan också skaffa en anläggningstillgång automatiskt på **sidan Anläggningstillgångskort** genom att välja åtgärden **Skaffa anläggningstillgång** . Mer information finns i [Skaffa en anläggningstillgång](#acquire-fixed-assets).

> [!NOTE]  
> Du kan också bokföra anskaffningstransaktioner som krediteringar. I detta fall ska du komma ihåg att värdet i fältet **Belopp** måste vara med ett minustecken för att ange en kreditering.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anl.tillg. redovisningsjournaler** och väljer sedan relaterad länk.
2. På sidan **Redovisningsjournaler för anl.tillg.** i fältet **Anl.bokföringstyp** väljer du **Anskaffningskostnad**.
3. Fyll i återstående fält om det behövs.
4. Välj åtgärden **Bokföra**.  

> [!TIP]  
> Om du fyller i Försäkringsnr **.**  [!INCLUDE[prod_short](includes/prod_short.md)] bokförs även anskaffningskostnaden för anläggningstillgången i försäkringstransaktionerna. Mer information finns i [Försäkra anläggningstillgångar](fa-how-insure.md).

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Så här ställer du in en komponentlista för en huvudtillgång

Du kan gruppera anläggningstillgångarna i huvudtillgångar och tillhörande komponenter. Du kanske till exempel har en produktionsmaskin som består av flera delar som du vill gruppera på det här sättet.  

Du måste ställa in huvudtillgången och alla dess komponenter som enskilda anläggningstillgångar. När du har skapat en komponentlista [!INCLUDE[prod_short](includes/prod_short.md)]  fylls fälten **Huvudtillgång/Komponent** och **Komponenter till huvudtillgång** i automatiskt för anläggningstillgångarna.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Markera den anläggningstillgång som är huvudtillgången och välj sedan åtgärden **Huvudtillgångskomponenter**.
3. På sidan **Huvudtillgångskomponenter** väljer du fältet **Anl.nr** och väljer den anläggningstillgång som du vill lägga till som en komponent i huvudtillgången.
4. Stäng sidan.
5. Upprepa steg 3 och 4 för varje tillgångskomponent som du vill lägga till.
6. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inställningar för anläggningstillgångar** och väljer sedan relaterad länk.
7. Aktivera växlingsknappen **Tillåt bokföring till huvudtillgångar** .

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Att rätta en bokföring av anskaffningskostnad för en anläggningstillgång,

Om du gör ett fel när du bokför en anskaffningskostnad kan du flytta transaktionen med batch-jobbet **Rätta anl.trans.** och sedan bokföra rätt anskaffningstransaktion. De felaktiga transaktionerna överförs till sidan **Anl. felaktiga transaktioner**.

Om du till exempel bokför en anskaffning med fel datum måste du rätta det så snart som möjligt eftersom Anl.bokföringsdatum används i många beräkningar.

> [!IMPORTANT]  
> Du kan inte använda **åtgärden Återför transaktioner** för anläggningstillgångstransaktioner.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ikonen, ange **Anl.transaktioner** och välj sedan relaterad länk.  
2. På sidan **Anl.transaktioner** markerar du den eller de transaktioner som du vill makulera.  
3. Välj menyn **Åtgärder** och välj sedan åtgärden **Avbryt transaktioner**.
4. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Klicka på **OK** för att köra batchjobbet.
6. Fortsätt med att bokföra rätt anskaffningskostnad när den felaktiga transaktionen, eller transaktionerna har rättats.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Att bokföra återanskaffningsvärdet tillsammans med anskaffningskostnaden

Återanskaffningsvärdet är en anläggningstillgångs restvärde när den inte längre kan användas. Du kan bokföra återanskaffningsvärdet samtidigt som du bokför anskaffningskostnaden. Mer information finns i [Avskrivning eller amortering av anläggningstillgångar](fa-how-depreciate-amortize.md).

Du kan bokföra återanskaffningsvärden tillsammans med anskaffningskostnaden från en journal för anläggningstillgångar.

> [!NOTE]
> Du kan behöva anpassa sidan Anläggningstillgångsjournaler genom att lägga till fältet Återanskaffningsvärde. Som standard visas inte fältet på sidan. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångsjournaler** och väljer sedan relaterad länk.
2. Skapa anskaffningsraden på sidan **Anläggningstillgångsjournaler**. Mer information finns i [Så här bokför du en anskaffning av anläggningstillgångar manuellt med en redovisningsjournal](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal) för anläggningstillgångar.
3. I fältet **Återanskaffningsvärde** på journalraden anger du återanskaffningsvärdets belopp som en kreditering (sätt ett minustecken framför beloppet, till exempel, **-** 100).
4. Välj åtgärden **Bokföra**.

> [!NOTE]
> Om det finns ett återanskaffningsvärde för en anläggningstillgång används det värdet i avskrivningsbokföringen i stället för värdet i fältet **Utgående bokföringsvärde** på **sidan Anl. avskrivningsregler** . Mer information finns i [Så här hanterar du utgående bokföringsvärde](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Utforma detaljer om icke avdragsgill momspåverkan på anläggningstillgångar](design-details-nondeductible-vat.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

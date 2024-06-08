---
title: Skapa avskrivning för anläggningstillgångar
description: Det finns flera avskrivningsmetoder. I Business Central definierar du avskrivningsmetoden för en anläggningstillgång sidan **Anläggningstillgångskort**.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-fixed-asset-depreciation"></a>Skapa avskrivning för anläggningstillgång

Du kan använda olika avskrivningsmetoder när du förbereder redovisningsrapporter och självdeklarationer. Många större företag använder linjär avskrivning i redovisningsrapporterna eftersom de då i allmänhet kan rapportera större inkomster. Vad gäller självdeklaration använder många företag däremot en accelererad avskrivningsmetod, till exempel degressiv avskrivning. Du kan definiera avskrivningsmetoden för en tillgång med fältet **Avskrivningsmetod** på sidan **Anläggningstillgångskort**. Mer information om vad de olika metoderna gör finns i [Avskrivningsmetoder](fa-depreciation-methods.md).

Du skapar avskrivningsregler där du definierar de olika sätt på vilka avskrivning måste beräknas för olika typer av anläggningstillgångar. Varje avskrivningsregel anger enskilda avskrivningsvillkor. Du kan t. ex. ange att en anläggningstillgång ska avskrivas under loppet av tre år i en regel och under loppet av fem år i en annan.

Efter att du har skapat de avskrivningsregler som behövs måste du koppla en eller flera avskrivningsregler till varje anläggningstillgång. En avskrivningsregel som tilldelats en anläggningstillgång kallas för anläggningstillgångens avskrivningsregel. Du kan skapa valfritt antal avskrivningsregler för en anläggningstillgång.  

## <a name="to-create-a-depreciation-book"></a>Att skapa en avskrivningsregel

I anläggningstillgångens avskrivningsregel anger du hur en anläggningstillgång ska skrivas av. Om du vill använda olika avskrivningsmetoder kan du skapa flera avskrivningsregler.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **avskrivningsregler** och väljer sedan relaterad länk.
2. På sidan **Lista över avskrivningsregler** väljer du åtgärden **Ny**.
3. På sidan **Avskrivningsregelkort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Du kan bokföra in anläggningstillgångstransaktioner på sidan **Anl.tillg. redovisningsjournal** eller på sidan **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering. Följ nästa steg för att definiera vilken journaltyp som används för de olika anläggningstillgångaktiviteterna som standard.
4. På snabbfliken **Integrering** markerar du kryssrutan för varje anläggningstillgångsaktivitet vars transaktioner du vill bokföra med hjälp av sidan **Anl.tillg. redovisningsjournal**.
5. Upprepa steg 2 till och med 4 för varje avskrivningmetod eller bokföringsmetod som du vill tilldela till anläggningstillgångar som en avskrivningsregel.

> [!IMPORTANT]
> Välj fältet **Använd avrundning i periodisk avskr.** om du vill avrunda de beräknade periodiska avskrivningsbeloppen till heltal. Om företaget till exempel också använder fakturaavrundning till heltal på sidan **Redovisningsinställningar** kan avrundning även avskrivningsbelopp till heltal bidra till transparens.

Om du till exempel avyttrar en anläggningstillgång där avskrivningsregeln inte anger avrundning men företagets redovisningsinställningar kräver avrundning, visas ett felmeddelande om att ett belopp måste avrundas på en redovisningstransaktion när du avyttrar anläggningstillgången.  

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Att tilldela en avskrivningsregel till en anläggningstillgång.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Välj anläggningstillgången som du vill skapa avskrivningsregeln för anläggningstillgångar för.
3. I snabbfliken **Avskrivningsregelkort** fyller du i fälten efter behov.
4. Om du vill använda mer än en avskrivningsregel till anläggningstillgången väljer du åtgärden **Lägg till flera avskrivningsregler**.
5. Välj alternativt åtgärden **Avskrivningsregler** för att ange en eller flera avskrivningsregler för anläggningstillgångar.

    > [!NOTE]  
    >   När du använder den manuella avskrivningsmetoden måste du föra in avskrivningen manuellt i redovisningsjournalen för anläggningstillgångar. Funktionen **Beräkna avskrivning** utesluter anläggningstillgångar där den manuella avskrivningsmetoden används. Du kan använda den här metoden för tillgångar som du inte längre kan skriva av, exempelvis mark.

    > [!NOTE]  
    > När du använder den användardefinierade avskrivningsmetoden måste du tilldela avskrivningsregeln på ett annat sätt. Mer information finns i [Skapa användardefinierad avskrivningsmetod](fa-how-setup-user-defined-depreciation-method.md).

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Att tilldela en avskrivningsregel till åtskilliga anläggningstillgångar med hjälp av ett batch-jobb

Om du vill tilldela en avskrivningsregel till flera anläggningstillgångar kan du använda batch-jobbet **Skapa anl. avskrivningsregler** för att skapa avskrivningsregler för anläggningstillgångar.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Markera den anläggningstillgång som du vill tilldela en avskrivningsregel till och välj sedan åtgärden **Redigera**.
3. På sidan **Avskrivningsregelkort** väljer du åtgärden **Skapa avskrivningsregler för anl.tillg.**.
4. På sidan **Välj Avskrivningsregler för anl.tillg.** fyller du i fältet **Avskrivningsregler**.
5. Välj fältet **Kopiera från anl.nr** och välj sedan det anläggningstillgångsnummer som du vill använda som bas för att skapa nya avskrivningsregler för anläggningstillgångar.

    Om du fyller i det här fältet kommer avskrivningsfälten i anläggningstillgångarnas nya avskrivningsregler att innehålla samma information som motsvarande fält i den avskrivningsregel för anläggningstillgång som du kopierar från. Lämna fältet tomt om du vill skapa nya avskrivningsregler för anläggningstillgångar med tomma avskrivningsfält.  
6. På snabbfliken **Anläggningstillgång** kan du ange ett filter så att du kan välja vilka tillgångar du vill skapa avskrivningsregler för anläggningstillgång .
7. Välj **OK**.

## <a name="to-set-up-depreciation-posting-types"></a>Så här skapar du bokföringstyper för avskrivning

För varje avskrivningsregel måste du ange hur du vill att [!INCLUDE[prod_short](includes/prod_short.md)] ska hantera olika bokföringstyper. Till exempel om bokföringen ska vara debet eller kredit och om bokföringstypen ska inkluderas i avskrivningsbasen.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **avskrivningsregler** och väljer sedan relaterad länk.  
2. Markera den avskrivningsregel som du vill ställa in och välj sedan åtgärden **Anl. inställningar bokföring**.
3. På sidan **Anl. inställningar bokföring** fyller du i fälten efter behov.

    > [!NOTE]  
    >   Du kan inte infoga eller ta bort rader på sidan **Anl. inställningar bokföring**. Du kan endast ändra de befintliga raderna.

Du bör inte ändra inställningen för avskrivningsregler som transaktioner redan har bokförts för. Ändringarna påverkar inte transaktioner som redan har bokförts, vilket gör att statistiken över avskrivningsregler blir missvisande.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Så här ställer du in standardmallar och journaler för avskrivningsregler för anläggningstillgångar.

För varje avskrivningsregel anger du en standardinställning för mallar och journaler. Du kan använda dessa standardinställningar för att duplicera rader från en journal till en annan, skapa journalrader med hjälp av batchjobben **Beräkna avskrivning** eller **Indexera anläggningstillgångar**, duplicera anskaffningskostnader i försäkringsjournalen.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **avskrivningsregler** och väljer sedan relaterad länk.  
2. Markera den avskrivningsregel som du vill skapa standardjournaler för och välj sedan åtgärden **Anl. journalinställningar**.  
3. Om du vill ha en standardinställning för varje användare väljer du fältet **Användar-ID** så visas sidan **Användare**.  
4. Välj journalmallen eller journalen som ska användas som standard i de andra fälten.  

## <a name="fiscal-year-365-days-field-depreciation"></a>Räkenskapsår på 365 dagar, fältavskrivning

När batchjobbet Beräkna avskrivning körs används normalt ett standardår med 360 dagar där varje månad har 30 dagar.

Om du väljer det här fältet använder batchjobbet Beräkna avskrivning kalenderåret med 365 dagar i stället och varje månad har då samma antal dagar som i kalendern. Det enda undantaget är februari månad under ett skottår, då batchjobbet räknar med 28 dagar och inte 29. Det betyder att alla år, även skottår, anses ha 365 dagar.

## <a name="see-also"></a>Se även

[Ställa in anläggningstillgångar](fa-setup.md)  
[Anläggningstillgångar](fa-manage.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

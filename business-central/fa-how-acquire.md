---
title: "Anskaffa anläggningstillgångar | Microsoft Docs"
description: "Du kan ställa in en anläggningstillgång, tilldela en avskrivningsregel och registrera anläggningstillgångens anskaffningskostnad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a5ce3c514ff649b5ad4a901f257816ae1a59d58
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="acquire-fixed-assets"></a>Skaffa anläggningstillgångar
För varje anläggningstillgång måste du skapa ett kort som innehåller information om tillgången. Du kan ställa in byggnads- eller produktionsutrustning som en huvudtillgång med en komponentlista och du kan gruppera dem på olika sätt, till exempel efter klass, avdelning eller plats. En avskrivningsregel måste ställas in och tilldelas till varje anläggningstillgång, innan du kan anskaffa den.

När en anläggningstillgång är inställd och en avskrivningsregel tilldelad måste du anskaffa anläggningstillgången. Om du vill anskaffa en anläggningstillgång, registrerar du dess anskaffningskostnad i relevant redovisningskonto, bankkonto eller leverantör genom att bokföra en förvärvtransaktion från fönstret **Anl.tillg. redovisningsjournal**. Du kan använda fönstret **Assisterad anskaffning av anläggningstillgång** för att skapa och bokföra de redovisningsjournalrader som behövs automatiskt.

Återanskaffningsvärdet är en anläggningstillgångs restvärde när den inte längre kan användas. Du kan bokföra återanskaffningsvärdet samtidigt som du bokför anskaffningskostnaden. För mer information, se [Så här skriver du av eller amorterar anläggningstillgångar](fa-how-depreciate-amortize.md).

Indexering används för att anpassa värden till den allmänna prisnivån. Du kan använda Batch-jobbet **Indexera anläggningstillgångar** när anskaffningskostnader beräknas som ersättningskostnader.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Så här skapar du en anläggningstillgång och anskaffar den automatiskt
Följande procedur beskriver hur du skapar en fast anläggningstillgång och sedan anskaffar den, genom att använda fönstret **Assisterad anskaffning av anläggningstillgång** för att skapa och bokföra anl.tillg. redovisningsjournal. Du kan också skapa och bokföra journalrader manuellt. För mer information, se avsnittet "Att bokföra en anskaffning av anläggningstillgång manuellt med redovisningsjournalen för anläggningstillgångar".

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anläggningstillgångar** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten på snabbfliken **Allmän** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I snabbfliken **Avskrivningsregelkort** fyller du i fälten efter behov. Dessa steg tilldelar en avskrivningsregel till anläggningstillgången.  
4. Om du vill använda mer än en avskrivningsregel till anläggningstillgången väljer du åtgärden **Lägg till flera avskrivningsregler**. För mer information, se avsnittet "Tilldela en avskrivningsregel till en anläggningstillgång" i [Så här ställer du in avskrivning av anläggningstillgång](fa-how-setup-depreciation.md).

    När alla fält som krävs för att anskaffa en anläggningstillgång är ifyllda kommer meddelandet **Du är redo att anskaffa anläggningstillgången** visas längst upp på sidan.
5. Välj åtgärden **Anskaffa** i meddelandet.
6. Följ stegen i fönstret **Assisterad anskaffning av anläggningstillgång** för att slutföra den automatiska anskaffningen av anläggningstillgången.

> [!NOTE]  
>   Du kan också bokföra anskaffningstransaktioner som krediteringar. I detta fall ska du komma ihåg att värdet i fältet **Anskaffningskostnad inkl. moms** måste vara med ett minustecken för att ange en kreditering.

När du väljer **Slutför**, kommer fältet **Bokföringsvärde** i fönstret **Anläggningstillgångskort** fyllas i och ange att fältet anläggningstillgång har anskaffats till den angivna anskaffningskostnaden.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Så här ställer du in en komponentlista för en huvudtillgång
Du kan gruppera anläggningstillgångarna i huvudtillgångar och tillhörande komponenter. Det kan exempelvis hända att du har en produktionsmaskin som består av flera olika delar och som du vill gruppera så här.  

Både huvudtillgången och dess komponenter måste skapas som enskilda anläggningstillgångskort. När du har skapat en komponentlista fyller [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt i fälten **Huvudtillgång/Komp.** och **Komp. till huvudtillg.** på anläggningstillgångskortet.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anläggningstillgångar** och välj sedan relaterad länk.
2. Markera den anläggningstillgång som är huvudtillgången och välj sedan åtgärden **Huvudtillgångskomponenter**.
3. I fönstret **Huvudtillgångskomponenter** väljer du fältet **Anl.nr** och väljer den anläggningstillgång som du vill lägga till som en komponent i huvudtillgången.
4. Stäng fönstret.
5. Upprepa steg 3 och 4 för varje tillgångskomponent som du vill lägga till.
6. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inställningar för anläggningstillgångar** och välj sedan relaterad länk.
7. Markera kryssrutan **Tillåt bokf. på huvudtillgång**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Att bokföra en anskaffning av anläggningstillgång manuellt med redovisningsjournalen för anläggningstillgångar.
Efterföljande procedur beskriver hur du anskaffar en anläggningstillgång manuellt, genom att skapa och bokföra rader i fönstret **Anl.tillg. redovisningsjournal**. Du kan också anskaffa en anläggningstillgång automatiskt genom att använda fönstret **Assisterad anskaffning av anläggningstillgång**. För mer information, se steg 5 i avsnittet "Så här skapar du en anläggningstillgång och anskaffar den automatiskt".

> [!NOTE]  
>   Du kan också bokföra anskaffningstransaktioner som krediteringar. I detta fall ska du komma ihåg att värdet i fältet **Belopp** måste vara med ett minustecken för att ange en kreditering.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.
2. I fönstret **Redovisningsjournaler för anl.tillg.** i fältet **Anl. bokföringstyp** väljer du **Anskaffningskostnad**.
3. Fyll i återstående fält om det behövs.
4. Välj åtgärden **Bokföra**.  

> [!TIP]  
>   Om du fyller i fältet **Försäkringsnr.** i journalen när du bokför en anskaffningskostnad bokför [!INCLUDE[d365fin](includes/d365fin_md.md)] även anskaffningskostnaden för anläggningstillgången i försäkringstransaktionerna. Mer information finns i [Så här försäkrar du anläggningstillgångar](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Att rätta en bokföring av anskaffningskostnad för en anläggningstillgång,
Om du gör ett fel när du bokför en anskaffningskostnad kan du flytta transaktionen med batch-jobbet **Rätta anl.trans.** och sedan bokföra rätt anskaffningstransaktion. De felaktiga transaktionerna överförs till fönstret **Anl. felaktiga transaktioner**.

Om du till exempel bokför en anskaffning med fel datum måste du rätta det så snart som möjligt eftersom anl. bokföringsdatum används i många kritiska beräkningar.

> [!IMPORTANT]  
>   Du kan inte använda funktionen **Återför transaktion** för anläggningstillgångstransaktioner.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rätta anl.trans.** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Klicka på **OK** för att köra batchjobbet.
4. Fortsätt med att bokföra rätt anskaffningskostnad när den felaktiga transaktionen, eller transaktionerna har rättats.

Använd batch-jobbet **Rätta anl.transaktioner** för att rätta transkationer för flera anläggningstillgångar åt gången.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Att bokföra återanskaffningsvärdet tillsammans med anskaffningskostnaden
Du kan bokföra återanskaffningsvärden tillsammans med anskaffningskostnaden från en redovisningsjournal för anläggningstillgångar.    

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Rätta anl.trans.** och välj sedan relaterad länk.
2. Skapa anskaffningsjournalraden. För mer information, se avsnittet "Att bokföra en anskaffning av anläggningstillgång manuellt med redovisningsjournalen för anläggningstillgångar".
3. I fältet **Återanskaffningsvärde** på journalraden anger du återanskaffningsvärdets belopp som en kreditering (med ett minustecken).
4. Välj åtgärden **Bokföra**.

> [!NOTE]  
>   Bokföringstypen **Återanskaffningsvärde** är endast ett alternativ i fönstret **Redovisningsjournal för anläggningstillgångar**. Den är inte tillgänglig i fönstret **Anl.tillg. redovisningsjournal** eftersom skrotvärde aldrig bokförs i redovisningen.

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


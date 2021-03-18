---
title: Skriva av eller amortera anläggningstillgångar | Microsoft Docs
description: Du måste definiera hur du ska skriva ner, skriva av eller amortera var och en av anläggningstillgångarna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 46a138d7168c48e47f9db823108abc6d6af280ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380587"
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Så här skriver du av eller amorterar anläggningstillgångar
Avskrivning används för att fördela kostnaden för anläggningstillgångar, som exempelvis maskiner och inventarier, över den avskrivningsbara livslängden. För varje anläggningstillgång måste du ange hur den ska avskrivas.  

 Du kan bokföra avskrivning på två sätt:  

* Automatiskt genom att köra batch-jobbet **Beräkna avskrivning**.  
* Manuellt genom att använda fältet anl.tillg. redovisningsjournal.  

[!INCLUDE[prod_short](includes/prod_short.md)] kan beräkna daglig avskrivning, vilket innebär att du kan beräkna avskrivning för vilken period som helst. Du kan därmed analysera aktuella operativa resultat på exempelvis månads-, kvartals- eller årsbasis. Beräkningen används ett standardår på 360 dagar och en standardmånad på 30 dagar. Mer information finns i [Avskrivningsmetoder](fa-depreciation-methods.md).  

Om flera avdelningar använder en anläggningstillgång kan periodisk avskrivning automatiskt fördelas på avdelningarna utifrån en användardefinierad fördelningstabell.  

Du kan rätta felaktiga avskrivningstransaktioner med hjälp av batch-jobbet **Rätta anl.transaktioner**. Därefter kan du bokföra det korrekta beloppet för avskrivningen genom att på nytt köra batch-jobbet **Beräkna avskrivning**. Felen du korrigerar bokförs som felaktiga transaktioner för anläggningstillgångar.  

Indexering används för att anpassa värden till den allmänna prisnivån. Du kan använda batch-jobbet **Indexera anläggningstillgångar** om du vill omberäkna avskrivningsbeloppen.  

## <a name="to-calculate-depreciation-automatically"></a>Så här beräknar du avskrivning automatiskt
En gång i månaden, eller när du vill, kan du köra batch-jobbet **Beräkna avskrivning**. Batch-jobbet ignorerar de anläggningstillgångar som har sålts, spärrats eller som använder den manuella avskrivningsmetoden.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Beräkna avskrivning** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj **OK**.  

    Batch-jobbet beräknar nedskrivningen och skapar rader i redovisningsjournalen för anläggningstillgångar.

4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.  

    På sidan **Anl.tillg. redovisningsjournal** i fältet **Antal avskrivningsdagar** kan du se hur många avskrivningsdagar som har beräknats.  
5. Välj åtgärden **Bokföra**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Att bokföra en avskrivning manuellt från en redovisningsjournalen för anläggningstillgångar.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov.  
3. Välj **Anskaffningskostnad** i fältet **Avskrivning**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av avskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Välj åtgärden **Bokför** om du vill bokföra journalen.  

Fältet **bokföringsvärde** på sidan **Anläggningstillgångskort** uppdateras därefter.

Om du har skapat fördelningsnycklar för anläggningstillgångar, som fördelar belopp på olika avdelningar eller projekt, kan beloppen fördelas under bokföring. Mer information finns i [Ställa in allmän information för anläggningstillgångar](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>Så här hanterar du utgående bokföringsvärde
I fältet **utgående bokföringsvärde** på sidan **Anl. avskrivningsregler** kan du ange det bokföringsvärde som du vill att anläggningstillgången ska ha i aktuell avskrivningsregel när den är helt avskriven. Du kan göra detta manuellt eller fylla i fältet **Standard utg. bokf.värde** på den relaterade sidan **avskrivningsregel**, som då används för att fylla i fältet automatiskt.

> [!NOTE]
> Om den senaste avskrivningen innebär att fältet **Bokföringsvärde** på sidan **Anläggningstillgångskort** är noll, den senaste avskrivningen minskar automatiskt med detta belopp.<br /><br />
> Är **bokföringsvärdet** större än noll efter den senaste avskrivningen, t. ex. på grund av avrundningsproblem eller att det finns ett befintligt återanskaffningsvärde, ignoreras fältet utgående **bokföringsvärde** på sidan **Anl. avskrivningsregler**. Mer information finns i [så här bokför du återanskaffningsvärdet tillsammans med anskaffningskostnaden](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Så här beräknar du fördelningar i redovisningsjournaler för anläggningstillgångar
Om en anläggningstillgång används av flera avdelningar kan periodisk avskrivning automatiskt fördelas på avdelningarna utifrån en användardefinierad fördelningstabell.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.  
2. Skapa en första rad och fyll i fälten efter behov.
3. Välj **Anskaffningskostnad** i fältet **Fördelning**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av fördelning.  
5. Välj åtgärden **Bokför** om du vill bokföra journalen.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Använd dubblettlistor för att förbereda att bokföra åtskilliga avskrivningsregler
När du fyller i journalrader som ska bokföras enligt en avskrivningsregel kan du kopiera raderna till en separat journal och bokföra dem enligt en annan avskrivningsregel. För mer information, se [Så här bokför du transaktioner enligt olika avskrivningsregler](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **avskrivningsregler** och välj sedan relaterad länk.  
2. Öppna avskrivningsregeln och markera sedan kryssrutan **Ingår i dubblettlista**.  

> [!IMPORTANT]  
>   Om du har markerat fältet **Använd dubblettlista** ska du inte använda nummerserien för journalen. Anledningen är att nummerserien för redovisningsjournalen för anläggningstillgångar gör inte nummerserien för anläggningstillgångsjournalen.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Så här bokför du transaktioner enligt olika avskrivningsregler
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.  
2. I journalen som du vill bokföra avskrivning med markerar du kryssrutan **Använd dubblettlista**.  
3. Fyll i återstående fält om det behövs.  
4. Välj åtgärden **Bokföra**.  
5. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Anl.journaler** och välj sedan relaterad länk.  

    > [!NOTE]  
    >   Sidan **Anlägg.tillg.journal** innehåller nya rader för olika avskrivningsregler enligt dubblettlistan.  
6. Granska och redigera raderna och välj sedan åtgärden **bokför**.  

    > [!NOTE]  
    >   Ett alternativt sätt att kopiera en transaktion enligt en annan regel är att ange en avskrivningsregelkod i fältet **Dubblett i avskrivningsregel** när du fyller i en journalrad.  

Du kan kopiera transaktioner från en avskrivningsregel till en annan med hjälp av batch-jobbet **Kopiera avskrivningsregel**. Batch-jobbet skapar journalrader i den journal som du har angett på sidan **Anl. journalinställningar** för den avskrivningsregel som du vill kopiera till. Mer information finns i följande procedur:  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Om du vill kopiera anläggningstillgångstransaktioner mellan avskrivningsregler
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **avskrivningsregler** och välj sedan relaterad länk.  
2. Öppna relevant avskrivningsregelkort och välj sedan åtgärden **Kopiera avskrivningsregel**.  
3. På sidan **Kopiera avskrivningsregel** fyller du i fälten efter behov.  
4. Välj knappen **OK**.  

De kopierade raderna skapas antingen i redovisningsjournalen för anläggningstillgångar eller i anläggningstillgångsjournalen, beroende på om avskrivningsregeln som du kopierar har integrering med redovisningen.  

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
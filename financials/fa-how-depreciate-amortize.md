---
title: "Skriva av eller amortera anläggningstillgångar | Microsoft Docs"
description: "Du måste definiera hur du ska skriva ner, skriva av eller amortera var och en av anläggningstillgångarna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 07e80551ca215eb4c2632faa9f534801a1813680
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-depreciate-or-amortize-fixed-assets"></a>Så här skriver du av eller amorterar anläggningstillgångar
Avskrivning används för att fördela kostnaden för anläggningstillgångar, som exempelvis maskiner och inventarier, över den avskrivningsbara livslängden. För varje anläggningstillgång måste du ange hur den ska avskrivas.  

 Du kan bokföra avskrivning på två sätt:  

* Automatiskt genom att köra batch-jobbet **Beräkna avskrivning**.  
* Manuellt genom att använda fältet anl.tillg. redovisningsjournal.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kan beräkna daglig avskrivning, vilket innebär att du kan beräkna avskrivning för vilken period som helst. Du kan därmed analysera aktuella operativa resultat på exempelvis månads-, kvartals- eller årsbasis. Beräkningen används ett standardår på 360 dagar och en standardmånad på 30 dagar. Mer information finns i [Avskrivningsmetoder](fa-depreciation-methods.md).  

Om flera avdelningar använder en anläggningstillgång kan periodisk avskrivning automatiskt fördelas på avdelningarna utifrån en användardefinierad fördelningstabell.  

Du kan rätta felaktiga avskrivningstransaktioner med hjälp av batch-jobbet **Rätta anl.transaktioner**. Därefter kan du bokföra det korrekta beloppet för avskrivningen genom att på nytt köra batch-jobbet **Beräkna avskrivning**. Felen du korrigerar bokförs som felaktiga transaktioner för anläggningstillgångar.  

Indexering används för att anpassa värden till den allmänna prisnivån. Du kan använda batch-jobbet **Indexera anläggningstillgångar** om du vill omberäkna avskrivningsbeloppen.  

## <a name="to-calculate-depreciation-automatically"></a>Så här beräknar du avskrivning automatiskt
En gång i månaden, eller när du vill, kan du köra batch-jobbet **Beräkna avskrivning**. Batch-jobbet ignorerar de anläggningstillgångar som har sålts, spärrats eller som använder den manuella avskrivningsmetoden.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport") , ange **Beräkna avskrivning**, och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj **OK**.  

    Batch-jobbet beräknar nedskrivningen och skapar rader i redovisningsjournalen för anläggningstillgångar.  
4. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.  

    I fönstret **Anl.tillg. redovisningsjournal** i fältet **Antal avskrivningsdagar** kan du se hur många avskrivningsdagar som har beräknats.  
5. Välj åtgärden **Bokföra**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Att bokföra en avskrivning manuellt från en redovisningsjournalen för anläggningstillgångar.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl.tillg. redovisningsjournal** och välj sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov.  
3. Välj **Anskaffningskostnad** i fältet **Avskrivning**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av avskrivning. För mer information, se avsnittet "Att ställa in bokföringsmallar för anläggningstillgångar" i [Så här ställer du in allmän information för anläggningstillgångar](fa-how-setup-general.md).  
5. På fliken **Start** väljer du **Bokför**.  

Om du har skapat fördelningsnycklar för anläggningstillgångar, som fördelar belopp på olika avdelningar eller projekt, kan beloppen fördelas under bokföring. Mer information finns i [Så här ställer du in allmän information för anläggningstillgångar](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Så här beräknar du fördelningar i redovisningsjournaler för anläggningstillgångar
Om en anläggningstillgång används av flera avdelningar kan periodisk avskrivning automatiskt fördelas på avdelningarna utifrån en användardefinierad fördelningstabell.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl.tillg. redovisningsjournal** och välj sedan relaterad länk.  
2. Skapa en första rad och fyll i fälten efter behov.
3. Välj **Anskaffningskostnad** i fältet **Fördelning**.  
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av fördelning.  
5. På fliken **Start** väljer du **Bokför**.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Använd dubblettlistor för att förbereda att bokföra åtskilliga avskrivningsregler
När du fyller i journalrader som ska bokföras enligt en avskrivningsregel kan du kopiera raderna till en separat journal och bokföra dem enligt en annan avskrivningsregel. För mer information, se avsnittet "Så här bokför du transaktioner enligt olika avskrivningsregler".

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport") , ange **Avskrivningsregler**, och välj sedan relaterad länk.  
2. Öppna avskrivningsregeln och markera sedan kryssrutan **Ingår i dubblettlista**.  

> [!IMPORTANT]  
>   Om du har markerat fältet **Använd dubblettlista** ska du inte använda nummerserien för journalen. Anledningen är att nummerserien för redovisningsjournalen för anläggningstillgångar gör inte nummerserien för anläggningstillgångsjournalen.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Så här bokför du transaktioner enligt olika avskrivningsregler
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl.tillg. redovisningsjournal** och välj sedan relaterad länk.  
2. I journalen som du vill bokföra avskrivning med markerar du kryssrutan **Använd dubblettlista**.  
3. Fyll i återstående fält om det behövs.  
4. Välj åtgärden **Bokföra**.  
5. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anl.journaler** och välj sedan relaterad länk.  

    > [!NOTE]  
>   Fönstret **Anlägg.tillg.journal** innehåller nya rader för olika avskrivningsregler enligt dublettlistan.  
6. Granska och redigera raderna och välj sedan åtgärden **bokför**.  

    > [!NOTE]  
>   Ett alternativt sätt att kopiera en transaktion enligt en annan regel är att ange en avskrivningsregelkod i fältet **Dubblett i avskrivningsregel** när du fyller i en journalrad.  

Du kan kopiera transaktioner från en avskrivningsregel till en annan med hjälp av batch-jobbet **Kopiera avskrivningsregel**. Batch-jobbet skapar journalrader i den journal som du har angett i fönstret **Anl. journalinställningar** för den avskrivningsregel som du vill kopiera till. Mer information finns i följande procedur:  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Om du vill kopiera anläggningstillgångstransaktioner mellan avskrivningsregler
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport") , ange **Avskrivningsregler**, och välj sedan relaterad länk.  
2. Öppna relevant avskrivningsregelkort och välj sedan åtgärden **Kopiera avskrivningsregel**.  
3. I fönstret **Kopiera avskrivningsregelkort** fyller du i fälten efter behov.  
4. Välj **OK**.  

De kopierade raderna skapas antingen i redovisningsjournalen för anläggningstillgångar eller i anläggningstillgångsjournalen, beroende på om avskrivningsregeln som du kopierar har integrering med redovisningen.  

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


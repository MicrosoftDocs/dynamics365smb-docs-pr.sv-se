---
title: "Underhålla anläggningstillgångar | Microsoft Docs"
description: "Du registrerr en underhållspost av reparationer och service för en anläggningstillgång."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 71210a9acbd196581aa4397264b462728007e5e8
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-maintain-fixed-assets"></a>Så här underhåller du anläggningstillgångar.
Underhållskostnaderna är rutinmässiga periodiska kostnader som utförs för att bevara värdet på en anläggningstillgång. Till skillnad från kapitalförbättringar ökar de inte värden.

Du kan registrera och underhålla en aktuell fil om underhåll och service av anläggningstillgångarna så att du enkelt har tillgång ett fullständiga underhållsregister för anläggningstillgångar. När en anläggningstillgång skickas på service noterar du all relevant information, som exempelvis servicedatum, leverantörsnummer och serviceföretagets telefonnummer. Underhållsregistrering registreras för varje anläggningstillgång från det aktuella anläggningstillgångskortet.

Indexering används för att anpassa värden till den allmänna prisnivån. Du kan använda batch-jobbet **Indexera anläggningstillgångar** om du vill omberäkna underhållskostnader.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Om du vill registrera underhållsarbete på en anläggningstillgång
Varje gång som underhåll har utförts, exempelvis ett servicebesök kan du registrera detta för den aktuella anläggningstillgången i fönstret  **Underhållsregistrering**.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.  
2. Markera den anläggningstillgång som du vill registrera underhåll för och välj sedan åtgärden **Underhållsregistreringar**.
3. I fönstret **Underhållsregistreringar** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Att bokföra underhållskostnader från en redovisningsjournalen för anläggningstillgångar.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport") , ange **Avskrivningsregellista**, och välj sedan relaterad länk.  
2. Markera den avskrivningsregel som är tilldelad anläggningstillgången och välj sedan åtgärden **Redigera**.
3. I fönstret **Avskrivningsregelkort** ser du till att kryssrutan **Underhåll** inte är markerad. Detta säkerställer att underhållskostnader inte bokförs till redovisningen.
4. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler för anl.tillg.** och välj sedan relaterad länk.  
5. Skapa en första journalrad och fyll i fälten efter behov.
6. Välj **Anskaffningskostnad** i fältet **Underhåll**.
7. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av underhåll.

    > [!NOTE]  
>   Steg 7 fungerar bara om du har ställt in följande: I fönstret **Anl. bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Underhållskonto** redovisningsdebitkontot och fältet **Underhållskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. För mer information, se avsnittet "Att ställa in bokföringsmallar för anläggningstillgångar" i [Så här ställer du in allmän information för anläggningstillgångar](fa-how-setup-general.md).
8. Välj åtgärden **Bokföra**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Så här följer du upp servicebesök för anläggningstillgångar
Du kan skriva ut rapporten **Underhåll – nästa service** om du vill se vilka tillgångar som du har bokat in ett servicebesök för. Du kan även använda den här rapporten när du uppdaterar fältet **Nästa servicedatum** på anläggningstillgångskortet.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Underhåll nästa service** och välj sedan relaterad länk.  
2. Fyll i fälten **Startdatum** och **Slutdatum**.  
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="to-monitor-maintenance-costs"></a>Så här övervakar du underhållskostnader:
Du kan se underhållskostnaderna när du visar statistiken för en anläggningstillgång.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.
2. Markera den anläggningstillgång som du vill visa underhållskostnader för välj sedan åtgärden **Avskrivningsregler**.
3. I fönstret **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Statistik**.
4. I **Anl.tillg.statistik** väljer du fältet **Underhåll**.

Fönstret **Underhållstransaktioner** öppnas och visar de poster som utgör beloppet i fältet **Underhåll**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Om du vill visa eller skriva ut underhållskostnader för åtskilliga anläggningstillgångar
I rapporten **Underhållsanalys** kan du välja om du vill visa underhåll baaserat på en, två eller tre underhållskoder för ett angivet datum eller en angiven period. Du kan se summan för alla de markerade tillgångarna eller summan för varje tillgång.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Underhållsanalys** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="to-view-maintenance-ledger-entries"></a>Så här visar du underhållstransaktioner
Du kan också studera underhållskostnader genom att visa underhållstransaktionerna.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anläggningstillgångar** och välj sedan relaterad länk.
2. Markera den fasta anläggningstillgång som du vill visa transaktioner för välj sedan åtgärden **Avskrivningsregler**.
3. I fönstret **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Underhållstransaktioner**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Om du vill visa eller skriva ut underhållstransaktioner för åtskilliga anläggningstillgångar
I rapporten **Underhåll - Uppgifter** kan du visa eller skriva ut underhållstransaktioner för en eller flera anläggningstillgångar.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Underhållsdetaljer** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="see-also"></a>Se även
[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


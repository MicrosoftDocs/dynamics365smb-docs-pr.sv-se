---
title: Underhålla anläggningstillgångar
description: Du kan hålla en underhålls post över alla reparationer och tjänster på en anläggningstillgång så att du behåller värdet på anläggningstillgången.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="maintain-fixed-assets"></a><a name="maintain-fixed-assets"></a>Underhålla anläggningstillgångar

Underhållskostnaderna är rutinmässiga periodiska kostnader som utförs för att bevara värdet på en anläggningstillgång. Till skillnad från kapitalförbättringar ökar de inte värden.

Du kan registrera och underhålla en aktuell fil om underhåll och service av anläggningstillgångarna så att du enkelt har tillgång ett fullständiga underhållsregister för anläggningstillgångar. När en anläggningstillgång skickas på service noterar du all relevant information, som exempelvis servicedatum, leverantörsnummer och serviceföretagets telefonnummer. Underhållsregistrering registreras för varje anläggningstillgång från det aktuella anläggningstillgångskortet.

Indexering används för att anpassa värden till den allmänna prisnivån. Du kan använda batch-jobbet **Indexera anläggningstillgångar** om du vill omberäkna underhållskostnader.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a><a name="to-record-maintenance-work-on-a-fixed-asset"></a>Om du vill registrera underhållsarbete på en anläggningstillgång

Varje gång som underhåll har utförts, exempelvis ett servicebesök kan du registrera detta för den aktuella anläggningstillgången på sidan **Underhållsregistrering**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.  
2. Markera den anläggningstillgång som du vill registrera underhåll för och välj sedan åtgärden **Underhållsregistreringar**.
3. På sidan **Underhållsregistreringar** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a><a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Att bokföra underhållskostnader från en redovisningsjournalen för anläggningstillgångar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lista för avskrivningsregel** och väljer sedan relaterad länk.  
2. Markera den avskrivningsregel som är tilldelad anläggningstillgången och välj sedan åtgärden **Redigera**.
3. På sidan **Avskrivningsregelkort** ser du till att kryssrutan **Underhåll** inte är markerad. Detta säkerställer att underhållskostnader inte bokförs till redovisningen.
4. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.  
5. Skapa en första journalrad och fyll i fälten efter behov.
6. Välj **Anskaffningskostnad** i fältet **Underhåll**.
7. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av underhåll.

    > [!NOTE]  
    >   Steg 7 fungerar bara om du har ställt in följande: På sidan **Anl.bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Underhållskonto** redovisningsdebitkontot och fältet **Underhållskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Välj åtgärden **Bokföra**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a><a name="to-follow-up-on-fixed-assets-service-visits"></a>Så här följer du upp servicebesök för anläggningstillgångar

Du kan skriva ut rapporten **Underhåll – nästa service** om du vill se vilka tillgångar som du har bokat in ett servicebesök för. Du kan även använda den här rapporten när du uppdaterar fältet **Nästa servicedatum** på anläggningstillgångskortet.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Underhåll, nästa service** och väljer sedan relaterad länk.  
2. Fyll i fälten **Startdatum** och **Slutdatum**.  
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="to-monitor-maintenance-costs"></a><a name="to-monitor-maintenance-costs"></a>Så här övervakar du underhållskostnader:

Du kan se underhållskostnaderna när du visar statistiken för en anläggningstillgång.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Markera den anläggningstillgång som du vill visa underhållskostnader för välj sedan åtgärden **Avskrivningsregler**.
3. På sidan **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Statistik**.
4. På sidan **Anl.tillg.statistik** väljer du fältet **Underhåll**.

Sidan **Underhållstransaktioner** öppnas och visar de poster som utgör beloppet i fältet **Underhåll**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Om du vill visa eller skriva ut underhållskostnader för åtskilliga anläggningstillgångar

I rapporten **Underhållsanalys** kan du välja om du vill visa underhåll baaserat på en, två eller tre underhållskoder för ett angivet datum eller en angiven period. Du kan se summan för alla de markerade tillgångarna eller summan för varje tillgång.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Underhåll, analys** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="to-view-maintenance-ledger-entries"></a><a name="to-view-maintenance-ledger-entries"></a>Så här visar du underhållstransaktioner

Du kan också studera underhållskostnader genom att visa underhållstransaktionerna.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Markera den fasta anläggningstillgång som du vill visa transaktioner för välj sedan åtgärden **Avskrivningsregler**.
3. På sidan **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Underhållstransaktioner**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Om du vill visa eller skriva ut underhållstransaktioner för åtskilliga anläggningstillgångar

I rapporten **Underhåll – Uppgifter** kan du visa eller skriva ut underhållstransaktioner för en eller flera anläggningstillgångar.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Underhåll, detaljer** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/manage-fixed-assets-maintenance-insurances/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

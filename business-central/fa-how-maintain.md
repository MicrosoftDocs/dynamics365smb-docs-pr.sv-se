---
title: Underhålla anläggningstillgångar
description: Registrera reparationer och service på en anläggningstillgång för att bevara dess värde.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Underhålla anläggningstillgångar

Underhållskostnader är driftskostnader för de saker du gör för att bevara anläggningstillgångarnas skick. Till skillnad från kapitalförbättringar ökar underhåll inte värdet på dina tillgångar.

Varje gång du skickar en anläggningstillgång för service, registrerar du information, t.ex. servicedatum, leverantören som utförde arbetet och servicerepresentantens telefonnummer. Du anger underhållsinformation på flera sidor:

* Anläggningstillgångskort
* Inköpsorder
* Inköpsfaktura
* Anl.tillg. redovisningsjournal

Indexering används för att anpassa värden till den allmänna prisnivån. Använd åtgärden **Indexera anläggningstillgångar** om du vill omberäkna underhållskostnader.

## Registrera en underhållskostnad direkt på en anläggningstillgång

Varje gång som underhåll har utförts för en tillgång, exempelvis ett servicebesök kan du registrera detta på sidan **Underhållsregistrering**.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.  
2. Markera den anläggningstillgång som du vill registrera underhåll för och välj sedan åtgärden **Underhållsregistreringar**.
3. På sidan **Underhållsregistreringar** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Bokför underhållskostnader från en redovisningsjournalen för anläggningstillgångar

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lista för avskrivningsregel** och väljer sedan relaterad länk.  
2. Markera den avskrivningsregel som är tilldelad anläggningstillgången och välj sedan åtgärden **Redigera**.
3. På sidan **Avskrivningsregelkort**, se till att kryssrutan **Underhåll** inte är markerad så att du inte bokför underhållskostnader i redovisningen.
4. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.  
5. Skapa en första journalrad och fyll i fälten efter behov.
6. Välj **Anskaffningskostnad** i fältet **Underhåll**.
7. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av underhåll.

    > [!NOTE]  
    > Steg 7 fungerar bara om du har ställt in följande: På sidan **Anl.bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Underhållskonto** redovisningsdebitkontot och fältet **Underhållskontosaldo** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Välj åtgärden **Bokföra**.

## Registrera underhållskostnader från en inköpsfaktura

Följande steg beskriver hur du registrerar underhållskostnader för en anläggningstillgång från en inköpsfaktura. Momenten är liknande för en inköpsorder.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. I snabbfliken **Allmänt** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. På snabbfliken **Rader** i fältet **Typ** markerar du **Anläggningstillgång**.
4. I fältet **Nr.** väljer tillgången och anger sedan kvantitet och kostnad.
5. I fältet **Anskaffningskostnad**, välj **Underhåll**.
6. Bokför inköpsfakturan

## Uppföljning av servicebesök

Du kan skriva ut rapporten **Underhåll – nästa service** om du vill ange de tillgångar som är bokade för service. Du kan även använda den här rapporten om du vill uppdatera fältet **Nästa servicedatum** på anläggningstillgångskortet.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Underhåll, nästa service** och väljer sedan relaterad länk.  
2. Fyll i fälten **Startdatum** och **Slutdatum**.  
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## Övervaka underhållskostnader

Du kan visa statistik för att övervaka underhållskostnader.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Markera den anläggningstillgång som du vill visa underhållskostnader för välj sedan åtgärden **Avskrivningsregler**.
3. På sidan **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Statistik**.
4. På sidan **Anl.tillg.statistik** väljer du fältet **Underhåll**.

Använd sidan **Underhållstransaktioner** för att visa de poster som utgör beloppet i fältet **Underhåll**.

## Visa eller skriva ut underhållskostnader för åtskilliga anläggningstillgångar

I rapporten **Underhållsanalys** kan du välja om du vill visa undersöka underhåll baserat på en, två eller tre underhållskoder för ett angivet datum eller en angiven period. Rapporten visar summan för alla markerade tillgångar eller summan för varje tillgång.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Underhåll, analys** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## Visa underhållstransaktioner

Du kan också utforska underhållskostnader genom att visa underhållstransaktionerna.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anläggningstillgångar** och väljer sedan relaterad länk.
2. Markera den fasta anläggningstillgång som du vill visa transaktioner för välj sedan åtgärden **Avskrivningsregler**.
3. På sidan **Avskrivningsregler för anl.tillg.** väljer du relevant avskrivningsregel för anläggningstillgång åtgärden **Underhållstransaktioner**.

## Visa eller skriva ut underhållstransaktioner för åtskilliga anläggningstillgångar

I rapporten **Underhåll – Uppgifter** kan du visa eller skriva ut underhållstransaktioner för en eller flera anläggningstillgångar.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Underhåll, detaljer** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

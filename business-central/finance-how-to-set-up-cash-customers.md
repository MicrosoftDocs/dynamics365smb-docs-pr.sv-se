---
title: Så här skapar du Kontantkunder
description: I det här avsnittet beskrivs de steg som krävs för att ställa in en faktura med ett kundnummer för kunder som betalar kontant.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Så här skapar du Kontantkunder

Det går inte att skapa fakturor utan kundnummer. Det gäller även vid kontantförsäljning då det inte finns något att registrera på kundkonton.  

## Så här skapar du en kontantkund

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kund** och väljer sedan relaterad länk.  
2. Skapa ett nytt kort för **Kund**. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).
3. I fältet **Nr.** ange t. ex. **Kassa**.  
4. Skriv till exempel **Kontanförsäljning** i fältet **Namn**.  
5. I snabbfliken **Fakturering** fyller du i fälten **Kundbokföringsmall** och **Gen. rörelsebokföringsmall**.  

 Nu har du skapat en kund som innehåller tillräckliga uppgifter för fakturering.  

> [!NOTE]  
> Du har kanske valt en bokföringsmall som också används vid inhemsk kreditförsäljning. Om du vill underhålla särskilda data om kontantförsäljning, t. ex. genom särskilda konton för försäljning eller kundkrediter, kan du skapa en extra bokföringsmall för detta ändamål.  
>
> Du måste ange ett nummer i bokföringsmallen för kundkreditkontot, även om saldot på detta alltid kommer att vara 0 när du har bokfört fakturor.  

## Se även

[Hantera kundreskontra](receivables-manage-receivables.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)
[Finans](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
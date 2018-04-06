---
title: "Så här skapar du kontantkunder | Microsoft Docs"
description: "Det här avsnittet beskriver hur du skapar en kund som betalar kontant."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 93c28879417b12bc142c84c38c054828b380cc53
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cash-customers"></a>Så här skapar du Kontantkunder
Det går inte att skapa fakturor utan kundnummer. Det gäller även vid kontantförsäljning då det inte finns något att registrera på kundkonton.  

## <a name="to-set-up-a-cash-customer"></a>Så här skapar du en kontantkund  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kund** och välj sedan relaterad länk.  
2.  Skapa ett nytt kort för **Kund**. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).
3.  I fältet **Nr.** ange t.ex. **Kassa**.  
4.  Skriv till exempel **Kontanförsäljning** i fältet **Namn**.  
5.  I snabbfliken **Fakturering** fyller du i fälten **Kundbokföringsmall** och **Gen. rörelsebokföringsmall**.  

 Nu har du skapat en kund som innehåller tillräckliga uppgifter för fakturering.  

> [!NOTE]  
>  Du har kanske valt en bokföringsmall som också används vid inhemsk kreditförsäljning. Om du vill underhålla särskilda data om kontantförsäljning, t.ex. genom särskilda konton för försäljning eller kundkrediter, kan du skapa en extra bokföringsmall för detta ändamål.  
>   
>  Du måste ange ett nummer i bokföringsmallen för kundkreditkontot, även om saldot på detta alltid kommer att vara 0 när du har bokfört fakturor.  

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)    
[Ekonomi](finance.md)  



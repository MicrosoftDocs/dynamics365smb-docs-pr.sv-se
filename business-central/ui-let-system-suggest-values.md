---
title: Konfigurera föreslagna fältvärden | Microsoft Docs
description: Om du vill undvika manuella beräkningar och genomföra uppgifter snabbt och effektivt ställer du in automatisk datainmatning så att Business Central fyller i fälten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5198c9d3e9c5d14c2155f7a4728ee501755909d4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783401"
---
# <a name="letting-prod_short-suggest-values"></a>Låta [!INCLUDE[prod_short](includes/prod_short.md)] föreslå värden
[!INCLUDE[prod_short](includes/prod_short.md)] kan hjälpa dig att avsluta uppgifter som är snabbare och korrektare genom att fylla i fält eller färdigställa rader med data som du annars måste annars beräkna och ange själv. Även om sådana automatiska datainmatningar inte alltid är korrekta kan du ändra den efteråt om du vill.

Funktionen som matar in fältvärden åt dig, erbjuds vanligtvis för uppgifter där du anger stora volymer av transaktionsdata och vill undvika fel och spara tid. Det här avsnittet innehåller ett urval av sådana funktioner. Mer avsnitt ska läggas till i framtida uppdateringar av [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Kryssrutan **Föreslå saldobelopp** på sidan **Redovisningsjournaler**
Om du till exempel vill ange redovisningsjournalrader för åtskilliga kostnader som alla måste bokföras till samma bankkontot, kan du när du varje gång anger en ny journalrad för en kostnad, låta fältet **Belopp** på bankkontoraden uppdateras automatiskt till beloppet som balanserar kostnaderna. Mer information om att arbeta med redovisningsjournaler finns i [arbeta med redovisningsjournaler](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Om du vill ha fältet **Belopp** på balanserande redovisningsjournalrader fyllas i automatiskt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan tillhörande länk.
2. På raden för din föredragna redovisningsjournal väljer kryssrutan **Föreslå saldobelopp**.
3. Öppna redovisningsjournalen och fortsätt att registrera och bokföra transaktioner med den beskrivna funktionen för automatisk bokföring av ett fältvärde.       

Mer information om hur du konfigurerar en personlig redovisningsjournal för t. ex. kostnadsbearbetning finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Fältet **Fyll i Tillbaka datum automatiskt** på sidan **Betalningregistrering**
Sidan **Betalningsregistrering** visar utestående inkommande betalningar som rader som representerar de försäljningsdokument, där ett belopp har förfallit till betalning. Mer information om att koppla kundbetalningar finns i [Så här stämmer du av kundutbetalningar från en lista med obetalda försäljningsdokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Dina huvudåtgärder på sidan är att fylla i kryssrutan **Utförd betalning** och fältet **Tillbaka datum**. Du kan konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] att automatiskt ange arbetsdatum i fältet **Tillbaka datum** när du markerar kryssrutan **Utförd betalning**.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Att ha fältet **Fyll i Tillbaka datum automatiskt** på sidan **Betalningregistrering** ifyllt automatiskt.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för betalningsregistrering** och välj sedan tillhörande länk.
2. Markera kryssrutan **Fyll i Tillbaka datum automatiskt**.
3. Öppna sidan **Betalningsregistrering** och fortsätt behandla inkommande kundbetalningar med hjälp av den beskrivna funktionen för automatisk bokföring av ett fältvärde.

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ekonomi](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
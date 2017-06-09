---
title: "Låta Dynamics 365 for Financials föreslå värden | Microsoft Docs"
description: "Beskriver hur du gör att systemet fyller i markerade fält med värden som du vill beräkna och annars fylla i manuellt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 785ad537f81b8388aa14654f375599a13b66e3c5
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="letting-dynamics-365-for-financials-suggest-values"></a>Låta Dynamics 365 for Financials föreslå värden
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan hjälpa dig att avsluta uppgifter som är snabbare och korrektare genom att fylla i fält eller färdigställa rader med data som du annars måste annars beräkna och ange själv. Även om sådana automatiska datainmatningar inte alltid är korrekta kan du ändra den efteråt om du vill.

Funktionen som matar in fältvärden åt dig, erbjuds vanligtvis för uppgifter där du anger stora volymer av transaktionsdata och vill undvika fel och spara tid. Det här avsnittet innehåller ett urval av sådana funktioner. Mer avsnitt ska läggas till i framtida uppdateringar av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Kryssrutan **Föreslå saldobelopp** i fönstret **Redovisningsjournaler**
Om du till exempel vill ange redovisningsjournalrader för åtskilliga kostnader som alla måste bokföras till samma bankkontot, kan du när du varje gång anger en ny journalrad för en kostnad, låta fältet **Belopp** på bankkontoraden uppdateras automatiskt till beloppet som balanserar kostnaderna. Mer information om att arbeta med redovisningsjournaler finns i [arbeta med redovisningsjournaler](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Om du vill ha fältet **Belopp** på balanserande redovisningsjournalrader fyllas i automatiskt
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Redovisningsjournaler**, och välj sedan relaterad länk.
2. På raden för din föredragna redovisningsjournal väljer kryssrutan **Föreslå saldobelopp**.
3. Öppna redovisningsjournalen och fortsätt att registrera och bokföra transaktioner med den beskrivna funktionen för automatisk bokföring av ett fältvärde.       

Mer information om hur du konfigurerar en personlig redovisningsjournal för t.ex. kostnadsbearbetning finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Fältet **Fyll i Tillbaka datum automatiskt** i fönstret **Betalningregistrering**
Fönstret **Betalningsregistrering** visar utestående inkommande betalningar som rader som representerar de försäljningsdokument, där ett belopp har förfallit till betalning. Mer information om att koppla kundbetalningar finns i [Så här stämmer du av kundutbetalningar manuellt från en lista med obetalda försäljningsdokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Dina huvudåtgärder i fönstret är att fylla i kryssrutan **Utförd betalning** och fältet **Tillbaka datum**. Du kan konfigurera [!INCLUDE[d365fin](includes/d365fin_md.md)] att automatiskt ange arbetsdatum i fältet **Tillbaka datum** när du markerar kryssrutan **Utförd betalning**.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Att ha fältet **Fyll i Tillbaka datum automatiskt** i fönstret **Betalningregistrering** ifyllt automatiskt.
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Inställning av betalningsregistrering**, och välj sedan relaterad länk.
2. Markera kryssrutan **Fyll i Tillbaka datum automatiskt**.
3. Öppna fönstret **Betalningsregistrering** och fortsätt behandla inkommande kundbetalningar med hjälp av den beskrivna funktionen för automatisk bokföring av ett fältvärde.

## <a name="see-also"></a>Se även
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ekonomi](Finance.md)



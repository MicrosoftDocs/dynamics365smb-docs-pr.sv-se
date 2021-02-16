---
title: Registrera och ersätta anställdas affärsrelaterad utgifter | Microsoft Docs
description: Bokför anställdas utgifter med redovisningsjournalen för den anställdas konto och bokför senare en betalning till den anställdes bankkonto för att ersätta för affärsrelaterade utgifter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4d19fceae0fd5c9b72910880d0f87b21206e8f47
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750836"
---
# <a name="record-and-reimburse-employees-expenses"></a>Skapa och återbetala de anställdas utgifter

[!INCLUDE[prod_short](includes/prod_short.md)] stöder transaktioner för medarbetare på samma sätt som för leverantörer. Därför finns medarbetares bokföringsmallar för att vara säker på att medarbetares transaktioner bokförs i relevanta konton i redovisningen.

> [!NOTE]  
> Medarbetartransaktioner kan bokföras i den lokala valutan. Återbetalning till anställda stödjer inte kassarabatter och betalningstoleranser.

Om medarbetare lägger ut sina egna pengar under affärsaktiviteter, kan du bokföra kostnader för den anställde. Du kan sedan ersätta den anställde genom att göra en betalning till den anställdes bankkonto på liknande sätt som när du betalar till leverantörer.  

> [!TIP]
> I den här artikeln beskrivs hur du registrerar kostnader i böckerna och hur du återbetalar den anställde. Din organisation kan ha en portal eller app där anställda kan skicka sina utgiftsrapporter.

## <a name="to-record-an-employees-expense"></a>Om du vill registrera en anställd utgifter
Du bokför anställdas utgifter på sidan **redovisningsjournal**.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan tillhörande länk.
2. Öppna relevant buntnamn för redovisningsjournalen. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten på en ny journalrad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Upprepa steg 3 för alla utgifter som anställde har.

    > [!TIP]  
    > Om du vill ange flera utgiftsrader ovanför en rad i motkontot, till exempel för den anställdes bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen på sidan **redovisningsjournaler**. Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera utgifterna.
5. Välj åtgärden **Bokför** för att registrera kostnader för den anställdes räkning.

## <a name="to-reimburse-an-employee"></a>Återbetala en medarbetare
Du återbetalar en medarbetare genom att bokföra betalningar till dennes bankkonto på sidan **betalningsjournal**.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Utbetalningsjournaler** och välj sedan relaterad länk.
2. Öppna relevant buntnamn för utbetalningsjournal. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten om det behövs. Mer information finns i [Gör betalningar](payables-make-payments.md).
4. Du kan också välja **föreslå betalning för medarbetare** för att automatiskt infoga journalrader för väntande medarbetare återbetalningar.
5. Om du vill registrera återbetalningen väljer du åtgärden **Bokför**.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Så här synkroniserar du återbetalningar med transaktioner för medarbetare
Du kopplar betalningar för medarbetare till deras relaterade öppna transaktioner för medarbetare på samma sätt som du gör för leverantörsbetalningar, till exempel på sidan **Betalningsavstämningsjournal** baserat på de relaterade bankkontoutdragstransaktioner. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan också koppla manuellt på sidan **Personaltransaktioner**. Mer information finns i tillhörande [Stäm av leverantörsbetalningar med betalningsjournalen eller från bokförda leverantörsreskontratransaktioner](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Se även
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

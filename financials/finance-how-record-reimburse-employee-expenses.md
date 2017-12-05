---
title: "Registrera och ersätta anställdas affärsrelaterad utgifter | Microsoft Docs"
description: "Bokför anställdas utgifter med redovisningsjournalen för den anställdas konto och bokför senare en betalning till den anställdes bankkonto för att ersätta för affärsrelaterade utgifter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 0e10011c598678134cb7badbd9a3be97751b4424
ms.contentlocale: sv-se
ms.lasthandoff: 10/17/2017

---
# <a name="how-to-record-and-reimburse-employees-expenses"></a>Så här: skapa och återbetala anställdas utgifter
[!INCLUDE[d365fin](includes/d365fin_md.md)] stöder transaktioner för medarbetare på samma sätt som för leverantörer. Därför finns medarbetares bokföringsmallar för att vara säker på att medarbetares transaktioner bokförs i relevanta konton i redovisningen.

> [!NOTE]  
> Medarbetartransaktioner kan bokföras i den lokala valutan. Återbetalning till anställda stödjer inte kassarabatter och betalningstoleranser.

Om medarbetare lägger ut sina egna pengar under affärsaktiviteter, kan du bokföra kostnader för den anställde. Du kan sedan ersätta den anställde genom att göra en betalning till den anställdes bankkonto på liknande sätt som när du betalar till leverantörer.

## <a name="to-record-an-employees-expense"></a>Om du vill registrera en anställd utgifter
Du bokför anställdas utgifter i fönstret **redovisningsjournal**.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. Öppna relevant buntnamn för redovisningsjournalen. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten på en ny journalrad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Upprepa steg 3 för alla utgifter som anställde har.

    > [!TIP]  
    > Om du vill ange flera utgiftsrader ovanför en rad i motkontot, till exempel för den anställdes bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen i fönstret **redovisningsjournaler**. Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera utgifterna.
5. Välj åtgärden **Bokför** för att registrera kostnader för den anställdes räkning.

## <a name="to-reimburse-an-employee"></a>Återbetala en medarbetare
Du återbetalar en medarbetare genom att bokföra betalningar till dennes bankkonto i fönstret **betalningsjournal**.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.
2. Öppna relevant buntnamn för utbetalningsjournal. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten om det behövs. Mer information finns i [Gör betalningar](payables-make-payments.md).
4. Du kan också välja **föreslå betalning för medarbetare** för att automatiskt infoga journalrader för väntande medarbetare återbetalningar.
5. Om du vill registrera återbetalningen väljer du åtgärden **Bokför**.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Så här synkroniserar du återbetalningar med transaktioner för medarbetare
Du kopplar betalningar för medarbetare till deras relaterade öppna transaktioner för medarbetare på samma sätt som du gör för leverantörsbetalningar, till exempel **Betalningsavstämningsjournal** baserat på de relaterade bankkontoutdragstransaktioner. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan också koppla manuellt i fönstret **Personaltransaktioner**. Mer information finns i de tillhörande [så här: stämma av leverantörsbetalningar manuellt](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Se även
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Så här: Återföra en bokning](finance-how-reverse-journal-posting.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


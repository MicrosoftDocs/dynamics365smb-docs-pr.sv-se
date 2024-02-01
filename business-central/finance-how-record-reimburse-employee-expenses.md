---
title: Skapa och återbetala de anställdas utgifter
description: Bokför anställdas utgifter med redovisningsjournalen för den anställdas konto och bokför en betalning till deras bankkonto för att ersätta för affärsrelaterade utgifter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="record-and-reimburse-employees-expenses"></a>Skapa och återbetala de anställdas utgifter

[!INCLUDE[prod_short](includes/prod_short.md)] stöder transaktioner för medarbetare på samma sätt som för leverantörer. Därför finns medarbetares bokföringsmallar för att vara säker på att medarbetares transaktioner bokförs i relevanta konton i redovisningen.

> [!NOTE]  
> Medarbetartransaktioner kan bokföras i den lokala valutan. Återbetalning till anställda stödjer inte kassarabatter och betalningstoleranser.

Om medarbetare lägger ut sina egna pengar under affärsaktiviteter, kan du bokföra kostnader för den anställde. Du kan sedan ersätta den anställde genom att göra en betalning till den anställdes bankkonto på liknande sätt som när du betalar till leverantörer.  

> [!TIP]
> I den här artikeln beskrivs hur du registrerar kostnader i böckerna och hur du återbetalar den anställde. Din organisation kan ha en portal eller app där anställda kan skicka sina utgiftsrapporter.

[!INCLUDE [prod_short](includes/prod_short.md)] är tillräckligt flexibel för att passa många olika metoder. Vilka kontonummer som ska användas beror på organisationens konfiguration och processer.  

## <a name="to-record-an-employees-expense"></a>Om du vill registrera en anställd utgifter

Du bokför anställdas utgifter på sidan **redovisningsjournal**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournaler** och väljer sedan relaterad länk.  
2. Öppna relevant redovisningsjournal. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten på en ny journalrad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Upprepa steg 3 för alla utgifter som anställde har.

    > [!TIP]  
    > Om du vill ange flera utgiftsrader ovanför en rad i motkontot, till exempel för den anställdes bankkonto markerar du kryssrutan **föreslå saldobelopp** på raden för journalen på sidan **redovisningsjournaler**. Fältet **belopp** på motkontots rad är fördefinierade automatiskt med det värde som krävs för att balansera utgifterna.
5. Välj åtgärden **Bokför** för att registrera kostnader för den anställdes räkning.

## <a name="to-reimburse-an-employee"></a>Återbetala en medarbetare

Du återbetalar en medarbetare genom att bokföra betalningar till dennes bankkonto på sidan **betalningsjournal**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.
2. Öppna relevant buntnamn för utbetalningsjournal. Mer information finns i [Arbeta med redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten om det behövs. Mer information finns i [Utföra betalningar](payables-make-payments.md).
4. Du kan också välja **föreslå betalning för medarbetare** för att automatiskt infoga journalrader för väntande medarbetare återbetalningar.
5. Om du vill registrera återbetalningen väljer du åtgärden **Bokför**.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Så här synkroniserar du återbetalningar med transaktioner för medarbetare

Du kopplar betalningar för medarbetare till deras relaterade öppna transaktioner för medarbetare på samma sätt som du gör för leverantörsbetalningar, till exempel på sidan **Betalningsavstämningsjournal** baserat på de relaterade bankkontoutdragstransaktioner. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan också koppla manuellt på sidan **Personaltransaktioner**. Mer information finns i tillhörande [Stäm av leverantörsbetalningar med betalningsjournalen eller från bokförda leverantörsreskontratransaktioner](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Se även

[Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

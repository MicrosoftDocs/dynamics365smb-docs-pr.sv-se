---
title: "Korrigera eller annullera bokförda försäljningsfakturor | Microsoft Docs"
description: "Beskriver hur du korrigerar, raderar, eller annullerar en bokförd försäljningsfaktura och kopplar en försäljningskreditnota."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 96430c92bf4fecbe98b53d09c06c82a5828b7326
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Korrigera eller makulera obetalda försäljningsfakturor
Du kan korrigera eller annullera en bokförd försäljningsfaktura. Det är användbart om du gör ett fel, eller om kunden begär ett ändring.

> [!NOTE]  
>   När en bokförd försäljningsfaktura har betalts helt eller delvis, kan du inte rätta eller annullera den från själva den bokförda försäljningsfakturan. I stället måste du manuellt skapa en försäljningskreditnota för att makulera försäljningen och för att ersätta kunden, alternaivt hanterat med en försäljningsreturorder. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).

I fönstret **Bokförd försäljningsfaktura** kan du välja åtgärden **Korrigera** eller **Avbryt** för att utföra de åtgärder som beskrivs i följande tabell.

| Åtgärd | Beskrivning |
| --- | --- |
| **Korrigera** |Den bokförda försäljningsfakturan avbryts. En ny försäljningsfaktura med samma information skapas. Du kan göra rättningen och sedan fortsätta försäljningsprocessen. Den nya försäljningsfakturan har ett annat antal än den ursprungliga försäljningsfakturan. En korrigerande försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. På den först bokförda försäljningsfakturan är kryssrutorna Avbruten och Betalad markerade. |
| **Annullera** |Den bokförda försäljningsfakturan avbryts. En korrigerande försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. På den först bokförda försäljningsfakturan är kryssrutorna Avbruten och Betalad markerade. |

När du uppdaterar eller avbryter en bokförd försäljningsfaktura gäller den korrigerande försäljningskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga försäljningsfakturan bokfördes. Det återför den bokförda försäljningsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av försäljningskreditnota för din verifieringskedja.

## <a name="to-correct-a-posted-sales-invoice"></a>Korrigera en bokförd försäljningsfaktura
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförd försäljningsfakturor** och välj sedan relaterad länk.  
2. Markera den bokförda försäljningsfakturan som du vill korrigera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte rätta den bokförda försäljningsfakturan, eftersom den redan har korrigerats eller annullerats.
3. I fönstret **Bokförd försäljningsfaktura** väljer du åtgärden **korrigera**.  
4. En ny försäljningsfaktura med samma information skapas där du kan göra rättningen. Fältet **Avbruten** på den först bokförda försäljningsfakturan ändras till **Ja**.

    En försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan.
5. Välj åtgärden **Visa korrigerande kreditnota** för att visa de bokförda försäljningskreditnotorna som annullerar den ursprungliga bokförda försäljningsfakturan.

## <a name="to-cancel-a-posted-sales-invoice"></a>Avbryta en bokförd försäljningsfaktura
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförd försäljningsfakturor** och välj sedan relaterad länk.  
2. Markera den bokförda försäljningsfakturan som du vill annullera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte avbryta den bokförda försäljningsfakturan, eftersom den redan har korrigerats eller annullerats.
3. I fönstret **Bokförd försäljningsfaktura** väljer du åtgärden **Avbryta**.

    En försäljningskreditnota skapas automatiskt och bokförs för att makulera den ursprungligt bokförda försäljningsfakturan. Fältet **Avbruten** på den först bokförda försäljningsfakturan ändras till **Ja**.
4. Välj åtgärden **Visa korrigerande kreditnota** för att visa de bokförda försäljningskreditnotorna som annullerar den ursprungliga bokförda försäljningsfakturan.

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


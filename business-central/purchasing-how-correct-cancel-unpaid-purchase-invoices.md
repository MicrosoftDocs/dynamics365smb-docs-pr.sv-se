---
title: "Korrigera eller annullera obetalda inköpsfakturor | Microsoft Docs"
description: "Förklarar hur du kan korrigera, avbryta eller ångra en bokförd inköpsfaktura eller skapa en inköpskreditnota automatiskt."
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
ms.openlocfilehash: 2ed3520b3724f9703fca128a2d20c28183795a93
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Korrigera eller annullera obetalda inköpsfakturor
Du kan korrigera eller annullera en bokförd inköpsfaktura. Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen.

Om du redan har betalt för produkter på den bokförda inköpsfakturan kan du inte rätta eller annullera den från själva den bokförda inköpsfakturan. I stället måste du skapa en inköpskreditnota manuellt för att återföra inköpet, alternaivt hanterat med en inköpsreturorder. Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

I fönstret **Bokförd inköpsfaktura** kan du välja knappen **Korrigera** eller knappen **Avbryt**. När du uppdaterar eller avbryter en bokförd inköpsfaktura gäller den korrigerande inköpskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga inköpsfakturan bokfördes. Det återför den bokförda inköpsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av inköpskreditnota för din verifieringskedja. I det följande beskrivs användningen av **Korrigera** och **Avbryt**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Korrigera en bokförd inköpsfaktura
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.  
2. Markera den bokförda inköpsfakturan som du vill korrigera.  

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte rätta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.
3. I fönstret **Bokförd inköpsfaktura** väljer du **korrigera**.

    En ny inköpsfaktura med samma information skapas där du kan göra rättningen. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md). Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.

    En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.
4. Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Avbryta en bokförd inköpsfaktura
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.  
2. Markera den bokförda inköpsfakturan som du vill annullera.

    > [!NOTE]  
    >   Om kryssrutan **Avbruten** kan du inte avbryta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.
3. I fönstret **Bokförd inköpsfaktura** väljer du **avbryt**.

    En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan. Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.
4. Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


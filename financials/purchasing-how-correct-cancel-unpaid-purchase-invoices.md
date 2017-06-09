---
title: "Så här korrigerar eller annullerar du obetalda inköpsfakturor | Microsoft Docs"
description: "Så här rättare eller makulerar du obetalda inköpsfakturor"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Så här rättare eller makulerar du obetalda inköpsfakturor
Du kan korrigera eller annullera en bokförd inköpsfaktura. Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen.

Om du redan har betalt för produkter på den bokförda inköpsfakturan kan du inte rätta eller annullera den från själva den bokförda inköpsfakturan. I stället måste du manuellt skapa en inköpskreditnota för att återföra köpet. Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

I fönstret **Bokförd inköpsfaktura** kan du välja knappen **Korrigera** eller knappen **Avbryt**. När du uppdaterar eller avbryter en bokförd inköpsfaktura gäller den korrigerande inköpskreditnotan för alla redovisnings- och inventeringstransaktioner som skapades när den ursprungliga inköpsfakturan bokfördes. Det återför den bokförda inköpsfakturan i dina ekonomiska transaktioner och lämnar bokförd korrigering av inköpskreditnota för din verifieringskedja. I det följande beskrivs användningen av **Korrigera** och **Avbryt**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Korrigera en bokförd inköpsfaktura
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bokförda inköpsfakturor**, och välj sedan relaterad länk.  
2. Markera den bokförda inköpsfakturan som du vill korrigera.  

    **Obs!** Om kryssrutan **Avbruten** är markerad, kan du inte rätta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.
3. I fönstret **Bokförd inköpsfaktura** väljer du **korrigera**.

    En ny inköpsfaktura med samma information skapas där du kan göra rättningen. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md). Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.

    En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan.
4. Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Avbryta en bokförd inköpsfaktura
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bokförda inköpsfakturor**, och välj sedan relaterad länk.  
2. Markera den bokförda inköpsfakturan som du vill annullera.

    **Obs!** Om kryssrutan **Avbruten** är markerad, kan du inte avbryta den bokförda inköpsfakturan, eftersom den redan har korrigerats eller annullerats.
3. I fönstret **Bokförd inköpsfaktura** väljer du **avbryt**.

    En inköpskreditnota skapas automatiskt och bokförs för att annullera den ursprungligt bokförda inköpsfakturan. Fältet **Avbruten** på den först bokförda inköpsfakturan ändras till **Ja**.
4. Välj **Visa korrigerande kreditnota** för att visa de bokförda inköpskreditnotorna som annullerar den ursprungliga bokförda inköpsfakturan.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Så här registrerar du inköp](purchasing-how-record-purchases.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


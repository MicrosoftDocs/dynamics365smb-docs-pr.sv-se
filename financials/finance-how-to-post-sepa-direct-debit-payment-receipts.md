---
title: "Bokför betalningar för SEPA direktdebitering | Microsoft Docs"
description: "När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 021c48efc6bf6b1fdb7b17bf742cb6f084d3964b
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a>Så här bokför du betalningsinleveranser för SEPA Autogiro
När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna. För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Du kan bokföra Betalningsinleverans direkt från den **Samlingar med autogiro** eller **Transaktioner för samlingar med autogiro**. Alternativt kan du vidarebefordra arbetet till en annan användare genom att förbereda de relaterade journalraderna.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Så här bokför du ett betalningskvitto för autogiroinsamling  
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Autogiroinsamlingar**, och välj sedan relaterad länk.  
2. Välj en rad för en autogiroinsamling som har exporterats till en bankfil och framgångsrikt bearbetats av banken. För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Välj åtgärden **Bokför betalningsinleveranser**.  
4. I fönstret **Bokför samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Autogirosamlingsnr.**|Ange autogiroinsamlingen som du vill bokföra betalningskvittot för.|  
    |**Redovisningsjournalmall**|Ange vilken redovisningsjournalmallen som ska användas för att bokföra betalningskvitto, t.ex. mall för inbetalningar.|  
    |**Redovisningsjournalnamn**|Ange vilka redovisningsjournalbatch som ska användas för att bokföra ett betalningskvitto.|  
    |**Skapa enbart journal**|Markera den här kryssrutan om du inte vill bokföra betalningskvittot när du väljer **OK** knappen. Betalningskvittot skall förberedas i den angivna journalen och bokförs inte förrän någon bokför journalraderna i fråga.|  

5. Välj knappen **OK**.  

## <a name="see-also"></a>Se även  
 [Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)   
 [Försäljning](sales-manage-sales.md)


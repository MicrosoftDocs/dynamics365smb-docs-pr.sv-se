---
title: "Bokför betalningar för SEPA direktdebitering | Microsoft Docs"
description: "När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ee07ca7ba498858fac794f1ee1f27f281de8ae02
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a>Så här bokför du betalningsinleveranser för SEPA Autogiro
När en direkt autogiroinsamling framgångsrikt bearbetas av din bank, kan du fortsätta att bokföra mottagandet av betalningen för de berörda försäljningsfakturorna. För mer information, se [Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Du kan bokföra Betalningsinleverans direkt från den **Samlingar med autogiro** eller **Transaktioner för samlingar med autogiro**. Alternativt kan du vidarebefordra arbetet till en annan användare genom att förbereda de relaterade journalraderna.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Så här bokför du ett betalningskvitto för autogiroinsamling  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Samlingar med autogiro** och välj sedan relaterad länk.  
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


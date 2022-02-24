---
title: Förstå hur du bokför inköpsdokument | Microsoft Docs
description: Lära dig olika bokföringsfunktioner för att bokföra inköpsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 01/17/2020
ms.author: sgroespe
ms.openlocfilehash: 2565133adfab4fb5f6febeeccb69c4f3d6f59e71
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991886"
---
# <a name="posting-purchases"></a>Bokföra inköp
I **Bokföringsgrupp** i ett inköpsdokument kan du välja mellan följande bokföringsfunktioner:

* **Bokföra**
* **Förhandsgranska bokföring**
* **Bokför och skriv ut**
* **Testa rapport**
* **Bokför batch-jobb**

När du har fyllt i alla raderna och skrivit in all information på inköpsordern kan du bokföra den, d.v.s. skapa en inleverans och en faktura.

När en inköpsorder bokförs, uppdateras leverantörens konto, redovisningen och artikeltransaktionerna.

För varje inköpsorder skapas en inköpstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på leverantörens konto i tabellen **Lev.reskontratransaktion** och en redovisningstransaktion på det relevanta kontot för leverantörsskulder. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Om rabattransaktionen är bokförd eller ej beror på innehållet i fältet **Rabattbokföring** på sidan **Inköpsinställningar**.

För varje inköpsorderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om inköpsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om inköpsraden innehåller ett redovisningskonto). Dessutom registreras inköpsorder alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**.

Innan du börjar bokföra kan du välja att skriva ut en testrapport som visar all information på inköpsordern tillsammans med eventuella fel. Om du vill skriva ut rapporten väljer du **Bokföring** och sedan **Testrapport**.

> [!IMPORTANT]  
>   När du bokför en order kan du skapa både en inleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delinleverans och en delfaktura genom att fylla i fältet **Ant. att inlevereras** och **Ant. att fakturera** på de enskilda inköpsorderraderna innan du bokför. Observera att du inte kan skapa en faktura för något som inte har inlevererats. Innan du kan fakturera måste du således ha registrerat en inleverans alternativt välja att inleverera och fakturera samtidigt.

Du kan bokföra eller bokföra och skriva ut. Om du väljer Bokför och Skriv ut, skrivs en rapport ut när ordern bokförs. Du kan även välja funktionen **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Mer information finns i [Bokföra flera dokument på samma gång](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visa reskontratransaktioner
När bokföringen är slutförd tas de bokförda inköpsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Sedan kan du se de bokförda transaktionerna på de olika sidor som innehåller bokförda transaktioner, t.ex. sidorna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktioner**, **Inleverans** och **Bokförda inköpsfakturor**.

I de flesta fall kan du öppna reskontratransaktioner från det berörda kortet eller dokumentet. Välj till exempel åtgärden **Transaktioner** på sidan **Leverantörskort**.

## <a name="editing-ledger-entries"></a>Redigera reskontratransaktioner
Du kan redigera vissa fält i bokförda inköpsdokument, till exempel fältet **Betalningsreferens**. Mer information finns i [Redigera bokförda dokument](across-edit-posted-document.md). För mer kritiska fält som påverkar granskningsspåret måste du återföra eller ångra bokföring. Mer information finns i [återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md). 

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Se även
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Bokföra flera dokument på samma gång](ui-batch-posting.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

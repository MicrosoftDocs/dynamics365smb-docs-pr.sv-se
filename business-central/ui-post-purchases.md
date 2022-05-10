---
title: Dokument efter köp
description: Lära dig olika bokföringsfunktioner för att bokföra inköpsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: ebf6c4c1a14bf14ed21a8661c14235efbee4a190
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655313"
---
# <a name="posting-purchases"></a>Bokföra inköp
I ett inköpsdokument kan du välja mellan följande bokföringsåtgärder:

* **Bokföra**
* **Förhandsgranska bokföring**
* **Bokför och skriv ut**
* **Testa rapport**
* **Bokför batch-jobb**

När ett inköpdokument bokförs uppdateras leverantörens konto, redovisningen, artikeltransaktionstransaktionerna samt resurstransaktionstransaktionerna.

För respektive inköpsdokument skapas en inköpstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på leverantörens konto i tabellen **Lev.reskontratransaktion** och en redovisningstransaktion på det relevanta kontot för leverantörsskulder. Dessutom kan bokföring av inköpet resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Om rabattransaktionen är bokförd eller ej beror på innehållet i fältet **Rabattbokföring** på sidan **Inköpsinställningar**.

För varje inköpsrad skapas följande transaktioner:
- En transaktion i tabellen **Artikeltransaktion** om inköpsraden är av typen **Artikel**.
- En transaktion i tabellen **Redovisningstransaktion** om inköpsraderna är av typen **Redovisningskonto**
- En transaktion i tabellen **Resurstransaktion** om inköpsraden är av typen **Resurs**.

Dessutom registreras inköpsdokument alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**.

Innan du börjar bokföra kan du välja att skriva ut en testrapport som visar all information på inköpsordern tillsammans med eventuella fel. Om du vill skriva ut rapporten väljer du **Bokföring** och sedan **Testrapport**.

> [!IMPORTANT]  
>   När du bokför en inköpsorder för artiklar kan du skapa både en inleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delinleverans och en delfaktura genom att fylla i fältet **Ant. att inlevereras** och **Ant. att fakturera** på de enskilda inköpsorderraderna innan du bokför. Observera att du inte kan skapa en faktura för något som inte har inlevererats. Innan du kan fakturera måste du således ha registrerat en inleverans alternativt välja att inleverera och fakturera samtidigt.

Du kan bokföra eller bokföra och skriva ut. Om du väljer Bokför och Skriv ut, skrivs en rapport ut när ordern bokförs. Du kan även välja funktionen **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Mer information finns i [Bokföra flera dokument på samma gång](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visa reskontratransaktioner
När bokföringen är slutförd tas de bokförda inköpsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Du kan därefter se bokförda transaktioner på de sidor som innehåller bokförda transaktioner, exempelvis sidorna **Lev.reskontratransaktioner**, **Redovisningstransaktioner**, **Artikeltransaktioner**, **resurstransaktioner**, **Inköpsleveranser** samt **Bokförda inköpsfakturor**.

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
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
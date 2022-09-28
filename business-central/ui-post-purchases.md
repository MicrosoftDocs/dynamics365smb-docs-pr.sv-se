---
title: Dokument efter köp
description: Lära dig olika sätt att bokföra inköpsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 1bae22c83f1e7138fbfe16bb39aea3ad9d65d788
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531006"
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

För varje inköpsrad, som tillämpligt, skapas poster i:

* Tabellen **Artikeltransaktion** om inköpsraden är av typen **Artikel**.
* Tabellen **Redovisningstransaktion** om inköpsraderna är av typen **Redovisningskonto**.
* Tabellen **Resurstransaktion** om inköpsraden är av typen **Resurs**.

Dessutom registreras inköpsdokument alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**.

Innan du börjar bokföra kan du välja att skriva ut en testrapport som visar all information på inköpsordern tillsammans med eventuella fel. Om du vill skriva ut rapporten väljer du **Bokföring** och sedan **Testrapport**.

> [!IMPORTANT]  
> När du bokför en inköpsorder för artiklar kan du skapa både en inleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delinleverans och en delfaktura genom att fylla i fältet **Ant. att inlevereras** och **Ant. att fakturera** på de enskilda inköpsorderraderna innan du bokför. Observera att du inte kan skapa en inköpsfaktura från en inköpsorder för produkter eller tjänster som inte har tagits emot. Innan du kan fakturera måste du således ha registrerat en inleverans alternativt välja att inleverera och fakturera samtidigt.
>
> Om du vill bokföra en inköpsfaktura utan att registrera en inleverans i sidan [!INCLUDE[prod_short](includes/prod_short.md)] skapar du dokumentet på **inköpsfakturor**. Läs mer i [Registrera inköp med inköpsfakturor](purchasing-how-record-purchases.md).

Du kan bokföra eller bokföra och skriva ut. Om du väljer Bokför och Skriv ut, skrivs en rapport ut när ordern bokförs. Du kan även välja åtgärden **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Läs mer på [Bokföra flera dokument på samma gång](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visa reskontratransaktioner

När bokföringen är slutförd tas de bokförda inköpsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Du kan därefter se bokförda transaktioner på de sidor som innehåller bokförda transaktioner, inklusive sidorna **Lev.reskontratransaktioner**, **Redovisningstransaktioner**, **Artikeltransaktioner**, **resurstransaktioner**, **Inköpsleveranser** samt **Bokförda inköpsfakturor**.

I de flesta fall kan du öppna reskontratransaktioner från det berörda kortet eller dokumentet. Välj till exempel åtgärden **Transaktioner** på sidan **Leverantörskort**.

## <a name="editing-ledger-entries"></a>Redigera reskontratransaktioner

Du kan redigera vissa fält i bokförda inköpsdokument, till exempel fältet **Betalningsreferens**. Mer information finns i [Redigera bokförda dokument](across-edit-posted-document.md). För mer kritiska fält som påverkar granskningsspåret måste du återföra eller ångra bokföring. Läs mer på [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Se även

[Redigera bokförda dokument](across-edit-posted-document.md)  
[Bokföra flera dokument på samma gång](ui-batch-posting.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

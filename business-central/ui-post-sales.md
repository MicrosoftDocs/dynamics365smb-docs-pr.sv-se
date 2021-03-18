---
title: Bokföra försäljningsdokument | Microsoft Docs
description: Lära dig olika bokföringsfunktioner för att bokföra försäljningsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: e0d1bd7770eb3bb44a2e9b3203ffa158a246cfa9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392055"
---
# <a name="posting-sales"></a>Bokföra försäljning

Under menyn **Bokföring** i ett försäljningsdokument kan du välja mellan följande bokföringsfunktioner:

* **Bokföra**
* **Bokför och nytt**
* **Bokför och skicka**
* **Förhandsgranska bokföring**
* **Bokför batch-jobb**
* **Testa rapport**

> [!OBS] För försäljningsorder kan du även visa alternativ som är relaterade till funktionen för förskottsbetalning. Mer information finns i [Fakturera förskottsbetalningar](finance-invoice-prepayments.md). 

När du har fyllt i alla raderna och skrivit in all information på försäljningsordern kan du bokföra den. Här skapas en leverans och en faktura.

När en försäljningsorder bokförs, uppdateras kundens konto, redovisningen och artikeltransaktionerna.

För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Huruvida rabattransaktionen bokförs eller inte beror på innehållet i fältet **Rabattbokföring** på sidan **Försäljningsinställningar**.

För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto). Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.

> [!IMPORTANT]  
> När du bokför en order kan du skapa både en utleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delutleverans och en delfaktura genom att fylla i fältet **Ant. att utleverera** och **Ant. att fakturera** på de enskilda försäljningsorderraderna innan du bokför. Observera att du inte kan skapa en faktura för något som inte har utlevererats. D.v.s. innan du kan fakturera måste du ha registrerat en leverans alternativt välja att leverera och fakturera samtidigt.

Du kan antingen bokföra eller bokföra och skicka. Om du väljer att bokföra och skicka, skapas en PDF-fil som du sedan kan skicka. Du kan även välja funktionen **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Mer information finns i [Bokföra flera dokument på samma gång](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Visa reskontratransaktioner

När bokföringen är slutförd tas de bokförda försäljningsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Sedan kan du se de bokförda transaktionerna på de olika sidorna som innehåller bokförda transaktioner, t. ex. sidorna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktion**, **Bokförda försäljningsutleveranser** och **Bokförda försäljningsfakturor**.  

I de flesta fall kan du öppna reskontratransaktioner från det berörda kortet eller dokumentet. Välj till exempel åtgärden **Reskontratransaktioner** på sidan **Kundkort**.

## <a name="editing-ledger-entries"></a>Redigera reskontratransaktioner

Du kan redigera vissa fält i bokförda inköpsdokument, till exempel fältet **Godsupplysningsnr**. . Mer information finns i [Redigera bokförda dokument](across-edit-posted-document.md). För mer kritiska fält som påverkar granskningsspåret måste du återföra eller ångra bokföring. Mer information finns i [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Bokföra flera dokument på samma gång](ui-batch-posting.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Korrigera eller makulera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
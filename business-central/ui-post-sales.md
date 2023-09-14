---
title: Bokföra försäljningsdokument
description: Lära dig olika bokföringsfunktioner för att bokföra försäljningsdokument och hur du kan uppdatera bokförda dokument.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Bokföra försäljning

Under menyn **Bokföring** i ett försäljningsdokument kan du välja mellan följande bokföringsfunktioner:

* **Bokföra**
* **Bokför och nytt**
* **Bokför och skicka**
* **Förhandsgranska bokföring**
* **Bokför batch-jobb**
* **Testa rapport**

> [!NOTE]
> För försäljningsorder kan du även visa alternativ som är relaterade till funktionen för förskottsbetalning. Mer information finns i [Fakturera förskottsbetalningar](finance-invoice-prepayments.md).

När du har fyllt i alla raderna och skrivit in all information på försäljningsordern kan du bokföra den. Här skapas en leverans och en faktura.

När en försäljningsorder bokförs, uppdateras kundens konto, redovisningen och artikeltransaktionerna.

För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Huruvida rabattransaktionen bokförs eller inte beror på innehållet i fältet **Rabattbokföring** på sidan **Försäljningsinställningar**.

För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto). Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Du kan antingen bokföra eller bokföra och skicka. Om du väljer att bokföra och skicka, skapas en PDF-fil som du sedan kan skicka. Du kan även välja funktionen **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Mer information finns i [Bokföra flera dokument på samma gång](ui-batch-posting.md).

## Visa reskontratransaktioner

När bokföringen är slutförd tas de bokförda försäljningsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Sedan kan du se de bokförda transaktionerna på de olika sidorna som innehåller bokförda transaktioner, t. ex. sidorna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktion**, **Bokförda försäljningsutleveranser** och **Bokförda försäljningsfakturor**.  

I de flesta fall kan du öppna reskontratransaktioner från det berörda kortet eller dokumentet. Välj till exempel åtgärden **Reskontratransaktioner** på sidan **Kundkort**.

## Redigera reskontratransaktioner

Du kan redigera vissa fält i bokförda inköpsdokument, till exempel fältet **Godsupplysningsnr**. . Mer information finns i [Redigera bokförda dokument](across-edit-posted-document.md). För mer kritiska fält som påverkar granskningsspåret måste du återföra eller ångra bokföring. Mer information finns i [Återföra journalbokningar och ångra inleveranser/utleveranser](finance-how-reverse-journal-posting.md).

## Se relaterad [Microsoft utbildning](/training/modules/ship-invoice-items-dynamics-365-business-central/index)

## Se även

[Försäljning](sales-manage-sales.md)  
[Bokföra flera dokument på samma gång](ui-batch-posting.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Korrigera eller makulera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  

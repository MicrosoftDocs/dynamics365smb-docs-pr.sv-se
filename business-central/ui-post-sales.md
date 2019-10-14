---
title: Bokföra försäljningsdokument | Microsoft Docs
description: Lära dig olika bokföringsfunktioner för att bokföra försäljningsdokument och hur du kan uppdatera bokförda dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c389a93a71b251b5b0e11f4450251fdf68b64345
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310786"
---
# <a name="posting-sales"></a>Bokföra försäljning
Under menyn **Bokföring** i ett försäljningsdokument kan du välja mellan följande bokföringsfunktioner:

* **Bokföra**
* **Bokför och nytt**
* **Bokför och skicka**
* **Förhandsgranska bokföring**
* **Fakturautkast**
* **Proformafaktura**
* **Testa rapport**

När du har fyllt i alla raderna och skrivit in all information på försäljningsordern kan du bokföra den. Här skapas en leverans och en faktura.

När en försäljningsorder bokförs, uppdateras kundens konto, redovisningen och artikeltransaktionerna.

För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Huruvida rabattransaktionen bokförs eller inte beror på innehållet i fältet **Rabattbokföring** på sidan **Försäljningsinställningar**.

För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto). Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.

> [!IMPORTANT]  
>   När du bokför en order kan du skapa både en utleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delutleverans och en delfaktura genom att fylla i fältet **Ant. att utleverera** och **Ant. att fakturera** på de enskilda försäljningsorderraderna innan du bokför. Observera att du inte kan skapa en faktura för något som inte har utlevererats. D.v.s. innan du kan fakturera måste du ha registrerat en leverans alternativt välja att leverera och fakturera samtidigt.

Du kan bokföra eller bokföra och skriva ut. Om du väljer Bokför och Skriv ut, skrivs en rapport ut när ordern bokförs. Du kan även välja funktionen **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt. Mer information finns i [Bokföra flera dokument på samma gång](ui-batch-posting.md).

När bokföringen är slutförd tas de bokförda försäljningsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Sedan kan du se de bokförda transaktionerna på de olika sidorna som innehåller bokförda transaktioner, t.ex. sidorna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktion**, **Bokförda försäljningsutleveranser** och **Bokförda försäljningsfakturor**.  

Du kan redigera vissa fält i bokförda försäljningsdokument, till exempel fältet **Godsupplysningsnr**. . Mer information finns i [Redigera bokförda dokument](across-edit-posted-document.md).

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Bokföra flera dokument på samma gång](ui-batch-posting.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Korrigera eller makulera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

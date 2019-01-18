---
title: "Förstå hur du bokför försäljningsdokument | Microsoft Docs"
description: "Få mer information om de olika bokföringsfunktionerna för att bokföra försäljningsdokument."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="posting-sales"></a>Bokföra försäljning
I **Bokföringsgrupp** i ett försäljningsdokument kan du välja mellan följande bokföringsfunktioner:

* **Bokföra**
* **Testa rapport**
* **Bokför och skicka**
* **Bokför och skriv ut**
* **Bokför och e-posta**
* **Bokför batch-jobb**
* **Förhandsgranska bokföring**

När du har fyllt i alla raderna och skrivit in all information på försäljningsordern kan du bokföra den. Här skapas en leverans och en faktura.

När en försäljningsorder bokförs, uppdateras kundens konto, redovisningen och artikeltransaktionerna.

För varje försäljningsorder skapas en försäljningstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på kundens konto i tabellen **Kundreskontra** och en redovisningstransaktion på det relevanta kontot för leverantörsreskontra. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Huruvida rabattransaktionen bokförs eller inte beror på innehållet i fältet **Rabattbokföring** på sidan **Försäljningsinställningar**.

För varje orderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om försäljningsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om försäljningsraden innehåller ett redovisningskonto). Därutöver registreras order alltid i tabellerna **Utleveranshuvud** och **Försäljningsfakturahuvud**.

> [!IMPORTANT]  
>   När du bokför en order kan du skapa både en utleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delutleverans och en delfaktura genom att fylla i fältet **Ant. att utleverera** och **Ant. att fakturera** på de enskilda försäljningsorderraderna innan du bokför. Observera att du inte kan skapa en faktura för något som inte har utlevererats. D.v.s. innan du kan fakturera måste du ha registrerat en leverans alternativt välja att leverera och fakturera samtidigt.

När bokföringen är slutförd tas de bokförda försäljningsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Sedan kan du se de bokförda transaktionerna på de olika sidorna som innehåller bokförda transaktioner, t.ex. sidorna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktion**, **Bokförda försäljningsutleveranser** och **Bokförda försäljningsfakturor**.

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)



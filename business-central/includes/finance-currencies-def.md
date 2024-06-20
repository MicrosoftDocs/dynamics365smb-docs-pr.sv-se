---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Du måste skapa en kod för varje valuta du använder om du:

- Köper eller säljer i andra valutor förutom den lokala valutan (BVA).  
- Registrerar redovisningstransaktioner i både BVA och en alternativ rapporteringsvaluta.  

När du har skapat koderna tilldelar du lämplig kod till respektive bankkonto för utländsk valuta, och tilldelar en standardvalutakod till de utländska kund- och leverantörskontona.

Du anger valutakoder i listan **Valutor**, inklusive extra information och inställningar som behövs för respektive valutakod.

> [!TIP]
> Skapa valutor med den internationella ISO-koden som kod för att förenkla arbetet med valutan i framtiden.

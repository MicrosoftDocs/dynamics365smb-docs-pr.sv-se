---
title: "Bokföra inköp | Microsoft Docs"
description: "Lär dig mer om hur du bokför inköp."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2016
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ac79d81aba2fb86a2c4a95356e8a621e5f5813ea
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


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

För varje inköpsorder skapas en inköpstransaktion i tabellen **Redovisningstransaktion**. Dessutom skapas en transaktion på leverantörens konto i tabellen **Lev.reskontratransaktion** och en redovisningstransaktion på det relevanta kontot för leverantörsskulder. Dessutom kan bokföring av inköpsordern resultera i en momstransaktion och en redovisningstransaktion för rabattbeloppet. Om rabattransaktionen är bokförd eller ej beror på innehållet i fältet **Rabattbokföring** i fönstret **Inköpsinställning**.

För varje inköpsorderrad skapas en artikeltransaktion i tabellen **Artikeltransaktion** (om inköpsraden innehåller artikelnummer) eller en redovisningstransaktion i tabellen **Redovisningstransaktion** (om inköpsraden innehåller ett redovisningskonto). Dessutom registreras inköpsorder alltid i tabellerna **Inleveranshuvud** och **Inköpsfakturahuvud**.

Innan du börjar bokföra kan du välja att skriva ut en testrapport som visar all information på inköpsordern tillsammans med eventuella fel. Om du vill skriva ut rapporten väljer du **Bokföring** och sedan **Testrapport**.

**Viktigt!** När du bokför en order kan du skapa både en inleverans och en faktura. Detta kan göras samtidigt eller oberoende av varandra. Du kan också skapa en delinleverans och en delfaktura genom att fylla i fältet **Ant. att inlevereras** och **Ant. att fakturera** på de enskilda inköpsorderraderna innan du bokför. Observera att du inte kan skapa en faktura för något som inte har inlevererats. Innan du kan fakturera måste du således ha registrerat en inleverans alternativt välja att inleverera och fakturera samtidigt.

Du kan bokföra eller bokföra och skriva ut. Om du väljer Bokför och Skriv ut, skrivs en rapport ut när ordern bokförs. Du kan även välja funktionen **Bokför batch-jobb** som ger dig möjlighet att bokföra fler fakturor samtidigt.

När bokföringen är slutförd tas de bokförda inköpsraderna bort från ordern. Du får ett meddelande när bokföringen är slutförd. Sedan kan du se de bokförda transaktionerna i de olika fönster som innehåller bokförda transaktioner, t.ex. fönsterna **Leverantörsreskontratransaktion**, **Redovisningstransaktion**, **Artikeltransaktioner**, **Inleverans** och **Bokförda inköpsfakturor**.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)



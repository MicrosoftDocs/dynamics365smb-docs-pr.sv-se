---
title: Så här begränsar och tillåter du användning av en post | Microsoft Docs
description: Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbb22a00e878e8c4d75cb5fcdbcc27a28d9d22a4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783997"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begränsa och tillåt användningen av en post
Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten. Ett arbetsflödessvar ska begränsa användningen av posten enligt definitionen i arbetsflödeshändelsen och villkoren. Ett annat arbetsflödessvar ska tillåta användning av posten enligt definitionen i arbetsflödeshändelsen och villkoren. Två svar finns i den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] för detta ändamål: **Tillåt användning av en post** och **tillåt användningen av en post.**.

> [!NOTE]  
>  Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder stöd för att begränsa en post från att bokföras, från att exporteras som en utbetalning och från att skrivas ut som en check. För att stödja andra begränsningar måste en Microsoft-partner anpassa programkoden.  

> [!NOTE]  
>  Arbetsflödesfunktionen för att begränsa och tillåta poster att användas är inte relaterad till funktionen att spärra artikel-, kund- och leverantörsposter från att bokföras.

Följande procedur beskriver hur du begränsar inköpsorder från att bokföras tills de har godkänts. Det nya arbetsflödet baseras på det befintliga arbetsflödesmallen Arbetsflöde för godkännande av inköpsfaktura.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Så här skapar du ett arbetsflödessteg som begränsar bokföring av icke godkända inköpsorder  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Arbetsflöden** och välj sedan relaterad länk.  
2. På sidan **Arbetsflöden** skapar du ett nytt arbetsflöde som kallas Arbetsflöde för godkännande av inköpsfaktura. Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).  
3. Välj åtgärden **Kopiera från arbetsflödesmallen**.  
4. Välj fältet **Källarbetsflödekod** och välj sedan på sidan **arbetsflödesmallen**, välj arbetsflödesmallen Arbetsflöde för godkännande av inköpsfaktura.  

     Lägg märke till att de första två arbetsflödesstegen är om du vill begränsa och sedan tillåta användning av inköpsfakturor. Fortsätt genom att ändra händelsevillkoret i det första steget i det nya arbetsflödet för att ange att det gäller inköpsorder.  
5. På snabbfliken **Arbetsflödessteg** väljer du fältet **Händelsevillkor** och sedan för filtret **Dokumenttyp**, välj **Order**.  
6. Fortsätt med att redigera, ta bort eller lägga till andra arbetsflödessteg så att de passar en affärsprocess som börjar med att begränsa så att icke godkända inköpsorder bokförs.  

## <a name="see-also"></a>Se även  
[Skapa arbetsflöden](across-how-to-create-workflows.md)   
[Arbetsflöde](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
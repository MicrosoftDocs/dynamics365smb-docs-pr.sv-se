---
title: "Avancerad: Bästa prisberäkningen | Microsoft Docs"
description: "Beskriver hur användning av särskilda priser och radrabatter innebär att din vinst på handel alltid är optimalt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: pricing, sales price
ms.date: 02/08/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e4dbe800abef3fa4afe3eabec3450b6ee0f20080
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="advanced-best-price-calculation"></a>Avancerad: Bästa prisberäkning
När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader.

Det bästa priset är det lägsta tillåtna priset med den högsta tillåtna radrabatten för ett visst datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar automatiskt detta när du skriver in enhetspriset och radrabattens procentsats för artiklar på nytt dokument och journalrader.

**Obs!** Följande beskriver hur det bästa priset beräknas för försäljning. Beräkningen är samma för inköp.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande kriterier:

    - Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    - Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    - Ligger orderdatumet (eller fakturans och kreditnotans bokföringsdatum) inom avtalet om priser eller radrabatter?
    - Har någon enhetskod angetts? I så fall gör [!INCLUDE[d365fin](includes/d365fin_md.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolelrar om pris/rabattavtal tillämpas på uppgifter i dokumentet eller journalen och infogar det tillämpliga enhetspriset och radrabattens procentsats enligt följande kriterier:

    - Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    - Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i BVA. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[d365fin](includes/d365fin_md.md)] det lägsta priset och den högsta radrabatten i BVA.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="see-also"></a>Se även
[Så här registrerar du speciella försäljningspriser och rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  
[Så här registrerar du speciella inköpspriser och rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


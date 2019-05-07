---
title: Betalningsavstämning med tillägget Envestnet Yodlee Bank Feeds | Microsoft Docs
description: Beskriver tillägget Envestnet Yodlee Bank Feeds, som länkar till bankkonton så att du kan stämma av betalningar snabbt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53ee8bb7ee798c473e1053ea8413be28f9185d1b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "911725"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Tillägget Envestnet Yodlee bankfeeder
För att snabbt avstämma utbetalningar som gjorts till dina bankkonton, låter dig Envestnet Yodlee bankfeeder länka ditt systembankkonto till ditt onlinebankkonto. Det betyder att det senaste kontoutdraget automatiskt eller manuellt matas in i din avstämningsjournal och ser till att du alltid behandlar de senaste utbetalningarna med minsta risk för fel.

> [!NOTE]
> Funktionen stöds bara i online-versionen av Business Central. Om du vill använda den här funktionen på plats, måste du skaffa ett cobrand-konto från Envestnet Yodlee.

Tjänsten Envestnet Yodlee bankfeeder ger följande förmåner:

* Tar bort behovet av manuell inmatning.
* Förbättrar effektivitet och ökar noggrannheten när du gör betalningsavstämning.
* Stöder ett stort antal banker.
* Tillåter aktuell information om banktransaktioner inifrån [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Stöder manuella samt automatiska bankfeeder.
* Aktiverar utkontraktering av utbetalningxavstämning till en revisor genom att ge åtkomst till kontoutdrag.

Mer information finns i [Konfigurera du bankfeedtjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Se även
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)    
[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

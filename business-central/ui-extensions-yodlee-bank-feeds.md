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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315354"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Tillägget Envestnet Yodlee Bank Feeds
För att snabbt avstämma utbetalningar som gjorts till dina bankkonton, låter dig Envestnet Yodlee Bank Feeds länka ditt systembankkonto till ditt onlinebankkonto. Det betyder att det senaste kontoutdraget automatiskt eller manuellt matas in i din avstämningsjournal och ser till att du alltid behandlar de senaste utbetalningarna med minsta risk för fel.

Tjänsten Envestnet Yodlee Bank Feeds stöds bara i USA och Kanada.

> [!NOTE]
> Funktionen stöds bara i online-versionen av Business Central. Om du vill använda den här funktionen på plats, måste du skaffa ett cobrand-konto från Envestnet Yodlee.<br /><br />

> [!IMPORTANT]
> På grund av det nya direktivet om betalningstjänster i Europa (PSD2), efter den 14 september 2019, kan du inte längre automatiskt importera bankutdrag från banker i Storbritannien till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vi undersöker möjligheten att erbjuda denna funktion igen i framtiden.

Tjänsten Envestnet Yodlee Bank Feeds ger följande fördelar:

* Tar bort behovet av manuell inmatning.
* Förbättrar effektivitet och ökar noggrannheten när du gör betalningsavstämning.
* Stöder ett stort antal banker.
* Tillåter aktuell information om banktransaktioner inifrån [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Stöder manuella samt automatiska bankfeeder.
* Aktiverar utkontraktering av utbetalningxavstämning till en revisor genom att ge åtkomst till kontoutdrag.

Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Se även
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)    
[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

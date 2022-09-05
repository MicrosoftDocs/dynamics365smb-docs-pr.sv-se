---
title: Betalningsavstämning med tillägget Envestnet Yodlee Bank Feeds
description: Beskriver tillägget Envestnet Yodlee Bank Feeds, som länkar till bankkonton så att du kan stämma av betalningar snabbt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.search.form: 1450, 1451, 1452, 1453, 1454, 1458, 1460,
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1e2c1b1b9030033ec35c79e478d0d5bd5246b3d6
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362001"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Tillägget Envestnet Yodlee Bank Feeds

För att snabbt avstämma utbetalningar som gjorts till dina bankkonton, låter dig Envestnet Yodlee Bank Feeds länka ditt systembankkonto till ditt onlinebankkonto. Det betyder att det senaste kontoutdraget automatiskt eller manuellt matas in i din avstämningsjournal och ser till att du alltid behandlar de senaste utbetalningarna med minsta risk för fel.

Tjänsten Envestnet Yodlee Bank Feeds stöds bara i USA och Kanada.

> [!NOTE]
> Funktionen Envestnet Yodlee Bank Feeds stöds bara i online-versionen av Business Central. Om du vill använda den här funktionen på plats, måste du skaffa ett cobrand-konto från Envestnet Yodlee.<br /><br />
> Tjänsten Envestnet Yodlee Bank Feeds stöds bara i USA och Kanada.
> Endast banker som finns i dessa länder stöds även om banker från andra länder kan visas i bankvalsfönstret Envestnet Yodlee Bank Feeds i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> På grund av det nya direktivet om betalningstjänster i Europa (PSD2), efter den 14 september 2019, kan du inte längre automatiskt importera bankutdrag från banker i Storbritannien till [!INCLUDE[prod_short](includes/prod_short.md)]. Vi undersöker möjligheten att erbjuda denna funktion igen i framtiden.

Tjänsten Envestnet Yodlee Bank Feeds ger följande fördelar:

* Tar bort behovet av manuell inmatning.
* Förbättrar effektivitet och ökar noggrannheten när du gör betalningsavstämning.
* Stöder ett stort antal banker.
* Tillåter aktuell information om banktransaktioner inifrån [!INCLUDE[prod_short](includes/prod_short.md)].
* Stöder manuella samt automatiska bankfeeder.
* Aktiverar utkontraktering av utbetalningxavstämning till en revisor genom att ge åtkomst till kontoutdrag.

## <a name="available-bank-feeds"></a>Tillgängliga bankflöden

Du kan kontrollera om en bank stöds genom att ställa in och ansluta till tjänsten Envestnet Yodlee Bank Feeds. Banken kommer att visas i listan om den stöds av Envestnet Yodlee.

Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Se även

[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg ](ui-extensions.md)  
[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

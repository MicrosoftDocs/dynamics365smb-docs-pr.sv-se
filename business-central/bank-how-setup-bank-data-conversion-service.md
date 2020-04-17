---
title: Så här skapar du bankdatakonvertering | Microsoft Docs
description: Du kan ställa in bankkonton för att följa upp transaktioner och importera eller exportera bankfeeder, till exempel Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e222e133313147cecd94c8cb7f2644776ee1034a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186266"
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Konfigurera tillägget AMC Banking 365 Fundamentals
En global tjänstleverantör för att konvertera betalningsinformation till alla dataformat som din bank kräver är ansluten och redo att aktiveras i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Detta kallas [!INCLUDE[d365fin](includes/d365fin_md.md)] för tillägget AMC Banking 365 Fundamentals.

Du kan exportera betalningsrader från sidan **Utbetalningsjournal** till en en fil eller en dataström som du sedan överför till din bank för automatisk behandling, så att du inte behöver göra electroniska betalningar individuellt. Mer information finns i [Så här exporterar du betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Du kan importera bankutdragsfiler på sidan **Betalningsavstämningsjournal** med hjälp av tillägget AMC Banking 365 Fundamentals för att konvertera en fil som du får från banken till en dataström som [!INCLUDE[d365fin](includes/d365fin_md.md)] kan importera. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Som ett alternativ till att importera bankutdrag med AMC Banking 365 Fundamentals du använda Envestnet Yodlee Bank Feeds-tjänsten. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Om du vill importera eller exportera bankfiler måste du ställa in ditt eget bankkonto och dina leverantörers bankkonton. Mer information finns i [Skapa bankkonton](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Tillägg AMC Banking 365 Fundamentals kan ha en gräns för antal rader som kan exporteras i en fil. Du får ett felmeddelande om gränsen överskrids. Vi rekommenderar att kontoutdragsfiler inte innehåller fler än 1 000 rader eftersom behandlingstiden i tillägg AMC Banking 365 Fundamentals annars kan öka markant.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Så här registrerar du ditt företag för tillägget AMC Banking 365 Fundamentals
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Serviceinställningar för bankdatakonv.** och välj sedan relaterad länk.  
2. Sidan **Serviceinställningar för bankdatakonv.** öppnas med tre fält förifyllda med relevanta URL-adresser till leverantören av tillägg AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   I CRONUS demodatabas har fälten Användarnamn och Lösenord fyllts i förväg med information om demonstrationsinloggningen, som du ska ersätta med företaget faktiska information när du registrerar dig för AMC Banking 365 Fundamentals.
3. I fältet **URL för registrering** väljer du webbläsarknappen för att öppna tjänstleverantörens inloggningssida.  
4. På bankdatatjänstleverantörens registreringssida anger du användarnamnet och lösenord för ditt företags prenumeration på tjänsten, och slutför sedan inloggningen enligt tjänstleverantörens anvisningar.

    Ditt företag är nu registrerat för tillägget AMC Banking 365 Fundamentals. Fortsätt med att ange användarnamnet och lösenordet som du har angett för tjänsten i de relaterade inställningsfälten i [!INCLUDE[d365fin](includes/d365fin_md.md)].

5. På sidan **Serviceinställningar för bankdatakonv.** i fältet **Användarnamn** anger du samma värde som du har angett som inloggningsnamn på tjänstleverantörens sida i steg 4.
6. I fältet **Lösenord** anger du samma värde som du angav i fältet **Lösenord** på tjänstleverantörens sida i steg 4.

> [!NOTE]  
> Dina inloggningsdata krypteras automatiskt.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Så här visar eller uppdaterar du listan över bankdataformat som stöds för närvarande
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Serviceinställningar för bankdatakonv.** och välj sedan relaterad länk.
2. På sidan **Serviceinställningar för bankdatakonv.** väljer du åtgärden **Banknamn – datakonverteringslista** för att öppna listan med banknamn som representerar bankdataformat som stöds av konverteringstjänsten.
3. På sidan **Banknamn – datakonverteringslista** väljer du åtgärden **Uppdatera lista med banknamn**.

Listan över bankdataformat som stöds av tillägget AMC Banking 365 Fundamentals uppdateras nu. Det här är listan över banknamn, filtrerade efter landet/regionen, som du kan välja mellan i fältet **Banknamn – Datakonvertering** på sidan **Bankkontokort**.

> [!NOTE]  
>   Uppdatering av bankdataformat som stöds inträffar också när du väljer eller anger ett värde i fältet **Banknamn – Datakonvertering** på bankkontot.

Du är nu registrerad för tillägget AMC Banking 365 Fundamentals. Fortsätt för att visa inloggningsinformationen på varje bankkonto som ska användas tjänsten.

## <a name="see-also"></a>Se även
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

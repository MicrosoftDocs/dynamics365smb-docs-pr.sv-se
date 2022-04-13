---
title: Ställa in bankdatakonvertering
description: Du kan ställa in bankkonton för att följa upp transaktioner och importera eller exportera bankfeeder, till exempel Yodlee.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer
ms.search.form: 304, 20106, 20105, 20100, 20101, 20107, 20109
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ea671a550dcada2573ae9b8e174a6e2e23051f9e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523182"
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Konfigurera AMC Banking 365 Fundamentals-tillägget
En global tjänstleverantör för att konvertera betalningsinformation till alla dataformat som din bank kräver är ansluten och redo att aktiveras i [!INCLUDE[prod_short](includes/prod_short.md)]. I [!INCLUDE[prod_short](includes/prod_short.md)] betecknas detta som tillägget AMC Banking 365 Fundamentals.

Du kan exportera betalningsrader från sidan **Utbetalningsjournal** till en en fil eller en dataström som du sedan överför till din bank för automatisk behandling, så att du inte behöver göra electroniska betalningar individuellt. Mer information finns i [Så här exporterar du betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Du kan importera bankutdragsfiler till sidan **Betalningsavstämningsjournal** genom att använda AMC Banking 365 Fundamentals-tillägget för att konvertera en fil erhåller från din bank till ett dataflöde som [!INCLUDE[prod_short](includes/prod_short.md)] kan importera. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Som ett alternativ till att importera bankutlåtanden med AMC Banking 365 Fundamentals-tillägget kan du istället använda tjänsten Envestnet Yodlee Bank Feeds. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Om du vill importera eller exportera bankfiler måste du ställa in ditt eget bankkonto och dina leverantörers bankkonton. Mer information finns i [Skapa bankkonton](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> AMC Banking 365 Fundamentals-tillägget kan komma att begränsa antalet rader som kan exporteras i en och samma fil. Du får ett felmeddelande om gränsen överskrids. Bankutlåtandefiler bör inte överskrida 1 000 rader, detta eftersom bearbetningstiden i AMC Banking 365 Fundamentals-tillägget annars kan komma att förlängas avsevärt.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>För att registrera ditt företag för AMC Banking 365 Fundamentals-tillägget
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Installation av konv.tjänst för bankdata** och väljer sedan relaterad länk.  
2. Sidan **Installation av konv.tjänst för bankdata** öppnas, med tre fält förifyllda med relevanta URL:er tillhörande leverantören av AMC Banking 365 Fundamentals-tillägget.

    > [!NOTE]  
    >   I demonstrationsdatabasen CRONUS International Ltd. är fälten Användarnamn och Lösenord förifyllda med information för demonstrationsinloggning som du kan ersätta med ditt företags faktiska information när du registrerar dig för AMC Banking 365 Fundamentals-tillägget.
3. I fältet **URL för registrering** väljer du webbläsarknappen för att öppna tjänstleverantörens inloggningssida.  
4. På bankdatatjänstleverantörens registreringssida anger du användarnamnet och lösenord för ditt företags prenumeration på tjänsten, och slutför sedan inloggningen enligt tjänstleverantörens anvisningar.

    Ditt företag har nu registrerats för AMC Banking 365 Fundamentals-tillägget. Fortsätt med att ange användarnamnet och lösenordet som du har angett för tjänsten i de relaterade inställningsfälten i [!INCLUDE[prod_short](includes/prod_short.md)].

5. På sidan **Serviceinställningar för bankdatakonv.** i fältet **Användarnamn** anger du samma värde som du har angett som inloggningsnamn på tjänstleverantörens sida i steg 4.
6. I fältet **Lösenord** anger du samma värde som du angav i fältet **Lösenord** på tjänstleverantörens sida i steg 4.

> [!NOTE]  
> Dina inloggningsdata krypteras automatiskt.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Så här visar eller uppdaterar du listan över bankdataformat som stöds för närvarande
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Installation av konv.tjänst för bankdata** och väljer sedan relaterad länk.
2. På sidan **Serviceinställningar för bankdatakonv.** väljer du åtgärden **Banknamn – datakonverteringslista** för att öppna listan med banknamn som representerar bankdataformat som stöds av konverteringstjänsten.
3. På sidan **Banknamn – datakonverteringslista** väljer du åtgärden **Uppdatera lista med banknamn**.

Listan över bankdataformat som stöds av AMC Banking 365 Fundamentals-tillägget har nu uppdaterats. Det här är listan över banknamn, filtrerade efter landet/regionen, som du kan välja mellan i fältet **Banknamn – Datakonvertering** på sidan **Bankkontokort**.

> [!NOTE]  
>   Uppdatering av bankdataformat som stöds inträffar också när du väljer eller anger ett värde i fältet **Banknamn – Datakonvertering** på bankkontot.

Du har nu registrerat dig för AMC Banking 365 Fundamentals-tillägget. Fortsätt för att visa inloggningsinformationen på varje bankkonto som ska användas tjänsten.

## <a name="see-also"></a>Se även
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
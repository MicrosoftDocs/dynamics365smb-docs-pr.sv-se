---
title: "Så här skapar du bankdatakonvertering | Microsoft Docs"
description: "Du kan ställa in bankkonton för att följa upp transaktioner och importera eller exportera bankfeeder, till exempel Yodlee."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d83cf02ebfdb45479343b65cd777b8918fc5097d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a>Ställa in konverteringstjänsten för bankdata
En global tjänstleverantör för att konvertera betalningsinformation till alla dataformat som din bank kräver är ansluten och redo att aktiveras i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Detta kallas i [!INCLUDE[d365fin](includes/d365fin_md.md)] för Bankdatakonverteringstjänsten.

Du kan exportera betalningsrader från fönstret **Utbetalningsjournal** till en en fil eller en dataström som du sedan överför till din bank för automatisk behandling, så att du inte behöver göra electroniska betalningar individuellt. Mer information finns i [Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md).

Du kan importera bankutdragsfiler i fönstret **Betalningsavstämningsjournal** med hjälp av bankdatakonverteringstjänsten för att konvertera en fil som du får från banken till en dataström som [!INCLUDE[d365fin](includes/d365fin_md.md)] kan importera. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Som ett alternativ till att importera bankutdrag med bankdatakonverteringstjänsten kan du använda tjänsten Envestnet Yodlee bankfeeder. Mer information finns i [Konfigurera du bankfeedtjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

Om du vill importera eller exportera bankfiler måste du ställa in ditt eget bankkonto och dina leverantörers bankkonton. Mer information finns i [Skapa bankkonton](bank-how-setup-bank-accounts.md).

> [!NOTE]  
>   Bankdatakonverteringstjänsten kan ha en gräns för antal rader som kan exporteras i en fil. Du får ett felmeddelande om gränsen överskrids. Vi rekommenderar att kontoutdragsfiler inte innehåller fler än 1 000 rader eftersom behandlingstiden i bankdatakonverteringstjänsten annars kan öka markant.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Så här registrerar du ditt företag för tjänsten bankdatakonvertering.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Serviceinställningar för bankdatakonv.** och välj sedan relaterad länk.  
2. Fönstret **Serviceinställningar för bankdatakonv.** öppnas med tre fält förifyllda med relevanta URL-adresser till leverantören av tjänsten för bankdatakonvertering.

    > [!NOTE]  
    >   I CRONUS International Ltd:s demodatabas har fälten Användarnamn och Lösenord fyllts i förväg med information om demonstrationsinloggningen, som du ska ersätta med företaget faktiska information när du registrerar dig för bankdatakonverteringen.
3. I fältet **URL för registrering** väljer du webbläsarknappen för att öppna tjänstleverantörens inloggningssida.  
4. På bankdatatjänstleverantörens registreringssida anger du användarnamnet och lösenord för ditt företags prenumeration på tjänsten, och slutför sedan inloggningen enligt tjänstleverantörens anvisningar.

  Ditt företag är nu registrerat för tjänsten bankdatakonvertering. Fortsätt med att ange användarnamnet och lösenordet som du har angett för tjänsten i de relaterade inställningsfälten i [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. I fönstret **Serviceinställningar för bankdatakonv.** i fältet **Användarnamn** anger du samma värde som du har angett som inloggningsnamn på tjänstleverantörens sida i steg 4.
6. I fältet **Lösenord** anger du samma värde som du angav i fältet **Lösenord** på tjänstleverantörens sida i steg 4.

## <a name="to-encrypt-your-login-information"></a>Så här kan du kryptera dina inloggningsuppgifter
Du rekommenderas att skydda de inloggningsuppgifter som du anger i fönstret **Serviceinställningar för bankdatakonv.**. Du kan kryptera data på [!INCLUDE[d365fin](includes/d365fin_md.md)]-servern genom att skapa nya eller importera befintliga krypteringsnycklar som aktiverar på [!INCLUDE[d365fin](includes/d365fin_md.md)]-serverinstansen med anslutningen till databasen.

1. I fönstret **Serviceinställningar för bankdatakonv.** väljer du åtgärden **Krypteringshantering**.
2. Aktivera krypteringen av dina data i fönstret **Datakrypteringshantering**.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Så här visar eller uppdaterar du listan över bankdataformat som stöds för närvarande
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Serviceinställningar för bankdatakonv.** och välj sedan relaterad länk.
2. I fönstret **Serviceinställningar för bankdatakonv.** väljer du åtgärden **Banknamn – datakonverteringslista** för att öppna listan med banknamn som representerar bankdataformat som stöds av konverteringstjänsten.
3. På sidan **Banknamn – datakonverteringslista** väljer du åtgärden **Uppdatera lista med banknamn**.

Listan över bankdataformat som stöds av tjänsten för bankdatakonvertering uppdateras nu. Det här är listan över banknamn, filtrerade efter landet/regionen, som du kan välja mellan i fältet **Banknamn – Datakonvertering** i fönstret **Bankkontokort**.

> [!NOTE]  
>   Uppdatering av bankdataformat som stöds inträffar också när du väljer eller anger ett värde i fältet **Banknamn – Datakonvertering** på bankkontot.

Du har nu registrerat dig för tjänsten bankdatakonvertering. Fortsätt för att visa inloggningsinformationen på varje bankkonto som ska användas tjänsten.

## <a name="see-also"></a>Se även
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


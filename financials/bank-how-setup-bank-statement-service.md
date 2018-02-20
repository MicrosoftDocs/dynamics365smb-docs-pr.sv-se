---
title: "Ställa in Yodlee Bank Feeds | Microsoft Docs"
description: "Du kan konvertera betalningsinformation till vilket dataformat som som krävs av din bank och aktivera exporten eller importen av Bankfilerna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa5c0c39dbbce40b59d639f810522c66da1a09ab
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Konfigurera bankfeedtjänsten Envestnet Yodlee
Du kan importera elektroniska bankutdrag från banken så att du snabbt kan fylla i fönstret **Betalningsavstämningsjournal** och koppla betalningar och stämma av bankkontot. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tjänsten Envestnet Yodlee bankfeeder har installerats som ett tillägg till [!INCLUDE[d365fin](includes/d365fin_md.md)] och är klar att aktiveras. Mer information finns i [Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md).

> [!NOTE]
> Tjänsten Envestnet Yodlee bankfeeder stöds bara i USA, Kanada och Storbritannien.

När du har aktiverat bankfeedtjänsten måste du länka det involverade bankkontot till det onlinebankkonto som feeden ska komma från. Du länkar bankkonton till onlinebankkonton i följande olika scenarier:

* Det finns inget bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)] för ditt onlinebankkonto. Därför skapar du bankkontot genom att länka från onlinebankkontot.
* Det finns ett bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du vill länka till ett onlinebankkonto.
* Ett länkat bankkonto måste länkas av eftersom du vill sluta använda bankfeedtjänsten för kontot.
* Onlinebankkonton har ändrat och du vill uppdatera informationen om bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)].

När bankfeedtjänsten är aktiverad, kan du konfigurera ett bankkonto att automatiskt importera nya kontoutdrag till fönstret **Betalningsavstämningsjournal** varannan timme. Transaktioner för utbetalningar som redan har bokförts som kopplade och/eller avstämda i fönstret **Betalningsavstämningsjournal** kommer inte att importeras. Mer information finns i avsnittet “Att aktivera automatisk import av kontoutdrag”.

> [!NOTE]  
>   Om du använder den assisterade inställningen Konfigurera företag kommer några av stegen i följande procedurer att utföras automatiskt när du kommer till inställningen av företagets bankkonto. Mer information finns i [Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## <a name="to-enable-the-bank-feed-service"></a>Så här aktiverar du bankfeedtjänsten
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Öppna det bankkonto som du ska använda för bankfeedtjänsten.
3. I fönstret **Bankkonto** i fältet **Format för bankutdragsimport** väljer du YODLEEBANKFEED.  

Bankfeedtjänsten aktiveras när du länkar ett bankkonto till dess relaterade onlinebankkonto. Visa nästa procedur.  

## <a name="to-create-a-new-linked-bank-account"></a>Så här skapar du ett nytt länkat bankkonto
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj det relevanta bankkontot och välj sedan **Skapa nytt länkat bakkonto**. Fönstret **Länkning av bankkonto** öppnas efter några ögonblick.

    > [!NOTE]  
>   Det här fönstret visar den verkliga webbsidan för tjänsten Envestnet Yodlee bankfeeder. Terminologi och funktionalitet i fönstret kanske inte matchar instruktionerna som tillhandahålls i det här avsnittet.  
3. I fönstret **Länka till onlinebankkonto** i rutan **Länka konto** använd Sökfunktionen för att hitta banken där du har ett eller flera onlinebankkonton.
4. Välj bankens namn. Rutan **Inloggning** öppnas.
5. Ange användarnamnet och lösenordet som du använder för att logga in på onlinebanken och tryck sedan på knappen **Nästa**.  
6. Bankfeedtjänsten förbereder dig på att länka det första onlinebankkontot på den angivna banken till ett nytt bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
>   Om du har fler än ett onlinebankkonto på banken, måste du skapa ytterligare bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)] för dem. Se steg 8 till 10.  

    När processen är klar visas bankens namn i rutan **Mina konton** på fliken **Länkade**. Siffran inom parentes visar hur många online bankkonton som länkades.  
7. Välj **OK**.

    Om du bara länkar ett onlinebankkonto, öppnas fönstret **bankkontokort** och visar namnet på onlinebankkontot. I det här fallet är bankkontolänkninguppgiften slutförd. Allt som återstår är att skapa bankkontot. Mer information finns i [Skapa bankkonton](bank-how-setup-bank-accounts.md).

    Om fler än ett bankkonto länkades kommer fönstret **Länkning av bankkonto** att öppnas med det ytterligare onlinebankkonton som inte ännu är länkade till bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I detta fall, följ nästa steg.  
8. I fönstret **Länkning av bankkonto** väljer du raden för ett onlinebankkonto och väljer sedan åtgärden **Länka till nytt bankkonto**.  

    Fönstret **Bankkontokort** för ett nytt bankkonto kommer att öppnas och visar namnet på den detta bankkonto.

    Om ett bankkonto redan finns i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vill länka det ytterligare onlinebankkontot till, följer du nästa steg.  
9. I fönstret **Länkning av bankkonto** väljer du raden för ett onlinebankkonto och väljer sedan åtgärden **Länka till befintligt bankkonto**.
10. I fönstret **Bankkontolista** väljer du det bankkonto som du vill länka till och väljer sedan knappen **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Så här länkar du ett bankkonto till ett onlinebankkonto
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj raden för ett bankkonto som inte är kopplad till ett onlinebankkonto och välj sedan åtgärden **Länka till onlinebankkonto**. Fönstret **Länka till onlinebankkonto** öppnas med bankens namn ifyllt i rutan **Länka konto**.
3. Välj bankens namn. Rutan **Inloggning** öppnas.
4. Ange användarnamnet och lösenordet som du använder för att logga in på onlinebanken och tryck sedan på knappen **Nästa**.  

    Bankfeedtjänsten förbereder dig på att länka ditt bankkontot bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)] till det relaterade onlinebankkontot.  

    När processen är klar visas bankens namn i rutan **Mina konton** på fliken **Länkade**. Om banken har mer än ett bankkonto kan endast det bankkonto som du valde i steg 2 länkas.  
5. Välj **OK**.

I fönstret **Bankkontolista** markeras kryssrutan **Länkad**.

## <a name="to-unlink-a-bank-account"></a>Så här tar du bort länk till bankkonto
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.  
2. Välj raden för ett länkat bankkonto som du vill ta bort länken till dess relaterade onlinebankkonto för och välj sedan åtgärden **Ta bort länk till onlinebankkonto**.

> [!NOTE]  
>   Om du väljer **Ja** i bekräftelsedialogrutan, tas länken till onlinebankkontot bort och inloggningsdetaljerna avmarkeras. Om du vill länka bankkontot till onlinebankkonto igen måste du logga in i banken igen. Mer information finns i avsnittet “Så här länkar du ett bankkonto till ett onlinebankkonto“.

## <a name="to-update-bank-account-linking"></a>Så här uppdaterar du länkning till bankkonto
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Välj det relevanta bankkontot och välj sedan åtgärden **Uppdatera länkning av bankkonto**.

Om problem finns för någon av de länkade bankkontona i fönstret **Bankkontolista** kommer fönstret **Länkning av bankkonto** med information om vilka bankkonton som har problem. Problemen kan bäst lösas genom att ta bort länken till onlinebankkontot och sedan återskapa länken. Mer information finns i avsnittet “Så här länkar du ett bankkonto till ett onlinebankkonto“.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Om du vill aktivera automatisk import av bankutdrag
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bankkonton** och välj sedan relaterad länk.
2. Markera raden för ett länkat bankkonto och välj sedan åtgärden **Inställningar för automatisk import av bankutdrag**.
3. I fönstret **Inställningar för automatisk import av bankutdrag** i fältet **Antal dagar som ingår** anger du hur långt tillbaka i tiden som du får nya banktransaktioner för.

    > [!NOTE]  
>   Det rekommenderas att du ställer in detta värde till 7 dagar eller fler.  
4. Markera kryssrutan **Aktiverad**.  

Varje timme kommer fönstret **Betalningsavstämningsjournal** att visa alla nya utbetalningar som har gjorts på detta onlinebankkonto.

> [!NOTE]  
>   Transaktioner för utbetalningar som redan har bokförts som kopplade och/eller avstämda i fönstret **Betalningsavstämningsjournal** kommer inte att importeras.

## <a name="see-also"></a>Se även
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


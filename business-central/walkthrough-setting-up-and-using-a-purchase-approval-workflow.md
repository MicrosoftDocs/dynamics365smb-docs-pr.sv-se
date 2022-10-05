---
title: Konfigurera och använda ett arbetsflöde för godkännande av inköp
description: Den här genom gången tar dig igenom alla de etapper som ingår när du ställer in och använder ett godkännande arbetsflöde för inköp i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: bf58b9f1c0702275df1dc6e2884444369d084b80
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585436"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp

Du kan automatisera processen för att godkänna nya eller ändrade transaktioner, t.ex dokument, journalrader och kundkort, genom att skapa arbetsflöden med stegen för godkännandena i fråga.

Innan du skapar godkännandearbetsflöden, måste du skapa en godkännare och ersättningsgodkännare för varje godkännandeanvändare. Du kan också ange godkännares beloppsgränser för att definiera vilka försäljnings- och inköpsposter de är behöriga att godkänna. Godkännandebegäranden och andra kan meddelanden skickas som e-post eller intern anteckning. För varje inställning av godkännandeanvändare kan du också ställa in när de tar emot meddelanden.

> [!NOTE]
> Förutom funktionerna för arbetsflöde inom [!INCLUDE[prod_short](includes/prod_short.md)] kan du använda Power Automate för att definiera arbetsflöden för händelser i [!INCLUDE[prod_short](includes/prod_short.md)]. Trots att det finns två separata arbetsflödessystem bör du notera att alla flödesmalla som du skapar med Power Automate lägga till i listan över arbetsflödesmallar i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Använda Business Central i ett automatiskt arbetsflöde ](across-how-use-financials-data-source-flow.md).  

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg. Läs mer i [arbetsflöden](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Om den här genomgången

Den här genom gången är ett scenario som illustrerar följande uppgifter:  

- Ställa in godkännandeanvändare  
- Ställa in meddelanden för godkännandeanvändare  
- Ändra och aktivera ett godkännandearbetsflöde  
- Begära godkännande av en inköpsorder, som Alicia  
- Ta emot ett meddelande och sedan godkänna begäran, som Sean  

## <a name="story"></a>Situation

Sean är en super user i CRONUS. Han skapar två godkännandeanvändare. En är Alicia som representerar en inköpsagent. Den andra är han själv som representerar Alicias godkännare. Sean ger sig själv obegränsade godkännanderättigheter för inköp och anger sedan att han ska få meddelanden genom intern anteckning så snart som en relevant händelse inträffar. Till slut skapar Sean det önskade godkännandearbetsflödet som en kopia av den befintliga arbetsflödesmallen för *Arbetsflöde för godkännande av inköpsorder* och låter alla befintliga händelsevillkor och svarsalternativ vara oförändrade, och aktiverar sedan arbetsflödet.  

För att testa godkännandearbetsflödet loggar Stefan först in på [!INCLUDE[prod_short](includes/prod_short.md)] som Alicia och begär sedan godkännande av en inköpsorder. Sedan loggar Sean in som sig själv, ser anteckningen i sitt rollcenter, följer länken till godkännandebegäran för inköpsordern och godkänner sedan begäran.  

## <a name="users"></a>Användare

Innan du kan ställa in godkännandeanvändare och deras meddelandemetod måste du kontrollera att det finns två användare i [!INCLUDE[prod_short](includes/prod_short.md)]: En användare representerar Alicia. Den andra användaren, du själv, representerar Sean. Läs mer på [Skapa användare enligt licenser](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Ställa in godkännandeanvändare

När du har loggat in som dig själv ställer du in Alicia som en godkännandeanvändare vars godkännare är du själv. Skapa dina godkännanderättigheter och ange hur och när du får meddelande om godkännandebegäranden.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Så här ställer du in dig själv och Alicia som godkännandeanvändare

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Användarinställningar för godkännande** och väljer sedan relaterad länk.  
2. Å¨sidan **Användarinställningar för godkännande** väljer du åtgärden **Ny**.  

    > [!NOTE]  
    >  Du måste registrera en godkännare innan du kan ställa in användare som kräver den godkännarens godkännande. Därför måste du ställa in dig själv innan du ställer in Alicia.  

3. Ställ in de två godkännandeanvändarna genom att fylla i fälten enligt beskrivningen i följande tabell.  

    |Användar-ID|Godkännar-ID|Obegränsad godkännande för inköp|  
    |-------|-----------|---------------------------|  
    |DU||Vald|
    |ALICIA|DU||

### <a name="setting-up-notifications"></a>Ställa in meddelanden

Användaren får ett internt meddelande om begäranden att godkänna i den här genomgången. Godkännandemeddelandet kan också skickas via e-post, och du kan lägga till ett svarssteg i arbetsflödet som meddelar avsändaren när en begäran godkänns eller avvisas. Läs mer på [Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Så här ställer du in hur och när du får meddelande

1. På sidan **Användarinställningar för godkännande** markerar du raden för dig själv och väljer sedan åtgärden **Meddelandeinställningar**.  
2. På sidan **Konfigurera meddelanden** i fältet **meddelandetyp** väljer du **godkännande**.  
3. I fältet **Meddelandemetod** väljer du **Notering**.  
4. På sidan **Konfigurera meddelanden** väljer du åtgärden **Meddelandeschema**.  
5. På sidan **Meddelandeschema** i fältet **Återkommande** väljer du **Omedelbart**.  

## <a name="creating-the-approval-workflow"></a>Skapa godkännandearbetsflödet

Skapa arbetsflödet för godkännande av inköpsorder genom att kopiera stegen från mallen **Arbetsflöde för godkännande av inköpsorder**. Lämna de befintliga arbetsflödesstegen oförändrade och aktivera sedan arbetsflödet.  

> [!TIP]
> Som tillval kan du lägga till ett arbetsflödessvarssteg för att meddela avsändaren när dennes begäran har godkänts eller avvisats. Läs mer på [Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Så här skapar och aktiverar du ett arbetsflöde för inköpsordergodkännade

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. På sidan **Arbetsflöden** väljer du **Åtgärder**, sedan **Ny** och sedan åtgärden **Nytt arbetsflöde från mall**.  
3. På sidan **Arbetsflödesmallar** väljer du arbetsflödesmallen kallad **Arbetsflöde för godkännande av inköpsorder**.  

   Sidan **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen. Värdet i fältet **Kod** utökas med *-01* i syfte att ange att detta är det första arbetsflöde som skapats från mallen **Arbetsflöde för godkännande av inköpsorder**.  
4. I huvudet på fönstret **Arbetsflöde** markerar du växlingskontrollen **Aktiverad**.  

## <a name="use-the-approval-workflow"></a>Använda godkännandearbetsflödet

Använd det nya arbetsflödet Arbetsflöde för godkännande av inköpsfaktura genom att först logga in på [!INCLUDE[prod_short](includes/prod_short.md)] som Alicia för att begära godkännande av en inköpsorder. Logga sedan in som dig själv, visa anteckningen i rollcentret, följ länken till godkännandebegäran och godkänn begäran.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Så här begär du godkännande av en inköpsorder, som Alicia.

1. Logga in som Alicia.
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
3. Markera raden om du vill öppna *inköpsorder 106001*.  
4. På sidan **Inköpsorder** väljer du **Åtgärder**, sedan **Begär godkännande** och sedan åtgärden **Skicka godkännandebegäran**.  

Observera att värdet i fältet **Status** har ändrats till **Väntar på godkännande**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Så här godkänner du inköpsordern, som Sean

1. Logga in som Sean.
2. I rollcentret går du till området **Självbetjäning** och väljer **Begäranden att godkänna**.
3. På sidan **Begäranden att godkänna** markerar du raden om inköpsordern från Alicia och väljer sedan åtgärden **Godkänn**.  

Värdet i fältet **Status** på Alicias inköpsorder ändras till **Släppt**.  

Du har nu ställt in och testat ett enkelt godkännandearbetsflöde som baseras på de två första stegen i arbetsflödet **Arbetsflöde för godkännande av inköpsorder**. Det är enkelt att utöka arbetsflödet så att det automatiskt bokför Alicias inköpsorder när Sean godkänner den. För att göra det måste du aktivera arbetsflödet **Arbetsflöde för godkännande av inköpsorder**, där svaret på en släppt inköpsfaktura är att bokföra den. Först måste du ändra händelsevillkoret i det första arbetsflödessteget från (inköp) **Faktura** till **Order**.  

Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller ett antal arbetsflödesmallar för scenarier som stöds av programkoden. De flesta mallar är för godkännandearbetsflöden.  

Du definierar arbetsflödesvariationer genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/use-approval-workflows/)

## <a name="see-also"></a>Se även

[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)  
[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md)  
[Arbetsflöde](across-workflow.md)  
[Använda Business Central i ett automatiskt arbetsflöde](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

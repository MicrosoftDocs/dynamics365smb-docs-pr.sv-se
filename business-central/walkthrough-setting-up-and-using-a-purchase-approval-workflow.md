---
title: Konfigurera och använda ett arbetsflöde för godkännande av inköp | Microsoft Docs
description: Du kan automatisera processen för att godkänna nya eller ändrade transaktioner, t.ex dokument, journalrader och kundkort, genom att skapa arbetsflöden med stegen för godkännandena i fråga. Innan du skapar godkännandearbetsflöden, måste du skapa en godkännare och ersättningsgodkännare för varje godkännandeanvändare. Du kan också ange godkännares beloppsgränser för att definiera vilka försäljnings- och inköpsposter de är behöriga att godkänna. Godkännandebegäranden och andra kan meddelanden skickas som e-post eller intern anteckning. För varje inställning av godkännandeanvändare kan du också ställa in när de tar emot meddelanden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca97d08166b73f75240203aa9949e4b0aa774ea6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310522"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp
Du kan automatisera processen för att godkänna nya eller ändrade transaktioner, t.ex dokument, journalrader och kundkort, genom att skapa arbetsflöden med stegen för godkännandena i fråga. Innan du skapar godkännandearbetsflöden, måste du skapa en godkännare och ersättningsgodkännare för varje godkännandeanvändare. Du kan också ange godkännares beloppsgränser för att definiera vilka försäljnings- och inköpsposter de är behöriga att godkänna. Godkännandebegäranden och andra kan meddelanden skickas som e-post eller intern anteckning. För varje inställning av godkännandeanvändare kan du också ställa in när de tar emot meddelanden.

> [!NOTE]
> Förutom funktionerna i arbetsflödet [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du integrera till Microsoft Flow för att definiera arbetsflöden för händelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Observera att trots att det finns två separata arbetsflödessystem, kommer alla Flow-mallar du skapar med Microsoft Flow läggas till i listan över arbetsflödesmallar i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Använda Business Central i ett automatiskt arbetsflöde ](across-how-use-financials-data-source-flow.md).   

 Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg. Mer information finns i [Arbetsflöden](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
I den här genomgången tas följande aktiviteter upp:  

-   Ställa in godkännandeanvändare.  
-   Ställa in meddelanden för godkännandeanvändare.  
-   Ändra och aktivera ett godkännandearbetsflöde.  
-   Begära godkännande av en inköpsorder, som Alicia.  
-   Ta emot ett meddelande och sedan godkänna begäran, som Sean.  

## <a name="prerequisites"></a>Förutsättningar  
Om du vill utföra den här genomgången behöver du demonstrationsföretaget CRONUS.

## <a name="story"></a>Situation  
Sean är en super user i CRONUS. Han skapar två godkännandeanvändare. En är Alicia som representerar en inköpsagent. Den andra är han själv som representerar Alicias godkännare. Sean ger sig själv obegränsade godkännanderättigheter för inköp och anger sedan att han ska få meddelanden genom intern anteckning så snart som en relevant händelse inträffar. Till slut skapar Sean det önskade godkännandearbetsflödet som en kopia av den befintliga arbetsflödesmallen för Arbetsflöde för godkännande av inköpsorder och låter alla befintliga händelsevillkor och svarsalternativ vara oförändrade, och aktiverar sedan arbetsflödet.  

För att testa godkännandearbetsflödet loggar Stefan först in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Alicia och begär sedan godkännande av en inköpsorder. Sedan loggar Sean in som sig själv, ser anteckningen i sitt rollcenter, följer länken till godkännandebegäran för inköpsordern och godkänner sedan begäran.  

## <a name="setting-up-sample-data"></a>Ställa in exempeldata
Innan du kan ställa in godkännandeanvändare och deras meddelandemetod måste du kontrollera att det finns två användare i [!INCLUDE[d365fin](includes/d365fin_md.md)]: En användare representerar Alicia. Den andra användaren, du själv, representerar Sean. Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Ställa in godkännandeanvändare  
När du har loggat in som dig själv ställer du in Alicia en godkännandeanvändare vars godkännare är du själv. Skapa dina godkännanderättigheter och ange hur och när du får meddelande om godkännandebegäranden.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Så här ställer du in dig själv och Alicia som godkännandeanvändare  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användarinställningar för godkännande** och välj sedan relaterad länk.  
2.  Å¨sidan **Användarinställningar för godkännande** väljer du åtgärden **Ny**.  

    > [!NOTE]  
    >  Du måste registrera en godkännare innan du kan ställa in användare som kräver den godkännarens godkännande. Därför måste du ställa in dig själv innan du ställer in Alicia.  

3.  Ställ in de två godkännandeanvändarna genom att fylla i fälten enligt beskrivningen i följande tabell.  

    |Användar-ID|Godkännar-ID|Obegränsad godkännande för inköp|  
    |-------------|-----------------|---------------------------------|  
    |DU||Vald|  
    |ALICIA|DU||  

### <a name="setting-up-notifications"></a>Ställa in e-postmeddelanden  
Användaren får ett internt meddelande om begäranden att godkänna i den här genomgången. Meddelande om godkännanden kan också ske via e-post. Mer information finns i [Så här anger du när och hur användare ska meddelas](across-how-to-specify-when-and-how-to-receive-notifications.md). 

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Så här ställer du in hur och när du får meddelande  
1.  På sidan **Användarinställningar för godkännande** markerar du raden för dig själv och väljer sedan åtgärden **Meddelandeinställningar**.  
2.  På sidan **Konfigurera meddelanden** i fältet **meddelandetyp** väljer du **godkännande**.  
3.  I fältet **Meddelandemetod** väljer du **Notering**.  
6.  På sidan **Konfigurera meddelanden** väljer du åtgärden **Meddelandeschema**.  
7.  På sidan **Meddelandeschema** i fältet **Förekomst** väljer du **Omedelbart**.  
8. Välj knappen **OK**.  

## <a name="creating-the-approval-workflow"></a>Skapa godkännandearbetsflödet  
 Skapa arbetsflödet för godkännande av inköpsorder genom att kopiera stegen från arbetsflödesmallen för Arbetsflöde för godkännande av inköpsorder. Lämna de befintliga arbetsflödesstegen oförändrade och aktivera sedan arbetsflödet.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Så här skapar och aktiverar du ett arbetsflöde för inköpsordergodkännade  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arbetsflöden** och välj sedan relaterad länk.  
2.  På sidan **arbetsflöden** väljer du åtgärden **skapa arbetsflödet från mall**.  
3.  På sidan **arbetsflödesmallar** väljer du arbetsflödesmallen kallad Godkännande av inköpsorder och väljer sedan knappen **OK**.  

    Sidan **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen. Värdet i fältet **Kod** utökas med ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen Arbetsflöde för godkännande av inköpsorder.  
5.  I huvudet på fönstret **Arbetsflöde** markerar du kryssrutan **Aktiverad**.  

## <a name="using-the-approval-workflow"></a>Använda godkännandearbetsflödet  
Använd det nya arbetsflödet för godkännande av inköpsorder genom att först logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Alicia för att begära godkännande av en inköpsorder. Logga sedan in som dig själv, visa anteckningen i rollcentret, följ länken till godkännandebegäran och godkänn begäran.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Så här begär du godkännande av en inköpsorder, som Alicia.  
1. Logga in som Alicia.
2.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsorder** och välj sedan relaterad länk.  
3.  Markera raden för öppen inköpsorder 104001 och välj åtgärden **redigera**.  
4.  På sidan **inköpsorder** väljer du åtgärden **Skicka godkännandebegäran**.  

Observera att värdet i fältet **Status** har ändrats till **Väntar på godkännande**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Så här godkänner du inköpsordern, som Sean  
1. Logga in som Sean.
2.  Sök efter ett nytt meddelande från Alicia i Rollcentret på sidan **Mina meddelanden**.  
3.  När meddelandet visas på sidan **Mina meddelanden** väljer du värdet **Godkännandetransaktion: XX, XX** i fältet **Sida**. Sidan **Begäranden att godkänna** öppnas med Alicias begäran om den markerade inköpsordern.  
4.  På sidan **förfrågningar att godkänna** väljer du åtgärden **Godkänn**.  

    Värdet i fältet **Status** på Alicias inköpsorder ändras till **Släppt**.  

Du har nu ställt in och testat ett enkelt godkännandearbetsflöde som baseras på de två första stegen i arbetsflödet Arbetsflöde för godkännande av inköpsorder. Det är enkelt att utöka arbetsflödet så att det automatiskt bokför Alicias inköpsorder när Sean godkänner den. För att göra det måste du aktivera arbetsflödet Arbetsflöde för godkännande av inköpsorder, där svaret på en släppt inköpsfaktura är att bokföra den. Först måste du ändra händelsevillkoret i det första arbetsflödessteget från (inköp) **Faktura** till **Order**.  

Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal arbetsflödesmallar för scenarier som stöds av programkoden. De flesta är för godkännandearbetsflöden.  

Du definierar arbetsflödesvariationer genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

Om ett företagsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds måste en Microsoft-partner implementera dem genom att anpassa applikationskoden. Mer information finns i [Genomgång: Genomföra nya arbetsflödeshändelser och svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjälpen för utvecklare och IT-proffs.  

## <a name="see-also"></a>Se även  
[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
[Skapa arbetsflöden](across-how-to-create-workflows.md)   
[Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md)   
[Arbetsflöde](across-workflow.md)  
[Använda Business Central i ett automatiskt arbetsflöde](across-how-use-financials-data-source-flow.md)

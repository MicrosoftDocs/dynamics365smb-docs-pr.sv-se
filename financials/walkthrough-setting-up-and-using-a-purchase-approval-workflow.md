---
title: "Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp | Microsoft Docs"
description: "Du kan automatisera processen för att godkänna nya eller ändrade transaktioner, t.ex dokument, journalrader och kundkort, genom att skapa arbetsflöden med stegen för godkännandena i fråga. Innan du skapar godkännandearbetsflöden, måste du skapa en godkännare och ersättningsgodkännare för varje godkännandeanvändare. Du kan också ange godkännares beloppsgränser för att definiera vilka försäljnings- och inköpsposter de är behöriga att godkänna. Godkännandebegäranden och andra kan meddelanden skickas som e-post eller intern anteckning. För varje inställning av godkännandeanvändare kan du också ställa in när de tar emot meddelanden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09d48e230291524e7771d4b4305c4290bd567eb9
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp
Du kan automatisera processen för att godkänna nya eller ändrade transaktioner, t.ex dokument, journalrader och kundkort, genom att skapa arbetsflöden med stegen för godkännandena i fråga. Innan du skapar godkännandearbetsflöden, måste du skapa en godkännare och ersättningsgodkännare för varje godkännandeanvändare. Du kan också ange godkännares beloppsgränser för att definiera vilka försäljnings- och inköpsposter de är behöriga att godkänna. Godkännandebegäranden och andra kan meddelanden skickas som e-post eller intern anteckning. För varje inställning av godkännandeanvändare kan du också ställa in när de tar emot meddelanden.  

 Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg. Mer information finns i [Arbetsflöden](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
I den här genomgången tas följande aktiviteter upp:  

-   Ställa in godkännandeanvändare (till exempel ställa in en användare i Windows och i [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Ställa in meddelanden för godkännandeanvändare.  
-   Ändra och aktivera ett godkännandearbetsflöde.  
-   Starta jobbkön som skickar ut meddelanden.  
-   Begära godkännande av en inköpsorder, som Alicia.  
-   Ta emot ett meddelande och sedan godkänna begäran, som Sean.  

## <a name="prerequisites"></a>Förutsättningar  
Om du vill utföra den här genomgången behöver du demonstrationsföretaget CRONUS.

## <a name="story"></a>Situation  
Stefan har en superanvändare i CRONUS på sin egen dator.  

Han skapar två godkännandeanvändare. En är Alicia som representerar en inköpsagent. Den andra är han själv som representerar Alicias godkännare. Sean ger sig själv obegränsade godkännanderättigheter för inköp och anger sedan att han ska få meddelanden genom intern anteckning så snart som en relevant händelse inträffar. Till slut skapar Sean det önskade godkännandearbetsflödet som en kopia av den befintliga arbetsflödesmallen för Arbetsflöde för godkännande av inköpsorder och låter alla befintliga händelsevillkor och svarsalternativ vara oförändrade, och aktiverar sedan arbetsflödet.  

För att testa godkännandearbetsflödet loggar Stefan först in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Alicia och begär sedan godkännande av en inköpsorder. Sedan loggar Sean in som sig själv, ser anteckningen i sitt rollcenter, följer länken till godkännandebegäran för inköpsordern och godkänner sedan begäran.  

## <a name="setting-up-the-sample-data"></a>Ställa in exempeldata  
Du måste skapa en ny användare på den lokala datorn och i [!INCLUDE[d365fin](includes/d365fin_md.md)] som representerar Alicia som du sedan vill välja som godkännandeanvändare. Ditt eget användarkonto representerar Sean.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Så här lägger du till Alicia som användare på den lokala datorn  

1.  Välj **Starta**, i rutan **Sök bland program och filer** anger du **Redigera lokala användare och grupper** och väljer sedan relaterad länk.  
2.  Öppna mappen **Användare**.  
3.  Välj **Ny användare** på fliken **Åtgärder**.  
4.  Ange Alicia i fältet **Användarnamn**.  
5.  Ange ett giltigt lösenord i fälten **Lösenord** och **Bekräfta lösenord**.  
6.  Avmarkera kryssrutan **Användaren måste ändra lösenordet vid nästa inloggning**.  
7.  Stäng fönstret **Lokala användare och grupper**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Så här lägger du till Alicia som användare i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användare** och välj sedan relaterad länk.  
2.  I fönstret **Windows-användare** på fliken **Start** i gruppen **Ny** väljer du **Ny**.  
3.  I fönstret **användarkort** i fältet **användarnamn** anger du Alicia.  
4.  I fältet **Windows användarnamn** väljer du AssistEdit-knappen.  
5.  I fönstret **Välj användare eller grupp**, i fältet **Ange objektnamn som ska väljas** skriver du Alicia och väljer knappen **Kontrollera namn**.  
6.  När [DATORNAMN]ALICIA visas i fältet väljer du knappen **OK**.  
7.  På snabbfliken **Användarbehörighetsuppsättning**, i fältet **Behörighetsuppsättning** väljer du **SUPER**.  
8.  I fältet **Företag** väljer du **CRONUS International Ltd.**  
9. Välj **OK**.  

## <a name="setting-up-approval-users"></a>Ställa in godkännandeanvändare  
Genom att använda Windows-användaren som du precis har skapat, ställer du in Alicia som en godkännandeanvändare vars godkännare är du själv. Skapa dina godkännanderättigheter och ange hur och när du får meddelande om godkännandebegäranden.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Så här ställer du in dig själv och Alicia som godkännandeanvändare  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Användarinställningar för godkännande** och välj sedan relaterad länk.  
2.  I fönstret **Användarinställningar för godkännande** på fliken **Start** i gruppen **Ny**, väljer du **Ny**.  

    > [!NOTE]  
    >  Du måste registrera en godkännare innan du kan ställa in användare som kräver den godkännarens godkännande. Därför måste du ställa in dig själv innan du ställer in Alicia.  

3.  Ställ in de två godkännandeanvändarna genom att fylla i fälten enligt beskrivningen i följande tabell.  

    |Användar-ID|Godkännar-ID|Obegränsad godkännande för inköp|  
    |-------------|-----------------|---------------------------------|  
    |[DATORNAMN][DU]||Vald|  
    |[DATORNAMN]ALICIA|[DATORNAMN][DU]||  

## <a name="setting-up-notifications"></a>Ställa in e-postmeddelanden  
Ange hur och när du får meddelande om godkännandebegäranden.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Så här ställer du in hur och när du får meddelande  
1.  I fönstret **Användarinställningar för godkännande** väljer du raden för dig själv, och på fliken **Start** i gruppen **Process** väljer du **Konfigurera meddelanden**.  
2.  I fönstret **Meddelandeinställningar** i fältet **meddelandetyp** anger du **godkännande**.  
3.  Välj fältet **Kod för meddelandemall** och välj sedan knappen **Avancerat**.  
4.  I fönstret **Kod för meddelandemall** i fliken **Start** i gruppen **Hantera** väljer du **Redigera lista**.  
5.  På raden för godkännandemallen, i fältet **Meddelandemetod**, ange **Notering**.  
6.  Välj knappen **OK**.  
7.  I fönstret **Konfigurera meddelanden** på fliken **Start** i gruppen **Process** väljer du **Meddelandeschema**.  
8.  I fönstret **Meddelandeschema** i fältet **Förekomst** väljer du **Omedelbart**.  
9. Välj knappen **OK**.  

## <a name="creating-the-approval-workflow"></a>Skapa godkännandearbetsflödet  
 Skapa arbetsflödet för godkännande av inköpsorder genom att kopiera stegen från arbetsflödesmallen för Arbetsflöde för godkännande av inköpsorder. Lämna de befintliga arbetsflödesstegen oförändrade och aktivera sedan arbetsflödet.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Så här skapar och aktiverar du ett arbetsflöde för inköpsordergodkännade  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.  
2.  I fönstret **Arbetsflöden** på fliken **Åtgärder** i gruppen **Allmänt** väljer du **Skapa arbetsflöde från mall**.  
3.  Välj **Skapa arbetsflöde från mall** i gruppen **Allmänt** på fliken **Åtgärder**. Fönstret **arbetsflödesmallar**.  
4.  Markera arbetsflödesmallen Arbetsflöde för godkännande av inköpsorder och välj sedan **OK**.  

    Fönstret **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen. Värdet i fältet **Kod** utökas med ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen Arbetsflöde för godkännande av inköpsorder.  
5.  I huvudet i fönstret **Arbetsflöde** markerar du kryssrutan **Aktiverad**.  

## <a name="starting-a-notification-job-queue"></a>Starta en meddelandejobbkö  
Se till att en jobbkö i din installation är konfigurerad för att hantera arbetsflödesmeddelanden.  

### <a name="to-start-the-notify-job-queue"></a>Så här startar du jobbkön MEDDELA  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Jobbköer** och välj sedan relaterad länk.  
2.  I fönstret **Jobbköer** väljer du först raden för jobbkön MEDDELA, och på fliken **Start** i gruppen **Process**, välj **Starta jobbkö**.  

## <a name="using-the-approval-workflow"></a>Använda godkännandearbetsflödet  
Använd det nya arbetsflödet för godkännande av inköpsorder genom att först logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Alicia för att begära godkännande av en inköpsorder. Logga sedan in som dig själv, visa anteckningen i rollcentret, följ länken till godkännandebegäran och godkänn begäran.  

Om du logga in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som olika användare använder du funktionen **Kör som annan användare**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Så här loggar du in på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Alicia  

1.  För [!INCLUDE[d365fin](includes/d365fin_md.md)]-webbklienten använder du skift+högerklick på webbläsarens startknapp för webbsidan, och väljer sedan **Kör som en annan användare**.  

    För [!INCLUDE[d365fin](includes/d365fin_md.md)]-Windowsklienten använder du skift+högerklick på programmets startknapp för webbsidan, och väljer sedan **Kör som en annan användare**.  

2.  I fönstret **Windows-säkerhet** anger du [DATORNAMN]ALICIA och det lösenord som krävs.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Så här begär du godkännande av en inköpsorder, som Alicia.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsorder** och välj sedan relaterad länk.  
2.  Markera raden öppen inköpsorder 104001 och på fliken **Start** i gruppen **Hantera** väljer du **Redigera**.  
3.  I fönstret **Inköpsorder** på fliken **Åtgärder** i gruppen **Godkännande**, välj **Skicka godkännandebegäran**.  

    Observera att värdet i fältet **Status** har ändrats till **Väntar på godkännande**.  

4.  Stäng [!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>Så här godkänner du inköpsordern, som Sean  

1.  Öppna [!INCLUDE[d365fin](includes/d365fin_md.md)] som vanligt. Programmet öppnas med dig som användare.  
2.  Sök efter ett nytt meddelande från Alicia i Rollcentret i fönstret **Mina meddelanden**.  

    > [!NOTE]  
    >  Även om meddelandets upprepning har ställts in på **Omedelbart** anländer meddelandet omkring en minut efter att Alicia har skickat godkännandebegäran. Det beror på standardinställningen för återkommandefrekvensen för funktionen Jobbkö.  

3.  När meddelandet visas i fönstret **Mina meddelanden** väljer du värdet **Godkännandetransaktion: XX, XX** i fältet **Sida**. Fönstret **Begäranden att godkänna** öppnas med Alicias begäran om den markerade inköpsordern.  
4.  I fönstret **Begäranden att godkänna** på fliken **Start** i gruppen **Process** väljer du **Godkänna**.  

    Värdet i fältet **Status** på Alicias inköpsorder ändras till **Släppt**.  

Du har nu ställt in och testat ett enkelt godkännandearbetsflöde som baseras på de två första stegen i arbetsflödet Arbetsflöde för godkännande av inköpsorder. Det är enkelt att utöka arbetsflödet så att det automatiskt bokför Alicias inköpsorder när Sean godkänner den. För att göra det måste du aktivera arbetsflödet Arbetsflöde för godkännande av inköpsorder, där svaret på en släppt inköpsfaktura är att bokföra den. Först måste du ändra händelsevillkoret i det första arbetsflödessteget från (inköp) **Faktura** till **Order**.  

Den generiska versionen [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett antal arbetsflödesmallar för scenarier som stöds av programkoden. De flesta är för godkännandearbetsflöden. Mer information finns i Arbetsflödesmallar.  

Du definierar arbetsflödesvariationer genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. (Mer information finns i [Så här skapar du arbetsflöde](across-how-to-create-workflows.md).)  

Om ett företagsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds måste en Microsoft-partner implementera dem genom att anpassa applikationskoden. Mer information finns i [genomgång: genomföra nya arbetsflödeshändelser och svar](https://msdn.microsoft.com/en-us/library/mt574349.aspx) på MSDN.  

## <a name="see-also"></a>Se även  
[Så här konfigurerar du godkännandeanvändare](across-how-to-set-up-approval-users.md)   
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
[Så här skapar du arbetsflöden](across-how-to-create-workflows.md)   
[Så här använder du godkännande av arbetsflöden](across-how-use-approval-workflows.md)   
[Arbetsflöde](across-workflow.md)


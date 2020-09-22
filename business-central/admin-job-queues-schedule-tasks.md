---
title: Schemalägga jobb att köras automatiskt | Microsoft Docs
description: Schemalagda aktiviteter hanteras av jobbkön. Dessa jobb kör rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/09/2020
ms.author: edupont
ms.openlocfilehash: 6816ba11203e697ff833b9ea96aa85139fbcffe9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783607"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Använda jobbköer för att schemalägga uppgifter

Med jobbköer i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan användarna schemalägga och köra specifika rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande. Exempelvis vill du kanske köra rapporten **Salesperson * Sales Statistics** veckovis i syfte att spåra en säljares säljaktivitet varje vecka, eller också kanske du vill köra codeunit **Delegate Approval Requests** dagligen i syfte att förhindra att dokument ansamlas eller på annat sätt blockerar arbetsflödet.

Sidan **Jobbkötransaktioner** fönstret visas alla aktuella jobb. Om du lägger till en ny jobbkötransaktion som du vill schemalägga, måste du ange information om typen av objekt du vill köra, till exempel en rapport eller kodenhet för objekttypen, namnet och objekt-ID för objektet som ska köras. Du kan också lägga till parametrar för att ange beteendet för jobbkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder. Du måste ha behörighet att köra en viss rapport eller kodenhet, annars returneras ett fel när jobbkön körs.  

En jobbkö kan ha många transaktioner, som är de projekt som dokumentkön hanterar och kör. Information i transaktionen anger vilken rapport eller kodenhet som körs, när och hur ofta transaktionen körs, i vilken kategori projekt löper, och hur det körs.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Att ställa in bakgrundsbokföring med jobbköer

Jobbköer är ett effektivt verktyg som schemalägger körning av affärsprocesser i bakgrunden, till exempel när flera användare prövar att bokföra försäljningsorder, men endast en order kan behandlas i taget.  

Nedan beskrivs hur du ställer in bakgrundsbokföring av försäljningsorder. Stegen är liknande för inköp.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Försäljningsinställningar** och välj sedan relaterad länk.
2. På sidan **Försäljningsinställningar** markerar du kryssrutan **Bokför med jobbkö**.
3. Välj fältet **Kategorikod för jobbkod** och ange sedan koden för **SÄLJSPOST**.

    > [!NOTE]
    > Vissa jobb ändrar samma data och bör inte köras samtidigt på grund av att det kan orsaka konflikter. Bakgrundsjobb för försäljningsdokument kommer till exempel att försöka ändra samma data på samma gång. Jobbkökategorier förhindrar dessa typer av konflikter genom att säkerställa att ett annat jobb som tillhör samma jobbkö inte körs förrän det är klart. Till exempel väntar ett jobb som tillhör en försäljningsjobbkökategori tills alla andra relaterade försäljningsjobb är klara. Du anger en kategori för jobbkö på snabbfliken **Bakgrundsbokföring** på sidan **Försäljningsinställningar**.
    >
    > I [!INCLUDE[d365fin](includes/d365fin_md.md)] finns jobbkökategorier för försäljnings-, inköps- och redovisningsbokföring. Du bör alltid ange en av dessa, eller en som du själv skapar. Om du upplever fel på grund av konflikter kan du lägga upp en kategori för all bakgrundsbokföring av försäljning, inköp och redovisning.

    Om du även vill skriva ut försäljningsdokument när de är bokförda, markera kryssrutan **Bokför och skriv ut med jobbkön** på sidan **Försäljningsinställningar**.  

    > [!IMPORTANT]  
    > Om du ställer in ett jobb som ska bokföra och skriva ut dokument och skrivaren visar en dialogruta, exempelvis en begäran för autentiseringsuppgifter eller en varning om låg bläcknivå, bokförs dokumentet men skrivs inte ut. Motsvarande jobbköpost gör slutligen timeout, och **Status** fältet anges till **Fel**. Därmed rekommenderar vi att du inte använder en skrivarinställning som kräver interaktioner med skrivaredialogrutor tillsammans med bakgrundsbokföring.

    Nästa gång du publicerar säljdokument kommer [!INCLUDE [prodshort](includes/prodshort.md)] automatiskt att skapa en jobbköpost för respektive dokument och köra jobben individuellt i bakgrunden.

4. Bokför en försäljningsorder för att verifiera att jobbkön arbetar som förväntat. Mer information finns i [Sälja produkter](sales-how-sell-products.md).

5. Granska på sidan **Loggtransaktioner för jobbkö** om försäljningsordern har bokförts. Mer information finns i [Visa status eller fel i jobbkön](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Skapa en jobbkötransaktion för batchbokföring av försäljningsorder

Alternativt kan du även skjuta upp publiceringar till när tillfället passar din organisation bättre. Inom ditt företag kanske det exempelvis passar bättre att köra vissa rutiner när merparten av datainmatningen har slutförts för dagen. Du gör detta genom att konfigurera jobbkön så att denna kör diverse masspubliceringsrapporter, exempelvis **Masspublicera säljorder**, **Masspublicera säljfakturor** och liknande rapporter. [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder bokföring i bakgrunden för alla försäljnings-, inköps- och servicedokument.

Följande förfarande visar hur du konfigurerar rapporten **Masspublicera säljordrar** så att denna automatiskt publicerar säljordrar klockan 16.00 på veckodagar.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **jobbkötransaktioner** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **objekttyp som ska köras** väljer du **Rapport**.  
4. I fältet **Objekt-ID som ska köras** väljer du 296, **Batch-bokför förs.order**.

   Du kan också använda följande rapporter:
  
   * 900 **Masspublicera monteringsordrar**
   * 497 **Masspublicera inköpsfakturor**
   * 496 **Masspublicera inköpsordrar**
   * 498 **Masspublicera kreditköpsnotor**
   * 6665 **Masspublicera köpreturordrar**
   * 298 **Masspublicera kreditsäljnotor**
   * 297 **Masspublicera säljfakturor**
   * 296 **Masspublicera säljordrar**
   * 6655 **Masspublicera säljreturordrar**
   * 6005 **Masspublicera kredittjänstnotor**
   * 6004 **Masspublicera tjänstefakturor**
   * 6001 **Masspublicera tjänsteordrar**

5. Markera kryssrutan **Rapportbegäransida**.
6. På begäransidan **batch-bokföra försäljningsorder** definierar du vad som ska tas med vid automatisk bokföring av försäljningsorder och väljer knappen **OK**.

    > [!IMPORTANT]
    > Kom ihåg att ange strikta filter - i annat fall kommer [!INCLUDE [prodshort](includes/prodshort.md)] att publicera samtliga dokument, även om dessa inte är färdiga. Överväg att applicera ett filter på fältet **Status** för värdet *Släppts*, samt ett filter på fältet **Publiceringsdatum** för värdet *..idag*. Mer information finns i [Sortera, söka och filtrera](ui-enter-criteria-filters.md).
7. Markera de relevanta kryssrutorna från **kör på måndagar** till **kör på fredagar**.
8. I fältet **starttid** anger du kl. 16:00.
9. Välj åtgärden **Ställ in status till klar**.

Säljordrar som befinner sig inom ramarna för definierade filter kommer nu att publiceras varje veckodag kl. 16.00.

> [!NOTE]
> Om jobbkön inte kan bokföra försäljningsorder, ändras status till **Fel**, och försäljningsordern läggs till listan över försäljningsorder som användaren måste att hantera manuellt. Mer information finns i [Visa status eller fel i jobbkön](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

När jobbköer är inställda och körs kan status ändras enligt följande inom varje återkommande period:

* **Stoppad**  
* **Klar**  
* **Pågående**  
* **Fel**  
* **Avslutad**  

När ett projekt har slutförts korrekt, tas det bort från listan över jobbkötransaktioner, om det inte är ett återkommande projekt. Om det är ett återkommande projekt justeras fältet **tidigaste starttiden** till att visa nästa gång projektet förväntas köras.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Så här visar du status eller fel i jobbkön
Data som skapas när en jobbkö körs lagras i databasen, så att du kan felsöka jobbköfel.

### <a name="to-view-status-for-any-job"></a>Så här visar du status för ett projekt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **jobbkötransaktioner** och välj sedan relaterad länk.
2. På sidan **jobbkötransaktioner** väljer du en jobbkötransaktion, och väljer sedan åtgärden **loggposter**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Så här visar du status från ett försäljnings- eller inköpsdokument
1. I dokumentet som du har försökt publicera med bakgrundspublicering väljer du fältet **Status för jobbkö**, som innehåller **Fel**.
2. Granska felmeddelande och lös problemet.

## <a name="the-my-job-queue-part"></a>Min jobbködel
I **Min jobbködel** i ditt rollcenter visas de jobbköer som du har inlett men som ännu inte slutfört. Som standard visas inte delen, så du behöver lägga till den i ditt rollcenter. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).  

I den här delen kan du se dokument med ditt ID i fältet **Tilldelat användar-ID** so behandlas eller står i kö, inklusive de som är relaterade till bakgrundsbokföring. Här ser du snabbt om det har uppstått ett fel i bokföringen av ett dokument, eller om det finns fel i en jobbkötransaktion. Delen ger dig också möjlighet att makulera en dokumentbokföring, om den inte körs.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Så här kan du visa ett fel från delen Min jobbkö
1. På en transaktion med statusen **fel**, väljer du åtgärden **Visa felet**.
2. Granska felmeddelande och lös problemet.

## <a name="security"></a>Säkerhet  
Jobbkötransaktioner körs baserat på behörigheter. De behörigheterna måste tillåta att rapporten eller kodmodulen körs.  

När en jobbkö aktiveras manuellt, körs den med autentiseringsuppgifterna för den användaren. När en jobbkö aktiveras som en schemalagd uppgift, körs den med autentiseringsuppgifterna för serverinstansen. När ett jobb körs, körs det med autentiseringsuppgifterna för jobbkön som aktiverar det. Dock, måste användaren som skapade den jobbkötransaktionen, även ha behörigheter. När ett jobb "körs i användarsession" (exempelvis i samband med bakgrundspublicering) körs det med autentiseringsuppgifterna för den användare som startat jobbet.  

> [!IMPORTANT]  
> Om du använder behörighetsuppsättningen SUPER som följer med demolicensen för [!INCLUDE[d365fin](includes/d365fin_md.md)], har du och dina användare behörigheter att köra alla artiklar. I det här fallet begränsas tillgång för varje användare endast av behörighet för data.  

## <a name="using-job-queues-effectively"></a>Använda jobbköer effektivt  
Jobbkötransaktionsposten har flera fält för att överföra parametrar till en kodmodul som du har angett ska köras med en jobbkö. Det innebär att även kodenheter, som ska köras via jobbkön, måste anges med jobbkötransaktionsposten som en parameter i utlösaren **OnRun**. Det hjälper till att ge ytterligare en nivå av säkerhet, eftersom det hindrar användare från att köra slumpmässiga kodmoduler via jobbkön. Om användaren måste överföra parametrar till en rapport, är det enda sättet att göra det att låta rapportkörningen ingå i en kodmodul, som sedan analyserar inparametrarna och anger dem i rapporten, innan den körs.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Schemalägga synkronisering mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)]

Om du har integrerat [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)] kan du använda jobbkön för att schemalägga när du vill synkronisera data för de poster som du har sammankopplat i de två företagsapparna.. Beroende på den riktning och de regler som du har definierat för integreringen kan synkroniseringsjobbet också skapa nya poster i målappen som matchar dem i källan. Om t.ex. en säljare skapar en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)] kan synkroniseringsschemat skapa kontakten för den kopplade säljaren i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer finns i [Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## <a name="see-also"></a>Se även

[Administration](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  

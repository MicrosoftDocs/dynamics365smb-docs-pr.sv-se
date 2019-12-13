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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: abca7de7ce91ebe32e8c17a2288c49684b53455c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879208"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Använda jobbköer för att schemalägga uppgifter
Med jobbköer i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan användarna schemalägga och köra specifika rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande. Du kanske till exempel vill köra rapporten **Säljare försäljningsstatistik** varje vecka, för att spåra försäljningen per säljare under en vecka, eller så kanske du vill köra kodenheten **E-postkö för bearbetningstjänst** dagligen, för att vara säker på att aktuella e-postmeddelanden till kunder angående deras serviceorder skickas ut i tid.

Sidan **Jobbkötransaktioner** fönstret visas alla aktuella jobb. Om du lägger till en ny jobbkötransaktion som du vill schemalägga, måste du ange information om typen av objekt du vill köra, till exempel en rapport eller kodenhet för objekttypen, namnet och objekt-ID för objektet som ska köras. Du kan också lägga till parametrar för att ange beteendet för jobbkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder. Du måste ha behörighet att köra en viss rapport eller kodenhet, annars returneras ett fel när jobbkön körs.  

En jobbkö kan ha många transaktioner, som är de projekt som dokumentkön hanterar och kör. Information i transaktionen anger vilken rapport eller kodenhet som körs, när och hur ofta transaktionen körs, i vilken kategori projekt löper, och hur det körs.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Att ställa in bakgrundsbokföring med jobbköer
Jobbköer är ett effektivt verktyg som schemalägger körning av affärsprocesser i bakgrunden, till exempel när flera användare prövar att bokföra försäljningsorder, men endast en order kan behandlas i taget. Alternativt kan du behöva planera bokföringar vid tidpunkter när det passar organisationen. Det kan till exempel passa bra för din verksamhet att köra vissa rutiner, när den mesta datainmatningen för dagen har slutförts.

Detta åstadkommer du genom att ställa in jobbkön till att köra olika batch-bokföringsrapporter som t.ex. **batch-bokför förs.order**, **batch-bokför försäljningsfakturor**, **batch-bokför förs.returorder** och **batch-bokför försäljningskreditnotor**. Mer information finns i [Att skapa en jobbkötransaktion för bakgrundsbokföring av försäljningsorder](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] stöder bokföring i bakgrunden för alla försäljnings-, inköps- och servicedokument.

Nedan beskrivs hur du ställer in bakgrundsbokföring av försäljningsorder. Momenten är liknande för inköp och en service.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsinställningar** och välj sedan relaterad länk.
2. På sidan **Försäljningsinställningar** markerar du kryssrutan **Bokför med jobbkö**.
3. Välj fältet **Kategorikod för jobbkö** och välj kategorin **FÖRSBOKF** för att filtrera till jobbkötransaktioner för bokföring av försäljningsorder.

    Ett jobbköobjekt, codeunit 88 **försäljningspost via jobbkö**, har skapats. Fortsätt med att aktivera den på sidan **jobbkötransaktioner**.
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **jobbkötransaktioner** och välj sedan relaterad länk.
5. På sidan **jobbkötransaktioner** väljer du åtgärden **ny**.
6. I fältet **objekttyp som ska köras** väljer du **Codeunit**.  
7. I fältet **Objekt-ID som ska köras** väljer du 88, **försäljningspost via jobbkö**.

    Inga andra fält som är relevanta för det här scenariot.
8. Välj åtgärden **Ställ in status till klar**.
9. Bokför en försäljningsorder för att verifiera att jobbkön arbetar som förväntat. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
10. Granska på sidan **Loggtransaktioner för jobbkö** om försäljningsordern har bokförts. Mer information finns i [Visa status eller fel i jobbkön](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Om du även vill skriva ut försäljningsdokument när de är bokförda, markera kryssrutan **Bokför och skriv ut med jobbkön** på sidan **Försäljningsinställningar**.  

> [!IMPORTANT]  
> Om du ställer in ett jobb som ska bokföra och skriva ut dokument och skrivaren visar en dialogruta, exempelvis en begäran för autentiseringsuppgifter eller en varning om låg bläcknivå, bokförs dokumentet men skrivs inte ut. Motsvarande jobbköpost gör slutligen timeout, och **Status** fältet anges till **Fel**. Därmed rekommenderar vi att du inte använder en skrivarinställning som kräver interaktioner med skrivaredialogrutor tillsammans med bakgrundsbokföring.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Skapa en jobbkötransaktion för batchbokföring av försäljningsorder
I följande procedur beskrivs hur du ställer in rapporten **batch-bokföra försäljningsorder** till att automatiskt bokföra släppta försäljningsorder klockan 16:00 på veckodagar.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **jobbkötransaktioner** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **objekttyp som ska köras** väljer du **Rapport**.  
4. I fältet **Objekt-ID som ska köras** väljer du 296, **Batch-bokför förs.order**.
5. Markera kryssrutan **Rapportbegäransida**.
6. På begäransidan **batch-bokföra försäljningsorder** definierar du vad som ska tas med vid automatisk bokföring av försäljningsorder och väljer knappen **OK**.
7. Markera de relevanta kryssrutorna från **kör på måndagar** till **kör på fredagar**.
8. I fältet **starttid** anger du kl. 16:00.
9. Välj åtgärden **Ställ in status till klar**.

Försäljningsorder som är redo att bokföras kommer nu att bokföras varje veckodag klockan 16:00.

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
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **jobbkötransaktioner** och välj sedan relaterad länk.
2. På sidan **jobbkötransaktioner** väljer du en jobbkötransaktion, och väljer sedan åtgärden **loggposter**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Så här visar du status från ett försäljnings- eller inköpsdokument
1. Från det dokument som du har provat att bokföra med jobbkön, väljer du fältet **Status för jobbkö** som innehåller **fel**.
2. Granska felmeddelande och lös problemet.

## <a name="the-my-job-queue-part"></a>Min jobbködel
I **Min jobbködel** i ditt rollcenter visas de jobbköer som du har inlett men som ännu inte slutfört. Som standard visas inte delen, så du behöver lägga till den i ditt rollcenter. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

I den här delen kan du se dokument med ditt ID i fältet **Tilldelat användar-ID** so behandlas eller står i kö, inklusive de som är relaterade till bakgrundsbokföring. Här ser du snabbt om det har uppstått ett fel i bokföringen av ett dokument, eller om det finns fel i en jobbkötransaktion. Delen ger dig också möjlighet att makulera en dokumentbokföring, om den inte körs.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Så här kan du visa ett fel från delen Min jobbkö
1. På en transaktion med statusen **fel**, väljer du åtgärden **Visa felet**.
2. Granska felmeddelande och lös problemet.

## <a name="security"></a>Säkerhet  
Jobbkötransaktioner körs baserat på behörigheter. De behörigheterna måste tillåta att rapporten eller kodmodulen körs.  

När en jobbkö aktiveras manuellt, körs den med autentiseringsuppgifterna för den användaren. När en jobbkö aktiveras som en schemalagd uppgift, körs den med autentiseringsuppgifterna för serverinstansen. När ett jobb körs, körs det med autentiseringsuppgifterna för jobbkön som aktiverar det. Dock, måste användaren som skapade den jobbkötransaktionen, även ha behörigheter. När ett jobb är Kör i användarsession (till exempel i bakgrundsbokföring), körs det med autentiseringsuppgifterna för den användare som skapade jobbet.  

> [!IMPORTANT]  
>  Om du använder behörighetsuppsättningen SUPER som följer med demolicensen för [!INCLUDE[d365fin](includes/d365fin_md.md)], har du och dina användare behörigheter att köra alla artiklar. I det här fallet begränsas tillgång för varje användare endast av behörighet för data.  

## <a name="using-job-queues-effectively"></a>Använda jobbköer effektivt  
Jobbkötransaktionsposten har flera fält för att överföra parametrar till en kodmodul som du har angett ska köras med en jobbkö. Det innebär att även kodenheter, som ska köras via jobbkön, måste anges med jobbkötransaktionsposten som en parameter i utlösaren **OnRun**. Det hjälper till att ge ytterligare en nivå av säkerhet, eftersom det hindrar användare från att köra slumpmässiga kodmoduler via jobbkön. Om användaren måste överföra parametrar till en rapport, är det enda sättet att göra det att låta rapportkörningen ingå i en kodmodul, som sedan analyserar inparametrarna och anger dem i rapporten, innan den körs.  

## <a name="scheduling-synchronization-between-included365finincludesd365fin_mdmd-and-includecrm_mdincludescrm_mdmd"></a>Schemalägga synkronisering mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)]
Om du har integrerat [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] kan du använda jobbkön för att schemalägga när du vill synkronisera data för de poster som du har kopplat till de två affärsprogrammen. Beroende på riktningen och reglerna som du har definierat för integrationen kan du också skapa nya poster i mål appen för att matcha dem i källan med synkroniseringsjobb. Om t.ex. en säljare skapar en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)] kan synkroniseringsschemat skapa kontakten för den kopplade säljaren i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Schemalägga en synkronisering mellan Business Central och Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)

## <a name="see-also"></a>Se även  
[Administration](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  

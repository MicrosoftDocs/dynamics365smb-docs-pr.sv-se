---
title: "Schemalägga jobb att köras automatiskt | Microsoft Docs"
description: "Schemalagda aktiviteter hanteras av jobbkön. Dessa jobb kör rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 05d2941d5124f333602cb2f73103389601ff3e85
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Använda jobbköer för att schemalägga uppgifter
Med jobbköer i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan användarna schemalägga och köra specifika rapporter och kodenheter. Du kan ange att jobb ska köras en gång eller återkommande. Du kanske till exempel vill köra rapporten **Säljare försäljningsstatistik** varje vecka, för att spåra försäljningen per säljare under en vecka, eller så kanske du vill köra kodenheten **E-postkö för bearbetningstjänst** dagligen, för att vara säker på att aktuella e-postmeddelanden till kunder angående deras serviceorder skickas ut i tid.  

## <a name="add-jobs-to-the-job-queue"></a>Lägg till jobb till jobbkön
Fönstret **Jobbkötransaktioner** fönstret visas alla aktuella jobb. Om du lägger till en ny jobbkötransaktion som du vill schemalägga, måste du ange information om typen av objekt du vill köra, till exempel en rapport eller kodenhet för objekttypen, namnet och objekt-ID för objektet som ska köras. Du kan också lägga till parametrar för att ange beteendet för jobbkötransaktionen. Du kan t.ex lägga till en planeringsparameter om att endast skicka bokförda försäljningsorder. Du måste ha behörighet att köra en viss rapport eller kodenhet, annars returneras ett fel när jobbkön körs.  

I fältet **Kategorifilter för jobbkö** kan du ange ett filter. Du kan använda jobbkökategorier för jobb i listan.

[!INCLUDE[d365fin](includes/d365fin_md.md)] kör automatiskt projekt efter angivna scheman för varje jobbkötransaktion. Du kan starta, stoppa och spärra en jobbkötransaktion manuellt.

### <a name="log-files"></a>Loggfiler
Fel visas i **loggtransaktioner för jobbkö** som du når från menyfliken. Du kan också felsöka fel i jobbkön. Data som skapas när en jobbkö körs sparas i databasen.  

### <a name="background-posting-with-job-queues"></a>Bakgrundsbokföring med jobbköer
Jobbköer är ett effektivt verktyg som schemalägger körning av affärsprocesser i bakgrunden. Det kan till exempel finnas en instans då flera användare som prövar att bokföra försäljningsorder samtidigt, men endast en order kan behandlas i taget. Genom att skapa en rutinmässig bakgrundsbokföring, kan du markera transaktionerna i en kö för att bearbeta dem i bakgrunden.  

 Alternativt kan du behöva planera bokföringar vid tidpunkter när det passar organisationen. Det kan till exempel passa bra för din verksamhet att köra vissa rutiner, när den mesta datainmatningen för dagen har slutförts. Detta åstadkommer du genom att ställa in jobbkön till att köra olika batch-bokföringsrapporter som t.ex. **Batch-bokför förs.order**, **batch-bokför försäljningsfakturor**, och **batch-bokför försäljningskreditnotor** rapporter.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)]  stöder bokföring i bakgrunden för följande dokumenttyper:  

-   Försäljning: försäljningsorder, returorder, kreditnota, faktura  

-   Inköp: inköpsorder, returorder, kreditnota, faktura  

 Om jobbkön inte kan bokföra försäljningsorder, ändras status till **Fel**, och försäljningsordern läggs till listan över försäljningsorder som användaren måste att hantera.  

> [!NOTE]  
>  När du schemalägger ett dokument för att bokföra, och bokföringsprocessen börjar, konfigureras bokföringsrutinen för automatisk timeout inom två timmar, om bokföringsrutinen slutar att svara.  

Du ställer in den här användningen av jobbkön i fönstret **Försäljningsinställningar** eller **inköp** respektive. På snabbfliken **bakgrundsbokföring** väljer du **Bokföra dokument via jobbkö** och sedan fyller du i relevant information. Här kan du även använda **Kategorikod för jobbkö** för att köra alla jobbkötransaktioner med samma kod. Du kan t.ex. använda kategorin **SalesPost** som filtrerar fram alla försäljningsorder som matchar en jobbkö med samma kategorikod.  

> [!IMPORTANT]  
>  Om du ställer in ett jobb som ska bokföra och skriva ut dokument och skrivaren visar en dialogruta, exempelvis en begäran för autentiseringsuppgifter eller en varning om låg bläcknivå, bokförs dokumentet men skrivs inte ut. Motsvarande jobbköpost gör slutligen timeout, och **Status** fältet anges till **Fel**. Därmed rekommenderar vi att du inte använder en skrivarinställning som kräver interaktioner med skrivaredialogrutor tillsammans med bakgrundsbokföring.  

## <a name="use-the-my-job-queue-part"></a>Så här använder du Min jobbködel
I **Min jobbkö** visas de jobbköer som en användare har inlett men som ännu inte slutfört. Som standard visas inte delen, så du måste lägga till den i ditt rollcenter. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

I den här delen kan du se vilka dokument som behandlas eller står i kö om ditt ID har angetts i fältet **Tilldelat användar-ID**. Här får du hjälp att hålla reda på alla jobbkötransaktioner, inklusive de som relaterar till bokföring i bakgrunden. Här ser du snabbt om det har uppstått ett fel i bokföringen av ett dokument, eller om det finns fel i en jobbkötransaktion. Delen ger dig också möjlighet att makulera en dokumentbokföring, om den inte körs.  

## <a name="security"></a>Säkerhet  
Jobbkötransaktioner körs baserat på behörigheter. De behörigheterna måste tillåta att rapporten eller kodmodulen körs.  

När en jobbkö aktiveras manuellt, körs den med autentiseringsuppgifterna för den användaren. När en jobbkö aktiveras som en schemalagd uppgift, körs den med autentiseringsuppgifterna för serverinstansen. När ett jobb körs, körs det med autentiseringsuppgifterna för jobbkön som aktiverar det. Dock, måste användaren som skapade den jobbkötransaktionen, även ha behörigheter. När ett jobb är Kör i användarsession (till exempel i bakgrundsbokföring), körs det med autentiseringsuppgifterna för den användare som skapade jobbet.  

> [!IMPORTANT]  
>  Om du använder behörighetsuppsättningen SUPER som följer med demolicensen för [!INCLUDE[d365fin](includes/d365fin_md.md)], har du och dina användare behörigheter att köra alla artiklar. I det här fallet begränsas tillgång för varje användare endast av behörighet för data.  

## <a name="using-job-queues-effectively"></a>Använda jobbköer effektivt  
Jobbkötransaktionsposten har flera fält för att överföra parametrar till en kodmodul som du har angett ska köras med en jobbkö. Det innebär att även kodenheter, som ska köras via jobbkön, måste anges med jobbkötransaktionsposten som en parameter i utlösaren **OnRun**. Det hjälper till att ge ytterligare en nivå av säkerhet, eftersom det hindrar användare från att köra slumpmässiga kodmoduler via jobbkön. Om användaren måste överföra parametrar till en rapport, är det enda sättet att göra det att låta rapportkörningen ingå i en kodmodul, som sedan analyserar inparametrarna och anger dem i rapporten, innan den körs.  

## <a name="see-also"></a>Se även  
[Installation och administration i Business Central](admin-setup-and-administration.md)  
[Ställa in Business Central](setup.md)  


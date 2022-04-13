---
title: Bokföra flera dokument på samma gång
description: Så här väljer du flera icke-bokförda dokument i en lista för direkt eller tidsplanerad batch-bokföring i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.reviewer: edupont
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 357a4a8d1eba62c3619439558cf81a5fc19f0963
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515985"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bokföra flera dokument på samma gång

I stället för att bokföra enskilda dokument var för sig kan du välja flera icke bokförda dokument i en lista för direkt bokföring eller för batch-bokföring enligt ett schema, t. ex. i slutet av dagen. Detta kan vara användbart om endast en ansvarig kan bokföra dokument som skapats av andra användare eller undvika problem med system prestanda vid bokföring under arbetstid.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Så här bokför du flera inköpsorder direkt

I proceduren nedan beskrivs hur du bokför flera inköpsorder direkt. Stegen är liknande för alla ingående och utgående dokument.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:
3. I fältet **Nr.** väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.
4. Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.
5. Välj åtgärden **bokföra** och välj sedan åtgärden **bokför**.
6. Välj knappen **Ja** på bekräftelsemeddelandet.

## <a name="to-batch-post-multiple-purchase-orders"></a>Så här bokför du flera inköpsorder

I proceduren nedan beskrivs hur du bokför flera inköpsorder. Stegen är liknande för alla inköps- och försäljningsdokument där åtgärden **batch-bokföring** är tillgänglig.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2. På sidan **inköpsorder** går du vidare för att välja alla order som ska bokföras:
3. I fältet **Nr.** väljer du de tre lodräta punkterna för att öppna snabbmenyn och sedan väljer du åtgärden **Välj fler**.
4. Markera kryssrutan för alla rader som motsvarar order som du vill bokföra samtidigt.
5. Välj åtgärden **bokföra** och välj sedan åtgärden **Bokför batch-jobb**.
6. På sidan **Batch-bokför inköpsorder** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Välj **OK**.
8. Om du vill visa potentiella problem som uppstod vid batch-bokföring av dokument öppnar du fönstret **registrera felmeddelande**.

> [!NOTE]
> Det kan ta en stund att bokföra flera dokument och samtidigt blockera andra användare. Överväg att aktivera bakgrundsbokföring. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>Att ställa in bakgrundsbokföring med jobbköer
Projektköer är ett effektivt verktyg som schemalägger körning av affärsprocesser i bakgrunden, till exempel när flera användare försöker bokföra försäljningsorder men endast en order i taget kan bearbetas.  

Nedan beskrivs hur du ställer in bakgrundsbokföring av försäljningsorder. Stegen är liknande för inköp.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.
2. På sidan **Försäljningsinställningar** markerar du kryssrutan **Bokför med jobbkö**.
3. Välj fältet **Kategorikod för jobbkod** och ange sedan koden för **SÄLJSPOST**.

    > [!NOTE]
    > Vissa jobb ändrar samma data och bör inte köras samtidigt på grund av att det kan orsaka konflikter. Bakgrundsjobb för försäljningsdokument kommer till exempel att försöka ändra samma data på samma gång. Projektkökategorier förhindrar dessa typer av konflikter genom att säkerställa att ett annat jobb som tillhör samma jobbkö inte körs förrän det är klart. Till exempel väntar ett jobb som tillhör en försäljningsjobbkökategori tills alla andra relaterade försäljningsjobb är klara. Du anger en kategori för jobbkö på snabbfliken **Bakgrundsbokföring** på sidan **Försäljningsinställningar**.
    >
    > I [!INCLUDE[prod_short](includes/prod_short.md)] finns jobbkökategorier för försäljnings-, inköps- och redovisningsbokföring. Du bör alltid ange en av dessa, eller en som du själv skapar. Om du upplever fel på grund av konflikter kan du lägga upp en kategori för all bakgrundsbokföring av försäljning, inköp och redovisning.

    Om du även vill skriva ut försäljningsdokument när de är bokförda, markera kryssrutan **Bokför och skriv ut med jobbkön** på sidan **Försäljningsinställningar**.  
    Om du väljer **PDF** i fältet **Rapportutdatatyp**, kommer bokförda inköpsorder vara tillgängliga i delen **rapportinkorg** i rollcentret.

    > [!IMPORTANT]  
    > Om du ställer in ett jobb som ska bokföra och skriva ut dokument och skrivaren visar en dialogruta, exempelvis en begäran för autentiseringsuppgifter eller en varning om låg bläcknivå, bokförs dokumentet men skrivs inte ut. Motsvarande jobbköpost gör slutligen timeout, och **Status** fältet anges till **Fel**. Därmed rekommenderar vi att du inte använder en skrivarinställning som kräver interaktioner med skrivaredialogrutor tillsammans med bakgrundsbokföring.

    Nästa gång du publicerar säljdokument kommer [!INCLUDE [prod_short](includes/prod_short.md)] automatiskt att skapa en jobbköpost för respektive dokument och köra jobben individuellt i bakgrunden.

4. Bokför en försäljningsorder för att verifiera att jobbkön arbetar som förväntat. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
    Försäljningsordern läggs nu till i en särskild jobbkötransaktion som definierar när dokumenten bokförs. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Så här visar du status från ett försäljnings- eller inköpsdokument
Om jobbkön inte kan bokföra försäljningsorder, ändras status till **Fel**, och försäljningsordern läggs till listan över försäljningsorder som användaren måste att hantera manuellt.
1. I dokumentet som du har försökt publicera med bakgrundspublicering väljer du fältet **Status för jobbkö**, som innehåller **Fel**.
2. Granska felmeddelandet och lös problemet.

Alternativt kan du också granska sidan **Loggtransaktioner för jobbkö** om försäljningsordern har bokförts. Mer information finns i avsnittet [Övervaka jobbkön](#monitor-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Skapa en jobbkötransaktion för batchbokföring av försäljningsorder

Alternativt kan du även skjuta upp publiceringar till när tillfället passar din organisation bättre. Inom ditt företag kanske det exempelvis passar bättre att köra vissa rutiner när merparten av datainmatningen har slutförts för dagen. Du gör detta genom att konfigurera jobbkön så att denna kör diverse masspubliceringsrapporter, exempelvis **Masspublicera säljorder**, **Masspublicera säljfakturor** och liknande rapporter. [!INCLUDE[prod_short](includes/prod_short.md)] stöder bokföring i bakgrunden för alla försäljnings-, inköps- och servicedokument.

Följande förfarande visar hur du konfigurerar rapporten **Massbokför försäljningsorder** så att denna automatiskt bokför försäljningsorder klockan 16.00 på vardagar.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **jobbkötransaktioner** och välj sedan relaterad länk.  
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
    > Kom ihåg att ange strikta filter – i annat fall kommer [!INCLUDE [prod_short](includes/prod_short.md)] att publicera samtliga dokument, även om dessa inte är färdiga. Överväg att applicera ett filter på fältet **Status** för värdet *Släppts*, samt ett filter på fältet **Publiceringsdatum** för värdet *..idag*. Mer information finns i [Sortera, söka och filtrera](ui-enter-criteria-filters.md).
7. Markera de relevanta kryssrutorna från **kör på måndagar** till **kör på fredagar**.
8. I fältet **starttid** anger du kl. 16:00.
9. Välj åtgärden **Ställ in status till klar**.

Försäljningsorder som befinner sig inom ramarna för definierade filter kommer nu att bokföras varje vardag kl. 16.00.

## <a name="monitor-the-job-queue"></a>Övervaka jobbkön

Om du konfigurerar bakgrundsbokföring med jobbköer gör du det till en vanlig uppgift för att övervaka jobbkön och uppmärksamma eventuella problem. Du kan spåra statusen på sidan **Jobbkötransaktioner**. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

Som administratör kan du använda [Application Insights](/azure/azure-monitor/app/app-insights-overview) för att samla in och analysera telemetri som du kan använda för att identifiera problem. Mer information finns i [Övervaka och analysera telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) i innehållet för utvecklare och administration.  

## <a name="see-also"></a>Se även

[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)  
[Redigera bokförda dokument](across-edit-posted-document.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
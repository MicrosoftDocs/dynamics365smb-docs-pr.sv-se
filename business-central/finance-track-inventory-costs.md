---
title: Spåra artikelkostnadsjusteringar
description: Läs om hur spårning av justeringar av artikelkostnader kan hjälpa dig att hålla artikelkostnadsdata korrekta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="track-item-cost-adjustments"></a>Spåra artikelkostnadsjusteringar

Det är viktigt att artikelkostnaderna är korrekta och att tiden förkortas från det att du bokför en transaktion tills kostnaden återspeglas i redovisningen. Du kan spåra resultatet av kostnadsjusteringarna för enskilda justeringskörningar och artiklar. Om fel inträffar kan du identifiera de problematiska artiklarna och göra korrigeringar. Du kan till exempel utesluta artiklarna från beräkningarna för att säkerställa att justeringar inte avbryts för andra artiklar. Du kan justera kostnader för enskilda artiklar eller skapa journaler med artiklar och justera dem samtidigt.

## <a name="start-tracking-cost-adjustments"></a>Börja spåra kostnadsjusteringar

Det är lätt att komma igång. På sidan **Lagerinställningar** erbjuder fältet **Loggning av kostnadsjustering** några alternativ:

* **Inaktiverad** innebär att du inte loggar kostnadsjusteringskörningar.
* **Endast fel** innebär att endast logga körningar som misslyckades.
* **Alla** innebär att logga alla körningar.

> [!NOTE]
> För att minimera loggens storlek loggar [!INCLUDE [prod_short](includes/prod_short.md)] inte de justeringar som sker automatiskt när någon bokför en artikel.

Du måste också ställa in jobbkötransaktionen **Bokför lagerkostnad i redov. (1002)**. Den här jobbkötransaktionen justerar automatiskt kostnaderna enligt ett schema. För att lära dig mer om jobbkötransaktioner, gå till [Använd jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="manage-cost-adjustments"></a>Hantera kostnadsjusteringar

Använd sidan **Kostnadsjustering av lager** för att hantera och övervaka kostnadsjusteringsprocessen. På den här sidan visas artiklarna tillsammans med deras kostnadsparametrar och kostnadsjusteringsstatus. Du kan filtrera listan så att den fokuserar på artiklar som behöver justeras eller som är undantagna från kostnadsjusteringsprocessen.

### <a name="about-item-batches"></a>Om artikelbatchar

Du kan köra kostnadsjustering för flera artiklar genom att gruppera dem i batchar. Batchar gör det enkelt att justera vissa artiklar separat, till exempel eftersom det tar längre tid att justera dem. Batchar kan också hjälpa till att identifiera artiklar som har problem.

Om du vill skapa en batch gör du något av följande på sidan **Justering av lagerkostnad**:

* Markera artiklarna i listan, välj **Kör kostnadsjustering** och välj sedan **Lägg till batch**.
* Om du vill skapa en batch och köra kostnadsjusteringen direkt markerar du artiklarna i listan, väljer du **Kör kostnadsjustering** och väljer sedan **Lägg till batch och kör**.
* Välj **Kör kostnadsjustering**, välj **Artikeljournaler** och ange sedan ett filter i fältet **Artikelfilter**.
  
> [!TIP]
> Om du snabbt vill skapa en ny batch för alla artiklar som inte redan ingår i en batch väljer du sidan **Kostnadsjustering – artikelbatchar** och sedan **Lägg till saknade artiklar**.

När en körning för en batch är klar har batchen har någon av följande statusar på sidan **Artikelbatchar**:

* **Klart**: Kostnadsjusteringen lyckades.
* **Misslyckades**: Om kostnadsjusteringen misslyckas identifierar [!INCLUDE [prod_short](includes/prod_short.md)] artikeln som orsakade felet och den aktuella batchen delas sedan upp i två. En batch med den problematiska artikeln och en annan med de återstående artiklarna. Kostnadsjusteringen körs på nytt för batchen med de återstående artiklarna. Om det misslyckas igen upprepas processen. Du definierar det maximala antalet delningar i fältet **Maximalt antal nya försök**. Standardvärdet för återförsök är 10, men du kan ange en ny gräns.
* **Tidsgränsen har nåtts**: Om kostnadsjusteringen för en batch inte har slutförs inom den period som anges i fältet **Tidsgräns (minuter)** (från 1 till 720 minuter) avslutas sessionen och ändringarna återställs. [!INCLUDE [prod_short](includes/prod_short.md)] delar sedan den aktuella batchen i hälften och kostnadsjusteringsprocessen körs på nytt för varje hälft. Den här processen fortsätter tills kostnadsjusteringen lyckas eller når maximalt antal försök igen.

> [TIPS!] Varje batch körs i en separat session. Om du vill övervaka förloppet använder du åtgärden **Uppdatera**.

### <a name="run-cost-adjustment"></a>Kör kostnadsjustering

Använd sidan **Kostnadsjustering av lager** för att göra justeringar.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kostnadsjustering av lager** och väljer sedan relaterad länk.
1. Beroende på vad du vill göra gör du med något av följande alternativ:

  * För en eller flera artiklar direkt markerar du artiklarna i listan och väljer sedan **Kör kostnadsjustering**.
  * För batcher använder du en av följande typer:

    * Om du vill skapa en batch och justera kostnader direkt väljer du artiklarna i listan och sedan **Kör kostnadsjustering** och väljer sedan **Lägg till batch och kör**.
    * Om du vill köra den för alla journaler väljer du **Kör kostnadsjustering**, **Artikelbatcher** och väljer sedan **Kör**.
    
    Mer information om batcher finns i [Om artikelbatchar](#about-item-batches).

### <a name="explore-item-details"></a>Utforska artikeldetaljer

Använd menyn **Artikel** menu för att få tillgång till information om kostnadsjusteringar för en vald artikel.

* **Artikeltransaktioner**: Visa en lista över artikeltransaktioner för artikeln. Med åtgärden **Markera för justering** kan du tvinga fram en omkörning av kostnadsjusteringar för artiklar som är direkt eller indirekt kopplade till de ingående transaktioner du väljer. Att tvinga fram en omkörning kan vara användbart om tidigare körningar ledde till felaktiga kostnader.
* **Värdetransaktioner**: Visa en lista över värdetransaktioner för artikeln.
* **Ingångspunkter för kostnadsjustering**: Öppna sidan **Ingångspunkt för genomsn.kostn.justering** som du främst använder för att beräkna genomsnittskostnaden. På sidan visas kombinationer av artiklar, lagerställen, varianter och värderingsdatum för vilka kostnadsjusteringar körs eller måste köras.
* **Kostnadsjusteringsorder**: Öppna sidan **Lagerjusteringstransaktion (order)** där du justerar produktions- och monteringsorder. Det visar att order är justerade eller behöver justeras.

### <a name="view-the-outcome"></a>Visa resultatet

Använd menyn **Logga per** för att visa resultatet av kostnadsjusteringar:

* **Kör**: Visa kostnadsjusteringsloggar för varje körning. Loggen innehåller data om artikelfiltret, status (lyckades/misslyckades/tidsgräns gått ut), start- och slutdatum/-tid, varaktighet och kostnadsskillnaderna som skapas av körningen.
* **Artikel**: Visa detaljerad information om justeringsprocessen för den valda artikeln.

### <a name="include-or-exclude-items-from-adjustments"></a>Inkludera eller exkludera artiklar från justeringar

Om ett eller flera objekt misslyckas kan du exkludera objekten från justeringskörningen och sedan inkludera dem i senare körningar. På menyn **Funktioner**, välj ett av följande:

* **Exkludera artikel från justering** och **Ta med artikel i justering**: Inaktivera tillfälligt och återaktivera sedan kostnadsjustering för en vald artikel. Kostnadsjusteringen fortsätter att hålla kostnaderna korrekta för andra artiklar medan du undersöker ett problem med en viss artikel.

## <a name="post-adjusted-costs-to-the-general-ledger"></a>Boka justerade kostnader till huvudboken

Vanligtvis bokförs nya värdetransaktioner i redovisningen enligt schemat för jobbkötransaktionen **Bokför lagerkostnad i redov. (1002)**. Du kan emellertid bokföra justeringar i redovisningen direkt från sidan **Kostnadsjustering av lager**. På menyn **Funktioner** väljer du **Bokför lagerkostnad i redov.**.

## <a name="troubleshoot-cost-adjustments"></a>Felsöka kostnadsjusteringar

Använd följande alternativ på menyn **Diagnostik** för att felsöka kostnadsjusteringskörningar.

* **Exportera artikeldata**: Exportera artikelrelaterade data till en textfil. Du kan använda filen för ytterligare analys i en miljö med begränsat läge eller koppla den till en supportbegäran när du undersöker problem med kostnadsberäkning.
* **Importera artikeldata**: Importera tillbaka den exporterade textfilen till databasen. Den här åtgärden är endast aktiverad i sandbox-miljöer eller utvärderingsföretag.
* **Återställ Kostnaden är justerad**: Återställ växlingsknappen **Kostnaden är justerad** för artiklar, produktionsorder eller monteringsorder. Med den här inställningen kan du tvinga fram en omkörning av kostnadsjusteringen för dem.
* **Rapport om identifiering av kostnadsproblem**: Diagnostisera typiska dataproblem som orsakar beräkningsfel vid kostnadsberäkning. Den kontrollerar om artikeltransaktionerna, värdetransaktionerna, artikelkopplingstransaktionerna och kapacitetstransaktionerna är korrekta.
* **Ta bort artikeldata**: Rensa alla artikelrelaterade tabeller i databasen. Den här åtgärden är endast tillgänglig i miljöer med begränsat läge eller utvärderingsföretag.

## <a name="see-also"></a>Se även

[Justera artikelkostnader](inventory-how-adjust-item-costs.md)  
[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)  

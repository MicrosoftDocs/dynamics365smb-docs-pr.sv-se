---
title: Ställ in företag att synkronisera huvuddata
description: Mer information om hur du ställer in ett eller flera företag för att synkronisera huvuddata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Kom i gång med synkronisering av huvuddata

När två eller flera företag använder en del av samma huvuddata kan du synkronisera data i stället för att lägga till dem manuellt i varje företag. Till exempel synkronisering av data är särskilt användbart när du ställer in nya dotterbolag.

Huvuddata omfattar inställningar och icke-transaktionell information om affärsentiteter. Till exempel kunder, leverantörer, artiklar och anställda. Data innehåller kontext för affärstransaktioner. Här följer några exempel på standarduppgifter för en kund:

* Name
* Identifieringsnummer
* Adress
* Betalningsvillkor
* Kreditgräns

Du sätter upp synkronisering i dotterbolagen. Genom att använda en pull-modell hämtar dotterbolagen data från det källföretag som de behöver göra affärer med. När du har ställt in synkroniseringen och synkroniserat data första gången är allt klart. Jobbköposter uppdaterar kopplade poster i dotterbolagen när någon ändrar data i källföretaget.

## Endast enkelriktad synkronisering

Du kan endast synkronisera data från källföretaget till dotterbolag med pullmetod. Dotterbolag kan inte skicka data till källföretaget.

> [!NOTE]
> Även om det är möjligt rekommenderar vi inte att du konfigurerar dubbelriktad synkronisering. Det vill säga att datasynkroniseras från källföretaget till dotterbolagen och från dotterbolagen till källföretaget. Om du synkroniserar data i båda riktningarna kan konflikter eller oönskade överskrivningar uppstå.

## Innan du börjar

Följande är krav för att ställa in synkronisering.

* Alla företag måste vara i samma miljö.
* Den användare som ställer in dotterbolaget måste ha licenserna **Essential**, **Premium** eller **Basic ISV**.

> [!NOTE]
> Licensen Teammedlem och Intern administratör låter någon komma åt men inte ändra poster, så den kan inte användas för att ställa in synkroniseringen. Med licensen Delegerad admin kan du inte schemalägga bakgrunds aktiviteter så du kommer inte att kunna slutföra installationen.

## Ange källföretaget

De första stegen är att ange företaget som ska bli datakälla och aktivera synkronisering. Dotterbolag hämtar data från källföretaget.

1. I ett dotterbolag väljer du ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Hanteringskonfiguration för huvuddata** och väljer sedan relaterad länk.
1. I fältet **källföretag** anger du det företag som du vill hämta ändringar från.
1. Aktivera växlingen **Aktivera synkronisering**.
1. Välj **OK** i bekräftelsedialogen. [!INCLUDE [prod_short](includes/prod_short.md)] visar de register och fält som är tillgängliga från källföretaget.

Nästa steg är att aktivera tabeller och fält för synkronisering.

## Aktivera eller inaktivera tabeller och fält

För att spara tid visar [!INCLUDE [prod_short](includes/prod_short.md)] en lista över de tabeller som företag ofta synkroniserar. Som standard är dessa tabeller aktiverade för synkronisering. Du kan ändra, inaktivera eller ta bort dem på det sätt som visas. Som en extra tidsbesparing är vissa fält i tabellerna redan inaktiverade eftersom de förmodligen inte är relevanta för dotterbolaget.

> [!NOTE]
> Om ett eller flera tillägg är installerade i källföretaget kan du när ett dotterbolag ställer in synkroniseringen innehåller sidan **Synkroniseringstabeller** tabeller från tilläggen och du kan komma åt deras fält. Om källföretaget lägger till ett tillägg när synkroniseringen har ställts in, måste dock varje dotterbolag lägga till tabellerna manuellt. Om du vill veta mer om hur du lägger till tabeller går du till [Lägg till eller ta bort tabeller från synkroniseringstabellistan](#add-or-delete-tables-from-the-synchronization-tables-list). Om du vill ha mer information om utöka [!INCLUDE [prod_short](includes/prod_short.md)] går du till [Utveckla tillägg i Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Hanteringskonfiguration för huvuddata** och väljer sedan relaterad länk.
1. Välj åtgärden **Synkroniseringstabeller**.
1. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Fältet **tabellfilter** är användbart när du vill styra vad som ska synkroniseras med en tabell. Du kan bara skapa filter som synkroniserar när vissa villkor är uppfyllda. Du kan till exempel lägga till filter som anger att du endast synkroniserar leverantörer i en viss region. Eller kunder som använder en viss valuta.
>
> Om dotterbolaget redan har data i sina tabeller är ett annat bra sätt att ställa in kriterier för synkronisering att ställa in matchningsbaserad koppling. Om du vill ha mer information om matchning går du till [Använd matchningsbaserad koppling](#use-match-based-coupling).

1. Om du vill aktivera fält för en tabell väljer du tabellen och väljer sedan åtgärden **fält**.
1. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Ett snabbt sätt att aktivera eller inaktivera flera fält samtidigt, är att markera dem i listan och sedan använda åtgärderna **aktivera** eller **inaktivera**.

### Använd matchningsbaserad koppling

Du kan ange vilka data som ska synkroniseras för en tabell genom att matcha poster baserat på villkor. På sidan **Hanteringskonfiguration för huvuddata** väljer du åtgärden **Matchningsbaserad koppling** för att öppna sidan **Välj kopplingsvillkor**. Du kan definiera följande kriterier för ditt matchande:

* Om du vill synkronisera efter att du kopplat poster.
* Om man ska skapa en ny post i dotterbolaget om en unik ej kopplad matchning med hjälp av matchningsvillkoret. Om du vill aktivera funktionen aktiverar du åtgärden **Skapa ny om det inte går att hitta någon matchning**.
* De fält som ska användas för att matcha poster och om matchningen är skiftlägeskänslig.
* Prioritera ordningen som posterna genomsöks i genom att ange en matchningsprioritet. [!INCLUDE [prod_short](includes/prod_short.md)] söker efter en matchning i stigande ordning baserat på matchningsprioritet. Ett tomt värde är lika med prioritet 0, som är högsta prioritet. Fält med prioritet 0 beaktas först.

## Synkronisera för första gången

När du är klar väljer du åtgärden **Hanteringskonfiguration för huvuddata**, välj åtgärden **Starta inledande synkronisering**. På sidan **Första synkronisering av huvuddata**, välj den typ av synkronisering som du vill använda för varje tabell.

* Om det redan finns poster i både käll- och dotterbolag och du vill matcha befintliga poster, väljer du åtgärd **Använd matchningsbaserad koppling**. [!INCLUDE [prod_short](includes/prod_short.md)] matchar poster i dotter bolaget med poster i källföretaget. Matchningarna baseras på matchande kriterier som du definierar. För flera standardtabeller [!INCLUDE [prod_short](includes/prod_short.md)] har redan befintliga poster matchats med primär nyckeln, men du kan ändra den om du vill. Du kan också låta synkroniseringen skapa nya poster i dotterbolaget för poster i källföretaget som dotterbolaget inte har. Om du vill ha mer information om matchning går du till [Använd matchningsbaserad koppling](#use-match-based-coupling).
* Om du väljer **Kör fullständig synkronisering**, synkroniseringen kommer att skapa nya poster för alla poster i källföretaget som inte är kopplade än. Det här alternativet är t.ex. användbart i följande fall:

    * Dotterbolaget saknar data i tabellen.
    * Du vill lägga till poster från källföretaget utan att matcha.  

När du har valt alternativet som ska användas väljer du **starta alla** för att starta synkroniseringen.

Medan synkroniseringen körs visar sidan **Jobbstatus** på sidan **Initiera fullständig synkronisering av huvuddata** visar status för varje jobbköpost. Tryck på **F5** på tangentbordet för att uppdatera statusen.

> [!TIP]
> Tabeller synkroniseras i fördefinierad ordning. Om synkroniseringen blir fastnad i en tabell, markerar du tabellen och väljer sedan åtgärden **starta om** för att komma igång igen.

Om du vill visa information om antalet poster som har infogats eller ändrats, kan du välja värdet i kolumnen **jobbstatus** för att öppna sidan **Visa – integrera synkroniseringsjobb** . När det gäller poster som har infogats kan du välja numret i kolumnen **infogad** för att få mer information om de nya posterna.

## Lägg till eller ta bort tabeller från listan över synkroniseringstabeller

### Lägg till en tabell

> [!IMPORTANT]
> Även om tabeller som innehåller transaktionsdata är tillgängliga i listan, till exempel tabeller som innehåller transaktioner, bör du inte välja dem. Synkronisering fungerar bara för tabeller som innehåller icke-transaktionella data.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Synkroniseringstabeller** och välj relaterad länk.
1. Välj **Ny** och välj sedan tabellen att lägga till.
1. Fyll i fälten om det behövs. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### Ta bort en tabell

> [!NOTE]
> Om du tar bort en post i källföretaget tas den även bort i dotterbolaget. Detta förhindrar oönskad förlust av data. Dotterbolaget kan bestämma om tabellen ska tas bort.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Synkroniseringstabeller** och välj relaterad länk.
1. Välj åtgärden **Radera**.

## Använd export och import för att dela en synkroniseringsinställningar

Om du lägger upp flera dotter bolag som använder samma eller liknande synkroniseringsinställningar, finns det en tidsinställning. Skapa ett dotter bolag och exportera dess inställningar till en .xml-fil. Filen innehåller hela inställningarna, inklusive tabell- och fältmappningar och filterkriterier. Du kan sedan importera filen till nästa dotterbolag. För att importera eller exportera en inställning, på sidan **Hanteringskonfiguration för huvuddata** använd åtgärd **Importera** eller **Exportera**.

## Se även

[Hantera synkronisering av huvuddata](admin-sync-master-data.md)
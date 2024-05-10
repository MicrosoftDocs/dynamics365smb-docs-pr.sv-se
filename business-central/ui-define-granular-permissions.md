---
title: Definiera detaljerade behörigheter
description: I den här artikeln beskrivs hur du definierar detaljerade behörigheter och tilldelar varje användare de behörighetsgrupper som de behöver för att utföra sina projekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
ms.service: dynamics-365-business-central
---

# <a name="assign-permissions-to-users-and-groups"></a>Tilldela behörigheter till användare och grupper

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

[!INCLUDE[prod_short](includes/prod_short.md)]-säkerhetssystemet kontrollerar vilka objekt som en användare har åtkomst till i varje databas eller miljö, i kombination med användarens licens. För varje användare kan du ange om de kan läsa, ändra eller ange data i databasobjekten. Mer information finns i [Datasäkerhet](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i hjälpen för utvecklare och administrationsinnehåll för [!INCLUDE[prod_short](includes/prod_short.md)].

Innan du tilldelar behörigheter till användare och användargrupper måste du ange vem som kan logga in genom att skapa användare enligt licensen. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).

I [!INCLUDE[prod_short](includes/prod_short.md)] finns det två behörighetsnivåer för databasobjekt:

- De övergripande behörigheterna enligt licensen, som också kallas för berättigandet.

  I licenserna ingår standard behörighets uppsättningar. Från och med 2022 utgivningscykel 1 kan administratörer anpassa standard behörigheterna för de licenstyper som krävs. Mer information finns i [Konfigurera behörigheter baserat på licenser](ui-how-users-permissions.md#licensespermissions).  

- Detaljerad behörighet som du tilldelar i [!INCLUDE[prod_short](includes/prod_short.md)].

I den här artikeln beskrivs hur du kan definiera, använda och tillämpa behörigheter i [!INCLUDE [prod_short](includes/prod_short.md)] för att ändra standardkonfigurationen.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Mer information finns i [Tilldelad administratörsåtkomst till Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] Online innehåller standard användargrupper som tilldelas användare automatiskt baserat på deras licens. Du kan ändra standardkonfigurationen genom att ändra eller lägga till säkerhetsgrupper, behörighetsgrupper och behörigheter. I följande tabell beskrivs viktiga scenarier för ändring av standardbehörigheterna.  

|Om du vill  |Gå till  |
|---------|---------|
|För att göra det enklare att hantera behörigheter för flera användare kan du ordna dem i säkerhetsgrupper och sedan tilldela eller ändra en behörighetsuppsättning för många användare med en åtgärd.| [Hantera behörigheter via användargrupper](#manage-permissions-through-user-groups) |
|Så här hanterar du behörighetsgrupper för specifika användare | [Tilldela behörighetsuppsättningar till användare](#assign-permission-sets-to-users) |
|Så här definierar du en behörighetsuppsättning|[Skapa en behörighetsuppsättning](#create-a-permission-set)|
|För att visa eller felsöka en användares behörigheter|[Få en översikt en användares behörigheter](#get-an-overview-of-a-users-permissions)|
|Information om säkerhet på postnivå|[Säkerhetsfilter begränsar användarens åtkomst till specifika poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Ett bredare sätt för att definiera vilka funktioner en användare har åtkomst till är att ställa in fältet **Upplevelse** på sidan **Företagsinformation**. Mer information finns i [ändra vilka funktioner som visas](ui-experiences.md).
>
> Du kan också ange vilka funktioner som är tillgängliga för användare i användargränssnittet och hur de interagerar med dem via sidor. Du gör detta genom profiler som du tilldelar olika typer av användare enligt deras projektroll eller avdelning. Mer information finns i [Hantera profiler](admin-users-profiles-roles.md) och [anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="create-a-permission-set"></a>Skapa en behörighetsuppsättning

> [!NOTE]
> I utgivningscykel 2 2022 blir det enklare att lägga till behörigheter i behörighetsuppsättningar. I stället för att lägga till behörigheter individuellt kan du lägga till hela behörighetsuppsättningar. Vid behov kan du utelämna enskilda behörigheter i dem. Mer information finns i [Lägga till andra behörighetsuppsättningar](#to-add-other-permission-sets). För att göra det möjligt ersatte vi sidan Behörighetsuppsättning med en ny. De viktigaste skillnaderna är de nya fönstren **Behörighetsuppsättningar** och **Resultat** samt faktarutan **Inkluderade behörigheter**. Om du vill fortsätta använda den ersatta sidan Behörigheter går du till sidan **Behörighetsuppsättningar** och väljer åtgärden **Behörigheter (äldre)**.

Underhåll är också lättare. När du lägger till systembehörighet uppdateras den användardefinierade behörighetsuppsättningen automatiskt med alla ändringar som Microsoft ger dessa behörigheter.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Behörighetsuppsättning** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj åtgärden **Behörigheter**.
5. På sidan **Behörighetsuppsättning**, i fältet **Typ**, inkluderar eller exkluderar du behörigheter till objektet enligt följande:

  För att inkludera behörigheten väljer du **Inkludera** och sedan åtkomstnivå som ska beviljas i fälten **Läsbehörighet**, **Infogningsbehörighet**, **Ändringsbehörighet**, **Borttagningsbehörighet** och **Verkställningsbehörighet**. Alternativen beskrivs i tabellen nedan.

  |Alternativ|Description|Rangordning|
  |------|-----------|-------|
  |**Tomt**|Användaren kan inte utföra åtgärden på objektet.|Lägsta|  
  |**Ja**|Användaren kan utföra åtgärden på objektet.|Högsta|
  |**Indirekt**|Användaren kan utföra åtgärden på objektet, men endast via ett annat relaterat objekt som användaren har fullständig åtkomst till. Mer information finns i [Exempel – Indirekt behörighet](#example---indirect-permission) i den här artikeln och [Behörighetsegenskap](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) i Hjälp för utvecklare och IT-proffs.|Andra högsta|
  
  Om du vill utesluta behörigheten, eller en eller flera åtkomstnivåer, väljer du **Uteslut**och sedan vilken åtkomst nivå du vill ge. Alternativen beskrivs i tabellen nedan.

  |Alternativ|Description|
  |------|-----------|-------|
  |**Tomt**|Använd åtkomstnivån baserat på behörighetens hierarki i uppsättningen.  |
  |**Uteslut**|Ta bort den specifika åtkomstnivån för objektet.|
  |**Reducera till indirekt**|Ändra åtkomstnivån till Indirekt om någon behörighetsuppsättning ger direkt åtkomst till objektet. Du kan till exempel välja det här alternativet om behörighetsuppsättningen ger direkt åtkomst till redovisningstransaktioner, men du vill inte att användarna ska ha fullständig åtkomst till transaktionerna.|
  
  > [!NOTE]
  > Om en behörighet finns i en behörighetsgrupp som ingår och även är i en behörighetsgrupp som har uteslutits, kommer behörigheten att uteslutas.

6. Använd fälten **Objekttyp** och **Objekt-ID** för att ange vilket objekt du ger åtkomst till.

  > [!TIP]
  > Nya rader innehåller standardvärden. Till exempel innehåller fältet **Objekttyp** **Tabelldata** och fältet **Objekt-ID** innehåller **0**. Standardvärdena är bara platshållare och används inte. Du måste välja en typ av objekt och ett objekt i fältet **Objekt-ID** innan du kan skapa en ny rad.

7. Valfritt: Om du definierar behörigheter för ett objekt av typen Tabelldata kan du i fältet **Säkerhetsfilter** filtrera data som en användare kan öppna i fält i den valda tabellen. Du kanske till exempel vill låta en användare endast komma åt de poster som innehåller information om en viss kund. Mer information finns i [Säkerhetsfilter begränsar användarens åtkomst till specifika poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table) och [Använda säkerhetsfilter](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Valfritt: Lägg till en eller flera andra behörighetsuppsättningar i rutan **Behörighetsuppsättningar**. Mer information finns i [Lägga till andra behörighetsuppsättningar](#to-add-other-permission-sets).

> [!IMPORTANT]
> Var försiktig när du tilldelar **infoga behörighet** eller **ändra behörighet** till **9001 användargruppmedlem** eller **9003 behörighetsuppsättning för användargrupp**. Alla användare som tilldelats behörighetsuppsättningen kan eventuellt tilldela sig själva till andra användargrupper, som i sin tur kan ge dem oavsiktliga behörigheter.

### <a name="example---indirect-permission"></a>Exempel – Indirekt behörighet

Du kan tilldela indirekt behörighet för att låta en användare använda ett objekt, men endast via ett annat objekt. En användare har till exempel behörighet att köra Codeunit 80, försäljningspost. Kodmodulen försäljningspost utför många uppgifter, inklusive ändra tabell 37 inköpsrad. När användaren bokför ett försäljningsdokument med codeunit Försäljningspost kontrollerar [!INCLUDE[prod_short](includes/prod_short.md)] om användaren har behörighet att ändra tabellen Försäljningsrad. Om inte kan inte codeuniten slutföra uppgiften och användaren tar emot ett felmeddelande. I så fall, kör Codeunit korrekt.

Användaren behöver dock inte ha fullständig åtkomst till tabellen Inköpsrad för att köra codeuniten. Om användaren har indirekt behörighet till tabellen Inköpsrad körs codeunit Försäljningspost korrekt. När en användare har indirekt behörighet kan användaren endast ändra tabellen inköpsrad genom att köra codeunit Försäljningspost eller ett annat objekt som har behörighet att ändra tabellen Inköpsrad. Användaren kan endast ändra tabellen inköpsrad när det görs från moduler som stöds. Användaren kan inte köra funktionen oavsiktligt eller på ett skadligt sätt med andra metoder.

### <a name="to-add-other-permission-sets"></a>Lägga till andra behörighetsuppsättningar

Expandera en behörighetsuppsättning genom att lägga till andra behörighetsuppsättningar i den. Därefter kan du ta med eller utelämna specifika behörigheter, eller hela behörighetsuppsättningar, i varje uppsättning som du lägger till. Detta inkluderar behörigheter i behörighetsuppsättningarna Tillägg och Systemtyp, som annars inte är tillåtna. Uteslutningar gäller endast den behörighetsuppsättning du expanderar. Den ursprungliga uppsättningen påverkas inte.

På sidan **Behörighetsuppsättning** lägger du till en behörighetsuppsättning i rutan **Behörighetsuppsättningar**. I rutan **Resultat** visas alla tillagda behörighetsuppsättningar. Om du vill utforska behörigheterna som inkluderas i uppsättningen du har lagt till, väljer du uppsättningen i rutan Resultat, så visas faktarutan **Inkluderade behörigheter** behörigheterna.

I rutan **Resultat** använder du fältet **Inkluderingsstatus** för att identifiera behörighetsuppsättningarna i vilka du har uteslutit behörigheter eller behörighetsuppsättningar. Om något har uteslutits kommer statusen att vara **Delvis**.

Om du vill ha en översikt över behörigheterna i behörighetsuppsättningen väljer du åtgärden **Visa alla behörigheter**. På sidan **Utökade behörigheter** visas alla behörigheter som redan tilldelats behörighetsuppsättningen och behörigheterna i de tillagda behörighetsuppsättningarna.

För att helt utesluta alla behörigheter från en behörighetsuppsättning som du har lagt till går du till rutan **Resultat**, väljer raden, väljer **Visa fler alternativ** och sedan **Uteslut**. När du utesluter en behörighetsuppsättning skapas en rad i rutan **Behörighetsuppsättningar** av typen Utesluten. Om du har uteslutit en behörighetsuppsättning, men vill ta med den igen, tar du bort raden i rutan **Behörighetsuppsättningar**.

Om du vill utesluta eller delvis utesluta en viss behörighet i en uppsättning som du har lagt till, skapar du en rad för objektet under **Behörigheter**. Fälten för åtkomstnivå, Infoga behörighet, Ändra behörighet och så vidare innehåller alla **Uteslut**. Om du vill tillåta en viss åtkomstnivå väljer du lämpligt alternativ.

Om du utesluter en behörighetsgrupp utesluts alla behörigheter i uppsättningen. [!INCLUDE [prod_short](includes/prod_short.md)] beräknar behörigheterna som följer:

1. Beräkna den fullständiga listan med inkluderade behörigheter
2. Beräkna den fullständiga listan med uteslutna behörigheter
3. Ta bort uteslutna behörigheter från listan över inkluderade behörigheter (borttagning av indirekt behörighet är detsamma som att minska till indirekt)

## <a name="copy-a-permission-set"></a>Kopiera behörighetsuppsättning

Skapa en ny behörighetsuppsättning genom att kopiera en annan. Den nya uppsättningen kommer att innehålla alla behörigheter och behörighetsuppsättningar från den uppsättning du kopierade. Hur behörigheterna och behörighetsuppsättningarna ordnas i den nya behörighetsuppsättningen skiljer sig åt beroende på vad du väljer i fältet **Kopiera åtgärd**. Alternativen beskrivs i tabellen nedan.

|Alternativ  |Description  |
|---------|---------|
|**Kopiera utifrån referens**     | Den ursprungliga behörighetsuppsättningen och alla behörighetsuppsättningar som har lagts till i den visas i rutan **Resultat**.       |
|**Platt behörighetskopia**  | Alla behörigheter för alla behörighetsuppsättningar tas med i en platt lista i **rutan Behörigheter**. Behörigheterna är inte ordnade efter behörighetsuppsättning.        |
|**Klona**     | Skapa en exakt kopia av den ursprungliga behörighetsuppsättningen.        |

1. I sidan **behörighetsuppsättningar**, markera raden för en behörighetsuppsättning som du vill kopiera och välj sedan åtgärden **Kopiera behörighetsuppsättning**.
2. På sidan **Kopiera behörighetsuppsättning** anger du namnet på den nya behörighetsuppsättningen.
3. I fältet **Kopiera åtgärd** anger du hur behörigheter ska ordnas i den nya behörighetsuppsättningen.
4. Valfritt: Om du lägger till en systembehörighetsuppsättning kanske du vill bli meddelad om namnet eller innehållet i den ursprungliga behörighetsuppsättningen ändras i en framtida version. På så sätt kan du överväga om du vill uppdatera den användardefinierade behörighetsuppsättningen. Om du vill ta emot ett meddelande aktiverar du alternativet **Meddela vid ändrad behörighetsuppsättning**.

> [!NOTE]
> Meddelandet kräver att meddelandet **Ursprunglig systembehörighetsuppsättning har ändrats** är aktiverat på sidan **Mina meddelanden**.

## <a name="create-or-modify-permissions-by-recording-your-actions"></a>Skapa eller ändra behörigheter genom att registrera dina åtgärder

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Behörighetsuppsättning** och väljer sedan relaterad länk.

    Alternativt kan du i sidan **Användare** välja åtgärden **Behörighetsuppsättningar**.
2. På sida **Behörighetsuppsättningar** väljer du åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov.
4. Välj åtgärden **Behörigheter**.
5. På sidan **behörigheter** väljer åtgärden **postbehörigheter** och välj sedan åtgärden **startar**.  
    Inspelning måste göras antingen genom att använda (popup) funktionen **Öppna denna sida i ett nytt fönster new windows** för att ha inspelningsfönstret **behörigheter** bredvid eller genom att arbeta i samma flik.  
    En registreringsprocess startar nu som fångar alla dina åtgärder i användargränssnittet.
6. Gå till olika sidor och aktiviteter i [!INCLUDE[prod_short](includes/prod_short.md)] som du vill att användare med denna behörighetsuppsättning ska lägga till. Du måste utföra de aktiviteter som du vill registrera behörigheter för.
7. Om du vill avsluta registreringen går du tillbaka till sidan **behörigheter** och väljer åtgärden **stoppa**.
8. Välj knappen **Ja** om du vill lägga till registrerade behörigheter till den nya behörighetsuppsättningen.
9. För varje objekt i den registrerade listan anger du om användarna ska kunna infoga, ändra eller ta bort poster i de registrerade tabellerna.

### <a name="to-export-and-import-a-permission-set"></a>Så här exporterar och importerar du en behörighetsgrupp

Om du snabbt vill ställa in behörigheter kan du importera behörighetsuppsättningar som du har exporterat från en annan [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation.

I miljöer med flera klientorganisationer importeras en behörighetsuppsättning till en särskild klientorganisation. Med andra ord är omfattningen för importen *Klientorganisation*.

1. I klientorganisation 1, på **Behörighetsuppsättningar** Välj raden eller linjerna för behörighetsuppsättningarna att exportera och välj sedan **Exportera behörighetsuppsättning**.

    En XML-fil skapas i hämtningsmappen på datorn. Som standard är namnet *Exportera behörighetsuppsättningar.xml*.

2. I klientorganisation 2, på sidan **behörighetsuppsättning** välj åtgärden **Importera behörighetsuppsättning**.
3. I dialogrutan **Importera behörighetsuppsättningar**, överväg om du vill slå ihop befintliga behörighetsuppsättningar med några nya behörighetsuppsättningar i XML-filen.

    Om du markerar kryssrutan **Uppdatera befintliga behörigheter** kommer befintliga behörighetsuppsättningar som matchar namnen i XML-filen att slås samman med de importerade behörighetsuppsättningarna.

    Om du inte markerar kryssrutan **Uppdatera befintliga behörigheter** kommer behörighetsuppsättningar som matchar namnen i XML-filen att hoppas över under importen. I så fall får du ett meddelande om behörighetsuppsättningar som hoppas över.

4. I dialogrutan **Import** hittar du och väljer den XML-fil som ska importeras och väljer sedan åtgärden **Öppna**.

Behörighetsgrupperna importeras.

## <a name="remove-obsolete-permissions-from-all-permission-sets"></a>Ta bort föråldrade behörigheter från alla behörighetsuppsättningar

På sidan **Behörighetsuppsättningar**, välj åtgärden **Ta bort inaktuella behörigheter**.

## <a name="set-up-time-constraints-for-users"></a>Så här ställer du in tidsbegränsningar för användare

Administratörer kan definiera tidsperioder under vilka angivna användare kan bokföra. Administratörer kan också ange om systemet loggar hur mycket tid användare är inloggade. På liknande sätt kan administratörer tilldela ansvarsenheter till användare. För mer information, se [Arbeta med ansvarsenheter](inventory-responsibility-centers.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställning** och väljer sedan relaterad länk.
2. I sidan **Användarinställningar** väljer du åtgärden **Ny**.
3. I den **Användar-ID** anger du ID för en användare, och väljer fältet för att se alla aktuella Windows-användare i systemet.
4. Fyll i fälten om det behövs.

## <a name="control-access-to-specific-companies"></a>Kontrollera åtkomst till specifika företag

När du har flera företag i Business Central krävs extra uppmärksamhet för att hantera behörigheter mellan företag. Du kanske inte vill att användarna ska ha samma åtkomsträttigheter som alla företag. I stället kan du behöva bevilja användarnas behörigheter baserat på deras företagstillhörighet. I det här scenariot kan du välja ett specifikt företag som behörighetsuppsättningen gäller när du tilldelar behörighetsuppsättningar till enskilda användare eller säkerhetsgrupper. Företaget anges inte uttryckligen i behörighetsuppsättningen, utan i stället när behörighetsuppsättningen tilldelas användaren eller säkerhetsgruppen.

Om du inte anger företaget när du tilldelar en behörighetsuppsättning gäller behörighetsuppsättningen för alla företag. Om du vill att en behörighetsuppsättning ska gälla för fler än ett företag, men inte för alla företag, lägger du till behörighetsuppsättningen specifikt för varje företag separat.

Mer information om [Tilldela behörighetsuppsättningar till användare](#assign-permission-sets-to-users) eller [Tilldela behörigheter till en säkerhetsgrupp](ui-security-groups.md#assign-permissions-to-a-security-group).

## <a name="manage-permissions-through-user-groups"></a>Hantera behörigheter via användargrupper

Med användargrupper kan du hantera behörighetsgrupper i företaget. [!INCLUDE [prod_short](includes/prod_short.md)] Online innehåller standard användargrupper som tilldelas användare automatiskt baserat på deras licens. Du kan lägga till användare manuellt i en användargrupp, och du kan skapa nya användargrupper som kopior av befintliga.  

Du börjar med att skapa en användargrupp. Sedan tilldelar du gruppen behörighetsuppsättningar för att definiera vilka objekt som användare av gruppen ska få åtkomst till. När du lägger till användare i gruppen gäller de behörighetsuppsättningar som har definierats för gruppen för användaren.

Behörighetsuppsättningar som tilldelas en användare via en användargrupp förblir synkroniserade. En ändring av användargruppsbehörigheter sprids automatiskt till användarna. Om du tar bort en användare från en användargrupp återkallas de berörda behörigheterna automatiskt.

### <a name="to-add-users-to-a-user-group"></a>Så här lägger du till användare i en användargrupp

I proceduren nedan beskrivs hur du skapar användargrupper manuellt. Information om hur du skapar användargrupper automatiskt finns i [Kopiera en användargrupp och dess behörighetsuppsättningar](#to-copy-a-user-group-and-all-its-permission-sets).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användargrupper** och väljer sedan relaterad länk.

    1. Alternativt kan du i sidan **Användare** välja åtgärden **Användargrupper**.
2. På sidan **Användargrupp** väljer du åtgärden **Medlemmar i användargrupp**.
3. På sidan **Användargrupp** väljer du åtgärden **Lägg användare**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Om du vill kopiera en användargrupp och dess behörighetsuppsättningar

Du kan kopiera alla behörighetsuppsättningar från en befintlig användargrupp till den nya användargruppen, om du snabbt vill definiera en ny användargrupp..

> [!NOTE]
> Medlemmarna i användargruppen kopieras inte till den nya användargruppen. Du måste lägga till dem manuellt i efterhand. Mer information finns i avsnittet [För att lägga till användare i en användargrupp](#to-add-users-to-a-user-group).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användargrupper** och väljer sedan relaterad länk.
2. Välj de användargrupper som du vill kopiera och välj sedan åtgärden **Kopiera användargrupp**.
3. I fältet **Ny användargruppkod** anger du ett namn på den nya gruppen och väljer sedan knappen **OK**.

Användargruppen läggs till i sidan **Användargrupper**. Fortsätt med att lägga till användare. Mer information finns i avsnittet [För att lägga till användare i en användargrupp](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Du får ett meddelande om verifieringsfel om du försöker tilldela en användargrupp en användare som refererar till en behörighetsgrupp som har definierats i ett tillägg som inte avinstallerats. Detta beror på att app-ID tillägget verifieras när det refereras. Om du vill tilldela en användare en användargrupp kan du antingen installera tillägget på nytt, ta bort referensen för det avinstallerade tillägget från behörighetsgruppen eller ta bort behörighetsuppsättningen från användargruppen.

### <a name="to-assign-permission-sets-to-user-groups"></a>Tilldela behörighetsuppsättningar till användargrupper

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användargrupper** och väljer sedan relaterad länk.
2. Markera den användargrupp som du vill tilldela behörighet till.  

    Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
3. Välj åtgärden **Användarbehörighetsuppsättning** för att öppna sidan **Användarbehörighetsuppsättning**.
4. På sidan **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Tilldela en behörighetsuppsättning på sidan Behörighetsuppsättning efter användargrupp

I proceduren nedan beskrivs hur du tilldelar behörighetsuppsättningar till en användargrupp på sidan **Behörighetsuppsättning efter användargrupp**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. På sidan **Användare** väljer du den relevanta användaren och väljer sedan åtgärden **Behörighetsuppsättning efter användargrupp**.
3. På sidan **Behörighetsuppsättning efter användargrupp** väljer du fältet **[användargruppsnamn]** på en rad för den relevanta behörighetsuppsättningen för att tilldela uppsättningen till användargruppen.
4. Markera kryssrutan **Alla användargrupper** om du vill tilldela behörighetsuppsättningen till alla användargrupper.

Du kan också tilldela behörighetsuppsättningar direkt till en användare.

## <a name="assign-permission-sets-to-users"></a>Tilldela behörighetsuppsättningar till användare

En behörighetsuppsättning är en samling behörigheter för specifika databasobjekt. Alla användare måste tilldelas en eller flera behörighetsuppsättningar innan de får tillgång till [!INCLUDE[prod_short](includes/prod_short.md)].  

En [!INCLUDE[prod_short](includes/prod_short.md)]-lösning innehåller fördefinierade behörighetsuppsättningar som läggs till av Microsoft eller av lösningsleverantören. Du kan också lägga till nya behörighetsuppsättningar som är skräddarsydda efter företagets behov. Mer information finns i avsnittet [Skapa en behörighetsuppsättning](#create-a-permission-set).

> [!NOTE]
> Om du inte vill begränsa en användares behörighet mer än vad som har definierats av licensen kan du tilldela en särskild behörighetsuppsättning som kallas SUPER för användaren. Den här behörighetsuppsättningen gör att användaren kan komma åt alla objekt som anges i licensen.
>
> En användare med Essential-licensen och SUPER behörighetsuppsättningen har tillgång till fler funktioner än användare med Team Member-licensen och behörighetsuppsättningen SUPER.

Du kan tilldela behörighetsuppsättningar till användare på två sätt:

- På sidan **Användarkort** genom att välja behörighetsuppsättningar att tilldela användaren.
- På sidan **Behörighetsuppsättning efter användare** genom att välja användare som en behörighetsuppsättning är tilldelad till.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Så här tilldelar du en behörighetsuppsättning till ett användarkort

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
1. Markera den användare som du vill tilldela behörighet till.

   Eventuella behörighetsuppsättningar som redan har tilldelats till användaren visas i faktaboxen **Behörighetsuppsättningar**.
1. I fönstret **Inkommande dokument** väljer du sidan **Användarkort**.
1. På snabbfliken **Användarbehörighetsuppsättning** fyller du i fälten efter behov på en ny rad. Mer information finns i avsnittet [Skapa eller redigera en behörighetsuppsättning](ui-define-granular-permissions.md#create-a-permission-set).

   Om du vill att behörighetsuppsättningen ska gälla för ett specifikt företag, ställ in **Företag** för det företaget. Om du vill att behörighetsuppsättningen ska gälla för alla företag lämnar du fältet **Företag** tomt. [Läs mer](#control-access-to-specific-companies).

## <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Så här tilldelar du en behörighetsuppsättning till sidan Behörighetsuppsättning efter användare

Den här metoden gör det enklare för dig att tilldela olika behörighetsuppsättningar till flera användare. 

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
1. På sidan **Användare** välja åtgärden **Behörighetsuppsättning för användare**.
1. Om du vill att behörighetsuppsättningen endast ska gälla för ett specifikt företag, ställ in **Företagsnamn** för det företaget. Om du vill att behörighetsuppsättningen ska gälla för alla företag lämnar du fältet **Företagsnamn** tomt. [Läs mer](#control-access-to-specific-companies).
1. På sidan **Behörighetsuppsättning efter användare** markerar du kryssrutan **[användarnamn]** på en rad för den aktuella behörighetsuppsättningen för att tilldela uppsättningen till användaren.

    Markera kryssrutan **Alla användare** om du vill tilldela behörighetsuppsättningen till alla användare.

## <a name="get-an-overview-of-a-users-permissions"></a>Få en översikt en användares behörigheter

Du kan endast visa andra användares gällande behörigheter om du tilldelats behörigheterna SÄKERHET eller SUPER. 

På sidan **Gällande behörigheter** finns ytterligare information om källan till respektive behörighet. Till exempel om källan är en säkerhetsgrupp eller om en behörighet ärvs. Sidan innehåller också en kolumn där administratörer kan granska de säkerhetsfilter som används. Mer information om säkerhetsfilter finns i [Säkerhetsfilter begränsar en användares åtkomst till specifika poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.
2. Öppna kortet för relevant användare.
3. Välj åtgärden **Gällande behörigheter**.

    Dellistan **behörigheter** listar alla de databasobjekt som användaren har åtkomst till. Avsnittet kan inte redigeras.

    Delen **Efter behörighetsuppsättning** visar tilldelade behörighetsuppsättningarna genom vilka behörigheterna beviljas användaren, källa och typ för behörighetsuppsättningen och som utökar de olika typerna tillåts.

    För varje rad som du väljer i avsnittet **behörigheter** under avsnittet **Efter behörighetsuppsättning** visar vilken behörighetsuppsättning eller uppsättningar som har beviljats behörighet till. I detta avsnitt kan du redigera värdena i var och en av fem åtkomsttypfält **läsbehörighet**, **infoga behörighet**, **ändra behörighet**, **ta bort behörighet** och **körningsbehörighet**.

    > [!NOTE]  
    > Endast behörighetsgrupper av typen **användardefinierade** kan redigeras.
    >
    > Rader med källberättigande kommer från prenumerationslicensen. Värdena på behörighetsvärdena för berättigandet åsidosätter värden i andra behörighetsuppsättningar om de har en högre rankning. Ett värde i en icke-berättigad behörighetsuppsättning som har en högre rankning än det relaterade värdet i berättigandet ska vara inom parentes för att ange att det inte är effektivt när det åsidosätts av berättigandet.
    >
    > Mer information om rankning finns i avsnittet [Skapa en behörighetsuppsättning](ui-define-granular-permissions.md#create-a-permission-set).  

4. Om du vill redigera en behörighet, i **Efter behörighetsuppsättning**, på raden för en relevant behörighetsuppsättning av typen **Användardefinierad**, välj ett av fem åtkomstfält och välj ett annat värde.

5. Om du vill redigera enskilda behörigheter inom behörighetsuppsättningen väljer du värdet i fältet **behörighetsuppsättning** för att öppna sidan **behörigheter**.

> [!NOTE]  
> När du redigerar en behörighetsuppsättning gäller ändringarna också för andra användare som har den behörighetsuppsättningen tilldelad.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Säkerhetsfilter – begränsa användarens åtkomst till specifika poster i en tabell

För postnivåsäkerhet i [!INCLUDE[prod_short](includes/prod_short.md)] kan du använda säkerhetsfilter för att begränsa användarens åtkomst till data i en tabell. Du kan skapa säkerhetsfilter på tabelldata. Ett säkerhetsfilter beskriver en uppsättning poster i en tabell som en användare har behörighet att komma åt. Du kan till exempel ange att en användare endast kan läsa de poster som innehåller information om en viss kund. På så sätt kan användaren inte kan komma åt de poster som innehåller information om andra kunder. Mer information finns i [Använda säkerhetsfilter](/dynamics365/business-central/dev-itpro/security/security-filters) i administrationsinnehållet.


## <a name="view-permission-changes-telemetry"></a>Visa telemetri över behörighetsförändringar

Du kan låta [!INCLUDE[prod_short](includes/prod_short.md)] skicka ändringar som har gjorts i behörighet för en Application Insights-resurs i Microsoft Azure. Med hjälp av Azure Monitor kan du sedan skapa rapporter och aviseringar för insamlade data. Mer information finns i följande artiklar i [!INCLUDE[prod_short](includes/prod_short.md)]-hjälpen för utvecklare och administratörer:

- [Övervaka och analysera telemetri – Aaktivera Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysera telemetri för fältövervakning](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Utsedda adminanvändare

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a>Se även

[Skapa användare enligt licenser](ui-how-users-permissions.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Lägg till användare till Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Säkerhet och skydd i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjälpen för utvecklare och IT-proffs  
[Tilldela ett telemetri-ID till användare](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Förbereda ett konfigurationspaket | Microsoft Docs
description: När du konfigurerar ett nytt företag, identifieras och hanteras tabellrelationer. Data importeras och kopplas i rätt ordning. Måttabeller importeras också, om de ingår i konfigurationspaketet.
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
ms.openlocfilehash: 0f74b3472b081d7968336fd16b6ef6addccff861
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308003"
---
# <a name="prepare-a-configuration-package"></a>Förbereda ett konfigurationspaket
När du konfigurerar ett nytt företag identifieras och hanteras tabellrelationer. Data importeras och kopplas i rätt ordning. Måttabeller importeras också, om de ingår i konfigurationspaketet. Mer information finns också i [Så här importerar du kunddata](admin-migrate-customer-data.md#to-import-customer-data). 

Om du vill hjälpa kunden att använda konfigurationspaketet kan du lägga till ett frågeformulär eller en uppsättning frågeformulär i paketet. Frågeformuläret kan hjälpa till kunden att förstå de olika inställningsalternativen. Frågeformulär skapas vanligtvis för de större inställningstabellerna där en kund kan kräva ytterligare vägledning om hur han/hon väljer en lämplig inställning. Mer information finns i [Samla inställningsvärden för kund](admin-gather-customer-setup-values.md).

Kontrollera att du är på implementerings-rollcentret för RapidStart Services. Mer information finns i [Använd implementerings-rollcentret för RapidStart Services](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md).

> [!IMPORTANT]  
>  När du exporterar och importerar konfigurationspaket mellan två företagsdatabaser ska databaserna ha samma schema för att alla data säkert ska överföras korrekt. Det betyder att databaserna ska ha samma tabell- och fältstruktur, där tabellerna har samma primärnycklar och fälten har samma ID och datatyper.  
>   
>  Du kan importera ett konfigurationspaket som har exporterats från en databas och har ett annat schema än i måldatabasen. Men alla tabeller och fält i konfigurationspaketet som saknas i måldatabasen importeras inte. Tabeller med olika primärnycklar och fält med olika datatyper importeras inte heller korrekt. Om t.ex. konfigurationspaketet innehåller tabellen **50000, Kund** som har primärnyckeln **Code20** och databasen som du importerar paketet till innehåller tabellen **50000, Kundbankkonto** som har primärnyckeln **Code20 + Code 20**, så importeras inga data.  

## <a name="to-create-a-configuration-package"></a>Så här skapar du ett konfigurationspaket  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationspaket** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i övriga fält på snabbfliken **Allmänt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Om du vill utesluta konfigurationsfrågeformulären, konfigurationsmallarna och konfigurationskalkylarkstabellerna från paketet markerar du kryssrutan **Uteslut konfigurationstabeller**. Annars kommer de här tabellerna att läggas till listan över pakettabeller automatiskt när du exporterar paketet.  
5. Välj åtgärden **Hämta tabeller**. Sidan **Hämta pakettabell** öppnas.  
6. Välj fältet **Markera tabeller**. Sidan **Konfigurationsurval** öppnas.  
7. Välj åtgärden **Markera allt** för att lägga till alla tabeller i paketet, eller markera kryssrutan **Vald** för varje tabell i listan som du vill lägga till.
8. Välj **OK**. Antalet tabeller som du har valt visas i fältet **Markera tabeller**. Ange ytterligare alternativ och välj sedan knappen **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller som läggs till på raderna på sidan **konfiguration. Paket**.  

    > [!NOTE]  
    >  Du kan också göra detta i konfigurationskalkylarket. Markera tabellerna som du vill ta med i paketet och välj sedan åtgärden **Tilldela paket**.

9. Om du vill markera fält som ska tas med från en tabell markerar du tabellen och väljer i fliken **Rader** sedan åtgärden **Fält**.
Ange vilka fält som ingår i paketet. Som standard inkluderas alla fält.

    - För att välja endast de fält som du vill inkludera, välj åtgärden **Rensa inkluderade**. Om du vill lägga till alla fält väljer du åtgärden **Ange inkluderade**.  
    - Om du vill ange att fältdata inte ska valideras avmarkerar du kryssrutan **Validera fält** för fältet.  

10. Bestäm huruvida du har introducerat potentiella fel genom att välja åtgärden **Validera paket**. Detta kan hända när tabeller som konfigurationen beror på inte ingår.  
11. Välj knappen **OK**.  

När du har förfinat listan över fält som ska ingå från en tabell, kan du se resultatet i Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Filtrera och granska din datauppsättning  
1. För att filtrera en viss uppsättning poster som ska inkluderas i paketet väljer du i fliken **Rader** åtgärden **Filter** och anger sedan lämpliga filtervärden.  
2. På paketkortets flik **Rader** väljer du åtgärden **Exportera till Excel**.  
3. Bekräfta meddelandena som aktiverar exporten av data till Excel. Den namngivna .xlsx-filen öppnas. Granska posterna som har exporterats.  
4. Stäng Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Ta med en mall för koppling till en tabell  
För vissa tabeller, sådana tabeller som innehåller huvuddata, kan du ange en mall som kopplas till datan. Mallen kan ta med de obligatoriska fälten som du vill koppla till alla huvuddata, och som du inte vill variera. Du kan till exempel skapa en mall som kan användas med kunddata. Mallen kan innehålla alla de obligatoriska fälten som sedan aktiverar konsekvent import av standardiserad information. Informationen som inte kan standardiseras, till exempel kundnamn, hanteras när du importerar kunddata.

1. På sidan **Konfig. paketkort** väljer du en tabell och sedan fältet **Datamall**. En lista över mallar baserade på tabellen visas.
2. Markera en mall och välj sedan knappen **OK**.  

När paketet är färdigt följer du nästa procedur om du vill spara paketet till en fil. Du kan sedan ge paketet till en kund eller en partner för användning.

### <a name="to-save-and-export-a-configuration-package"></a>Spara och exportera ett konfigurationspaket  
- På sidan **Konfig. paketkort** väljer du åtgärden **Exportera paket**.  

Paketet skapas i en .rapidstart-fil, vilket levererar paketinnehållen i ett komprimerat format. Konfigurationsfrågeformulär, konfigurationsmallar och konfigurationskalkylark läggs till paketet automatiskt, såvida du inte väljer att utesluta dem.  

Du kan spara filen med ett namn som är meningsfullt för dig, men du kan inte ändra filtillägget. Det måste vara .rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Kopiera ett konfigurationspaket  
När du har skapat ett paket som uppfyller de flesta av behoven kan du använda det som en grund för att skapa liknande paket. Det kan påskynda implementeringstiden och gör det lättare att upprepa RapidStart Services.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationspaket** och välj sedan relaterad länk.  
2. Välj ett paket i listan och välj sedan åtgärden **Kopiera paket**.  
3. I fältet **Kod för nytt paket** anger du en kod för det nya paketet.  
4. Markera kryssrutan **Kopiera data** om du också vill kopiera databasdata från det befintliga paketet.  
5. Välj knappen **OK**.

## <a name="to-customize-a-configuration-package"></a>Så här anpassar du ett konfigurationspaket
Använd konfigurationskalkylarket för att samla ihop och kategorisera information som du vill använda för att konfigurera ett nytt företag, och ordna tabellerna på ett logiskt sätt. Formateringen i kalkylarket baseras på en enkel hierarki: områden innehåller grupper, som i sin tur innehåller tabeller. Områden och grupper är valfria, men nödvändiga om du vill kunna se en översikt över konfigurationsprocessen i rollcentret för RapidStart Services.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.  
2.  Välj **Område** i fältet **Radtyp**. Ange ett beskrivande namn i fältet **Namn**.  
3.  Välj **Grupp** i fältet **Radtyp**. Ange ett beskrivande namn i fältet **Namn**.  
4.  Välj **Tabell** i fältet **Radtyp**. Välj tabellen som du vill ta med i kalkylarket i fältet **Tabell-ID**.  

Du kan nu tilldela tabellerna till specifika konfigurationspaket som du har skapat eller planerar att skapa. För mer information, se [Så här tilldelar du en tabell till ett konfigurationspaket](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Så här kan du arbeta med prioriterade tabeller  
1. Markera kryssrutan **Prioriterad tabell** för att framhäva en tabell som ofta ska användas under inställning av en typisk kund, till exempel tabellen **Redovisningskonto**. När en tabell har den här beteckningen ska en kund enkelt kunna filtrera sitt kalkylark för att bara se listan över prioriterade tabeller som behöver åtgärdas.  
2. Välj åtgärden **Endast visade** för att visa den filtrerade vyn. Listan över tabeller innehåller endast de tabeller där den här kryssrutan är markerad.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Så här tilldelar du en tabell till ett konfigurationspaket  
När du har definierat tabeller som du vill hantera som en del av konfigurationen, kan du enkelt tilldela tabellerna till konfigurationspaket. En tabell kan endast tilldelas till ett paket. I följande procedur tilldelar du paketet inifrån konfigurationskalkylarket.  

> [!NOTE]  
>  Du kan också skapa ett paket direkt och lägga till tabeller i det. För mer information, se [Så här skapar du ett konfigurationspaket](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.
2. Markera en rad eller en grupp med rader som du vill tilldela till ett konfigurationspaket i konfigurationskalkylarket, och välj sedan åtgärden **Tilldela paket**.  
3.  Välj ett paket i listan eller välj åtgärden **Nytt** för att skapa ett nytt paket, och välj sedan knappen **OK**.  

    Om en tabell inte redan finns i paketet läggs det till nu. Paketkodfältet på kalkylarksraden ska fyllas i med koden på paketet som tabellen har tilldelats till.  
4. Om du väljer ett befintligt paket kan du se hur många tabeller som redan finns i paketet genom att granska informationen i fältet **Antal tabeller**.

## <a name="to-review-or-customize-existing-database-data"></a>Så här granskar och anpassar du befintliga databasdata
När du skapar ett konfigurationspaket för en lösning kan du visa och anpassa tillgängliga databasdata så att dessa stämmer överens med dina kundbehov. Databastabellen måste vara kopplad till en sida.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.
2. Identifiera tabellerna med data som du vill visa eller anpassa i konfigurationskalkylarket.  

    > [!NOTE]  
    >  Se till att varje tabell tilldelats ett sid-ID. Som standarden [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell fylls detta värdet i automatiskt. För anpassade tabeller måste du ange ID.

3. Välj åtgärden **Databasdata**. Sidan för den relaterade sidan öppnas.
4. Granska den tillgängliga informationen. Ändra den efter behov genom att ta bort transaktioner som inte är relevanta eller lägga till nya.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Så här kopierar du data från en testmiljö till en produktionsmiljö  
När du har kontrollerat och testat alla inställningar kan du fortsätta med att kopiera informationen till din produktionsmiljö. Du skapar ett nytt företag i samma databas.

1. Öppna och initialisera det nya företaget.  
2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.  
3. Välj åtgärden **Kopiera data från företag**.  
4. På sidan **Kopiera från** i fönstret **Kopiera företagsdata**. Sidan **Företag** visas.  
5. Välj det företag som du vill kopiera data ifrån och välj sedan knappen **OK**. En lista över tabeller som har valts i konfigurationskalkylarket öppnas. Endast tabeller som innehåller poster tas med i listan.
6. Välj de tabeller som du vill kopiera data ifrån, och välj sedan åtgärden **Kopiera data**. Välj **OK** på sidan **Kopiera företagsdata**.  

## <a name="see-also"></a>Se även  
[Samla in kundinställningsvärden](admin-gather-customer-setup-values.md)  
[Ställa in företagskonfiguration](admin-set-up-company-configuration.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)

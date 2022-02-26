---
title: Skapa arbetsflöden för att koppla aktiviteter
description: Du kan skapa arbetsflöden som sammankopplar affärsprocesser som utförs av olika användare, samt inkludera systemaktiviteter som automatisk bokföring, som arbetsflödessteg.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2021
ms.author: edupont
ms.openlocfilehash: 2734f4d65869ba666a53333c9338239a1cb1a1b4
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588232"
---
# <a name="create-workflows-to-connect-business-process-tasks"></a>Skapa arbetsflöden för att koppla affärsprocessuppgifter

Du kan skapa arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar med svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

När du skapar arbetsflöden kan du kopiera stegen från befintliga arbetsflöden eller från arbetsflödesmallar. Arbetsflödesmallar representerar icke-redigerbara arbetsflöden som finns i den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)]. Koden för arbetsflödesmallar som läggas till av Microsoft har prefixet ”MS-”, till exempel "MS-PIW”. Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).  

Om ditt företagsscenario kräver arbetsflödeshändelser eller svar som inte stöds måste en Microsoft-partner implementera dem genom att skapa ett tillägg som implementerar det relevant arbetsflödeshändelse.  

> [!NOTE]  
> Alla meddelanden om arbetsflödessteg skickas via en jobbkö. Kontrollera att jobbkön återspeglar dina affärsbehov. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustration av ett exempel på ett arbetsflöde.":::

Arbetsflödet är uppdelat i tre delar:

1) **När händelse** Det är här som utlösaren väljs.
    Exempel på utlösare kan vara:
    - En huvuddatapost ändras
    - En journalrad skapas
    - ett inkommande dokument skapas eller släpps
    - Godkännande av ett dokument krävs

2) **På villkor** **Villkoren** är relaterade till händelsen och öppnas för att skapa filter för när händelsen utlöses
3) **Sedan svar** **Svaren** svarar till det som nästa steg i arbetet är.

För båda typerna av händelser är händelserna systemdefinierade. Nya händelser måste läggas till genom utveckling av ett tillägg.

## <a name="to-create-a-workflow"></a>Skapa ett arbetsflöde

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflöde** visas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Så här skapar du arbetsflödet från en arbetsflödesmall, på sidan **Arbetsflöden**, välj åtgärden **Så här skapar du arbetsflödet från en arbetsflödesmall**. Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).  
5. Beskriv arbetsflödet i fältet **Beskrivning**.  
6. I fältet **kategorin** ange kategorin som arbetsflödet tillhör.  
7. I fältet **När händelse** ange den händelse som måste uppstå för att starta arbetsflödessteget.  

    När du väljer fältet öppnas sidan **Arbetsflödeshändelse** där du kan välja mellan alla arbetsflödeshändelser som finns  
8. I fältet **Tillstånd** skriver du ett eller flera villkor som måste uppfyllas innan händelsen i fältet **När händelse** kan uppstå.  

    När du väljer fältet öppnas sidan **Händelseförhållanden** där du väljer från en lista med filterfält som är relevanta som villkor för händelsen i fråga. Du kan lägga till nya filterfält som du vill använda som händelsevillkor. Du ställer in händelsevillkorfilter så som du ställer in filter på rapportsidor.  

    Om arbetsflödeshändelsen är ändringen av ett visst fält i en post, då öppnas sidan **Händelsevillkor** med alternativ för att markera fältet och typen av ändring.  

    1. Så här anger du en fältändring för händelsen: i sidan **Händelsevillkor**, i fältet **Fält**, markerar du det fält som ska ändras.  
    2. Välj antingen **Minskad**, **Ökad** eller **Ändrad** i fältet **Operator**.  
9. I fältet **Sedan svar** anger du svaret som ska följa när arbetsflödeshändelsen inträffar.  

     När du väljer fältet öppnas sidan **Arbetsflödessvar** där du kan välja mellan alla arbetsflödessvar som finns och ange svarsalternativ för det valda svaret.  
10. På snabbfliken **Alternativ för valt arbetsflödessvar** anger du alternativ för arbetsflödessvaret genom att välja värden i de olika fälten som visas, enligt följande:  

    1. Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skicka ett meddelande.  

        |Fält|Beskrivning|  
        |-----|-----------|  
        |**Meddela avsändare**|Ange om den som har fått godkännandet ska meddelas i stället för mottagaren om godkännandeförfrågan. Om du markerar kryssrutan inaktiveras fältet **Mottagarens användar-ID** eftersom den som skickar godkännandet kommer att meddelas i stället. Namnet på arbetsflödessvar ändras enligt detta till **skapa ett meddelande för &lt;avsändaren&gt;**. Om kryssrutan inte är markerad kan namnet på arbetsflödetssvar **skapa ett meddelande för &lt;användaren&gt;**.
        |**Mottagarens användar-ID**|Ange den användare som meddelande ska skickas till. **Obs**! Alternativet är bara tillgängligt för arbetsflödesvar med en platshållare för en specifik användare. För arbetsflödesvar utan platshållare för användare definieras meddelandemottagaren vanligtvis av inställningen av godkännandeanvändare.|  
        |**Transaktionstyp för meddelande**|Anger om arbetsflödesmeddelandet utlöses av en poständring, en begäran om godkännande eller en data som har passerats.|
        |**Målsida för länk**|Ange en annan sida som länken i meddelandet öppnar i stället för standardsidan. Observera att sidan måste ha samma källtabell som posten.|
        |**Anpassad länk**|Ange URL-adressen till en länk som läggs till i meddelandet utöver länken till sidan.|  

    2. Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skapa en godkännandebegäran.  

        |Fält|Description|  
        |-----|-----------|  
        |**Formel för förfallodatum**|Ange hur många dagar det är kvar tills godkännandebegäran måste lösas från datumet då det skickades.|
        |**Delegera efter**|Ange om och när en godkännandebegäran delegeras automatiskt till den relevanta ersättaren. Du kan välja att automatiskt delegera en, två eller fem dagar efter datumet när godkännandet begärdes.|
        |**Godkännartyp**|Ange vem godkännaren är, enligt inställningarna av godkännandeanvändare och arbetsflödesanvändare. När fältet anges till **Säljare/Inköpare** som anger att användaren som ställs in i fältet **Säljare/inköpare kod** i sidan **Användarinställningar för godkännande** fastställer godkännaren. Godkännandebegäranposter skapas sedan enligt värdet i fältet **Gränstyp för godkännare**. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-workflow-users.md).|
        |**Visa bekräftelsemeddelande**|Ange om ett bekräftelsemeddelande visas för användarna när de har begärt ett godkännande.|
        |**Gränstyp för godkännare**|Ange hur godkännares godkännandegränser påverkas när godkännandebegärandeposter skapas för dem. En kvalificerad godkännare är en godkännare vars godkännandegräns är högre än värdet på begäran. Följande alternativ finns. <ol><li>**Godkännarkedja** anger att godkännandebegärandeposter skapas för alla begärandens godkännare upp till och med den första kvalificerade godkännaren.</li><li>**Direkt godkännare** anger att en godkännandebegärandepost skapas endast för begärandens omedelbara godkännare, oberoende av godkännarens godkännandegräns.</li><li>**Första kvalificerade godkännare** anger att en godkännandebegärandepost skapas endast för begärandens första kvalificerade godkännare.</li></ol>|
    3. Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skapa journalrader.  

        |Fält|Description|  
        |-----|-----------|  
        |**Namn på redovisningsjournalmall**|Ange namnet på redovisningsjournalmallen som de angivna journalraderna skapas i.|  
        |**Redovisningsjournalnamn**|Ange namnet på redovisningsjournalbatchen som de angivna journalraderna skapas i.|  

11. Välj knapparna **Öka indrag** och **Minska indrag** för att göra ett indrag för händelsenamnet i fältet **När** för att definiera stegets position i arbetsflödet.  

    1. Ange att steget är nästa i arbetsflödesföljden genom att göra ett indrag för händelsenamnet i det föregående steget.  
    2. Ange att steget är ett av flera alternativa steg som kan startas beroende på dess villkor genom att placera händelsenamnet med samma indrag som de andra alternativa stegen. Ordna sådana valfria efter prioritet genom att placera det viktigaste steget först.  

    > [!NOTE]  
    >  Du kan endast ändra indrag för ett steg som inte har ett efterföljande steg.  

12. Upprepa steg 7 till 11 för att lägga till fler arbetsflödessteg, antingen före eller efter steget som du precis har skapat.  
13. Markera kryssrutan **Aktiverad** för att ange att arbetsflödet ska starta så snart som händelsen i det första steget av typen **Insteg** inträffar. Mer information finns i [Använda arbetsflöden](across-use-workflows.md).  

> [!NOTE]  
> Aktivera inte ett arbetsflöde förrän du vet att arbetsflödet är avslutat och att relevanta arbetsflödessteg kan startas.  

> [!TIP]  
> Om du vill visa relationer mellan tabeller som används i arbetsflöden väljer du den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **arbetsflöde – tabellrelationer**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Exempel på hur du skapar ett nytt arbetsflöde med hjälp av befintliga händelser

I följande exempel görs ett nytt arbetsflöde för att godkänna ändringar av namnet på en befintlig leverantör:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflöde** visas.
3. I arbetsflödet, fyll i fälten enligt beskrivningen i följande tabell på snabbfliken Alternativ.

    |Fält  |Värde  |
    |---------|---------|
    |**Kod**|**VENDAPN-01**|
    |**Beskrivning**|**Godkännande av ändring av leverantörens namn** |
    |**Kategori**|**INKÖP**|

4. Skapa det första arbetsflödessteget enligt följande instruktioner.

    1. I fältet **när händelse** anger du att *en leverantörspost har ändrats*.  
    2. I fältet **på villkor** väljer du ordet **alltid** och på sidan **Händelsevillkor** lägg till **Lägg till ett villkor för när ett fältvärde ändras** och markerar sedan fältet *namn*.  

      Resultatet av det här steget är att villkoret läses som *namn ändras*.  
    3. I fältet **Sedan svar**, välj länken **Välj svar** och sedan på sidan **Arbetsflödessvar** i fältet **Välj svar**, välj *Återställ värdet för fältet \<Field\> på posten och spara ändringar* och sedan i avsnittet **Alternativ för valda svar** anger du fältet *Namn*.  
    4. Välj länken **Lägg till fler svar** och lägg till en post för *skapa en godkännandebegäran för posten med hjälp av typen god kännare <%1> och <%2>.* svar.  
    5. I avsnittet **alternativ för det valda svar** för det nya svaret ändrar du fältet **godkännartyp** till *Arbetsflödesanvändargrupp* och anger sedan relevant användargrupp i fältet **Arbetsflödesanvändargrupp**.  

    Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  
    6. Lägg till ett tredje svar *Skicka godkännandebegäranden för posten och skapa ett meddelande*.  
    7. Lägg till ett fjärde svar, *Visa meddelande "%1"* och sedan, i avsnittet **alternativ för markerade svar**, i fältet meddelande, anger du att **en begäran om godkännande har skickats**.  
    8. Välj knappen OK om du vill återvända till arbetsflödessteget.  

5. Lägg till ett nytt arbetsflödessteg för *en begäran om godkännande på nästa rad*. händelse.  

    1. I fältet **När händelse** ange *en begäran om godkännande på nästa rad*.  
    2. Välj radmenyn och välj sedan **öka indrag**.  
    3. I fältet **På villkor** välj ordet **Alltid** och sedan i fältet **Väntar på godkännanden** anger du *0*.  

      Resultatet av det här steget är att villkoret läses som *Väntar på godkännanden:0* för att ange att det är den sista godkännaren.  
    4. I fältet **Sedan svar**, välj länken **Välj svar** och sedan på sidan **Arbetsflödessvar** i fältet **Välj svar** väljer du svaret *Skicka godkännandebegäranden för posten och skapa ett meddelande*.  
    5. Välj OK.  
6. Lägg till ett andra arbetsflödessteg för händelsen *en begäran om godkännande på nästa rad*.  

    1. I fältet **När händelse** ange *en begäran om godkännande på nästa rad*.
    2. I fältet **På villkor** välj ordet **Alltid** och sedan i fältet **Väntar på godkännanden** anger du *>0*.  

      Resultatet av det här steget är att villkoret läses som *Väntar på godkännanden:>0* för att ange att det *inte* är den sista godkännaren.  
    3. I fältet **Sedan svar**, välj länken **Välj svar** och sedan på sidan **Arbetsflödessvar** i fältet **Välj svar** väljer du svaret *Skicka godkännandebegäranden för posten och skapa ett meddelande*.  
    4. Välj OK.  
7. Lägg till ett arbetsflödessteg för händelsen *en begäran om godkännande har avvisats*.  

    1. I fältet **När händelse** ange *en begäran om godkännande har avvisats*.  
    2. I fältet **På villkor** lämnar du värdet som *Alltid*.  
    3. I fältet **Sedan svar**, välj länken **Välj svar** och sedan på sidan **Arbetsflödessvar** i fältet **Välj svar** väljer du svaret *Avvisa nya värden*.  
    4. Välj länken **Lägg till fler svar** och lägg till en post för svaret *Avvisa godkännandebegäran för posten och skapa ett meddelande*.
    5. Välj OK.  
8. Lägg till ett andra arbetsflödessteg för händelsen *en begäran om godkännande har avvisats*.  

    1. I fältet **När händelse** ange *en begäran om godkännande har avvisats*.  
    2. I fältet **På villkor** lämnar du värdet som *Alltid*.  
    3. I fältet **Sedan svar**, välj länken **Välj svar** och sedan på sidan **Arbetsflödessvar** i fältet **Välj svar** väljer du svaret *Skicka godkännandebegäranden för posten och skapa ett meddelande*.  
    4. Välj OK.  
9. Välj fältet **aktiverad** om du vill aktivera arbetsflödet.  

Följande illustrationer ger en översikt över resultatet av proceduren.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustration av arbetsflödet för godkännande av leverantörsnamn.":::

Sedan måste du och testa arbetsflödet genom att öppna en befintlig leverantör och ändra namnet. Kontrollera att en begäran om godkännande har gjorts när du ändrar leverantörens namn.

## <a name="see-also"></a>Se även

[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  
[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Ta bort arbetsflöden](across-how-to-delete-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden](across-set-up-workflows.md)  
[Använda arbetsflöden](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

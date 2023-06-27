---
title: Skapa arbetsflöden för godkännande för att koppla aktiviteter
description: Lär dig skapa arbetsflöden som kopplar uppgifter som utförs av olika människor i affärsprocesser.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
---
# <a name="create-workflows-to-connect-tasks-in-business-processes" />Skapa arbetsflöden för att koppla uppgifter i affärsprocesser

Du kan skapa arbetsflöden som kopplar uppgifter i affärsprocesser som ska utföras av olika användare. Du kan inkludera systemuppgifter, till exempel automatisk bokföring, som ett steg i arbetsflöden som är före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange stegen på raderna. Varje steg består av en utlösare och ett svar:

* En händelse som anger de villkor som gäller för att starta arbetsflödet.
* Ett arbetsflödessvar som definierar vad arbetsflödet gör.

[!INCLUDE[workflow](includes/workflow.md)]

När du skapar arbetsflöden kan du kopiera stegen från befintliga arbetsflöden eller från arbetsflödesmallar. Arbetsflödesmallar är icke-redigerbara arbetsflöden som [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller. Identifierare för arbetsflödesmallar har prefixet ”MS-”, till exempel "MS-PIW”. Läs mer på [Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  

> [!NOTE]  
> Alla meddelanden om arbetsflödessteg skickas via en jobbkö. Kontrollera att jobbkön återspeglar dina affärsbehov. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustration av ett exempel på ett arbetsflöde.":::

Ett arbetsflöde är uppdelat i tre delar:

1. **När händelse**  
   Det är här som utlösaren väljs.  
   Exempel på utlösare kan vara:
   * En huvuddatapost ändras
   * En journalrad skapas
   * Ett inkommande dokument skapas eller släpps
   * Godkännande av ett dokument krävs
2. **Vid villkor**  
   **Villkoren** är relaterade till händelsen och tillåter att filter skapas för att bestämma hur arbetsflödet ska fortsätta.
3. **Då svar**  
   **Svaren** anger nästa steg i arbetsflödet.

Alternativen för båda händelser och svar är systemdefinierade. Om du vill lägga till nya alternativ måste du utveckla ett tillägg.

## <a name="to-create-a-workflow" />Skapa ett arbetsflöde

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflöde** visas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Så här skapar du arbetsflödet från en arbetsflödesmall, på sidan **Arbetsflöden**, välj åtgärden **Nytt arbetsflöde från en arbetsflödesmall**. Läs mer på [Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  
5. Beskriv arbetsflödet i fältet **Beskrivning**.  
6. I fältet **kategorin** ange kategorin som arbetsflödet tillhör.  
7. I fältet **När händelse** ange den händelse som måste uppstå för att starta arbetsflödessteget.  

   När du väljer fältet öppnas sidan **Arbetsflödeshändelse** som anger alla arbetsflödeshändelser som är tillgängliga.  
8. I fältet **På villkor** skriver du ett eller flera villkor som måste uppfyllas innan händelsen i fältet **När händelse** kan uppstå.  

   När du väljer fältet visar sidan **Händelsevillkor** filterfält som kan vara villkor för händelsen. Du kan lägga till nya filterfält om du vill.  

   Om arbetsflödeshändelsen är ändringen av ett visst fält i en post, använd sidan **Händelsevillkor** med för att markera fältet och typen av ändring.  

   1. Så här anger du en fältändring för händelsen: i sidan **Händelsevillkor**, i fältet **Fält**, markerar du det fält som ska ändras.  
   2. Välj antingen **Minskad**, **Ökad**eller **Ändrad** i fältet **Operator**.  
9. I fältet **Sedan svar** anger du svaret som ska följa när arbetsflödeshändelsen inträffar.  

   När du väljer fältet öppnas sidan **Arbetsflödessvar** som anger alla arbetsflödessvar och svarsalternativ som är tillgängliga.  
10. På snabbfliken **Alternativ för valt arbetsflödessvar** anger du alternativ för arbetsflödessvaret genom att välja värden i de olika fälten som visas, enligt följande:  

    1. Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skicka ett meddelande.  

    > [!NOTE]
    > Dessa fält varierar beroende på vilket svar du valt.

       |Fält|Description|
       |-----|-----------|
       |**Meddela avsändare**|Ange om den som har fått godkännandet ska meddelas i stället för mottagaren om godkännandeförfrågan. Om du markerar kryssrutan inaktiveras fältet **Mottagarens användar-ID** eftersom den som skickar godkännandet kommer att meddelas i stället. Namnet på arbetsflödessvar ändras enligt detta till **skapa ett meddelande för &lt;avsändaren&gt;**. Om kryssrutan inte är markerad kan namnet på arbetsflödessvar **skapa ett meddelande för &lt;användaren&gt;**.|
       |**Mottagarens användar-ID**|Ange den användare som meddelande ska skickas till. **Obs**! Alternativet är bara tillgängligt för arbetsflödesvar med en platshållare för en specifik användare. För arbetsflödesvar utan platshållare för användare definieras meddelandemottagaren vanligtvis av **inställningen av godkännandeanvändare**.|
       |**Transaktionstyp för meddelande**|Ange en utlösare för arbetsflödesmeddelandet. Utlösaren kan vara en ändring av posten, en godkännandebegäran eller ett förfallodatum som har passerat.|
       |**Målsida för länk**|Ange sidan som länken i meddelandet öppnas på. Sidan måste ha samma källtabell som posten.|
       |**Anpassad länk**|Ange URL-adressen till en länk som läggs till i meddelandet utöver länken till sidan.|

    2. Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skapa en godkännandebegäran.  

       |Fält|Description|  
       |-----|-----------|  
       |**Formel för förfallodatum**|Ange antalet dagar som godkännaren har för att svara på begäran. Perioden inleds när begäran skickas.|
       |**Delegera efter**|Ange om och när en godkännandebegäran delegeras automatiskt till ersättaren. Du kan välja att automatiskt delegera en, två eller fem dagar efter datumet när godkännandet begärdes.|
       |**Godkännartyp**|Ange vem godkännaren är, enligt inställningarna av godkännandeanvändare och arbetsflödesanvändare. När fältet anges till **Säljare/Inköpare** användaren som anges i fältet **Säljare/inköpare kod** i sidan **Användarinställningar för godkännande** fastställer godkännaren. Godkännandebegäranposter skapas sedan enligt värdet i fältet **Gränstyp för godkännare**. Läs mer i [Så här skapar du användare för godkännande](across-how-to-set-up-workflow-users.md).|
       |**Visa bekräftelsemeddelande**|Ange om ett bekräftelsemeddelande visas för användarna eller inte när en användare begär ett godkännande.|
       |**Gränstyp för godkännare**|Ange effekten av begränsningar för godkännare. En godkännares godkännandegräns måste vara över värdet i begäran. Följande alternativ finns: <ol><li>**Godkännarkedja** anger att godkännandebegärandeposter skapas för alla begärandens godkännare upp till och med den första kvalificerade godkännaren.</li><li>**Direkt godkännare** anger att en godkännandebegärandepost skapas endast för begärandens omedelbara godkännare, oberoende av godkännarens godkännandegräns.</li><li>**Första kvalificerade godkännare** anger att en godkännandebegärandepost skapas endast för begärandens första godkännare.</li><li>**Specifik godkännare** anger att användaren ska meddelas i fältet **godkännar-ID**.</li></ol>|

    3. Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skapa journalrader.  

       |Fält|Description|  
       |-----|-----------|  
       |**Namn på redovisningsjournalmall**|Ange namnet på redovisningsjournalmallen som de angivna journalraderna skapas i.|  
       |**Redovisningsjournalnamn**|Ange namnet på redovisningsjournalbatchen som de angivna journalraderna skapas i.|  

11. Välj knapparna **Öka indrag** och **Minska indrag** för att göra ett indrag för händelsenamnet i fältet **När** för att definiera stegets position i arbetsflödet.  

    1. Dra in händelsen under namnet på föregående steg för att ange att det är nästa steg.  
    2. Ange att steget är ett av flera alternativa steg som kan startas beroende på dess villkor genom att placera händelsenamnet med samma indrag som de andra alternativa stegen. Ordna sådana valfria efter prioritet genom att placera det viktigaste steget först.  

    > [!NOTE]  
    >  Du kan endast ändra indrag för ett steg som inte har ett efterföljande steg.  

12. Upprepa steg 7 till 11 för att lägga till fler arbetsflödessteg, antingen före eller efter steget som du har skapat.  
13. Aktivera växlingskontrollen **Aktiverad** för att ange att arbetsflödet ska starta när händelsen i det första steget av typen **Insteg** inträffar. Läs mer i [Använd arbetsflöden](across-use-workflows.md).  

> [!NOTE]  
> Aktivera inte ett arbetsflöde förrän du är säker på att det är klart.  

> [!TIP]  
> Om du vill utforska relationer mellan tabeller som används i arbetsflöden väljer du ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **arbetsflöde – tabellrelationer**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events" />Exempel på hur du skapar ett nytt arbetsflöde med hjälp av befintliga händelser

Följande exempel skapar ett arbetsflöde för att godkänna en ändring av namnet på en leverantör:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflöde** visas.
3. I arbetsflödet, fyll i fälten enligt beskrivningen i följande tabell på snabbfliken Alternativ.

    |Fält  |Värde  |
    |---------|---------|
    |**Kod**|**VENDAPN-01**|
    |**Beskrivning**|**Godkännande av ändring av leverantörens namn** |
    |**Kategori**|**INKÖP**|

4. Skapa det första arbetsflödessteget enligt följande instruktioner.

    1. I fältet **när händelse** anger du att *en leverantörspost har ändrats*.  
    2. I fältet **På villkor** lämnar du ordet som **Alltid**. På sidan **Händelsevillkor** lägg till **Lägg till ett villkor för när ett fältvärde ändras** och markerar sedan fältet **namn**. Resultatet av det här steget är att villkoret läses som *namn ändras*.  
    3. I fältet **Sedan svar** välj länken **Välj svar**. På sidan **Arbetsflödessvar** i fältet **Välj svar** välj svaret **Återställ värdet för fältet \<Field\> på posten och spara ändringar**. Sedan i avsnittet **alternativ för markerade svar** ange fältet **Namn**.  
    4. Välj länken **Lägg till fler svar** och lägg till en post för **skapa en godkännandebegäran för posten med hjälp av typen god kännare <%1> och <%2>** svar.  
    5. I avsnittet **Alternativ för markerade svar** för det nya svaret ändrar du fältet **Godkännartyp** till **Arbetsflödesanvändargrupp**. I fältet **Arbetsflödesanvändargrupp** anger du sedan användargruppen. Läs mer i [Så här skapar du användare för godkännande](across-how-to-set-up-approval-users.md).  
    6. Lägg till ett tredje svar **Skicka godkännandebegäranden för posten och skapa ett meddelande**.  
    7. Lägg till ett fjärde svar **Visa meddelande "%1"**. Sedan i avsnittet **Alternativ för markerade svar** i fältet **Meddelande** ange **En begäran om godkännande har skickats**.  
    8. Välj **OK** om du vill återvända till arbetsflödessteget.  

5. Lägg till ett nytt arbetsflödessteg för händelsen **en begäran om godkännande på nästa rad**.

    1. I fältet **När händelse** ange **en begäran om godkännande på nästa rad**.  
    2. Välj radmenyn och välj sedan **öka indrag**.  
    3. I fältet **På villkor** väljer du **Alltid**. I fältet **Väntar på godkännanden** anger du **0**. Villkoret läses som **Väntar på godkännanden:0** för att indikera att begäran inte kräver fler godkännare.  
    4. I fältet **Sedan svar** välj länken **Välj svar**. På sidan **Arbetsflödessvar** i fältet **Välj svar**, välj svaret **Skicka godkännandebegäranden för posten och skapa ett meddelande**.  
    5. Välj **OK**.  
6. Lägg till ett andra arbetsflödessteg för händelsen **en begäran om godkännande på nästa rad**.  

    1. I fältet **När händelse** ange **en begäran om godkännande på nästa rad**.
    2. I fältet **På villkor** väljer du **Alltid**. I fältet **Väntar på godkännanden** anger du **>0**. Villkoret läses som **Väntar på godkännanden:>0** för att ange att det är den sista godkännaren.  
    3. I fältet **Sedan svar** välj länken **Välj svar**. På sidan **Arbetsflödessvar** i fältet **Välj svar**, välj svaret **Skicka godkännandebegäranden för posten och skapa ett meddelande**.  
    4. Välj **OK**.  
7. Lägg till ett arbetsflödessteg för händelsen **en begäran om godkännande har delegerad**.  

    1. I fältet **När händelse** ange **en begäran om godkännande är delegerad**.  
    2. I fältet **På villkor** lämnar du värdet som **Alltid**.  
    3. I fältet **Sedan svar** välj länken **Välj svar**. På sidan **Arbetsflödessvar** i fältet **Välj svar**, välj svaret **Skicka godkännandebegäranden för posten och skapa ett meddelande**.  
    4. Välj **OK**.  
8. Lägg till ett andra arbetsflödessteg för händelsen **en begäran om godkännande har avvisats**.  

    1. I fältet **När händelse** ange **en begäran om godkännande har avvisats**.  
    2. I fältet **På villkor** lämnar du värdet som **Alltid**.  
    3. I fältet **Sedan svar** välj länken **Välj svar**. På sidan **Arbetsflödessvar** i fältet **Välj svar** välj **Avvisa nya värden**.  
    4. Välj länken **Lägg till fler svar** och lägg till en post för svaret **Avvisa godkännandebegäran för posten och skapa ett meddelande**
    5. Välj **OK**.  
9. För att aktivera arbetsflödet, aktivera växlingskontrollen **Aktiverad**.  

Följande illustrationer ger en översikt över resultatet av proceduren.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustration av arbetsflödet för godkännande av leverantörsnamn.":::

Sedan måste du och testa arbetsflödet genom att öppna en befintlig leverantör och ändra namnet. Kontrollera att en begäran om godkännande har gjorts när du ändrar leverantörens namn.

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also" />Se även

[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  
[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Konfigurera aviseringar för arbetsflöde](across-setting-up-workflow-notifications.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Ta bort arbetsflöden för godkännande](across-how-to-delete-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

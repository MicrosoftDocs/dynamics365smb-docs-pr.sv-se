---
title: 'Genomgång: Genomföra en försäljningskampanj'
description: Den här genom gången innehåller en detaljerad översikt över alla aktiviteter som ingår i en försäljningskampanj i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Genomgång: Genomföra en försäljningskampanj

En kampanj är alla typer av aktiviteter som inkluderar flera kontakter. En viktig del när man planerar en kampanj är att välja målgrupp för kampanjen. Av den anledningen skapar du ett segment, eller en grupp med kontakter, med hjälp av filter i [!INCLUDE[prod_short](includes/prod_short.md)].  

 Du använder dessa funktioner i Försäljning och marknadsföring för att noggrant planera dina marknadsaktiviteter och hantera dina aktiviteter med kontakter och kunder. Du kan skapa kampanjer och lägga upp segment för utskick och andra typer av aktiviteter med dina kontakter och eventuella kunder.  

 Med kampanj- och segmentfunktionerna och tillhörande automatiserade processer kan du planera, organisera och hålla ordning på dina marknadsaktiviteter. Det kommer att öka dina möjligheter att vinna nya kunder och behålla befintliga kunder.  

## <a name="about-this-walkthrough"></a>Om den här genomgången

 I den här genomgången beskrivs processen för att följa upp en mässa och välja ut potentiella kunder (kontakter) i en uppföljningskampanj.  

 I genomgången beskrivs kampanj- och segmenthanteringsfunktionerna i avdelningen Försäljning och marknadsföring. I den här genomgången tas följande aktiviteter upp:  

- Förbereder data.
- Skapa en kampanj.  
- Välja ut målgrupp.  
- Utvinna data.  
- Skicka brev till kontakter.  
- Registrera kampanjsvar.  

## <a name="roles"></a>Roller

 Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

- Marknadsföringschef eller försäljningschef  
- Marknadsföringsassistent  

## <a name="prerequisites"></a>Förutsättningar

 Innan du kan utföra aktiviteterna i den här genomgången måste du installera [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="story"></a>Situation

 Marknadsföringschefen på försäljningsavdelningen hos CRONUS är ansvarig för planering och genomförande av kampanjer. Marknadsföringschefen fattar också beslut om vilka mässor som företaget ska delta i och utvärderar hur kampanjerna går.  

 Marknadsföringsassistenten på marknadsföringsavdelningen ansvarar för att ta fram, distribuera och placera ut marknadsföringsmaterial.  

 Företaget har precis lanserat en ny produkt som heter Rome Guest Chair. Produkten visades nyligen upp på en mässa, Office Futurus. Många kunder visade stort intresse för produkten och de kunder som köpte Rome Guest Chair under kampanjen erbjöds ett särskilt kampanjpris.  

 En av marknadsföringsassistentens uppgifter efter mässan är att registrera alla potentiella kunder som kontakter.  

 Marknadsföringschefen lägger upp en kampanj, skapar ett segment som innehåller alla nya kontakter och analyserar sedan kontaktuppgifterna för att välja ut målgruppen för kampanjen.  

 Assistenten hjälper till att skicka ut tackbrev till alla kontakter som lämnade sina visitkort i montern och chefen registrerar sedan alla svar som de får in från de potentiella kunderna.  

## <a name="setting-up-a-campaign"></a>Lägga upp en kampanj

 Som fort assistenten har registrerat de visitkort som togs emot under mässan lägger marknadsföringschefen upp ett kampanjkort för att hantera de aktiviteter som krävs för kampanjen.  

### <a name="to-set-up-a-campaign"></a>Så här lägger du upp en kampanj

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kampanjer** och väljer sedan relaterad länk.  
2. Välj åtgärden **nytt** för att skapa en ny kampanj. På kampanjkortet trycker du på <kbd>Retur</kbd> för att ett kampanjnummer automatiskt ska infogas.  
3. I fältet **Beskrivning** anger du en beskrivning av kampanjen, till exempel **Office Futurus-mässa**.  
4. Välj fältet **Statuskod** och välj statuskoden "1-PLAN". 
5. Fyll i fälten **Startdatum** och **Slutdatum** för kampanjen.  

## <a name="selecting-the-target-audience"></a>Välja målgrupp

 Marknadsföringschefen skapar ett segment för att välja kontakter som de kan arbeta med.  
 
 När du skapar ett segment kan du använda en mängd olika kriterier för att välja vilka kontakter som ska vara mål för segmentet. Du kan till exempel välja kontaktpersoner som arbetar på ett företag eller en potentiell kund som är ansvarig för inköp på ett företag. Du använder filter för att lägga till kontakter efter de villkor som bäst passar dina ändamål. Du kan till exempel välja att filtrera på ansvarsområde för kontaktpersonen eller affärsrelation eller bransch för kontaktföretaget. I den här genomgången väljer du filtret **Arbetsansvar** för att välja kontakter.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Så här skapar du ett segment med relevanta kontakter

1. Välj åtgärden **Navigera** och välj sedan **Segment**.  
2. Välj åtgärden **nytt** för att skapa ett nytt segment. På segmentkortet trycker du på **Retur** för att ett segmentnummer automatiskt ska infogas.  
3. På snabbfliken **Allmänt**, i fältet **Beskrivning**, anger du till exempel *Besökare på Office Futurus-mässan*.
4. Välj åtgärden **Lägg till kontakter** för att öppna filtret **Lägg till kontakter**.  
5. Rulla ned till snabbfliken **Kontakt arbetsansvar**, välj filtret **Inköp** som **Arbetsansvarskod** och tryck på knappen **OK**.  

Sidan **Segment** innehåller nu en lista med kontakter baserat på det filter som du har angett. På Snabbfliken **Allmänt**, i fältet **Antal rader**, kan du snabbt se antalet kontakter som uppfyller dessa villkor.  

> [!NOTE]  
> Du kan spara ditt segmentkriterium så att du kan använda det vid ett senare tillfälle.

### <a name="to-save-your-segmentation-criteria"></a>Så här sparar du kriterier för segmentering

1. På sidan **Segment** väljer du **Åtgärder**.
2. Välj **Funktioner**, sedan **Segment** och välj sedan åtgärden **Spara kriterier**.  
3. På sidan **Spara segmentkriterium** anger du en kod för segmentet. I fältet **Beskrivning** anger du en beskrivning av ditt segmentkriterium.
4. Välj **OK**.  

## <a name="mining-the-data"></a>Utvinna data

 Marknadsföringschefen tar en närmare titt på segmentlistan med kontakter och inser att den är alldeles för stor. Chefen bestämmer sig för att minska ned listan och i stället basera den på verkligt potentiella kunder för att se till att han fokuserar på rätt målgrupp. Den här processen att förfina och minska data kallas även för datautvinning.  

### <a name="to-remove-contacts-from-the-segment"></a>Så här tar du bort kontakter från segmentet

1. På sidan **Segment** väljer du **Åtgärder**.
2. I menyfältet väljer du **Funktioner**, **Kontakter** och **Minska kontakter**.  

  Detta öppnar dialogen **Ta bort kontakter – Minska**.  
4. På snabbfliken **Kontakt affärsrelation** väljer du filtret **CUST** i **Affärsrelationskod** och väljer sedan knappen **OK**.

 Sidan **Segment** innehåller nu en reducerad lista med kontakter och i fältet **Antal rader** kan du se det antal kontakter som uppfyller de nya kriterierna.  

 > [!NOTE]  
 > Om du behöver reversera borttagningen av en grupp kontakter kan du göra det med funktionen **Gå tillbaka**. Med andra ord kan du ångra din senast utförda segmentering.  

### <a name="to-bring-back-the-removed-contacts"></a>Så här återställer du de borttagna kontakterna

1. På sidan **Segment** väljer du åtgärden **Segment**.
2. Välj åtgärden **Gå tillbaka**.

Kontakter, som du precis tog bort, läggs tillbaka till listan med kontakter.

## <a name="linking-a-segment-to-a-campaign"></a>Länka ett segment till en kampanj

Marknadsföringschefen bestämmer sig för att den reducerade listan är den slutgiltiga listan med kontakter som de vill ska ingå i kampanjen. De länkar därför det här segmentet till kampanjen FUTURUS-mässan.  

### <a name="to-link-a-segment-to-the-campaign"></a>Så här länkar du ett segment till kampanjen

1. På sidan **Segment** klickar du på snabbfliken **Kampanje**  och väljer du fältet **Kampanjnr** för att välja den kampanj som du vill att segmentet ska kopplas till, exempelvis **CP0001**.
2. Välj **Ja**.  
3. Eftersom det här segmentet är målgruppen för kampanjen markerar du kryssrutan **Kampanjmål** och väljer **Ja**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Skicka brev och e-postmeddelande till kontakter

 Marknadsassistenten hjälper marknadsföringschefen med korrespondensen till de potentiella kunderna och tackar dem för att de besökte mässan.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Så här använder du ett segment så att skicka ett brev till en kontakt

> [!NOTE]  
> I den här proceduren måste du bifoga ett Word-dokument. Du kan lägga till bifogade filer på valfritt språk.

> [!NOTE]  
> Om det behövs klickar du på ikonen **Redigeringspenna** för att öppna sidan i redigeringsläge.

1. Öppna kortet **Segment** för **Besökare på FUTURUS-mässan**.  
2. Under snabbfliken **Interaktion**, i fältet **Interaktionsmallkod**, väljer du affärsbrevmallkoden **BUS** och sedan **Ja**.
3. Öppna sidan **Segmentinteraktion språk** genom att välja fältet **Språkkod (standard)**. Markera en **språkkod** och välj sedan knappen **OK**.
4. Kontrollera att **motsvarande typ (standard)** har angetts som **papperskopia**.
5. I fältet **Bilaga** väljer du rutan **Ellips**. Då öppnas dialogrutan Importera bilaga.
    1. Tryck på knappen **Välj** för att välja filen.
    1. Leta reda på filen och tryck på knappen **Öppna** för att bifoga den.
6. I fältet **Angående (standard)** skriver du följande exempeltext: **Tack för att du besökte mässan**. Tryck på <kbd>Tab</kbd>-tangenten för att lämna fältet och välj **Ja**-knappen..
7. Skjut reglaget **Skicka Word-dokument som bilaga** till På och tryck på knappen **Ja**.
8. Välj åtgärden **Logg**. I popup-fönstret Logga segment aktiverar du: **Skapa uppföljningssegment**
9. Klicka på **OK** om du vill starta **batchjobbet Loggsegment**.  

Bilagorna skickas. När processen är klar för väljer du knappen **OK** för meddelandet som anger att segmentet har loggats.  

 Breven skrivs ut automatiskt och segmentet loggas. Eftersom segmentet har loggats finns det inte längre i listan över segment utan flyttas till listan över loggade segment. För att se den listan, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Loggade segment** och väljer sedan relaterad länk.  

När segmentet har loggats registreras varje brev som skickas som en interaktion, som du kan visa i loggen.  

Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Interaktionslogg** och välj sedan relaterad länk. Det finns en transaktion för varje skickat brev.  

### <a name="to-send-an-email-message-to-a-contact"></a>Så här skickar du ett e-postmeddelande till en kontakt

1. På snabbfliken **Interaktion**, i fältet **Interaktionsmallkod**, väljer du affärsbrevmallen, kod **BUS**.  
2. I fältet **Angående (standard)** skriver du följande exempeltext: **Tack för att du besökte mässan**.  
3. Välj **E-post** i fältet **Korrespondenstyp**.  
4. Ange språkinställningar och bifoga Word-dokument som i föregående procedur.  
5. Välj åtgärden **Logg**. Sidan **Loggsegment** öppnas.  
6. Markera kryssrutan **Skicka bilagor** om du vill att bilagorna ska skickas med e-post.  
7. Markera kryssrutan **Skapa uppföljningssegment**.  
8. Välj knappen **OK**.  

 Breven skickas automatiskt med e-post och segmentet loggas. Eftersom segmentet har loggats finns det inte längre i listan över segment utan sparas i listan över loggade segment. För att se den listan, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Loggade segment** och väljer sedan relaterad länk.  

## <a name="registering-campaign-responses"></a>Registrera kampanjsvar

 Under de närmaste veckorna svarar de potentiella kunderna på brevet. Marknadsföringschefen vill hålla ordning på svaren och registrerar korrespondensen.  

 För att hålla ordning på svaren lägger du upp ett segment för de kontakter som har svarat på brevet.  

### <a name="to-register-campaign-responses"></a>Så här registrerar du kampanjsvar

1. På sidan **Segment**, under snabbfliken **Interaktion**, väljer du fältet **Interaktionsmallkod**.  

 Det finns ingen interaktionsmall för att registrera svar på kampanjer. Skapa därför en ny mall.  

2. På listrutan **Interaktionsmallar** väljer du åtgärden **Ny**.  
3. I fältet **Kod** anger du **SVAR** och i fältet **Beskrivning** anger du **Kampanjsvar**.  
4. Välj **OK**.
5. Välj **Ja** om du vill att koden för interaktionsmallen ska kopplas till alla segmentrader.
6. Under snabbfliken **Kampanj** väljer du fältet **Kampanjsvar**. Välj **Ja** för att bekräfta meddelandet *Du har ändrat kampanjsvaret*.  
7. På sidan **Segment** väljer du åtgärden **Logg**.  
8. På sidan **Logga segment** avmarkerar du kryssrutan **Skicka bilagor**. Tryck på **OK** för att bekräfta meddelandet om att segmentet har loggats.  
  
## <a name="see-also"></a>Se även
[Kundhantering](marketing-relationship-management.md)  
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

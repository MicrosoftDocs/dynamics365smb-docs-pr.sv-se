---
title: "Genomgång: Genomföra en försäljningskampanj | Microsoft Docs"
description: "En kampanj är alla typer av aktiviteter som inkluderar flera kontakter. En viktig del när man planerar en kampanj är att välja målgrupp för kampanjen. Av den anledningen skapar du ett segment, eller en grupp med kontakter, med hjälp av filter i Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 492976f9ab0553b67b73317040878c825eaa1808
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Genomgång: Genomföra en försäljningskampanj
En kampanj är alla typer av aktiviteter som inkluderar flera kontakter. En viktig del när man planerar en kampanj är att välja målgrupp för kampanjen. Av den anledningen skapar du ett segment, eller en grupp med kontakter, med hjälp av filter i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Du använder dessa funktioner i Försäljning och marknadsföring för att noggrant planera dina marknadsaktiviteter och hantera dina aktiviteter med kontakter och kunder. Du kan skapa kampanjer och lägga upp segment för utskick och andra typer av aktiviteter med dina kontakter och eventuella kunder.  

 Med kampanj- och segmentfunktionerna och tillhörande automatiserade processer kan du planera, organisera och hålla ordning på dina marknadsaktiviteter. Det kommer att öka dina möjligheter att vinna nya kunder och behålla befintliga kunder.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
 I den här genomgången beskrivs processen för att följa upp en mässa och välja ut potentiella kunder (kontakter) i en uppföljningskampanj.  

 I genomgången beskrivs kampanj- och segmenthanteringsfunktionerna i avdelningen Försäljning och marknadsföring. I den här genomgången tas följande aktiviteter upp:  

-   Skapa en kampanj.  
-   Välja ut målgrupp.  
-   Utvinna data.  
-   Skicka brev till kontakter.  
-   Registrera kampanjsvar.  

## <a name="roles"></a>Roller  
 Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroller:  

-   Marknadsföringschef eller försäljningschef  
-   Marknadsföringsassistent  

## <a name="prerequisites"></a>Förutsättningar  
 Innan du kan utföra aktiviteterna i den här genomgången måste du installera [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="story"></a>Situation  
 Marknadsföringschefen på försäljningsavdelningen hos CRONUS är ansvarig för planering och genomförande av kampanjer. Han fattar också beslut om vilka mässor som företaget ska delta i och utvärderar hur kampanjerna går.  

 Marknadsföringsassistenten på marknadsföringsavdelningen ansvarar för att ta fram, distribuera och placera ut marknadsföringsmaterial.  

 Företaget har precis lanserat en ny produkt som heter Millennium Server. Produkten visades nyligen upp på en mässa, Computer Futurus. Många kunder visade stort intresse för produkten och de kunder som köpte Millennium Server under kampanjen erbjöds ett särskilt kampanjpris.  

 En av marknadsföringsassistentens uppgifter efter mässan är att registrera alla potentiella kunder som kontakter.  

 Marknadsföringschefen lägger upp en kampanj, skapar ett segment som innehåller alla nya kontakter och analyserar sedan kontaktuppgifterna för att välja ut målgruppen för kampanjen.  

 Assistenten hjälper till att skicka ut tackbrev till alla kontakter som lämnade sina visitkort i montern och chefen registrerar sedan alla svar som de får in från de potentiella kunderna.  

## <a name="setting-up-a-campaign"></a>Lägga upp en kampanj  
 Som fort assistenten har registrerat de visitkort som togs emot under mässan lägger marknadsföringschefen upp ett kampanjkort för att hantera de aktiviteter som krävs för kampanjen.  

### <a name="to-set-up-a-campaign"></a>Så här lägger du upp en kampanj  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport") , ange **Kampanjer**, och välj sedan relaterad länk.  
2.  Välj åtgärden **nytt** för att skapa en ny kampanj. På kampanjkortet trycker du på retur för att ett kampanjnummer automatiskt ska infogas.  
3.  I fältet **Beskrivning** anger du en beskrivning av kampanjen, till exempel **FUTURUS-mässa**.  
4.  Välj fältet **Statuskod** och en statuskod från listan som öppnas i fönstret **Kampanjstatus**.  
5.  Fyll i fälten **Startdatum** och **Slutdatum** för kampanjen.  

## <a name="selecting-the-target-audience"></a>Välja målgrupp  
 Marknadsföringschefen skapar ett segment för att välja kontakter som han kan arbeta med.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Så här skapar du ett segment med relevanta kontakter  

1.  Välj åtgärden **Segment**.  
2.  Välj åtgärden **nytt** för att skapa ett nytt segment. På segmentkortet trycker du på retur för att ett segmentnummer automatiskt ska infogas.  
3.  På snabbfliken **Allmänt**, i fältet **beskrivning**, anger du till exempel **Besökare på FUTURUS-mässan**.  

     När du har angett allmän information om segmentet väljer du de kontakter som ska ingå i segmentet.  

     Du kan använda en mängd olika kriterier för att välja kontakter. Det kan exempelvis vara kontaktpersoner som arbetar på ett företag eller en potentiell kund som är ansvarig för inköp på ett företag.  

     Du använder filter för att lägga till kontakter efter de kriterier som bäst passar dina ändamål. Du kan till exempel välja att filtrera på ansvarsområde för kontaktpersonen eller affärsrelation eller bransch för kontaktföretaget. I den här genomgången väljer du filtret **Arbetsansvar** för att välja kontakter.  

4.  I fönstret **Segment** väljer du åtgärden **Lägg till kontakter** för att öppna filtret **Lägg till kontakter**.  
5.  På snabbfliken **Arbetsansvar** väljer du filtret **Inköp** i **Arbetsansvarskod** och knappen **OK**.  

     Fönstret **Segment** innehåller nu en lista med kontakter baserat på det filter som du har angett. På Snabbfliken **Allmänt**, i fältet **Antal rader**, kan du snabbt se antalet kontakter som uppfyller dessa kriterier.  

    > [!NOTE]  
    >  Du kan spara ditt segmentkriterium så att du kan använda det vid ett senare tillfälle.

    1.  I fönstret **Segment** väljer du åtgärden **Segment** och väljer sedan åtgärden **Spara kriteriet**.  
    2.  I fönstret **Spara segmentkriterium** anger du en kod för segmentet. I fältet **Beskrivning** anger du en beskrivning av ditt segmentkriterium.
    3.  Välj **OK**.  

## <a name="mining-the-data"></a>Utvinna data  
 Marknadsföringschefen tar en närmare titt på segmentlistan med kontakter och inser att den är alldeles för stor. Han bestämmer sig för att minska ned listan och i stället basera den på verkligt potentiella kunder för att se till att han fokuserar på rätt målgrupp. Den här processen att förfina och minska data kallas även för datautvinning.  

### <a name="to-remove-contacts-from-the-segment"></a>Så här tar du bort kontakter från segmentet  

1.  I fönstret **Segment** väljer du åtgärden **Kontakter** och väljer sedan åtgärden **Reducera kontakter**  för att öppna fönstret **Ta bort kontakter - minska**.  
2.  På snabbfliken **Affärsrelation** väljer du filtret **PROS** i **Affärsrelationskod** och väljer sedan knappen **OK**.  

     Fönstret **Segment** innehåller nu en reducerad lista med kontakter och i fältet **Antal rader** kan du se det antal kontakter som uppfyller de nya kriterierna.  

    > [!NOTE]  
    >  Om du behöver reversera borttagningen av en grupp kontakter kan du göra det med funktionen **Gå tillbaka**. Med andra ord kan du ångra din senast utförda segmentering.  
    >   
    >  I fönstret **Segment** väljer du åtgärden **Segment** och väljer sedan åtgärden **Föregående**.  
    >   
    >  Kontakter, som du precis tog bort, läggs tillbaka till listan med kontakter.  

## <a name="linking-a-segment-to-a-campaign"></a>Länka ett segment till en kampanj  
 Marknadsföringschefen bestämmer sig för att den reducerade listan är den slutgiltiga listan med kontakter som han vill ska ingå i kampanjen. Han länkar därför det här segmentet till kampanjen FUTURUS-mässan.  

### <a name="to-link-a-segment-to-the-campaign"></a>Så här länkar du ett segment till kampanjen  

1.  I fönstret **Segment** klickar du på snabbfliken **Kampanje**  och väljer du fältet **Kampanjnr** för att välja den kampanj som du vill att segmentet ska kopplas till, exempelvis **CP0001**.  
2.  Eftersom det här segmentet är målgruppen för kampanjen markerar du kryssrutan **Kampanjmål**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Skicka brev och e-postmeddelande till kontakter  
 Marknadsassistenten hjälper marknadsföringschefen med korrespondensen till de potentiella kunderna och tackar dem för att de besökte mässan.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Så här använder du ett segment så att skicka ett brev till en kontakt  

1.  Öppna kortet **Segment** för **Besökare på FUTURUS-mässan**.  
2.  På snabbfliken **Interaktion**, i fältet **Interaktionsmallkod**, väljer du affärsbrevmallen, kod **BUS**.  
3.  I fältet **Angående (standard)** skriver du följande exempeltext: **Tack för att du besökte mässan**.  

    > [!NOTE]  
    >  Den här mallen består av flera bifogade dokument som är skrivna på olika språk. Exempelspråk är standardspråket engelska och danska.  

4.  Öppna fönstret **Segmentinteraktion språk** genom att välja fältet **Språkkod (standard)**. Markera en språkkod och välj sedan knappen **OK**.  
5.  Du kan visa dokumentet på det valda språket. Välj åtgärden **Bilaga** och välj sedan åtgärden **Öppna**.  

     Välj alternativet **Tillåt för denna klientsession** om du vill svara på meddelandet som begär tillstånd att starta Word.  

     Då öppnas det bifogade word-dokument, så att du kan granska det. Här har du också möjlighet att redigera och ändra brevet. Stäng Word-dokumentet när du är klar.  

6.  Ange ärendet för brevet i fältet **Ämne** på det språk som valts för mallen.  
7.  Välj åtgärden **Logg**.
8.  Markera kryssrutan **Skicka bilagor** om du vill att bilagorna ska skrivas ut.  

    1. Markera kryssrutan **Skapa uppföljningssegment**.  
    2. Klicka på **OK** om du vill starta batchjobbet **Loggsegment**.  

9. Bilagorna skickas. När processen är klar för väljer du knappen **OK** för meddelandet som anger att segmentet har loggats.  

     Breven skrivs ut automatiskt och segmentet loggas. Eftersom segmentet har loggats finns det inte längre i listan över segment utan flyttas till listan över loggade segment. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Loggade segment** och välj sedan relaterad länk för att se den listan.  

10. När segmentet har loggats registreras varje brev som skickas som en interaktion, som du kan visa i loggen.  

     Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Interaktionslogg** och välj sedan relaterad länk. Det finns en transaktion för varje skickat brev.  

### <a name="to-send-an-email-message-to-a-contact"></a>Så här skickar du ett e-postmeddelande till en kontakt  

1.  På snabbfliken **Interaktion**, i fältet **Interaktionsmallkod**, väljer du affärsbrevmallen, kod **BUS**.  
2.  I fältet **Angående (standard)** skriver du följande exempeltext: **Tack för att du besökte mässan**.  
3.  Välj **E-post** i fältet **Korrespondenstyp**.  
4.  Ange språkinställningar, som i föregående steg.  
5.  Välj åtgärden **Logg**. Fönstret **Loggsegment** öppnas.  
6.  Markera kryssrutan **Skicka bilagor** om du vill att bilagorna ska skickas med e-post.  
7.  Markera kryssrutan **Skapa uppföljningssegment**.  
8.  Välj knappen **OK**.  

     Breven skickas automatiskt med e-post och segmentet loggas. Eftersom segmentet har loggats finns det inte längre i listan över segment utan sparas i listan över loggade segment. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Loggade segment** och välj sedan relaterad länk för att se den listan.  

## <a name="registering-campaign-responses"></a>Registrera kampanjsvar  
 Under de närmaste veckorna svarar de potentiella kunderna på brevet. Marknadsföringschefen vill hålla ordning på svaren och registrerar korrespondensen.  

 För att hålla ordning på svaren lägger du upp ett segment för de kontakter som har svarat på brevet.  

### <a name="to-register-campaign-responses"></a>Så här registrerar du kampanjsvar  

1.  I fönstret **Segment** expanderar du snabbfliken **Interaktion**.  
2.  Välj fältet **Interaktionsmallkod**.  

     Det finns ingen interaktionsmall för att registrera svar på kampanjer. Skapa därför en ny mall.  

3.  I fönstret **Interaktionsmallar** väljer du åtgärden **Ny**.  
4.  I fältet **Kod** anger du **SVAR** och i fältet **Beskrivning** anger du **Kampanjsvar**.  
5.  Välj **OK**.  
6.  Välj den här interaktionsmallen i fältet **Interaktionsmallkod** och bekräfta meddelandet där du blir tillfrågad om du vill uppdatera segmentraderna med samma interaktionskod.  

     Ange nu att dessa kontakter har svarat på kampanjen:  
7.  I fältet **Kampanj** på snabbfliken **Kampanjnr** väljer du din kampanj.  
8.  Lämnar fältet **Kampanjnr** och bekräfta meddelandet där du blir tillfrågad om du vill uppdatera segmentraderna med samma interaktionsmallkod.  
9. Välj fältet **Kampanjsvar** och bekräfta det meddelande som följer.  

     Logga segmentet för att se till att korrespondensen registreras.  
10. I fönstret **Segment** väljer du åtgärden **Logg**.  
11. I fönstret **Loggsegment** avmarkerar du kryssrutan **Skicka bilagor** och klickar sedan på **OK** och bekräftar det meddelande som visas.  

     När segmentet är loggat skapas automatiskt en transaktion för kampanjen för att registrera åtgärden i fönstret **Kampanjtransaktioner**.  

## <a name="see-also"></a>Se även  
[Kundhantering](marketing-relationship-management.md)  
 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


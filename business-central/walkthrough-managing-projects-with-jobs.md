---
title: Genomgång – Hantera projekt med Projekt
description: I den här genomgången får du en introduktion till projekthanteringsfunktionerna i projekt som gör det möjligt att schemalägga användningen av ditt företagsresurser med mera.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-managing-projects-with-jobs" />Genomgång: Hantera projekt med Projekt

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Den här genomgången introducerar dig för projekthanteringsfunktionerna i projektet. Med Projekt kan du schemalägga förbrukningen av ditt företags resurser och hålla reda på de olika kostnader som är förknippade med resurser i ett visst projekt. I projekt ingår förbrukningen av anställdas arbetstimmar, maskintimmar, lagerartiklar samt andra typer av förbrukning som du behöver hålla koll på i takt med att arbetet fortskrider.  

 I den här genomgången beskrivs hur du lägger upp ett nytt projekt samt några av de vanligaste aktiviteterna, som att hantera fast prissättning, delbetalningar, bokföra fakturor från projekt och kopiera projekt.  

## <a name="about-this-walkthrough" />Om den här genomgången

 I den här genomgången tas följande aktiviteter upp:  

### <a name="setting-up-a-job" />Lägga upp ett projekt

 Med fältet budgetstrukturinställningar för projekt kan du skapa projekt på ett okomplicerat sätt. Den här genomgången beskriver följande procedurer:  

- Lägga upp aktivitetsrader och planeringsrader.  
- Skapa projektspecifika priser för artiklar, resurser och redovisningskonton.  
- Fakturering från ett projekt.  

### <a name="handling-fixed-prices" />Hantera fasta priser

 I Projekt kan du hantera fasta priser och priser för tjänster och produkter som överenskommits i förväg med kunderna. I denna genomgång kan du göra följande:  

- Se hur kontrakts- och fakturavärden fastställs.  
- Lämna utrymme för extra (ej fakturerat) arbete i planeringen.  

### <a name="copying-a-job" />Kopiera ett projekt

 I det här scenariot fokuserar vi på hur du kopierar en del eller hela projektet för att minska den manuella dataregistreringen och öka noggrannheten. Detta omfattar följande:  

- Kopiera en del av ett projekt till ett nytt projekt.  
- Kopiera projektspecifika priser.  
- Kopiera planeringsrader.  

### <a name="making-payment-by-installment" />Göra delbetalningar

 När ett stort och kostsamt projekt sträcker sig över en längre period kommer oftast kunden överens med företaget om att dela upp betalningen. I det här scenariot visas hur du konfigurerar delbetalningar och det omfattar:  

- Hur du skapar delbetalningar för ett projekt.  
- Fakturera kunder för utbetalningar.  
- Bokföra förbrukning i ett delbetalningsprojekt.  

## <a name="roles" />Roller

 Den här genomgången innehåller aktiviteter för följande roller:  

- Projektchef  
- Projektmedlemmen  

## <a name="prerequisites" />Förutsättningar

 Innan du kan utföra aktiviteterna i den här genomgången måste du göra följande  

- Installera demonstrationsdatabasen CRONUS.
- Skapa exempeldata med hjälp av stegen i följande avsnitt.  

## <a name="story" />Situation

Det här scenariot handlar om CRONUS, ett design- och konsultföretag som ritar och bygger till exempel konferenshallar och kontor, med möbler, utrustning och lagerutrymmen. Deras arbete är för det mesta projektorienterat. Prakash, en projektledare på CRONUS använder projekt för att få en överblick över alla pågående projekt som CRONUS har startat, sig samt de projekt som har avslutats. Prakash brukar avtala med kunderna om vad som ska göras och registrerar grunderna för projektet, dvs. aktivitets- och planeringsrader samt priser, i [!INCLUDE[prod_short](includes/prod_short.md)]. Prakash upptäcker att det är okomplicerat att skapa, underhålla och granska informationen. Prakash tycker också om hur [!INCLUDE[prod_short](includes/prod_short.md)] aktiverar kopiering av projektet och delbetalningar.

 Tricia, en projektmedlem som rapporterar till Prakash, är ansvarig för övervakning av det dagliga arbetet. Tricia registrerar sitt eget arbete samt det arbete som utförs av teknikerna i varje aktivitet, registrerar de artiklar som de har använt och de kostnader som har uppstått.  

## <a name="preparing-sample-data" />Förbereda exempeldata

 För att förbereda för genomgången måste du lägga till Tricia som en ny resurs.  

### <a name="to-prepare-the-sample-data" />Så här förbereder du exempeldata

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Resurser** och väljer sedan relaterad länk.  
2.  Välj **Ny** för att skapa ett nytt resurskort.  
3.  Ange följande information i fälten på snabbfliken **Allmänt**:  

    - **Nr**: **Tricia**  
    - **Namn**: **Tricia**  
    - **Typ**: **Person**  

4.  I fältet **Basenhet** klickar du på **Ny** för att öppna sidan **Resursenhet**. I fältet **Kod** väljer du **Timme**.  
5.  På snabbfliken **Fakturering** anger du följande information:  

    - **Inköpspris**: **5**  
    - **Indirekt kostnad %**: **4**  
    - **Styckkostnad**: **10**  
    - **Produktbokföringsmall**: **Tjänster**  
    - **Moms produktbokföringsmall**: **Moms 25**  

6. Stäng sidan.

I nästa procedur skapar du en projektjournal för Tricia för att bokföra deras förbrukning.  

### <a name="to-create-a-job-journal-batch" />Skapa en ny journal

1.  Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2.  På sidan **Journalnamn** i fönstret **Projektjournal**. Sidan **Projektjournaler** öppnas.  
3.  Välj åtgärden **Ny** för att skapa en rad med följande information:  

    - **Namn**: **Tricia**  
    - **Beskrivning**: **Tricia**  
    - **Nr-serie**: **JJNL-GEN**  

4.  Välj **OK** för att spara ändringar.

## <a name="setting-up-a-job" />Lägga upp ett projekt

 I det här scenariet har CRONUS tecknat ett avtal med en kund, Progressive Home Furnishings, för att inreda ett konferensrum och en matsal. Kunden finns i USA och programmet kommer att kräva särskild programvara. projektledaren går igenom upplägget med kunden och skapar ett projekt utifrån det.  

### <a name="to-set-up-a-job" />Så här lägger du upp ett projekt:

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2.  Välj **Ny** för att skapa ett nytt kort.  
3.  Ange följande information i fälten på snabbfliken **Allmänt**:  

    - **Beskrivning**: **Rekommendationer för konferenslokal**  
    - **Faktureringskundnr**: **01445544**  

4.  På snabbfliken **Bokföring** anger du följande information:  

    - **Status**: **Planering**  
    - **Projektbokföringsmall**: **Inreda**  
    - **PIA-metod**: **Kostnadsvärde**  

5.  På snabbfliken **Varaktighet** anger du dagens datum i fälten **Startdatum** och **Slutdatum**. Dessa datum underlättar när du ska konvertera valutor när projektet ska faktureras.  
6.  På snabbfliken **Utlandshandel** anger du valutakoden **USD**. Om du väljer USD i fältet **Fakturavalutakod** kommer projektet att faktureras i USD och planeras endast i den lokala valuta för CRONUS.  

 Du kan anpassa serviceprissättningen för kunder på projektbasis, beroende på vilka avtal som du har skapat. I nästa procedur anger projektchefen en kostnad för Tricias tid, priset för den obligatoriska programvaran och resekostnader som kunden har avtalat att betala.  

### <a name="to-customize-pricing" />Anpassa prissättning

1.  Från projektkortet kan du välja åtgärden **resurs**.  
2.  På sidan **Resurspriser för projekt** anger du följande information:  

    - **Kod**: **Tricia**  
    - **A-pris**: **20**  

3.  Stäng sidan.  
4.  Välj åtgärden **Artikel**.  
5.  På sidan **Artikelpriser för projekt** anger du följande information och anpassat pris:  

    1.  **Artikelnr**: **80201 (grafikprogram)**  
    2.  **A-pris**: **200**  

6.  Stäng sidan.  
7.  Välj åtgärden **Redovisningskonto**.  
8.  Ange följande information, och resekostnader, som kunden har avtalat att betala för kostnader, plus 25 procent, på sidan **Redov.kontopriser**:  

    1.  **Redovisningskonto**: **8430 (resa)**  
    2.  **Styckkostnadsfaktor**: **1,25**  

9. Stäng sidan.  

 Det slutliga steget i konfigurera ett projekt är att lägga till projektaktiviteterna och planeringsrader som ingår i varje aktivitet. Planeringsraderna styr vad kunden faktureras för.  

### <a name="to-add-job-tasks" />Lägga till projektaktiviteter

1.  På kortet **preojekt** för det nya projektet, väljer du åtgärden **Projektaktivitetsrader**.  
2.  I följande tabell beskrivs den information som du ska ange i fälten.  

    |Projektaktivitetsnr|Description|Typ av projektaktivitet|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Rådgivning om inredning av konferenslokal|Från-summa|  
    |1010|Rådgivningsmöte med kunden|Bokföring|  
    |1020|Utveckling|Bokföring|  
    |1090|Rådgivning, summa|Till-summa|  

3.  Om du vill visa att vissa aktiviteter är underkategorier till andra aktiviteter väljer du åtgärden **Indrag för projektaktiviteter**.  

 En planeringsrad kan vara en av följande typer:  

- **Budget**: Läggs till i schemat, men faktureras inte.  
- **Fakturerbart**: Faktureras men läggs inte till i schemat.  
- **Både budget och fakturerbart**: Faktureras och läggs till i schemat.  

 I den här genomgången använder projektchefen **Både budget och fakturerbart**. De skapar tre planeringsrader för aktivitet 1010 och två planeringsrader för aktivitet 1020.  

### <a name="to-create-planning-lines" />Skapa planeringsrader

1. Välj rad 1010 och välj sedan åtgärden **Projektplaneringsrader**.  

2. Skapa planeringsrader med följande information:  

    | Rad | Radtyp | Planeringsdatum  | Typ        | Nr   | Antal | Styckpris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både Budget och Fakturerbart | (dagens datum) | Resurs | Tricia | 40        |     |
    | 2    | Både Budget och Fakturerbart | (dagens datum) | Resurs | Timothy | 40        |     |
    | 3    | Både Budget och Fakturerbart | (dagens datum) | Redovisningskonto | 8430 (resa) | 2 | 400    |

     Stäng sidan. Summorna uppdateras på sidan **Projektaktivitetsrader**.  
3. Välj rad 1020 och välj sedan åtgärden **Projektplaneringsrader**. Ange följande information:  

    | Rad | Radtyp | Planeringsdatum  | Typ        | Nr   | Antal | Styckpris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både Budget och Fakturerbart | (dagens datum) | Resurs | Tricia | 80        |     |
    | 2    | Både Budget och Fakturerbart | (dagens datum) | Artikel | 80201 (grafikprogram) | 1 |     |

4. Stäng sidan. Summorna uppdateras på sidan **Projektaktivitetsrader**.  

## <a name="calculating-remaining-usage" />Beräkna återstående förbrukning

 Tricia, teamprojektmedlem, har arbetat med projektet ett tag och vill registrera sina timmar och sin förbrukning för projektet. Tricia har inte arbetat mer timmar än vad som överenskommits med kunden. Tricia använder batch-jobbet **Ber. återstående förbrukning** för att beräkna återstående förbrukning för projekter i en projektjournal. För varje projektaktivitet beräknas skillnaden mellan planerad förbrukning av artiklar, resurser, redovisningskostnader och verklig förbrukning i projekttransaktioner. Den återstående förbrukningen visas sedan i den projektjournal som hon kan bokföra den ifrån.  

### <a name="to-calculate-remaining-usage" />Så här beräknar du återstående förbrukning

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2.  På sidan **Projektjournal**, i fältet **Journalnamn**, öppnar du listan **Projektjournaler**. Välj projektjournalen **Tricia**.  
3.  Välj åtgärden **Ber. återstående förbrukning**.  
4.  Välj fältet **Projektnr** och välj relevant projektnummer, vanligtvis projekt J00010, på sidan **Projekt – Beräkna återstående förbrukning** på snabbfliken **Projektaktivitet**.  
5.  På snabbfliken **Alternativ** skriver du **J00001** i fältet **Dokumentnr**. Det gör det enklare att senare söka efter bokföringen.  
6.  Ange dagens datum som bokföringsdatum.  
7.  Välj **OK**. Alla rader som föreslagits utifrån de planeringsrader som Prakash skapade för projektjournalen genereras.  
8.  Välj **OK** på bekräftelsesidan. De genererade raderna läggs till i projektjournalen.  
9. Se till att alla dokument har numret J00001. Välj sedan åtgärden **Bokföra**. Klicka på knappen **Ja** för att bokföra.  

Raderna är nu bokförda.  

## <a name="creating-and-posting-a-job-sales-invoice" />Skapa och bokföra en försäljningsfaktura för ett projekt

 I nästa steg kan Tricia skapa en ny faktura för hela projektet eller för en del av ett projekt. Tricia kan även bifoga fakturan till en annan faktura för samma kund inom samma projekt. I detta fall kan Tricia fakturera hela projektet eftersom projektet nu är slutfört.  

### <a name="to-create-a-job-sales-invoice" />Så här skapar du en projektförsäljningsfaktura

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2.  Välj det projekt som du skapade tidigare och klicka på åtgärd **Skapa försäljningsfaktura för projekt**.  
3.  På snabbfliken **Projektaktivitet** rensar du alla filter för **Projektaktivitetsnr** för att kunna fakturera projektet. I fältet **Nr** väljer du önskat projekt.  
4.  På snabbfliken **Alternativ** fyller du i bokföringsdatumet och anger om du vill skapa en faktura per aktivitet eller en enda faktura för samtliga aktiviteter.  
5.  Välj **OK** för att skapa fakturan och välj sedan **OK** på bekräftelsesidan.  

 När Tricia har skapat fakturan kan hon nå den från rollcentret **Försäljningsorderhandläggare** till exempel. 

### <a name="to-post-a-new-sales-invoice" />Så här bokför du en ny försäljningsfaktura

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.  
2.  Öppna fakturan för kund nr. 01445544. Du kan se den information som registrerades från planeringsraderna.  
3.  Välj åtgärden **Bokföra**. Klicka på knappen **Ja** för att bokföra.  

### <a name="to-view-the-posted-invoice" />Så här visar du den bokförda fakturan

1.  Öppna relevant projekt och välj sedan åtgärden **Projektplaneringsrader**.  
2.  Markera en av planeringsraderna som har fakturerats och klicka på **Försäljningsfakturor/kreditnotor**.
3. På sidan **Projektfakturor** väljer du åtgärden **Öppna försäljningsfaktura/-kreditnota**.  

 Tricia vill visa information om priser, kostnader och vinster som avser det här projektet och det gör hon på sidan **Statistik**.  

### <a name="to-open-the-statistics-page" />Så här öppnar du sidan Statistik

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Statistik**. Du kan granska detaljerad information om projektets priser, kostnader och vinster i både lokala och utländska valutor.  
3.  Välj **Stäng** för att stänga sidan **Projektstatistik**.  

## <a name="handling-fixed-prices" />Hantera fasta priser

 CRONUS har fått uppdraget att inreda tio konferensrum. Som projektchef vill Prakash ha en god översikt över de aktiviteter som ska utföras i projektet samt tillhörande budget och kostnader för respektive aktivitet. Prakash vill dessutom veta det totala pris som överenskommits för projektet och det belopp som har fakturerats hittills. De har nått en överenskommelse med kunden om att projektet ska ha ett fast pris.  

### <a name="to-manage-fixed-pricing-in-jobs" />Så här hanterar du fast prissättning i projekt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Markera projektnummer **Nyström** och välj sedan åtgärd **Projektaktivitetsrader**.  
3. Markera rad 1120 och i fältet **Budget (totalkostnad)** högerklickar du på beloppet och väljer **Specificera**.  

     Genom att granska Projektplaneringslista inser Prakash att Tricia behövs i 30 timmar under den här projektfasen. Prakash kommer överens med kunden om ett fast pris.  

4. På sidan **Projektaktivitetsrader** väljer du rad 1120 och väljer sedan åtgärden **Projektplaneringsrader**. Skapa en planeringsrad med följande information:  

    | Rad | Radtyp | Typ        | Nr   | Antal |
    |------|-----------|-------------|-------|----------|
    | 1    | Både Budget och Fakturerbart  | Resurs | Tricia | 30 |

     Stäng sidan.  
5. I fältet **Budget (totalkostnad)**, högerklicka i fältet och välj **Specificering** igen på sidan **Projektaktivitetsrader**. Visa de ändringar som gjorts i schemat. Du ser att 30 timmar har lagts till i schemat.  
6. Stäng sidorna.  

När Tricia har lagts till i schemat för den här aktivitetsraden arbetar hon 25 timmar på projektet och registrerar dessa timmar i projektjournalen.  

### <a name="to-enter-hours-in-the-job-journal" />Så här registrerar du timmar i projektjournalen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Jobbjournaler** och väljer sedan relaterad länk.  
2. På den nya raden anger du följande information:  

    - **Typ av rad**: **(tom)**  
    - **Bokföringsdatum**: **(dagens datum)**  
    - **Verifikationsnr**: **J00002**  
    - **Projektnr**: **Nyström**  
    - **Projektaktivitetsnr**: **1120**  
    - **Typ**: **Resurs**  
    - **Nr**: **Tricia**  
    - **Antal**: **25**  

3. Välj åtgärden **Bokföra**.  

     Några dagar senare arbetar Tricia för ytterligare tio timmar på projektet och har nu arbetat 35 timmar. Eftersom avtalet gäller för 30 timmar med kunden debiteras kunden endast 5 av dessa timmar. Tricia ska manuellt lägga till dessa extra fem timmar som hon arbetade i schemat.  

4. På sidan **Projektjournal** väljer du åtgärden **Ber. återstående förbrukning**.  
5. På sidan **Projekt – Beräkna återstående förbrukning** anger du följande information på snabbfliken **Alternativ**:  

    - **Verifikationsnr**: **J00003**  
    - **Bokföringsdatum**: **(dagens datum)**  

6. Ange följande på snabbfliken **Projektaktivitet**:  

    - **Projektnr**: **Nyström**  
    - **Projektaktivitetsnr**: **1120**  

7. Klicka på **OK** för att köra beräkningen.

    Det finns fem arbetstidar som återstår för Tricia. Fältet **Radtyp** är tomt, vilket innebär att endast förbrukningen återstår att bokföras eftersom arbetet redan är planerat.  

8. I **Projektjournaler** skapar du en ny rad med följande information. Se till att båda projektnummer är i ordningen efter dem som du redan har använt:  

    - **Typ av rad**: **budget**  
    - **Projektnr**: **Nyström**  
    - **Projektaktivitetsnr**: **1120**  
    - **Typ**: **Resurs**  
    - **Nr**: **Tricia**  
    - **Antal**: **5**  

     Via **Budget** uppdateras de planerade kostnaderna och priset utan att uppdatera de kontraktskostnader och priser som faktureras kunden.  

9. Välj åtgärden **Bokföra**. Välj **OK** för att stänga sidan.  
10. Öppna listan **Projekt**.  
11. Välj jobbet GUILDFORD och sedan i avsnittet **Projektaktivitetsrader**, välj raden 1120 och i fältet **Budget (total kostnad)** högerklicka på beloppet. Välj **Specificera** för att visa informationen.  

     Ändringar registreras automatiskt på raden för Projektaktivitetsnr. 1120 I totalkostnaden för det planerade arbetet är fem ytterligare arbetstimmarna som Tricia lagts till i schemat.  

12. Välj **Stäng** för att stänga sidan.  
13. Högerklicka på beloppet i fältet **Kontrakt (totalkostnad)** och välj **Specificera** för att visa informationen.  

I kontraktets totalpris finns endast de ursprungligen kontrakterade 30 timmarna med, eftersom det är det som har överenskommits med kunden.  

## <a name="copying-jobs" />Kopiera projekt

Prakash har slutit ett avtal med en kund, Selagorian Ltd, om att inreda tio konferensrum. Avtalet påminner om ett tidigare projekt. Därför kan det spara tid att kopiera det tidigare projektet.  

Markera de projekt- och aktivitetsrader som du vill kopiera på sidan **Kopiera projekt**. Du kan också välja att kopiera de ursprungliga projekttransaktionerna, som skapar planeringsrader baserat på faktisk förbrukning, eller så kan du kopiera de ursprungliga projektplaneringsraderna som kopierar de ursprungliga planeringsraderna till det nya projektet. Du kan då välja vilken planeringsrad- eller reskontratransaktionsradtyp som du vill inkludera, och endast välja det som är relevant för det nya projektet. Slutligen kan du välja det projekt som du vill kopiera till, och ange om priser och antal också ska kopieras.  

### <a name="to-copy-a-job" />Så här kopierar du ett projekt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj **Ny** för att skapa ett nytt projekt. Ange följande information:  

    - **Beskrivning**: **Inreda tio konferensrum**  
    - **Faktureringskundnr**: **20000**  

3. Välj fältet **Kopiera projektaktiviteter från**  
4. Ange följande på sidan **Kopiera projektaktiviteter**:  

    - **Projektnr**: **Nyström**  
    - **Projektaktivitetsnr från**: **1000**  
    - **Källa**: **Projektplaneringsrader**  
    - **Inkl. planeringsradtyp**: **Budget + fakturerbar**  
    - **Till projektnr**: **Guildford Inreda tio konferensrum**  
    - Markera fälten **Kopiera dimensioner** och **Kopiera antal**.  

5. Välj **OK** för att kopiera projektet och välj sedan åtgärden **OK** för att stänga bekräftelsesidan.  

Genom att jämföra priser, projektaktivitetsrader och projektplaneringsrader för de två projekten kan du se att informationen kopieras korrekt.  

## <a name="making-payments-by-installments" />Göra delbetalningar

CRONUS har precis fått ett stort projekt som kommer att pågå under ett år. Eftersom det krävs en hel del resurser gör projektledaren upp kontraktet så att kunden ska betala en del av projektet i förväg, en del när projektet är till hälften slutfört och resten när projektet är helt slutfört.  

### <a name="to-set-up-a-new-account" />Så här lägger du upp ett nytt konto

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. På sidan **Kontoplan** på fliken **Ny** för att skapa ett nytt kort.  
3. På det nya **redovisningskontokortet** anger du följande information:  

    - **Nr**: **40255**  
    - **Namn**: **Projektbetalning**  

4. På snabbfliken **Bokföring**, i fältet **Produktbokföringsmall** väljer du **Tjänster**. Stäng sidan.  
5. På sidan **Kontoplan** väljer du **Nr 40255, projektbetalning**, och välj **Indrag av kontoplan**. Välj **Ja** för att bekräfta.  

Procedurerna visar hur du skapar ett nytt projekt, anger prissättning och ställer in möjlighet till delbetalningar. På projektaktivitetsraderna kan du skapa särskilda rader avsedda för delbetalningarna. Allt arbete som slutförs i projektet och läggs till i planen registreras på förbrukningsraderna. För varje ny betalningsaktivitetsrad på planeringsraderna är radtypen **Fakturerbart**, vilket innebär att kunden ska faktureras. Registrera en ny rad för handpenningen. På förbrukningsraden kan du ange information om de artiklar och resurser som har förbrukats i projektet och som utökar planen, t. ex. arbetstid och artiklar som används i projektet.  

### <a name="to-make-a-payment-by-installment" />Så här gör du en delbetalning

1. Skapa ett nytt projekt.  
2. På det nya **projektkortet** fyller du i följande information:  

    - **Beskrivning**: **Renovering av reception**  
    - **Faktureringskundnr**: **30000**  
    - **Projektbokföringsmall**: **Inreda**  
    - **PIA-metod**: **Kostnadsvärde**  

3. På jobbkortet, välj åtgärden **Priser** och välj sedan åtgärden **Resursen**. Ange följande information:  

    - **Kod**: **Tricia**  
    - **A-pris**: **10**  

     Stäng sidan.  

4. På kortet **Jobb** i avsnittet **Aktiviteter**, lägg till jobbuppgiftsrader som beskrivs i följande tabell:  

    | Rad | Projektaktivitetsnr | Beskrivning          | Typ av projektaktivitet |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Betalning – handpenning | Bokföring       |
    | 2    | 2000         | Användning                | Bokföring       |
    | 3    | 3000         | Betalning – halvvägs     | Bokföring       |
    | 4    | 4000         | Betalning – slutförande | Bokföring       |

5. Välj uppgift 1000 och välj sedan åtgärden **Projektplaneringsrader**.  

6. Skapa en planeringsrad med följande information:  

    | Rad | Radtyp | Planeringsdatum  | Typ        | Nr   | Antal | Styckpris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbart  | (dagens datum) | Redovisningskonto | 40255 | 1        | 5000       |

     Stäng sidan.  

7. Välj uppgift 2000 och välj sedan åtgärden **Projektplaneringsrader**.  

8. Skapa en planeringsrad med följande information:

    | Rad | Radtyp | Planeringsdatum  | Typ     | Nr    | Antal |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budget    | (dagens datum) | Resurs | Tricia | 120      |
    | 2    | Budget    | (dagens datum) | Artikel     | 70104  | 10       |

     Stäng sidan. På sidan **Projektaktivitetsrader** ser du de planerade belopp som har uppdaterats.  

9. Välj uppgift 32000 och välj sedan åtgärden **Projektplaneringsrader**.  

10. Skapa en planeringsrad med följande information:

    | Rad | Radtyp | Planeringsdatum   | Typ        | Nr   | Antal | Styckpris |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbart  | (ett framtida datum) | Redovisningskonto | 40255 | 1        | 5000       |

     Stäng sidan.  

11. Skapa en liknande planeringsradtransaktion för projektaktivitet 4000.  

 Nu när aktivitets- och planeringsraderna har registrerats kan Prakash skapa en faktura på den första betalningen. Prakash gör det från projektaktivitetsraderna för att vara säker på att fakturan bara innehåller raderna för den första betalningen. Du kan öppna försäljningsordern från planeringsraderna eller projektaktivitetsraderna.  

### <a name="to-create-an-invoice" />Så här skapar du en faktura

1.  På sidan **Projektaktivitetsrader** väljer du rad 1000 och väljer sedan åtgärden **Skapa förs.faktura**.  
2.  Ange dagens datum som bokföringsdatum på sidan **Skapa försäljningsfaktura**, ange **Per aktivitet** och välj **OK** för att skapa en faktura med standardinformationen. Välj **OK** för att stänga bekräftelsesidan.  
3.  Välj åtgärden **Skapa försäljningsfaktura/kreditnota**. På försäljningsfakturan ser du att det bara är handpenningen som ingår i fakturan. Du kan nu skicka fakturan till kunden enligt överenskommelse.  

## <a name="next-steps" />Gå vidare

 Den här genomgången har handlat om några av de grundläggande stegen när man arbetar med projekt i [!INCLUDE[prod_short](includes/prod_short.md)]. Du har lärt dig hur du skapar ett nytt projekt, hur du kopierar ett projekt och hur du hanterar betalningar. Du har också sett en demonstration av hur du kan följa upp timmar och skapa fakturor.  

## <a name="see-related-microsoft-trainingtrainingpathscreate-jobs" />Se relaterad [Microsoft utbildning](/training/paths/create-jobs/)

## <a name="see-also" />Se även

 [Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Ställa in projekthantering](projects-setup-projects.md)  
 [Använda resurser](projects-how-use-resources.md)  
 [Övervaka framsteg och resultat](projects-how-monitor-progress-performance.md)  
 [Fakturera projekt](projects-how-invoice-jobs.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

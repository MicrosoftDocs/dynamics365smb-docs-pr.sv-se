---
title: Skapa nummerserier
description: Lära dig hur du anger nummerserier som tilldelar unika ID-koder till konton och dokument i Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="create-number-series"></a>Skapa nummerserier

För varje företag som du lägger upp måste du tilldela unika ID-koder till exempelvis redovisningskonton, kund- och leverantörskonton, fakturor och dokument. Numrering är viktigt inte enbart för identifiering. Ett adekvat numreringssystem gör också företaget mer hanterbart och enkelt att analysera, och kan minska antalet fel som uppstår vid datainmatning.

> [!Important]
> Som standard är luckor inte tillåtna i nummerserier eftersom den exakta historiken över de ekonomiska transaktionerna måste vara tillgänglig för granskning, enligt lag, och därför måste följa en obruten sekvens utan borttagna nummer.
> 
> Om du vill tillåta luckor i vissa nummerserier ska du först samråda med revisorn eller redovisningschefen och se till att du följer de juridiska kraven i ditt land/din region. Mer information finns i avsnittet [Luckor i nummerserier](#gaps-in-number-series).

> [!NOTE]  
> Vi rekommenderar att du använder samma nummerserie som du ser på sidan **Nr-serielista** i demonstrationsföretaget CRONUS. Koder som *P-INV+* kanske inte passar direkt, men [!INCLUDE[prod_short](includes/prod_short.md)] har flera standardinställningar som hör ihop med dessa nummerseriekoder.

Du skapar ett numreringssystem genom att skapa en eller flera koder för varje typ av huvuddata eller dokument. Du kan till exempel skapa en kod för numrering av kunder, en annan för numrering av försäljningsfakturor och en annan för numrering av dokument i redovisningsjournaler. När du har skapat en kod måste du ställa in minst en nummerserierad. Nummerserieraden innehåller information som första och sista nummer i serien och startdatum. Du kan registrera flera nummerserierader per nummerseriekod, med olika startdatum på varje rad. Nummerserierna används löpande, med början på respektive startdatum.

> [!NOTE]
> Den maximala längden för ett tal i nummerserien är 20 tecken. I vissa situationer där [!INCLUDE[prod_short](includes/prod_short.md)] läggs ett nummer till med ett systemgenererat ID. När exempelvis dokument som t.ex. fakturor används för att koppla transaktioner, t.ex. betalningar, [!INCLUDE[prod_short](includes/prod_short.md)] genereras identifierare för de transaktioner som tillämpas. Identifieraren består av ett nummer från en nummerserie och ett sex tecken som tilldelats systemet, t.ex. -12345. Om du förväntar dig att hantera fler än 9999 dokument i bank- eller GIRO-journaler, eller inbetalningsjournaler, anger du nummerserier för dessa dokument typer så att de innehåller färre än 14 tecken.

Du ställer normalt in nummerserier till att automatiskt infoga nästa nummer på nya kort eller dokument som du skapar. Men kan du också skapa en nummerserie för att manuellt ange det nya numret. Du anger detta med kryssrytan **Manuell numrering.**

Om du vill använda mer än en nummerseriekod för en typ av huvuddata, till exempel om du vill använda olika nummerserier för olika kategorier med artiklar, kan du använda nummerseriesamband.

## <a name="gaps-in-number-series"></a>Luckor i nummerserier
Alla poster som du skapar i [!INCLUDE[prod_short](includes/prod_short.md)] är inte ekonomiska transaktioner som måste använda sekventiell numrering. Kundkort, försäljningsofferter och lageraktiviteter är exempel på poster som tilldelas ett nummer från en nummerserie, men som inte omfattas av finansiell granskning och/eller kan tas bort. För en sådan nummerserie kan du markera kryssrutan **Tillåt luckor i nummer** på sidan **Nr-serier rader**. Den här inställningen kan också ändras efter att nummerserien skapats. För mer information, se [Så här skapar du en ny nummerserie](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Fältet Nr. på dokument och kort

På försäljnings-, inköps- och överföringsdokument och alla kort kan **Nr.** kan fyllas i automatiskt från en fördefinierad nummerserie, eller så kan du lägga till den manuellt. I vissa fall är dock fältet **Nr.** fältet är osynligt så att du inte kan redigera det.  

Fältet **nr.** kan fyllas i på tre sätt:

1. Om endast en nummerserie finns för typen av dokument eller kort finns där fältet **Förvalda nr.** är markerad och **Manuella nr.** inte är markerad för den nummerserien, så fylls fältet automatiskt i med nästa nummer i serien, och fältet Nr. Fältet **nr.** Fältet visas inte på kortet eller dokumentet.  

    Även om du definierar mallar med olika nummerserier för kunder, om den nummer serie som har definierats på sidan **försäljningsinställningar** har angetts på det här sättet, visas fältet **Nr.** fältet kommer att vara osynligt på kundkortet, oavsett vilken mall du använder. Detsamma gäller för andra typer av kort och dokument.  

    > [!NOTE]  
    > Om nummerserien inte fungerar, till exempel eftersom antalet nummer har tagit slut, kommer fältet **Nr.** att visas och du kan manuellt ange ett nummer eller lösa problemet på sidan **Nummerserie**.

2. Om mer än en nummerserie finns för typen av dokument eller kort, och kryssrutan **Förvalda nr.** inte har markerats för den nummerserie som för tillfället tilldelats, så kommer fältet **Nr.** att visas, och du kan öppna sidan **Nummerserie** och välja den nummerserie som du vill använda. Nästa nummer i serien förs då in i fältet **Nr.** .

3. Om du inte har skapat en nummerserie för dokument- eller korttypen, eller om fältet **Manuella nr.** har valts för nummerserien, så kommer fältet **Nr.** att visas, och du måste ange en siffra manuellt. Du kan ange högst 20 tecken, både siffror och bokstäver.

När du öppnar ett nytt dokument eller kort som det finns en nummerserie för, öppnas tillhörande **Inställningar för nummerserie**-sida så att du kan ställa in en nummerserie för den typen av dokument eller kort innan du fortsätter med övriga datainmatningar.

> [!NOTE]  
> Om du behöver aktivera manuell numrering för till exempel nya artikelkort som har skapats med en datamigreringsprocess som döljer fältet **Nr.** som standard, gå då till sidan **Lagerinställningar** och välj sedan fältet **Artikelnr.** om du vill öppna och ange relaterade nummerserier som **Manuell numrering**.

## <a name="to-create-a-new-number-series"></a>Så här skapar du nummerserier

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Nummerserier** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.  
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Välj åtgärden **Rader**.  
5. På sidan **Nr-serier rader** fyller du i fälten för att definiera den faktiska användningen och innehållet i nummerserien som du skapade i steg 2.  
6. Upprepa steg 5 för alla andra användningsområden för nummerserien som du behöver. Fältet **Startdatum** anges vilken nummerserierad som är aktiv.  

> [!TIP]
> Om du vill att användarna ska kunna ange nummer manuellt när de registrerar en ny kund eller leverantör kan du t. ex. välja fältet **Manuell numrering** i nummerserien. Rensa fältet om du inte vill tillåta manuell numrering.

Du kan tilldela nummerserier till de mallar som du konfigurerar för de olika typer av kunder och leverantörer som dina säljare och inköpare oftast lägger till i din [!INCLUDE [prod_short](includes/prod_short.md)]. I så fall kan du registrera de relevanta nummerserierna, länka dem till olika relationer och sedan lägga till den första nummerserien i relevant relation till relevant inställningssida. När en användare skapar en kund väljer de relevant mall och den nya kunden får ett nummer från den nummerserie som har definierats för mallen.  

## <a name="to-create-relationships-between-number-series"></a>Så här skapar du samband mellan nummerserier

Om du har definierat mer än en nummerseriekod för samma typ av allmän information eller transaktioner kan du skapa samband mellan koderna. Den här funktionen gör det enklare för dig att välja bland koderna när du använder ett nummer. När du skapar ett samband mellan ett antal nummerserier associerar du alla relaterade nummerserier till en nummeseriekod. Sedan kan du ange koden i ett fält under snabbfliken **Numrering** på en av de relevanta inställningssidorna, till exempel **Försäljningsinställningar**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Nummerserier** och väljer sedan relaterad länk.
2. Markera raden med de nummerserier som du vill skapa relationer för och välj sedan **Relationer**.
3. I fältet **Seriekod** anger du koden för nummerserien som du vill koppla till serien du valde i steg 2.
4. Lägg till en rad för varje kod som du vill koppla till den valda nummerserien.
5. Stäng sidan.

När du hädanefter definierar något för vilket ett nummer krävs kan du använda sambanden som har skapats för att välja bland de kopplade nummerserierna.

## <a name="to-set-up-where-a-number-series-is-used"></a>Om du vill konfigurera var en nummerserie används

I följande procedur beskrivs hur du ställer in nummerserier för området Försäljning. Stegen är liknande för andra områden.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Försäljningsinställningar** och väljer sedan relaterad länk.
2. På sidan **försäljning** klickar du på snabbfliken **nr-serier** och väljer önskade nummerserier för varje försäljningskort och dokument.

Det markerade numret kommer nu att användas för att fylla i fältet **nr.** på kortet eller dokumentet i fråga enligt de inställningar du har gjort på nummerserieraden.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

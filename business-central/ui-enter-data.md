---
title: Så här anger du data i Business Central | Microsoft Docs
description: Lär dig mer om allmänna funktioner som hjälper dig att ange data i fälten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/03/2020
ms.author: edupont
ms.openlocfilehash: 1ad2eb6d2e9a423aa1891eb52f71e815f4b89eff
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785452"
---
# <a name="entering-data"></a>Ange data

Det finns många allmänna funktioner som hjälper dig att ange data lättare, snabbare och mer exakt. Dessa grundläggande principer och avancerade funktioner för dataregistrering beskrivs i den här artikeln.  

I exemplen nedan används demonstrationsdata.

## <a name="working-with-editable-fields"></a>Arbeta med redigerbara fält
Fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan innehålla olika redigerbara data, t.ex. text eller valutabelopp. Redigerbara fält visar oftast en inmatningsruta där du kan skriva eller välja ett värde. Fält som inte kan redigeras visas vanligtvis med grå bakgrund.   

Vissa redigerbara fält innehåller en väljare som du kan använda för att ange ett värde.  

<!-- TODO: Add illustrations or images of each picker -->
|**Plockare**        |**Så här kan du ange ett värde**|
|------------------|------------------------------------|
|Datumväljare       |Den här väljaren visar en kalender som baseras på de aktuella nationella inställningarna. Du kan välja ett enstaka datum.|
|Listruta          |Listrutor ger dig möjlighet att välja fasta värden eller referera till poster från en annan tabell|
|Växel eller kryssruta|Vissa fält ger ett enkelt alternativ med värdena *Ja* eller *Nej*. Växeln används för att ange det här värdet och visas alltid som en kryssrutor i listor|
|Assist redigera       |Vissa fält tillhandahåller anpassade väljare som passar för att söka efter och välja det bästa värdet för fältet, till exempel popup-fönster.|


### <a name="modifying-a-field-value"></a>Ändra ett fältvärde

Om du vill ändra värdet i ett fält måste du först ställa in fokus på det fältet. Du ställer in fokus genom att göra följande:

- Använd **Tabb**-nyckel. Åtgärden markerar hela värdet.
- Vänsterklicka på musen eller på en liknande indataenhet. Med den här instruktionen kan du bara markera hela fältvärdet om fältet finns i en lista.  

När du interagerar med fält i användargränssnittet prioriterar [!INCLUDE[d365fin](includes/d365fin_md.md)] normalt hela fältvärdet så att det blir enklare att ersätta värdet.

När hela fältvärdet är markerat:
- Ersätt värdet genom att bara ange ett nytt värde. Om fältet innehåller en väljare kan du aktivera det med hjälp av kortkommandot **Alt + nedpil**.
- Använd **Ta bort** eller **Backsteg** för att rensa värdet.

Tryck på **F2** för att växla mellan att markera hela fältets värde eller att placera markören efter fältets värde. Om du placerar markören i slutet av värdet blir det enklare att lägga till det befintliga värdet.

När markören visas i slutet av fältvärdet:
- Lägg till värdet genom att bara skriva.
- Använd nyckel **Start**, **Slut**, **Vänsterpil** och **Högerpil** för att flytta markören i värdet. Om du redigerar ett fält i en lista, trycker du på **vänsterpilen** igen när markören är i början av värdet så aktiveras föregående fält. På samma sätt kan du trycka på **högerpilen** igen när markören är i slutet av värdet för att ge fokus till nästa fält.

> [!NOTE]
> När du har angett ett värde kommer Business Central endast att kontrollera att den är giltig när du har klickat utanför fältet eller ange ett annat element, t.ex. nästa fält.  


## <a name="keyboard-shortcuts"></a>Kortkommandon

Det finns flera kortkommandon som du kan använda för att arbeta med musen och snabba upp din datainmatning. Dessa kortkommandon är särskilt användbara när du vill ha stora och repetitiva uppgifter.

Mer information om genvägar finns i [Kortkommandon](keyboard-shortcuts.md). I den här artikeln beskrivs några kortkommandon.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Påskynda datainmatning med snabbinmatning

Snabbinmatning är en funktion som skapats för datainmatning vid användning av tangentbordet. Snabbinmatning fungerar på fält (t.ex. på kortsidorna) och i listor (rader och kolumner). Det är praktiskt när du utför återkommande uppgifter som kräver att flera poster skapas i sekvens. Exempel omfattar en grupp försäljningsorder eller registrering av nya artiklar.

Du kan använda Tabb-tangenten för att gå från ett fält på en sida till nästa redigerbara fält. Nackdelen med att använda Tabb-tangenten är att det alltid går sekventiellt till nästa fält. <!-- even if the field is non-editable or seldom filled it in.-->Snabbinmatning låter dig ändra den här sökvägen. Med snabbinmatning gör att du kan använda returtangenten för att navigera genom enbart de fält som du är intresserad av. Snabbinmatning hoppar över icke redigerbara fält och fält som du vanligtvis inte fyller i. Du kanske redan har upptäckt denna funktion på vissa sidor. Detta beteende beror på att fälten som ska inkluderas när du trycker på retur och vilka som ska hoppas över har fördefinierats. Du kan anpassa snabbinmatning genom att anpassa arbetsytan och optimera hur du anger data på varje sida.

### <a name="how-quick-entry-works"></a>Hur snabbinmatning fungerar

Varje fält kan markeras som antingen *inkluderas i snabbinmatning* eller *exkluderas från snabbinmatning*. Fält som inkluderas i snabbinmatning infogas i sökvägen när du trycker på retur. Fält som utesluts från snabbinmatning kommer inte.

När du är klar med att ange data i ett fält trycker du bara på Retur för att bekräfta ändringarna och gå till nästa fält. Om du vill byta riktning och fortsätter till föregående fält trycker du på Shift + Retur. Mer information om genvägar finns i [kortkommandon för snabbinmatning för fält](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tips och råd

Listan nedan ger användbar information om hur du använder snabbinmatning.

- Den är tillgänglig för alla fält som kan redigeras.
- Den fungerar även i kolumner och rader.
- Den hindrar inte från att komma åt andra element på en sida, till exempel åtgärder. Dessa element är tillgängliga genom att använda Tabb och Shift + Tabb.  
- Det är inte nödvändigt att snabbflikar expanderas för att snabbinmatning ska fungera. Om nästa snabbinmatningsfält finns i en komprimerad snabbflik kommer den snabbfliken automatiskt expandera och fokusera på det valda fältet. [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer ihåg att snabbfliken ska expanderas nästa gång du besöker sidan.  
- Snabbinmatning fungerar oavsett om fälten är obligatoriska. Så det är en bra idé att kontrollera att obligatoriska fält är inkluderade i snabbinmatning.
- Som standard inkluderas de flesta fält i snabbinmatning. Så i början kommer uppgiften troligen att utesluta fält från snabbinmatning.

### <a name="to-change-quick-entry-fields"></a>Så här ändrar du snabbinmatningsfält

Om du vill ställa in snabbinmatning för fält använder du anpassning.

1. Starta anpassning genom att välja ikonen ![Inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan åtgärden **Anpassa**.
2. Markera ett fält som du vill ändra. Markera motsvarande kolumnrubrik i listor. Välj sedan antingen **Inkludera i snabbinmatning** eller **Exkludera från snabbinmatning**.

Mer information om anpassning finns i [Anpassa arbetsyta](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Obligatoriska fält

När du anger data på sidor markeras vissa fält med en röd asterisk. Den röda asterisken innebär att fältet måste fyllas i för att slutföra en viss operation. Ett exempel är när du bokför en transaktion som använder värdet i fältet.  

Även om ett fält är obligatoriskt tvingas du inte fylla i fältet innan du fortsätter till andra fält eller stänger sidan. Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.  

## <a name="finding-data-as-you-type"></a>Söka efter data allt eftersom du skriver

 När du börjar skriva tecken i ett fält visas en listruta med möjliga fältvärden. Listan ändras allt eftersom du skriver fler tecken, och du kan välja rätt värde när det visas.  

 Många fält har en nedpil-knapp som du kan välja. Du kan välja pilen om du vill visa en lista med data som är tillgängliga för fältet. Knappen har två funktioner beroende på typen av fält:  

-   Sökning – Visar information från en annan tabell som du kan infoga i fältet. Du kan bara välja en i taget.  

-   Lista – Visar den uppsättning alternativ (fasta val) som finns för fältet. Du kan bara markera ett av alternativen.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Kopiera och klistra in fält och rader för vanliga frågor

Du kan kopiera en eller flera rader från en lista eller ett enstaka fält på en sida. Klistra sedan in det du kopierade på samma sida, en annan sida eller ett externt dokument. Du kan t.ex. klistra in Microsoft Excel eller Outlook-e-post. Kortfattat, för att kopiera trycker du på CTRL + C (cmd + C i macOS) på tangentbordet. Klistra in genom att trycka på CTRL+V eller cmd+V i macOS.

I en lista kopierar du fältet i samma kolumn i raden ovanför och klistra in den i den aktuella raden, tryck bara på F8.

Mer information finns i avsnittet [kopiera och klistra in vanliga frågor](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Filtrera radposter

För att starta filtrering, välj ![Filterrutaikon](media/open-filter-pane-icon.png "Filterrutaikon") högst upp i listan eller tryck på Shift+F3 för att öppna filterrutan. Du kan arbeta med filterrutan som på vilken lista som helst. Mer information finns i [Filtrering](ui-enter-criteria-filters.md#filtering).

Filtrering är särskilt användbart när du visar och analyserar längre dokument. Anta att du öppnar en bokförd försäljningsfaktura. Sedan kan du filtrera radartiklarna så att de visar alla radartiklar som har en individuell rabatt på över 5 %. Du kan också filtrera fram cykel tillbehör med "pro" i namnet.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Fokusera på radartiklar

När du arbetar med dokument som innehåller en del av en radartikel, kan du växla vyn så att endast radartiklarna fokuseras. Exempel på dokument är försäljningsorder och faktura. Radartikeldelen expanderas så att den upptar nästan hela arbetsytan. Den döljer andra delar av sidan utom området åtgärder högst upp. Denna layout ger dig en bättre översikt över radobjekten och ger mer plats att arbeta med dem.

Du får särskilt fördelar när du arbetar med stora radartikellistor och du vill ange data snabbt. Den här funktionen ger även avancerad filtreringskapacitet. På samma sätt som i andra listor blir det ännu enklare att bläddra och söka igenom radobjekt.

### <a name="switching-the-focus-on-and-off"></a>Aktivera och inaktivera fokus

För att fokusera på radartiklar väljer du var som helst i radartikeldelen och välj ![ikonen Fokusläge](media/focus-mode.png "Ikonen Fokusläge") i övre högra hörnet eller tryck på Ctrl+Shift+F12.

Om du vill växla tillbaka till normal vy, välj ![ikonen Fokusläge](media/focus-mode.png "Ikonen Fokusläge") eller tryck på Ctrl+Shift+F12 igen.

## <a name="multitasking-across-multiple-pages"></a>Multikörning över flera sidor

Du kan öppna ett kort eller en dokument sida i ett nytt fönster. När du öppnar ett nytt fönster kan du:

- Arbeta med flera uppgifter samtidigt
- Hantera avbrott för den aktuella uppgiften, t.ex. inkommande samtal.
- Håll ett fönster öppet för en pågående uppgift medan du startar eller slutför en annan uppgift i fönster.

Om du vill öppna det aktuella kortet eller dokumentet i ett nytt fönster väljer du ![Öppna nytt fönster](media/open-new-window-icon.png "Ikonen Öppna nytt fönster") i det övre högra hörnet eller trycker på Alt+Shift+W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Om du vill öppna det aktuella kortet eller dokumentet i ett nytt fönster väljer du ![Öppna nytt fönster](media/open-new-window-icon.png "Ikonen Öppna nytt fönster") i det övre högra hörnet eller trycker på Alt+Shift+W.

> [!NOTE]
> När du öppnar andra sidor från ett kort eller dokument som öppnas i ett nytt fönster öppnas sidorna i ett nytt fönster även om du inte väljer ![Öppna nytt fönster](media/open-new-window-icon.png "Ikonen Öppna nytt fönster").

> [!NOTE]
> Om du arbetar i Safari kan det hända att det nya fönstret inte öppnas i popup-blockeraren. I så fall anger du produktens URL som en tillåten webbplats. För information, se [Ändra inställningar i Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Samma sak kan hända i andra webbläsare, till exempel Firefox. Mer information finns i [Inställningar för blockering av popup-fönster i Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Ett ytterligare sätt att multitaska är att öppna [!INCLUDE[d365fin](includes/d365fin_md.md)] i två eller flera webbläsarflikar. När du gör detta bör du skapa en ny flik och sedan kopiera/klistra in URL-adressen för den ursprungliga fliken på den nya fliken. Då skapas en ny session.   

> [!NOTE]
> Använd inte funktionen **Kopiera** i webbläsaren för att skapa den nya fliken eftersom detta kan medföra att åtgärder på en flik blockerar åtgärder på andra flikar då dessa ingår i samma session.

## <a name="entering-quantities-by-calculation"></a>Ange antal genom beräkning

När du skriver siffror i antalsfält, till exempel fältet **Antal** för en artikeljournalrad, kan du skriva formeln i stället för summan.  

### <a name="examples"></a>Exempel  

-   Om du skriver 19+19 beräknas fältet till 38.  

-   Om skriver 41-9 beräknas fältet till 32.  

-   Om du skriver 12*4 beräknas fältet till 48.  

-   Om du skriver 12/4 beräknas fältet till 3.  

## <a name="entering-negative-numbers"></a>Ange negativa antal

Du kan ange negativa antal på två sätt. Numret -20,5 som kan anges:  

-   -20.5  

    eller
-   20.5-  

 I båda fallen registreras beloppet som -20,5.  

 Om det sista tecknet i uttrycket är **+** eller **-**, kommer hela uttrycket registreras med det tecknet. Ett exempel, **10-20+**, ska leda till 10 och inte -10.  

## <a name="entering-dates-and-times"></a>Ange datum och tider

Du kan ange datum och tider i alla datumfält. Du kan skriva datum med eller utan avgränsare.

> [!NOTE]  
> Hur du anger datum och klockslag beror på dina **region**-inställningar. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Ange datum

Du kan antingen använda dataväljaren för att välja ett datum från en kalender, eller också kan du ange datumen manuellt. Det här avsnittet innehåller en kort översikt över hur du anger datum. Mer information finns i [arbeta med kalenderdatum och tider](ui-enter-date-ranges.md).

För manuell datainmatning kan du skriva in två, fyra, sex eller åtta siffror.  

-   Två siffror tolkas som dagen. Månad och år läggs till i arbetsdagens datum.  

-   Fyra siffror tolkas som dag och månad. År läggs till i arbetsdagens datum.  

-   Om det datum du vill använda ligger inom intervallet 1930-01-01 till 2029-12-31 anger du året med två siffror. Ange annars året med fyra siffror.  

Du kan också ange ett datum som en veckodag följt av ett veckonummer. Du kan också ange ett år. Till exempel Mån25 eller mån25 betyder måndag vecka 25.  

I stället för att skriva in ett visst datum kan du skriva in någon av dessa koder.  

|Kod|Resultat|  
|--------------|----------------|  
|d|Det här anger dagens datum (detta är datorns systemdatum).|  
|p|Det här anger en bokföringsperiod där p innebär den första bokföringsperioden, p2 innebär den andra bokföringsperioden och så vidare. |
|a|Detta anger arbetsdatumet som har lagts upp i programmet. Om du vill ändra arbetsdatumet, [ändra grundläggande inställningar](ui-change-basic-settings.md). Det är praktiskt att använda arbetsdatum om du har många transaktioner med ett annat datum än dagens datum.|
|a|Detta anger att datumet efter a är ett avslutsdatum, till exempel A120131.|  

## <a name="entering-times"></a>Ange tider

När du anger tider kan du infoga vilken avgränsare du vill mellan enheterna. Detta är dock inte obligatoriskt. Du behöver inte skriva minuter, sekunder eller AM/PM.  

I följande tabell visas de olika sätt som du kan ange tider på, samt hur de tolkas.  

|Transaktion|Tolkning|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5.50|05:30:05.5|  
|053005050|05:30:05.05|  

 Du måste ange två siffror för varje tidsenhet om du inte använder någon avgränsare.  

## <a name="entering-datetimes"></a>Ange datum och tid

När du anger datum och tid måste du ange ett blanksteg mellan datumet och tiden.  

Listan nedan innehåller de olika sätt som du kan ange datum och tid på och en förklaring av hur de ska tolkas.  

|Transaktion|Tolkning|  
|---------------|------------------------|  
|`131202` 132455|02-12-13 13:24:55|  
|1-12-02 10|02-12-01 10:00:00|  
|1.12.02 5|02-12-01 05:00:00|  
|1.12.02|02-12-01 00:00:00|  
|11 12|innevarande år-innevarande månad-11 12:00:00|  
|1112 12|innevarande år-12-11 12:00:00|  
|d eller dagens datum|dagens datum 00:00:00|  
|d tid|dagens datum aktuell tid|  
|d 10:30|dagens datum 10:30:00|  
|d 03:03:03|dagens datum 03:03:03|  
|a eller arbetsdagens datum|arbetsdagens datum 00:00:00|  
|m eller måndag|måndag i innevarande vecka 00:00:00|  
|ti eller tisdag|tisdag i innevarande vecka 00:00:00|  
|on eller onsdag|onsdag i innevarande vecka 00:00:00|  
|to eller torsdag|torsdag i innevarande vecka 00:00:00|  
|fr eller fredag|fredag i innevarande vecka 00:00:00|  
|lö eller lördag|lördag i innevarande vecka 00:00:00|  
|sö eller söndag|söndag i innevarande vecka 00:00:00|  
|ti 10:30|tisdag i innevarande vecka 10:30:00|  
|ti 03:03:03|tisdag i innevarande vecka 03:03:03|  

## <a name="entering-duration"></a>Ange varaktighet

Du anger varaktigheten som en siffra följd av en enhet.  

Här följer några exempel.  

|Varaktighet|Måttenhet**|  
|------------------|-------------------------|  
|2t|2 timmar|  
|6t 30m|6 timmar 30 minuter|  
|6,5t|6 timmar 30 minuter|  
|90m|1 timme 30 minuter|  
|2d 6t 30m|2 dagar 6 timmar 30 minuter|  
|2d 6t 30m 56s 600ms|2 dagar 6 timmar 30 minuter 56 sekunder 600 millisekunder|  

 Du kan även ange en siffra som automatiskt konverteras till en varaktighet. Det tal som anges konverteras med den standardenhet som har angetts för varaktighetsfältet.  

 Om du vill veta vilken enhet som används i ett varaktighetsfält kan du ange en siffra och kontrollera vilken enhet den konverteras till.  

 Numret 5 konverteras till 5 timmar om enheten är timmar.  

## <a name="see-also"></a>Se även  
 [Sortera, söka och filtrera listor](ui-enter-criteria-filters.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

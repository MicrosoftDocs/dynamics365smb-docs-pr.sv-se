---
title: Konfiguration av bokföringsmall
description: Lär dig hur du använder bokföringsmallar för att spara tid och för att undvika misstag när du bokför transaktioner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 02/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Konfigurera bokföringsmallar

Bokföra gruppmappningsentiteter till redovisningskonton. Exempel på entiteter är kunder, leverantörer, artiklar, resurser och försäljnings- och inköpsdokument. Bokföringsmallar sparar tid och hjälper dig undvika fel när du bokför transaktioner. Transaktionsvärdet går till de konton som anges i bokföringsmallen för den aktuella enheten. Det enda kravet är att det finns en kontoplan. Mer information finns i [Ställa in kontoplanen](finance-setup-chart-accounts.md).  

Bokföringsmallar omfattas av tre paraplyer:  

* Allmänt

  Definiera vem du säljer till och köper från, samt vad du säljer och vad du köper. Du kan också slå ihop mallar om du vill ange bland annat resultatkontona att bokföra till eller använda mallar för att filtrera rapporter.  
* Specifik

  Exempelvis använda försäljningsdokument istället för att bokföra direkt i redovisningen. När du skapar transaktioner i kundreskontra används motsvarande transaktioner i redovisningen.  
* Moms

  Definiera vilka skatteprocentsatser och beräkningstyper som gäller för vem du säljer till och köper från, samt vad du säljer och vad du köper.

I följande avsnitt beskrivs bokföringsmallarna under varje paraply.  

## Generella bokföringsmallar

I följande tabell beskrivs de allmänna bokföringsmallarna.

| Typ | Beskrivning |
| --- | --- |
| Generella rörelsebokföringsmallar |Tilldela denna mall till kunder och leverantörer för att ange vem du säljer till och som du vill köpa från. Ställ in dessa bokföringsmallar på sidan **Rörelsebokföringsmallar**. När du gör det ska du tänka på hur många mallar som du måste bryta ned försäljning och inköp. Till exempel kunder och leverantörer efter geografiskt område eller efter typ av verksamhet. |
| Generella produktbokföringsmallar |Tilldela den här mallen till artiklar och resurser för att ange vad du säljer och vad du köper. Ställ in dessa bokföringsmallar på sidan **Produktbokföringsmallar**. När du gör det måste du tänka över hur många mallar du måste bryta ner försäljning per produkt (artiklar och resurser) och inköp per artikel. Dela exempelvis upp mallarna efter råmaterial, detaljhandel, resurser, kapacitet och så vidare. |
| Bokföringsinställningar |Kombinera rörelse- och produktbokföringsmallar och välj sedan konton att bokföra till. För varje kombination av rörelse- och produktbokföringsmallar kan du tilldela en specifik uppsättning redovisningskonton. Detta betyder att du till exempel kan bokföra försäljningen av samma artikel på olika försäljningskonton i redovisningen eftersom kunder tilldelas olika rörelsebokföringsmallar. Ställ in dessa konfigurationer på sidan **Bokföringsinställningar**. |

## Specifika bokföringsmallar

I tabellen nedan beskrivs de bokföringsmallar som är specifika för datatyper.

|Typ | Beskrivning |
| --- | --- |
| Kundbokföringsmallar |Ange kontona som ska användas när du bokför transaktioner i kundreskontra. Om du använder lagret tillsammans med kundreskontra bestämmer den generella rörelsebokföringsmallen som har tilldelats till kunden och den generella produktbokföringsmallen som har tilldelats till lagerartikeln vilka konton som försäljningsorderraden ska bokföras till. Se *Generella rörelsebokföringsmallar* och *Generella produktbokföringsmallar* i avsnittet [Generella bokföringsmallar](#general-posting-groups). Ställ in dessa bokföringsmallar på sidan **Kundbokföringsmallar**. |
| Leverantörsbokföringsmallar |Definiera var transaktioner för leverantörsreskontrakonton, serviceavgiftskonton och kassarabattskonton ska bokföras. Detta liknar kundbokföringsmallar. Ställ in dessa bokföringsmallar på sidan **Leverantörsbokföringsmallar**. |
| Lagerbokföringsmallar |Definiera lagerbokföringsmallar som du sedan tilldelar motsvarande artikelkonton på sidan **Lagerbokföringsinställning**. På så sätt bokför systemet till det redovisningskonto som har angetts för den kombination av lagerbokföringsmall och lagerställe som har kopplats till artikeln, när du bokför transaktioner avseende artikeln. Med lagerbokföringsmallar kan du även på ett utmärkt sätt organisera ditt lager. När du genererar rapporter kan du separera artiklar efter deras bokföringsmallar. Ställ in dessa bokföringsmallar på sidan **Lagerbokföringsmallar**. |
| Bokföringsmallar för bankkonto |Definiera redovisningskonton som bank-kontotransaktioner bokförs på. Detta kan till exempel förenkla processer för att spåra transaktioner och stämma av bankkonton. Ställ in dessa bokföringsmallar på sidan **Bokföringsmallar för bankkonto**. Vi rekommenderar att redovisningskontona har fältet **Direkt bokföring** inställt på *Nej*. |
| Bokföringsmallar för anläggningstillgångar |Definiera konton för olika typer av utgifter och kostnader som t. ex. förvärvskostnader, ackumulerade avskrivningsbelopp, förvärvskostnader vid avyttring, ackumulerad avskrivning vid avyttring, vinster vid avyttring, förluster vid avyttring, underhållskostnader och avskrivningsutlägg. Ställ in dessa bokföringsmallar på sidan **Anl.bokföringsmallar**. |

### Tillåta ersättningsbokföringsmallar för kunder eller leverantörer i dokument

Du kan låta användarna välja andra kund- och leverantörsbokföringsmallar än standardgrupper när de arbetar med försäljnings- eller inköpsdokument och -journaler.

Om du vill tillåta ändringar av kundbokföringsmallar väljer du **Tillåt flera bokföringsmallar** på sidorna **Inställningar för försäljning och kundreskontra** och **Serviceinställningar**, samt sidan **Inställningar för inköp och skulder** för ändringar i bokföringsmall för leverantör.

Påp sidorna **Kundbokföringsmallar** eller **Leverantörsbokföringsmallar** kan du ange de bokföringsmallar som du vill tillåta som ersättningar genom att välja **Ersättningar**. Ersättningsbokföringsmallar kan ersätta de standardmässiga kund- eller leverantörsbokföringsmallar som angetts för en kund eller leverantör.

När du har skapat detta kan du välja mellan de tillåtna ersättningsbokföringsmallarna och ändra kund- eller leverantörsbokföringsmallen när du bokför försäljnings- eller inköpsdokument och -journaler. Ersättningsbokföringsmallarna för kund eller leverantör kopieras till bokförda dokument och journaler, och leverantörs- och kundreskontratransaktioner bokförs på de redovisningskonton som har angetts för ersättningarna.

Om till exempel en faktura och betalning som bokförs med olika kund- eller leverantörsbokföringsmallar tillämpas (olika redovisningskonton) överför [!INCLUDE[prod_short](includes/prod_short.md)] beloppen mellan redovisningskontona för att balansera dem.

## Momsbokföringsmallar

I följande tabell beskrivs de momsrelaterade bokföringsmallarna.

| Typ | Beskrivning |
| --- | --- |
| Momsbokföringsmallar |Se hur du kan beräkna och bokföra moms för kunder och leverantörer. Konfigurera dessa bokföringsmallar på sidan **Rörelsebokföringsmallar för moms**. När du gör det ska du tänka på hur många mallar du behöver. Detta beror t. ex. på ett antal faktorer som t. ex. lokal lagstiftning samt om du gör affärer både inrikes och utrikes. |
| Momsbokföringsmallar |Ange de momsberäkningar som behövs för typerna av artiklar eller resurser som du köper eller säljer. |
| Momsbokföringsinställningar |Kombinera momskombinationer av momsbokföringsmallar. När du fyller i en allmän journalrad, inköpsrad eller försäljningsrad ska vi titta på kombinationen för att identifiera kontona som ska användas. |

Om landet/regionen använder mervärdesskatt (moms), se [Konfigurera beräkningar och bokföringsmetoder för mervärdesskatt](finance-setup-vat.md).  

## Exempel på koppling av bokföringsmallar

Här är ett scenario.  

Dessa bokföringsmallar väljs på kundkortet:  

* Generell rörelsebokföringsmall
* Kundbokföringsmall  

Dessa bokföringsmallar väljs på artikelkortet:  

* Generella produktbokföringsmallar  
* Lagerbokföringsmall  

När du skapar ett försäljningsdokument använder försäljningshuvud kundkortsinformationen och försäljningsraderna använder artikelkortsinformationen.  

* Bokföringen av intäkter (resultaträkning) bestäms av kombinationen av generell rörelsebokföringsmall och generell produktbokföringsmall.  
* Bokföringen av kundreskontra (balansräkning) bestäms av kundbokföringsmallen.  
* Bokföringen av lager (balansräkning) bestäms av lagerbokföringsmallen.  
* Bokföringen av kostnad för sålda varor (resultaträkning) bestäms av kombinationen av generell rörelsebokföringsmall och generell produktbokföringsmall.  

Inställningen avgör när bokföring sker. När är exempelvis timing påverkas av periodiska aktiviteter, som till exempel bokföra lagerkostnad eller justera kost. – artikeltrans.

## Kopiera bokföringsinställningsrader

Ju fler produkt- och rörelsebokföringsmallar du har, desto fler rader ser du på sidan **Allmänna bokföringsinställningar**. Det kan finnas många olika kombinationer av rörelse- och produktbokföringsmallar, men olika kombinationer kan fortfarande bokföras till samma redovisningskonton. Om du vill begränsa andelen manuell inmatning kopierar du redovisningskontona från en befintlig rad på sidan **Generella bokföringsinställningar**.

## Skapa inläggsgrupper när du är på språng

För att användarna ska komma igång snabbare kan [!INCLUDE[prod_short](includes/prod_short.md)] visa meddelanden om redovisningskonton som saknas i olika konfigurationer för bokföringsmallar. För att få dessa meddelanden, se till att meddelandet **Redovisningskonto saknas i bokföringsmall eller inställningar** väljs på sidan **Mina meddelanden**, som du kan komma åt från fältet **Ändra när jag får meddelanden** på sidan **Mina inställningar**.  

På så sätt får du ett meddelande när du arbetar med ett dokument som använder en bokföringsmall eller en inställning som saknar ett nödvändigt redovisningskonto. Välj länken i meddelandet för att öppna en sida där du kan utföra relevanta ändringar, förutsatt att du har behörighet att göra det.  

> [!NOTE]
> För att du ska kunna ta dig direkt till bokförings mal len eller för den inställning som saknar ett redovisningskonto, [!INCLUDE[prod_short](includes/prod_short.md)] skapas en platshållare för bokföringsmall eller inställningar. Bokföringsmallar och -inställningar är ett sätt för revisorn att kontrollera hur transaktioner bokförs i redovisningen så att bokföringsmallar och inställningar inte kan skapas i organisationen just nu.  
>
> I så fall kan du inaktivera meddelandet *Redovisningskonto saknas i bokföringsmall eller inställningar* och sedan samarbeta med din revisor för att göra relevanta ändringar i bokföringsgruppen, inställningarna eller ditt dokument. Det här är ett viktigt steg, eftersom efter att dokumenten har bokförts kan du inte ta bort alla felaktigt använda bokföringsmallar eller inställningar eftersom redovisningstransaktioner skapas för dem.

Använd fältet **Spärrat** i fönstret **Bokföringsinställningar** för att förhindra att användare av misstag använder en konfiguration som inte längre är relevant för nya bokföringar. 

## Få åtkomst till alla fält och konton när du ställer in en bokföringsmall  

Bokföringsmallar kan vara komplicerade att skapa. Eftersom vissa typer av konton inte används ofta visar [!INCLUDE [prod_short](includes/prod_short.md)] inte dem som kolumner på raderna. För att göra det lite lättare att välja rätt konton filtrerar [!INCLUDE [prod_short](includes/prod_short.md)] de konton som du kan välja i fältsökningar. 

Om du vill komma åt alla konton på raderna och i fältsökningarna finns det några inställningar som kan vara till hjälp:

* Om du vill visa alla konton som kolumner på raderna aktiverar du växlingsknappen **Visa alla konton**.
* På enskilda rader markerar du kryssrutan **Visa alla konton vid sökning** för att komma åt alla konton i fältsökningen.

> [!NOTE]
> Växlingsknappen **Visa alla konton** kanske inte verkar fungera på sidan **Bokföringsinställningar**. Det beror på att [!INCLUDE [prod_short](includes/prod_short.md)] alltid visar alla konton som kolumner på raderna på den sidan.

## Felsökning av bokföringsmallfel

Bokföringsmallar är ett av de mer avancerade koncepten som du ställer in i [!INCLUDE[prod_short](includes/prod_short.md)]. Om de inte är korrekt konfigurerade kan fel uppstå vid bokföring av dokument eller journalrader. Dessa fel orsakas exempelvis vanligen av ett misstag i hur redovisningskonton tilldelas eller hur bokföringsmallar kombineras.

Om något är fel visar [!INCLUDE[prod_short](includes/prod_short.md)] sidan **felmeddelanden**. På sidan **felmeddelanden** kan det bli enklare att identifiera och lösa problemet. Sidan ger en beskrivning av felet som pekar ut bokföringsmallinställningarna som behöver åtgärdas. Meddelandet kan t.ex. "förskottsbet. konto för försäljning saknar en bokföringsinställning". Det finns också en länk för att öppna sidan som är orsaken till problemet, så att du snabbt kan lösa det.  

> [!NOTE]
> Fel hanteringen som beskrivs ovan är inte tillgänglig för artikel-, resurs-, personal- och anläggningstillgångsjournaler eller för redovisningskonton som lagts till i lokala versioner av bokföringsmallar.

## Se även

[Huvudbok och kontolista](finance-general-ledger.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

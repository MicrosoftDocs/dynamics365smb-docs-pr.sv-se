---
title: Om beräkning av standardkostnad
description: I standardkostnadssystemet fastställs styckkostnaden i lagret utifrån en historisk eller förväntad kostnad som är rimlig.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Om beräkning av standardkostnad

Många produktionsföretag använder värderingsbasen för standardkostnad. Detta gäller också företag som utför lätt produktion, t. ex. montering och paketering. I standardkostnadssystemet fastställs styckkostnaden i lagret utifrån en historisk eller förväntad kostnad som är rimlig. På det här sättet skapas ett underlag för standardkostnaderna, eftersom tidigare och förväntade framtida kostnadsdata undersöks. Innan ett beslut fattas om att ändra de här kostnaderna förblir de frysta. Den faktiska kostnaden för att tillverka en produkt kan skilja sig från den beräknade standardkostnaden. Den faktiska kostnaden jämförs sedan med standardkostnaden för en särskild artikel och skillnaderna eller *avvikelserna* identifieras och analyseras för den ekonomiska styrningen.  

Standardkostnader kan bibehållas för artiklar som fylls i via inköp, montering och produktion. För varje återanskaffning kan standardkostnader bestå av följande delar.  

|Återanskaffningssystem|Standardkostnadselement|  
|--------------------------|----------------------------|  
|**Inköp**|Inköpskostnad för varor och material och materialkostnad, om det behövs.|  
|**Montering**|Inköpskostnad för material, direkt eller fast arbetskostnad och omkostnad.|  
|**Prod.order**|Inköpskostnad för material, arbetskostnad, underleverantörskostnad och omkostnad.|  

## Ställa in standardkostnader

Eftersom standardkostnaden för en producerad eller monterad artikel kan innehålla flera kostnadsslag måste en standardkostnad utarbetas för alla följande kostnadsslag: materialkostnader, kapacitetskostnader (arbete) och leveratörskostnader (inköpskostnader och overheadkostnader).  

Redovisningen i ett produktionsföretag som använder standardkostnadskalkylering består av:  

- Att uppskatta en standardkostnad för en färdig artikel samt att ställa in den på artikelkortet.  
- Att registrera och fördela den faktiska kostnaden för de viktigaste kostnadsslagen samt att redovisa avvikelser.  

Alla komponentkostnader måste räknas samman när den direkta kostnaden för en färdig artikel ska bestämmas. En monterad eller en tillverkad artikel kan bestå av halvfabrikat, som också består av flera komponenter.  

Följande viktiga kostnadselement utgör den totala inköpskostnaden för en färdig och bearbetad artikel:  

- Materialkostnader.  
- Kapacitetskostnad.  
- Underleverantörskostnader endast för den producerade artikeln.  

### Materialkostnader

Materialkostnaderna är kostnader som är kopplade till detaljmontage och inköpt råmaterial. Materialkostnaden kan bestå av kostnadsslag för både inköpskostnad och indirekt kostnad.  

- Inköpskostnaden för materialet utgörs av ett fakturerat belopp för inköpt råmaterial eller av produktionskostnaden för ett detaljmontage.  
- Den indirekta kostnaden för materialet eller *overheadkostnaden* kan t. ex. utgöras av lagerhållningskostnaden för den färdiga artikeln när den har tillverkats.  

Inställningen av materialkostnaden för inköpta artiklar, som påverkar inköpskostnad och indirekt kostnad, beror på den värderingsprincip du har valt för den aktuella artikeln. Du kan skapa kostnadsinformation för varje värderingsprincip på artikelkortet. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

Kassationskostnaden (endast produktion) är ytterligare en faktor att beakta när du beräknar den totala materialkostnaden. När en viss mängd med råmaterial kasseras när du monterar eller tillverkar en artikel brukar komponentkvantiteten som krävs för att tillverka denna artikel öka. Detta ökar materialkostnaden för komponenterna som förbrukas vid tillverkningen av en struktur. Du ställer in kassationskostnad för material i produktionsstrukturen eller produktionsverksamhetsföljden.  

Materialkostnaden för en tillverkad artikel kan visas på två sätt som motsvarar följande standardsätt för kostnadsberäkning.  

|Kostnadsberäkningsbas|Materialkostnadsberäkning|  
|----------------------------|-------------------------------|  
|En nivå|Den producerade artikeln är lika med totalkostnaden för alla inköpta eller detaljmonterade artiklar i artikelns produktionsstruktur.|  
|En nivå eller flera nivåer|Producerad artikel är summan av materialkostnaden för alla delmontage i den artikelns struktur och kostnaden för alla inköpta artiklar i den artikelns produktionsstruktur.|  

### Kapacitetskostnader

Kapacitetskostnaderna är kostnader som är kopplade till interna kostnader för arbetskraft och maskiner. Du måste lägga upp dessa kostnader för varje resurs (i monteringshanteringen) och arbete eller maskingrupp i verksamhetsföljden (i produktion). På samma sätt som med materialkostnaderna kan du identifiera kostnadsslag för kapacitetskostnaden, vad beträffar både inköpskostnaden och den indirekta kostnaden. Inköpskostnaden för en produktionsgrupp kan t.ex. vara "verkstadskostnaden" som har skapats för en särskild uppgift. Den indirekta kostnaden för en produktionsgrupp kan utgöras av allmänna kostnader för fabriken, t. ex. belysning, uppvärmning o.s.v. På liknande sätt som med materialkostnaderna kan kapacitetsoverhead uttryckas i form av en procentsats för den indirekta kostnaden eller en fast overheadkostnad.  

Inställningen av kapacitetskostnaderna för monterade artiklar består av följande delar:  

- Inköpskostnad och indirekt styckkostnad för resursen.  
- Fast eller direkt resursförbrukningstyp.  

Inställningen av kapacitetskostnaderna för producerade artiklar består av följande delar:  

- Inköpskostnad och indirekt styckkostnad för maskin- eller produktionsgruppen.  
- Inställning av tid och partistorlek.  

Om en standardinställd kapacitetskostnad ska kunna beräknas måste du fastställa standardinställda tidskostnader som behövs till operationerna i maskin- och produktionsgrupperna. Den totala tiden för att slutföra en operation består vanligtvis av omställningstiden, bearbetningstiden och av väntetiden och transporttiden.  

Du ställer in kostnaderna för varje tidstyp för varje maskin-/produktionsgrupp i enskilda verksamhetsföljder.  

> [!NOTE]  
>  Kostnaderna för bearbetningstiden gäller för varje enskild tillverkad artikelenhet och att kostnaderna för omställningstiden gäller för varje enskilt parti. Därför måste omställningstiden i verksamhetsföljden fördelas proportionellt över partistorleken för varje operation. Partistorleken anges i motsvarande fält på snabbfliken **Återanskaffning** på sidan **Artikelkort**.  

För att ange omställningstid i verksamhetsföljden i planeringssyfte, men inte inkludera den här kostnaden i den standardinställda kostnadsberäkningen avmarkerar du fältet **Kostnad inkl. omst.tid** på sidan **Produktionsinställningar**.  

På En-nivå-basis är detta den arbetskostnad som krävs för att producera den färdiga produktionsartikeln och anges på produktionsartikelns verksamhetsföljd. På en fler-nivå-basis är den kapacitet som har angetts för varje enskild tillverkad artikel som ingår i den överordnade artikelns struktur.  

### Underleverantörskostnader

Underleverantörskostnaderna är kostnader som är kopplade till tjänster från företagets fristående leverantörer eller underleverantörer. På liknande sätt som med material- och kapacitetskostnaderna kan underleverantörskostnaderna bestå av både inköpskostnad och overheadkostnad. Inköpskostnaden för legotillverkningen utgörs av den faktiska avgiften per enhet för de erhållna tjänsterna. Overheadkostnaden för legotillverkningen kan t. ex. vara frakt- och hanteringskostnader som företaget ådrog sig vid en legotillverkningsorder.  

Eftersom legotillverkning är en utlagd kapacitet ställs kostnaden för legotillverkningstjänsterna (inköpskostnad och indirekt kostnad) in för produktionsgruppkortet som motsvarar legotillverkningsoperationen.  

## Uppdatera standardkostnader

Använd funktionen från artikelkortet för att uppdatera eller beräkna standardkostnaden för monteringsartiklar.  

Processen för att uppdatera eller att beräkna standardkostnader består vanligtvis av följande uppgifter:  

1.  Uppdatera kostnader på komponent- och kapacitetsnivå. Mer information finns i batch-jobben **Föreslå artikelstandardkostnad** och **föreslå kapacitet standardkostnad**.  
2.  Konsolidera och summera komponent- och kapacitetskostnader för att beräkna den totala monterings- eller produktionskostnaden för artiklarna. Mer information finns i [Beräkna standardkostnaden för en monteringsartikel](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Använda standardkostnaderna som anges när du kör de föregående batch-jobben. Standardkostnaderna börjar inte gälla förrän de implementeras. Använd batch-jobbet **Implementera ändringar av standardkostnad**, som uppdaterar ändringarna av standardkostnaden för artiklar med de i tabellen Standardkostnadsformulär.  
4.  Implementera ändringarna för att uppdatera fältet **Styckkostnad** för artikelkortet och utföra lagerutvärderingen. Mer information finns i [Omvärdera lager](inventory-how-revalue-inventory.md).

## Använda batch-jobb för att uppdatera standardkostnader
I följande avsnitt beskrivs de batch-jobb som du kan använda för att uppdatera standardkostnader.
### Föreslå artikelstandardkostnad

 Skapar förslag för ändring av kostnader och kostnadsandelar för standardkostnader på artikelkortet. När batch-jobbet är klart visas resultatet i fönstret Standardkostnadsförslag.

> [!NOTE]  
> Det här batchjobbet används endast för inköpta artiklar. Om du vill uppdatera en artikel med en produktionsstruktur eller monteringsstruktur måste du först fylla i formuläret med alla komponenterna och sedan köra batch-jobbet Uppsummerad standardkostnad.

Det här batch-jobbet skapar bara förslag. De föreslagna ändringarna införs inte. Om du är nöjd med förslagen och vill implementera dem, det vill säga uppdatera dem på artikelkorten och infoga dem i omvärderingsjournalen, välj sedan Implementera standardkostnadsändringar i fönstret Standardkostnadskalkylblad.
#### Alternativ

**Standardkostnad**: Ange den justeringsfaktor som ska användas vid uppdateringen av standardkostnaden. Du kan också välja en avrundningsmetod för den nya standardkostnaden. Du måste fylla i fältet med en decimal för den procentuella ökningen, till exempel 1,1.

**Indirekt kostnad %**: Ange den justeringsfaktor som ska användas vid uppdateringen av indirekt kostnad %. Du kan också välja en avrundningsmetod för den nya indirekt kostnad %. Du måste fylla i fältet med en decimal för den procentuella ökningen, till exempel 1,1.

**Overheadkostnad**: Ange den justeringsfaktor som ska användas vid uppdateringen av overheadkostnaden. Du kan också välja en avrundningsmetod för den nya overheadkostnaden. Du måste fylla i fältet med en decimal för den procentuella ökningen, till exempel 1,1.

### Föreslå prod./maskin std.kostnad

Skapar förslag för ändring av kostnader och kostnadsandelar för standardkostnader på produktionsgrupper, maskingrupper eller resurskort. När batch-jobbet är klart visas resultatet i fönstret **Standardkostnadsförslag**.

Det här batch-jobbet skapar bara förslag. De föreslagna ändringarna införs inte. Om du är nöjd med förslagen och vill implementera dem, det vill säga uppdatera dem på arbets/maskingrupper och resurskort och infoga dem i fönstret Omvärderingsjournal och välj sedan **Implementera standardkostnadsändringar** i fönstret **Standardkostnadsformulär**.

När du har kört batchjobbet och vill visa effekten på produktionen eller monteringsavdelningar, kör du batchjobbet **Uppsummerad standardkostnad** för att uppdatera standardkostnader på arbetsplatser, maskincenter, monteringsresurser, produktionsstycklistor och monteringsstycklistor.
#### Alternativ
**Standardkostnad**: Ange den justeringsfaktor som ska användas vid uppdateringen av standardkostnaden. Du kan också välja en **avrundningsmetod** för den nya standardkostnaden. Du måste fylla i fältet med en decimal för den procentuella ökningen, till exempel 1,1.

**Indirekt kostnad %**: Ange den justeringsfaktor som ska användas vid uppdateringen av indirekt kostnad %. Du kan också välja en avrundningsmetod för den nya indirekt kostnad %. Du måste fylla i fältet med en decimal för den procentuella ökningen, till exempel 1,1.

**Overheadkostnad**: Ange den justeringsfaktor som ska användas vid uppdateringen av overheadkostnaden. Du kan också välja en avrundningsmetod för den nya overheadkostnaden. Du måste fylla i fältet med en decimal för den procentuella ökningen, till exempel 1,1.

### Bokför lagerkostnad i redov.

 Registrera antals- och värdeändringar i lagret i lagertransaktionerna och värdetransaktionerna när du bokför artikeltransaktioner, t.ex. försäljningsutleveranser eller inköpsinleveranser.

Om du inte har markerat kryssrutan **Automatisk kostnadsbokföring** i fönstret **Lagerinställningar** registreras inte lagerkostnader dynamiskt i redovisningen och kostnad för sålda varor beräknas inte i samband med en försäljning. Därför måste du bokföra detta i redovisningen manuellt genom att köra batch-jobbet **Bokför lagerkostnad i redov.** för att uppdatera redovisningen och eventuellt att skriva ut en rapport över de värdetransaktioner som bokförs.

Batch-jobbet använder värdetransaktioner som bas. För att beräkna värdet som ska bokföras används skillnaden mellan fältet **Kost.belopp (aktuellt)** och fältet **Kostnad bokförd i redov.** i värdetransaktionerna. Om du markerat kryssrutan **Förväntad kost.bokf. i redov.** i fönstret **Lagerinställningar** visar batch-jobbet även skillnaden mellan fälten **Kost.belopp (förväntat)** och **Förv. kost. bokf i red.** till interimskonton i redovisningen.

> [!NOTE]
> Om du inte har markerat kryssrutan **Förväntad kost.bokf. i redov.** i fönstret **Lagerinställningar**, sedan kommer den sista delen av rapporten att lista värdeposter som hoppas över eftersom de representerar förväntade kostnader.

> [!NOTE] 
> Om fel som involverar dimensioner eller dimensionsinställning påträffas i batchjobbet åsidosätts felet och transaktionen bokförs i redovisningen med hjälp av dimensionerna i värdetransaktionen.

Om du vill vara säker på att inga fel påträffas av batch-jobbet kan du köra rapporten **Bokför lagerkostnad i redovisning – Test** för att se alla fel som du kan hitta. Du kan då korrigera felen och köra batchjobbet **Bokför lagerkostnad i redov.** med vetskapen att alla transaktioner behandlas.
 
> [!IMPORTANT]  
> Innan du använder det här batch-jobbet kan du köra batch-jobbet **Justera kostn. – artikeltrans**. När du kör det här batch-jobbet uppdateras kostnaderna du bokför i redovisningen.
#### Alternativ

|Alternativ  |Description  |
|--------------|---------|
|**Bokföringsmetod**|Med hjälp av batch-jobbet kan du antingen bokföra lagervärde till redovisningen per bokföringsmall eller per bokförd transaktion. Om du bokför per transaktion kan du få en detaljerad specifikation över hur lagret påverkar redovisningen, men du får även ett stort antal redovisningsposter. Om du bokför per bokföringsmall skapas en generell redovisningstransaktion av batch-jobbet för varje kombination av bokföringsdatum och bokföringsmall. Det innebär att en redovisningspost skapas för varje kombination av bokföringsdatum, generell rörelsebokföringsmall, generell produktbokföringsmall, lagerbokföringsmall och lagerställekod. Dessutom skapas separata redovisningstransaktioner för kostnader med olika tecken.|
|**Verifikationsnr**|I det här fältet kan du skriva in ett verifikationsnummer om du har valt alternativet Bokför per lagerbokföringsmall. Verifikationsnumret visas på bokförda transaktioner.|
|**Bokför**|Markera det här fältet om du vill bokföra automatiskt i redovisningen via batchjobbet. Om du väljer att inte bokföra lagerkostnaden i redovisningen kommer batch-jobbet bara att skriva ut en testrapport som visar värden som kan bokföras i redovisningen och på rapporten kommer det att stå: **Testrapport (inte bokförd)**.|

### Uppsummerad standardkostnad

Summerar standardkostnaden för monterade och tillverkade artiklar. Dessa påverkas av standardkostnadsändringen för komponenterna som föreslås för batch-jobbet **Föreslå artikelstandardkostnad**. Dessutom påverkas de av förändringen av standardkostnad av produktionskapacitet och monteringsresurser som föreslås av batch-jobbet **Föreslå prod./maskin std.kostnad**.

När du har kört någon av (eller båda) dessa batchjobb och du summerar, kommer alla ändringar av standardkostnader i formuläret att infogas i tillhörande produktions- och monteringsstrukturer, och kostnaderna används på varje strukturnivå.

> [!NOTE] 
> Den här funktionen summerar bara standardkostnader på artikelkort, inte på Lagerställeenhet kort.

Det här batch-jobbet skapar bara förslag. De föreslagna ändringarna införs inte. Om du är nöjd med förslagen och vill använda dem, det vill säga uppdatera dem på artikelkorten och infoga dem i fönstret **omvärderingsjournal**, sedan kan du använda batch-jobbet **Inför stand.kost.ändring**. Du öppnar batch-jobbet från fönstret **Standardkostnadsformulär**.
#### Alternativ

**Beräkningsdatum**: Skriv det datum som gäller för den produktionsstrukturversion du vill summera för.
 
### Inför stand.kost.ändring

Uppdaterar standardkostnadsändringarna i tabellen **Artikel** med de som finns i tabellen **Standardkostnadsformulär**. Förslagen på standardkostnadsändringar kan skapas med batch-jobbet **Föreslå artikelstandardkostnad** och/eller **Föreslå prod./maskin std.kostnad**, och de kan också ändras. Innehållen i alla fält i förändringsförslaget för standardkostnader överförs. När du implementerar ändringsförlagen för standardkostnad kan du visa dem på artikelkortet och/eller produktions-/maskingruppskorten. En omvärderingsjournal skapas också så att du kan uppdatera värdet på det befintliga lagret.
#### Alternativ

**Bokföringsdatum**: Skriv det datum som omvärderingen ska ske.

**Dokumentnr**: Skriv numret för omvärderingsjournalraderna. Om en nummerserie har lagts upp för artikeljournalnamnet, följer dokumentnumret de redovisningstransaktioner som skapats vid bokföringen av omvärderingsjournalen. Annars kan du ange ett nummer manuellt.

**Artikeljournalmall**: Skriv namnet på omvärderingsjournalmallen.

**Artikeljournalnamn**: Skriv namnet på den faktiska omvärderingsjournalen

Välj **OK** när du vill starta batchjobbet. Om du inte vill köra batch-jobbet nu klickar du på **Avbryt** för att stänga fönstret.

## Se även

[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Uppdatera standardkostnader](finance-how-to-update-standard-costs.md)  
[Designdetaljer: Lagerkostnader](design-details-inventory-costing.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Skapa produktionsstrukturer](production-how-to-create-production-boms.md)  
[Arbeta med strukturer](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

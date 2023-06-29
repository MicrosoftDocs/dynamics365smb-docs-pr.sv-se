---
title: Definiera hur data överförs elektroniskt
description: 'Definiera hur Business Central överför data med externa filer som elektroniska dokument, bankdata, artikelkataloger m.m.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="set-up-data-exchange-definitions"></a><a name="set-up-data-exchange-definitions"></a>Skapa dataintegreringsdefinitioner

Du kan konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] för att utbyta data i specifika tabeller med data om externa filer. Om du t.ex. vill skicka och ta emot elektroniska dokument, importerar och exporterar du bankdata eller andra data, t.ex. lön och artikelkataloger. Läs mer i [Utbyta data elektroniskt](across-data-exchange.md).  

För att skapa en datautbytesdefiniera för en datafil eller en dataström kan du använda det relaterade XML-schemat för att definiera vilka dataelement som du vill inkludera på snabbfliken **Kolumndefinitioner**. Se steg 6 i avsnittet [Så här beskriver du formateringen av rader och kolumner i filen](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Läs mer i [Använda XML-uppställningar för att förbereda datautbytesdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Vanligtvis skapar du skapar datautbytesdefinitioner på sidan **Datautbytesdefinition**. För att uppdatera valutakurser går det emellertid snabbare att använda en valutakursservice. Läs mer i [Uppdatera valutakurser](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Om filen som konverteras är i XML-format ska termen *"kolumn"* i den här artikeln tolkas som ett *"XML-element som innehåller data"*.  

I den här artikeln beskrivs följande procedurer:  

* Skapa en datautbytesdefinition.
* Exportera en datautbytesdefinition som en XML-fil som andra ska använda.
* Importera en XML-fil för en befintlig datautbytesdefinition.

## <a name="create-a-data-exchange-definition"></a><a name="create-a-data-exchange-definition"></a>Skapa en datautbytesdefinition

Två uppgifter måste utföras för att skapa en definition för datautbyte:  

1. Sidan **datautbytesdefinitioner** beskriver layouten för rader och kolumner i filen. Läs mer i avsnittet [Beskriva formateringen av rader och kolumner i filen](#formatlinescolumns).  
2. Sidan **Datautbytesmappning** mappar kolumner i datafilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i avsnittet [Mappa kolumner i datafilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name=formatlinescolumns></a>Beskriva formateringen av rader och kolumner i filen

1. Välj ![glödlampan som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Datautbytesdefinition** och välj relaterad länk.  
2. Välj åtgärden **Ny**.  
3. På snabbfliken **Allmänt** beskriver du definitionen för datautbytet och datafiltypen genom att fylla i fälten som beskrivs i följande tabell.  

    |Fält|Definition|  
    |---------------------------------|---------------------------------------|  
    |**Kod**|Registrera en kod som identifierar definitionen för datautbyte.|  
    |**Namn**|Ange ett namn på definitionen för datautbyte.|  
    |**Filtyp**|Ange vilken typ av fil datautbytesdefinitionen används för. Du kan välja mellan fyra filtyper:<br /><br /> -   **XML**: Överlappande strängar med innehåll och pålägg omgivna av taggar som anger funktionen.<br />-   **Variabel text**: Poster har variabel längd och avgränsas av ett tecken, som ett kommatecken eller semikolon\-, även kallad *avgränsad fil*.<br />-   **Fas text**: Poster har samma längd, med hjälp av utfyllnadstecken, och varje post är på en separat rad, även kallad *fil med fast bredd*.<br />- **Json**: överlappande innehållsträngar i JavaScript.|  
    |**Radtyp**|Ange vilken typ av affärsaktivitet definitionen för datautbyte används till, till exempel **Betalningsexport**.|  
    |**Kodenhet för datahantering**|Ange den kodenhet som överför data till och från tabeller i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Kodenhet för validering**|Ange den kodenhet som används för att verifiera data mot fördefinierade affärsregler.|  
    |**Kodenhet för läsning/skrivning**|Ange den kodenhet som behandlar importerade data före mappningen och exporterade data efter mappningen.|  
    |**Läsning/skrivning XMLport**|Anger den XMLport genom vilken en importerad datafil eller tjänst skickas in före mappning och genom vilken exporterade data skickas ut när de skrivs till en datafil eller tjänst efter mappning.|  
    |**Kodenhet för hantering av ext. data**|Ange den kodenhet som överför externa data in i och ut ur ramverket för datautbyte.|  
    |**Kodenhet för användarfeedback**|Ange kodenheten för olika slags rensningar efter mappningen, till exempel för markering av rader som exporterade och radering av temporära poster.|  
    |**Filkodning**|Ange kodningen för filen. **Obs:** Det här fältet är endast relevant för import.|  
    |**Kolumnavgränsare**|Ange hur kolumner i datafilen avskiljs, om filen är av typen **Variabel text**.|  
    |**Rubrikrader**|Ange hur många rubrikrader som finns i filen.<br /><br /> Denna inställning säkerställer att huvuddata inte importeras. **Obs:** Det här fältet är endast relevant för import.|  
    |**Rubriktagg**|Om en huvudrad finns på flera positioner i filen anger du den första kolumnens text på huvudraden.<br /><br /> Detta alternativ säkerställer att huvuddata inte importeras. **Obs:** Det här fältet är endast relevant för import.|  
    |**Sidfotstagg**|Om en sidfotsrad finns på flera positioner i filen anger du den första kolumnens text på sidfotsraden.<br /><br /> Detta alternativ säkerställer att sidfotsdata inte importeras. **Obs:** Det här fältet är endast relevant för import.|  

   > [!TIP]
   > Om du vill se vilka codeunits som Microsoft använder i befintliga definitioner för standardprodukten, granska de tre fälten för **Codeunit** på sidan **Fältmappning** under snabbfliken **Allmänt** för varje definition.  

4. På snabbfliken **Raddefinitioner** beskriver du formateringen av rader i datafilen genom att fylla i fälten som beskrivs i följande tabell.  

    > [!NOTE]  
    > För import av bankutdrag skapar du endast en rad för den enda formatet på kontoutdragsfilen som du vill importera.  
    >
    > För export av betalningar kan du skapa en rad för varje betalningstyp som du vill exportera. I så fall visar snabbfliken **Kolumndefinitioner** olika kolumner för varje betalningstyp.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Radtyp**|Anger typen av rad i filen.|  
    |**Kod**|Ange en kod som identifierar raden i filen.|  
    |**Namn**|Ange ett namn som beskriver raden i filen.|  
    |**Kolumnantal**|Ange hur många kolumner raden i datafilen har. **Obs:** Det här fältet är endast relevant för import.|  
    |**Dataradstagg**|Ange positionen i det relaterade XML-schemat för element som representerar datafilens huvudtransaktion. **Obs:** Det här fältet är endast relevant för import.|  
    |**Namnområde**|Ange namnområdet som förväntas i filen för att aktivera du namnområdevalidering. Du kan låta fältet vara tomt om du inte vill aktivera validering för namnområdet.|  
    |**Överordnad kod**|Ange radens överordnade, som visas i fältet **Kod** i de fall då konfigurationen av dataintegrationen gäller filer med överordnade och underordnade transaktioner, till exempel ett dokumenthuvud och rader.

5. Upprepa moment 4 för att skapa en rad för varje typ av fildata som du vill exportera.  

     Sedan beskriver du formateringen av kolumner i datafilen genom att fylla i fälten på snabbfliken **Kolumndefinitioner** så som beskrivs i följande tabell. Du kan använda strukturfilen, till exempel en .xsd-fil, för att datafilen ska autofylla snabbfliken med de relevanta elementen. Läs mer i [Använda XML-uppställningar för att förbereda datautbytesdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Välj åtgärden **Hämta filstruktur** på snabbfliken **Kolumndefinitioner**.  
7. På sidan **Hämta filstruktur** markerar du den relaterade strukturfilen och väljer sedan **OK**. Raderna på snabbfliken **Kolumndefinitioner** fylls i enligt strukturen i datafilen.  
8. Redigera eller fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Kolumndefinitioner**.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kolumnnr**|Ange numret som återspeglar kolumnens position på raden i filen.<br /><br /> För XML-filer anger du numret som återspeglar typen av element i filen som innehåller data.|  
    |**Namn**|Ange namnet på kolumnen.<br /><br /> För XML-filer anger du de pålägg som markerar att data ska utbytas.|  
    |**Datatyp**|Ange om data som ska utbytas är av typen **Text**, **Datum** eller **Decimal**.|  
    |**Dataformat**|Ange formatet för data, om det finns något. Till exempel **MM-dd-åååå** om datatypen är **Datum**. **Obs:** Ange dataformatet enligt [!INCLUDE[prod_short](includes/prod_short.md)] för export. Ange dataformatet enligt .NET Framework för import. Läs mer i [Standarddatum och tidsformatsträngar](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Dataformateringskultur**|Ange det regionala dataformatet, om sådant finns. Exempelvis **en-US** om datatypen är **Decimal** för att säkerställa att komma används som tusentalsseparator enligt USA-formatet. Läs mer i [Standarddatum och tidsformatsträngar](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Obs:** Det här fältet är endast relevant för import.|  
    |**Längd**|Ange längden på raden med fast bredd som innehåller kolumnen om datafilen är av typen **Fast Text**.|  
    |**Beskrivning**|Anger en beskrivning av kolumnen för informationsändamål.|  
    |**Sökväg**|Ange positionen för elementen i det relaterade XML-schemat.|  
    |**Identifierare för negativt tecken**|Ange värdet som används i datafilen för att identifiera negativa belopp, i datafiler som inte kan innehålla negativt tecken. Detta ID används sedan för att återföra de identifierade beloppen till negativt tecken vid import. **Obs:** Det här fältet är endast relevant för import.|  
    |**Konstant**|Ange data som du vill exportera i den här kolumnen, till exempel ytterligare information om betalningstypen. **Obs:** Fältet är endast relevant för export.|  
    |**Textutfyllnad krävs**|Ange att data måste innehålla textutfyllnad.|  
    |**Utfyllnadstecken**|Ange textens utfyllnadstecken.|  
    |**Justering**|Ange om kolumnjusteringen är vänster eller höger.|  

9. Upprepa moment 8 för varje kolumn eller XML-element i datafilen som har data som du vill att utbyta med [!INCLUDE[prod_short](includes/prod_short.md)].  

Nästa steget i att skapa en definition för datautbyte är att avgöra vilka kolumner eller XML-element i datafilöversikten som ska mappas till vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Den specifika mappningen beror på affärsavsikten med datafilen som ska utbytas och på lokala varianter. Även SEPA-bankstandarden har lokala varianter. [!INCLUDE[prod_short](includes/prod_short.md)] stöder import av förinstallerade bankutdragsfiler för SEPA CAMT\-\-\-. Det representeras av koden för posten med definition av datautbyte **SEPA CAMT** på sidan **datautbytesdefinitioner**. Information om specifik fältmappning för detta SEPA CAMT-stöd finns i [fältmappning när du importerar SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name=mapfields></a>Mappa kolumner i datafilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Ibland är värdena i de fält som du vill mappa olika. I ett företagsprogram är till exempel språkkoden för USA "U.S.", men i det andra är det "US". Det innebär att du måste omvandla värdet när du utbyter data. Detta sker genom omvandlingsregler som du definierar för fälten. Läs mer i [Omvandlingsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Från och med utgivningscykel 2 år 2022 kan du även gruppera efter valfritt fält. Använd nyckelindexet för att sortera resultat och de nya omvandlingstyperna **Avrundning** och **Fältsökning**.

1. På snabbfliken **Raddefinitioner** markerar du raden som du vill mappa kolumner till fält för och väljer sedan **Fältmappning**. Sidan **Datautbytesmappning** öppnas.  
2. På snabbfliken **Allmänt** anger du mappningskonfigurationen genom att fylla i fälten enligit beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Tabell-ID**|Ange tabellen som innehåller fälten som data utbyts till eller från enligt mappningen.|  
    |**Använd som cachelagringstabell**|Ange att tabellen som du väljer i fältet **Tabell-ID** är en cachelagringstabell där importerade data lagras innan de mappas till måltabellen.<br /><br /> Du kan använda den här cachelagringstabellen när definitionen för datautbyte används för att importera och konvertera elektroniska dokument, till exempel från leverantörsfakturor till inköpsfakturor i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Utbyta data elektroniskt](across-data-exchange.md).|  
    |**Namn**|Ange ett namn på mapningsinställningen.|  
    |**Nyckelindex**|Ange nyckelindexet som ska användas för att sortera källposterna före export.|
    |**Förmappningskodenhet**|Ange den kodenhet som förbereder mappningen mellan fält i [!INCLUDE[prod_short](includes/prod_short.md)] och externa data.|  
    |**Mappningskodenhet**|Ange den kodenhet som används för att mappa specifika kolumner eller XML-dataelement till fält i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Eftermappningskodenhet**|Ange den kodenhet som slutför mappningen mellan fält i [!INCLUDE[prod_short](includes/prod_short.md)] och externa data. **OBS!**  När du använder tilläggsfunktionen AMC Banking 365 Fundamentals konverterar kodenheten exporterade data från [!INCLUDE[prod_short](includes/prod_short.md)] till ett standardformat som är redo för export. För import konverterar kodenheten externa data till ett format som är klart att importera till [!INCLUDE[prod_short](includes/prod_short.md)].|
3. På snabbfliken **Fältmappning** anger du vilka kolumner som mappas till vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)] genom att fylla i fälten enligt beskrivningen i följande tabeller, beroende på om fältet **Använd som cachelagringstabell** var aktivt eller inte.  
   * Med **Använd som cachelagringstabell** av:

     |Fält|Description|  
     |--------------------------------- |---------------------------------------|  
     |**Kolumnnr**|Ange vilken kolumn i datafilen som du vill definiera en översikt för.<br /><br /> Du kan bara välja kolumner som representeras av rader på snabbfliken **Kolumndefinitioner** på sidan **datautbytesdefinition**.|
     |**Kolumnrubrik**|Ange rubriken för kolumnen i den externa filen som mappas till fältet i fältet **Måltabell-ID**, när du använder en cachelagringstabell för dataimport.|
     |**Fält-ID**|Ange vilka fält kolumnen i fältet **Kolumnnr.** mappas till.<br /><br /> Du kan bara välja från fält som finns i tabellen som du har angett i fältet **Tabell-ID** på snabbfliken **Allmänt**.|
     |**Fältrubrik**|Ange rubriken för fältet i den externa filen som mappas till fältet i fältet **Måltabell-ID**, när du använder en cachelagringstabell för dataimport.|
     |**Valfri**|Ange om mappningen ska hoppas över när fältet är tomt. Om du inte väljer det här alternativet så inträffar ett exportfel om fältet är tomt.|  
     |**Omvandlingsregel**|Ange regeln för att omvandla importerad text till ett värde som stöds innan det kan mappas till det angivna fältet. När du väljer ett värde i det här fältet anges samma värde i fältet **Omvandlingsregel** i **Mappningsbuff. för datautbytesfält** och vice versa. Mer information om tillgängliga omvandlingsregler som kan användas finns i nästa avsnitt.|
     |**Skriv över värde**|Ange att det aktuella värdet skrivs över av ett nytt värde.|
     |**Prioritet**|Ange i vilken ordning fältmappningarna måste bearbetas. Fältmappningen med högst prioritetsnummer kommer att bearbetas först.|
     |**Multiplikator**|Ange en multiplikator som ska användas på numeriska data, inklusive negativa värden.|

   * Med **Använd som cachelagringstabell** aktiv:

     |Fält|Description|  
     |---------------------------------|---------------------------------------|  
     |**Kolumnnr**|Ange vilken kolumn i datafilen som du vill definiera en översikt för.<br /><br /> Du kan bara välja kolumner som representeras av rader på snabbfliken **Kolumndefinitioner** på sidan **datautbytesdefinition**.|
     |**Kolumnrubrik**|Ange rubriken för kolumnen i den externa filen som mappas till fältet i fältet **Måltabell-ID**, när du använder en cachelagringstabell för dataimport.|
     |**Måltabell-ID**|Ange tabellen som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|
     |**Tabellrubrik**|Ange namnet på tabellen i fältet **Måltabell-ID** som är den tabell som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|
     |**Målfält-ID**|Ange fältet i måltabellen som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|
     |**Fältrubrik**|Ange namnet på fältet i måltabellen som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|
     |**Validera endast**|Ange att mappning av element till fält inte används för att konvertera data, utan endast för att verifiera data.|
     |**Omvandlingsregel**|Ange regeln för att omvandla importerad text till ett värde som stöds innan det kan mappas till det angivna fältet. När du väljer ett värde i det här fältet anges samma värde i fältet **Omvandlingsregel** i **Mappningsbuff. för datautbytesfält** och vice versa. Mer information om tillgängliga omvandlingsregler som kan användas finns i nästa avsnitt.|
     |**Prioritet**|Ange i vilken ordning fältmappningarna måste bearbetas. Fältmappningen med högst prioritetsnummer kommer att bearbetas först.|

4. På snabbfliken **Fältgruppering** anger du regler som du vill använda för att gruppera fälten när du skapar filen genom att fylla i fälten enligt beskrivningen i följande tabell.  

     |Fält|Description|  
     |--------------------------------- |---------------------------------------|  
     |**Fält-ID**|Ange numret på fältet i den externa filen som används för gruppering och detta fält måste anges av användare.|
     |**Fältrubrik**|Ange rubriken på fältet i den externa filen som används för gruppering.|

## <a name="transformation-rules"></a><a name="transformation-rules"></a>Omvandlingsregler

Om värdena i fälten som du mappar skiljer sig åt, måste du använda omvandlingsregler för datautbytesdefinitioner för att göra dem likadana. Du definierar omvandlingsregler för datautbytesdefinitioner genom att öppna en befintlig definition (eller skapa en ny definition) och sedan, på snabbfliken **Raddefinitioner**, välja **Hantera**och sedan **Fältmappning**. Fördefinierade regler tillhandahålls, men du kan också skapa egna. I följande register beskrivs de typer av omvandlingar som du kan utföra.

|Alternativ|Beskrivning|
|---------|---------|
|**Versaler**|Skriv alla bokstäver i versaler.|
|**Gemener**|Skriv alla bokstäver som gemener.|
|**Huvudärende**|Skriv första bokstaven i varje ord i versaler.|
|**Trimma**|Ta bort tomma mellanslag före och efter värdet.|
|**Delsträng**|Omvandla en viss del av ett värde. Om du vill ange var du vill starta omvandlingen väljer du antingen **Startposition** eller **Starttext**. Startpositionen är ett tal som representerar det första tecknet som ska omvandlas. Starttexten är bokstaven omedelbart före bokstaven som ska ersättas. Om du vill börja med den första bokstaven i värdet använder du en startposition i stället. Om du vill ange var du vill stoppa omvandlingen väljer du aningen **Längd**, som är antalet tecken som ska ersättas, eller den **avslutande texten**, som är tecknet direkt efter det sista tecknet som ska omvandlas.|
|**Byt ut**|Hitta ett värde och ersätt det med ett annat. Denna omvandling är användbar för att ersätta enkla värden, till exempel ett visst ord.|
|**Reguljärt uttryck – Ersätt**|Använd ett reguljärt uttryck som en del av en sök-och ersätt-åtgärd. Denna omvandling är användbar för att ersätta flera, eller mer komplexa, värden.|
|**Ta bort icke-alfanumeriska tecken**|Ta bort tecken som inte är bokstäver eller siffror, till exempel symboler eller specialtecken.|
|**Datumformatering**|Ange hur datum ska visas. Du kan till exempel omvandla DD-MM-ÅÅÅÅ till ÅÅÅÅ-MM-DD.|
|**Decimalformat**|Definiera regler för decimalplacering och avrundningsprecision.|
|**Matchning – reguljärt uttryck**|Använd ett reguljärt uttryck för att hitta ett eller flera värden. Denna regel liknar alternativen för **Delsträng** och **Reguljärt uttryck – Byt ut**.|
|**Anpassat**|Denna omvandlingsregel är ett avancerat alternativ som kräver hjälp från en utvecklare. Det möjliggör en integreringshändelse som du kan prenumerera på om du vill använda din egen omvandlingskod. Om du är utvecklare och vill använda det här alternativet läser du avsnittet nedan.|
|**Format för datum och tid**|Definiera hur du vill visa aktuellt datum och tid på dagen.|
|**Fältsökning**|Använd fält från olika tabeller. Du måste följa stegen för att använda den. Använd först **tabell-ID** för att ange ID för tabellen som innehåller posten för fältsökningen. Sedan i fältet **Källfält-ID** anger du ID för fältet som innehåller posten för fältsökningen. Slutligen i fältet **Målfält-ID** anger du ID för fältet för att hitta posten för fältsökningen. Du kan också använda **Regel för fältsökning** för att ange typen av fältsökning. För fältet **Mål** används värdet från **Målfält-ID** även om det är tomt. För fältet **Ursprungligt om mål är tomt** används det ursprungliga värdet om målet är tomt.|
|**Avrunda**|Avrunda värdet i det här fältet med hjälp av några ytterligare regler. I fältet **precision** anger du i första hand en avrundningsprecision. Sedan i fältet **riktning** anger du sedan avrundningsriktningen.|

> [!NOTE]  
> Lär dig mer om datum- och tidsformatering på [Standardsträngar för datum- och tidsformat](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### <a name="tip-for-developers-example-of-the-custom-option"></a><a name="tip-for-developers-example-of-the-custom-option"></a>Tips för utvecklare: exempel på det anpassade alternativet

I följande exempel visas hur du implementerar din egen omvandlingskod.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

När du har definierat dina regler kan du testa dem. På snabbfliken **Test** anger du ett exempel på ett värde som du vill omvandla och kontrollerar sedan resultatet genom att välja **Uppdatera**.

## <a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a><a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Exportera en datautbytesdefinition som en XML-fil som andra ska använda

När du har skapat definitionen för datautbyte för en viss datafil kan du exportera definitionen för datautbyte som en XML-fil du kan importera. Den här uppgiften beskrivs i följande procedur.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Datautbytesdefinition** och välj relaterad länk.  
2. Välj den definition för datautbyte som du vill exportera.  
3. Välj åtgärden **Exportera datautbytesdefinition**.  
4. Spara XML-filen som representerar definitionen för datautbytet på ett lämpligt ställe.  

    Om en definition för datautbyte redan har skapats behöver du bara importera XML-filen till ramverket för datautbyte. Den här uppgiften beskrivs i följande procedur.  

## <a name="import-an-existing-data-exchange-definition"></a><a name="import-an-existing-data-exchange-definition"></a>Importera en befintlig datautbytesdefinition

1. Spara XML-filen som representerar definitionen för datautbytet på ett lämpligt ställe.  
2. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Datautbytesdefinition** och välj relaterad länk.  
3. Välj åtgärden **Importera datautbytesdefinition**.  
4. Välj filen som du har sparat i steg 1.  

## <a name="see-also"></a><a name="see-also"></a>Se även

[Konfigurera dataintegration](across-set-up-data-exchange.md)  
[Konfigurera utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Ta betalt med SEPA-postförskott](finance-collect-payments-with-sepa-direct-debit.md)  
[Göra betalningar med AMC Banking 365 Fundamentals-tillägg eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

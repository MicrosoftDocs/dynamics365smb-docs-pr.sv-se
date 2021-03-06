---
title: Definiera hur data överförs elektroniskt | Microsoft Docs
description: Använd en extern leverantör för OCR-tjänster för att omvandla PDF- eller bildfiler till elektroniska dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 58e98a2fa3e7a0d61ad6dc49ac2291a21105ddcb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774692"
---
# <a name="set-up-data-exchange-definitions"></a>Skapa dataintegreringsdefinitioner
Du kan konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] för utbyte av data i vissa tabeller mot data i externa filer, till exempel för att skicka och ta emot elektroniska dokument, importera och exportera bankdata eller övriga data som löneutbetalningar, valutakurser och artikelkataloger. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).  

Som förberedelsen för att skapa en datautbytesdefiniera för en datafil eller en dataström kan du använda det relaterade XML-schemat för att definiera vilka dataelement som du vill inkludera på snabbfliken **Kolumndefinitioner**. Se steg 6 i avsnittet [Så här beskriver du formateringen av rader och kolumner i filen](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Mer information finns i [Använda XML-scheman för att förbereda dataintegreringsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Du skapar normalt definitioner för datautbyte på sidan **datautbytesdefinitioner**. Men när du skapat en datautbytesdefinitioner för tjänsten med uppdatering av valutakurser startar du processen på den förenklade sidan **Inställning valutakursuppdatering**.  

> [!NOTE]  
>  Om filen som konverteras är i XML-format ska termen *kolumn* i det här avsnittet tolkas som ett *XML-element som innehåller data*.  

I det här avsnittet beskrivs följande procedurer:  

* Så här skapar du en definition för datautbyte  
* Så här exporterar du en definition för datautbyte som en XML-fil som andra ska använda  
* Så här importerar du en XML-fil för en befintlig definition av datautbyte  

## <a name="to-create-a-data-exchange-definition"></a>Så här skapar du en definition för datautbyte  
Två uppgifter måste utföras för att skapa en definition för datautbyte:  

1. Sidan **datautbytesdefinitioner** beskriver layouten för rader och kolumner i filen.  
2. Sidan **Datautbytesmappning** mappar kolumner i datafilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)].  

Beskrivs i följande procedurer.  

> [!TIP]
> Om du vill se vilka kodmoduler som Microsoft använder i befintliga definitioner för standardprodukten, granska de tre fälten för **Codeunit** i rubriken på sidan **Fältmappning** för varje definition.

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Så här beskriver du formateringen av rader och kolumner i filen  
1. I rutan **Sök** anger du **Definitioner för datautbyte** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. På snabbfliken **Allmänt** beskriver du definitionen för datautbytet och datafiltypen genom att fylla i fälten som beskrivs i följande tabell.  

    |Fält|Definition|  
    |---------------------------------|---------------------------------------|  
    |**Kod**|Registrera en kod som identifierar definitionen för datautbyte.|  
    |**Namn**|Ange ett namn på definitionen för datautbyte.|  
    |**Filtyp**|Ange vilken typ av fil definitionen för datautbytet används för. Du kan välja mellan fyra filtyper:<br /><br /> -   **XML**: Överlappande strängar med innehåll och pålägg omgivna av taggar som anger funktionen.<br />-   **Variabel text**: Transaktioner har variabel längd och avskiljs av ett tecken, t. ex. komma eller semikolon\-. Kallas även *avgränsad fil*.<br />-   **Fast text**: Transaktioner har samma längd, med hjälp av utfyllnadstecken, och varje transaktion uttrycks på en egen rad. Kallas även *fil med fast bredd*.<br />- **Json**: överlappande innehållsträngar i JavaScript.|  
    |**Radtyp**|Ange vilken typ av affärsaktivitet definitionen för datautbyte används till, till exempel **Betalningsexport**.|  
    |**Kodenhet för datahantering**|Ange den kodenhet som överför data till och från tabeller i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Kodenhet för validering**|Ange den kodenhet som används för att verifiera data mot fördefinierade affärsregler.|  
    |**Kodenhet för läsning/skrivning**|Ange den kodenhet som behandlar importerade data före mappningen och exporterade data efter mappningen.|  
    |**Läsning/skrivning XMLport**|Anger den XMLport genom vilken en importerad datafil eller tjänst skickas in före mappning och genom vilken exporterade data skickas ut när de skrivs till en datafil eller tjänst efter mappning.|  
    |**Kodenhet för hantering av ext. data**|Ange den kodenhet som överför externa data in i och ut ur ramverket för datautbyte.|  
    |**Kodenhet för användarfeedback**|Ange kodenheten för olika slags rensningar efter mappningen, till exempel för markering av rader som exporterade och radering av temporära poster.|  
    |**Filkodning**|Ange kodningen för filen. **Obs:**  Fältet är endast relevant för import.|  
    |**Kolumnavgränsare**|Ange hur kolumner i datafilen avskiljs, om filen är av typen **Variabel text**.|  
    |**Rubrikrader**|Ange hur många rubrikrader som finns i filen.<br /><br /> Detta säkerställer att huvuddata inte importeras. **Obs:**  Fältet är endast relevant för import.|  
    |**Rubriktagg**|Om en huvudrad finns på flera positioner i filen anger du den första kolumnens text på huvudraden.<br /><br /> Detta säkerställer att huvuddata inte importeras. **Obs:**  Fältet är endast relevant för import.|  
    |**Sidfotstagg**|Om en sidfotsrad finns på flera positioner i filen anger du den första kolumnens text på sidfotsraden.<br /><br /> Detta säkerställer att sidfotsdata inte importeras. **Obs:**  Fältet är endast relevant för import.|  

4. På snabbfliken **Raddefinitioner** beskriver du formateringen av rader i datafilen genom att fylla i fälten som beskrivs i följande tabell.  

    > [!NOTE]  
    >  För import av bankutdrag skapar du endast en rad för den enda formatet på kontoutdragsfilen som du vill importera.  
    >   
    >  För export av betalningar kan du skapa en rad för varje betalningstyp som du vill exportera. I så fall visar snabbfliken **Kolumndefinitioner** olika kolumner för varje betalningstyp.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kod**|Ange en kod som identifierar raden i filen.|  
    |**Namn**|Ange ett namn som beskriver raden i filen.|  
    |**Kolumnantal**|Ange hur många kolumner raden i datafilen har. **Obs:**  Fältet är endast relevant för import.|  
    |**Dataradstagg**|Ange positionen i det relaterade XML-schemat för element som representerar datafilens huvudtransaktion. **Obs:**  Fältet är endast relevant för import.|  
    |**Namnområde**|Ange namnområdet som förväntas i filen för att aktivera du namnområdevalidering. Du kan låta fältet vara tomt om du inte vill aktivera validering för namnområdet.|  

5. Upprepa moment 4 för att skapa en rad för varje typ av fildata som du vill exportera.  

     Sedan beskriver du formateringen av kolumner i datafilen genom att fylla i fälten på snabbfliken **Kolumndefinitioner** så som beskrivs i följande tabell. Du kan använda strukturfilen, till exempel en XSD-fil, för att datafilen ska autofylla snabbfliken med de relevanta elementen. Mer information finns i [Använda XML-scheman för att förbereda dataintegreringsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. Välj **Hämta filstruktur** på snabbfliken **Kolumndefinitioner**.  
7. På sidan **Hämta filstruktur** markerar du den relaterade strukturfilen och väljer sedan knappen **OK**. Raderna på snabbfliken **Kolumndefinitioner** fylls i enligt strukturen i datafilen.  
8. Redigera eller fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Kolumndefinitioner**.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kolumnnr**|Ange numret som återspeglar kolumnens position på raden i filen.<br /><br /> För XML-filer anger du numret som återspeglar typen av element i filen som innehåller data.|  
    |**Namn**|Ange namnet på kolumnen.<br /><br /> För XML-filer anger du de pålägg som markerar att data ska utbytas.|  
    |**Datatyp**|Ange om data som ska utbytas är av typen **Text**, **Datum** eller **Decimal**.|  
    |**Dataformat**|Ange formatet för data, om det finns något. Till exempel **MM-dd-åååå** om datatypen är **Datum**. **Obs:**  Ange dataformatet enligt [!INCLUDE[prod_short](includes/prod_short.md)] för export. Ange dataformatet enligt .NET Framework för import. Mer information finns i [Standarddatum och tidsformatsträngar](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Dataformateringskultur**|Ange kulturen för dataformatet, om det finns någon. Exempelvis **en-US** om datatypen är **Decimal** för att säkerställa att komma används som tusentalsseparator enligt USA-formatet. Mer information finns i [Standarddatum och tidsformatsträngar](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Obs:**  Fältet är endast relevant för import.|  
    |**Längd**|Ange längden på raden med fast bredd som innehåller kolumnen om datafilen är av typen **Fast Text**.|  
    |**Beskrivning**|Ange en beskrivning av kolumnen, för information.|  
    |**Sökväg**|Ange positionen för elementen i det relaterade XML-schemat.|  
    |**Identifierare för negativt tecken**|Ange värdet som används i datafilen för att identifiera negativa belopp, i datafiler som inte kan innehålla negativt tecken. Detta ID används sedan för att återföra de identifierade beloppen till negativt tecken vid import. **Obs:**  Fältet är endast relevant för import.|  
    |**Konstant**|Ange data som du vill exportera i den här kolumnen, till exempel ytterligare information om betalningstypen. **Obs:**  Fältet är endast relevant för export.|  

9. Upprepa moment 8 för varje kolumn eller XML-element i datafilen som har data som du vill att utbyta med [!INCLUDE[prod_short](includes/prod_short.md)].  

 Nästa steget i att skapa en definition för datautbyte är att avgöra vilka kolumner eller XML-element i datafilöversikten som ska mappas till vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
>  Den specifika mappningen beror på affärsavsikten med datafilen som ska utbytas och på lokala varianter. Även SEPA-bankstandarden har lokala varianter. [!INCLUDE[prod_short](includes/prod_short.md)] stöder import av förinstallerade bankutdragsfiler för SEPA CAMT\-\-\-. Det representeras av koden för posten med definition av datautbyte **SEPA CAMT** på sidan **datautbytesdefinitioner**. Information om specifik fältmappning för detta SEPA CAMT-stöd finns i [fältmappning när du importerar SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-prod_short"></a>Så här mappar du kolumner i datafilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)]  
> [!TIP]
> Ibland är värdena i de fält som du vill mappa olika. I ett företagsprogram är till exempel språkkoden för USA "USA", men i det andra är det "US". Det innebär att du måste omvandla värdet när du utbyter data. Detta sker genom omvandlingsregler som du definierar för fälten. Mer information finns i [Omvandlingsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

1. På snabbfliken **Raddefinitioner** markerar du raden som du vill mappa kolumner till fält för och väljer sedan **Fältmappning**. Sidan **Datautbytesmappning** öppnas.  
2. På snabbfliken **Allmänt** anger du mappningskonfigurationen genom att fylla i fälten enligit beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Tabell-ID**|Ange tabellen som innehåller fälten som data utbyts till eller från enligt mappningen.|  
    |**Använd som cachelagringstabell**|Ange att tabellen som du väljer i fältet **Tabell-ID** är en cachelagringstabell där importerade data lagras innan de mappas till måltabellen.<br /><br /> Du kan använda den här cachelagringstabellen när definitionen för datautbyte används för att importera och konvertera elektroniska dokument, till exempel från leverantörsfakturor till inköpsfakturor i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).|  
    |**Namn**|Ange ett namn på mapningsinställningen.|  
    |**Förmappningskodenhet**|Ange den kodenhet som förbereder mappningen mellan fält i [!INCLUDE[prod_short](includes/prod_short.md)] och externa data.|  
    |**Mappningskodenhet**|Ange den kodenhet som används för att mappa specifika kolumner eller XML-dataelement till fält i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Eftermappningskodenhet**|Ange den kodenhet som slutför mappningen mellan fält i [!INCLUDE[prod_short](includes/prod_short.md)] och externa data. **OBS!**  När du använder tilläggsfunktionen AMC Banking 365 Fundamentals konverterar kodenheten exporterade data från [!INCLUDE[prod_short](includes/prod_short.md)] till ett standardformat som är redo för export. För import konverterar kodenheten externa data till ett format som är klart att importera till [!INCLUDE[prod_short](includes/prod_short.md)].|  

3.  På Snabbfliken **Fältmappning** anger du vilka kolumner som mappas mot vilka fält i [!INCLUDE[prod_short](includes/prod_short.md)] genom att fylla i fälten som beskrivs i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kolumnnr**|Ange vilken kolumn i datafilen som du vill definiera en översikt för.<br /><br /> Du kan bara välja kolumner som representeras av rader på snabbfliken **Kolumndefinitioner** på sidan **datautbytesdefinition**.|  
    |**Fält-ID**|Ange vilka fält kolumnen i fältet **Kolumnnr.** mappas till.<br /><br /> Du kan bara välja från fält som finns i tabellen som du har angett i fältet **Tabell** på snabbfliken **Allmänt**.|  
    |**Valfri**|Ange att mappningen hoppas över om fältet är tomt. **Obs!**  Om du inte markerar den här kryssrutan inträffar ett exportfel om fältet är tomt. **Obs:**  Fältet är endast relevant för export.|  
    |**Måltabell-ID**|Visas endast när kryssrutan **Använd som cachelagringstabell** är markerad.<br /><br /> Ange tabellen som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|  
    |**Måltabellrubrik**|Visas endast när kryssrutan **Använd som cachelagringstabell** är markerad.<br /><br /> Ange namnet på tabellen i fältet **Måltabell-ID** som är den tabell som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|  
    |**Målfält-ID**|Visas endast när kryssrutan **Använd som cachelagringstabell** är markerad.<br /><br /> Ange fältet i måltabellen som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|  
    |**Målfältsrubrik**|Visas endast när kryssrutan **Använd som cachelagringstabell** är markerad.<br /><br /> Ange namnet på fältet i måltabellen som värdet i fältet **Kolumnrubrik** mappas till när du använder en cachelagringstabell för dataimport.|  
    |**Valfri**|Visas endast när kryssrutan **Använd som cachelagringstabell** är markerad.<br /><br /> Ange om mappningen ska hoppas över när fältet är tomt. Om du inte markerar den här kryssrutan så inträffar ett exportfel om fältet är tomt.|  

Definitionen för datautbyte är nu klar att aktiveras för användare. Mer information finns i [Konfigurera skickande och mottagande av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Konfigurera SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer), [Ta betalt med SEPA-postförskott](finance-collect-payments-with-sepa-direct-debit.md) samt [Betala med AMC Banking 365 Fundamentals -tillägg eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

### <a name="transformation-rules"></a>Omvandlingsregler
Om värdena i fälten som du mappar skiljer sig åt, måste du använda omvandlingsregler för datautbytesdefinitioner för att göra dem likadana. Du definierar omvandlingsregler för datautbytesdefinitioner genom att öppna en befintlig definition (eller skapa en ny definition) och sedan, på snabbfliken **Raddefinitioner**, välja **Hantera** och sedan **Fältmappning**. Fördefinierade regler tillhandahålls, men du kan också skapa egna. I följande register beskrivs de typer av omvandlingar som du kan utföra.

|Alternativ|Beskrivning|
|---------|---------|
|**Versaler**|Skriv alla bokstäver i versaler.|
|**Gemener**|Skriv alla bokstäver som gemener.|
|**Huvudärende**|Skriv första bokstaven i varje ord i versaler.|
|**Trimma**|Ta bort tomma mellanslag före och efter värdet.|
|**Delsträng**|Omvandla en viss del av ett värde. Om du vill ange var du vill starta omvandlingen väljer du antingen **Startposition** eller **Starttext**. Startpositionen är ett tal som representerar det första tecknet som ska omvandlas. Starttexten är bokstaven omedelbart före bokstaven som ska ersättas. Om du vill börja med den första bokstaven i värdet använder du en startposition i stället. Om du vill ange var du vill stoppa omvandlingen väljer du aningen **Längd**, som är antalet tecken som ska ersättas, eller den **avslutande texten**, som är tecknet direkt efter det sista tecknet som ska omvandlas.|
|**Byt ut**|Hitta ett värde och ersätt det med ett annat. Detta är användbart för att ersätta enkla värden, till exempel ett visst ord.|
|**Reguljärt uttryck – Ersätt**|Använd ett reguljärt uttryck som en del av en sök-och ersätt-åtgärd. Detta är användbart för att ersätta flera, eller kanske mer komplexa, värden.|
|**Ta bort icke-alfanumeriska tecken**|Ta bort tecken som inte är bokstäver eller siffror, till exempel symboler eller specialtecken.|
|**Datumformatering**|Ange hur datum ska visas. Du kan till exempel omvandla DD-MM-ÅÅÅÅ till ÅÅÅÅ-MM-DD.|
|**Decimalformat**|Definiera regler för decimalplacering och avrundningsprecision.|
|**Matchning – reguljärt uttryck**|Använd ett reguljärt uttryck för att hitta ett eller flera värden. Detta liknar alternativen för **Delsträng** och **Reguljärt uttryck – Byt ut**.|
|**Anpassat**|Detta är ett avancerat alternativ som kräver hjälp från en utvecklare. Det möjliggör en integreringshändelse som du kan prenumerera på om du vill använda din egen omvandlingskod. Om du är utvecklare och vill använda det här alternativet kan du läsa avsnittet "tips för utvecklare: exempel på det anpassade alternativet" nedan.|
|**Format för datum och tid**|Definiera hur du vill visa aktuellt datum och tid på dagen.|

#### <a name="tip-for-developers-example-of-the-custom-option"></a>Tips för utvecklare: exempel på det anpassade alternativet
I följande exempel visas hur du implementerar din egen omvandlingskod.

```
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
När du har definierat dina regler kan du testa dem. I avsnittet **Test** anger du ett exempel på ett värde som du vill omvandla och kontrollerar sedan resultaten.

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Så här exporterar du en definition för datautbyte som en XML-fil som andra ska använda
När du har skapat definitionen för datautbyte för en viss datafil kan du exportera definitionen för datautbyte som en XML-fil du kan importera. Beskriv i följande procedur.  

1. I rutan **Sök** anger du **Definitioner för datautbyte** och väljer sedan relaterad länk.  
2. Välj den definition för datautbyte som du vill exportera.  
3. Välj åtgärden **Exportera datautbytesdefinition**.  
4. Spara XML-filen som representerar definitionen för datautbytet på ett lämpligt ställe.  

    Om en definition för datautbyte redan har skapats behöver du bara importera XML-filen till ramverket för datautbyte. Beskriv i följande procedur.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Så här importerar du en befintlig definition av datautbyte  
1. Spara XML-filen som representerar definitionen för datautbytet på ett lämpligt ställe.  
2. I rutan **Sök** anger du **Definitioner för datautbyte** och väljer sedan relaterad länk.  
3. Välj åtgärden **Ny**. Sidan **Datautbytesdefinition** öppnas.  
4. Välj åtgärden **Importera datautbytesdefinition**.  
5. Välj filen som du har sparat i steg 1.  

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Konfigurera utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Ta betalt med SEPA-postförskott](finance-collect-payments-with-sepa-direct-debit.md)  
[Göra betalningar med AMC Banking 365 Fundamentals-tillägg eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inkommande dokument](across-income-documents.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: 'Så här: Skapa och rapportera Intrastat | Microsoft Docs'
description: Lär dig hur du konfigurerar funktioner för rapportering av Intrastat och att rapportera handel med företag i andra EU-länder.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 57ac1956c2e7b22a04615c4ebd0ab5b502787a93
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "918834"
---
# <a name="how-to-set-up-and-report-intrastat"></a>Så här: Skapa och rapportera Intrastat
Alla företag i Europeiska unionen måste rapportera sin handel med andra länder/regioner inom EU. I Sverige måste du rapportera transport av varor till de statistiska myndigheterna varje månad. I programmet kallas detta för intrastatrapportering. Du använder sidan **Intrastatjournal** när du vill fylla i periodiska intrastatrapporter.  

## <a name="required-and-optional-setups"></a>Nödvändiga och frivilliga inställningar
Innan du kan använda intrastatjournalen för att rapportera Intrastat-information, finns det flera saker som du måste ställa in:  

* **Intrastatjournalmallar**: du måste ställa in de intrastatjournalmallar och intrastatjournaler som du kommer att använda. Eftersom intrastat rapporteras månadsvis måste skapa 12 intrastatjournaler baserade på samma mall.  
* **Artikelkoder**: Tull- och skattemyndigheterna har fastställt numeriska koder som klassificera artiklar och tjänster. Du kan ange koder för artiklar.
* **Koder för transaktionstyp**: länder och regioner har olika koder för olika typer av Intrastat-transaktioner, till exempel ordinär inköp och försäljning, byte av returnerade varor och byte av inte returnerade varor. Ställ in alla koder som gäller för ditt land/din region. Använd koderna på försäljnings- och inköpsdokument och när du bearbetar returer.  
* **Transportsätt**: det finns sju, ensiffrig kod för Intrastat transportsätt. **1** för sjötransport, **2**för järnvägstransport, **3** för vägtransport, **4** flygtransport, **5** för brev, **7** för fasta installationer och **9** för egen framdrivning (t.ex. transport av en bil genom att köra den). [!INCLUDE[d365fin](includes/d365fin_md.md)] kräver inte dessa koder, men vi rekommenderar att beskrivningarna ger liknande betydelse.  

Du kan även ställa in:

* **Transaktionsspecifikationer**: Använd dessa för att komplettera beskrivningar från transaktionstyperna.  
* **Områden**: Använd dessa för att komplettera uppgifterna om länder och regioner.  
* **In-/ utförselplatser**: Använd dessa för att ange platser där du kan skicka eller ta emot artiklar till eller från andra länder. Flygplatsen Heathrow är ett exempel på en in-/utförselplats. Du kan ange in-/utförselplatser på försäljnings- och inköpsdokument på snabbfliken **Utlandshandel**. Informationen kopieras också från artikeltransaktionerna när du skapar intrastatjournalen.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Så här ställer du in intrastatjournalmallar och intrastatjournaler
Batch-jobbet Intrastat inkluderar endast artikeltransaktioner, inte redovisningstransaktioner. Om du har redovisningstransaktioner som bör ingå i intrastatrapporteringen måste du ange dem manuellt. Om du till exempel köper en dator från ett annat land eller en annan region inom EU, placeras den inte på lager utan bokförs på ett redovisningskonto. Den här typen av transaktioner måste registreras manuellt i intrastatjournalen.  

Du kan exportera transaktionerna till en fil som du kan skicka till de intrastatmyndigheterna. Du kan även skriva ut en rapport, lägga till informationen manuellt i formulären från myndigheterna och sedan skicka informationen.

>  [!Note]
> Vi rekommenderar att du skapar en intrastatjournal varje månad.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Intrastatjournalmallar** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Skapa en mall för varje Intrastatformulär som du använder.  
3. Om du vill skapa journaler, välj fliken **analysera** och välj sedan **journaler**.  
4. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Skapa en mall för varje Intrastatformulär som du använder.  

> [!Note]
> I fältet **statistikperiod** anger du statistikperioden med fyra siffror varav de första två siffrorna representerar året och följande två siffror motsvarar månaden. Skriv till exempel 1706 för juni 2017.

### <a name="to-set-up-commodity-codes"></a>Så här skapar du artikelkoder
Alla artiklar som du köper eller säljer måste ha en artikelkod.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelkoder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Om du vill tilldela en artikel en artikelkod, går du till sidan **artikelkort**, expanderar snabbfliken **kostnader och bokföring**och anger koden i fältet **Artikelkod**.   

### <a name="to-set-up-transaction-nature-codes"></a>Så här skapar du koder av transaktionstyp
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koder för transaktionstyp** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Om du ofta använder en kod av transaktionstyp kan göra du den till standard. Gör detta genom att gå till sidan **Intrastatinställningar** och välja koden.

### <a name="to-set-up-transport-methods"></a>Så här ställer du in transportsätt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Transportmetoder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Om du vill ställa in vilka Intrastatrapportfält som är obligatoriska
I vissa länder, exempelvis Spanien och Storbritannien, kräver myndigheterna att Intrastatrapporter omfattar, exempelvis leveransmetod för inköp eller andra värden när försäljningen är över ett visst gränsvärde. På sidan **Intrastat-inställningarna** kan du ange att **Kontrollisteinställningar för Intrastat** ange obligatoriska fält på sidan **Intrastatjournal**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Intrastatinställningar** och välj sedan relaterad länk.
2. Välj åtgärden **Kontrollisteinställningar för Intrastat**.
3. På sidan **Kontrollisteinställningar för Intrastat** klickar du på **fältnamnet** för att välja det Intrastatrapportfält som du vill ska vara obligatorisk. 

## <a name="to-report-intrastat"></a>Att rapportera intrastat
När du har fyllt i Intrastatjournalen kan du köra åtgärden **checklisterapport** när du vill kontrollera att all information i journalen är korrekt. Obligatoriska fält som du har angett på sidan **Kontrollisteinställningar för Intrastat** som saknar värden visas i faktaboxen Fel och varning på sidan **Intrastatjournal**. Därefter kan du skriva ut en intrastatrapport som ett formulär eller skapa en fil som ska skickas till skattemyndigheten i Sverige.  

### <a name="to-fill-in-intrastat-journals"></a>Så här fyller du i intrastatjournaler  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Intrastatjournal** och välj sedan relaterad länk.  
2. På sidan **Intrastatjournal** i fältet **Journalnamn** väljer du relevant journal och sedan knappen **OK**.  
3. Välj åtgärden **Föreslå rader**. Fälten **Startdatum** och **Slutdatum** innehåller redan de datum som angavs för statistikperioden i journalen.  
4. I fältet **Omkostnad reglering %** kan du ange ett värde i procent som täcker transport och försäkring. Om du gör detta är innehållet i fältet **Statistiskt värde** i journalen proportionellt sett högre.  
5. Välj **OK** när du vill starta batchjobbet.  

När du kör batch-jobbet hämtas alla artikeltransaktioner inom statistikperioden och infogas som rader i intrastatjournalen. Du kan redigera raderna efter behov.  

> [!IMPORTANT]  
>  Med batch-jobbet hämtas endast de transaktioner som innehåller en lands-/regionkod som en intrastatkod har angetts för på sidan **Länder/regioner**. Därför måste du ange intrastatkoder för de lands-/regionkoder som du vill köra batch-jobbet för.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Rapportera intrastat på ett formulär eller en fil
Du måste skriva ut rapporten **Intrastat - formulär** för att erhålla den information som behövs i INTRASTAT-formuläret från de statistiska myndigheterna. Innan du kan göra detta måste du lägga upp intrastatjournalen och fylla i den. Om du både har försäljnings- och inköpstransaktioner måste du fylla i ett separat formulär för varje typ, vilket innebär att du måste skriva ut rapporten två gånger.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Intrastatjournaler** och välj sedan relaterad länk.  
2. På sidan **Intrastatjournal** väljer du den relevanta journalen i fältet **Journalnamn**.  
3. Om du inte redan har fyllt i journalen gör du det nu, antingen manuellt eller genom att välja **Föreslå rader**.  
4. Välj åtgärden **skriver ut intrastatjournal**.  
5. På snabbfliken **Intrastatjournalrad** lägger du till filtret **Typ** och anger om det är **Inleverans** eller **Utleverans**.  
6. Välj **skicka till** för att skriva ut rapporten.  

### <a name="report-intrastat-in-a-file"></a>Rapportera intrastat i en fil
Du kan skicka Intrastat-rapporten som en fil. Innan du skapar filen kan du skriva ut en kontrollrapport som innehåller samma information som filen.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Intrastatjournal** och välj sedan relaterad länk.  
2. På sidan **Intrastatjournal** väljer du den relevanta journalen i fältet **Journalnamn**.  
3. Om du inte redan har fyllt i journalen gör du det nu, antingen manuellt eller genom att välja **Föreslå rader**.  
4. Välj åtgärden **Skapa fil**.  
5. Klicka på **OK** på batch-jobbets sida.  
6. Välj **Spara**.  
7. Bläddra till den plats där du vill spara filen och skriv filnamnet. Klicka på  **Spara**.

## <a name="reorganize-intrastat-journals"></a>Omorganisera intrastatjournaler
Eftersom du måste skicka en INTRASTAT-rapport varje månad och skapa en ny journal för varje rapport kommer det sannolikt att finnas många journaler. Journalraderna tas inte bort automatiskt. Om du vill kan du ordna om journalnamnen med jämna mellanrum. Du gör detta genom att ta bort de journaler som inte längre behövs. Även journalraderna i de här journalerna tas bort.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Intrastatjournaler** och välj sedan relaterad länk.  
2. Om du vill visa alternativen väljer du fältet **Journalnamn**.  
3. Välj journalerna som tas bort, och välj sedan **Ta bort**.  

## <a name="see-also"></a>Se även
[Ekonomihantering](finance.md)

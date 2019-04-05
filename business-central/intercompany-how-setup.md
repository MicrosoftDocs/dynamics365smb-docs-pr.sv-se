---
title: Ställa in bokföring av koncerninterna transaktioner | Microsoft Docs
description: Skapa dina koncerninterna leverantörer och kunder som så kallade koncerninterna partners och konfigurera en koncernintern kontoplan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 03/11/2019
ms.author: sgroespe
ms.openlocfilehash: a549dd926894e8c14a5f57437ca9402e2ddde5d1
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/19/2019
ms.locfileid: "852545"
---
# <a name="set-up-intercompany"></a>Koncerninterna inställningar
Om du vill skicka en transaktion (till exempel en försäljningsjournalrad) från ett företag och att motsvarande transaktion (till exempel en inköpsjournalrad) skapas automatiskt i partnerföretaget, måste de berörda företagen komma överens om en gemensam kontoplan och ange vilka dimensioner som ska användas för koncerninterna transaktioner. Den koncerninterna kontoplanen kan till exempel vara en förenklad version av moderbolagets kontoplan. Varje företag kopplar sin fullständiga kontoplan till den gemensamma kontoplanen, och varje företag kopplar sina dimensioner till de företagsinterna dimensionerna.  

Du måste också ställa in en koncernintern partnerkod för varje partnerföretag som godtas av alla företag, och sedan tilldela dem till kundkort respektive leverantörskort genom att fylla i fältet **koncernintern partnerkod**.  

Om du vill skapa eller ta emot koncerninterna rader med artiklar kan du använda egna artikelnummer eller lägga upp partnerns artikelnummer för artikeln. Det gör du antingen i fältet **Leverantörens artikelnr** eller i fältet **Gemensamt artikelnr** som är kopplat till artikelkortet. Du kan också använda funktionen **Artikelkrossreferens**: För att mappa dina artiklars nummer till dina koncerninterna partners beskrivningar av artiklarna öppnar du kortet för varje artikel och väljer sedan åtgärden **Krossreferens** för att ställa in korsreferenser mellan dina artikelbeskrivningar och leverantörens.  

Om du ska skapa koncerninterna försäljningstransaktioner där resurser ingår måste du fylla i fältet **Ink.red.ktonr konc.int partner** på den aktuella resursens resurskort. Det här är numret på det koncerninterna redovisningskontot i partnerföretaget som beloppet för resursen ska bokföras på. Mer information finns i [Ange resurser](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Så här konfigurerar du företag för koncerninterna transaktioner.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Företagsinformation** och välj sedan relaterad länk.  
2. På sidan **företagsinformation** fyller du i fälten **Koncernintern partnerkod**, **Typ av koncernintern inkorg**. och **Uppgifter om koncernintern inkorg**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>För att konfigurera koncerninterna partners
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna partner** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Koncerninterna partners** fyller du i fälten efter behov.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Så här ställer du in koncerninterna leverantörer och koncerninterna kunder
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörer** och välj sedan relaterad länk.
2. Du kan också komma åt leverantören från fältet **Leverantörsnr** på sidan **Koncerninterna partners**.
3. Öppna kortet för en leverantör som är en koncernintern partner. Mer information finns i [Registrera nya leverantörer](purchasing-how-register-new-vendors.md).
4. I fältet **Koncernintern partnerkod** markerar du den relevanta koncernintern partnerkoden.
5. Upprepa steg 1 till och med 4 för kunder.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Så här ställer du in koncernintern kontoplan
Om en koncern med flera företag ska kunna göra koncerninterna transaktioner måste de komma överens om en kontoplan som de använder som gemensam referens. Du måste komma överens med partnerföretagen om de kontonummer som ska användas när ni skapar koncerninterna transaktioner. Koncernens moderbolag skapar till exempel en förenklad version av sin kontoplan och exporterar den koncerninterna kontoplanen från företagets databas till en XML-fil som distribueras till alla företag inom koncernen.  

Om ditt företag är moderbolaget och har den definierande koncerninterna kontoplanen som din grupp kommer att använda som en gemensam referens följer du proceduren: [Konfigurera den koncerninterna kontoplanen](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Om ditt företag är ett dotterbolag och du har fått en XML-fil med den gemensamma koncerninterna kontoplanen följer du proceduren: [Att importera den koncerninterna kontoplanen](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Så här konfigurerar du den definierande koncerninterna kontoplanen
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konc.int. kontoplan** och välj sedan relaterad länk.
2. På sidan **Konc.int. kontoplan Accounts** anger du varje konto på en rad på sidan.  
3. Om den koncerninterna kontoplanen ska vara identisk med eller likna den vanliga kontoplanen kan du fylla i sidan automatiskt genom att välja åtgärden **Kopiera från kontoplan**. Du kan redigera de nya raderna efter behov.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Så här exporterar du en koncernintern kontoplan:
För att din koncerninterna partner ska kunna importera den definierande kontoplanen måste du exportera den till en fil.      
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konc.int. kontoplan** och välj sedan relaterad länk.
2. På sidan **Konc.int. kontoplan** kan du välja åtgärden **Exportera** och sedan välja knappen **Spara**.
3. Ange filnamnet och sökvägen där du vill spara XML-filen och välj sedan knappen **Spara**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Så här importerar du den koncerninterna kontoplanen  
När det finns en fil för den definierande koncerninterna kontoplanen, kan koncerninterna partnerföretag importera den för att säkerställa att de har samma konton.  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konc.int. kontoplan** och välj sedan relaterad länk.  
2. På sidan **Konc.int. kontoplan** kan du välja åtgärden **Importera**.  
3. Välj filnamnet och sökvägen till XML-filen och välj sedan knappen **Öppna**.  

Sidan **Konc.int. kontoplan** fylls i med en ny eller redigerad redovisningskontorad enligt den koncerninterna kontoplanen i filen. Alla befintliga, ej relaterade rader på sidan ändras inte.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Så här kopplar du den koncerninterna kontoplanen till företagets kontoplan  
När du har definierat eller importerat den koncerninterna kontoplanen som du och de koncerninterna partnerna har kommit överens om att använda, måste du koppla varje koncerninternt redovisningskonto till något av företagets redovisningskonton och tvärtom. På sidan **KI-kontoplan** anger du hur de koncerninterna redovisningskontona i inkommande transaktioner ska översättas till redovisningskonton från företagets kontoplan.

Om kontona i den koncerninterna kontoplanen har samma nummer som motsvarande konton i kontoplanen kan du koppla kontona automatiskt.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konc.int. kontoplan** och välj sedan relaterad länk.  
2. Markera de rader som du vill koppla automatiskt och välj sedan åtgärden **Koppla till konto med samma nummer**.  
3. För varje koncerninternt redovisningskonto som inte har kopplats automatiskt fyller du i fältet **Koppla till redovisningskontonr**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Så här ställer du in standardredovisningskonton för koncernintern partner  
När du skapar en koncernintern försäljnings- eller inköpsrad som du ska skicka som en utgående transaktion anger du ett konto från den koncerninterna kontoplanen som standard för det konto i partnerns företag som beloppet ska bokföras på. På sidan **Kontoplan**, för konton som du använder ofta utgående koncerninterna försäljnings- eller inköpsrader, kan du ange ett standardredovisningskonto för koncerninterna partner. För kundreskontrakonton kan du till exempel ange motsvarande leverantörsreskontrakonton från den koncerninterna kontoplanen.  

När du anger ett redovisningskonto i fältet **Balanskontonr** på en koncernintern rad med **Koncernintern partner** i fältet **Kontotyp** fylls fältet **Redov. konto för konc.int. partner**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontoplan** och välj sedan relaterad länk.  
2. På raden för ett konto som används för koncerninterna transaktioner i fältet **Std.kontonr. konc.int. part.** anger det koncerninterna redovisningskonto som partnern ska bokföra på när du bokför till redovisningskontot på den raden.  
3. Upprepa steg 2 för varje konto som du ofta anger i fältet **Balanskontonr** på en rad i en koncernintern journal eller i ett koncerninternt dokument.

## <a name="to-set-up-intercompany-dimensions"></a>Så här ställer du in koncerninterna dimensioner
Om du och dina koncerninterna partner vill kunna utbyta transaktioner med tillhörande dimensioner måste ni komma överrens om de dimensioner som ni alla kommer att använda. Koncernens moderbolag kan till exempel skapa en förenklad version av sin uppsättning dimensioner, exportera de som koncerninterna dimensioner till en XML-fil och distribuera den till företagen i koncernen. Varje dotterbolag importerar sedan XML-filen till sidan **Koncerninterna dimensioner** och kopplar de koncerninterna dimensionerna till dimensionerna i deras egen **Dimensions**-sida.  

Om ditt företag är moderbolaget och har den definierande uppsättningen koncerninterna dimensioner som koncernen ska använda som en gemensam referens följer du proceduren: [Definiera koncerninterna dimensioner](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Om företaget är ett dotterbolaget och du får en XML-fil med de koncerninterna dimensioner som ska användas som gemensam referens i koncernen följder du proceduren: [Importera koncerninterna dimensioner](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Definiera koncerninterna dimensioner
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna dimensioner** och välj sedan relaterad länk.  
2. På sidan **Koncerninterna dimensioner** anger du varje dimension på en rad.

    Om de koncerninterna dimensionerna ska vara identiska med eller likna företagets dimensioner kan du fylla i sidan automatiskt genom att använda funktionen **Kopiera från dimensioner** och sedan redigera de resulterande raderna.  
3. Du kan exportera de koncerninterna dimensionerna till en XML-fil för distribution till partnerföretagen genom att välja åtgärden **Exportera**.  
4. Ange filnamnet och sökvägen där du vill spara XML-filen och välj sedan knappen **Spara**.  

### <a name="to-import-the-intercompany-dimensions"></a>Så här importerar du koncerninterna dimensioner  
När det finns en fil för den definierande koncerninterna dimensionerna, kan koncerninterna partnerföretag importera den för att säkerställa att de har samma dimensioner.  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna dimensioner** och välj sedan relaterad länk.  
2. På sidan **Koncerninterna dimensioner** kan du välja åtgärden **Importera**.  
3. Ange filnamnet och sökvägen till XML-filen och välj sedan knappen **Öppna**.  

Raderna på sidan **Konc.int. dimensioner** och på sidan **Konc.int. dimensionsvärden** importeras.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Så här kopplar du koncerninterna dimensioner till företagets dimensioner
När du har definierat eller importerat dimensionerna som du och de koncerninterna partnerna har kommit överens om att använda, måste du koppla varje koncernintern dimension till någon av företagets dimensioner och tvärtom. På sidan **Konc.int. dimensioner** anger du hur de koncerninterna dimensionerna i inkommande transaktioner ska översättas till dimensioner från företagets lista över dimensioner. På sidan **Dimension** anger du hur företagets dimensioner ska översättas till koncerninterna dimensioner i utgående transaktioner.

Om några av de koncerninterna dimensionerna har samma koder som motsvarande dimensioner i företagets lista över dimensioner kan du låta dimensionerna kopplas automatiskt och sedan kan du koppla kontona automatiskt.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna dimensioner** och välj sedan relaterad länk.
2. På sidan **konc. int. dimensioner** markerar du de rader som du vill koppla automatiskt och väljer sedan åtgärden **Koppla till dimension med samma kod**.
3. Fyll i fältet **Koppla till dimensionskod** för varje koncernintern dimension som inte har kopplats automatiskt.
4. Välj åtgärden **Konc. int. dimensionsvärden**.
5. På sidan **Konc. int. dimensionsvärden** fyller du i fältet **Koppla till dimensionsvärdekod**.

    Fortsätt att koppla dimensioner till koncerninterna dimensioner på liknande sätt.
6. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Dimensioner** och välj sedan relaterad länk.
7. På sidan **konc. int. dimensioner** markerar du de rader som du vill koppla automatiskt och väljer sedan åtgärden **Koppla till konc.int. dimension med samma kod**.
8. För varje koncernintern dimension som inte har kopplats automatiskt fyller du i fältet **Koppla t konc.int. dim.v.kod**.
9. Välj åtgärden **Dimensionsvärden**.
10. På sidan **Konc. int. dimensionsvärden** fyller du i fältet **Koppla till konc.int. dimensionsvärdekod**.

## <a name="see-also"></a>Se även
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

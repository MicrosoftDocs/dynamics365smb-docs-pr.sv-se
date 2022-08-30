---
title: Synkronisera artiklar och lager
description: Ställ in och kör synkronisering av artiklar mellan Shopify och Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: c7aea0d0b3d9a8902e704a2d390d6a244e8cbbef
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317306"
---
# <a name="synchronize-items-and-inventory"></a>Synkronisera artiklar och lager

**Artiklar** i [!INCLUDE[prod_short](../includes/prod_short.md)] motsvarar *produkter* i Shopify, som innefattar fysiska varor, digitala nedladdningar, tjänster och presentkort som du säljer. Det finns två huvudsakliga anledningar till att synkronisera artiklarna:

1. Datahanteringen utförs främst i [!INCLUDE[prod_short](../includes/prod_short.md)]. Du måste exportera alla eller vissa data till Shopify och göra dem synliga. Du kan exportera artikelnamn, beskrivning, bild, priser, tillgänglighet, varianter, leverantörsinformation och streckkod. När artiklarna har importerats kan du direkt göra dem synliga eller så kan de granskas och förbättras av en ansvarig person först.
2. När en order importeras från Shopify importeras är informationen om artiklarna väsentlig för ytterligare behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)].

Dessa två scenarier är alltid aktiverade.

Ett tredje scenario är att hantera data i Shopify men importera dessa artiklar till [!INCLUDE[prod_short](../includes/prod_short.md)]. Det här scenariot kan vara användbart för datamigreringshändelser när en befintlig online-butik måste vara ansluten till en ny [!INCLUDE[prod_short](../includes/prod_short.md)] miljö.

## <a name="to-define-item-synchronizations"></a>Så här definierar du artikelsynkronisering

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik**. Öppna en butik som du vill konfigurera synkronisering av artiklar för.
2. Från fältet **Synkronisera artikel** väljer du det alternativ som efterfrågas. <br>Skillnaden mellan alternativen beskrivs i följande tabell.

|Alternativ|Description|
|------|-----------|
|**Tomt**| Produkter importeras tillsammans med import av order. Produkter exporteras till Shopify om användare kör åtgärden **Lägg till artikel** från sidan **Shopify-produkter**. Den här processen är standardbeteendet. |
|**Till Shopify**| Välj det här alternativet om du, efter den första synkroniseringen som utlösts av åtgärden **Lägg till artikel**, planerar att uppdatera produkter manuellt med hjälp av åtgärden **Synkronisera produkt** eller via jobbkön för återkommande uppdateringar. Glöm inte att aktivera fältet **Kan uppdatera Shopify-produkt**. Om det inte är aktiverat är det samma som **Tomt**. Mer information finns i [Exportera artiklar till Shopify](synchronize-items.md#export-items-to-shopify)|
|**Från Shopify**| Välj det här alternativet om du planerar att importera produkter från Shopify i bulk, antingen manuellt med hjälp av åtgärden **Synkronisera produkt** eller via jobbkön för återkommande uppdateringar. Om inget alternativ har valts är det samma som **Tomt**. Mer information om hur du importerar objekt finns i [Importera objekt från Shopify](synchronize-items.md#import-items-from-shopify)|

## <a name="import-items-from-shopify"></a>Importera artiklar från Shopify

Antingen importerar du artiklar från Shopify i bulk eller tillsammans med orderimporten. Dessa artiklar läggs till i tabellerna **Shopify-produkt** och **Shopify-variant** först. Med följande inställningar kan du hantera processer:

|Fält|Description|
|------|-----------|
|**Skapa okända artiklar automatiskt**|När Shopify-produkter och -varianter importeras till [!INCLUDE[prod_short](../includes/prod_short.md)] försöker alltid funktionen [!INCLUDE[prod_short](../includes/prod_short.md)] att hitta matchande poster i artikellistan först. **SKU-mappning** har en inverkan på hur matchningen utförs och skapar nya artiklar och/eller artikelvarianter. Aktivera det här alternativet om du vill skapa en ny artikel eller om det inte finns någon matchande post. Den nya artikeln skapas med hjälp av importerade data och **Kod för artikelmall**. Om det här alternativet inte har aktiverats måste du skapa en artikel manuellt och använda åtgärden **Mappa produkt** från sidan **Shopify-produkter**.|
|**Kod för artikelmall**|Används tillsammans med **Skapa okända artiklar automatiskt**. <br> Välj den mall som ska användas för automatiskt skapade artiklar.|
|**SKU-mappning**|Välj hur du vill använda **SKU**-värdet som importerats från Shopify under mappning och skapande av artikel/variant. Mer information finns i [Så påverkar SKU och streckkod som definierats i Shopify produkt mappningen och skapandet av artiklar och varianter](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**Fältavgränsare för lagerställeenhet**|Används tillsammans med **SKU-mappning** inställd på **Artikelnr + Variantkod**.<br> Definiera en avgränsare som ska användas för att dela upp SKU. <br>Om du i Shopify till exempel skapar en variant med SKU ”1000/001”, skriver du ”/” i fältet **Fältavgränsare för lagerställeenhet** för att få artikelnumret i [!INCLUDE[prod_short](../includes/prod_short.md)] till ”1000” och artikelvariantkoden till ”001”.
|**Prefix för variant**|Används tillsammans med **SKU-mappning** inställd på **Variantkod** eller **Artikelnr + Variantkod** som en säkerhetsstrategi när lagerställeenheten som kommer från Shopify är tom.<br>Om du vill skapa artikelvarianten i [!INCLUDE[prod_short](../includes/prod_short.md)] automatiskt måste du ange ett värde i **Kod**. Som standard används det värde som anges i fältet för lagerställeenhet som har importerats från Shopify. Om lagerställeenheten är tom genereras koden med det definierade variantprefixet och ”001”.|
|**Shopify kan uppdatera artikel**| Välj det här alternativet om du vill uppdatera artiklar och/eller varianter automatiskt.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Så påverkar SKU och streckkod som definierats i Shopify-produkter mappningen och skapandet av artiklar och varianter i Business Central

När produkter importeras från Shopify till tabellerna **Shopify-produkter** och **Shopify-varianter** försöker [!INCLUDE[prod_short](../includes/prod_short.md)] att hitta befintliga poster. Skillnaden mellan alternativen i fältet **SKU-mappning** beskrivs i följande tabell.

|Alternativ|Inverkan på mappning|Inverkan på skapande|
|------|-----------------|------------------|
|**Tomt**|Fältet SKU används inte i rutinen för artikelmappning.|Ingen inverkan på skapandet av artikeln. <br>Förhindrar att varianter skapas. Det är användbart när du använder försäljningsorder endast huvudartikel. En variant kan fortfarande mappas manuellt från fönstret **Shopify-produkt**.|
|**Artikelnr**|Välj om fältet SKU innehåller artikelnumret.|Ingen inverkan på skapandet av artikel utan varianter. För artiklar med varianter skapas varje variant som en separat artikel.<br> Om Shopify till exempel har en produkt med två varianter och deras SKU:er är ”1000” och ”2000”, skapas två artiklar med numren ”1000” och ”2000” i [!INCLUDE[prod_short](../includes/prod_short.md)]-systemet.|
|**Variantkod**|Fältet SKU används inte i rutinen för artikelmappning.|Ingen inverkan på skapandet av artikeln. När en artikelvariant skapas används värdet i fältet SKU som kod. Om SKU är tom genereras en kod med hjälp av fältet **Variantprefix**.|
|**Artikelnr + variantkod**| Välj om fältet SKU innehåller ett artikelnr och artikelvariantkod avgränsade med värdet som definieras i fältet **Fältavgränsare för lagerställeenhet**.|När en artikel skapas används den första delen av värdet i fältet SKU som **nr**. Om SKU är tom genereras ett artikelnr med hjälp av nummerserier som definierats i **Kod för artikelmall** eller **Artikelnr** från fönstret **Lagerinställningar**.<br>När en artikel skapas använder variantfunktionen den andra delen av värdet i fältet SKU som **kod**. Om SKU är tom genereras en kod med hjälp av fältet **Variantprefix**.|
|**Leverantörens artikelnr**| Välj om fältet SKU innehåller leverantörens artikelnr. I det här fallet används inte **Artikelleverantörsnr** i fönstret **Artikelkort**, utan **Leverantörens artikelnr** från **Katalog från artikelleverantör**. Om posten i *Katalog från artikelleverantör* innehåller en variantkod används denna variantkod för att mappa Shopify-varianten.|Om en motsvarande leverantör finns i [!INCLUDE[prod_short](../includes/prod_short.md)] används SKU-värdet som **Leverantörens artikelnr** i **Artikelkort** och som **Artikelreferens** av typen Leverantör. <br>Förhindrar att varianter skapas. Det är användbart när du bara vill använda huvudartikeln i försäljningsordern. Du kan fortfarande mappa en variant manuellt från fönstret **Shopify-produkt**.|
|**Streckkod**| Välj om fältet SKU innehåller en streckkod. En sökning utförs bland **Artikelreferenser** av typen Leverantör. Om posten Artikelreferens som hittas innehåller en variantkod används denna variantkod för att mappa Shopify-varianten.|Ingen inverkan på skapandet av artikeln. <br>Förhindrar att varianter skapas. Det kan vara användbart när du endast använder huvudartiklen i försäljningsordern. En variant kan fortfarande mappas manuellt från fönstret **Shopify-produkt**.|

I följande tabell beskrivs effekten av fältet **Streckkod**.

|Inverkan på mappning|Inverkan på skapande|
|-----------------|------------------|
|En sökning utförs bland **Artikelreferenser** av typen Streckkod efter det värde som anges i fältet Streckkod i Shopify. Om posten Artikelreferens som hittas innehåller en variantkod används denna variantkod för att mappa Shopify-varianten.|Streckkoden sparas som **Artikelreferens** för artikel och artikelvariant.|

> [!NOTE]  
> Du kan utlösa mappning för de valda produkterna/varianterna eller alla importerade omappade produkter genom att välja **Försök att hitta produktmappning** (för valda) eller **Försök att hitta mappningar** (för alla).

## <a name="export-items-to-shopify"></a>Exportera artiklar till Shopify

Välj elementen från artikellistan som ska exporteras till Shopify. Använd åtgärden **Lägg till artikel** från fönstret **Shopify-produkter** för att lägga till artiklar till listan över Shopify-produkter.

Med följande inställningar kan du hantera exporten av artiklar:

|Fält|Description|
|------|-----------|
|**Kundprisgrupp**|Ange priset för en artikel i Shopify. Försäljningspriset för den här kundprisgruppen har tagits. Om ingen grupp anges används priset på artikelkortet.|
|**Kundrabattgrupp**|Bestäm vilken rabatt som ska användas i beräkningen av priset på en artikel i Shopify. Rabatterade priser lagras i fältet **Pris** och det fulla priset lagras i fältet **Jämför pris**.|
|**Synkronisera utökad text för artikel**|Välj för att synkronisera den utökade texten för artikeln. Så som den läggs till i *Beskrivning* kan den innehålla HTML-kod. |
|**Synkronisera artikelattribut**|Välj om du vill synkronisera artikelattribut. Attribut formateras som tabeller och inkluderas i fältet *Beskrivning* på Shopify.|
|**Språkkod**|Om detta väljs används de översatta versionerna för titel, attribut och utökad text.|
|**SKU-mappning**|Välj hur du vill fylla i SKU-fältet i Shopify. Följande alternativ stöds:<br> - **Artikelnr** för att använda artikelnr för både produkter och varianter.<br> - **Artikelnr + Variantkod** för att skapa en SKU genom att sammanfoga värden från två fält. För artiklar utan varianter används endast artikelnr.<br>- **Artikelleverantörsnr** för att använda det artikelleverantörsnummer som definierats i *Artikelkort* för både produkter och varianter.<br> - **Streckkod** – använder **Artikelreferens** av typen Streckkod. Det här alternativet respekterar varianter. |
|**Fältavgränsare för lagerställeenhet**|Definiera en avgränsare för alternativet **Artikelnr + Variantkod**.|
|**Lager spårat**|Välj hur systemet ska fylla i fältet **Spåra lager** för produkter som exporteras till Shopify. Du kan uppdatera information om tillgänglighet från [!INCLUDE[prod_short](../includes/prod_short.md)] för produkter i Shopify som lagerspårning har aktiverats för. Mer information finns i [Lager](synchronize-items.md#sync-inventory-to-shopify).|
|**Standardlagerprincip**|Välj *Neka* för att förhindra negativt lager på Shopify-sidan. |
|**Kan uppdatera Shopify-produkter**|Ange om [!INCLUDE[prod_short](../includes/prod_short.md)] endast kan skapa artiklar eller om det kan uppdatera artiklar också. Välj det här alternativet om du, efter den första synkroniseringen som utlösts av åtgärden **Lägg till artikel**, planerar att uppdatera produkter manuellt med hjälp av åtgärden **Synkronisera produkt** eller via jobbkön för återkommande uppdateringar. Glöm inte att välja **Till Shopify** i fältet **Artikelsynkronisering**.|
|**Kod för kundmall**|Välj den standard mall som ska användas under prisberäkningen. Mer information finns i [Ställ in moms](setup-taxes.md).|


### <a name="fields-mapping-overview"></a>Översikt över fältmappning

|Shopify|Källan när den exporteras från [!INCLUDE[prod_short](../includes/prod_short.md)]|Mål när den importeras till [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|Enligt **Status för skapade produkter** på **Shopify-butikskortet**. Mer information finns i [Ad-hoc-uppdateringar av Shopify-produkter](synchronize-items.md#ad-hock-updates-of-shopify-products).|Inte använd.|
|Rubrik|**Beskrivning**. Om språkkoden är definierad och motsvarande artikelöversättning finns kommer artikelöversättningen att användas i stället för beskrivning.|**Beskrivning**|
|Description|Kombinerar utökade texter och attribut om motsvarande reglage på Shopify-butikskortet har aktiverats. Respekterar språkkod.|Inte använd.|
|Sidrubrik, SEO|Korrigera värde: Tom, se [Ad-Hoc-uppdateringar av Shopify-produkter](synchronize-items.md#ad-hock-updates-of-shopify-products). |Inte använd.|
|Metabeskrivning, SEO|Korrigera värde: Tom, se [Ad-Hoc-uppdateringar av Shopify-produkter](synchronize-items.md#ad-hock-updates-of-shopify-products). |Inte använd.|
|Media|**Bild**, mer information finns i [Synkronisera artikelbilder](synchronize-items.md#sync-item-images)|**Bild**|
|Pris|Beräknande av slutkundens pris omfattar artikelprisgrupp, artikelrabattgrupp, valutakod och kod för kundmall. |**A-pris**|
|Jämför med pris|Beräknande av pris utan rabatt omfattar artikelprisgrupp, artikelrabattgrupp, valutakod och kod för kundmall. |Inte använd.|
|Styckkostnad|**Styckkostnad**|**Styckkostnad**|
|Lagerställeenhet|Se **SKU-mappning** i [Exportera artiklar till Shopify](synchronize-items.md#export-items-to-shopify)| Läs [Så påverkar SKU och streckkod som definierats i Shopify produkter mappningen och skapandet av artiklar och varianter](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|Streckkod|**Artikelreferenser** av typen Streckkod|**Artikelreferenser** av typen Streckkod|
|Spåra antal|Enligt **Lager spårat** på **Shopify-butikskortet**. Mer information finns i [Lager](synchronize-items.md#sync-inventory-to-shopify).|Inte använd.|
|Fortsätta sälja när de är slut i lager|Enligt **Standardlagerprincip** på **Shopify-butikskortet**. Inte importerad.|Inte använd.|
|Kontakttyp|**Beskrivning** av **Artikelkategorikod**. Om typen inte har angetts i Shopify läggs den till som en anpassad typ.|**Artikelkategorikod**. Mappning per beskrivning.|
|Leverantör|**Namn** på leverantör från **Leverantörsnr** |**Leverantörsnr**-mappning efter namn.|
|Vikt|**Bruttovikt**.|Inte använd.|
|Momspliktig|Fast värde: aktiverat.|Inte använd.|
|Momskoder|**Momsgruppskod**. Endast relevant för moms. Mer information finns i [Ställ in moms](setup-taxes.md). |Inte använd.|

### <a name="tags"></a>Taggar

Granska importerade taggar i faktaboxen **Taggar** på sidan **Shopify produkt**. Du kan redigera taggar genom att välja åtgärden **Taggar** på sidan **Shopify-produkt**.
Om alternativet **Till Shopify** har valts i fältet **Synkronisera artikel** exporteras tilldelade taggar till Shopify vid nästa synkronisering.

## <a name="run-item-synchronization"></a>Kör atikelsynkronisering

Fullständig eller delvis synkronisering av artiklar kan utföras på många olika sätt.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Inledande synkronisering av artiklar från Business Central till Shopify

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-produkter** och välj relaterad länk.
2. Välj åtgärden **Lägg till artiklar**.
3. Ange koden i fältet **Butikskod**. Om du öppnar fönstret **Shopify-produkt** från fönstret **Butikskort** fylls butikskoden i automatiskt.
4. Definiera filter för artiklar efter behov. Du kan till exempel filtrera per artikelnummer. eller artikelkategorikod.
5. Välj **OK**.

De resulterande artiklarna skapas automatiskt i Shopify med priser, men bilder och lagernivåer ingår inte. Åtgärden kan ta lite tid om ett stort antal artiklar läggs till.

### <a name="sync-products-from-shopify-to-business-central"></a>Synkronisera produkter från Shopify till Business Central

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill synkronisera artiklar för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Synkronisera produkter**.

Alternativt kan du använda åtgärden **Synkronisera produkter** i fönstret **Shopify-produkter** eller söka efter batchjobbet **Synkronisera produkter**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Mer information finns i [Schemalägger du återkommande uppgifter](background.md#to-schedule-recurring-tasks).

### <a name="ad-hock-updates-of-shopify-products"></a>Ad-hoc-uppdateringar av Shopify-produkter

När posterna uppdateras i tabellen **Shopify-produkt** synkroniseras följande ändringar med Shopify.

Uppdatera:

* **Status** – du kan välja mellan aktiv, arkiverad och utkast.
* **SEO-rubrik**
* **SEO-beskrivning**

Borttagning:

Baserat på värdet i **Åtgärd för borttagna produkter** på **Shopify-butikskortet** uppdateras produkten i Shopify när posten raderas från sidan **Shopify-produkter**.

* **Tom** – ingenting händer. Om det behövs måste användaren utföra den åtgärd som krävs från Shopify-admin.
* **Status till Ukast** – statusen för produkten i Shopify anges till *Utkast*.
* **Status till Arkiverad** – produkten arkiveras i Shopify.

## <a name="sync-item-images"></a>Synkronisera artikelbilder

Synkronisering av bilder kan konfigureras för synkroniserade artiklar. Du kan välja något av följande alternativ:

* **Tom** – synkronisering av bilder inaktiveras.
* **Till Shopify** – bilder på artiklar exporteras till Shopify
* **Från Shopify** – bilder från Shopify importeras till [!INCLUDE[prod_short](../includes/prod_short.md)]

Synkronisering av bilder kan initieras på två sätt.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Synkronisera produktbilder från fönstret Shopify-butik

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik som du vill synkronisera bilder för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Synkronisera produktbilder**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Synkronisera produktbilder från fönstret Shopify-produkter

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-produkter** och välj relaterad länk.
2. Välj åtgärden **Synkronisera produktbilder**.

### <a name="image-synchronization-remarks"></a>Anmärkningar om bildsynkronisering

* När du exporterar bilder från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify läggs de nya bilderna till i Shopify och de gamla bilderna hålls intakta. Om en bild uppdateras i [!INCLUDE[prod_short](../includes/prod_short.md)] måste du ta bort gamla bilder i Shopify-admin.
* Bilder som exporteras till Shopify och inte uppfyller villkoren som anges av Shopify importeras inte. Mer information finns i [Typer av produktmedia på help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Synkronisera priser med Shopify

Priser kan exporteras för synkroniserade artiklar på de sätt som beskrivs nedan.

### <a name="sync-prices-from-the-shopify-products-window"></a>Synkronisera priser från fönstret Shopify-produkter

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-produkter** och välj relaterad länk.
2. Välj åtgärden **Synkronisera priser med Shopify**.

### <a name="price-calculation-remarks"></a>Anmärkningar om prisberäkning

* För prisberäkning är det viktigt att ha ett värde i fältet **Standardkundmall**. Mer information finns i [Ställ in moms](setup-taxes.md).
* Ange en **valutakod** om din onlinebutik använder en annan valuta än BVA. Den angivna valutan måste ha växlingskurser konfigurerade. Lämna fältet tomt om din onlinebeställning använder samma valuta som [!INCLUDE[prod_short](../includes/prod_short.md)].
* När du fastställer ett pris använder [!INCLUDE[prod_short](../includes/prod_short.md)] logiken ”Lägsta pris”. Det innebär att om enhetspriset som anges på artikelkortet är lägre än vad som anges i prisgruppen används enhetspriset från artikelkortet.

## <a name="sync-inventory-to-shopify"></a>Synkronisera lager med Shopify

Lagersynkronisering kan konfigureras för artiklar som redan synkroniserats. Två villkor måste uppfyllas:

1. Lagerspårning måste aktiveras för en produkt i Shopify. Om artiklar exporteras till Shopify bör du överväga att aktivera reglaget **Lager spårat** på kortet **Shopify-butik**. Mer information finns i [Exportera artiklar till Shopify](synchronize-items.md#export-items-to-shopify).
2. Lagersynkronisering måste aktiveras för **Shopify-platser**.

### <a name="to-enable-inventory-sync"></a>Aktivera lagersynkronisering

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill synkronisera lager för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Platser** för att öppna **Shopify-butiksplatser**.
4. Välj åtgärden **Hämta Shopify-platser** för att importera alla platser som har definierats i Shopify. Du hittar dem i inställningarna för [**Platser**](https://www.shopify.com/admin/settings/locations) under **Shopify-admin**.
5. I fältet **Platsfilter** lägger du till platser om du endast vill inkludera lager från specifika platser. Du kan till exempel ange *ÖST|VÄST*, så att lager från enbart dessa två platser är tillgängligt för försäljning via onlinebutiken.
6. Avmarkera reglaget **Inaktiverad** för att aktivera lagersynkronisering för utvalda Shopify-platser.

Du kan starta lagersynkronisering på två sätt.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Synkronisera lager från fönstret Shopify-butik

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butiker** och välj relaterad länk.
2. Välj den butik som du vill synkronisera lager för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Synkronisera lager**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Synkronisera lager från fönstret Shopify-produkter

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-produkter** och välj relaterad länk.
2. Välj åtgärden **Synkronisera lager**.

### <a name="inventory-remarks"></a>Lageranmärkningar

* Kopplingen beräknar **Prognostiserat tillgängligt saldo** och exporterar det till Shopify.
* Du kan inspektera lagerinformationen från Shopify på sidan **Faktabox om Shopify-lager**. I den här faktaboxen får du en översikt över Shopify-lagret och det senast beräknade lagret i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finns en post per plats.
* Om lagerinformationen i Shopify skiljer sig från **Prognostiserat tillgängligt saldo** i [!INCLUDE[prod_short](../includes/prod_short.md)] uppdateras lagret i Shopify.

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

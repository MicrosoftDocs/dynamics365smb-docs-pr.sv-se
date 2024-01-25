---
title: Ställa in moms för Shopify anslutning
description: Anger hur du konfigurerar moms i Shopify och Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Ställa in moms för Shopify anslutning

I den här artikeln ska vi undersöka hur olika inställningar i Shopify påverkar webbutikspriser och moms som visas för kunden. Vi ska också ta upp hur du konfigurerar [!INCLUDE[prod_short](../includes/prod_short.md)] för att stödja inställningarna i Shopify. Denna artikel är inte avsedd att vara en omfattande momsguide. Kontakta din lokala skattemyndighet eller en revisor för mer information.  

Artikeln förutsätter att du måste betala moms när du säljer varor lokalt eller internationellt.

## Om du säljer inrikes

När du har konfigurerat Shopify för att samla in moms i ditt land eller din region kan du bestämma hur du vill visa priser i din onlinebutik.

Du anger om skatt ska inkluderas i priserna genom att slå på eller av växlingsknappen **Alla priser inklusive moms** i [**Skatter och avgifter**](https://www.shopify.com/admin/settings/taxes) i din **Shopify administration**.

Växlingen är normalt aktiverad för följande länder/regioner:

* Australien
* Österrike
* Belgien
* Tjeckien
* Danmark
* Finland
* Frankrike
* Tyskland
* Island
* Italien
* Nederländerna
* Nya Zeeland
* Norge
* Spanien
* Sverige
* Schweiz
* Storbritannien. 

På marknader som sådana är det ett pris av 100 EUR som definierats på produktkortet redan innehåller moms (VAT). Priset, inklusive moms, visas för kunden i butiken och kassan.  

I USA och Kanada förväntar sig kunderna inte priserna på att ta med skatt. Tak läggs till i kassan, vilket innebär att växlingsknappen **Alla priser inkluderar växling av momssats** som normalt inaktiveras. I det här fallet representerar priset 100 USD som definierats på produktkortet priset utan moms. I kassan läggs momsen till i priset.

Om du vill stödja scenariot där **Alla priser inkluderar moms** fyller du i följande fält på [!INCLUDE[prod_short](../includes/prod_short.md)] sidan **Shopify butikskortet**:  

1. Aktivera växlingen **Priser inklusive moms**.  
2. I fältet **Rörelsebokföringsmall för moms**, ange den bokföringsgrupp du använder för inhemska kunder.  

Definiera nu artikel priser i fälten **Artikelkort** eller **Försäljningsprislista** med eller utan skatt. Vid export av priser till Shopify, [!INCLUDE [prod_short](../includes/prod_short.md)] inkluderar inhemska skatter i det beräknade priset och visar det priset för produkten i Shopify.

[!Note]
> Dessa inställningar påverkar exporten av priser. När du importerar order från Shopify, kommer inställningen för fältet **Priser inklusive moms** från **Kundmall** på Shopify butikskort eller kundmall per land/region. Även om du använder standard kunden för importerade order måste du fylla i **Kod för kundmall**.

## Om du säljer internationellt

I det här avsnittet utforskar vi inställningarna för de scenarier där du måste samla in skatter när du säljer till ett annat land/region, till exempel andra länder/regioner inom EU.

Tillägget Shopify-anslutning stöder för närvarande endast export av ett pris. Shopify använder automatiskt lokala skatter, valutor och avrundning. Växlingsknappen **Alla priser inkluderar moms** resulterar i de åtgärder som beskrivs i följande underavsnitt.

### Alla priser inklusive moms är markerade

|-|Inrikes försäljning|Utländskt land/region där du inte ska samla in skatt|Utländskt land/region där du inte ska samla in skatt|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1200|1200|1200|
|Momssatsprocenten|20|25|0|
|Pris i kassan|1200|1200|1200|

Priset för kunden förblir intakt, oavsett var de befinner sig, men marginalen påverkas på grund av momssatser som skiljer sig åt per land/region.

### Alla priser inklusive moms är inte markerade

|-|Inrikes försäljning|Utländskt land där du ska samla in skatt|Utländskt land där du inte ska samla in skatt|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1 000|1 000|1 000|
|Momssatsprocenten|20|25|0|
|Pris i kassan|1200|1250|1 000|

Shopify lägger till lokala skatter över det pris som definierats på produktkortet baserat på var varor levereras.

## Dynamisk moms, inklusive prissättning

Länder/regioner har olika behov av att ta med skatt i priser. Om du vill att skatten ska inkludera moms automatiskt, kan du aktivera [Dynamisk moms, inklusive prissättning](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) i Shopify.

I din **Shopify administration**, välj **inkludera eller exkludera moms baserat på kundens land** i avsnittet **Övriga marknader – Inställningar** i inställningarna för [**Marknader**](https://www.shopify.com/admin/settings/markets).  

> [!NOTE]
> Den här inställningen påverkar inte priser på de inhemska marknaderna, som kontrolleras av växlingsknappen **Alla priser inklusive moms**.

### Alla priser inklusive moms är markerade

|-|Inrikes försäljning|Utländskt land/region där moms inkluderas i priset|Utländskt land/region där moms utesluts|
|------------------------|---------------|---------------|--------|
|Pris som visas i onlinebutiken|1200|1250|1 000|
|Momssatsprocenten|20|25|10|
|Pris i kassan|1200|1250|1100|

Priset för varje kund ändras beroende på var de befinner sig.

### Alla priser inklusive moms är inte markerade

|-|Inrikes försäljning|Utländskt land/region där moms inkluderas i priset|Utländskt land/region där moms utesluts|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1 000|1250|1 000|
|Momssatsprocenten|20|25|10|
|Pris i kassan|1200|1250|1100|

> [!NOTE]
> Växlingsknappen **Alla priser inklusive moms** ändras inte hur priser visas för internationella kunder.

## Om du säljer till EU-kunder

Olika EU-länder/regioner har olika lokala momssatser. Om du befinner dig i EU och säljer till andra EU-länder/regioner kan du dock använda din lokala momssats i vissa fall.  

I din **Shopify administration**, markera kryssrutan **Använder moms** i avsnittet **Europeiska unionen** i [**skatter och avgifter**](https://www.shopify.com/admin/settings/taxes).

|Använder moms|Momssats|
|-|-|
|Undantag för mikroföretag|Använd din inhemska momssats för all försäljning inom EU|
|En kontaktpunkt eller land-/regionsspecifik registrering|Använd momssatsen i kundens land/region|

### Använder moms ställs in på registrering av kontaktpunkt

I följande exempel är **Alla priser inkluderar moms** aktiverad. Priset på produkt kortet är inställt på *1200*.

|-|Inrikes försäljning|Främmande land-/regionskod|
|------------------------|--------|--------|
|Pris som visas i onlinebutiken|1200|1250|
|Momssatsprocenten|20|25|
|Pris i kassan|1200|1250|

### Använder moms ställs in på undantag för mikroföretag

I följande exempel är **Alla priser inkluderar moms** aktiverad. Priset på produkt kortet är inställt på *1200*.

|-|Inrikes försäljning|Utländskt land/region med lokal momssats på 25 procent.|
|------------------------|--------|--------|
|Pris som visas i onlinebutiken|1200|1200|
|Momssatsprocenten|20|20|
|Pris i kassan|1200|1200|

Shopify använder den inhemska momssatsen och ignorerar momssatsen i det främmande landet/regionen när den beräknar slutpriser.

## Importera Shopify order som har sålts till internationella kunder

Om du samlar in moms från flera länder/regioner måste du definiera en land-/regionsspecifika inställning i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finns en anledning till att den här inställningen är obligatorisk. När ett försäljningsdokument skapas i [!INCLUDE[prod_short](../includes/prod_short.md)], [!INCLUDE [prod_short](../includes/prod_short.md)] beräknas skatter istället för att återanvända de skatter som importeras från Shopify.

Dina lands-/regionsspecifika inställningar väljs på sidan **Shopify kundmall**. Där definieras **Standardkundnr** eller **Kod för kundmall**. Kontrollera i båda fallen att den valda kunden eller mallen har följande definierade fält:

1. **Generell rörelsebokföringsmall** (används för utländska kunder).
2. **Rörelsebokföringsmall för moms** (används för utländska kunder).
3. **Priser inklusive moms** (justerad enligt inställning på Shopify sidan):

* Välj **Ja** om **Alla priser inkluderar moms** är aktiverade och **Inkludera eller exkludera moms baserat på kundens land** är inaktiverat.
* Välj **No** om **Alla priser inkluderar moms** är inaktiverade och **Inkludera eller exkludera moms baserat på kundens land** är inaktiverat.
* Välj **Ja** om **Inkludera eller exkludera skatt baserat på din kunds land** är aktiverat och landet eller regionen listas i [länder/regioner med skatt](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Välj **Nej** om **Inkludera eller exkludera skatt baserat på din kunds land** är aktiverat och landet/regionen inte listas i [länder/regioner med skatt](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> Inställningen av fältet **Priser inklusive moms** kommer från mallen, inte från den specifika kunden. Därför är det viktigt att du har definierat kundmallen.

## Andra skatteanmärkningar

Även om den importerade Shopify-ordern innehåller information om skatt, omberäknas skatten när du skapar ett försäljningsdokument. Den omräkningen gör det viktigt att moms- och skatteinställningar är korrekta i [!INCLUDE[prod_short](../includes/prod_short.md)].

* Flera moms- och skattesatser. Vissa produktkategorier är berättigade till exempel av reducerade skattesatser. Du kan använda funktionen [momsåsidosättning](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override)i Shopify. När artiklar importeras och skapas i [!INCLUDE[prod_short](../includes/prod_short.md)], använder de momsinställningarna som anges på artikelns mallkod för Shopify butiken. Innan du importerar order med sådana artiklar måste du uppdatera produkt bokföringsmallen för moms.  
* Adressberoende skattesatser. Använd fältet **Skatteområdesprioritet** tillsammans med tabellen **Kundmallar** för att skriva över standardlogik som fylls i **Skatteområdeskod** i försäljningsdokumentet. I fältet **Skatteområdesprioritet** anges prioritet om den plats där funktionen ska hämta information om land/region och län/provins. Sedan hittas motsvarande post i Shopify-kundmallarna och **Skatteområdeskod**, **Skattepliktig** och **Moms rörelsebokföringsmall** används när ett försäljningsdokument skapas.  

## Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

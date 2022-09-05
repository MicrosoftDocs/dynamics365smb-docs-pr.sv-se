---
title: Ställa in moms för Shopify anslutning
description: Anger hur du konfigurerar moms i Shopify och Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 4146a84aae98b97b9486d4b5fa53ad663d6d5f91
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362197"
---
# <a name="set-up-taxes-for-the-shopify-connection"></a>Ställa in moms för Shopify anslutning

I den här artikeln ska vi undersöka hur olika inställningar i Shopify påverkar webbutikspriser och moms som visas för kunden. Vi ska också läsa hur du konfigurerar [!INCLUDE[prod_short](../includes/prod_short.md)] för att stödja inställningarna i Shopify. Denna artikel är inte avsedd att vara en omfattande momsguide. Kontakta din lokala skattemyndighet eller en revisor för mer information.  

Artikeln förutsätter att du måste betala moms när du säljer varor lokalt eller internationellt.

## <a name="if-you-sell-domestically"></a>Om du säljer inrikes

När du har konfigurerat Shopify för att samla in moms i ditt land eller din region kan du bestämma hur du vill visa priser i din onlinebutik.
Du styr detta genom att aktivera eller inaktivera växlingsknappen **Alla priser inkludera moms** i inställningarna [**skatter och avgifter**](https://www.shopify.com/admin/settings/taxes) i din **Shopify administration**.

Det är vanligt att denna växelknapp är aktiverad för länder som Australien, Österrike, Belgien, Tjeckien, Danmark, Finland, Frankrike, Tyskland, Island, Italien, Nederländerna, Nya Zeeland, Norge, Spanien, Sverige, Schweiz och Storbritannien. På marknader som dessa innehåller priset *100 euro* som definieras i produktkortet redan moms (VAT) och samma pris visas för kunden i onlinebutiken och i kassan.  

I USA och Kanada förväntar sig kunderna att se produktpriser utan moms, som läggs till kassan. Så fältet **Alla priser inkluderar moms** markeras inte vanligtvis. I det här fallet representerar priset *100 USD* som definierats på produktkortet priset utan moms. I kassasteget läggs momsen till över det pris som ska användas för att räkna fram det totala kassabeloppet.

Om du vill stödja scenariot där **Alla priser inkluderar moms** väljs på sidan [!INCLUDE[prod_short](../includes/prod_short.md)] fyller du i fältet **Kundmallkod** på sidan **Shopify butikskort** för att komma åt mallen med följande fält definierade:  

1. **Generell rörelsebokföringsmall**, används för inrikes kunder.  
2. **Rörelsebokföringsmall för moms**, används för inrikes kunder.  
3. **Priser inklusive moms** inställd på *Ja*.  

Definiera nu artikel priser i fältet **Artikelkort** eller **Försäljningsprislista** med eller utan skatt. Vid export av priser till Shopify beräknar systemet priset för att inkludera inhemsk moms då visas det priset i produktkortet i Shopify.

> [!NOTE]
> Om du har konfigurerat Shopify kopplingen till att skapa kunder automatiskt, kan du behöva fler fält i mallen, t.ex. **Kundbokföringsmall**. Om du använder standardkunden för importerade order måste du se till att kunden har samma fält ifyllda. Om du fortfarande måste fylla i **Kod för kundmall** som anges ovan eftersom fälten **Priser inklusive moms**/**Priser inklusive moms** fältet i det skapade försäljningsdokumentet beror inte på kunden, utan på **Kundmall** från Shopify butikskort eller kundmall per land.

## <a name="if-you-sell-internationally"></a>Om du säljer internationellt

I det här avsnittet utforskar vi inställningarna för de scenarier där du måste samla in skatter när du säljer till ett annat land, till exempel andra länder inom EU.

Tillägget stöder för närvarande **Shopify-anslutning** endast export av ett pris. Shopify använder automatiskt lokala skatter, valutor och avrundning. Växlingsknappen **Alla priser inkluderar moms** resulterar i de åtgärder som beskrivs i följande underavsnitt.

### <a name="all-prices-include-tax-is-selected"></a>*Alla priser inklusive moms* är markerade

|-|Inrikes försäljning|Utländskt land där du ska samla in skatt|Utländskt land där du inte ska samla in skatt|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1200|1200|1200|
|Momssatsprocenten|20|25|0|
|Pris i kassan|1200|1200|1200|

Priset för kunden förblir intakt, oavsett var de befinner sig, men marginalen påverkas på grund av momssatser som skiljer sig åt per land.

### <a name="all-prices-include-tax-is-not-selected"></a>*Alla priser inklusive moms* är inte markerade

|-|Inrikes försäljning|Utländskt land där du ska samla in skatt|Utländskt land där du inte ska samla in skatt|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1 000|1 000|1 000|
|Momssatsprocenten|20|25|0|
|Pris i kassan|1200|1250|1 000|

Shopify lägger till lokala skatter över det pris som definierats på produktkortet baserat på var varor levereras.

## <a name="dynamic-tax-inclusive-pricing"></a>Dynamisk moms, inklusive prissättning

Eftersom olika länder har olika behov beroende på om du inkluderar skatt på det visade priset eller inte, kan du växla till [dynamisk moms inklusive prissättning](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing)i Shopify. Detta automatiserar funktionen för inkludering av moms.

Välj **inkludera eller exkludera moms baserat på kundens land** i avsnittet **Övriga marknader - Inställningar** i [**Marknader**](https://www.shopify.com/admin/settings/markets) inställningar i din **Shopify administration**.  

> [!NOTE]
> Den här inställningen påverkar inte åter givningen av priser på de inhemska marknaderna, som kontrolleras av växlingsknappen **Alla priser inklusive moms**.

### <a name="all-prices-include-tax-is-selected"></a>*Alla priser inklusive moms* är markerade

|-|Inrikes försäljning|Utländskt land där moms inkluderas i priset|Utländskt land där moms utesluts|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1200|1250|1 000|
|Momssatsprocenten|20|25|10|
|Pris i kassan|1200|1250|1100|

Priset för varje kund ändras beroende på var de befinner sig.

### <a name="all-prices-include-tax-is-not-selected"></a>*Alla priser inklusive moms* är inte markerade

|-|Inrikes försäljning|Utländskt land där moms inkluderas i priset|Utländskt land där moms utesluts|
|------------------------|--------|--------|--------|
|Pris som visas i onlinebutiken|1 000|1250|1 000|
|Momssatsprocenten|20|25|10|
|Pris i kassan|1200|1250|1100|

> [!NOTE]
> Växlingsknappen **Alla priser inklusive moms** ändras inte hur priser visas för internationella kunder.

## <a name="if-you-sell-to-eu-customers"></a>Om du säljer till EU-kunder

Olika EU-länder har olika lokala momssatser. Om du befinner dig i EU och säljer till andra EU-länder kan du dock använda din lokala momssats i vissa fall.  

Kontrollera rutan **Använder moms** i avsnittet **Europeiska unionen** i inställningarna [**skatter och avgifter**](https://www.shopify.com/admin/settings/taxes) i din **Shopify administration**.

|Använder moms|Momssats|
|-|-|
|Undantag för mikroföretag|Använd din inhemska momssats för all försäljning inom EU|
|En kontaktpunkt eller landspecifik registrering|Använd momssatsen i kundens land|


### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Använder moms ställs in på registrering av kontaktpunkt

I följande exempel är **Alla priser inkluderar moms** aktiverad. Priset på produkt kortet är inställt på *1200*.
        
|-|Inrikes försäljning|Utländskt land|
|------------------------|--------|--------|
|Pris som visas i onlinebutiken|1200|1250|
|Momssatsprocenten|20|25|
|Pris i kassan|1200|1250|       
        
### <a name="collect-vat-set-to-micro-business-exemption"></a>Använder moms ställs in på undantag för mikroföretag

I följande exempel är **Alla priser inkluderar moms** aktiverad. Priset på produkt kortet är inställt på *1200*.
        
|-|Inrikes försäljning|Utländskt land med lokal momssats på 25 procent.|
|------------------------|--------|--------|
|Pris som visas i onlinebutiken|1200|1200|
|Momssatsprocenten|20|20|
|Pris i kassan|1200|1200|           
    
Shopify ignorerar momssatsen i det utländska landet när du beräknar slutgiltiga priser och använder den inhemska momssatsen.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Importera Shopify order som har sålts till internationella kunder

Om du samlar in moms från flera länder måste du förmodligen definiera en landsspecifika inställning i [!INCLUDE[prod_short](../includes/prod_short.md)]. Detta är obligatoriskt eftersom när ett försäljningsdokument skapas i [!INCLUDE[prod_short](../includes/prod_short.md)] beräknar systemet moms i stället för att använda de som importerats från Shopify.

Lands-/regionsspecifika inställningar väljs i fönstret **Shopify kundmall**. Där definieras **Standardkundnr** eller **Kod för kundmall**. Kontrollera i båda fallen att den valda kunden eller mallen har följande definierade fält:

1. **Generell rörelsebokföringsmall** (används för utländska kunder).
2. **Rörelsebokföringsmall för moms** (används för utländska kunder).
3. **Priser inklusive moms** (justerad enligt inställning på Shopify sidan):
* Välj *Ja* om **Alla priser inkluderar moms** är aktiverade och **Inkludera eller exkludera moms baserat på kundens land** är inaktiverat.
* Välj *No* om **Alla priser inkluderar moms** är inaktiverade och **Inkludera eller exkludera moms baserat på kundens land** är inaktiverat.
* Välj *Ja* om **Inkludera eller exkludera skatt baserat på din kunds land** är aktiverat och landet eller regionen listas i [länder med skatt](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Välj *Nej* om **Inkludera eller exkludera skatt baserat på din kunds land** är aktiverat och landet eller regionen inte listas i [länder med skatt](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> Inställningen av fältet **Priser inklusive moms** kommer från mallen, inte från den specifika kunden. Därför är det viktigt att du har definierat kundmallen.

## <a name="other-tax-remarks"></a>Andra skatteanmärkningar

Även om den importerade Shopify-ordern innehåller information om skatt, omberäknas skatten när du skapar ett försäljningsdokument. Den omräkningen gör det viktigt att moms- och skatteinställningar är korrekta i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flera moms- och skattesatser. Vissa produktkategorier är berättigade till exempel av reducerade skattesatser. Du kan använda funktionen [momsåsidosättning](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override)i Shopify. När artiklar importeras och skapas i [!INCLUDE[prod_short](../includes/prod_short.md)], använder de momsinställningarna som fyllts i på artikelns mallkod för Shopify butiken. Innan du importerar order med sådana artiklar måste du uppdatera produkt bokföringsmallen för moms.  

- Adressberoende skattesatser. Använd fältet **Skatteområdesprioritet** tillsammans med tabellen **Kundmallar** för att skriva över standardlogik som fylls i **Skatteområdeskod** i försäljningsdokumentet. I fältet **Skatteområdesprioritet** anges prioritet om den plats där funktionen ska hämta information om land/region och län/provins. Sedan hittas motsvarande post i Shopify-kundmallarna och **Skatteområdeskod**, **Skattepliktig** och **Moms rörelsebokföringsmall** används när ett försäljningsdokument skapas.  

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

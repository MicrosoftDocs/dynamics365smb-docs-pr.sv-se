---
title: Synkronisera kunder
description: Importera kunder från eller exportera kunder till Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 75c4de7736572ff923c74464dc33b218d0665e3f
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808872"
---
# <a name="synchronize-customers"></a>Synkronisera kunder

När en order importeras från Shopify är informationen om kunden väsentlig för ytterligare behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finns två huvudalternativ och kombinationer:

* Använd särskild kund för alla order.
* Importera information om den faktiska kunden från Shopify. Det här alternativet är också tillgängligt när du exporterar kunder till Shopify från [!INCLUDE[prod_short](../includes/prod_short.md)] först.

## <a name="how-connector-chooses-which-customer-to-use"></a>Så väljer kopplingen vilken kund som ska användas

Funktionen *Importera order från Shopify* försöker att välja kunder i följande ordning:

1. Om **Standardkundnr** definieras i **Shopify-kundmall** för motsvarande land används **Standardkundnr** oavsett inställningar i **Kundimport från Shopify** och **Kundmappningstyp**. Mer information finns i [Kundmall per land](synchronize-customers.md#customer-template-per-country)
2. Om **Kundimport från Shopify** anges till *Ingen* och **Standardkundnr.** definieras i **Shopify butikskort**, sedan **Standardkundnr.** .

Nästa steg beror på **Kundmappningstyp**.

* **Ta alltid standardkunden** och använd sedan kunden som definierats i fältet **Standardkundnr** i fönstret **Shopify-butikskort**.
* **Via e-post/telefon**, kopplingen försöker att hitta befintliga kunder genom ID först, sedan via e-post och sedan via telefon. Om kunden inte hittas skapar kopplingen en ny kund.
* **Genom faktureringsinfo**, kopplingen försöker att hitta befintliga kunder genom ID först och sedan genom information om faktureringsadressen. Om kunden inte hittas skapar kopplingen en ny kund.

> [!NOTE]  
> Kopplingen använder information från faktureringsadressen och skapar en faktureringskund i [!INCLUDE[prod_short](../includes/prod_short.md)]. Försäljningskund är samma som faktureringskund.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Viktiga inställningar när du importerar kunder från Shopify

Antingen importerar du kunder från Shopify i bulk eller tillsammans med orderimporten. Du kan hantera processen med följande inställningar:

|Fält|Description|
|------|-----------|
|**Kundimport från Shopify**|Välj **Alla kunder** om du planerar att importera kunder från Shopify i bulk, antingen manuellt med åtgärden **Synkronisera kunder** eller via jobbkön för återkommande uppdateringar. Oavsett val importeras alltid kundinformationen tillsammans med ordrar. Användningen av den här informationen beror emellertid på **Shopify-kundmallar** och inställningar i fältet **Kundmappningstyp**.|
|**Kundmappningstyp**|Definiera hur kopplingen ska utföra mappning.<br>- **Via e-post/telefon** om du vill att kopplingen mappar importerade Shopify-kunder till befintliga kunder i [!INCLUDE[prod_short](../includes/prod_short.md)] med hjälp av e-post och telefon.</br>- **Genom faktureringsinfo** om du vill att kopplingen mappar importerade Shopify-kunder till befintliga kunder i [!INCLUDE[prod_short](../includes/prod_short.md)] med hjälp av adressinformation eller information om fakturamottagaren.</br>Välj **Ta alltid standardkunden** om du vill att systemet använder en kund från **Standardkundnr** . |
|**Shopify kan uppdatera kunder**| Välj om du vill att kopplingen uppdaterar kunder som inte hittas, när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**.|
|**Skapa okända kunder automatiskt**| Välj om du vill att kopplingen skapar saknade kunder när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**. En ny kund skapas med hjälp av importerade data och **Kod för kundmall** definierad på någon av sidorna **Shopify-butikskort** eller **Shopify-kundmall**. Observera att Shopify-kunden måste ha minst en adress. Om alternativet inte har aktiverats måste du skapa kunden manuellt och koppla den till Shopify-kunden. Du kan alltid upprätta en kundsskapelse manuellt från sidan **Shopify-order**.|
|**Kod för kundmall**|Används tillsammans med **Skapa okända automatiskt**.<br> Välj den standardmall som ska användas för automatiskt skapade kunder. Du kan definiera mallar per land/region i fönstret **Shopify-kundmallar**, vilket är användbart för korrekt momsberäkning. Mer information finns i [Momsanmärkningar](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Kundmall per land

Vissa inställningar kan definieras på lands-/regionnivå eller på läns-/provinsnivå. Inställningarna kan konfigureras i [Leverans](https://www.shopify.com/admin/settings/shipping) på Shopify.

Med **Shopify-kundmallen** kan du göra följande för varje land:

1. Ange **Standardkundnr**, vilket har högre prioritet än valen i fälten **Kundimport från Shopify** och **Kundmappningstyp**. Används i den importerade försäljningsordern.
2. Definiera **Kod för kundmall**, som används för att skapa saknade kunder om **Skapa okända kunder automatiskt** har aktiverats. Om **Kod för kundmall** är tom använder funktionen **Kod för kundmall** som har definierats på **Shopify-butikskortet**.
3. I vissa fall räcker inte **Kod för kundmall** per land för att säkerställa korrekt beräkning av moms. För till exempel länder med moms.

> [!NOTE]  
> Landskoderna är ISO 3166-1 alpha-2 landskoder. Mer information finns i [Landskod](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Exportera kunder till Shopify

Befintliga kunder kan exporteras till Shopify i bulk. Detta innebär att en kund och en standardadress skapas. Du kan hantera processen med hjälp av följande inställningar:

|Fält|Description|
|------|-----------|
|**Exportera kunder till Shopify**|Välj om du planerar att exportera alla kunder med en giltig e-postadress från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify i bulk, antingen manuellt med hjälp av åtgärden **Synkronisera kunder** eller via jobbkön för återkommande uppdateringar.|
|**Kan uppdatera Shopify-kunder**|Används tillsammans med **Exportera kunder till Shopify**. Aktivera om du till generera uppdateringar senare från [!INCLUDE[prod_short](../includes/prod_short.md)] för kunder som redan finns i Shopify.|

> [!NOTE]  
> När du har skapat kunderna i Shopify kanske du vill skicka direktinbjudningar till kunderna. Det uppmanar dem att aktivera sitt konto.

### <a name="populate-customer-information-in-shopify"></a>Fylla i kundinformation i Shopify

En kund i Shopify har förnamn, efternamn, e-post och/eller telefonnummer. Du kan fylla i förnamn och efternamn baserat på informationen från kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Kontaktnamn**|Högsta prioritet om fältet **Kontaktnamn** har fyllts i och fältet **Kontaktkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|2|**Namn 2**|Om fältet **Namn 2** har fyllts i och fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|3|**Namn**|Lägsta prioritet om fältet **Namn** har fyllts i och fältet **Namnkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|

En kund i Shopify har också en standardadress, som utöver förnamn, efternamn, e-post och/eller telefon kan innehålla företag och adress. Du kan fylla i fältet **Företag** baserat på data från kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Namn**|Högsta prioritet om fältet **Namnkälla** på **Shopify-butikskortet** innehåller *Företagsnamn*.|
|2|**Namn 2**|Lägsta prioritet om fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller *Företagsnamn*.|

För adresser där land/provins används väljer du *Kod* eller *Namn* i fältet **Landskälla** på **Shopify-butikskortet** för att specificera vilken typ av data som lagras i [!INCLUDE[prod_short](../includes/prod_short.md)] i fältet **Land**.

## <a name="sync-customers"></a>Synka kunder

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj den butik som du vill synkronisera kunder för och öppna sidan **Shopify-butikskort**.
3. Välj åtgärden **Synkronisera kunder**.

Alternativt kan du använda åtgärden **Starta synkronisering av kunder** i fönstret **Shopify-kunder** eller söka efter batchjobbet **Synkronisera kunder**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Mer information finns i [Schemalägger du återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

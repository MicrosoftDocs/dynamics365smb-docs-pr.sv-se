---
title: Synkronisera kunder
description: Importera kunder från eller exportera kunder till Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: d4ff86179fa5b82bcc398ee58cf92fc121c486d8
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361428"
---
# <a name="synchronize-customers"></a>Synkronisera kunder

När en order importeras från Shopify är informationen om kunden väsentlig för ytterligare behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finns två huvudalternativ och kombinationer:

* Använd särskild kund för alla order.
* Importera information om den faktiska kunden från Shopify. Det här alternativet är också tillgängligt när du exporterar kunder till Shopify från [!INCLUDE[prod_short](../includes/prod_short.md)] först.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Så väljer kopplingen vilken kund som ska användas

Funktionen *Importera order från Shopify* försöker att välja kunder i följande ordning:

1. Om **Standardkundnr** definieras i **Shopify-kundmall** för motsvarande land används **Standardkundnr** oavsett inställningar i **Kundimport från Shopify** och **Kundmappningstyp**. Läs mer i [Kundmall per land](synchronize-customers.md#customer-template-per-country).
2. Om **Kundimport från Shopify** anges till *Ingen* och **Standardkundnr.** definieras på sidan **Shopify butikskort**, sedan **Standardkundnr.** .

Nästa steg beror på **Kundmappningstyp**.

* Om det är **Ta alltid standardkunden** använder kopplingen sedan kunden som definierats i fältet **Standardkundnr** på sidan **Shopify-butikskort**.
* Om det är **Via e-post/telefon** försöker kopplingen hitta befintliga kunder genom ID först, sedan via e-post och sedan via telefonnummer. Om kunden inte hittas skapar kopplingen en ny kund.
* Om det är **Genom faktureringsinfo** försöker kopplingen att hitta befintliga kunder genom ID först och sedan genom information om faktureringsadressen. Om kunden inte hittas skapar kopplingen en ny kund.

> [!NOTE]  
> Kopplingen använder information från faktureringsadressen och skapar en faktureringskund i [!INCLUDE[prod_short](../includes/prod_short.md)]. Försäljningskunden är densamma som faktureringskunden.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Viktiga inställningar när du importerar kunder från Shopify

Oavsett om du importerar kunder från Shopify i bulk eller samtidigt som du importerar order kan du hantera processen med följande inställningar:

|Fält|Description|
|------|-----------|
|**Kundimport från Shopify**|Välj **Alla kunder** om du planerar att importera kunder från Shopify i bulk, antingen manuellt med åtgärden **Synkronisera kunder** eller via jobbkön för återkommande uppdateringar. Oavsett val importeras alltid kundinformationen tillsammans med ordrar. Användningen av den här informationen beror emellertid på **Shopify-kundmallar** och inställningar i fältet **Kundmappningstyp**.|
|**Kundmappningstyp**|Definiera hur kopplingen ska utföra mappning.<br>- **Via e-post/telefon** om du vill att kopplingen mappar importerade Shopify-kunder till befintliga kunder i [!INCLUDE[prod_short](../includes/prod_short.md)] med hjälp av e-post och telefon.</br>- **Genom faktureringsinfo** om du vill att kopplingen ska använda adressen för fakturamottagaren för att mappa importerade Shopify-kunder till befintliga kunder i [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Välj **Ta alltid standardkunden** om du vill att systemet använder en kund från **Standardkundnr** . |
|**Shopify kan uppdatera kunder**| Välj detta fält om du vill att kopplingen uppdaterar kunder som hittas, när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**.|
|**Skapa okända kunder automatiskt**| Välj detta fält om du vill att kopplingen skapar saknade kunder när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**. En ny kund skapas med hjälp av importerade data och **Kod för kundmall** definierad på någon av sidorna **Shopify-butikskort** eller **Shopify-kundmall**. Observera att Shopify-kunden måste ha minst en adress. Om alternativet inte har aktiverats måste du skapa kunden manuellt och koppla den till Shopify-kunden. Du kan alltid upprätta en kundsskapelse manuellt från sidan **Shopify-order**.|
|**Kod för kundmall**|Detta fält används tillsammans med **Skapa okända automatiskt**.<br>- Välj den standardmall som ska användas för automatiskt skapade kunder. Kontrollera att den valda mallen innehåller de obligatoriska fälten, till exempel **Gen. rörelsebokföringsmall**, **Kundbokföringsmall** och moms eller momsrelaterade fält.<br>- Du kan definiera mallar per land/region i sidan **Shopify-kundmallar**, vilket är användbart för korrekt momsberäkning. <br>- Läs mer i [Ställa in moms](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Kundmall per land

Vissa inställningar kan definieras på lands-/regionnivå eller på läns-/provinsnivå. Inställningarna kan konfigureras i [Leverans](https://www.shopify.com/admin/settings/shipping) på Shopify.

Med **Shopify-kundmallen** kan du göra följande för varje kund:

1. Ange **Standardkundnr**, vilket har högre prioritet än valen i fälten **Kundimport från Shopify** och **Kundmappningstyp**. Används i den importerade försäljningsordern.
2. Definiera **Kod för kundmall**, som används för att skapa saknade kunder om **Skapa okända kunder automatiskt** har aktiverats. Om **Kod för kundmall** är tom använder funktionen **Kod för kundmall** som har definierats på **Shopify-butikskortet**.
3. Ange om priser inkluderar skatt/moms för importerade order.
4. I vissa fall räcker inte den **Kod för kundmall** som definieras för ett land inte för att säkerställa korrekt beräkning av skatter (till exempel för länder med moms). I det här fallet kan **skatteområdena** vara ett användbart tillägg.

> [!NOTE]  
> Landskoderna är ISO 3166-1 alpha-2 landskoder. Läs mer om [landskod](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Exportera kunder till Shopify

Befintliga kunder kan exporteras till Shopify i bulk. I varje fall kommer en kund och en standardadress skapas. Med följande inställningar kan du hantera processer:

|Fält|Description|
|------|-----------|
|**Exportera kunder till Shopify**|Välj detta om du planerar att exportera alla kunder med en giltig e-postadress från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify i bulk. Du kan göra det antingen manuellt, med hjälp av åtgärden **synkronisera kunder** eller automatiskt med hjälp av en jobbkö för återkommande uppdateringar.<br> När du exporterar kunder med adresser som inkluderar provinser/stater måste du se till att **ISO-koden** fylls i för länder/regioner.|
|**Kan uppdatera Shopify-kunder**|Detta används tillsammans med inställning **Exportera kunder till Shopify**. Aktivera om du till generera uppdateringar senare från [!INCLUDE[prod_short](../includes/prod_short.md)] för kunder som redan finns i Shopify.|

> [!NOTE]  
> När du har skapat kunderna i Shopify kan du skicka direkt inbjudningar till dem och på så vis uppmuntra dem att aktivera sina konton.

### <a name="populate-customer-information-in-shopify"></a>Fylla i kundinformation i Shopify

En kund i Shopify har förnamn, efternamn, e-post och/eller telefonnummer. Du kan fylla i förnamn och efternamn baserat på informationen från kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Kontaktnamn**|Högsta prioritet om fältet **Kontaktnamn** har fyllts i och fältet **Kontaktkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|2|**Namn 2**|Om fältet **Namn 2** har fyllts i och fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|3|**Namn**|Lägsta prioritet om fältet **Namn** har fyllts i och fältet **Namnkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|

En kund i Shopify har också en standardadress, som kan innehålla ettt företag och en adress utöver förnamn, efternamn, e-post och/eller telefon. Du kan fylla i fältet **Företag** baserat på data från kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Namn**|Högsta prioritet om fältet **Namnkälla** på **Shopify-butikskortet** innehåller *Företagsnamn*.|
|2|**Namn 2**|Lägsta prioritet om fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller *Företagsnamn*.|

För adresser där land/provins används väljer du *Kod* eller *Namn* i fältet **Landskälla** i **Shopify-butikskort**. Här anges vilken typ av data som lagras i [!INCLUDE[prod_short](../includes/prod_short.md)] i fältet **land**.

## <a name="sync-customers"></a>Synka kunder

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den specifika butik som du vill synkronisera kunder för.
3. Välj åtgärden **Synkronisera kunder**.

Alternativt kan du använda åtgärden **Starta synkronisering av kunder** i fönstret **Shopify-kunder** eller söka efter batchjobbet **Synkronisera kunder**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

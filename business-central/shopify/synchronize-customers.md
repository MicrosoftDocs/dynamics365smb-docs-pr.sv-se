---
title: Synkronisera kunder
description: Importera kunder från eller exportera kunder till Shopify
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Synkronisera kunder

När en order importeras från Shopify är informationen om kunden väsentlig för ytterligare behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finns två huvudalternativ och flera kombinationer:

* Använd särskild kund för alla order.
* Importera information om den faktiska kunden från Shopify. Det här alternativet är också tillgängligt när du exporterar kunder till Shopify från [!INCLUDE[prod_short](../includes/prod_short.md)] först.

## Viktiga inställningar när du importerar kunder från Shopify

Antingen importerar du kunder från Shopify i bulk eller tillsammans med orderimporten. Du kan hantera processen med följande inställningar:

|Fält|Beskrivning|
|------|-----------|
|**Kundimport från Shopify**|Välj **Alla kunder** om du planerar att importera kunder från Shopify i bulk, antingen manuellt med åtgärden **Synkronisera kunder** eller via jobbkön för återkommande uppdateringar. Oavsett val importeras alltid kundinformationen tillsammans med ordrar. Användningen av den här informationen beror emellertid på **Shopify-kundmallar** och inställningar i fältet **Kundmappningstyp**.|
|**Kundmappningstyp**|Definiera hur kopplingen ska utföra mappning.<br>- **Via e-post/telefon** om du vill att kopplingen mappar importerade Shopify-kunder till befintliga kunder i [!INCLUDE[prod_short](../includes/prod_short.md)] med hjälp av e-post och telefon.</br>- **Genom faktureringsinfo** om du vill att kopplingen ska använda adressen för fakturamottagaren för att mappa importerade Shopify-kunder till befintliga kunder i [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Välj **Ta alltid standardkunden** om du vill att systemet använder en kund från **Standardkundnr** . |
|**Shopify kan uppdatera kunder**| Välj detta fält om du vill att kopplingen uppdaterar kunder som hittas, när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**.|
|**Skapa okända kunder automatiskt**| Välj detta fält om du vill att kopplingen skapar saknade kunder när något av alternativen **Via e-post/telefon** eller **Genom faktureringsinfo** har valts i fältet **Kundmappningstyp**. En ny kund skapas med hjälp av importerade data och **Kod för kundmall** definierad på någon av sidorna **Shopify-butikskort** eller **Shopify-kundmall**. Observera att Shopify-kunden måste ha minst en adress. Order som skapats via Shopify POS försäljningskanal saknar ofta adressinformation. Om alternativet inte har aktiverats måste du skapa kunden manuellt och koppla den till Shopify-kunden.|
|**Kod för kundmall**|Detta fält används tillsammans med **Skapa okända automatiskt**.<br>- Välj den standardmall som ska användas för automatiskt skapade kunder. Kontrollera att den valda mallen innehåller de obligatoriska fälten, till exempel **Gen. rörelsebokföringsmall**, **Kundbokföringsmall** och moms eller momsrelaterade fält.<br>- Du kan definiera mallar per land/region i sidan **Shopify-kundmallar**, vilket är användbart för korrekt momsberäkning. <br>- Läs mer i [Ställa in moms](setup-taxes.md).|

### Kundmall per land/region

Vissa inställningar kan definieras på lands-/regionnivå eller på läns-/provinsnivå. Inställningarna kan konfigureras i [Leverans](https://www.shopify.com/admin/settings/shipping) på Shopify.

Med **Shopify-kundmallen** kan du göra följande för varje kund:

1. Ange **Standardkundnr**, vilket har högre prioritet än valen i fälten **Kundimport från Shopify** och **Kundmappningstyp**. Används i den importerade försäljningsordern.
2. Definiera **Kod för kundmall**, som används för att skapa saknade kunder om **Skapa okända kunder automatiskt** har aktiverats. Om **Kod för kundmall** är tom använder funktionen **Kod för kundmall** som har definierats på **Shopify-butikskortet**. Systemet försöker först hitta en mall för **lands-/regionkod** för standardadressen. Om det inte finns någon mall används den första adressen.
3. I vissa fall räcker inte den **Kod för kundmall** som definieras för ett land/region inte för att säkerställa korrekt beräkning av skatter (till exempel för länder/regioner med moms). I det här fallet kan **skatteområden** vara ett användbart tillägg.
4. Fältet **Momsområde** innehåller också **Landsnummer** och **Landsnamn**. Det här paret är användbart när kopplingen måste konvertera en kod till ett namn eller vice versa.

> [!NOTE]  
> Landskoderna är ISO 3166-1 alpha-2 landskoder. Läs mer om [landskod](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Exportera kunder till Shopify

Du kan exportera befintliga kunder till Shopify i bulk. I varje fall kommer en kund och en standardadress skapas. Med följande inställningar kan du hantera processer:

|Fält|Beskrivning|
|------|-----------|
|**Exportera kunder till Shopify**|Välj detta alternativ om du planerar att exportera alla kunder från [!INCLUDE[prod_short](../includes/prod_short.md)] till Shopify i bulk. Du kan göra det antingen manuellt, med hjälp av åtgärden **synkronisera kunder** eller automatiskt med hjälp av en jobbkö för återkommande uppdateringar.<br> När du exporterar kunder med adresser som inkluderar provinser/stater måste du se till att **ISO-koden** fylls i för länder/regioner.|
|**Kan uppdatera Shopify-kunder**|Detta används tillsammans med inställning **Exportera kunder till Shopify**. Aktivera detta alternativ om du till generera uppdateringar senare från [!INCLUDE[prod_short](../includes/prod_short.md)] för kunder som redan finns i Shopify.|

Följande krav gäller för export av en kund:

* Kunden måste ha en giltig e-postadress.
* Ett land/en region har valts på kund kortet för lokala kunder, med tomt land/region det land/den region som har angetts på sidan **företagsinformation** måste ha en definierad ISO-kod.
* Om kunden har ett telefonnummer måste numret vara unikt eftersom Shopify inte ska acceptera ytterligare en kund med samma telefonnummer.
* Om kunden har ett telefonnummer måste det vara i formatet E.164. Olika format stöds om de representerar ett tal som kan ringas upp var som helst i världen. Följande format är giltiga:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

När du har skapat kunderna i Shopify kan du skicka direkt inbjudningar till dem och på så vis uppmuntra dem att aktivera sina konton.

### Fylla i kundinformation i Shopify

En kund i Shopify har förnamn, efternamn, e-post och/eller telefonnummer. Du kan ange förnamn och efternamn baserat på namn på kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Kontaktnamn**|Högsta prioritet om fältet **Kontaktnamn** har fyllts i och fältet **Kontaktkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|2|**Namn 2**|Om fältet **Namn 2** har fyllts i och fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|
|3|**Namn**|Lägsta prioritet om fältet **Namn** har fyllts i och fältet **Namnkälla** på **Shopify-butikskortet** innehåller något av alternativen *Förnamn och efternamn* eller *Efternamn och förnamn*, som anger hur värdena ska delas.|

Det finns också en standardadress för en kund i Shopify. Adressen kan innehålla ett företag och en adress utöver förnamn, efternamn, e-post och/eller telefon. Du kan fylla i fältet **Företag** baserat på data från kundkortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Fält i kundkort|Description|
|------|------|-----------|
|1|**Namn**|Högsta prioritet om fältet **Namnkälla** på **Shopify-butikskortet** innehåller *Företagsnamn*.|
|2|**Namn 2**|Lägsta prioritet om fältet **Källa till namn 2** på **Shopify-butikskortet** innehåller *Företagsnamn*.|

För adresser där delstat/provins används väljer du **Kod** eller **Namn** i fältet **delstatskälla** på sidan **Shopify-butikskort**. Koden eller namnet anger vilken typ av data som lagras i [!INCLUDE[prod_short](../includes/prod_short.md)] i fältet **Delstat**. Kom ihåg att initiera kundmallar per land/region så att delstatskoden/namnmappningen är klar. 


## Synka kunder

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Shopify butik** och väljer sedan relaterad länk.
2. Välj den specifika butik som du vill synkronisera kunder för.
3. Välj åtgärden **Synkronisera kunder**.

Alternativt kan du använda åtgärden **Starta synkronisering av kunder** i fönstret **Shopify-kunder** eller söka efter batchjobbet **Synkronisera kunder**.

Du kan schemalägga uppgifter så att de utförs på ett automatiserat sätt. Läs mer i [Schemalägg återkommande uppgifter](background.md#to-schedule-recurring-tasks).

## Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

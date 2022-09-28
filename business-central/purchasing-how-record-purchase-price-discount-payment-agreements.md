---
title: Registrera speciella inköpspriser och rabatter
description: Du kan definiera olika eller alternativa priser och rabattavtal och koppla dem till inköpsdokument för leverantörer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2b3914f292ca94770694960d4f202f18408b1191
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534568"
---
# <a name="record-special-purchase-prices-and-discounts"></a>Registrera speciella inköpspriser och rabatter

> [!NOTE]
> I 2020 års utgivningscykel 2 släppte vi effektiviserade processer för att ställa in och hantera priser och rabatter. Om du är en ny kund som använder den versionen använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

De olika pris- och rabattavtalen som gäller när artiklar köps in från olika leverantörer måste definieras så att de överenskomna reglerna och värdena används i de inköpsdokument som du skapar för leverantören.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[prod_short](includes/prod_short.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i [bästa prisberäkning](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

När det gäller priser kan du infoga ett särskilt inköpspris på inköpsrader, om en viss kombination av leverantör, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns.

När det gäller rabatter kan du ställa in och använda två olika typer av inköpsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Inköpsradrabatt** |En beloppsrabatt som infogas på inköpsrader, om en viss kombination av leverantör, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. Denna typ fungerar på samma sätt som för inköpspriser. |
| **Fakturarabatt** |En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett inköpsdokument överstiger ett viss minimivärde. |

Eftersom inköpsradrabatter och inköpspriser baseras på en kombination av artikel och leverantör kan du också ställa in den här konfigurationen på det artikelkort där reglerna och värdena har definierats. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Om du vill definiera ett speciellt inköpspris för en leverantör

#### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna det relevanta leverantörskortet och välj sedan åtgärden **Priser.**.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyll i en rad för varje kombination för vilken leverantören beviljar dig en inköpsradrabatt.

#### <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Välj leverantör och sedan åtgärden **Försäljningsprislistor**.
3. Välj **Ny** för att skapa en ny inköpsprislista.
4. På snabbflikarna **Allmänt** och **Moms** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Om du vill lägga till objekt i listan gör du något av följande:
   * Om du vill lägga till många objekt väljer du **Föreslå rader** och anger sedan filtervillkor för att ange vilka typer av objekt som ska läggas till. Du kan också ange ytterligare inställningar för de artiklar som är specifika för prislistan. Du kan ändra dessa senare vid behov.
   * Om du vill kopiera artiklar från en annan prislista väljer du **Kopiera rader** och väljer sedan den prislista som ska kopieras.
   * Om du vill lägga till artiklar manuellt väljer du fältet **Produkttyp** och den produkttyp som prislistan är avsedd för. Beroende på dina val fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om du vill börja använda prislistan går du till fältet **Status** och väljer **Aktiv**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Om du vill definiera en radrabatt för en leverantör

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna det relevanta leverantörskortet och välj sedan åtgärden **Radrabatter.**.

   Fältet **Inköpsleverantörsnr** är förifyllt med leverantörsnumret.
3. Fyll i fälten på den första raden efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyll i en rad för varje kombination för vilken leverantören beviljar dig en inköpsradrabatt.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Så här definierar du radrabatt för en leverantör

När dina leverantörer har informerat dig om vilka fakturarabatter som de beviljar, skriver du fakturarabattkoderna på leverantörskorten och lägger upp villkoren för respektive kod.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna leverantörskortet för en leverantör som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för leverantören.

    > [!NOTE]  
    > Fakturarabattkoder representeras av befintliga leverantörskort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till leverantörer, genom att välja namnet på en andra leverantörer som ska ha dessa villkor.

    Så här definierar du fakturarabattvillkor för inköp:
4. På sidan **Leverantörskort** väljer du åtgärden **Fakturarabatter**. Sidan **Leverantörsfakturarabatter** öppnas.
5. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i SEK.
6. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
7. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
8. Upprepa steg 5 till och med 7 för varje valuta som leverantören ska ta emot en annan fakturarabatt för.

Fakturarabatten ställs nu in i fältet och fördelas till leverantören i fråga. När du väljer leverantörkoden i fältet **Fakturarabattkod** på andra leverantörskort, kopplas samma fakturarabatt till dessa leverantörer.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Så här väljer du princip för bokföring av inköpsrabatter:

När du bokför en inköpsfaktura som innehåller en eller flera rabatter kan du välja mellan två principer för bokföringen av rabattbeloppen. Du kan bokföra rabatter separat eller dra dem från fakturarabatterna.  

Innan du kan göra detta måste du redan ha definierat de nödvändiga kontona för bokföring av rabattbelopp i kontoplanen. Du måste också kontrollera att du har angett rätt kontonummer i bokföringsinställningarna i fälten **Inköpsradrabatt** och **Inköpsfakturarabatt**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inköpsinställningar** och väljer sedan relaterad länk.
2. I fältet **Rabattbokföring** väljer du en av följande principer för bokföring av rabatter.

|**Princip för rabattbokföring**|**Fakturarabatt**|**Radrabatt**|  
|------------------------------------|--------------------------|-----------------------|  
|**Samtliga rabatter**|Bokförd separat|Bokförd separat|  
|**Fakturarabatter**|Bokförd separat|Subtraherade|  
|**Radrabatter**|Subtraherade|Bokförd separat|  
|**Ingen rabatt**|Subtraherade|Subtraherade|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Inköpsfakturarabatter och faktureringsavgifter

Om bestämda villkor för fakturarabatter gäller vid inköp från vissa leverantörer kan du ange dessa för motsvarande leverantörer. Rabatten kan sedan beräknas automatiskt när du fyller i inköpsfakturor.  

Innan du kan använda fakturarabatter vid inköp måste du ange vilka leverantörer som erbjuder rabatterna.  

Du kan koppla rabattsatser till särskilda fakturabelopp på sidan **Leverantörsfakturarabatter**. Varje kund kan ha en separat sida. Alternativt kan du koppla flera leverantörer till samma sida.  

Förutom en procentuell rabatt kan du koppla en faktureringsavgift till ett särskilt fakturabelopp.  

Du kan definiera villkoren för fakturarabatten i BVA för inrikes leverantörer och i utländsk valuta för utrikes leverantörer.  

Du kan ange att fakturarabatterna för offerter, avropsorder, order, fakturor eller kreditnotor ska beräknas automatiskt med [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!TIP]  
> Innan du anger den här informationen i programmet kan det vara praktiskt att skapa ett utkast av den rabattstruktur som du vill använda. På så sätt blir det lättare att se vilka leverantörer som kan kopplas till samma fakturarabattsida. Ju färre sidor som behöver definieras, ju snabbare går det att ange basinformationen.

## <a name="best-price-calculation"></a>Bästa prisberäkning

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[prod_short](includes/prod_short.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader.

Det bästa priset är det lägsta tillåtna priset med den högsta tillåtna radrabatten för ett visst datum. [!INCLUDE[prod_short](includes/prod_short.md)] beräknar automatiskt priset när du skriver in enhetspriset och radrabattens procentsats för artiklar på nytt dokument och journalrader.

> [!NOTE]  
> Följande beskriver hur det bästa priset beräknas för försäljning. Beräkningen är samma för inköp.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande villkor:

    - Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    - Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    - Ligger orderdatumet (eller fakturans och kreditnotans bokföringsdatum) inom avtalet om priser eller radrabatter?
    - Har någon enhetskod angetts? I så fall gör [!INCLUDE[prod_short](includes/prod_short.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrolelrar om pris/rabattavtal tillämpas på uppgifter i dokumentet eller journalen och infogar det tillämpliga enhetspriset och radrabattens procentsats enligt följande villkor:

    - Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    - Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i BVA. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[prod_short](includes/prod_short.md)] det lägsta priset och den högsta radrabatten i BVA.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/set-up-prices-discounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Ställa in inköp](purchasing-setup-purchasing.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

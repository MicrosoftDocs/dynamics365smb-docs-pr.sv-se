---
title: "Ställ in särskilda och alternativa priser och rabatter för leverantörer | Microsoft Docs"
description: "Du kan definiera olika eller alternativa priser och rabattavtal och koppla dem till inköpsdokument för leverantörer."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0a718c45256a1e7cc7fbde794491814f1c26dd4a
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="record-special-purchase-prices-and-discounts"></a>Registrera speciella inköpspriser och rabatter
De olika pris- och rabattavtalen som gäller när artiklar köps in från olika leverantörer måste definieras så att de överenskomna reglerna och värdena används i de inköpsdokument som du skapar för leverantören.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i avsnittet "Bästa prisberäkning".

När det gäller priser kan du infoga ett särskilt inköpspris på inköpsrader, om en viss kombination av leverantör, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns.

När det gäller rabatter kan du ställa in och använda två olika typer av inköpsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Inköpsradrabatt** |En beloppsrabatt som infogas på inköpsrader, om en viss kombination av leverantör, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. Detta fungerar på samma sätt som för inköpspriser. |
| **Fakturarabatt** |En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett inköpsdokument överstiger ett viss minimivärde. |

Eftersom inköpsradrabatter och inköpspriser baseras på en kombination av artikel och leverantör kan du också ställa in den här konfigurationen på det artikelkort där reglerna och värdena har definierats. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Om du vill definiera ett speciellt inköpspris för en leverantör
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörer** och välj sedan relaterad länk.
2. Öppna det relevanta leverantörskortet och välj sedan åtgärden **Priser.**.

    Fältet **Inköpstyp** är förifyllt med **leverantör** och fältet **inköpskod** är förifyllt med leverantörsnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyll i en rad för varje kombination för vilken leverantören beviljar dig en inköpsradrabatt.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Om du vill definiera en radrabatt för en leverantör
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörer** och välj sedan relaterad länk.
2. Öppna det relevanta leverantörskortet och välj sedan åtgärden **Radrabatter.**.

    Fältet **Inköpstyp** är förifyllt med **leverantör** och fältet **inköpskod** är förifyllt med leverantörsnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyll i en rad för varje kombination för vilken leverantören beviljar dig en inköpsradrabatt.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Så här definierar du radrabatt för en leverantör
När dina leverantörer har informerat dig om vilka fakturarabatter som de beviljar, skriver du fakturarabattkoderna på leverantörskorten och lägger upp villkoren för respektive kod.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörer** och välj sedan relaterad länk.
2. Öppna leverantörskortet för en leverantör som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för leverantören.

    > [!NOTE]  
    >   Fakturarabattkoder representeras av befintliga leverantörskort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till leverantörer, genom att välja namnet på en andra leverantörer som ska ha dessa villkor.

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

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsinställningar** och välj sedan relaterad länk.
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

 Du kan ange att fakturarabatterna för offerter, avropsorder, order, fakturor eller kreditnotor ska beräknas automatiskt med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Innan du anger den här informationen i programmet kan det vara praktiskt att skapa ett utkast av den rabattstruktur som du vill använda. På så sätt blir det lättare att se vilka leverantörer som kan kopplas till samma fakturarabattsida. Ju färre sidor som behöver definieras, ju snabbare går det att ange basinformationen.

## <a name="best-price-calculation"></a>Bästa prisberäkning
När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader.

Det bästa priset är det lägsta tillåtna priset med den högsta tillåtna radrabatten för ett visst datum. [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar automatiskt detta när du skriver in enhetspriset och radrabattens procentsats för artiklar på nytt dokument och journalrader.

> [!NOTE]  
>   Följande beskriver hur det bästa priset beräknas för försäljning. Beräkningen är samma för inköp.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar kombinationen av faktureringskund och artikel och beräknar sedan tillämpligt enhetspris och radrabattens procentsats utifrån följande villkor:

    - Finns det ett särskilt avtal om priser eller radrabatter för den här kunden, eller tillhör kunden en grupp som har ett sådant avtal?
    - Ingår artikeln eller artikelrabattgruppen på raden i något av dessa pris-/rabatt-avtal?
    - Ligger orderdatumet (eller fakturans och kreditnotans bokföringsdatum) inom avtalet om priser eller radrabatter?
    - Har någon enhetskod angetts? I så fall gör [!INCLUDE[d365fin](includes/d365fin_md.md)] en sökning efter priser eller rabatter med samma enhetskod och efter priser eller rabatter som saknar enhetskod.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolelrar om pris/rabattavtal tillämpas på uppgifter i dokumentet eller journalen och infogar det tillämpliga enhetspriset och radrabattens procentsats enligt följande villkor:

    - Finns det krav på en lägsta kvantitet i pris-/ rabattavtalet som är uppfyllda?
    - Finns det krav på valuta i pris-/ rabattavtalet som är uppfyllda? I så fall infogas det lägsta priset och den högsta radrabatten för den valutan, även om de skulle ge ett bättre pris i BVA. Om det inte finns några pris-/rabattavtal för den angivna valutakoden infogar [!INCLUDE[d365fin](includes/d365fin_md.md)] det lägsta priset och den högsta radrabatten i BVA.

Om inga specialpriser kan beräknas för artiklarna på raden infogas antingen det senaste inköpspriset eller à-priset från artikelkortet.

## <a name="see-also"></a>Se även
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


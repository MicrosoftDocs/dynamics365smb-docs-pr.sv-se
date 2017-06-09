---
title: "Så här registrerar du speciella inköpspriser och rabatter| Microsoft Docs"
description: "Så här registrerar du inköpspriser och rabatter"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Så här registrerar du speciella inköpspriser och rabatter
De olika pris- och rabattavtalen som gäller när artiklar köps in från olika leverantörer måste definieras så att de överenskomna reglerna och värdena används i de inköpsdokument som du skapar för leverantören.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i [Avancerat: bästa prisberäkning ](advanced-best-price-calculation.md).

När det gäller priser kan du infoga ett särskilt inköpspris på inköpsrader, om en viss kombination av leverantör, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns.

När det gäller rabatter kan du ställa in och använda två olika typer av inköpsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Inköpsradrabatt** |En beloppsrabatt som infogas på inköpsrader, om en viss kombination av leverantör, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. Detta fungerar på samma sätt som för inköpspriser. |
| **Fakturarabatt** |En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett inköpsdokument överstiger ett viss minimivärde. |

Eftersom inköpsradrabatter och inköpspriser baseras på en kombination av artikel och leverantör kan du också ställa in den här konfigurationen på det artikelkort där reglerna och värdena har definierats. Mer information finns i [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Om du vill definiera ett speciellt inköpspris för en leverantör
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Leverantörer**, och välj sedan relaterad länk.
2. Öppna det relevanta leverantörskortet och välj sedan åtgärden **Priser.**.

    Fältet **Inköpstyp** är förifyllt med **leverantör** och fältet **inköpskod** är förifyllt med leverantörsnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyll i en rad för varje kombination för vilken leverantören beviljar dig en inköpsradrabatt.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Om du vill definiera en radrabatt för en leverantör
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Leverantörer**, och välj sedan relaterad länk.
2. Öppna det relevanta leverantörskortet och välj sedan åtgärden **Radrabatter.**.

    Fältet **Inköpstyp** är förifyllt med **leverantör** och fältet **inköpskod** är förifyllt med leverantörsnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyll i en rad för varje kombination för vilken leverantören beviljar dig en inköpsradrabatt.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Så här definierar du radrabatt för en leverantör
När dina leverantörer har informerat dig om vilka fakturarabatter som de beviljar, skriver du fakturarabattkoderna på leverantörskorten och lägger upp villkoren för respektive kod.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Leverantörer**, och välj sedan relaterad länk.
2. Öppna leverantörskortet för en leverantör som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för leverantören.

    **Obs!** Fakturarabattkoder representeras av befintliga leverantörskort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till leverantörer, genom att välja namnet på en andra leverantörer som ska ha dessa villkor.

    Så här definierar du fakturarabattvillkor för inköp:
4. I fönstret **leverantörskort** väljer du åtgärden **Fakturarabatter**. Fönstret **Leverantörsfakturarabatter** öppnas.
5. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i USD.
6. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
7. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
8. Upprepa steg 5 till och med 7 för varje valuta som leverantören ska ta emot en annan fakturarabatt för.

Fakturarabatten ställs nu in i fältet och fördelas till leverantören i fråga. När du väljer leverantörkoden i fältet **Fakturarabattkod** på andra leverantörskort, kopplas samma fakturarabatt till dessa leverantörer.

## <a name="see-also"></a>Se även
[Avancerad: Bästa prisberäkning](advanced-best-price-calculation.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


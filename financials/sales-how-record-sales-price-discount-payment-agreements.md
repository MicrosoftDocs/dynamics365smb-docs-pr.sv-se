---
title: "Så här registrerar du speciella försäljningsspriser och rabatter | Microsoft Docs"
description: "Så här registrerar du speciella försäljningspriser och rabatter"
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
ms.openlocfilehash: 5ceddded2f95e15a6a7449bf2776b7776ce8a55c
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Så här registrerar du speciella försäljningspriser och rabatter
De olika pris- och rabattavtalen som gäller när du säljer till olika kunder måste definieras så att de överenskomna reglerna och värdena tillämpas på de försäljningsdokument som du skapar för kunden.

När du har registrerat särskilda priser och radrabatter för försäljning och inköp, ser [!INCLUDE[d365fin](includes/d365fin_md.md)] till att din vinst på artikelhandel alltid är optimal genom att automatiskt beräkna det bästa priset på försäljnings- och inköpsdokument och i artikeljournalrader. Mer information finns i [Avancerat: bästa prisberäkning ](advanced-best-price-calculation.md).

När det gäller priser kan du infoga ett särskilt försäljningspris på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns.

När det gäller rabatter kan du ställa in och använda två olika typer av försäljningsrabatter:

| Rabattyp | Beskrivning |
| --- | --- |
| **Förs.radrabatt** |En beloppsrabatt som infogas på försäljningsrader, om en viss kombination av kund, artikel, minsta kvantiteten, måttenhet eller start-/slutdatum finns. En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett försäljningsdokument överstiger ett viss minimivärde. |
| **Fakturarabatt** |En procentrabatt som dras av från dokumentets summa om värdebeloppet för alla rader i ett inköpsdokument överstiger ett viss minimivärde. |

Eftersom försäljningsradrabatter och försäljningspriser baseras på en kombination av artikel och kund, kan du också utföra den här konfigurationen från artikelkortet för artikeln när reglerna och värdena gäller.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Så här skapar du försäljningspriser för en kund:
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kunder**, och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Priser.**.

    Fältet **Förs.typ** är ifyllt med aktuell **kund **och fältet **Förs.kod **innehåller kundnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja ett speciellt försäljningspris till kunden.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Så här skapar du försäljningsradrabatter för en kund
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kunder**, och välj sedan relaterad länk.
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Radrabatter.**.

    Fältet **Förs.typ** är ifyllt med aktuell **kund **och fältet **Förs.kod **innehåller kundnumret.
3. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll i en rad för varje kombination som ska bevilja en speciell försäljningsradrabatt till kunden.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Så här definierar du radrabatt för en kund
När du har bestämt vilka kunder som är aktuella för fakturarabatter, skriver du fakturarabattkoderna på kundkorten och lägger upp villkoren för respektive kod.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kunder**, och välj sedan relaterad länk.
2. Öppna kundkortet för en kund som är aktuell för fakturarabatter.
3. Välj i fältet  **Fakturarabattkod** koden för den fakturarabatt som ska användas vid beräkning av fakturarabatter för kunden.

    **Obs!** Fakturarabattkoder representeras av befintliga kundkort. Detta aktiverar dig att snabbt tilldela fakturarabattvillkor till kunder, genom att välja namnet på en andra kunder som ska ha dessa villkor.

    Så här definierar du fakturarabattvillkor för försäljning:
4. I fönstret **Kundkort** väljer du åtgärden **Fakturarabatter**. Fönstret **Kundfakturarabatter** öppnas.
5. Ange valutakoden som du vill definiera fakturarabattvillkor för i fältet **Valutakod**. Lämna det här fältet tomt om du vill ange fakturarabattvillkor i USD.
6. Ange i fältet **Minimibelopp** det minsta belopp som en faktura måste vara på för att komma i fråga för rabatt.
7. Fakturarabatten beräknas som en procentandel av fakturabeloppet i fältet **Rabatt %**.
8. Upprepa steg 5 till och med 7 för varje valuta som kunden ska ta emot en annan fakturarabatt för.

Fakturarabatten ställs nu in i fältet och fördelas till kunden i fråga. När du väljer kundkoden i fältet **Fakturarabattkod** på andra kundkort, kopplas samma fakturarabatt till dessa kunder.

## <a name="see-also"></a>Se även
[Avancerad: Bästa prisberäkning](advanced-best-price-calculation.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


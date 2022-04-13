---
title: Skapa koder för granskningshistorik
description: Lära dig mer om aktiviteterna för att ställa in ursprungskoder och orsakskoder som du kan använda för att spåra granskningshistorik.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.search.form: 257, 259, 279
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08545d1bb23b8a70d10c6114f4840ce186aa94cc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515569"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Ställa in ursprungskoder och orsakskoder för granskningshistorik

Alla bokförda transaktioner tilldelas automatiskt en ursprungskod så att transaktionerna kan spåras till dess ursprung. Om du vill ge transaktionerna en extra ursprungskod kan du använda uppföljningskoder. Uppföljningskoder används för att ange varför en transaktion har upprättats. När du skapar uppföljningskoder kan du tilldela dem till hela journalmallar och journaler, och du kan tilldela dem till enskilda journalrader och dokument.  

För både ursprungskoder och orsakskoder bör du använda koder som är lätta att komma ihåg och som är beskrivande. Koden måste vara unik och du kan registrera så många koder du vill.

## <a name="define-source-codes"></a>Definiera ursprungskoder

Ibland behöver du se hur en viss transaktion uppstod, t. ex. om den har sitt ursprung i en redovisningsjournal eller en inköpsfaktura. En ursprungskod anger var en transaktion har skapats. Transaktioner skapas när journaler och fakturor bokförs och när vissa batch-jobb körs. Varje bokföringstyp har en specifik ursprungskod som tilldelas när enskilda transaktioner skapas.  

Bokföring av journaler, order, fakturor eller kreditnotor, och körningar av olika batch-jobb, skapar transaktioner i räkenskaperna. Fönstret **Ursprungskodinställningar** innehåller flera snabbflikar, en för varje modul. Varje snabbflik innehåller ursprungskoder som gäller för den modulen.

När du bokför, eller kör ett batch-jobb, kompletterar programmet automatiskt transaktionen med rätt ursprungskod. När du t. ex. bokför en redovisningsjournal, kodar programmet transaktionen som *REDOVJNL*. Du kan sedan filtrera sidan **redovisningstransaktioner** för att visa vilka transaktioner som bokförts från redovisningsjournalen eller från försäljningsdokument, t. ex.

### <a name="to-define-source-codes"></a>Så här definierar du ursprungskoder

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Ursprungskodinställningar** och väljer sedan relaterad länk.  

2. I fönstret **Ursprungskodinställningar** för varje bokföringstyp och batch-jobb, ange relevant källkod.  

Du kan ändra innehållet i ett fält senare, så att ändringen påverkar framtida bokföringar.

## <a name="change-source-codes"></a>Ändra ursprungskoder

Det kan hända att du vill ändra en ursprungskod. Du kanske t. ex. vill ändra ursprungskoden *GENJNL* till *GNJ*.

### <a name="to-change-source-codes"></a>Så här ändrar du ursprungskoder

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **ursprungskoder** och väljer sedan relaterad länk.

2. På raden med den kod som ska ändras markerar du koden i fältet **Kod**.

3. Ange en ny kod och klicka sedan på **Ja**. Du kan också ändra innehållet i fältet **Beskrivning**.

Alla nya transaktioner som har bokförts från redovisningsjournalen får den nya ursprungskoden.

## <a name="define-reason-codes"></a>Definiera uppföljningskoder

Uppföljningskoderna kompletterar ursprungskoderna och används för att ange varför en transaktion har upprättats. Du kan tilldela uppföljningskoder på enskilda transaktioner och du kan tilldela permanenta koder för särskilda journalmallar och journaler. När en uppföljningskod kopplas till en journalrad eller ett försäljnings- eller inköpshuvud, kommer programmet att märka alla transaktionerna med den angivna uppföljningskoden när de bokförs.  

### <a name="to-set-up-reason-codes"></a>Så här lägger du upp uppföljningskoder

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport")  anger du **orsakskoder** och väljer sedan relaterad länk.

2. I fönstret **uppföljningskoder** anger du den första koden i fältet **kod**. Skriv in en beskrivning i fältet **Beskrivning**.

Upprepa den här proceduren för alla koder som du vill använda. Du kan skapa så många koder du vill.

I följande procedur beskrivs hur du lägger till en uppföljningskod i en journalmall, men liknande åtgärder gäller för att lägga till en uppföljningskod till en journalrad eller journal.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>Så här tilldelar du uppföljningskoder till journalmallar

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport")  anger du **Redovisningsjournalmallar** och väljer sedan relaterad länk.

2. Ange relevant kod i fältet **Uppföljningskod** på raden med journalmallen.

3. Stäng journalmallen.

Den valda uppföljningskoden kopieras till nya journaler som skapas med den här journalmallen. Du kan tilldela uppföljningskoder till journalmallar i andra moduler på samma sätt.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Så här använder du uppföljningskoder i försäljnings- och inköpsdokument

1. Öppna relevant försäljnings- eller inköpsdokument.

2. Ange koden i fältet **Uppföljningskod** i försäljnings- eller inköpshuvudet.

När fakturan bokförs kopieras uppföljningskoden till alla redovisnings-, kund- och leverantörstransaktioner. Du kan inte tilldela olika uppföljningskoder till de enskilda inköps- och försäljningsraderna eftersom alla rader bokförs som en transaktion.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
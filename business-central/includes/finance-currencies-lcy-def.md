---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
---
Eftersom företag verkar i fler länder/regioner blir det viktigt att de kan handla och rapportera ekonomisk information i fler än en valuta. Den lokala valutan (BVA) definieras på sidan **Redovisningsinställningar** enligt beskrivningen i artikeln [Att förstå redovisning och kontoplan](../finance-general-ledger.md). När den lokala valutan (BVA) har definierats visas den som en tom valuta, så när fältet **Valuta** är tomt betyder det att valutan är BVA.  

Sedan måste du registrera valutakoder för varje valuta du använder om du köper eller säljer i andra valutor än den lokala valutan (BVA). Du kan även skapa bankkonton med hjälp av valutor. Du kan dock registrera redovisningstransaktioner i olika valutor, men redovisningstransaktionen bokförs alltid i lokal valuta (BVA).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Din redovisning ställs in för att använda den lokala valutan (BVA), men du kan ställa in den så att den använder en annan valuta med en tilldelad valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[prod_short](prod_short.md)] att registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion samt för andra transaktioner, t. ex. momstransaktioner. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](../finance-how-setup-additional-currencies.md). Den alternativa rapporteringsvalutan används oftast för att underlätta ekonomisk rapportering till ägare som finns i länder/regioner som använder andra valutor än den lokala valutan (BVA).  

> [!IMPORTANT]
> Om du vill använda en alternativ rapporteringsvaluta för ekonomisk rapportering måste du känna till begränsningarna. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> När du bokför i redovisning med hjälp av en valutakod, till exempel för att bokföra en utgift i en redovisningsjournal med en valutakod, konverteras transaktionen till BVA med hjälp av valutakursen för bokföringsdatumet. Redovisningstransaktionen kommer inte att innehålla information om vilken valuta som har använts, bara dess värde i BVA. Om du vill kunna spåra originalvalutan, till exempel för en faktura, måste du använda både försäljnings-och inköpsdokument samt bankkonton som lagrar information om valutakod för transaktionerna.

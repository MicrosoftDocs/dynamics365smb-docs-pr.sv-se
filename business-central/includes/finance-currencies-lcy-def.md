---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Om ditt företag är verksamt i mer än ett land eller en region är det förmodligen viktigt att du kan göra affärer i mer än en valuta. Du definierar din lokala valuta (BVA) på sidan **Redovisningsinställningar**. Därefter representeras din lokala valuta som tom valuta i dokument och transaktioner. När fältet **Valuta** är tomt är valutan BVA.

Följande video förklarar hur du ställer in din lokala valuta.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Sedan måste du registrera valutakoder för varje valuta du använder om du köper eller säljer i andra valutor än den lokala valutan (BVA). Du kan även skapa bankkonton med hjälp av valutor. Du kan dock registrera redovisningstransaktioner i olika valutor, men redovisningstransaktionen bokförs alltid i lokal valuta (BVA).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Din redovisning ställs in för att använda den lokala valutan (BVA), men du kan ställa in den så att den använder en annan valuta med en tilldelad valutakurs. Genom att ange en andra valuta som en så kallad alternativ rapporteringsvaluta kommer [!INCLUDE[prod_short](prod_short.md)] att registrera belopp automatiskt i både BVA och den alternativa rapporteringsvalutan för varje redovisningstransaktion samt för andra transaktioner, t. ex. momstransaktioner. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](../finance-how-setup-additional-currencies.md). Den alternativa rapporteringsvalutan används oftast för att underlätta ekonomisk rapportering till ägare som finns i länder/regioner som använder andra valutor än den lokala valutan (BVA).  

> [!IMPORTANT]
> Om du vill använda en alternativ rapporteringsvaluta för ekonomisk rapportering måste du känna till begränsningarna. Mer information finns i [Ställa in en alternativ rapporteringsvaluta](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> När du bokför i redovisningen med en utländsk valuta [!INCLUDE [prod_short](prod_short.md)] omvandlas transaktionen till BVA med hjälp av bokföringsdatumets valutakurs. Redovisningstransaktionen kommer inte att innehålla information om vilken valuta som har använts, bara dess värde i BVA. För att hålla reda på den ursprungliga valutan, använd försäljnings- och inköpsdokumenten och bankkonton som lagrar valutainformation för poster.

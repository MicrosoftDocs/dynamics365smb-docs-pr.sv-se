---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

## Metodtips för att arbeta med kolumndefinitioner

Kolumndefinitioner versionshanteras inte. När du ändrar en kolumndefinition ersätts den gamla versionen när ändringen sparas i databasen. Följande lista innehåller några metodtips för hur du arbetar med kolumndefinitioner.

- Om du lägger till kolumndefinitioner väljer du en bra kod och fyller i beskrivningsfältet med en meningsfull text samtidigt som du vet vad du använder kolumndefinitionen till. Den här informationen hjälper dina medarbetare (och ditt framtida jag) att arbeta med ekonomiska rapporter och kanske ändra kolumndefinitionen.
- Innan du ändrar en kolumndefinition bör du överväga att ta en kopia av den som säkerhetskopia, ifall ändringen inte fungerar som förväntat. Du kan antingen bara kopiera definitionen (ge den ett bra namn) eller exportera den. För mer information går du till [Importera eller exportera kolumndefinitioner](#import-or-export-financial-report-column-definitions).
- Om du behöver en ny kopia av en definition som [!INCLUDE [prod_short](prod_short.md)] tillhandahåller är ett enkelt sätt att skapa ett nytt företag som bara innehåller inställningsdata. Exportera sedan definitionen och importera den till det företag där definitionen behöver uppdateras.
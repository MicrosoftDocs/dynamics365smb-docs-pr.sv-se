---
ms.service: dynamics-365-business-central
---
> [!NOTE]
> Det var möjligt att hämta data från olika företag i en enda rapport med OData-webbtjänster. Eftersom sedan [!INCLUDE [prod_short](prod_short.md)] 2021 utgivningscykel 2 stöds endast ODataV4, som inte exporterar data från flera företag. Funktionen **$expand** i Power BI som du kanske tror är ett alternativt sätt att skapa en rapport för flera företag, kan inte heller användas. En kolumn skapas med företagsnamnet, men den fylls inte med företagsdata efter en uppdatering.
---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!NOTE]
> När du kopierar ett företag i en miljö där Dataverse eller Försäljningsintegrering är aktiverad [!INCLUDE [prod_short](prod_short.md)] rensas följande inställningar vid kopiering till målföretaget:
>
> * Dataverse och Dynamics-anslutningsinställningar för att säkerställa att integrationen återinitieras korrekt i målföretaget.
> * Integrationsposter för att säkerställa att målföretaget inte pekar på poster som är kopplade i källföretaget.
> * Integreringssynkroniseringsjobb för att stoppa synkroniseringsbakgrundsjobb.
> * Synkroniseringsfel, om de finns, pekar på fel i källföretaget och skulle bara betraktas som brus i målföretaget.
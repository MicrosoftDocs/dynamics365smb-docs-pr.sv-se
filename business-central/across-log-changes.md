---
title: Spåra användaraktivitetet i en ändringslogg | Microsoft Docs
description: Du kan aktivera en användarlogg så att du har en historik över alla ändringar som gjorts i spårade tabeller.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.openlocfilehash: 2a71909faf66c13a0923a10bfc12369127642875
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/19/2019
ms.locfileid: "852896"
---
# <a name="auditing-changes-in-business-central"></a>Revision av ändringar i Business Central

Du kan aktivera ändringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att du får en historik över aktiviteter. Loggen är baserad på ändringar av data i tabeller som du spårar. På sidan **Poster i ändringslogg** sorteras poster kronologiskt och visar de ändringar som har gjorts i fälten i de angivna posterna. I ändringsloggen samlas alla ändringar som gjorts i tabellen.

> [!Important]
> En användares ändringar visas inte i **ändringsloggtransaktioner** förrän sessionen har startats om, vilket sker i följande fall:
<br />
> * Sessionen har upphört att gälla och har uppdaterats.
> * Användaren valde ett annat företag eller rollcenter.
> * Den användaren har loggat ut och in igen.

## <a name="working-with-the-change-log"></a>Arbeta med ändringsloggen

Ett vanligt problem i många ekonomisystem är att ta reda på var fel och ändringar av data har sina ursprung. Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen. Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen. Du måste ange vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen.  

Du aktiverar och avaktiverar ändringsloggen på sidan **Ändringslogg inställning**. När en användare aktiverar eller inaktiverar ändringsloggen, loggas denna aktivitet så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen.

På sidan **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[d365fin](includes/d365fin_md.md)] spårar även nummer av systemtabeller.

När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen på sidan **Ändringslogg transaktioner**. Om du vill ta bort transaktioner kan du göra det på sidan **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.  

## <a name="see-also"></a>Se även
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Med hjälp av Berätta för att hitta funktioner och Information](ui-search.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

---
title: "Spåra användaraktivitetet i en ändringslogg | Microsoft Docs"
description: "Du kan aktivera en användarlogg så att du har en historik över alla ändringar som gjorts i spårade tabeller."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a>Logga ändringar i Business Central
Du kan aktivera ändringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att du får en historik över aktiviteter. Loggen är baserad på ändringar av data i tabeller som du spårar. I ändringsloggen sorteras poster kronologiskt och visar de ändringar som har gjorts i fälten i de angivna posterna. I ändringsloggen samlas alla ändringar som gjorts i tabellen.  

## <a name="working-with-the-change-log"></a>Arbeta med ändringsloggen
Ett vanligt problem i många ekonomisystem är att ta reda på var fel och ändringar av data har sina ursprung. Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen. Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen. Du måste ange vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen.  

Du aktiverar och avaktiverar ändringsloggen i fönstret **Ändringslogg inställning**. Du kan aktivera eller inaktivera ändringsloggen, denna aktivitet loggas så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen. Denna loggningsfunktion går inte att stänga av.  

I fönstret **Ändringslogginställningar** om du väljer åtgärden **Tabeller** kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[d365fin](includes/d365fin_md.md)] spårar även nummer av systemtabeller.

När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen i fönstret **Ändringslogg transaktioner**. Om du vill ta bort transaktioner kan du göra det i fönstret **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.  

## <a name="see-also"></a>Se även
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Använda Söka efter sida eller rapport](ui-search.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


---
title: "Logga ändringar i Dynamics 365 for Financials | Microsoft Docs"
description: "Logga ändringar som görs av användare."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 03/04/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 470931febc303ace8fa1e8015453c20b587762b0
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a>Logga ändringar i Dynamics 365 for Financials
Du kan aktivera ändringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)] så att du får en historik över aktiviteter. Loggen baseras på ändringar som gjorts till data i tabellerna, som du spårar. I ändringsloggen sorteras kronologiskt och visas de ändringar som gjorts i fälten på de angivna tabellerna. I ändringsloggen samlas alla ändringar som gjorts i tabellen.  

## <a name="working-with-the-change-log"></a>Arbeta med ändringsloggen
Ett vanligt problem i många ekonomisystem är att ta reda på var fel och ändringar av data har sina ursprung. Det kan vara allt från ett felaktigt kundtelefonnummer till en felaktig bokföring i redovisningen. Med ändringsloggen kan du spåra alla direkta ändringar som användare gör av data i databasen. Du måste ange vad du vill att systemet ska logga för varje tabell och fält och därefter måste du aktivera ändringsloggen.  

Du aktiverar och avaktiverar ändringsloggen i fönstret **Ändringslogg inställning**. Du kan aktivera eller inaktivera ändringsloggen, denna aktivitet loggas så du kan alltid se vilken användare som har inaktiverat respektive återaktiverat ändringsloggen. Denna loggningsfunktion går inte att stänga av.  

I fönstret **ändringslogginställningar** om du väljer åtgärden **tabeller**, kan du ange vilka tabeller som du vill spåra ändringar för och vilka ändringar som ska spåras. [!INCLUDE[d365fin](includes/d365fin_md.md)] spårar också flera systemregister.

När du har skapat ändringsloggen och aktiverat den, och gjort en ändring av data, kan du visa och filtrera ändringen i fönstret **Ändringslogg transaktioner**. Om du vill ta bort transaktioner kan du göra det i fönstret **ta bort ändringsloggtransaktioner**, där du kan ange filter baserat på datum och tider.  

## <a name="see-also"></a>Se även
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Sortering](ui-sorting.md)  
[Använda Sök efter sida eller rapport](ui-search.md)  
[Så här hanterar du användare och behörigheter](ui-how-users-permissions.md)    
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


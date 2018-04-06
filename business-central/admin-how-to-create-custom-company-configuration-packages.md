---
title: "Så här skapar du anpassade konfigurationspaket för företag | Microsoft Docs"
description: "När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder. Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7feaa0e41cf5800ffd51d5807a90f6929492804e
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a>Så här skapar du anpassade konfigurationspaket för företag
När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder. Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning.  

I allmänhet skapar du ett konfigurationspaket per funktionellt område, till exempel ett paket för din produktionsfunktion. Då kan du koppla och skapa nya områden i företaget efter behov  

En annan metod är att skapa ett paket som innehåller tabellerna för definition av inställningen. Exempel:  

-   Anläggningstillgånginställningar  
-   Redovisningsinställningar  
-   Lagerinställningar  
-   Produktionsinställningar  
-   Inköpsinställningar  
-   Marknadsföringsinställningar  
-   Serviceinställningar  
-   Försäljningsinställningar  
-   Lagerstyrningsinställningar  
-   Bokföringsinställningar  
-   Bokföringsinställningar för moms  
-   Lagerbokföringsinställning  

För att visa en fullständig list över inställningstabeller väljer du ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), öppnar **Inställningar** och väljer sedan relaterad länk.  

## <a name="to-create-a-custom-company-configuration-package"></a>Så här skapar du ett anpassat konfigurationspaket för företag  
1.  Skapa en ny [!INCLUDE[d365fin](includes/d365fin_md.md)]. ***INTE MÖJLIGT Länk till hjälp för ”Skapa en ny klientorganisation***.   
2.  Skapa ett nytt företag bransch- eller lösningsmallen. För mer information, se [Skapa ett nytt företag](admin-how-to-create-a-new-company.md).  
3.  Ställ in det nya företaget efter behov. Fyll i alla inställningstabeller som behövs.  
4.  Öppna det nya företaget.
5. Öppna fönstret **Konfigurationskalkylark**.  
6.  Lägg till tabellerna som du vill överföra till ett annat företag i kalkylarket. Tilldela kalkylarksraderna till paketet.  
7.  Skapa ett frågeformulär för de mest använda inställningstabellerna.  
8.  Skapa konfigurationsmallar för att göra det lättare att skapa huvuddata, som för kunder eller artiklar.  
9.  Exportera ditt paket som en rapidstart-fil.  

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


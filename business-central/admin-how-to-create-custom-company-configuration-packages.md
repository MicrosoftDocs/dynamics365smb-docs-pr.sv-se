---
title: Så här skapar du anpassade konfigurationspaket för företag | Microsoft Docs
description: När verksamheten växer, kommer du antagligen att behöva förlita dig på en uppsättning företagstyper som du använder med de flesta av dina kunder. Du kan rationalisera implementeringsprocessen genom att omvandla dessa typer till företagskonfigurationspaket som är tillgängliga för återanvändning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 511281b5f4d8c7437324ed123a5a5a62bd4cc51d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783663"
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

För att se en komplett lista över inställningstabeller, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Manuell inställning** och välj sedan relaterad länk.  

> [!IMPORTANT]
> Var försiktig om du väljer tabeller eller fält med samma tidsdefinierade namn men som skiljer sig åt med specialtecken, till exempel %, &, <, >, (, och ). Tabellen "XYZ" kan t.ex. innehålla fälten "Fält 1" och "Fält 1 %".
>
> XML-processorn accepterar endast vissa specialtecken och tar bort de som inte accepteras. Om du tar bort ett specialtecken, t.ex. %-symbolen i "Fält 1 %", resulterar det i två eller flera tabeller eller fält med samma namn och ett fel uppstår när du exporterar eller importerar ett konfigurationspaket.

## <a name="to-create-a-custom-company-configuration-package"></a>Så här skapar du ett anpassat konfigurationspaket för företag  
1.  Skapa ett nytt företag. Mer information finns i [Skapa nya företag i Business Central](about-new-company.md).  
3.  Ställ in det nya företaget efter behov. Fyll i alla inställningstabeller som behövs.  
4.  Öppna det nya företaget.
5. Öppna sidan **Konfigurationsformulär**.  
6.  Lägg till tabellerna som du vill överföra till ett annat företag i kalkylarket. Tilldela kalkylarksraderna till paketet.  
7.  Skapa ett frågeformulär för de mest använda inställningstabellerna.  
8.  Skapa konfigurationsmallar för att göra det lättare att skapa huvuddata, som för kunder eller artiklar.  
9.  Exportera ditt paket som en rapidstart-fil.  

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)

---
title: Så här skapar du en Lista över kostnadstyper | Microsoft Docs
description: Planen över kostnadstyper liknar kontoplanen i redovisningen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: e0bf6a8c7595155785949ed51c765fef0524173b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922118"
---
# <a name="set-up-cost-types"></a>Skapa kostnadstyper
Listan över kostnadstyper liknar kontoplanen i redovisningen. Du kan definiera planen för kostnadstyper på följande sätt:  

-   Strukturera planen över kostnadstyper på samma sätt som resultaträkningens konton i kontoplanen i redovisningen. Sedan kan du överföra kontoplanen i redovisningen till planen över kostnadstyper. Du kan göra nödvändiga justeringar efter överföringen.  
-   Skapa ny plan över kostnadstyper eller lägg till nya kostnadstyper till befintlig plan över kostnadstyper. Du måste skapa varje ny kostnadstyp för sig.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Överföra kontoplanen i redovisningen till redovisningsplanen över kostnadstyper  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Lista över kostnadstyper** och välj sedan relaterad länk.  
2.  Välj åtgärden **Hämta kostnadstyper från kontoplan** action. Välj **ja** i dialogrutan för att bekräfta överföringen. Funktionen använder kontoplanen i redovisningen för att skapa en plan över kostnadstyper.  

    Planen över kostnadstyper innehåller nu alla resultaträkningskonton i redovisningen inklusive rubriker och delsummor. Du kan ändra planen över kostnadstyper efter behov. Du kan till exempel ta bort dubbletter av befintliga kostnadstyper.  

    > [!IMPORTANT]  
    >  Funktionen **Registrera kostnadstyper i kontoplan** uppdaterar relationen mellan kontoplanen och planen över kostnadstyper. Fältet **nr.** -fältet fylls och verifieras för att se till att varje redovisningskonto är kopplade till endast ett kostnadstyp. Kör funktionen automatiskt, före överföring av redovisningstransaktioner mot kostnadsredovisning.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Så här skapar du nya kostnadstyper på sidan Lista över kostnadsbärare.  
1.  Öppna sidan **Lista över kostnadstyper** i redigeringsläge.  
2.  Fyll i fälten som beskrivs efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Du kan lägga upp och underhålla kostnadstupen antingen i kortet **Kort för Kostnadstyper** eller på sidan **Lista över Kostnadstyper**. I den här proceduren skapar du Kostnadstyper på sidan **Lista över kostnadstyper**.

3.  När du har skapat alla kostnadstyper väljer du åtgärden **Indrag för kostnadstyper**. Välj **ja** i dialogrutan.  
4.  Koppla den nya kostnadstypen till motsvarande redovisningskonto.  

    > [!IMPORTANT]  
    >  Om du har angett definitioner i fältet **Summering** för rader av typen **Till-summa** innan du kör funktionen **Indrag för kostnadstyper** måste du ange definitionerna igen eftersom funktionen ersätter alla värden i alla **Till-summa**-fält.  

## <a name="to-update-cost-types"></a>Uppdatera kostnadstyper  
1.  Markera om du vill att planen över kostnadstyper automatiskt ska uppdateras när kontoplanen ändras på sidan **Inställningar för kostnadsredovisning**.  
2.  I fältet **Justera redovisningskonto** kan du välja något av följande alternativ.  

- **Ingen justering** - Ingen motsvarande ändring görs i planen över kostnadstyper när du ändrar kontoplanen.  
- **Automatisk** - Det görs en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.  
- **Prompt** - Ett meddelande visas och frågar om du vill göra en motsvarande ändring i planen över kostnadstyper när du ändrar kontoplanen.  

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)  
[Definiera kostnadsställen och kostnadsbärare för kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldon mellan kostnadstyp, kostnadsställe och kostnadsbärare](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)   
[Om kostnadsredovisning](finance-about-cost-accounting.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

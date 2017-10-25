---
title: "Så här skapar du kostnadsställen | Microsoft Docs"
description: "Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter. Planen för kostnadsställen liknar dimensionsinformationen för redovisningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 433526fbd2a13f32e64be94cc1936151445c19f5
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cost-centers"></a>Så här: Skapa kostnadsställen
Kostnadsställen är avdelningar som ansvarar för kostnader och intäkter. Planen för kostnadsställen liknar dimensionsinformationen för redovisningen. Du kan definiera planen för kostnadsställen på följande sätt:  

-   Överför dimensionsvärden i redovisningen till företagets plan för kostnadsställen. Du kan göra nödvändiga justeringar efter överföringen.  
-   Skapa en ny plan för kostnadsstället som är oberoende av redovisningen, eller lägg till ett nytt kostnadsställe i en befintlig plan för kostnadsställen. Du måste skapa varje kostnadsställe var för sig.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Överföra dimensionsvärden i redovisningen till planen för kostnadsställen  
1.  Skapa en dimension som ska vara kostnadsställesdimensionen i fönstret **Uppdatera kostnadsredovisningsdimensioner**. Endast värdena från dimensionen överförs.  
2.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lista över kostnadsställen** och välj sedan relaterad länk.  
3.  Välj **Hämta kostnadsställen från dimension** för att överföra dimensionsvärden till planen för kostnadsställen på fliken **Åtgärder** i gruppen **Funktioner**. Funktionen överför de dimensionsvärden som du har definierat i steg 1.  

    > [!NOTE]  
    >  Du kan ställa in fältet **Justera dimension för kostnadsställe** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen. Du kan inte definiera en synkronisering av diagrammet över kostnadsställen till dimensionsvärden från redovisningen.  

Diagrammet över kostnadsställen innehåller nu alla angivna dimensionsvärden från redovisningen inklusive titlar och delsummor.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a>Så här skapar du nya kostnadsställen i fönstret Lista över kostnadsställen.  
Du kan lägga upp och underhålla kostnadsställen antingen i kortet **Kort för kostnadsställe** eller i fönstret **Lista över kostnadsställen**. I den här proceduren skapar du kostnadsställen i fönstret **Lista över kostnadsställen**.  

1. Öppna fönstret **Lista över kostnadsställen** i redigeringsläge.  
2. Ange kostnadsställets kod i fältet **Kod**. Alla kostnadsställen måste ha en kod.  
3. Ange kostnadsställets namn i fältet **Namn**.  
4. Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsstället.  

    - För kostnadsställen av typen **Summa** måste du fylla fältet **Summering**. Använd **eller** operatorn som är en vertikal rad (**&#124;**) för att ange intervall av kostnadsställen.  
    - För kostnadsställen av radtypen **till-summa** fylls det här fältet i automatiskt när du använder indragsfunktionen.  
5.  Fyll i fälten **Sorteringsordning** och **Kostnadssubtyp**.  
6.  Välj nästa tomma rad för att skapa ett nytt kostnadsställe, och upprepa sedan steg 2 till 5.  
7.  När du har skapat alla kostnadsställen, väljer du åtgärden **Indrag för kostnadstyper**. Välj **Ja**.  

> [!IMPORTANT]  
>  Om du har angett definitioner i fältet  **Summering** för **Till-summa**-kostnadsställen innan du kör indragsfunktionen måste du ange dessa igen. Funktionen ersätter värdena i alla fält för **slutsummor**.  

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)  
[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)   
[Om kostnadsredovisning](finance-about-cost-accounting.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


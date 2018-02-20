---
title: "Så här skapar du kostnadsbärare | Microsoft Docs"
description: "Lär dig ställa in kostnadsbärare som motsvarar dimensionerna för redovisningen."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f371a772f710576a70bac4808b15be091a61d66
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-cost-objects"></a>Skapa kostnadsobjekt
Kostnadsbärare är projekt, produkter eller tjänster i ett företag. Planen för kostnadsbärare liknar dimensionsinformationen för redovisningen. Du kan definiera planen för kostnadsbärare på följande sätt:  

* Överför dimensionsvärden i redovisningen till företagets plan för kostnadsbärare. Du kan göra nödvändiga justeringar efter överföringen.  
* Skapa en ny plan för kostnadsbäraren som är oberoende av redovisningen, eller lägg till en ny kostnadsbäraren i en befintlig plan för kostnadsbärare. Du måste skapa varje kostnadsbärare var för sig.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Så här överför du dimensionsvärden från redovisningen till kontoplanen för kostnadsbärare  
1.  Skapa en dimension som ska vara kostnadsbärardimensionen i fönstret **Uppdatera CA-dimensioner**. Endast värdena från dimensionen överförs.  
2.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lista över kostnadsbärare** och välj sedan relaterad länk.  
3.  Välj åtgärden **Hämta kostnadsbärare från dimension** för att överföra dimensionsvärden till planen för kostnadsbärare. Funktionen överför de dimensionsvärden som du har definierat i steg 1.  

    > [!NOTE]  
    >  Du kan ställa in fältet **Justera dimension för kostnadsbärare** för att definiera en enkelriktad synkronisering av dimensionsvärden från redovisningen till diagrammet över kostnadsställen. Du kan inte definiera en synkronisering av diagrammet över kostnadsbärare till dimensionsvärden från redovisningen.  

Diagrammet över kostnadsbärare innehåller nu alla angivna dimensionsvärden från redovisningen inklusive rubriker och delsummor.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a>Så här skapar du nya kostnadsbärare i fönstret Lista över kostnadsbärare.  
Du kan lägga upp och underhålla kostnadsbärare antingen i kortet **Kort för kostnadsbärare** eller i fönstret **Lista över kostnadsbärare**. I den här proceduren skapar du kostnadsbärare i fönstret **Lista över kostnadsbärare**.  

1.  Öppna fönstret **Lista över kostnadsbärare** i redigeringsläge.  
2.  Ange kostnadsbäraren kod i fältet **Kod**. Alla kostnadsbärare måste ha en kod.  
3.  Ange kostnadsbärarens namn i fältet **Namn**.  
4.  Välj listpilen i fältet **Radtyp** för att ange syftet med kostnadsbäraren.  

    * För kostnadsbärare av radtypen **Summa** fyller du i fältet **Summa från/till**. Använd operatorn **eller** som är ett vertikalt streck (**&#124;**), för att ange intervall av kostnadsbärare.  
    * För kostnadsbärare av radtypen **slutsumma** fylls det här fältet i automatiskt när du använder indragsfunktionen.  
5.  Fyll i fältet **Bokföringsdatum**.  
6.  Välj nästa tomma rad för att skapa en ny kostnadsbäraren och upprepa sedan steg 2 till 5.  
7.  När du har skapat alla kostnadsbärare, väljer du åtgärden **Indrag för kostnadsbärare**. Välj **Ja**.  

> [!IMPORTANT]  
>  Om du har angett definitioner i fälten **Summa från/till** för **Till-summa** för kostnadsbärare innan du kör indragsfunktionen måste du ange dessa igen. Funktionen ersätter värdena i alla fält för **slutsummor**.  

## <a name="see-also"></a>Se även  
[Redovisa kostnader](finance-manage-cost-accounting.md)  
[Definiera kostnadsställen och kostnadsbärare för kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldon mellan kostnadstyp, kostnadsställe och kostnadsbärare](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Ställa in kostnadsredovisning](finance-set-up-cost-accounting.md)   
[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)   
[Om kostnadsredovisning](finance-about-cost-accounting.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


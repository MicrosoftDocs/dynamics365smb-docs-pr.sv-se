---
title: Skapa redovisningsbudgetar| Microsoft Docs
description: "Beskriver hur du skapar redovisningsbudgetar för att förutse olika ekonomiska aktiviteter och koppla dimensioner för affärssystemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dd3be77519075b67a942402bd01d5a2a562a1c32
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-gl-budgets"></a>Skapa redovisningsbudgetar
Om du vill kan du använda flera olika budgetar för samma tidsperioder genom att skapa budgetar med separata namn. Först definierar du budgetnamnet och matar in budgetsiffrorna. Budgetnamnet infogas sedan i alla budgettransaktioner du skapar.  

 När du skapar en budget kan du definiera fyra dimensioner för varje budget. De här budgetspecifika dimensionerna kallas för budgetdimensioner. Du kan välja budgetdimensionerna bland de dimensioner som redan finns upplagda. Budgetdimensioner kan användas för att skapa filter för en budget och lägga till dimensionsinformation till budgettransaktioner. Mer information finns i [Arbeta med](finance-dimensions.md).

 Budgetar spelar en viktig roll i business intelligence, exempelvis i bokslut som baseras på kontoscheman som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i diagrammet över konton. Mer information finns i [Affärsstöd](bi.md).

 Budgetar spelar en viktig roll i business intelligence, exempelvis i bokslut som baseras på kontoscheman som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i diagrammet över konton. Mer information finns i [Affärsstöd](bi.md).

I kostnadsredovisning arbetar du med kostnadsbudgetar på liknande sätt. (Mer information finns i [Skapa kostnadsbudgetar](finance-create-cost-budgets.md).)    

## <a name="to-create-a-new-gl-budget"></a>Så här skapar du en ny redovisningsbudget  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.  
2. Välj åtgärden **Redigera lista** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj åtgärden **Redigera budget**.
4. Högst upp i fönstret **Budget** fyller du i fälten för att definiera vad som ska visas.  

    Endast transaktioner som innehåller budgetnamnet som du angav i fältet **Budgetnamn** visas. Fönstret är för närvarande tomt eftersom budgetnamnet just har skapats och det därför inte finns några transaktioner som matchar filtret. Därför är fönstret tomt.  
5. Om du vill ange ett belopp väljer du relevant cell i matrisen. Fönstret **Redov.budgettransaktioner** öppnas.  
6. Skapa en ny rad och fyll i fältet **Belopp**. Stäng fönstret **Redov.budgettransaktioner**.  
7. Upprepa steg 5–6 tills du har angett alla budgetbeloppen.  

> [!NOTE]  
>  På snabbfliken **Filter** kan du filtrera budgetinformationen beroende på hur många budgetdimensioner som definierats under budgetnamnet.   

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Affärsstöd](bi.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


---
title: Skapa redovisningsbudgetar| Microsoft Docs
description: Beskriver hur du skapar redovisningsbudgetar för att förutse olika ekonomiska aktiviteter och koppla dimensioner för affärssystemet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/07/2019
ms.author: sgroespe
ms.openlocfilehash: 990124036c5a9dfc7195669185836f556a8d8d0a
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629671"
---
# <a name="create-gl-budgets"></a>Skapa redovisningsbudgetar
Om du vill kan du använda flera olika budgetar för samma tidsperioder genom att skapa budgetar med separata namn. Först definierar du budgetnamnet och matar in budgetsiffrorna. Budgetnamnet infogas sedan i alla budgettransaktioner du skapar.  

När du skapar en budget kan du definiera fyra dimensioner för varje budget. De här budgetspecifika dimensionerna kallas för budgetdimensioner. Du kan välja budgetdimensionerna bland de dimensioner som redan finns upplagda. Budgetdimensioner kan användas för att skapa filter för en budget och lägga till dimensionsinformation till budgettransaktioner. Mer information finns i [Arbeta med](finance-dimensions.md).

Budgetar spelar en viktig roll i business intelligence, exempelvis i bokslut som baseras på kontoscheman som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i diagrammet över konton. Mer information finns i [Affärsstöd](bi.md).

I kostnadsredovisning arbetar du med kostnadsbudgetar på liknande sätt. (Mer information finns i [Skapa kostnadsbudgetar](finance-create-cost-budgets.md).)    

## <a name="to-create-a-new-gl-budget"></a>Så här skapar du en ny redovisningsbudget  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Redovisningsbudgetar** och välj sedan relaterad länk.  
2. Välj åtgärden **Redigera lista** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj åtgärden **Redigera budget**.
4. Högst upp på sidan **Budget** fyller du i fälten för att definiera vad som ska visas.  

    Endast transaktioner som innehåller budgetnamnet som du angav i fältet **Budgetnamn** visas. Fönstret är för närvarande tomt eftersom budgetnamnet just har skapats och det därför inte finns några transaktioner som matchar filtret. Därför är sidan tom.  
5. Om du vill ange ett belopp väljer du relevant cell i matrisen. Sidan **Redov.budgettransaktioner** öppnas.  
6. Skapa en ny rad och fyll i fältet **Belopp**. Stäng sidan **Redov.budgettransaktioner**.  
7. Upprepa steg 5–6 tills du har angett alla budgetbeloppen.  

> [!NOTE]  
>  På snabbfliken **Filter** kan du filtrera budgetinformationen beroende på hur många budgetdimensioner som definierats under budgetnamnet.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Exportera och importera redovisningsbudgetar i Excel
För praktiskt taget alla andra sidor kan du exportera data på sidor i budgeten till Excel för vidare bearbetning och analys. Mer information finns i [Exportera dina affärsdata till Excel](about-export-data.md).

> [!NOTE]
> Kontoplanen som redovisningsbudgetarna baseras på, har rader för kontotypen Rubrik som innehåller där summan av raderna under. När du exporterar en redovisningsbudget exporteras data på alla rader oavsett kontotypen. Men endast data på rader med kontotypen Bokföring kan importera data igen. I enlighet med detta: <br /><br /> **När du importerar en redovisningsbudget tas alla värden som fanns på Rubrikrader bort.** <br /><br /> Detta är för att undvika fel summor när du har importerat data som har skapats eller redigerats i Excel.<br /><br /> **Scenario**: du vet att nya budgeterade lönkostnader ska vara BVA 1 200 000. Du vill att budget för löneavdelningen för tre specifika rader (av kontotypen Bokföring) för heltidsanställda, deltidsanställda och timanställda. De tre raderna grupperas under rubrikraden Löner.<br /><br />Du anger 1 200 000 på rubrikraden, exporterar budget till Excel och skickar sedan den till löneavdelningen och ber dem distribuera BVA 1 200 000.<br /><br /> Löneavdelningen fördelar beloppet på tre bokföringskonton. När du importerar tillbaka till redovisningsbudget fylls de tre kontona i med den nya Excel-informationen och summerar till BVA 1 200 000 och rubrikraden är tom.

## <a name="see-also"></a>Se även
[Exportera affärsdata till Excel](about-export-data.md)  
[Ekonomi](finance.md)  
[Affärsstöd](bi.md)  
[Ställa in Finance](finance-setup-finance.md)  
redovisning[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

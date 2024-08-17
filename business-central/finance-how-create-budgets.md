---
title: Skapa redovisningsbudgetar
description: Beskriver hur du skapar redovisningsbudgetar för att förutse olika ekonomiska aktiviteter och koppla dimensioner för affärssystemet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="create-gl-budgets"></a>Skapa redovisningsbudgetar

Om du vill kan du använda flera olika budgetar för samma tidsperioder genom att skapa budgetar med separata namn. Först definierar du budgetnamnet och matar in budgetsiffrorna. Budgetnamnet infogas sedan i alla budgettransaktioner du skapar.  

När du skapar en budget kan du tilldela budgetspecifika dimensioner för varje budget, kallade budgetdimensioner för den. Du kan använda budgetdimensioner kan användas för att skapa filter för en budget och lägga till dimensionsinformation till budgettransaktioner. Mer information: [Arbeta med dimensioner](finance-dimensions.md).

Budgetar spelar en viktig roll i Business Intelligence. Exempelvis i bokslut som baseras på ekonomiska rapporter som innehåller budgettransaktioner eller när du analyserar budgeterade och faktiska belopp i kontoplanen. Läs mer i [Business Intelligence](bi.md).

I kostnadsredovisning arbetar du med kostnadsbudgetar på liknande sätt. Läs mer i [Skapa kostnadsbudgetar](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Så här skapar du en ny redovisningsbudget

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsbudgetar** och väljer sedan relaterad länk.  
2. Välj åtgärden **Redigera lista** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj åtgärden **Redigera budget**.
4. Högst upp på sidan **Budget** fyller du i fälten för att definiera vad som ska visas.  

   Sidan visar endast transaktioner som innehåller budgetnamnet som du angav i fältet **Budgetnamn**. Eftersom du just har skapat budgetnamnet finns det inte några transaktioner som matchar filtret. Därför är sidan tom.  
5. Om du vill ange ett belopp väljer du relevant cell i matrisen. Sidan **Redov.budgettransaktioner** öppnas.  
6. Skapa en ny rad och fyll i fältet **Belopp**. Stäng sidan **Redov.budgettransaktioner**.  
7. Upprepa steg 5 och 6 för alla belopp i budgeten.  

> [!NOTE]  
> På snabbfliken **Filter** kan du filtrera budgetinformationen efter de budgetdimensioner du har definierat under budgetnamnet.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Exportera och importera redovisningsbudgetar med Excel

För praktiskt taget alla andra sidor kan du exportera data på sidor i budgeten till Microsoft Excel för vidare bearbetning och analys. Läs mer i [Exportera dina affärsdata till Excel](about-export-data.md).

> [!NOTE]
> Kontoplanen, som redovisningsbudgetar baseras på, har rader av kontotypen Rubrik. Dessa rader innehåller summan av raderna under den. När du exporterar en redovisningsbudget exporteras data på alla rader oavsett kontotypen. Du kan endast importera data på rader av typen Bokföringskonto.

När du importerar en redovisningsbudget tas alla värden på Rubrikrader bort. De tas bort för att undvika felaktiga summor när du importerar data som har skapats eller redigerats i Excel.

### <a name="scenario"></a>Scenario

Du vet att nya budgeterade lönkostnader ska vara lokal valuta (BVA) 1,200,000. Du vill aktivera budget för löneavdelningen för tre specifika rader (av kontotypen Bokföring) för heltidsanställda, deltidsanställda och timanställda. De tre raderna grupperas under rubrikraden Löner.

Du anger 1 200 000 på rubrikraden, exporterar budgeten till Excel och skickar sedan den till löneavdelningen och ber dem distribuera BVA 1 200 000.

Löneavdelningen fördelar beloppet på tre bokföringskonton. När du importerar tillbaka till redovisningsbudget fylls de tre kontona i med den nya Excel-informationen och summerar till BVA 1 200 000 och rubrikraden är tom.

## <a name="see-also"></a>Se även

[Exportera affärsdata till Excel](about-export-data.md)  
[Ekonomi](finance.md)  
[Affärsstöd](bi.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

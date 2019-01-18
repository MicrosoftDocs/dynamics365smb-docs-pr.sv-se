---
title: "Importera lönetransaktioner | Microsoft Docs"
description: "Om du vill hantera lön, importera och bokföra ekonomiska transaktioner från leverantören lön i redovisningen med hjälp av filtillägget lön, till exempel Ceridian eller Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 642c35fa993b9177ec51deccaef7beb3615ab336
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="import-payroll-transactions"></a>Importera lönetransaktioner
För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen. För att göra detta måste du först importera en fil som du får från lönelistleverantören till sidan **Redovisningsjournal**. Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot. Slutligen bokför du lönetransaktioner enligt kontomappningen.

> [!NOTE]  
>   Om du vill använda denna funktion måste ett tillägg för lönelisteimport ha installerats och aktiverats. Tilläggen Ceridian lön och importera Quickbooks lön är förinstallerade i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Att importera en lönefil
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. I relevant redovisningsjournal väljer du åtgärden **Importera lönetransaktioner**. En assisterad inställningsguide öppnas.
3. Följ anvisningarna på sidan **Importera lönetransaktioner**.

    > [!TIP]  
    >   I steget som berör mappning av externa löneposter till dina redovisningskonton kommer mappningarna som du skapar att sparas till nästa gång samma poster importeras. Detta sparar tid samtidigt som du inte behöver fylla i fältet **Kontonr** manuellt i redovisningsjournalen när du har importerat återkommande lönetransaktioner.   

    När du väljer knappen **OK** i den assisterade inställningsguiden, fylls sidan **Redovisningsjournal** med rader som representerar de transaktioner som lönefilen innehåller, samt med relevanta konton redan ifyllda i fälten **Redovisningsjournal** i enlighet med de mappningar som du har gjort i guiden.
4. Ändra eller bokför journalrader som för alla andra redovisningtransaktioner. Mer information finns i [Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  


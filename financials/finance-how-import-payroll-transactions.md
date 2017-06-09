---
title: "Så här importerar du lönetransaktioner | Microsoft Docs"
description: "Beskriver hur du importerar löneutbetalningar och relaterade transaktioner från ditt lönesystem till redovisningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Så här Importera du lönetransaktioner 
För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen. För att göra detta måste du först importera en fil som du får från lönelistleverantören till fönstret **Redovisningsjournal**. Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot. Slutligen bokför du lönetransaktioner enligt kontomappningen.

**Obs**: Om du vill använda denna funktion måste ett tillägg för lönelisteimport ha installerats och aktiverats. Tilläggen Ceridian lön och importera Quickbooks lön är förinstallerade i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Att importera en lönefil
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Redovisningsjournaler**, och välj sedan relaterad länk.
2. I relevant redovisningsjournal väljer du åtgärden **Importera lönetransaktioner**. En assisterad inställningsguide öppnas.
3. Följ anvisningarna i fönstret **Importera lönetransaktioner**.

    **Tips**: I steget som berör mappning av externa löneposter till dina redovisningskonton kommer mappningarna som du skapar att sparas till nästa gång samma poster importeras. Detta besparar dig tid eftersom du inte behöver fylla i fältet **Kontonummer** manuellt varje gång du importerar återkommande lönetransaktioner.   

    När du väljer knappen **OK** i den assisterade inställningsguiden, fylls fönstret **Redovisningsjournal** med rader som representerar de transaktioner som lönefilen innehåller, samt med relevanta konton redan ifyllda i fälten **Redovisningsjournal** i enlighet med de mappningar som du har gjort i guiden.
4. Ändra eller bokför journalrader som för alla andra redovisningtransaktioner. Mer information finns i [Så här arbetar du med redovisningsjournaler](ui-work-general-journals.md).   

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]med tillägg](ui-extensions.md)  
[Så här arbetar du med redovisningsjournaler](ui-work-general-journals.md)  


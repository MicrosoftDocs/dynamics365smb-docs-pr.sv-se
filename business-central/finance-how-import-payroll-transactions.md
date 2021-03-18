---
title: Importera lönetransaktioner | Microsoft Docs
description: Om du vill hantera lön, importera och bokföra ekonomiska transaktioner från leverantören lön i redovisningen med hjälp av filtillägget lön, till exempel Ceridian eller Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6bd078c6cf12023088dfa2f925e5a61bcc61778
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387455"
---
# <a name="import-payroll-transactions"></a>Importera lönetransaktioner
För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen. För att göra detta måste du först importera en fil som du får från lönelistleverantören till sidan **Redovisningsjournal**. Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot. Slutligen bokför du lönetransaktioner enligt kontomappningen.

> [!NOTE]  
>   Om du vill använda denna funktion måste ett tillägg för lönelisteimport ha installerats och aktiverats. Tilläggen Ceridian lön och importera Quickbooks lön är förinstallerade i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Att importera en lönefil
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan relaterad länk.
2. I relevant redovisningsjournal väljer du åtgärden **Importera lönetransaktioner**. En assisterad inställningsguide öppnas.
3. Följ anvisningarna på sidan **Importera lönetransaktioner**.

    > [!TIP]  
    >   I steget som berör mappning av externa löneposter till dina redovisningskonton kommer mappningarna som du skapar att sparas till nästa gång samma poster importeras. Detta sparar tid samtidigt som du inte behöver fylla i fältet **Kontonr** manuellt i redovisningsjournalen när du har importerat återkommande lönetransaktioner.   

    När du väljer knappen **OK** i den assisterade inställningsguiden, fylls sidan **Redovisningsjournal** med rader som representerar de transaktioner som lönefilen innehåller, samt med relevanta konton redan ifyllda i fälten **Redovisningsjournal** i enlighet med de mappningar som du har gjort i guiden.
4. Ändra eller bokför journalrader som för alla andra redovisningtransaktioner. Mer information finns i [Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Importera lönetransaktioner
description: 'Om du vill hantera lön, importera och bokföra ekonomiska transaktioner från leverantören lön i redovisningen med hjälp av filtillägget lön, till exempel Ceridian.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="importing-payroll-transactions"></a>Importera lönetransaktioner

För att ta hänsyn till lönutbetalningar och relaterade transaktioner måste du importera och bokföra finansiella transaktioner som gjorts av ditt lönesystem i redovisningen. För att göra detta måste du först importera en fil som du får från lönelistleverantören till sidan **Redovisningsjournal**. Sedan mappar du de externa kontona i lönefilen till det relevanta redovisningskontot. Slutligen bokför du lönetransaktioner enligt kontomappningen.

> [!NOTE]  
> Om du vill använda denna funktion måste ett tillägg för lönelisteimport ha installerats och aktiverats. Tilläggen Ceridian lön och importera Quickbooks lön är förinstallerade i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Att importera en lönefil

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournaler** och väljer sedan relaterad länk.
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

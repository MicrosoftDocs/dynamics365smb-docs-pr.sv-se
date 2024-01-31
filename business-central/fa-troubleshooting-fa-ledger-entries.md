---
title: Tillägget Felsöka poster i redovisningen för fasta anläggningstillgångar
description: Det är enklare att arbeta med heltal. Använd det här tillägget för att avrunda belopp för anläggningstillgångar i redovisningen för fasta anläggningstillgångar.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Tillägget Felsöka poster i redovisningen för fasta anläggningstillgångar
Använd tillägget Felsöka poster i redovisningen för fasta anläggningstillgångar för att avrunda avskrivnings- och anskaffningsbelopp i poster för anläggningstillgångar till heltal. Om du till exempel vill avrunda beloppet 30 000,44 till 30 000. Vanliga orsaker till avrundningsproblem är datamigrering, att man plötsligt börjar bokföra belopp i redovisningen, samt anpassningar i [!INCLUDE[prod_short](includes/prod_short.md)].

Tillägget Felsöka poster i redovisningen för fasta anläggningstillgångar är förinstallerat och klart att köra. Om du tar bort tillägget men vill installera det igen hitar du det på AppSource.

## Felsöka redovisningsposter för fasta anläggningstillgångar
När du öppnar sidan **Kort för fast anläggningstillgång** för första gången schemaläggs jobbkön **Skanna redovisningsposter för fasta anläggningstillgångar** till att övervaka belopp varje söndag. Om denna funktion hittar belopp som du kan vilja avrunda visas ett meddelande nästa gång du öppnar sidan Kort för fast anläggningstillgång. Meddelandet innehåller alternativet **Visa fler** som öppnar sidan **Redovisningsposter för fasta anlägningstillgångar med avrundningsproblem**, som innehåller de transaktioner med belopp som du kan vilja avrunda. Om du vill avrunda beloppen väljer du transaktionerna och sedan åtgärden **Acceptera urval**. Du kan använda åtgärden **Sök poster med problem** för att uppdatera listan med nya problem som inträffat efter det att jobbkötransaktionen kördes föregående söndag.

## Se även
[Anläggningstillgångar](fa-manage.md)  
[Hantera anläggningstillgångar](fa-manage.md)  
[Underhålla anläggningstillgångar](fa-how-maintain.md)  
[Anpassa Business Central Online med hjälp av tillägg](ui-extensions.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]




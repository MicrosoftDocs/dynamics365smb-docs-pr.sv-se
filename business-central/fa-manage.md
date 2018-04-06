---
title: "Hantera anläggningstillgångar | Microsoft Docs"
description: "Lär dig mer om funktionen för anläggningstillgångar i Financials och få en översikt över hur du arbetar med anläggningstillgångar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ccfca6c5feaf9b67d9f423a7cf4b61a51682f358
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="fixed-assets"></a>Anläggningstillgångar
Genom funktionerna för anläggningstillgångar i [!INCLUDE[d365fin](includes/d365fin_md.md)] får du en översikt över anläggningstillgångarna och en korrekt periodisk avskrivning. Tack vare funktionen kan du även hålla reda på dina underhållskostnader, hantera försäkringsbrev, bokföra transaktioner för anläggningstillgångar samt skapa olika rapporter och statistik.

För varje anläggningstillgång måste du skapa ett kort som innehåller information om tillgången. Du kan ställa in byggnads- eller produktionsutrustning som en huvudtillgång med en komponentlista och du kan gruppera dem på olika sätt, till exempel efter klass, avdelning eller plats. Sedan kan du börja anskaffa, underhålla och sälja anläggningstillgångarna. Du kan även skapa budgeterade tillgångar. På så sätt kan du inkludera eventuella förutsedda anskaffningar och försäljningar i rapporter.

För att hålla reda på avskrivningar av anläggningstillgångar och andra ekonomiska transaktioner relaterade till anläggningstillgångar skapar du en eller flera avskrivningsregler för varje anläggningstillgång i företaget. Avskrivning görs genom att köra en rapport för att beräkna periodiska avskrivningar och genom att fylla i en journal med de resulterande transaktionerna som är klara att bokföras. [!INCLUDE[d365fin](includes/d365fin_md.md)] ger stöd för flera avskrivningmetoder. Mer information finns i [Avskrivningsmetoder](fa-depreciation-methods.md). Du kan ställa in åtskilliga avskrivningsregler per anläggningstillgång för olika syften, till exempel en för skattrapportering och en annan för rapportering.

För varje tillgång kan du registrera underhållskostnader och nästa servicedatum. Det kan vara viktigt att hålla reda på underhållsutgifter för budgetändamål och för att kunna ta beslut om en anläggningstillgång ska ersättas.

Varje anläggningstillgång kan kopplas till ett eller flera försäkringsbrev. Du kan på så sätt enkelt verifiera att försäkringsbrevsbeloppen stämmer överens med värdet på den tillgång som är kopplad till brevet. Det blir även enklare att bevaka årliga försäkringspremier.

> [!NOTE]  
>   Du kan bokföra in anläggningstillgångstransaktioner i fönstret **Anl.tillg. redovisningsjournal** eller i fönstret **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering. Hjälp för anläggningstillgångar beskriver endast hur du använder fönstret **Anl.tillg. redovisningsjournal**. Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).

Innan du kan hantera anläggningstillgångar måste du skapa standardvärden, bokföring av anläggningstillgångar, bokföringsmallar, fördelningsnycklar, journaler och bokföringstyper. Mer information finns i [Konfigurera anläggningstillgångar](fa-setup.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| skapa anläggningstillgångar, tilldela avskrivningsmetoder, bokföra anskaffningar, återanskaffningsvärden och skriva ut listor över anläggningstillgångar. |[Skaffa anläggningstillgångar](fa-how-acquire.md) |
| Registrera servicebesök, bokföra underhållsarbete och övervaka underhållskostnader. |[Underhålla anläggningstillgångar](fa-how-maintain.md) |
| Uppdatera försäkringsinformation, bokföra anskaffningskostnader i försäkringsbrev, ändra försäkringsskydd, visa försäkringsstatistik och visa listor över försäkringsbrev. |[Försäkra anläggningstillgångar](fa-how-insure.md) |
| gruppera anläggningstillgångar, flytta anläggningstillgångar mellan olika lagerställen, dela upp eller slå ihop tillgångar. |[Överföra, dela eller kombinera anläggningstillgångar](fa-how-trans-split-combine.md) |
| justera värden på anläggningstillgångar, bokföra avskrivning och bokföra nedskrivningsstransaktioner. |[Omvärdera anläggningstillgångar](fa-how-revalue.md) |
| Beräkna avskrivningar, bokföra avskrivningar och analysera avskrivningar i rapporter om anläggningstillgångar. |[Så här skriver du av eller amorterar anläggningstillgångar](fa-how-depreciate-amortize.md) |
| bokföra avyttringstransaktioner, visa avyttringstransaktioner och bokföra delvisa avyttringar. |[Avyttra eller ställa av anläggningstillgångar](fa-how-dispose-retire.md) |
| Hanter budgetar för anläggningstillgångar, budgeterar anskaffningskostnader, budgeterar avyttringar av anläggningstillgångar och budgeterar avskrivning. |[Hantera budgetar för anläggningstillgångar](fa-how-manage-budgets.md) |

## <a name="see-also"></a>Se även
[Ställa in anläggningstillgångar](fa-setup.md)  
[Anpassa din [!INCLUDE[d365fin](includes/d365fin_md.md)]-upplevelse](ui-experiences.md)  
[Ekonomi](finance.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]


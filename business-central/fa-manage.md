---
title: Hantera anläggningstillgångar (innehåller video)
description: Lär dig mer om funktionen för anläggningstillgångar och få en översikt över hur du arbetar med och hanterar anläggningstillgångar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Hantera anläggningstillgångar

Genom funktionerna för anläggningstillgångar i [!INCLUDE[prod_short](includes/prod_short.md)] får du en översikt över anläggningstillgångarna och hjälper till att säkerställa att deras avskrivning är korrekt. Detta låter dig även hålla reda på dina underhållskostnader, hantera försäkringsbrev, bokföra transaktioner för anläggningstillgångar samt skapa olika rapporter och statistik.

## Videoöversikt

I följande video beskrivs grunderna för anläggningstillgångar:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Inledande inställning av anläggningstillgångar

Innan du kan hantera anläggningstillgångar måste du göra följande inställningar:

- Standardvärden
- Redovisning av anläggningstillgångar
- Bokföringsmallar och bokföringstyper
- Fördelningsnycklar
- Anläggningstillgångsjournaler

Läs mer på [Ställa in anläggningstillgångar](fa-setup.md).

## Analys av anläggningstillgångar

I det här avsnittet beskrivs analysverktyg som du kan använda för att få insikter om data om dina anläggningstillgångar.

| Till... | Gå till |
| --- | --- |
| Läs mer om funktionerna för att analysera data om anläggningstillgångar. | [Översikt över analys av anläggningstillgångar](fa-analytics-overview.md) |
| Utför ad hoc-analys av anläggningstillgångar direkt på listsidor och frågor. | [Ad hoc-analys av data för anläggningstillgångar](ad-hoc-analysis-fa.md) |
| Utforska inbyggda rapporter för anläggningstillgångar. | [Inbyggda rapporter om anläggningstillgångar](fa-reports.md) |
| Övervaka underhållskostnader. | [Övervaka underhållskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Bevaka försäkringsskydd. | [Bevaka försäkringsskydd](fa-how-insure.md#to-monitor-insurance-coverage) |
| Visa avyttringstransaktioner | [Visa avyttringstransaktioner](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Visa planerade avyttringsvärden. | [Visa planerade avyttringsvärden](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Registrera anläggningstillgångar

För varje anläggningstillgång måste du skapa ett kort som innehåller information om dem. Du kan till exempel ange byggnads- eller fabriksinventarier som en huvudtillgång med en komponentlista. Du kan gruppera tillgångar på olika sätt, till exempel efter klass, avdelning eller plats. Sedan kan du anskaffa, underhålla och sälja anläggningstillgångarna. Du kan även skapa budgeterade tillgångar. Med budgetering kan du inkludera eventuella förutsedda anskaffningar och försäljningar i rapporter.

| Till  | Gå till |
| --- | --- |
| Hanter budgetar för anläggningstillgångar, budgeterar anskaffningskostnader, budgeterar avyttringar av anläggningstillgångar och budgeterar avskrivning. |[Hantera budgetar och anläggningstillgångar](fa-how-manage-budgets.md) |
| skapa anläggningstillgångar, tilldela avskrivningsmetoder, bokföra anskaffningar, återanskaffningsvärden och skriva ut listor över anläggningstillgångar. |[Anskaffa anläggningstillgångar](fa-how-acquire.md) |

## Ställ in avskrivningar för dina anläggningstillgångar

För att hålla reda på avskrivningar av anläggningstillgångar och andra ekonomiska transaktioner för anläggningstillgångar skapar du en eller flera avskrivningsregler för varje. Det finns några steg för att avskriva tillgångar:

1. Kör en rapport för att beräkna periodisk avskrivning.
1. Fyll i en journal med de resulterande transaktioner.
1. Bokför journalen.

[!INCLUDE[prod_short](includes/prod_short.md)] ger stöd för flera avskrivningmetoder. Mer information finns i [Avskrivningsmetoder](fa-depreciation-methods.md). Du kan ställa in åtskilliga avskrivningsregler för varje anläggningstillgång för olika syften, till exempel en för skattrapportering och en annan för rapportering.

| Till  | Gå till |
| --- | --- |
| Lär dig mer om olika avskrivningsmetoder för anläggningstillgångarna. |[Avskrivningsmetoder](fa-depreciation-methods.md) |
| Beräkna avskrivningar, bokföra avskrivningar och analysera avskrivningar i rapporter om anläggningstillgångar. |[Skriva av eller amortera anläggningstillgångar](fa-how-depreciate-amortize.md) |
| Visa ändrade värden för avskrivningsregler. | [Visa ändrade värden för avskrivningsregler](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Du kan manuellt registrera anläggningstillgångstransaktioner på sidan **Anl.tillg. redovisningsjournal** eller på sidan **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering. | [Konfigurera avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md) |

## Underhåll och försäkring av anläggningstillgångar

För varje tillgång kan du registrera underhållskostnader och nästa servicedatum. Det kan vara viktigt att hålla reda på underhållsutgifter för budgetändamål och för att kunna ta beslut om en anläggningstillgång ska ersättas. Du kan koppla varje anläggningstillgång till ett eller flera försäkringsbrev och kontrollera att försäkringspremierna stämmer överens med tillgångarnas värde.

| Till  | Gå till |
| --- | --- |
| Registrera servicebesök, bokföra underhållsarbete och övervaka underhållskostnader. |[Underhålla anläggningstillgångar](fa-how-maintain.md) |
| Övervaka underhållskostnader. | [Övervaka underhållskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Uppdatera försäkringsinformation, bokföra anskaffningskostnader i försäkringsbrev, ändra försäkringsskydd, visa försäkringsstatistik och visa listor över försäkringsbrev. |[Försäkra anläggningstillgångar](fa-how-insure.md) |
| Bevaka försäkringsskydd. | [Bevaka försäkringsskydd](fa-how-insure.md#to-monitor-insurance-coverage) |

## Gruppera, överföra, dela upp/slå ihop, justera värde, skriva ned och avyttra anläggningstillgångar

| Till  | Gå till |
| --- | --- |
| gruppera anläggningstillgångar, flytta anläggningstillgångar mellan olika lagerställen, dela upp eller slå ihop tillgångar. |[Överföra, dela eller kombinera anläggningstillgångar](fa-how-trans-split-combine.md) |
| justera värden på anläggningstillgångar, bokföra avskrivning och bokföra nedskrivningsstransaktioner. |[Omvärdera anläggningstillgångar](fa-how-revalue.md) |
| bokföra avyttringstransaktioner, visa avyttringstransaktioner och bokföra delvisa avyttringar. |[Avyttra eller ställa av anläggningstillgångar](fa-how-dispose-retire.md) |
| Visa avyttringstransaktioner | [Visa avyttringstransaktioner](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Visa planerade avyttringsvärden. | [Visa planerade avyttringsvärden](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Se även

[Ställa in anläggningstillgångar](fa-setup.md)  
[Översikt över analys av anläggningstillgångar](fa-analytics-overview.md)  
[Översikt över ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]

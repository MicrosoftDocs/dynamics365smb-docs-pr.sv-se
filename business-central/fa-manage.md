---
title: Hantera anläggningstillgångar (innehåller video)
description: Lär dig mer om funktionen för anläggningstillgångar och få en översikt över hur du arbetar med och hanterar anläggningstillgångar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Hantera anläggningstillgångar

Genom funktionerna för anläggningstillgångar i [!INCLUDE[prod_short](includes/prod_short.md)] får du en översikt över anläggningstillgångarna och en korrekt periodisk avskrivning. Tack vare funktionen kan du även hålla reda på dina underhållskostnader, hantera försäkringsbrev, bokföra transaktioner för anläggningstillgångar samt skapa olika rapporter och statistik.

## Videoöversikt

I följande video beskrivs grunderna för anläggningstillgångar:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Översikt över anläggningstillgångar

För varje anläggningstillgång måste du skapa ett kort som innehåller information om tillgången. Du kan ställa in byggnads- eller produktionsutrustning som en huvudtillgång med en komponentlista och du kan gruppera dem på olika sätt, till exempel efter klass, avdelning eller plats. Sedan kan du börja anskaffa, underhålla och sälja anläggningstillgångarna. Du kan även skapa budgeterade tillgångar. Med budgetering kan du inkludera eventuella förutsedda anskaffningar och försäljningar i rapporter.

> [!IMPORTANT]
> Innan du kan hantera anläggningstillgångar måste du göra följande inställningar:
>
> * Standardvärden
> * Redovisning av anläggningstillgångar
> * Bokföringsmallar
> * Fördelningsnycklar
> * Anläggningstillgångsjournaler
>
> Mer information finns i [Konfigurera anläggningstillgångar](fa-setup.md).

För att hålla reda på avskrivningar av anläggningstillgångar och andra ekonomiska transaktioner för anläggningstillgångar skapar du en eller flera avskrivningsregler för varje. Avskrivning görs genom att köra en rapport för att beräkna periodiska avskrivningar och genom att fylla i en journal med de resulterande transaktionerna och sedan bokför journalen. [!INCLUDE[prod_short](includes/prod_short.md)] ger stöd för flera avskrivningmetoder. Mer information finns i [Avskrivningsmetoder](fa-depreciation-methods.md). Du kan ställa in åtskilliga avskrivningsregler per anläggningstillgång för olika syften, till exempel en för skattrapportering och en annan för rapportering.

För varje tillgång kan du registrera underhållskostnader och nästa servicedatum. Det kan vara viktigt att hålla reda på underhållsutgifter för budgetändamål och för att kunna ta beslut om en anläggningstillgång ska ersättas.

Du kan koppla varje anläggningstillgång till ett eller flera försäkringsbrev och kontrollera att försäkringspremierna stämmer överens med tillgångarnas värde.

> [!NOTE]  
> Du kan bokföra in anläggningstillgångstransaktioner på sidan **Anl.tillg. redovisningsjournal** eller på sidan **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering. Hjälp för anläggningstillgångar beskriver endast hur du använder sidan **Anl.tillg. redovisningsjournal**. Mer information finns i [Ställa in avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md).

## Så här använder du anläggningstillgångar

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

| Till  | Gå till |
| --- | --- |
| Ställ in förutsättningar för att använda funktionen anläggningstillgångar (definiera standardvärden, bokföring av anläggningstillgångar, bokföringsmallar, fördelningsnycklar, journaler och bokföringstyper). | [Ställa in anläggningstillgångar](fa-setup.md)|
| Hanter budgetar för anläggningstillgångar, budgeterar anskaffningskostnader, budgeterar avyttringar av anläggningstillgångar och budgeterar avskrivning. |[Hantera budgetar och anläggningstillgångar](fa-how-manage-budgets.md) |
| skapa anläggningstillgångar, tilldela avskrivningsmetoder, bokföra anskaffningar, återanskaffningsvärden och skriva ut listor över anläggningstillgångar. |[Anskaffa anläggningstillgångar](fa-how-acquire.md) |
| Lär dig mer om olika avskrivningsmetoder för anläggningstillgångarna. |[Avskrivningsmetoder](fa-depreciation-methods.md) |
| Beräkna avskrivningar, bokföra avskrivningar och analysera avskrivningar i rapporter om anläggningstillgångar. |[Skriva av eller amortera anläggningstillgångar](fa-how-depreciate-amortize.md) |
| Läs mer om inbyggda rapporterings- och analysfunktioner för anläggningstillgångar. | [Översikt över analys av anläggningstillgångar](fa-analytics-overview.md) |
| Registrera servicebesök, bokföra underhållsarbete och övervaka underhållskostnader. |[Underhålla anläggningstillgångar](fa-how-maintain.md) |
| Uppdatera försäkringsinformation, bokföra anskaffningskostnader i försäkringsbrev, ändra försäkringsskydd, visa försäkringsstatistik och visa listor över försäkringsbrev. |[Försäkra anläggningstillgångar](fa-how-insure.md) |
| gruppera anläggningstillgångar, flytta anläggningstillgångar mellan olika lagerställen, dela upp eller slå ihop tillgångar. |[Överföra, dela eller kombinera anläggningstillgångar](fa-how-trans-split-combine.md) |
| justera värden på anläggningstillgångar, bokföra avskrivning och bokföra nedskrivningsstransaktioner. |[Omvärdera anläggningstillgångar](fa-how-revalue.md) |
| bokföra avyttringstransaktioner, visa avyttringstransaktioner och bokföra delvisa avyttringar. |[Avyttra eller ställa av anläggningstillgångar](fa-how-dispose-retire.md) |


## Se även

[Ställa in anläggningstillgångar](fa-setup.md)  
[Översikt över analys av anläggningstillgångar](fa-analytics-overview.md)   
[Översikt över ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]

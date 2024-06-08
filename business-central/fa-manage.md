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

# <a name="manage-fixed-assets"></a>Hantera anläggningstillgångar

Genom funktionerna för anläggningstillgångar i [!INCLUDE[prod_short](includes/prod_short.md)] får du en översikt över anläggningstillgångarna och hjälper till att säkerställa att deras avskrivning är korrekt. Det hjälper dig också att spåra underhållskostnader, hantera försäkringar, bokföra transaktioner med anläggningstillgångar och generera olika rapporter och statistik.

## <a name="what-is-a-fixed-asset"></a>Vad är en anläggningstillgång?

Anläggningstillgångar skiljer sig från andra artiklar i distributionslagret. En anläggningstillgång, även känd som en kapitaltillgång, är en materiell fastighet, anläggning eller utrustning (PP&E) som du äger eller förvaltar med förväntan att den kommer att fortsätta att bidra till att generera inkomster. En tillgång är fast när det är en artikel som ditt företag inte kommer att konsumera, sälja eller konvertera till kontanter under nästa kalenderår. Anläggningstillgångar skiljer sig från omsättningstillgångar, som är kontanta eller planerade att omvandlas till kontanter inom de närmaste 12 månaderna. Anläggningstillgångar skiljer sig också från ditt lager, eftersom lager vanligtvis förbrukas inom kort tid.

## <a name="types-of-fixed-assets"></a>Typer av anläggningstillgångar

Företag investerar vanligtvis i några typer av anläggningstillgångar. Några exempel är:

- Byggnader och anläggningar
- Datorutrustning och programvara
- Möbler och inventarier
- Maskinell
- Fordon

## <a name="understanding-fixed-asset-accounting"></a>Förstå redovisning av anläggningstillgångar

Redovisning av anläggningstillgångar innebär att du håller exakta finansiella register om dina kapitaltillgångar. Dessa poster innehåller information om de fem stadierna i en tillgångs livscykel. Efter det första inköpet omfattar livscykeln för varje anläggningstillgång minst tre av följande steg:

- Anskaffning: Du lägger till en ny anläggningstillgång i dina böcker.
- Avskrivning: Du registrerar en tillgångs periodiska värdeminskning, som du använder en avskrivningsmetod för att beräkna. Mer information finns i [Anl. avskrivningsberäkning](LocalFunctionality/India/FA_Depreciation.md).
- Omvärdering: Du registrerar en bedömning av en tillgångs aktuella verkliga marknadsvärde. Mer information finns i [Omvärdera anläggningstillgångar](fa-how-revalue.md).
- Nedskrivning: Du registrerar en värdeminskning på grund av händelser eller omständigheter.
- Avyttring: Du säljer, skrotar eller använder ett annat sätt att göra dig av med en tillgång när den är uttjänt.

Revisioner ingår också i de detaljerade kontrollerna av ditt företags bokföring efter att räkenskaperna för räkenskapsåret har avslutats. Oavsett om det är internt eller externt, revisioner är där du kan märka inkonsekvenser eller skillnader mellan dina anteckningar och det faktiska tillståndet för dina tillgångar. Revisioner främjar transparens i dina tillgångar och redovisning om du förlorar mer pengar än väntat.

## <a name="video-overview"></a>Videoöversikt

I följande video beskrivs grunderna för anläggningstillgångar:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Inledande inställning av anläggningstillgångar

Innan du kan hantera anläggningstillgångar måste du göra följande inställningar:

- Standardvärden
- Redovisning av anläggningstillgångar
- Bokföringsmallar och bokföringstyper
- Fördelningsnycklar
- Anläggningstillgångsjournaler

Läs mer på [Ställa in anläggningstillgångar](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Analys av anläggningstillgångar

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

## <a name="register-fixed-assets"></a>Registrera anläggningstillgångar

För varje anläggningstillgång måste du skapa ett kort som innehåller information om dem. Du kan till exempel ange byggnads- eller fabriksinventarier som en huvudtillgång med en komponentlista. Du kan gruppera tillgångar på olika sätt, till exempel efter klass, avdelning eller plats. Sedan kan du anskaffa, underhålla och sälja anläggningstillgångarna. Du kan även skapa budgeterade tillgångar. Med budgetering kan du inkludera eventuella förutsedda anskaffningar och försäljningar i rapporter.

| Till  | Gå till |
| --- | --- |
| Hanter budgetar för anläggningstillgångar, budgeterar anskaffningskostnader, budgeterar avyttringar av anläggningstillgångar och budgeterar avskrivning. |[Hantera budgetar och anläggningstillgångar](fa-how-manage-budgets.md) |
| skapa anläggningstillgångar, tilldela avskrivningsmetoder, bokföra anskaffningar, återanskaffningsvärden och skriva ut listor över anläggningstillgångar. |[Anskaffa anläggningstillgångar](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Ställ in avskrivningar för dina anläggningstillgångar

För att hålla reda på avskrivningar av anläggningstillgångar och andra ekonomiska transaktioner för anläggningstillgångar skapar du en eller flera avskrivningsregler för varje. Det finns några steg för att avskriva tillgångar:

1. Kör en rapport som beräknar periodisk avskrivning.
1. Fyll i en journal med de resulterande transaktioner.
1. Bokför journalen.

[!INCLUDE[prod_short](includes/prod_short.md)] ger stöd för flera avskrivningmetoder. Mer information finns i [Avskrivningsmetoder](fa-depreciation-methods.md). Du kan ställa in åtskilliga avskrivningsregler för varje anläggningstillgång för olika syften, till exempel en för skattrapportering och en annan för rapportering.

| Till  | Gå till |
| --- | --- |
| Lär dig mer om olika avskrivningsmetoder för anläggningstillgångarna. |[Avskrivningsmetoder](fa-depreciation-methods.md) |
| Beräkna avskrivningar, bokföra avskrivningar och analysera avskrivningar i rapporter om anläggningstillgångar. |[Skriva av eller amortera anläggningstillgångar](fa-how-depreciate-amortize.md) |
| Visa ändrade värden för avskrivningsregler. | [Visa ändrade värden för avskrivningsregler](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Du kan manuellt registrera anläggningstillgångstransaktioner på sidan **Anl.tillg. redovisningsjournal** eller på sidan **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering. | [Konfigurera avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Underhåll och försäkring av anläggningstillgångar

För varje tillgång kan du registrera underhållskostnader och nästa servicedatum. Det kan vara viktigt att hålla reda på underhållsutgifter för budgetändamål och för att kunna ta beslut om en anläggningstillgång ska ersättas. Du kan koppla varje anläggningstillgång till ett eller flera försäkringsbrev och kontrollera att försäkringspremierna stämmer överens med tillgångarnas värde.

| Till  | Gå till |
| --- | --- |
| Registrera servicebesök, bokföra underhållsarbete och övervaka underhållskostnader. |[Underhålla anläggningstillgångar](fa-how-maintain.md) |
| Övervaka underhållskostnader. | [Övervaka underhållskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Uppdatera försäkringsinformation, bokföra anskaffningskostnader i försäkringsbrev, ändra försäkringsskydd, visa försäkringsstatistik och visa listor över försäkringsbrev. |[Försäkra anläggningstillgångar](fa-how-insure.md) |
| Bevaka försäkringsskydd. | [Bevaka försäkringsskydd](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Gruppera, överföra, dela upp/slå ihop, justera värde, skriva ned och avyttra anläggningstillgångar

| Till  | Gå till |
| --- | --- |
| gruppera anläggningstillgångar, flytta anläggningstillgångar mellan olika lagerställen, dela upp eller slå ihop tillgångar. |[Överföra, dela eller kombinera anläggningstillgångar](fa-how-trans-split-combine.md) |
| justera värden på anläggningstillgångar, bokföra avskrivning och bokföra nedskrivningsstransaktioner. |[Omvärdera anläggningstillgångar](fa-how-revalue.md) |
| bokföra avyttringstransaktioner, visa avyttringstransaktioner och bokföra delvisa avyttringar. |[Avyttra eller ställa av anläggningstillgångar](fa-how-dispose-retire.md) |
| Visa avyttringstransaktioner | [Visa avyttringstransaktioner](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Visa planerade avyttringsvärden. | [Visa planerade avyttringsvärden](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="tips-for-improving-your-fixed-asset-accounting"></a>Tips för att förbättra redovisningen av anläggningstillgångar

Det finns några saker du kan implementera i din redovisningsstrategi för anläggningstillgångar som kan hjälpa dig att maximera dina intäkter.

- Upprätta ett tröskelvärde för versaler. När du köper en artikel, bestäm ett fast belopp för versaler. Beloppet hjälper till att säkerställa att dina redovisningsböcker är konsekventa och gör det lättare för dig och ditt team att upptäcka bokföringsfel.
- Omvärdera utrustningens livscykel. Det är viktigt att korrekt uppskatta hur länge du kan använda anläggningstillgångarna för deras ursprungliga ändamål. Eftersom redovisning och avskrivning är beroende av korrekta livscykeluppskattningar bör du omvärdera vid behov eftersom det kan ändras med tiden.
- Tagga dina tillgångar. Det är viktigt att spåra och tagga dina tillgångar under hela livscykeln eftersom många faktorer kan påverka deras värde. Taggning hjälper till att spåra dina varor genom stadierna av deras livscykel och hjälper till att förhindra stöld, eliminera felplacering och stödja ekonomisk statistik.
- Automatisera insikter med bokföringsprogram för anläggningstillgångar. Automatisering av manuella aktiviteter för att spåra dina data med bokföringsprogram för anläggningstillgångar gör processer enklare att slutföra. Lösenordsskydd kan hjälpa till att ge åtkomst endast till de personer som behöver det och är utbildade för det.

## <a name="see-also"></a>Se även

[Ställa in anläggningstillgångar](fa-setup.md)  
[Översikt över analys av anläggningstillgångar](fa-analytics-overview.md)  
[Översikt över ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Dela och exportera rapporter med rapportinkorgen
description: 'Använd sidan Rapportinkorgen när du vill hämta, dela och exportera rapporter i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Dela och exportera rapporter med rapportinkorgen

På sidan **Rapportinkorgen** visas schemalagda rapporter som genererats av användaren i [!INCLUDE[prod_short](includes/prod_short.md)] och kan användas inte bara för att öppna genererade rapporter, utan även för att dela och öppna filer i OneDrive för företag.

> [!TIP]
> Följande åtgärder är också tillgängliga i delen **Rapportinkorgen** i rollcentret. Om delen inte visas i gränssnittet kan du lära dig att anpassa ditt rollcenter här: [Anpassa arbetsytan](ui-personalization-user.md).

## Hämta genererade rapporter

Om du vill spara tidigare rapporter öppnar du sidan **Rapportinkorgen** på följande sätt:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Rapportinkorgen** och väljer sedan relaterad länk.  
2. På sidan **Rapportinkorgen** väljer du önskad rapport.

> [!NOTE]
> Sidan visar inte tidigare rapporter som genererats med åtgärden **Skriv ut** eller som sparats som en fil i menyn **Rapporter**.
>
> De genererade filerna sparas i det format som definieras vid schemaläggningen av rapporten och kan ändras på sidan **Jobbkötransaktioner** tillsammans med återkommande och andra inställningar. Lär dig ändra rapportfilformatet och ange ytterligare alternativ på [Hantera schemalagda återkommande rapporter](ui-work-report.md#manage-scheduled-recurring-reports).

## Öppna genererade rapporter i OneDrive

Om du vill exportera rapportfilen till Microsoft OneDrive för företag, väljer du rapporten på sidan **Rapportinkorgen** och väljer åtgärden **Öppna i OneDrive**. Rapporten kopieras sedan till [!INCLUDE[prod_short](includes/prod_short.md)]-mappen i OneDrive och öppnas i ett nytt webbläsarfönster där du kan skriva ut och hantera dokumentfilen.

> [!IMPORTANT]
>
> Rapporter som är på väg att upphöra att gälla på sidan **Schemalägg en rapport** och som kopierats till OneDrive tas inte automatiskt bort från den delade mappen.

## Dela schemalagda rapporter

Du kan dela rapporter med samarbetspartner på sidan **Rapportinkorgen**. Välj rapporten och välj åtgärden **Dela**. På sidan **Skicka länk** väljer du vem som kan öppna filen, definierar redigeringsbehörigheter och väljer sedan **Skicka** för att skicka en länk för åtkomst till den sparade rapporten.

> [!NOTE]
> Om du vill veta mer om OneDrive-integrering och -funktioner på [!INCLUDE[prod_short](includes/prod_short.md)], inklusive första konfigurationen och alternativ för hantering av filnamnskonflikter, läser du artikeln [Öppna och dela filer i OneDrive](across-share-onedrive.md).
>
> Med hjälp av åtgärden **Dela** blir den genererade rapportfilen tillgänglig för andra användare på OneDrive för företag, och visar inte den schemalagda rapporten i **Rapportinkorgen**.

## Se även

[Köra och skriva ut rapporter](ui-work-report.md)  
[Tillgängliga rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Använda rapporter i det dagliga arbetet](reports-use-reports.md)  
[Business Intelligence och rapporteringsöversikt](reports-bi-reporting.md)  
[Ställa in skrivare](ui-specify-printer-selection-reports.md)  
[Arbeta med kalenderdatum och tider](ui-enter-date-ranges.md)  
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]- och OneDrive-integration](across-onedrive-overview.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

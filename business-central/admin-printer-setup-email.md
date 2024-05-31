---
title: Konfigurera e-postutskrift
description: Beskrivning av instruktioner
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers"></a>Konfigurera e-postutskrift

I den här artikeln beskrivs hur du konfigurerar e-postaktiverad skrivare i [!INCLUDE[prod_short](includes/prod_short.md)]. Med dessa skrivare skickar [!INCLUDE[prod_short](includes/prod_short.md)] utskriftsjobben till skrivaren med hjälp av skrivarens e-postadress.

> [!TIP]
> Om du vill veta mer om andra skrivarmöjligheter går du till [Översikt över skrivarhanteringen](admin-printer-setup-overview.md). 

## <a name="prerequisites"></a>Förutsättningar

- [!INCLUDE[prod_short](includes/prod_short.md)] utgivningscykel 1 år 2020 eller senare
- Tillägget **Skicka till e-postskrivare** är installerat

    Detta tillägg instalelras dessutom som standard. Läs mer om att installera tillägg på [Installera och avinstallera tillägg i Business Central](ui-extensions-install-uninstall.md).
- E-postfunktionen har konfigurerats.

   Läs mer i [Ställa in e-post](admin-how-setup-email.md).

## <a name="add-an-email-printer"></a>Lägg till en e-postskrivare

På sidan **Utskriftshantering** kan du se vilka skrivare som är inställda. Sidan ger dig också åtkomst till sidan **Inställningar** för varje skrivare för att redigera en befintlig konfiguration eller ställa in en ny skrivare.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.
2. Välj **E-posta utskrift** och välj sedan **Lägg till en e-postskrivare**.
3. På sidan **Inställningar av e-postskrivare** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du måste manuellt välja rätt pappersstorlek för en skrivare eftersom det varken finns någon lokal skrivare eller några användarinställningar som kan lagras.
    >
    > Tänk på att tillägget för e-postskrivare är inställt på pappersformatet **A4**, vilket exempelvis inte lämpar sig för Nordamerika.

## <a name="privacy-notice"></a>Sekretesspolicy

Om du använder tillägget för e-postskrivare skickas alla eller vissa utskriftsjobb till den e-postadress som konfigurerats för skrivaren. Vi rekommenderar starkt att ett unikt e-transaktion-ID kopplas till en skrivarenhet endast med de officiella tjänster som tillhandahålls av maskinvarutillverkaren, till exempel HP ePrint, KonicaMinolta EveryonePrint eller Epson Email Print.

Du måste vidta alla nödvändiga sekretessåtgärder, inklusive att se till lösningen för e-postutskrift har korrekt konfigurerade behörigheter, sekretessinställningar och lagringsmetoder. Det är ditt ansvar att skapa en korrekt, verifierad och fungerande e-postadress. Läs mer i [Microsofts sekretesspolicy](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps"></a>Nästa steg

[Ställa in standardskrivare](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a>Se även

[Översikt över skrivarhantering](admin-printer-setup-overview.md)  
[Ställa in skrivare för Universell utskrift ](admin-printer-setup-universal-print.md)
[Skriva ut en rapport](ui-work-report.md#PrintReport)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kör batchjobb](ui-how-run-batch-jobs.md)  

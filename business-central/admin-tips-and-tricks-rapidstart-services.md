---
title: Tips och råd - RapidStart Services | Microsoft Docs
description: När du konfigurerar företag som använder RapidStart Services finns några tips och trick som du kan använda för att implementeringen ska gå smidigt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e301d788fdedacf0fc2ac3ce29946df965bed711
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777072"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Tips och råd: RapidStart Services

När du konfigurerar företag som använder RapidStart Services finns några tips och trick som du kan använda för att implementeringen ska gå smidigt.  

## <a name="take-advantage-of-configuration-templates"></a>Utnyttja fördelarna med konfigurationsmallar

Konfigurationsmallar kan hjälpa dig att rationalisera din implementering. Genom att använda dem kan du ta med liknande kunder i segment och sedan utveckla ett implementeringsprotokoll som behandlar alla kunder i ett segment på ungefär samma sätt. På så sätt kan du tillämpa en nivå av förkonfiguration på varje segment och fortsätta med en snabb implementering.  

## <a name="configuration-questionnaires"></a>Konfigurationsfrågeformulär

Som hjälp vid processen att fylla i ett konfigurationsfrågeformulär bör du överväga att definiera standardsvar för att ange metodtips.  

## <a name="batch-creation-of-journal-lines"></a>Batchskapande av journalrader

Vi rekommenderar att du använder datamigreringsverktygen som tillhandahålls för att migrera journaltransaktioner. Annars, om du använder batch-jobbet för att skapa journalrader, har det en begränsad omfattning och skapar endast pre-standardfält i en journal. Resten av journalen måste sedan avslutas manuellt.  

## <a name="migrating-transactions"></a>Migrera transaktioner

Vi rekommenderar att du migrerar ingående balanser i följande ordning. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Migrera redovisningen av ingående balanser utan att använda underredovisningarna för redovisningskonto. Använd specifika motkonton för ingående balanser, en inställning för varje underredovisning. Skapa motkonteringskontona för att aktivera direkt bokföring.  
2. Migrera öppna kundreskontratransaktioner.  <!--work on these-->
3. Migrera öppna artikeltransaktioner.  
4. Migrera öppna anläggningstillgångstransaktioner.  

## <a name="make-each-package-manageable"></a>Gör respektive paket hanterbart

När du använder konfigurationspaket för att migrera data separerar du datan i separata paket för en enklare överföring. Om du till exempel vill migrera 20 års poster i transaktionsregister kan importen ta många timmar och dagar i anspråk. Se istället till att dela upp datan så att respektive paket blir mer hanterbart. Det finns för tillfället inga fasta regler för vad som gör ett paket effektivt, men om du upplever problem med att importera eller exportera ett paket, försök då göra det mindre och se om det hjälper.  

## <a name="see-also"></a>Se även

[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
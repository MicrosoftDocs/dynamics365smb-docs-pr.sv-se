---
title: Basic Experience-tillägg | Microsoft Docs
description: Detta tillägg är ett modernt alternativ till Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.search.form: 20600,
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: b0443ef53a564e103810543225cc0c4a0c6bced7
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606042"
---
# <a name="the-basic-experience-extension"></a>Basic Experience-tillägget

Om du har använt Microsoft Dynamics C5 kan Microsoft-partner hjälpa dig ta steget över till en mer modern lösning som baseras på [!INCLUDE[prod_short](includes/prod_short.md)], så att du kan fortsätta avnjuta samma effektiviserade möjligheter som Dynamics C5.

Det här tillägget är avsett för mindre företag och kan stödja upp till tre användare. Om du behöver fler användare måste du uppgradera till en [!INCLUDE[prod_short](includes/prod_short.md)]-licens och avinstallera tillägget.

> [!NOTE]
> Nu är det här tillägget bara tillgängligt för kunder i Danmark och Island.

## <a name="whats-available"></a>Vad som finns

I följande tabell beskrivs de funktioner som är tillgängliga om du installerar Basic Experience-tillägget.

|Yta  |Funktionalitet  |
|---------|---------|
|**Redovisning** |Grundläggande finans, ekonomiska rapporter, anläggningstillgångar, bankhantering, bankavstämning, betalningar, direktdebitering, dimensioner, flera valutor, budgetar, arbetsflöde, dokumenthantering/OCR, konsolidering, obegränsat antal företag|
|**Kundfordringar/försäljning** |Grundläggande kundreskontra, försäljningsfakturering, försäljningsrabatter, prissättning, moms, kontakthantering |
|**Leverantörsreskontra/inköp** |Grundläggande leverantörsreskontra, inköpsfakturering |
|**Projekthantering** |Projekt, projektpris, tidrapporter, tilldelning, uppgifter, resurser |
|**Lager** |Grundläggande lager, artikelersättningar, artikeltvärreferens |

## <a name="getting-started"></a>Kom i gång

Det här tillägget skiljer sig från de flesta, och du behöver hjälp från en Microsoft-partner för att installera och konfigurera det. För att visa vad du kan förvänta dig får du här en övergripande vy över vad Microsoft-partnern gör.

1. Skapa en ny [!INCLUDE[prod_short](includes/prod_short.md)]-klientorganisation. Det kan antingen vara en utvärderings- eller CSP-version.
2. Lägg till minst en användare som är tilldelad en Basic Experience-licens på ditt Azure Active Directory-konto.
3. Ta bort alla företag, inklusive exempelföretaget Cronus.
4. Skapa ett nytt företag som inte innehåller exempeldata eller inställningar.
5. Lägg till paketet **Demo RapidStart**. <!--what does the package contain?-->
6. Hämta och installera Basic Experience-tillägget från AppSource.

## <a name="migrating-data"></a>Migrera data

Ta med dina Dynamics C5-data. När din Microsoft-partner har installerat Basic Experience-tillägget får du ett tomt företag. Ett enkelt sätt att flytta data från Dynamics C5 till Basic Experience är att använda tillägget C5 för datamigrering, som ingår i [!INCLUDE[prod_short](includes/prod_short.md)]. Tillägget flyttar kunder, leverantörer, artiklar, dina redovisningskonton och transaktioner däri.

## <a name="see-also"></a>Se även

[Tillägget C5 Datamigrering](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

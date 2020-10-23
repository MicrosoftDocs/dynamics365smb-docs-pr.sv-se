---
title: Basic Experience-tillägg | Microsoft Docs
description: Det här tillägget är ett modernt alternativ till Microsoft Dynamics C5.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: e7377d1413e2f1969543374f1b819e6fc8a2a263
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927734"
---
# <a name="the-basic-experience-extension"></a>Basic Experience-tillägget
Om du har använt Microsoft Dynamics C5 kan Microsoft-partner hjälpa dig över till en mer modern lösning som baseras på [!INCLUDE[d365fin](includes/d365fin_md.md)], så att du kan fortsätta att njuta av samma strömlinjeformade möjligheter som Dynamics C5.

Det här tillägget är avsett för mindre företag och kan stödja upp till tre användare. Om du behöver fler användare måste du uppgradera till en [!INCLUDE[d365fin](includes/d365fin_md.md)]-licens och avinstallera tillägget.

> [!NOTE]
> Nu är det här tillägget bara tillgängligt för kunder i Danmark och Island. 

## <a name="whats-available"></a>Vad som finns
I följande tabell beskrivs de funktioner som är tillgängliga om du installerar Basic Experience-tillägget.

|Område  |Funktionalitet  |
|---------|---------|
|**Redovisning** |Grundläggande finans, Kontouppställningar, Anläggningstillgångar, Bankhantering, Bankavstämning, Betalningar, Direktdebitering, Dimensioner, Flera valutor, Budgetar, Arbetsflöde, Dokumenthantering/OCR, Konsolidering, Obegränsat antal företag|
|**Konto – kundreskontra/försäljning** |Grundläggande kundreskontra, försäljningsfakturering, försäljningsrabatter, prissättning, moms, kontakthantering |
|**Konto – leverantörsreskontra/inköp** |Grundläggande leverantörsreskontra, inköpsfakturering |
|**Projekthantering** |Projekt, projektpris, tidrapporter, tilldelning, uppgifter, resurser |
|**Lager** |Grundläggande lager, artikelersättningar, artikeltvärreferens |

## <a name="getting-started"></a>Komma igång
Det här tillägget skiljer sig från de flesta, och du behöver hjälp från en Microsoft-partner för att installera och konfigurera det. För att visa vad du kan förvänta dig får du här en övergripande vy över vad Microsoft-partnern gör.

1. Skapa en ny [!INCLUDE[d365fin](includes/d365fin_md.md)]-klientorganisation. Det kan antingen vara en utvärderings- eller CSP-version.
2. Lägg till minst en användare som är tilldelad en Basic Experience-licens på ditt Azure Active Directory-konto.
3. Ta bort alla företag, inklusive exempelföretaget Cronus.
4. Skapa ett nytt företag som inte innehåller exempeldata eller inställningar.
5. Lägg till paketet **Demo RapidStart**. <!--what does the pockage contain?-->
6. Hämta och installera Basic Experience-tillägget från AppSource.

## <a name="migrating-data"></a>Migrera data
Ta med dina Dynamics C5-data. När din Microsoft-partner har installerat Basic Experience-tillägget får du ett tomt företag. Ett enkelt sätt att flytta data från Dynamics C5 till Basic Experience är att använda tillägget C5-datamigrering, som ingår i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tillägget flyttar kunder, leverantörer, artiklar, dina redovisningskonton och transaktioner däri.

## <a name="see-also"></a>Se även
[Tillägget C5 Datamigrering ](ui-extensions-c5-data-migration.md)
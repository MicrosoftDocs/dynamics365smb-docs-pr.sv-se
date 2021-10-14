---
title: Tillägget Dataarkiv
description: Om du arkiverar data skapas en låg säkerhetskopia av posterna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 032c425f10bae29416cf8602d0c339f3ffaa3043
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589532"
---
# <a name="the-data-archive-extension"></a>Tillägget Dataarkiv
Med tiden kommer ditt företag att samla en stor mängd data och som administratör är det förmodligen en god idé att ha en strategi för att arkivera data. Att få mycket data kan sakta ner sig, t.ex. ta något längre tid att generera rapporter eller till och med låsa poster. Dessutom kan stora mängder data leda till ökade lagringskostnader.

Dataarkiv tillägget ger en grundläggande ram för att arkivera och säkerhetskopiera data som en del av datumkomprimeringen. När du använder datumkomprimering konsolideras relaterade transaktioner till en enda post och originalen tas bort. Mer information finns i [Komprimera data med datumkomprimering](admin-manage-documents.md#compress-data-with-date-compression). Det kan dock finnas ett värde där informationen sparas, så i stället för att ta bort den, kan du arkivera den för senare användning.

## <a name="start-archiving-data"></a>Starta arkivering av data
Tillägget är förinstallerat och tillgängligt i **tilläggshantering** så du behöver inte göra någonting för att komma igång. Tillägget finns också tillgängligt på Microsoft AppSource. 

Dataarkiven visas på sidan **dataarkivlistan**. Varje arkiv kan innehålla data från flera tabeller och kan innehålla upp till 10 000 poster. Om det finns fler än 10 000 poster i en tabell skapas ett andra arkiv för nästa 10 000-post och så vidare. Om du till exempel arkiverar 10 100 redovisningstransaktioner, skapar Business Central en "redovisningstransaktion" för de första 10 000 posterna och sedan en andra arkiv för de återstående 100 transaktionerna. 

När du har arkiverat data kan du utforska det genom att använda Microsoft Excel eller som en CSV-fil.

* Om du använder Excel-alternativet kommer arbetsboken att innehålla ett kalkylblad för varje dataarkivtabell.
* Om du använder alternativet CSV kommer du att få en ZIP-fil med en CSV-fil för varje dataarkivtabell.

> [!TIP]
> Alternativen Excel och CSV gör det enklare att använda en annan app eller tjänst för att flytta data till en annan plats, till exempel Azure Blob Storage eller analysverktyg, till exempel Microsoft Power BI.

Dataarkiv tilläggen används av följande batch-jobb för datumkomprimering.

|Batchjobb  |
|---------|
|Datumkomp. Artikelbudgettransaktioner     |
|Datumkompr. bankkontotrans.     |
|Datumkompr. kundreskontra     |
|Datumkompr. anl. trans.     |
|Datumkompr. redov.trans.     |
|Datumkompr. försäkringstrans.     |
|Datumkompr. underhållstrans     |
|Datumkompr. underhållstrans     |
|Datumkompr. resurstrans.     |
|Datumkompr. momstrans.     |
|Datumkompr. lev.reskontra     |
|Datumkompr. dist.lager. Transaktioner     |
|Datumkomp. Redov.budgettransaktioner     |

Aktivera arkivering av data när du kör något av batch-jobben genom att aktivera växlingsknappen **arkivera borttagna transaktioner**.

## <a name="storage-considerations"></a>Överväganden vid lagring
Arkiverade data lagras i tabellen **innehavaradministration i media**. Den här tabellen ingår inte när databasstorleken beräknas enligt dina licensvillkor. I stället räknas det som fillagring. Vi rekommenderar dock att du exporterar gamla arkiv till t.ex. en CSV-fil och sedan tar bort de gamla arkivposterna.

## <a name="see-also"></a>Se även
[Hantera lagring genom att ta bort dokument eller komprimera data](admin-manage-documents.md)

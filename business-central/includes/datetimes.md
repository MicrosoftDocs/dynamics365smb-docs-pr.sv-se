---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788595"
---
När du anger datum och tid som datum och tid som kombineras till ett enda fält, måste du ange ett blanksteg mellan datumet och tiden. Datumdelen kan bara innehålla blanksteg i form av officiella datumavgränsare för din regionsinställning. Tiden kan innehålla blanksteg runt AM/PM-indikatorn i relevanta regionala inställningar.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

Listan nedan innehåller de olika sätt som du kan ange datum och tid på och en förklaring av hur de ska tolkas.  

|Transaktion|Tolkning|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|innevarande år-innevarande månad-11 12:00:00|
|1112 12|innevarande år-12-11 12:00:00|
|d eller dagens datum|dagens datum 00:00:00|
|d tid|dagens datum aktuell tid|
|d 10:30|dagens datum 10:30:00|
|d 03:03:03|dagens datum 03:03:03|
|a eller arbetsdagens datum|arbetsdagens datum 00:00:00|
|m eller måndag|måndag i innevarande vecka 00:00:00|
|ti eller tisdag|tisdag i innevarande vecka 00:00:00|
|on eller onsdag|onsdag i innevarande vecka 00:00:00|
|to eller torsdag|torsdag i innevarande vecka 00:00:00|
|fr eller fredag|fredag i innevarande vecka 00:00:00|
|lö eller lördag|lördag i innevarande vecka 00:00:00|
|sö eller söndag|söndag i innevarande vecka 00:00:00|
|ti 10:30|tisdag i innevarande vecka 10:30:00|
|ti 03:03:03|tisdag i innevarande vecka 03:03:03|
|t23 t|Tisdag i en vecka 23 av arbetsdatumets år, aktuell tid på dagen|
|t23|Tisdag av vecka 23 arbetsdatumets år|
|t 23|Idag 23:00:00|
|t-1|Tisdag av vecka 1 arbetsdatumets år|



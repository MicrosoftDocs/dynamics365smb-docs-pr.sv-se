---
title: Fel sökning av synkroniseringsfel | Microsoft Docs
description: Innehåller vägledning för att identifiera och lösa synkroniseringsfel.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 489e66165c5441ea63043a30dee8af314ef5d815
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991814"
---
# <a name="troubleshooting-synchronization-errors"></a>Felsöka synkroniseringsfel
Det finns många rörliga delar som används för att integrera [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] och ibland kan det bli fel. I det här avsnittet beskrivs några vanliga fel som uppstår och du får tips om hur du åtgärdar dem.

Fel inträffar ofta antingen på grund av något som en användare har gjort för att sammanföra poster, eller något är fel med hur integreringen har upprättats. För fel som rör kopplade poster kan användare matcha dem själva. Dessa fel orsakas av åtgärder som att ta bort en post i en, men inte både och, affärsappar och sedan synkronisera. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fel som rör hur integreringen ställs in kräver vanligt vis en administratörs uppmärksamhet. Du kan visa dessa fel på sidan **Integreringssynkroniseringsfel**. Exempel på typiska problem är:  
  
* De behörigheter och roller som tilldelats till användare är felaktiga.  
* Administratörskontot har angetts som integrationsanvändare.  
* Lösenordet för integrationsanvändaren anges för att kräva en ändring när användaren loggar in.  
* Valutakurserna för valutor har inte angetts i den ena eller den andra appen.  
  
Du måste lösa felen manuellt, men det finns ett par sätt på vilka sidan kan hjälpa dig. Som exempel:  

* Fälten **Källa** och **mål** kan innehålla länkar till posten där felet hittades. Klicka på länken för att öppna posten och undersöka felet.  
* Åtgärderna **Ta bort transaktioner som är äldre än 7 dagar** och **Ta alla transaktioner** rensar listan. Vanligtvis använder du dessa åtgärder när du har löst orsaken till ett fel som påverkar många poster. Var försiktig. De här åtgärderna kan ta bort fel som fortfarande är relevanta.

Ibland kan tidsstämplar för poster orsaka konflikter. Tabellen "CRM-integreringspost" behåller tidsstämplarna "Senast synkad ändrad den" och "Senast synkad CRM ändrad den" för den senaste integrationen som gjordes i båda riktningarna för en post. Dessa tidsstämplar jämförs med tidsstämplar på Business Central- och Sales-poster. I Business Central finns tidstämpeln i tabellen Integrationspost.

Du kan filtrera efter poster som ska synkroniseras genom att jämföra posttidsstämplar i tabellen "Tabellmappning för integrering" i fälten "Synk. ändrad i filter" och "Synk. int.tabell, ändrad i filter".

Konfliktfelmeddelandet "Det går inte att uppdatera kundposten eftersom den har ett senare ändringsdatum än kontoposten" eller "Det går inte att uppdatera kontoposten eftersom den har ett senare ändringsdatum än kundposten" kan inträffa om en post har en tidstämpel som större än IntegrationTableMapping."Synk. ändrad i filter" men den inte är senare än tidsstämpeln på försäljningsintegrationsposten. Det innebär att källposten har synkroniserats manuellt, inte av jobbkötransaktionen. 

Konflikten beror på att målposten också har ändrats – postens tidsstämpel är senare än tidsstämpeln för försäljningsintegrationsposten. Målkontrollen sker bara för dubbelriktade tabeller. 

De här posterna flyttas nu till sidan "Hoppade över Synkronisera poster" som du öppnar från sidan för Microsoft Dynamics-anslutningsinställningar i Business Central. Där kan du ange vilka ändringar som ska behållas och sedan synkronisera posterna igen.

## <a name="see-also"></a>Se även
[Integrera med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Ställa in konton för integrering med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  

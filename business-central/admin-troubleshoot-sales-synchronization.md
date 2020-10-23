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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: db8b05aa74583d8ba74fcfeb8fae1d3c28893fac
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922398"
---
# <a name="troubleshooting-synchronization-errors"></a>Felsöka synkroniseringsfel
Det finns många rörliga delar som används för att integrera [!INCLUDE[d365fin](includes/d365fin_md.md)] med Common Data Service och ibland kan det bli fel. I det här avsnittet beskrivs några vanliga fel som uppstår och du får tips om hur du åtgärdar dem.

Fel inträffar ofta antingen på grund av något som en användare har gjort för att sammanföra poster, eller något är fel med hur integreringen har upprättats. För fel som rör kopplade poster kan användare matcha dem själva. Dessa fel orsakas av åtgärder som att ta bort en post i en, men inte både och, affärsappar och sedan synkronisera. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Exempel
I det här videoklippet visas ett exempel på hur du felsöker fel som har uppstått vid synkronisering med Sales. Samma procedur kommer att användas för alla integreringar. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fel som rör hur integreringen ställs in kräver vanligt vis en administratörs uppmärksamhet. Du kan visa dessa fel på sidan **Integreringssynkroniseringsfel**. Exempel på typiska problem är:  
  
* De behörigheter och roller som tilldelats till användare är felaktiga.  
* Administratörskontot har angetts som integreringsanvändare.  
* Lösenordet för integreringsanvändaren ställs in att kräva en ändring när användaren loggar in.  
* Valutakurserna för valutor har inte angetts i den ena eller den andra appen.  
  
Du måste lösa felen manuellt, men det finns ett par sätt på vilka sidan kan hjälpa dig. Som exempel:  

* Fälten **Källa** och **mål** kan innehålla länkar till posten där felet hittades. Klicka på länken för att öppna posten och undersöka felet.  
* Åtgärderna **Ta bort transaktioner som är äldre än 7 dagar** och **Ta alla transaktioner** rensar listan. Vanligtvis använder du dessa åtgärder när du har löst orsaken till ett fel som påverkar många poster. Var försiktig. De här åtgärderna kan ta bort fel som fortfarande är relevanta.

Ibland kan tidsstämplar för poster orsaka konflikter. Tabellen "CDS-integreringspost" behåller tidsstämplarna "Senast synkad ändrad den" och "Senast synkad CDS ändrad den" för den senaste integreringen som gjordes i båda riktningarna för en post. Dessa tidsstämplar jämförs med tidsstämplar på Business Central- och Sales-poster. I Business Central finns tidstämpeln i tabellen Integreringspost.

Du kan filtrera efter transaktioner som ska synkroniseras genom att jämföra posttidsstämplar i tabellen "Tabellmappning för integrering" med fälten "Synk. ändrad i filter" och "Synk. int.tabell ändrad i filter".

Konfliktfelmeddelandet "Det går inte att uppdatera kundposten eftersom den har ett senare ändringsdatum än kontoposten" eller "Det går inte att uppdatera kontoposten eftersom den har ett senare ändringsdatum än kundposten" kan inträffa om en post har en tidstämpel som större än IntegreringTableMapping."Synk. ändrad i filter" men den inte är senare än tidsstämpeln på försäljningsintegreringsposten. Det innebär att källposten har synkroniserats manuellt, inte av jobbkötransaktionen. 

Konflikten beror på att målposten också har ändrats – postens tidsstämpel är senare än tidsstämpeln för försäljningsintegreringsposten. Målkontrollen sker bara för dubbelriktade tabeller. 

De här posterna flyttas nu till sidan "Hoppade över Synkronisera poster" som du öppnar från sidan för Microsoft Dynamics-anslutningsinställningar i Business Central. Där kan du ange vilka ändringar som ska behållas och sedan synkronisera posterna igen.

## <a name="remove-couplings-between-records"></a>Ta bort kopplingar mellan poster
När något går fel i integrationen och du behöver ta bort kopplingen mellan poster för att sluta synkronisera dem, kan du göra det för en eller flera poster i taget. På sidan **Tabellmappningar för integrering** kan du välja **Bortkoppling** och sedan **Ta bort koppling**. Du kan också, på sidan **Synkroniseringsfel av kopplade data**, välja fel och sedan **Ta bort kopplingar**. 

## <a name="see-also"></a>Se även
[Integrera med Common Data Service](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Ställa in konton för integrering med Common Data Service](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  

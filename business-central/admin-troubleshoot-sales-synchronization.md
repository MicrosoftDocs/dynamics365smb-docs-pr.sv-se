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
ms.openlocfilehash: 1c2181ee381425a168a9b6b6ce321e595a01ed8e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754998"
---
# <a name="troubleshooting-synchronization-errors"></a>Felsöka synkroniseringsfel
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Det finns många rörliga delar som används för att integrera [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] och ibland kan det bli fel. I det här avsnittet beskrivs några vanliga fel som uppstår och du får tips om hur du åtgärdar dem.

Fel inträffar ofta antingen på grund av något som en användare har gjort i fråga om kopplade poster, eller också är något fel med hur integreringen har upprättats. För fel som rör kopplade poster kan användare matcha dem själva. Dessa fel orsakas av åtgärder som att ta bort data i en - men inte båda - affärsappar och sedan synkronisera. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Exempel
I det här videoklippet visas ett exempel på hur du felsöker fel som har uppstått vid synkronisering med Sales. Samma procedur kommer att användas för alla integreringar. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fel som rör hur integreringen ställs in kräver vanligt vis en administratörs uppmärksamhet. Du kan visa dessa fel på sidan **Integreringssynkroniseringsfel**. Exempel på typiska problem är:  
  
* De behörigheter och roller som tilldelats till användare är felaktiga.  
* Administratörskontot har angetts som integreringsanvändare.  
* Lösenordet för integreringsanvändaren ställs in att kräva en ändring när användaren loggar in.  
* Valutakurserna för valutor har inte angetts i den ena eller den andra appen.  
  
Du måste lösa felen manuellt, men det finns ett par sätt på vilka sidan kan hjälpa dig. Som exempel:  

* Fälten **Källa** och **Mål** kan innehålla länkar till den rad där felet hittades. Klicka på länken för att undersöka felet.  
* Åtgärderna **Ta bort transaktioner som är äldre än 7 dagar** och **Ta alla transaktioner** rensar listan. Vanligtvis använder du dessa åtgärder när du har löst orsaken till ett fel som påverkar många poster. Var försiktig. De här åtgärderna kan ta bort fel som fortfarande är relevanta.

Ibland kan tidsstämplar för poster orsaka konflikter. Tabellen "CDS-integreringspost" behåller tidsstämplarna "Senaste synkronisering ändrad den" och "Senaste synkronisering CDS ändrad den" för den senaste integreringen som gjordes i båda riktningarna för en rad. Dessa tidsstämplar jämförs med tidsstämplar på Business Central- och Sales-poster. I Business Central finns tidstämpeln i tabellen Integreringspost.

Du kan filtrera efter transaktioner som ska synkroniseras genom att jämföra radtidsstämplar för fälten "Synk. ändrad i filter" och "Synk. int. tabell" i tabellen "Registermappning för integrering". ändrad i filter".

Konfliktfelmeddelandet "Det går inte att uppdatera kundposten eftersom den har ett senare ändringsdatum än kontoposten" eller "Det går inte att uppdatera kontoposten eftersom den har ett senare ändringsdatum än kundposten" kan inträffa om en rad har en tidstämpel som större än IntegreringTableMapping."Synk. ändrad i filter" men inte är senare än tidsstämpeln på försäljningsintegreringsposten. Det innebär att källraden har synkroniserats manuellt, inte av jobbkötransaktionen. 

Konflikten beror på att målraden också har ändrats – radens tidsstämpel är senare än tidsstämpeln för försäljningsintegreringsposten. Målkontrollen sker bara för dubbelriktade tabeller. 

De här posterna flyttas nu till sidan "Hoppade över Synkronisera poster" som du öppnar från sidan för Microsoft Dynamics-anslutningsinställningar i Business Central. Där kan du ange vilka ändringar som ska behållas och sedan synkronisera posterna igen.

## <a name="remove-couplings-between-records"></a>Ta bort kopplingar mellan poster
När något går fel i integrationen och du behöver ta bort kopplingen mellan poster för att sluta synkronisera dem, kan du göra det för en eller flera poster i taget. Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**. Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**. 

## <a name="see-also"></a>Se även
[Integrera med Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Ställa in konton för integrering med Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  

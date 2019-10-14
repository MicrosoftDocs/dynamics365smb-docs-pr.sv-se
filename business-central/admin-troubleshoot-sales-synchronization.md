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
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304273"
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

## <a name="see-also"></a>Se även
[Integrera med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Ställa in konton för integrering med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  
---
title: Företags- och affärsenhetsmappning | Microsoft-dokument
description: Företagen är både juridiska och affärskonstruktioner och används för att säkra och visualisera affärsdata.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 4f8e5959098e01cd08134a37ae706aa852d88729
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911667"
---
# <a name="data-ownership-models"></a>Modeller för dataägarskap
[!INCLUDE[d365fin](includes/cds_long_md.md)] kräver att du anger en ägare till de data du lagrar. Mer information finns i [Enhetsägarskap](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) i Power Apps-dokumentationen. När du ställer in integreringen mellan [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du välja en av två ägarskapsmodeller för transaktioner som synkroniseras:

* Team 
* Person (användare)

Åtgärder som kan utföras på dessa transaktioner kan styras på användarnivå. Mer information finns i [Användar- och teamenheter](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Vi rekommenderar gruppägandemodellen eftersom den gör det enklare att hantera ägarskap för flera personer.

## <a name="team-ownership"></a>Gruppägarskap
I [!INCLUDE[d365fin](includes/d365fin_md.md)] är ett företag en juridisk person och en affärsenhet som erbjuder metoder att säkra och visualisera affärsdata. Användarna fungerar alltid inom ramen för ett företag. Det närmaste [!INCLUDE[d365fin](includes/cds_long_md.md)] kommer detta koncept är affärsenheten, som inte har några rättsliga eller affärsmässiga följder.

Eftersom affärsenheterna saknar legala eller affärsmässiga konsekvenser kan du inte tvinga fram en 1-till-1-mappning (1:1) för att synkronisera data mellan ett företag och en affärsenhet, vare sig enkelriktad eller dubbelriktad. När du aktiverar synkronisering för ett företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] händer följande i [!INCLUDE[d365fin](includes/cds_long_md.md)] för att möjliggöra synkronisering:

* Vi skapar en företagsenhet som är lika med företagets enhet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Namnet på företaget erhåller suffixet "BC-företags-ID". Till exempel CRONUS International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Vi skapar en standardaffärsenhet som har samma namn som företaget. Till exempel CRONUS International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Vi skapar ett separat ägarteam med samma namn som företaget, och associerar det med affärsenheten. Teamnamnet föregås av "BCI -". Till exempel BCI - CRONUS International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Poster som skapas och synkroniseras till [!INCLUDE[d365fin](includes/cds_long_md.md)] tilldelas teamet "BCI Owner", som är länkat till affärsenheten.

> [!NOTE]
> Om du byter namn på ett företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] uppdateras inte namnen på företaget, verksamheten och teamet som du skapar automatiskt i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Eftersom endast företags-ID:t används för integration påverkas inte synkroniseringen. Om du vill att namnen ska matcha måste du uppdatera företaget, affärsenheten och teamet i [!INCLUDE[d365fin](includes/cds_long_md.md)].

I följande bild visas ett exempel på dessa datainställningar i [!INCLUDE[d365fin](includes/cds_long_md.md)].

![Huvudaffärsenheten ligger högst upp, teamen visas i mitten och sedan företagen längst ned.](media/cds_bu_team_company.png)

I den här konfigurationen ägs transaktioner som är relaterade till företaget Cronus USA av ett team som är länkat till affärsenheten Cronus US <ID> i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Användare som har åtkomst till den affärsenheten via en säkerhetsroll som anges till synlighet på affärsenhetsnivå i [!INCLUDE[d365fin](includes/cds_long_md.md)] kan nu se dessa transaktioner. Följande exempel visar hur du kan använda team för att ge åtkomst till dessa transaktioner.

* Rollen försäljningschef tilldelas till medlemmar av försäljningsteamet för CRONUS USA.
* Användare som har rollen Försäljningschef kan komma åt kontotransaktioner för medlemmar i samma affärsenhet.
* Försäljningsteamet för CRONUS USA är länkat till affärsenheten CRONUS USA som omnämndes tidigare. Medlemmar av försäljningsteamet CRONUS USA kan se alla konton som ägs av användaren CRONUS USA <ID>, som kommer från företagsenheten Cronus USA i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1:1-mappningen mellan affärsenhet, företag och team är emellertid bara en utgångspunkt, precis som visas i följande bild.

![Säkerhetsrollen styr datasynligheten.](media/cds_bu_team_company_2.png)

I det här exemplet skapas en ny europeisk (EUR) rotaffärsenhet i [!INCLUDE[d365fin](includes/cds_long_md.md)] som överordnad för både Cronus DE (Tyskland) och Cronus ES (Spanien). Affärsenheten EUR är inte kopplad till synkronisering. Den kan emellertid ge medlemmarna i försäljningsteamet EUR åtkomst till kontodata i såväl Cronus DE som Cronus ES genom att ange datasynligheten för **Överordnad/underordnad AE** i associerad säkerhetsroll i [!INCLUDE[d365fin](includes/cds_long_md.md)].

Synkroniseringen bestämmer vilka team som ska äga transaktioner. Detta styrs av fältet **Fördefinierat ägarteam** i BCI - <ID>-transaktionen. När en BCI - <ID>-transaktion är aktiverad för synkronisering skapas automatiskt associerad affärsenhet och associerat ägarteamet (om dessa inte redan finns), och fältet **Förvalt ägarteam**. När synkroniseringen är aktiverad för en entitet kan administratören ändra det ägande teamet, men ett team måste alltid tilldelas.

> [!NOTE]
> Posterna blir skrivskyddade när ett företag har lagts till och sparats, så se till att välja rätt företag.

## <a name="choosing-a-different-business-unit"></a>Välja en annan affärsenhet
Du kan ändra affärsenhetsvalet om du använder gruppägandemodellen. Om du använder ägarskapsmodellen för person är standardaffärsenheten alltid markerad. 

Om du väljer en annan affärsenhet, till exempel en som du har skapat tidigare i [!INCLUDE[d365fin](includes/cds_long_md.md)], behåller den sitt ursprungliga namn. Detta innebär att den inte kommer att få ett suffix med företags-ID:t. Vi kommer att skapa ett team som använder namnkonventionen.

När du ändrar en affärsenhet kan du bara välja de affärsenheter som finns på en nivå under huvudaffärsenheten.

## <a name="person-ownership"></a>Personligt ägarskap
Om du väljer ägandeskapsmodellen Personlig måste du ange respektive säljare som ska äga nya transaktioner. Affärsenheten och teamet skapas på det sätt som beskrivs i avsnittet [Gruppägarskap](admin-cds-company-concept.md#team-ownership) section.

Standardaffärsenheten används när ägandemodellen person väljs och du kan inte välja en annan affärsenhet. Teamet som är kopplat till standardaffärsenheten kommer att äga poster för vanliga entiteter, till exempel produktentitet, som inte är relaterade till vissa säljare.

När du kopplar säljare i [!INCLUDE[d365fin](includes/d365fin_md.md)] till användare i [!INCLUDE[d365fin](includes/cds_long_md.md)], kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] att lägga till användaren i standardteamet i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Du kan kontrollera att användare läggs till genom att titta i kolumnen **Standardteammedlem** på sidan **Användare – Common Data Service**. Om användaren inte läggs till kan du lägga till den manuellt genom att använda åtgärden **Lägg till kopplade användare i Team**. Mer information finns i [Synkronisera data i Business Central med Common Data Service](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Se även
[Om [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)
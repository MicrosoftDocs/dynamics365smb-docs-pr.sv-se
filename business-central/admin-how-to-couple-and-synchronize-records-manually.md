---
title: Koppling och synkronisering
description: Genom att synkronisera en mappning av integreringstabellen möjliggörs datasynkronisering i alla poster i en tabell i Business Central eller Dynamics 365 Sales som är kopplade.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8e2b36b4b90e1cc348ef381a6d0f6145a87ed043
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588732"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Koppla och synkronisera poster mellan Dataverse och Business Central

I det här avsnittet beskrivs hur du kopplar en eller flera transaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] med transaktioner i Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. Koppling av poster låter dig visa Dataverse information från [!INCLUDE[prod_short](includes/prod_short.md)] och vice versa. Kopplingen låter dig också synkronisera data mellan posterna. Du kan koppla befintliga poster eller skapa och koppla nya poster.

> [!Note]
> Du kan bara koppla och synkronisera data om din systemadministratör har skapat en anslutning mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**. Om åtgärden är tillgänglig är apparna sammankopplade.   

## <a name="video-example"></a>Videoexempel

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Om du vill koppla en post  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  

    Du kan också bara öppna listsidan och välja den post som du vill koppla.  

2.  Välj åtgärden **konfigurera koppling**.  
3.  Fyll i fälten och välj sedan **OK**.  

## <a name="to-synchronize-a-single-record"></a>Om du vill synkronisera en enda post  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  
2.  Välj åtgärden **synkronisera nu**.  
3.  Om en transaktion kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Om du vill synkronisera en enda transaktion från [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  I [!INCLUDE[crm_md](includes/crm_md.md)] öppnar du formuläret för den transaktion du vill koppla. Till exempel formuläret Kontokort eller Kontaktkort.  
2.  Välj åtgärden **[!INCLUDE[prod_short](includes/prod_short.md)]** i menyfliksområdet för att öppna och koppla transaktioner automatiskt.

> [!Note]
> Du kan endast synkronisera en enskild transaktion automatiskt från [!INCLUDE[crm_md](includes/crm_md.md)] när **Synka endast kopplade transaktioner** är inaktiverat och synkroniseringen har angetts som dubbelriktad eller Från integreringstabell på sidan **Registermappning för integrering** för transaktionen. Mer information finns i [Mappa de tabeller och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>För at koppla flera poster med matchningsbaserad koppling

Du kan ange vilka data som ska synkroniseras för en entitet, t.ex. en kund eller kontakt, genom kopplingsposter som baseras på matchningar. Du kan förfina matchningarna genom att göra sökningen skifteslägeskänslig och tilldela varje matchning en prioritet. Om ingen matchning hittas kan du även ange att du vill skapa entiteten i Dataverse. Mer information finns i [Anpassa matchningsbaserad koppling](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.
2. Välj åtgärden **matchningsbaserad koppling**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Om du vill synkronisera flera poster  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.  
2.  Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.  
3.  Om transaktioner kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="uncoupling-records"></a>Frånkopplingsposter
Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**. Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**.

## <a name="see-also"></a>Se även  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
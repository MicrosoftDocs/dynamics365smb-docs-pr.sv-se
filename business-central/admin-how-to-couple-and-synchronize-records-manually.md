---
title: Koppling och synkronisering | Microsoft-dokument
description: Genom att synkronisera en mappning av integreringstabellen möjliggörs datasynkronisering i alla poster i en tabell i Business Central eller Dynamics 365 Sales som är kopplade.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: b9ea85ea320aea35d1df661be9a9d16502d33776
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378354"
---
# <a name="coupling-and-synchronizing"></a>Koppling och synkronisering
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

## <a name="to-synchronize-multiple-records"></a>Om du vill synkronisera flera poster  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.  
2.  Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.  
3.  Om transaktioner kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="uncoupling-records"></a>Frånkopplingsposter
Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**. Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**.

## <a name="see-also"></a>Se även  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
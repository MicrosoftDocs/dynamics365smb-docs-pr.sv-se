---
title: Koppla och synkronisera poster manuellt | Microsoft Docs
description: Synkronisera en mappning för integreringstabellen tillåter datasynkronisering data i alla poster i en tabell i Business Central och den Dynamics 365 Sales-enhet som används.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8140f71709208a271eff5c8de415b0e95736072
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911411"
---
# <a name="couple-and-synchronize-records-manually"></a>Koppla och synkronisera poster manuellt
I det här avsnittet beskrivs hur du kopplar en eller flera transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] med transaktioner i Common Data Service eller [!INCLUDE[crm_md](includes/crm_md.md)]. Koppling av poster låter dig visa Common Data Service information från [!INCLUDE[d365fin](includes/d365fin_md.md)] och vice versa. Kopplingen låter dig också synkronisera data mellan posterna. Du kan koppla befintliga poster eller skapa och koppla nya poster.

> [!Note]
> Du kan bara koppla och synkronisera data om din systemadministratör har skapat en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och Common Data Service eller [!INCLUDE[crm_md](includes/crm_md.md)]. Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**. Om åtgärden är tillgänglig är apparna sammankopplade.   

## <a name="video-example"></a>Videoexempel

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Om du vill koppla en post  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  

    Du kan också bara öppna listsidan och välja den post som du vill koppla.  

2.  Välj åtgärden **konfigurera koppling**.  
3.  Fyll i fälten och välj sedan **OK**.  

## <a name="to-synchronize-a-single-record"></a>Om du vill synkronisera en enda post  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  
2.  Välj åtgärden **synkronisera nu**.  
3.  Om en transaktion kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Om du vill synkronisera en enda transaktion från [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  I [!INCLUDE[crm_md](includes/crm_md.md)] öppnar du formuläret för den transaktion du vill koppla. Till exempel formuläret Kontokort eller Kontaktkort.  
2.  Välj åtgärden **[!INCLUDE[d365fin](includes/d365fin_md.md)]** i menyfliksområdet för att öppna och koppla transaktioner automatiskt.

> [!Note]
> Du kan endast synkronisera en enskild transaktion automatiskt från [!INCLUDE[crm_md](includes/crm_md.md)] när **Synka endast kopplade transaktioner** är inaktiverat och synkroniseringen har angetts som dubbelriktad eller Från integreringstabell på sidan **Tabellmappning för integrering** för transaktionen. Mer information finns i [Mappa de tabeller och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Om du vill synkronisera flera poster  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.  
2.  Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.  
3.  Om transaktioner kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="see-also"></a>Se även  
[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)

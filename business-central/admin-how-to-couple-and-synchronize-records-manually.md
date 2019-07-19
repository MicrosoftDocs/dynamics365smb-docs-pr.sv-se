---
title: Koppla och synkronisera poster manuellt | Microsoft Docs
description: Synkronisera en mappning för integrationstabellen tillåter datasynkronisering data i alla poster i en tabell i Business Central och den Dynamics 365 for Sales enhet som används.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6d1248ac77208e382c5594af57335df6ff824630
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726773"
---
# <a name="couple-and-synchronize-records-manually"></a>Koppla och synkronisera poster manuellt
I det här avsnittet beskrivs hur du kopplar en eller flera poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i [!INCLUDE[crm_md](includes/crm_md.md)]. Koppling av poster låter dig visa [!INCLUDE[crm_md](includes/crm_md.md)] information från [!INCLUDE[d365fin](includes/d365fin_md.md)] och vice versa. Kopplingen låter dig också synkronisera data mellan posterna. Du kan koppla befintliga poster eller skapa och koppla nya poster.

> [!Note]
> Koppla och synkronisera data med [!INCLUDE[crm_md](includes/crm_md.md)] är endast tillgängligt om administratören har skapat en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)]. Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**. Om åtgärden är tillgänglig är apparna sammankopplade.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Om du vill koppla en post  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  

    Du kan också bara öppna listsidan och välja den post som du vill koppla.  

2.  Välj åtgärden **konfigurera koppling**.  
3.  Fyll i fälten och välj sedan **OK**.  

## <a name="to-synchronize-a-single-record"></a>Om du vill synkronisera en enda post  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  
2.  Välj åtgärden **synkronisera nu**.  
3.  Om en post kan synkroniseras antingen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] eller från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)] välj det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="to-synchronize-multiple-records"></a>Om du vill synkronisera flera poster  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.  
2.  Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.  
3.  Om poster kan synkroniseras antingen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] eller från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)] välj det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## <a name="see-also"></a>Se även  
[Med hjälp av Dynamics 365 for Sales från Business Central](marketing-integrate-dynamicscrm.md)

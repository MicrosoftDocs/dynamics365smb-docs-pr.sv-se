---
title: Så här granskar och anpassar du befintliga databasdata | Microsoft Docs
description: När du skapar ett konfigurationspaket för en lösning kan du visa och anpassa tillgängliga databasdata så att dessa stämmer överens med dina kundbehov. Databastabellen måste vara kopplad till en sida.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "917942"
---
# <a name="review-and-customize-existing-database-data"></a>Så här granskar och anpassar du befintliga databasdata
När du skapar ett konfigurationspaket för en lösning kan du visa och anpassa tillgängliga databasdata så att dessa stämmer överens med dina kundbehov. Databastabellen måste vara kopplad till en sida.  

### <a name="to-customize-data-in-the-database"></a>Så här kan du anpassa data i databasen  

1.  Identifiera tabellerna med data som du vill visa eller anpassa i konfigurationskalkylarket.  

    > [!NOTE]  
    >  Se till att varje tabell tilldelats ett sid-ID. Som standarden [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell fylls detta värdet i automatiskt. För anpassade tabeller måste du ange ID.  

2.  Välj **Databasdata** på fliken **Åtgärder** i gruppen **Visa**.  

     Sidan [!INCLUDE[d365fin](includes/d365fin_md.md)] för sidan öppnas.  

3.  Granska den tillgängliga informationen. Ändra den efter behov genom att ta bort transaktioner som inte är relevanta eller lägga till nya.  

## <a name="see-also"></a>Se även  
 [Så här hanterar du företagskonfigurationen i ett kalkylark](admin-how-to-manage-company-configuration-in-a-worksheet.md)

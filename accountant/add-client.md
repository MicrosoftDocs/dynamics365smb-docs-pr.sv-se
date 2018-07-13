---
title: "Hämta klienter till Dynamics 365 revisorsupplevelse | Microsoft Docs"
description: "Lär dig hur du lägger till befintliga klienter i Accountant Hub för Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/15/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4bc9199b879c23115082b07a81d6da5a0b46e60d
ms.openlocfilehash: 00e0d0a131b586d3aee39b3d08064defff81814a
ms.contentlocale: sv-se
ms.lasthandoff: 05/31/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Lägga till klienter i instrumentpanelen i [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Du kan lägga till en klient med hjälp av fönstret **klienter** som du öppnar genom att välja åtgärd **hantera klienter** i menyfliksområdet. Välj bara **Ny** och fyll sedan i relevanta fält.  

![Lägg till en klient](./media/accountant-add-client/manage-client.png)

Datan i ett kort för varje klient som anges av dig och du kan ändra den efter behov. Men fältet **klient-URL** är kritiskt – detta är hur du får tillgång till varje klients [!INCLUDE [d365fin](includes/d365fin_md.md)]. Använd åtgärden **Validera klient-URL** i menyfliksområdet för att kontrollera att du har angett rätt länk. Den URL du måste ange pekar på klientens [!INCLUDE [d365fin](includes/d365fin_md.md)], inklusive deras domänadress. Till exempel om de har angett en domän, till exempel MyBusiness.com och sedan klickar på länken till deras [!INCLUDE [d365fin](includes/d365fin_md.md)] är *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Innan uppdateringen maj 2018 har den URL du har angett ett annat format med kundens företagsnamn i början. Med uppdateringen maj 2018 är formatet ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, där ```clientdomain``` representerar din klients domän.  

Klien-URL:en används sedan när du väljer menyobjektet **Gå till företag** på instrumentpanelen [!INCLUDE [d365acc](includes/d365acc_md.md)].  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Bli inbjuden till en klients [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]
Ett företag som använder [!INCLUDE [d365fin](includes/d365fin_md.md)]kan bjuda in dig till [!INCLUDE [d365fin](includes/d365fin_md.md)]som deras extern revisor. Om du vill bli inbjuden måste du ge dem den e-postadress som du använder med [!INCLUDE [d365acc](includes/d365acc_md.md)], såsom <em>me@accountant.com</em>. Klientens administratör kan sedan lägga till dig i sina system genom att köra guiden **bjuda in extern revisor**.  

Därför får du e-post från en klient med länkar till deras [!INCLUDE [d365fin](includes/d365fin_md.md)]. Den första länken är en inbjudan för att få tillgång till företaget – öppna länken och acceptera stegen som lägger till klienternas [!INCLUDE [d365fin](includes/d365fin_md.md)]. Den andra länken är för att lägga till den här klienten till instrumentpanelen i [!INCLUDE [d365acc](includes/d365acc_md.md)] som beskrivs ovan.  

När du har accepterat inbjudan kan du har loggat in och kan komma åt den klientens ekonomiska data från rollcentret **Revisor**. Mer information finns i [Revisorupplevelse i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Se även
[Komma igång med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Felsökning [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  


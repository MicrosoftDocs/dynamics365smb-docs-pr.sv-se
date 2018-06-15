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
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8b8d92e114733d87b1866d66ee3111208e233ad3
ms.contentlocale: sv-se
ms.lasthandoff: 05/15/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Lägga till klienter i instrumentpanelen i [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Du kan lägga till en klient med hjälp av fönstret **klienter** som du öppnar genom att välja åtgärd **hantera klienter** i menyfliksområdet. Välj bara **Ny** och fyll sedan i relevanta fält.  

![Lägg till en klient](./media/accountant-add-client/manage-client.png)

Datan i ett kort för varje klient som anges av dig och du kan ändra den efter behov. Men fältet **klient-URL** är kritiskt – detta är hur du får tillgång till varje klients [!INCLUDE [d365fin](includes/d365fin_md.md)]. Använd åtgärdem **Testa klient-URL** i menyfliksområdet för att kontrollera att du har angett rätt länk. Den måste du ange URL-adressen pekar på klientens [!INCLUDE [d365fin](includes/d365fin_md.md)], såsom *<https://mybusiness.financials.dynamics.com>*. Denna URL används sedan när du väljer menyobjektet **Gå till företag** på instrumentpanelen [!INCLUDE [d365acc](includes/d365acc_md.md)].  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Bli inbjuden till en klients [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]
Ett företag som använder [!INCLUDE [d365fin](includes/d365fin_md.md)]kan bjuda in dig till [!INCLUDE [d365fin](includes/d365fin_md.md)]som deras extern revisor. För att bli inbjuden måste du du ge det e-postmeddelande som du använder med [!INCLUDE [d365acc](includes/d365acc_md.md)], såsom <em>me@accountant.com</em>. Kundens administratör kan sedan lägga till dig i sina system genom att köra guiden **bjuda in extern revisor**.  

Därför får du e-post från en klient med länkar till deras [!INCLUDE [d365fin](includes/d365fin_md.md)]. Den första länken är en inbjudan för att få tillgång till företaget – öppna länken och acceptera stegen som lägger till klienternas [!INCLUDE [d365fin](includes/d365fin_md.md)]. Den andra länken är för att lägga till den här klienten till instrumentpanelen i [!INCLUDE [d365acc](includes/d365acc_md.md)] som beskrivs ovan.  

När du har accepterat inbjudan kan du har loggat in och kan komma åt den klientens ekonomiska data från rollcentret **Revisor**. Mer information finns i [Revisorupplevelse i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Se även
[Komma igång med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Felsökning [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  


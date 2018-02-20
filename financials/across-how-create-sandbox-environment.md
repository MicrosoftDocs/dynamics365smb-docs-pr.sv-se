---
title: "Skapa miljö för begränsat läge | Microsoft Docs"
description: "Skapa en miljö där du kan utforska, utbilda demo, utveckla och prova."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3ee160e2c38107aea1342b51d729aa172bbbc3e
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a>Skapa en miljö för begränsat läge
Begränsat läge (förhandsgranskning) är en instans av [!INCLUDE[d365fin](includes/d365fin_md.md)] utanför produktionsmiljön. Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.

## <a name="to-create-a-sandbox-environment"></a>Skapa miljö för begränsat läge.
Du måste ha en prenumeration på [!INCLUDE[d365fin](includes/d365fin_md.md)] för att skapa begränsat läge. Det kan bara finnas ett begränsat läge per prenumeration.

1. Logga in i din instans för produktionsmiljö i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjänsten.
2. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **begränsat läge**, och välj sedan relaterad länk.
![Konfigurera miljö för begränsat läge.](./media/across-sandbox/sandbox-environment-setup.png)
3. Välj **skapa**.  
  En annan flik i webbläsaren öppnas för att slutföra inställningarna för begränsat läge.
> [!NOTE]  
>  Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen *.financials.dynamics.com.   

4. När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.
![välkomstguiden för begränsat läge](./media/across-sandbox/sandbox-wizard.png)

5. Välj **Mer information** om du vill veta om scenarier som du kan pröva i begränsat läge. Klicka på **Stäng** för att fortsätta till rollcenter din [!INCLUDE[d365fin](includes/d365fin_md.md)]-instans för begränsat läge.
6. Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge. Du kan också se vilken typ av miljön i namnlisten på klienten.
![Rollcenteraviseringar för begränsat läge](./media/across-sandbox/sandbox-rolecenter-notification.png)  
I begränsat läge, har en helt ny innehavare skapats. Den här innehavaren laddas med standarddemonstrationsdata för företaget CRONUS. Inga data kopieras till eller på annat sätt överförs från produktionsmiljön när begränsat läge skapas.
7.  När som helst kan du återgå till sidan **begränsat läge** och återställa begränsat läge.
> [!NOTE]  
>  Återställa begränsat läge tar bort den helt och skapar den sedan igen med standarddemonstrationsdata.  

8.  Du kan använda programmarstartbilden för Finance and Operations, Business edition om du vill växla mellan miljöerna för produktion och begränsat läge.
![Begränsat läge Dynamics365 meny](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Det är möjligt för en administratör eller en annan användare att begränsa eller även spärra åtkomsten för vissa användare till begränsat läge. Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper.

![Behörighetsuppsättningar för begränsat läge](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerade funktioner i begränsat läge
### <a name="the-in-client-designer"></a>Designern på klienten.
I begränsat läge finns i designern på klienten aktiverad, som du kan aktivera genom att markera ikonen design ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida.

![Designern på klienten.](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Aktivera avancerade användare
Det går att aktivera och prova avancerade (alla) funktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett begränsat läge för innehavare genom att ange fältet **upplevelse** på sidan **företagsinformation**.

![Avancerad miljö för begränsat läge.](./media/across-sandbox/sandbox-advanced.png)

![Begränsat läge för produktion](./media/across-sandbox/sandbox-production.png)

När du har aktiverat den avancerade funktionen i en begränsad innehavare kan få du tillgång till alla vanliga profiler och rollcenter. Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten.

![Begränsat nytt företag](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


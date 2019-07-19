---
title: Skapa miljö för begränsat läge | Microsoft Docs
description: Skapa en miljö där du kan utforska, utbilda demo, utveckla och prova.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 217310522d7e54eeaa9dbd50df4ff89b0d68517d
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711089"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Skapa en miljö för begränsat läge
Begränsat läge (förhandsgranskning) är en instans av [!INCLUDE[d365fin](includes/d365fin_md.md)] utanför produktionsmiljön. Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.

## <a name="to-create-a-sandbox-environment"></a>Skapa miljö för begränsat läge.
Du måste ha en prenumeration på [!INCLUDE[d365fin](includes/d365fin_md.md)] för att skapa begränsat läge. Det kan bara finnas ett begränsat läge per prenumeration.

1. Logga in i din instans för produktionsmiljö i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjänsten.

2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Miljö för begränsat läge** och välj sedan relaterad länk.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Klicka på knappen **Skapa**.  

    En annan flik med [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnas där du kan slutföra inställningarna i miljön för begränsat läge.

    > [!NOTE]  
    >  Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen *.businesscentral.dynamics.com.

4. När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Välj knappen **lär dig mer** om du vill läsa om scenarier som du kan prova i en miljö för begränsat läge eller välja knappen **Stäng** för att fortsätta till rollcenter för din [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljö för begränsat läge.

    Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge. Du kan också se miljötypen i namnlisten på klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > En miljö för begränsat läge som skapas på det här sättet innehåller endast standarddemonstrationsdata för CRONUS-företaget. Inga data kopieras till eller på annat sätt överförs från produktionsmiljön.<br /><br />
    > Du kan också skapa en miljö för begränsat läge som innehåller produktionsdata. Du måste göra detta i administrationscentret. Mer information finns i [Hantera miljöer](/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjälpen för utvecklare och IT-proffs.

6. När som helst kan du återgå till sidan **begränsat läge** och återställa begränsat läge.
    > [!NOTE]  
    >  Återställa begränsat läge tar bort den helt och skapar den sedan igen med standarddemonstrationsdata.  

7. Du kan använda Business Centrals programmarstartbild om du vill växla mellan miljö för produktion och begränsat läge.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. Det är möjligt för en administratör eller en annan användare att begränsa eller även spärra åtkomsten för vissa användare till begränsat läge. Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerade funktioner i begränsat läge
### <a name="designer"></a>Designer
I begränsat läge finns i **designern** på klienten aktiverad, som du kan aktivera genom att markera ikonen ![designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Aktivera avancerade användare
Det går att aktivera och prova avancerade (alla) funktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett begränsat läge för innehavare genom att ange fältet **upplevelse** på sidan **företagsinformation**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

När du har aktiverat den avancerade funktionen i en begränsad innehavare kan få du tillgång till alla vanliga profiler och rollcenter. Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

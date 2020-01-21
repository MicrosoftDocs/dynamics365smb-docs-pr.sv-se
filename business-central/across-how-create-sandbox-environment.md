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
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910642"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a>Skapa en miljö för begränsat läge i [!INCLUDE [prodshort](includes/prodshort.md)]

Med [!INCLUDE [prodshort](includes/prodshort.md)] kan du enkelt skapa en säker miljö där du kan testa, träna eller felsöka utan att störa företagets arbetsprocesser eller företagsdata. En sådan icke-produktionsmiljö kallas för *begränsat läge*. Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.  

Administratören kan skapa miljö för begränsat läge i [administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men om du snabbt vill testa något kan du skapa en miljö för begränsat läge från insidan [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Tekniskt sett skiljer sig miljöer i begränsat läge mycket från produktionsmiljöer, även om administratören skapar ett begränsat läge som omfattar produktionsdata. Du kan inte använda begränsat läge för benchmarking och du kan exempelvis inte begära en databasexport. Om du vill skapa ett begränsat läge för benchmark-hantering kan administratören skapa en dedikerad produktionsmiljö i administrationscentret. Mer information finns i [Typer av miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a>Skapa miljö för begränsat läge i din [!INCLUDE [prodshort](includes/prodshort.md)]

1. Logga in i din instans för produktionsmiljö i [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **miljö för begränsat läge** och välj sedan relaterad länk.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Klicka på knappen **Skapa**.  

    En annan flik med [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnas där du kan slutföra inställningarna i miljön för begränsat läge.

    > [!NOTE]  
    >  Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen *.businesscentral.dynamics.com.

När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Du kan välja **lär dig mer** om du vill läsa om utvecklarscenarier som du kan prova i en miljö för begränsat läge eller välja knappen **Stäng** för att fortsätta till rollcenter för din [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljö för begränsat läge.

Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge. Du kan också se miljötypen i namnlisten på klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> En miljö för begränsat läge som skapas på det här sättet innehåller endast standarddemonstrationsdata för CRONUS-företaget. Inga data kopieras till eller på annat sätt överförs från produktionsmiljön.<br /><br />
> Du kan också skapa en miljö för begränsat läge som innehåller produktionsdata. Du måste göra detta i administrationscentret. Mer information finns i [Hantera miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjälpen för utvecklare och IT-proffs.

När som helst kan du återgå till sidan **begränsat läge** och återställa begränsat läge.

> [!NOTE]  
> Återställa begränsat läge tar bort den helt och skapar den sedan igen med standarddemonstrationsdata.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

En administratör kan begränsa eller även spärra åtkomsten för vissa användare till begränsat läge. Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerade funktioner i begränsat läge

Miljön i begränsat läge är inte minst användbar eftersom den innehåller ett par praktiska funktioner.

### <a name="designer"></a>Designer

I en miljö för begränsat läge kan du se att **designer** är aktiverat. Du kan aktivera designer genom att välja ikonen ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida eller genom att välja menyalternativet **design** på inställningsmenyn ![inställningar](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Aktivera avancerade användare
Det går att aktivera och prova alla funktioner i standardversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett begränsat läge för klientorganisation genom att ställa in fältet **Erfarenhet** på sidan **Företagsinformation**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

När du har aktiverat användarupplevelsen *Premium* får du tillgång till alla standardprofiler (roller) och Rollcenter i standardversionen. Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten. Alternativt kan du kontakta en återförsäljare för en demonstration av funktionerna. Mer information finns i [Hur hittar jag efter en återförsäljningspartner?](across-faq.md#findpartner).  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a>Se även

[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Utvärderingsversioner och prenumerationer](across-preview.md)  
[Hantera miljöer i Business Central administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  

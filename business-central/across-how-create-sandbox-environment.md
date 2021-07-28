---
title: Skapa miljö för begränsat läge
description: Skapa en begränsad miljö för säkerhet där du kan utforska, utbilda, demonstrera, utveckla, felsöka och prova inifrån Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: 2f4ca6a98aac49fa5fea7d8658ef51a9510c97d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437683"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Skapa en miljö för begränsat läge i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du enkelt skapa en säker miljö där du kan testa, träna eller felsöka utan att störa företagets arbetsprocesser eller företagsdata. En sådan icke-produktionsmiljö kallas för *begränsat läge*. Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.  

Administratören hanterar miljö för begränsat läge i [administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men om du snabbt vill testa något kan du skapa en miljö för begränsat läge från insidan [!INCLUDE[prod_short](includes/prod_short.md)]. När du är klar kan du ta bort det begränsade läget med hjälp av administrationscentret.  

> [!NOTE]
> Tekniskt sett skiljer sig miljöer i begränsat läge mycket från produktionsmiljöer, även om administratören skapar ett begränsat läge som omfattar produktionsdata. Du kan inte använda begränsat läge för benchmarking och du kan exempelvis inte begära en databasexport. Om du vill skapa ett begränsat läge för benchmark-hantering kan administratören skapa en dedikerad miljö i administrationscentret. Mer information finns i [Produktionsmiljöer and miljöer för begränsat läge](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Skapa miljö för begränsat läge i din [!INCLUDE[prod_short](includes/prod_short.md)]

1. Logga in i din instans för produktionsmiljö i [!INCLUDE[prod_short](includes/prod_short.md)].

2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **miljö för begränsat läge** och väljer sedan relaterad länk.
    <!-- ![Sandbox Environment Setup.](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Klicka på knappen **Skapa**.  

    En annan flik med [!INCLUDE[prod_short](includes/prod_short.md)] öppnas där du kan slutföra inställningarna i miljön för begränsat läge.

    > [!NOTE]  
    >  Om du har ett popup-fönster aktiverat i din webbläsare, kan du ändra koden så att URL-adresser tillåts från adressen *.businesscentral.dynamics.com.

När begränsat läge är klart, omdirigeras till välkomstguiden för begränsat läge.
<!-- ![Sandbox Welcome Wizard.](./media/across-sandbox/sandbox-wizard.png) -->

Du kan välja **lär dig mer** om du vill läsa om utvecklarscenarier som du kan prova i en miljö för begränsat läge eller välja knappen **Stäng** för att fortsätta till rollcenter för din [!INCLUDE[prod_short](includes/prod_short.md)]-miljö för begränsat läge.

Högst upp i Rollcentret visas ett meddelande att informera dig om att det är begränsat läge. Du kan också se miljötypen i namnlisten på klienten.
    <!-- ![Sandbox RoleCenter Notification.](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> En miljö för begränsat läge som skapas på det här sättet innehåller endast standarddemonstrationsdata för CRONUS-företaget. Inga data kopieras till eller på annat sätt överförs från produktionsmiljön.
>
> Du kan också skapa en begränsad miljö baserad på produktionsdata. Du måste göra detta i administrationscentret. Mer information finns i [Hantera miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i utvecklar- och administrationsinnehållet.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu.](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

En administratör kan begränsa eller även spärra åtkomsten för vissa användare till begränsat läge. Detta kan göras med hjälp av produktens standardsäkerhetsfunktioner som användarkort, användargrupper och behörighetsgrupper. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets.](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avancerade funktioner i begränsat läge

Miljön i begränsat läge är inte minst användbar eftersom den innehåller ett par praktiska funktioner:

* [Avancerad användarupplevelse](#advanced-user-experience)  
* [Fullständiga exempeldata](#complete-sample-data)  
* [Designer](#designer)  

### <a name="advanced-user-experience"></a>Avancerad användarupplevelse

Det går att aktivera och prova alla funktioner i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)]  i ett begränsat läge för klientorganisation genom att ställa in fältet **Erfarenhet** på sidan **Företagsinformation** till *Premium*. Leta upp sidan **företagsinformation** i menyn :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="ikonen Inställningar":::. meny.  

När du har aktiverat användarupplevelsen *Premium* får du tillgång till alla standardprofiler (roller) och Rollcenter i standardversionen. Du kan också skapa ett utvärderingsföretag som helt har ställts in, inklusive demonstrationsdata och tillgång till avancerade delar av produkten. Alternativt kan du kontakta en återförsäljare för en demonstration av funktionerna. Mer information finns i [Hur hittar jag efter en återförsäljningspartner?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Fullständiga exempeldata

Om du behöver ytterligare exempeldata kan du prata med återförsäljningspartnern.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Så här skapar du ett företag med fullständiga exempeldata i ett begränsat läge

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Företag** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och välj sedan **Skapa nytt företag**.  
3. På sidan **Assisterad konfiguration för att skapa ett företag** välj **Nästa**.  
4. Ange ett namn på det nya företaget och sedan i fältet **Välj data och konfiguration för att komma igång** välj **Avancerad utvärdering – fullständig exempeldata**.  
5. Följ resten av instruktionerna i assisterad konfiguration.  

När assisterad konfiguration är klar kan du börja utforska det nya företaget med de fullständiga exempeldata. Mer information finns i [Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Designer

I en miljö för begränsat läge kan du se att **designer** är aktiverat. Du kan aktivera Designer genom att välja designikonen ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida eller genom att välja menyalternativet **Design** på menyn ![Inställningar](media/ui-experience/settings_icon_small.png).  

Mer information finns i [Använda designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i utvecklar- och administrationsinnehållet (enbart på engelska).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Se även

[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Utvärderingsversioner och prenumerationer](across-preview.md)  
[Hantera miljöer i Business Central administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Begränsade miljöer
description: Lär dig mer om hur en dedikerad miljö kan hjälpa dig att utforska, lära dig, demonstrera, utveckla, felsöka och testa Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 07/27/2021
ms.author: solsen
ms.openlocfilehash: f704afaf8e7c581aa1f8e65bd06e04fd31d0056a
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688310"
---
# <a name="sandbox-environments-in-prod_short"></a>Begränsade miljöer i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] online kan du enkelt få en säker miljö där du kan testa, träna eller felsöka utan att störa företagets arbetsprocesser eller affärsdata. En sådan icke-produktionsmiljö kallas för *begränsat läge*. Isolerad från produktionen är begränsat läge stället för att säkert utforska, lära sig, demonstrera, utveckla och testa tjänsten utan att risk för att data och inställningar påverkas i din produktionsmiljö.  

Administratören hanterar begränsade miljöer i [administrationscentret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Om du exempelvis vill skapa ett begränsade läge för benchmark-hantering kan administratören skapa en dedikerad miljö i administrationscentret. Mer information finns i [Produktions och begränsade miljöer](/dynamics365/business-central/dev-itpro/administration/environment-types) i utvecklar- och administrationsinnehållet.  

Du kan också använda begränsade miljöer på ett säkert sätt i utbildningssyfte, t. ex. för att följa en utbildningsväg från [Microsoft Learn](/learn/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), eftersom det är en säker miljö att experimentera med. Om något går fel tar du bara bort begränsade miljön och börjar om.  

När du är klar kan du ta bort det begränsade läget med hjälp av administrationscentret.  

> [!NOTE]
> Tekniskt sett skiljer sig begränsade miljöer mycket från produktionsmiljöer. Administratören kan skapa en begränsade miljö som omfattar produktionsdata - men det är fortfarande en begränsade miljö, och du kan därför exempelvis inte begära en databasrapport. Mer information finns i [Begränsade miljöer](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) i utvecklar- och administrationsinnehållet.

Miljön i begränsat läge är inte minst användbar eftersom den innehåller ett par praktiska funktioner:

* [Avancerad användarupplevelse](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Designer](#designer)  

## <a name="advanced-user-experience"></a>Avancerad användarupplevelse

Det går att aktivera och prova alla funktioner i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)]  i ett begränsat läge för klientorganisation genom att ställa in fältet **Erfarenhet** på sidan **Företagsinformation** till *Premium*. Leta upp sidan **företagsinformation** i menyn :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="ikonen Inställningar":::. meny.  

När du har aktiverat användarupplevelsen *Premium* får du tillgång till alla standardprofiler (roller) och Rollcenter i standardversionen. Alternativt kan du kontakta en återförsäljare för en demonstration av funktionerna. Mer information finns i [Hur hittar jag efter en återförsäljningspartner?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Fullständiga exempeldata

Om du behöver ytterligare exempeldata kan du prata med återförsäljningspartnern.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Designer

I en miljö för begränsat läge kan du se att **designer** är aktiverat. Du kan aktivera Designer genom att välja designikonen ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) på en sida eller genom att välja menyalternativet **Design** på menyn ![Inställningar](media/ui-experience/settings_icon_small.png).  

Mer information finns i [Använda designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i utvecklar- och administrationsinnehållet (enbart på engelska).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Se även

[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Utvärderingsversioner och prenumerationer](across-preview.md)  
[Hantera miljöer i Business Central administrationscenter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Produktions- och begränsade miljöer](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

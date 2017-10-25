---
title: "Så här ställer du in lagerplatstyper | Microsoft Docs"
description: "Du kan dirigera flödet av artiklar via lagerplatser som du har definierat för särskilda distributionslageraktiviteter. Du ger varje lagerplats dess grundläggande flödesaktiviteter, genom att tilldela lagerplatsen en lagerplatstyp, och definierar därmed det sätt som lagerplatsen ska användas på."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aaa710de292e7f4bd7bfd32238160b332f24cad3
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bin-types"></a>Så här: Skapa Lagerplatstyper
Du kan dirigera flödet av artiklar via lagerplatser som du har definierat för särskilda distributionslageraktiviteter. Du ger varje lagerplats dess grundläggande flödesaktiviteter, genom att tilldela lagerplatsen en lagerplatstyp, och definierar därmed det sätt som lagerplatsen ska användas på.  

Det finns åtta olika lagerplatstyper. Du kan använda alla åtta olika lagerplatstyperna i distributionslagret, eller välja att endast använda lagerplatstyperna INLEVERERA, ARTINFPLOC, LEVERERA och KS. De här fyra lagerplatstyperna aktiverar förslag på hur artikelflödet ska se ut och du kan även registrera lageravvikelser.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Så här skapar du de lagerplatstyper som du vill använda  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Lagerplatstyper** och välj sedan relaterad länk.  
2.  I fönstret **Lagerplatstyper** skapar du en kod på tio tecken för en lagerplatstyp.  
3.  Välj de aktiviteter som kan utföras med varje lagerplatstyp.  

> [!NOTE]  
>  Lagerplatstyper är bara tillgängliga om du använder dirigerad artikelinförsel och plockning för lagerstället.  

lagerplatstypen styr bara hur en lagerplats används när artiklar flyttas i distributionslagret. Du kan alltid åsidosätta förslagen för valfritt distributionslagerdokument och du kan flytta artiklar till eller från valfri lagerplats genom att utföra en lagerplatstransport.  

De lagerplatstyper som du kan skapa visas nedan.  

|Lagerplatstyp|Description|  
|------------------|---------------------------------------|  
|INLEVNS|Artiklar som har registrerats som bokförda inleveranser, men som ännu inte har förts in.|  
|LEVERERA|Artiklar som har plockats till utleveransrader, men som ännu inte har bokförts som levererade.|  
|ARTIKELINFÖRSEL|Artiklar som normalt ska lagras i stora enheter, men som du inte vill att programmet ska använda vid plockning. Eftersom de här lagerplatserna inte används för plockning, varken för produktionsorder eller utleveranser, kan användningen av en lagerplats av typen Artikelinförsel vara begränsad, men den är användbar om du har köpt ett stort antal artiklar. Lagerplatser av den här typen bör alltid ha en låg lagerplatsordning, så att när mottagna artiklar förs in, görs det först med andra högprioriterade ARTINFPLOC-lagerplatser som är kopplade till artikeln. Om du använder den här typen av lagerplats måste du regelbundet utföra återanskaffningar för lagerplatsen, så att de artiklar som lagras där också är tillgängliga på lagerplatser av typen ARTINFPLOC och PLOCKA.|  
|PLOCKA|Artiklar som endast ska användas för plockning, till exempel för artiklar med ett utgångsdatum som snart har uppnåtts, som du har flyttats till den här typen av lagerplats. Du bör ange en hög lagerplatsordning på de här lagerplatserna, så att de föreslås för plockning först.|  
|ARTINFPLOC|Artiklar på lagerplatser som föreslås för både artikelinförsel- och plockningsfunktioner. Lagerplatser av den här typen har förmodligen olika lagerplatsordning. Du kan skapa volymlagerplatser av den här typen med låg lagerplatsordning jämfört med de vanliga plocklagerplatserna eller lagerplatserna för framåtplockning.|  
|KS|Den här lagerplatsen används för lagerjusteringar om du anger lagerplatsen i fältet **Justering lagerplatskod** på lagerställekortet. Du kan även skapa lagerplatser av den här typen för felaktiga artiklar och artiklar om ska kontrolleras. Du kan flytta artiklar till den här lagerplatstypen om du vill isolera dem från det vanliga artikelflödet.<br /><br /> **OBS:** Till skillnad från andra lagerplatstyper har **KS** lagerplatstypen inga av artikelhanteringskryssrutorna markerade som standard. Det betyder att lagerplatsinnehåll som du placerar i en KS lagerplats undantas från artikelflöden.|  

## <a name="see-also"></a>Se även
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


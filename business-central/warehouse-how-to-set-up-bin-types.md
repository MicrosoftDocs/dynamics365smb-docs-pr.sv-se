---
title: Så här ställer du in lagerplatstyper | Microsoft Docs
description: Du kan dirigera flödet av artiklar via lagerställen som du har definierat för särskilda distributionslageraktiviteter. Du ger varje lagerplats dess grundläggande flödesaktiviteter, genom att tilldela lagerstället en lagerplatstyp, och definierar därmed det sätt som lagerstället ska användas på.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a5e05531e1cadc32b609cd2fb4f50a575ef87f5b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386330"
---
# <a name="set-up-bin-types"></a>Skapa lagerplatstyper
Du kan dirigera flödet av artiklar via lagerställen som du har definierat för särskilda distributionslageraktiviteter. Du ger varje lagerplats dess grundläggande flödesaktiviteter, genom att tilldela lagerstället en lagerplatstyp, och definierar därmed det sätt som lagerstället ska användas på.  

Det finns sex typer: Du kan använda alla sex olika lagerplatstyperna i distributionslagret, eller välja att endast använda lagerplatstyperna INLEVERERA, ARTINFPLOC, LEVERERA och KS. De här fyra lagerplatstyperna aktiverar förslag på hur artikelflödet ska se ut och du kan även registrera lageravvikelser.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Så här skapar du de lagerplatstyper som du vill använda  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **lagerplatstyper** och välj sedan relaterad länk.  
2.  På sidan **Lagerplatstyper** skapar du en kod på tio tecken för en lagerplatstyp.  
3.  Välj de aktiviteter som kan utföras med varje lagerplatstyp.  

> [!NOTE]  
>  Lagerplatstyper är bara tillgängliga om du använder dirigerad artikelinförsel och plockning för lagerstället.  

lagerplatstypen styr bara hur en lagerplats används när artiklar flyttas i distributionslagret. Du kan alltid åsidosätta förslagen för valfritt distributionslagerdokument och du kan flytta artiklar till eller från valfri lagerplats genom att utföra en lagerplatstransport.  

De lagerplatstyper som du kan skapa visas nedan.  

|Lagerplatstyp|Description|  
|------------------|---------------------------------------|  
|INLEVNS|Artiklar som har registrerats som bokförda inleveranser, men som ännu inte har förts in.|  
|LEVERERA|Artiklar som har plockats till utleveransrader, men som ännu inte har bokförts som levererade.|  
|ARTIKELINFÖRSEL|Artiklar som normalt ska lagras i stora enheter, men som du inte vill att programmet ska använda vid plockning. Eftersom de här lagerställena inte används för plockning, varken för produktionsorder eller utleveranser, kan användningen av en lagerplats av typen Artikelinförsel vara begränsad, men den är användbar om du har köpt ett stort antal artiklar. Lagerställen av den här typen bör alltid ha en låg lagerplatsordning, så att när mottagna artiklar förs in, görs det först med andra högprioriterade ARTINFPLOC-lagerställen som är kopplade till artikeln. Om du använder den här typen av lagerplats måste du regelbundet utföra återanskaffningar för lagerstället, så att de artiklar som lagras där också är tillgängliga på lagerställen av typen ARTINFPLOC och PLOCKA.|  
|PLOCKA|Artiklar som endast ska användas för plockning, till exempel för artiklar med ett utgångsdatum som snart har uppnåtts, som du har flyttats till den här typen av lagerplats. Du bör ange en hög lagerplatsordning på de här lagerställena, så att de föreslås för plockning först.|  
|ARTINFPLOC|Artiklar på lagerställen som föreslås för både artikelinförsel- och plockningsfunktioner. Lagerställen av den här typen har förmodligen olika lagerplatsordning. Du kan skapa volymlagerställen av den här typen med låg lagerplatsordning jämfört med de vanliga plocklagerställena eller lagerställena för framåtplockning.|  
|KS|Den här lagerstället används för lagerjusteringar om du anger lagerstället i fältet **Justering lagerställeskod** på lagerställekortet. Du kan även skapa lagerställen av den här typen för felaktiga artiklar och artiklar om ska kontrolleras. Du kan flytta artiklar till den här lagerplatstypen om du vill isolera dem från det vanliga artikelflödet.<br /><br /> **OBS:** Till skillnad från andra lagerplatstyper har **KS** lagerplatstypen inga av artikelhanteringskryssrutorna markerade som standard. Det betyder att lagerställesinnehåll som du placerar i en KS lagerplats undantas från artikelflöden.|  

## <a name="see-also"></a>Se även
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
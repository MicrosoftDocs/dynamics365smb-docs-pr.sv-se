---
title: Bryta ned volym med dirigerad artikelinförsel och plockning
description: Lär dig hur du aktiverar automatisk uppdelning av bulk med dirigerad artikelinförsel och plockning, samt enhetsbrytning vid i plockningar, artikelinförsel, transporter med mera.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: a3e992b86b2c53393ee385fd4abde05bd2b915f2
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6324845"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Aktivera automatisk volymnedbrytning med dirigerad artikelinförsel och plockning
För lagerställen, som använder artikelinförsel och plockning, kan [!INCLUDE[prod_short](includes/prod_short.md)] i olika situationer, automatiskt använda brytenhet, d.v.s. dela upp en större enhet till mindre enheter, när du skapar lagerinstruktioner som uppfyller behoven hos källdokument, produktionsorder eller intern plockning och artikelinförsel. Med brytenhet menas ibland också samling av mindre måttenheter, om det behövs, för att uppfylla utgående förfrågningar, genom att analysera den större måttenheten i ursprungsdokumentet eller produktionsorder till de mindre enheter som är tillgängliga i distributionslagret.   

## <a name="breakbulking-in-picks"></a>Enhetsbrytning vid plockning  
Om du vill lagra artiklar i flera olika måttenheter och tillåta dem att kombineras automatiskt efter behov vid plockning väljer du fältet **Tillåt brytenhet** på lagerställekortet.  

När en aktivitet ska utföras söker programmet automatiskt efter en artikel i den begärda måttenheten. Om artikeln inte finns i denna enhet och du har valt fältet, föreslår programmet att du bryter ned en större måttenhet till den mindre måttenhet som behövs.  

Om systemet bara hittar mindre måttenheter, föreslår programmet att du samlar ihop flera artiklar för att komma upp i den kvantitet som begärs på utleverans- eller produktionsordern. Det som sedan sker är att den större måttenheten i ursprungsdokumentet bryts ned i mindre enheter för plockning.  

## <a name="breakbulking-in-put-aways"></a>Enhetsbrytning vid artikelinförsel  
Vid en artikelinförsel i distributionslagret föreslås automatiskt åtgärdsrader för Placera i den måttenhet som används i artikelinförseln, till exempel enheter, även om artiklarna inlevereras i en annan måttenhet.  

## <a name="breakbulking-in-movements"></a>Enhetsbrytning vid transport  
Enhetsbrytning sker också automatiskt vid påfyllningstransporter om fältet **Tillåt brytenhet** är valt på snabbfliken **Alternativ** på sidan **Beräkna lagerplatsåteranskaffning**.  

Du kan granska resultaten av enhetskonverteringsprocessen som övergångsrader för enhetsbrytning i instruktionerna för artikelinförsel, plockning eller transport.  

> [!NOTE]  
>  Om du väljer fältet **Sätt brytenhetsfilter** i huvudet för instruktionerna för distributionslagret, döljs enhetsbrytningsraderna om det uteslutande är den större måttenheten som ska användas. Exempel: Om en lastpall består av 12 enheter och samtliga enheter kommer att användas, dirigeras du under plockningen att ta en lastpall och placera 12 enheter. Om du bara ska plocka nio enheter döljs inte enhetsbrytningsraderna, även om du markerar fältet **Brytenhetsfilter**, eftersom du måste placera de återstående tre enheterna någonstans i distributionslagret.  

> [!NOTE]  
>  Om du vill att måttenheterna ska fungera så bra som möjligt i distributionslagret, också när du använder enhetsbrytning, ska du alltid försöka göra följande:  
>   
> - Ange den minsta måttenhet som du tror kommer att användas i distributionslagret som basmåttenhet för artiklar.  
> - Ange alternativa måttenheter för artiklar som multiplar av basmåttenheten.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: "Så här ställer du in resursfördelningar | Microsoft Docs"
description: "Lär dig hur systemet kan hjälpa dig tilldela någon som har de kvalifikationer som krävs för att tillhandahålla tjänster."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6c20c0b346186adad6e4b125dbd48bd0d3f56ab2
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-resource-allocation"></a>Så här kan du ställa in resursfördelningar
För att säkerställa att en serviceuppgift utförs är det viktigt att hitta en resurs som är kvalificerad att göra arbetet. Du kan ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)] så att det är enkelt att allokera någon som har rätt kunskaper för projektet. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kallas detta _resursfördelning_. Du kan fördela resurser utifrån deras kunskaper, tillgänglighet, eller om de finns i samma servicezon som kunden. 

Om du vill använda resursfördelning, måste du ställa in:  
  
* De kunskaper som krävs för att reparera och underhålla serviceartiklar. Du tilldelar dem till serviceartiklar och resurser.  
* Geografiska områden, kallade zoner som anges för din marknad. Det kan t.ex. vara öst, väst, mittregion o.s.v. Du tilldelar dessa till kunder och resurser.  
* Om du vill visa resursernas kunskaper och zoner och om du vill visa en varning om någon väljer icke-kvalificerade resurser eller resurser som inte finns i kundzonen.  

## <a name="to-set-up-skills"></a>Så här ställer du in kvalifikationer
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **kvalifikationer** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Du tilldelar kvalifikationer till serviceartiklar och resurser.
1. Välj den ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") ikon, ange **Serviceartiklar** eller **Resurser**, och välj sedan relaterad länk.  
2. Öppna kortet för den serviceartikel eller resurs och välj något av följande:  
  
    * För serviceartiklar, välj **Resurskvalifikationer**.  
    * För resurser, välj **kvalifikationer**.  

## <a name="to-set-up-zones"></a>Så här skapar du zoner:
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **kvalifikationer** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Så här tilldelar du zoner till kunder och resurser 
1. Välj den ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") ikon, ange **Kunder** eller **Resurser**, och välj sedan relaterad länk.  
2. Öppna kortet för den serviceartikel eller resurs och välj något av följande:  
  
    * För kunder, väljer du en zon i fältet **Servicezonskod**.  
    * För resurser, väljer du åtgärden **servicezoner**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Om du vill ange vad som ska visas när en resurs har valts
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **serviceinställningar** och välj sedan relaterad länk. 
2. I fältet **Resurskvalifikationsförbr**, välj ett av alternativen som beskrivs i följande tabell.  
  
    |**Alternativ**|**Beskrivning**|  
    |------------|-------------|  
    |Visad kod | Visar endast koden.|  
    |Visad varning | Informationen visas och en varning visas om du väljer en resurs som inte är kvalificerade.|  
    |Inte använd | Den här informationen visas inte.|  

## <a name="to-update-resource-capacity"></a>Så här uppdaterar du resurskapacitet:  
Du kan behöva ändra kapaciteten för resurser.  
  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **resurskapacitet**, och välj sedan relaterad länk.  
2. Välj resursen och välj sedan åtgärd **Ange kapacitet**.  
3. Gör önskade ändringar och klicka på **uppdatera kapacitet**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Uppdatera kunskaper för artiklar, serviceartiklar eller serviceartikelgrupper
Om du vill ändra de kvalifikationskoder som har tilldelats till artiklar, till exempel från **PC** till **PCS**, gör du det för en artikel, serviceartikel eller för alla artiklar i en serviceartikelgrupp.  
  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Artiklar**, **Serviceartikel**, eller **Serviceartikelgrupp** och välj sedan relaterad länk.  
2. Välj enheten som ska uppdateras och välj sedan åtgärd **Resurskvalifikationer**.  
3. På den rad där den kod som ska ändras finns, väljer du önskad kvalifikationskod i fältet **Kvalifikationskod**.  
4.  Om artikeln har associerade serviceartiklar öppnas en dialogruta med två alternativ:  
  
    * Ändra kvalifikationskoderna till det valda värdet: Välj det här alternativet om du vill ersätta den gamla kvalifikationskoden med den nya för alla relaterade serviceartiklar.  
    * Ta bort kvalifikationskoderna eller uppdatera relationen: Välj det här alternativet om du vill ändra endast den här artikelns kvalifikationskod. Kvalifikationskoden för de relaterade serviceartiklarna kommer att omfördelas, vilket innebär att fältet **Tilldelad från** kommer att uppdateras.  
  
## <a name="see-also"></a>Se även
[Så här fördelar du resurser:](service-how-to-allocate-resources.md)  
[Ställa in arbetstimmar och servicetider](service-how-setup-work-service-hours.md)  
[Så här: Skapa felrapportering](service-how-setup-fault-reporting.md)  
[Så här skapar du koder för standardservice](service-how-setup-service-coding.md)  
 



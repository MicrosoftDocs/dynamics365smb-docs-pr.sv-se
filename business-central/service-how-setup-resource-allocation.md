---
title: Så här ställer du in resursfördelningar | Microsoft Docs
description: Lär dig hur systemet kan hjälpa dig tilldela någon som har de kvalifikationer som krävs för att tillhandahålla tjänster.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-resource-allocation"></a><a name="set-up-resource-allocation"></a>Så här skapar du resursfördelningar
För att säkerställa att en serviceuppgift utförs är det viktigt att hitta en resurs som är kvalificerad att göra arbetet. Du kan ställa in [!INCLUDE[prod_short](includes/prod_short.md)] så att det är enkelt att allokera någon som har rätt kunskaper för projektet. I [!INCLUDE[prod_short](includes/prod_short.md)] kallas detta _resursfördelning_. Du kan fördela resurser utifrån deras kunskaper, tillgänglighet, eller om de finns i samma servicezon som kunden. 

Om du vill använda resursfördelning, måste du ställa in:  
  
* De kunskaper som krävs för att reparera och underhålla serviceartiklar. Du tilldelar dem till serviceartiklar och resurser.  
* Geografiska områden, kallade zoner som anges för din marknad. Det kan t. ex. vara öst, väst, mittregion o.s.v. Du tilldelar dessa till kunder och resurser.  
* Om du vill visa resursernas kunskaper och zoner och om du vill visa en varning om någon väljer icke-kvalificerade resurser eller resurser som inte finns i kundzonen.  

## <a name="to-set-up-skills"></a><a name="to-set-up-skills"></a>Så här ställer du in kvalifikationer
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kvalifikationer** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><a name="to-assign-skills-to-service-items-and-resources"></a>Du tilldelar kvalifikationer till serviceartiklar och resurser.
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Tjänstartiklar** eller **Resurser** och väljer sedan relaterad länk.  
2. Öppna kortet för den serviceartikel eller resurs och välj något av följande:  
  
    * För serviceartiklar, välj **Resurskvalifikationer**.  
    * För resurser, välj **kvalifikationer**.  

## <a name="to-set-up-zones"></a><a name="to-set-up-zones"></a>Så här skapar du zoner:
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Zoner** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><a name="to-assign-zones-to-customers-and-resources"></a>Så här tilldelar du zoner till kunder och resurser
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** eller **Resurser** och väljer sedan relaterad länk.  
2. Öppna kortet för den serviceartikel eller resurs och välj något av följande:  
  
    * För kunder, väljer du en zon i fältet **Servicezonskod**.  
    * För resurser, väljer du åtgärden **servicezoner**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Om du vill ange vad som ska visas när en resurs har valts
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfigurera servicehantering** och väljer sedan relaterad länk. 
2. I fältet **Resurskvalifikationsförbr**, välj ett av alternativen som beskrivs i följande tabell.  
  
    |**Alternativ**|**Beskrivning**|  
    |------------|-------------|  
    |Visad kod | Visar endast koden.|  
    |Visad varning | Informationen visas och en varning visas om du väljer en resurs som inte är kvalificerade.|  
    |Inte använd | Den här informationen visas inte.|  

## <a name="to-update-resource-capacity"></a><a name="to-update-resource-capacity"></a>Så här uppdaterar du resurskapacitet:
Du kan behöva ändra kapaciteten för resurser.  
  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Resurskapacitet** och väljer sedan relaterad länk.  
2. Välj resursen och välj sedan åtgärd **Ange kapacitet**.  
3. Gör önskade ändringar och klicka på **uppdatera kapacitet**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Uppdatera kunskaper för artiklar, serviceartiklar eller serviceartikelgrupper
Om du vill ändra de kvalifikationskoder som har tilldelats till artiklar, till exempel från **PC** till **PCS**, gör du det för en artikel, serviceartikel eller för alla artiklar i en serviceartikelgrupp.  
  
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Ikonen, ange **artiklar**, **serviceartikel** eller **serviceartikelgrupp** och välj sedan relaterad länk.  
2. Välj enheten som ska uppdateras och välj sedan åtgärd **Resurskvalifikationer**.  
3. På den rad där den kod som ska ändras finns, väljer du önskad kvalifikationskod i fältet **Kvalifikationskod**.  
4.  Om artikeln har associerade serviceartiklar öppnas en dialogruta med två alternativ:  
  
    * Ändra kvalifikationskoderna till det valda värdet: Välj det här alternativet om du vill ersätta den gamla kvalifikationskoden med den nya för alla relaterade serviceartiklar.  
    * Ta bort kvalifikationskoderna eller uppdatera relationen: Välj det här alternativet om du vill ändra endast den här artikelns kvalifikationskod. Kvalifikationskoden för de relaterade serviceartiklarna kommer att omfördelas, vilket innebär att fältet **Tilldelad från** kommer att uppdateras.  
  
## <a name="see-also"></a><a name="see-also"></a>Se även
[Så här tilldelar du resurser](service-how-to-allocate-resources.md)  
[Ställa in arbetstimmar och tjänstetider](service-how-setup-work-service-hours.md)  
[Konfigurera felrapportering](service-how-setup-fault-reporting.md)  
[Skapa koder för standardtjänster](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]

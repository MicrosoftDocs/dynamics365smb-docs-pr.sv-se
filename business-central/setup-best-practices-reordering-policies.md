---
title: Skapa metodtips – partiformningsmetoder | Microsoft Docs
description: Partiformningsmetod-fältet på artikelkort erbjuder fyra olika planeringsmetoder som bestämmer hur de enskilda planeringsparametrarna kommunicerar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setup-best-practices-reordering-policies"></a><a name="setup-best-practices-reordering-policies"></a>Skapa metodtips: partiformningsmetoder

**Partiformningsmetod**-fältet på artikelkort erbjuder fyra olika planeringsmetoder som bestämmer hur de enskilda planeringsparametrarna kommunicerar.  

En grund för bästa metod för val av en partiformningsmetod är artikelns ABC-klassificering. När du använder ABC-klassificeringen för lagerkontroll och leveransplanering, artiklar hanteras enligt tre olika indelningar beroende på deras värden och volym, i förhållande till summan i lager. Volymfördelning av de tre indelningar visas i följande tabell.

|Klass|Procent av totala antalet i lagervolym|Procent av totala antalet i lagervärde|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|L|60-70|10-30|

ABC-klassificeringen anger att insats och pengar kan sparas genom lösare kontroll av artiklar med låg värdevolym, än av artiklar med hög värdevolym. Illustrationen visar vilken partiformningsmetod i [!INCLUDE[prod_short](includes/prod_short.md)] som är bättre lämpade för A-, B- och C-objekt, respektive.

![ABC-klassificering.](media/abc_classification.png "abc_classification")

I följande tabell visas bästa metod för att välja mellan de fyra regler.  

|Inställningsalternativ|Best practice|Kommentar|  
|------------------|-------------------|-------------|  
|**Order**|Använd för a-artiklar.<br /><br /> Använd för tillverka-mot-order-artiklar.<br /><br /> Använd för artiklar på den högsta nivån och för dyra komponenter och halvfabrikat i produktionen.<br /><br /> Använd för artikel som köps, som direktutleveranser och specialorder.<br /><br /> Använd inte, om du inte accepterar automatisk reservation.|A-artiklar, till exempel lädersoffor i ett möbler lager, är högvärderade artiklar med låg, och ojämnt orderomsättning där lagret är oacceptabelt, eller de obligatoriska attributen varierar. Den bästa partiformningsmetoden är därför en som planerar specifikt för varje behov.|  
|**Parti-för-parti**|Använd för B-artiklar.<br /><br /> Använd för komponenter som finns i flera strukturer i produktionen. Detta säkerställer att inköpsorder kombineras för samma leverantör, så bättre pris kan förhandlas.<br /><br /> Använd om du inte vet om vilken partiformningsmetoden som ska väljas.|B-artiklar, till exempel matsalsmöbelstolar, har en regelbunden och relativt hög orderomsättning men innebär också höga lagerhållningskostnader. Den bästa partiformningsmetoden för B-objekt är därför ett som är ekonomisk, genom att sammanföra behov i Beställningscykeln.<br /><br /> 80 procent av artiklar kan använda den här principen.<br /><br /> Kan användas, utan planeringsparametrar.|  
|**Fast orderkvantitet**|Använd för C-artiklar.<br /><br /> Kombinera med beställningspunktparametrar.<br /><br /> Använd för låg-nivå komponenter i produktionen.<br /><br /> Använd inte, om artikeln har reserverats ofta.|C-objekt, till exempel tekoppar, är låg-värde artiklar med hög, och regelbunden orderomsättning. Den bästa partiformningsmetoden för C-objekt är därför ett som garanterar konstant tillgänglighet, genom att alltid hålla sig över en beställningspunkt.<br /><br /> Om användaren reserveras ett antal för något avlägset behov, störs planeringsgrunden. Även om den planerade distributionslagernivån är accepterad av ordermottagaren med hänsyn till beställningspunkten, kan det hända att antalet inte är tillgängligt på grund av reservation.|  
|**Maximalt antal**|Använd för C-objekt med höga lagerhållningskostnader eller lagringsbegränsningar.<br /><br /> Kombinera tillsammans med en eller flera orderändringar (lägsta/max partistorlek eller Partistorleksmultipel).|C-objekt, till exempel tekoppar, är låg-värde artiklar med hög, och regelbunden orderomsättning. Den bästa partiformningsmetoden för C-objekt är därför ett som garanterar konstant tillgänglighet, genom att alltid hålla sig över en beställningspunkt, men under en maximal lagerkvantitet.<br /><br /> Om du vill ändra den föreslagna order, kan du behöva minska partistorleken till en angiven maximal partistorlek, öka till en angiven minimal partistorlek eller avrundad uppåt för att uppfylla en viss partistorleksmultipel. **Obs!** Lagret stannar då mellan beställningspunkt och högsta antal, om använd med en beställningspunkt.|  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/replenish-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se även

 [Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
 [Designdetaljer: Hantera partiformningsmetoder](design-details-handling-reordering-policies.md)  
 [Skapa komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

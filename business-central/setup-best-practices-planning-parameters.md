---
title: "Lägga upp bästa praxis - Planeringsparametrar | Microsoft Docs"
description: "Snabbfliken **Planering** på artikelkortet är mitten av ett företags försörjningskedja. Det är mycket viktigt att ställa in rätt planeringsparametrar för kostnadseffektiv lagerkontroll och hög kundservicenivå."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6054136dc0722be673b5a7593a371cbec2948e6c
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-planning-parameters"></a>Skapa metodtips: planeringsparametrar
Snabbfliken **Planering** på artikelkortet är mitten av ett företags försörjningskedja. Det är mycket viktigt att ställa in rätt planeringsparametrar för kostnadseffektiv lagerkontroll och hög kundservicenivå.  

 I tabellen nedan finns best practice för hur du lägger upp valda planeringsparameterfält. Välj länken i kolumnen **Inställningsfält** om du vill ha mer information om ett fält.  

|Inställningsfält|Best practice|Kommentar|  
|-----------------|-------------------|-------------|  
|Partiformningsmetod||Mer information finns i [Skapa metodtips: partiformningsmetoder](setup-best-practices-reordering-policies.md).|  
|Reservera|Välj **aldrig**, när artikeln planeras med hjälp av en beställningspunkt.<br /><br /> I tillverkning, välj **aldrig** för att låta planeringssystemet omfatta alla kunderna.<br /><br /> Välj **Valfri** för de artiklar som du kan vilja reservera för kunder som har högsta priorit.<br /><br /> Välj **alltid** för icke-unika artiklar, till exempel artiklar av typen diverse som är ankommande för specifika behov.|Reservationer motverkar i allmänhet syftet med planering, som är att balansera tillgång och efterfrågan. Därför bör artiklar som har upprättats för planering, generellt sett inte reservers.<br /><br /> Om användaren reserverar en lagerkvantitet för framtida behov, störs fönstret planeringsgrund, och beställningspunkten kan inte användas på rätt sätt. Även om den planerade distributionslagernivån är accepterad av ordermottagaren med hänsyn till beställningspunkten, kan det hända att antalet inte är tillgängligt på grund av reservation.|  
|Max. utjämningsperiod|Ange med hänsyn till leverantörens flexibilitet.|Om leverantören accepterar sista-minutenändringar i order, använd en längre period. Om leverantören kräver fast planering, förkorta din period så mycket som möjligt.<br /><br /> Information om globala inställningar finns i [Detaljer: planeringsparametrar](design-details-planning-parameters.md).|  
|Max. avvikelsekvantitet||Information om globala inställningar finns i [Detaljer: planeringsparametrar](design-details-planning-parameters.md).|  
|Ta med lager|Välj alltid när du använder partiformningsmetoden parti-för-parti.|Välj inte endast i vissa situationer, t.ex, när lagerartiklar inte är säljbara.|  
|Säkerhetsledtid|Ställ in mellan 1D och 6D.<br /><br /> Ange en säkerhetsledtid på minst en dag för att se till att leveransen är tillgänglig dagen innan de behövs.<br /><br /> Definiera en längre tid, till dess att deras leveransprestanda är känd, om du använder en ny leverantör.<br /><br /> Definiera längre säkerhetsledtider för kritiska komponenter i produktionen.|Leverans som planeras i systemet för att undvika att varan tar slut i lager kommer på samma dag som varan tar slut. Det kan vara flera timmar för sent, om till exempel, leveransen behövs på morgonen, och den tas emot på eftermiddagen. **Obs!** Fältet **Säkerhetsledtid** använder baskalendern. Därför är 14D inte nödvändigtvis två veckor.|  
|Säkerhetslager|Använda för artiklar med större skillnader i efterfrågan.<br /><br /> Använd för kritiska komponenter i produktionen.<br /><br /> Använda för artiklar, som ingår i serviceavtal.|Om fältet **Beställningspunkt** inte fylls, fungerar säkerhetslagret också som en beställningspunkt.|  
|Partiackumuleringsperiod|Om du endast vill ha få stora order, och du accepterar att ha lager, anger du en lång partiackumuleringsperiod.<br /><br /> Om du vill ha flera små order och minimalt lager, anger du en kort partiackumuleringsperiod.|I allmänhet är partiackumuleringsperioden den längsta period som du ska har lagret.|  
|Beställningspunkt|Basera beställningspunkten på artikelns efterfrågeprofil.|Om historiskt data visar att artikelns genomsnittsbehov är 100 enheter under en ledtid på sju dagar, kan beställningspunkten ställas in till 100 som ett minimum.<br /><br /> Det innebär att när lagernivån sjunker under 100 enheter kommer planeringssystemet föreslå att fylla på, eftersom det tar sju dagar för att leverera artikeln och det måste finnas tillräckligt för att täcka behovet under sju dagar.|  
|Tidsenhet|Lämna fältet tomt, vilket innebär att lagernivån kontrolleras varje dag.|När du styr lagernivån varje dag säkerställer du optimal beställningspunktplanering. **Obs!** En tidsenhet på 1v innebär att lagernivån kan vara under beställningspunkten i en vecka, innan en leveransorder föreslås.|  
|Avrundning|I kostsam produktion ange till 0,00001.|Stora avrundningskvantiteter av kassationsartiklar, eller materialförbrukning kan uppgå till mycket stor lagerkostnader. Den kan därför vara nödvändigt att ange den minsta avrundningsprecisionen för att minska den potentiella kostnad.|  

> [!NOTE]  
>  De bästa praxisna för planeringsparametrarna på artikelkort kan också tillämpas på samma fält på lagerställeenhetskort.  
>   
>  Om företag planerar för behov på olika lagerställen, rekommenderas det att att definiera lagerställeenheter för varje lagerställe och att alla behov skapas, med hjälp av ett värde i fältet **Lagerställekod** . Mer information finns i [Designdetaljer: Efterfrågan vid tomt lagerställe](design-details-demand-at-blank-location.md).  

## <a name="see-also"></a>Se även  
 [Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)   
 [Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
 [Skapa komplexa moduler med hjälp av bästa praxis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


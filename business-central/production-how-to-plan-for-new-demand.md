---
title: Så här kan du planera per order | Microsoft Docs
description: Den här planeringsuppgiften kan utföras på sidan **Orderplanering** där du kan se alla nya behov samt tillgänglighetsinformation och förslag om leverans. Du ser allt du behöver veta och har tillgång till alla verktyg du behöver för att effektivt kunna planera hur du ska möta behov från försäljningsrader och komponentrader och direkt skapa olika typer av leveransorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: aa0d9039ff48d05e0a96ceb5480b40cde864499c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883220"
---
# <a name="plan-for-new-demand-order-by-order"></a>Planera ny behovsorder efter order
Den här planeringsuppgiften kan utföras på sidan **Orderplanering** där du kan se alla nya behov samt tillgänglighetsinformation och förslag om leverans. Du ser allt du behöver veta och har tillgång till alla verktyg du behöver för att effektivt kunna planera hur du ska möta behov från försäljningsrader och komponentrader och direkt skapa olika typer av leveransorder.  

Du kan gå till sidan **Orderplanering** på två sätt beroende på vad ditt fokus: från en order som du vill planera för särskilt eller i batch-läge när du vill planera för alla och nya behov.  


## <a name="to-plan-for-new-production-order-demand"></a>Så här planerar du för ett nytt produktionsorderbehov  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Planerade produktionsorder** och välj sedan relaterad länk. (Du kan utföra dessa steg för en planerad, fast planerad eller släppt produktionsorder).
2.  Öppna produktionsordern som du vill planera för och välj sedan åtgärden **Planering**.  
3.  På sidan **Orderplanering** väljer du åtgärden **Skapa inköpsförslag**.  

Sidan visar planeringsrader enligt visningsfiltret **Produktionsbehov**, dvs komponentrader med ouppfyllda behov från alla befintliga produktionsorder. Behov för endast en produktionsorder visas inte eftersom det är nödvändigt att planera för en produktionsorder med en översikt över behoven för möjliga tidigare komponentrader. Planeringsraderna för produktionsorder som du öppnade fönstret från expanderas.  

## <a name="to-plan-for-any-new-demand"></a>Så här planerar du för valfritt nytt behov  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Orderplanering** och välj sedan relaterad länk.  
2.  På sidan **Orderplanering** väljer du åtgärden **Skapa inköpsförslag**.
3.  Välj knappen **Expandera (+)** framför datumet i fältet **Behövd datum** om du vill se de underliggande planeringsraderna som motsvarar behovsrader med otillräcklig tillgänglighet.  
4.  Du kan se värden för varje expanderad planeringsrad (behovsrad) i informationsfält längst ned på sidan.  

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Antal på andra lagerställen**|Visar om artikeln finns på ett annat lagerställe. I så fall kan du söka efter den och markera den.|  
    |**Ersättningar finns**|Visar om en ersättningsartikel har skapats för artikeln. I så fall kan du söka efter den och markera den. Observera att den här funktionen bara kan användas för komponenter, dvs från behovsrader av typen **Produktion**.|  
    |**Disponibelt antal**|Visar den totala tillgängligheten för artikeln (Lagerutveckling över tiden).|  
    |**Tidigast disponibelt den**|Visar införseldatum för en inkommande leveransorder som kan täcka behovskvantiteten, men på ett datum som är senare än behovsdatumet.|  

5.  I fältet **Återanskaffningssystem** väljer du vilken typ av leveransorder som ska skapas.  

    Standardvärdet är värdet på artikelkortet (eller kortet för lagerställeenhet), men du kan ändra det till något av följande tre alternativ:  

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Inköp**|Skapar en inköpsorder.|  
    |**Överföring**|Skapar en överföringsorder.|  
    |**Prod.order**|Skapar en produktionsorder.|  

    I fönstret **Leverera från** måste du välja ett värde enligt det återanskaffningssystem som du har markerat.  

    > [!NOTE]  
    >  Om fältet inte fylls i visas ett felmeddelande när du använder funktionen **Skapa leveransorder**, och ingen leveransorder skapas för den aktuella planeringsraden. Detta gäller inte om återanskaffningssystemet är **Prod.order**.  

6.  I fältet **Leverera från** kan du söka i lämplig lista och välja varifrån leveransen ska ske:  

    - Om återanskaffningssystemet är **Inköp** görs sökningen med sökknappen på sidan **Artikelleverantörskatalog**.  
    - Om återanskaffningssystemet är **Överföring** görs sökningen med sökknappen på sidan **Lagerställelista**.  

    Om artikeln finns på ett annat lagerställe visas ett värde i fältet **Antal på andra lagerställen** längst ned, och du kan då söka efter och markera det lagerställe som artikeln ska levereras från när du skapar överföringsordern.  

    Om det finns en ersättningsartikel för artikeln som behövs visas värdet **Ja** i fältet **Ersättningar finns**, och du kan då söka på sidan **Artikelersättningstrans.** och markera ersättningsartikeln.  

7.  Markera kryssrutan **Reservera** om du vill skapa en reservation mellan leveransordern som du skapar och den behovsrad som den skapas för. Som standard är fältet tomt.  

    > [!NOTE]  
    >  Du kan bara markera den här kryssrutan om artikeln har **Valfri** eller **Alltid** i fältet **Reservera** på artikelkortet för artikeln.  

8.  I fältet **Kvant. mot order** kan du ange den kvantitet som ska anges på leveransordern som du skapar.   
    Standardvärdet är samma kvantitet som i fältet **Behövt antal**. Men du kan ange ett högre eller lägre värde utifrån din kunskap om behovssituationen. Om du till exempel, ser du på sidan **Orderplanering** att flera ej relaterade behovsrader är för samma inköpta artikel, och, dessa är kring samma datum, kan du kan konsolidera dessa genom att ange den totala behovskvantiteten i fältet **Antal i order** på en rad och sedan ta bort andra, föråldrade planeringsrader för artikeln.  

9.  I fälten **Förfallodatum** och **Orderdatum** kan du ange de datum som ska gälla för de leveransorder som skapas.  

    De här två fälten är beroende av varandra i enlighet med värdet i fältet **Standard säkerhetsledtid** som finns på sidan **Produktionsinställningar**. Som standard är värdet för Förfallodatum detsamma som för Behovsdatum, men du kan ändra detta om du vill.  

> [!NOTE]  
>   Om du anger ett senare datum än behovsdatumet får du ett varningsmeddelande.  

## <a name="to-make-supply-orders"></a>Så här skapar du leveransorder  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Planerade produktionsorder** och välj sedan relaterad länk. Du kan utföra dessa steg för en planerad, fast planerad eller släppt produktionsorder.  
2.  Öppna produktionsordern som du vill planera för och välj sedan åtgärden **Planering**.  
3.  Placera markören på en planeringsrad och klicka på åtgärder **Skapa order**.  
4.  På sidan **Skapa leveransorder** på snabbfliken **Orderplanering** , i fältet **Skapa order för**, markera ett av följande alternativ.  

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**den aktiva raden**|Skapa en leveransorder för den rad där markören finns.|  
    |**den aktiva ordern**|Skapa en leveransorder för alla rader i ordern där markören finns.|  
    |**Alla rader**|Skapa leveransorder för alla rader på sidan **Orderplanering**.|  

5.  På snabbfliken **Alternativ** anger du vilken typ av leveransorder, eller inköpsförslagsrader, som ska skapas.  

    > [!NOTE]  
    >  De inställningar som du gör på sidan **Skapa leveransorder** sparas under ditt användar-ID, och de visas igen nästa gång du öppnar sidan.  

6.  Klicka på **OK** när du vill skapa angivna leveransorder eller inköpskalkylarksrader.  

Nu har du planerat för de ouppfyllda behoven genom att skapa motsvarande leveransorder. Exakt hur du ska arbeta med sidan **Orderplanering** beror på vad som gäller i just ditt företag.  

När du är klar med planeringen på sidan **Orderplanering**, och du till exempel har angett ett alternativt sätt att leverera kvantiteten, kan du fortsätta med att skapa leveransorder för en eller flera av planeringsraderna.  

> [!NOTE]  
>  De leveransorder som du skapar kan innebära att nya beroende behov uppstår, till exempel behov av underliggande produktionsorder, och därför bör du klicka på **Skapa inköpsförslag** igen för att identifiera dessa behov och hantera dem innan du går vidare i listan.  

## <a name="see-also"></a>Se även  
[Planerad](production-planning.md)  
[Ställa in Produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagersaldo](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Leveransplanering](design-details-supply-planning.md)   
[Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

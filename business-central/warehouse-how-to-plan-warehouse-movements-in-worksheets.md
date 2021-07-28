---
title: 'Så här: Planera lagertransporter i kalkylark | Microsoft Docs'
description: Planera transporter i kalkylarket med hjälp av Återanskaffningsfunktionen eller manuellt planera de rader som du vill skapa som transportinstruktioner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e779bb1d2916c031dea66a52ed7b3b9ccc006aee
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438163"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Planera lagertransporter i kalkylark
Planera transporter i kalkylarket med hjälp av Återanskaffningsfunktionen eller manuellt planera de rader som du vill skapa som transportinstruktioner.  

## <a name="to-calculate-a-replenishment-movement"></a>Så här beräknar du återanskaffningstransporter:  
Allt eftersom artiklarna i distributionslagret levereras till kunderna innehåller lagerställen med högst lagerplatsordning allt färre artiklar. Om du vill fylla på plocklagerställena med högst lagerplatsordning med artiklar från andra lagerställen kan du köra funktionen **Beräkna lagerplatsåteranskaffning** på sidan **Transportkalkylark**

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transportkalkylark** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Beräkna lagerplatsåteranskaffning**.  

    [!INCLUDE[prod_short](includes/prod_short.md)] skapar rader som anger exakt hur du ska flytta artiklar från lagerställen med låg lagerplatsordning till lagerställen med högre lagerplatsordning.  

    > [!NOTE]  
    >  Föreslår en transport enligt FEFO när du aktiverar **Skapa transport** operationen, om följande villkor är uppfyllda för en artikel:  
    >   
    >  -   artikeln har ett utgångsdatum,  
    > -   Fältet **Plocka enligt FEFO** på lagerställekortet är markerat och  
    > -   På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.  
    > -   fälten **Från zon** och **Från lagerplats** innehåller inga värden.  

    Mer information finns i [Plocka enligt FEFO](warehouse-picking-by-fefo.md).  

3.  Titta igenom raderna och ändra dem vid behov, eller ta bort vissa av raderna om du inte har tillräckligt med tid att utföra alla.  
4.  Välj åtgärden **Skapa transport** för att skapa en distributionslagerinstruktion till lagerpersonalen.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Du kan flytta hela innehållet i en eller flera lagerställen med funktionen Hämta lagerställesinnehåll:  
Du kan även använda Transportkalkylark för att planera andra lagertransporter inom distributionslagret. När du till exempel vill placera artiklar på en lagerplats för kvalitetskontroll kan du använda transportförslaget för att planera den åtgärden och sedan skapa en transportinstruktion för en anställd.  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Transportkalkylark** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Hämta lagerställesinnehåll**. Använd sidan för begäran för att filtrera vilka lagerställen och artiklar som ska visas på transportförslagets rader.  
3.  Fyll i de relevanta fälten på sidan för begäran av batch-jobb. Om du till exempel vill visa lagerställesinnehållet för alla lagerställen i en viss zon på lagerstället fyller du i fältet **Zonkod**. Om du vill hämta rader för alla lagerställen som innehåller en viss artikel fyller du i fältet **Artikelnr**.  

    > [!NOTE]  
    >  Du kan inte manuellt flytta artiklar in och ut ur en lagerplats av typen RECEIVE. Detta beror på att artiklar som finns i en lagerplats av RECEIVE-typ måste registreras som införda innan de blir en del av det tillgängliga lagret.  

4.  Om du hämtar många rader väljer du **Sortera** för att välja en sorteringsmetod som du kan använda för att bestämma den ordning som raderna ska visas med i kalkylarket och klickar sedan på **OK**.  

    > [!NOTE]  
    >  Förflyttningsrader hämtas enligt FEFO när du aktiverar **Hämta lagerställesinnehåll** operationen, om följande villkor är uppfyllda för en artikel:  
    >   
    >  -   artikeln har ett utgångsdatum,  
    > -   Fältet **Plocka enligt FEFO** på lagerställekortet är markerat och  
    > -   På lagerställekortet måste kryssrutan **Lagerplats ska finnas** vara markerad.  
    > -   fälten **Från zon** och **Från lagerplats** innehåller inga värden.  

5.  Fyll i en del av de hämtade raderna för att spegla de ändringar som du vill utföra. För varje artikel som du vill flytta måste du fylla i fälten **Artikelnr**, **Från lagerställeskod**, **Till lagerställeskod** och **Antal**.  
6.  Ta bort ofullständiga rader som du bara använde i informationssyfte.  
7.  När raderna i transportkalkylarket korrekt speglar hur transporten ska utföras av lagerpersonalen klickar du på åtgärden **Skapa transport** för att skapa instruktionerna för personalen.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
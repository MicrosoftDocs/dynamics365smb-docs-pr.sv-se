---
title: Använda automatiskt datainsamlingssystem (ADCS) | Microsoft Docs
description: Du kan använda det automatiska datainsamlingssystemet (ADCS eller Automatiskt datainsamlingssystem) för att registrera förflyttningen av alla artiklar i distributionslagret och för att registrera några journalaktiviteter, däribland kvantitetsjusteringar i artikeljournalen för distributionslagret, inventeringsjournalen och fysisk inventering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 71433b584ea02e4561a2e9e391d3ee92c5284488
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788239"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Använda ADCS (Automatiskt datainsamlingssystems)

> [!NOTE]
> Med hjälp av ADCS-lösningen (Automated Data Capture System) ger en väg [!INCLUDE[prod_short](includes/prod_short.md)] kan du kommunicera med handburna enheter via webbtjänster. Du måste arbeta med en Microsoft-partner som kan tillhandahålla länken mellan webbtjänsten och den specifika handhållen enheten. 

Du kan använda det automatiska datainsamlingssystemet (ADCS eller Automatiskt datainsamlingssystem) för att registrera förflyttningen av alla artiklar i distributionslagret och för att registrera några journalaktiviteter, däribland kvantitetsjusteringar i artikeljournalen för distributionslagret, inventeringsjournalen och fysisk inventering. ADCS inbegriper vanligen streckkod.

Om du ska använda ADCS måste du ge varje artikel i distributionslagret en artikelidentifierare. Du måste även lägga upp miniformulär, handdatorfunktioner, datautbyten och specificeras inställningar för fältet som kontrollerar ADCS. Du anger om du ska använda ADCS på lagerställekortet för ett lager.

Baserat på behovsnivån i lagret definierar du den mängd information som ska visas i miniformulärinställningarna för den aktuella handenheten. Följande är exempel information som du kan visa:  

- Data från tabeller i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en lista över plockningsdokument som användaren kan välja från.  
- Textinformation.  
- Meddelanden som innehåller bekräftelser eller fel om aktiviteter som utförts och registrerats av handenheter användaren.

## <a name="to-enable-web-services-for-adcs"></a>Så här aktiverar du webbtjänster för ADCS
Om du vill använda det automatiska datainsamlingssystemet måste du aktivera ADCS-webbtjänst.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>För att aktivera och publicera ADCS-webbtjänsten  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Webbtjänster** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.  
3. På sidan **webbtjänster** anger du följande information på en ny rad:  

    |Fält|Värde|  
    |---------------------------------|-----------|  
    |**Objekttyp**|Kodmodul|  
    |**Objekt-ID**|7714|  
    |**Tjänstnamn**|ADCS **viktigt:** du måste namnge tjänsten **ADCS**.|  

5. Markera kryssrutan **Publicerat**.  
6. Välj **OK**.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Så här konfigurerar ett lager att använda ADCS  
Om du ska använda ADCS måste du ange vilka distributionslagerställen som använder teknologin.  

> [!NOTE]  
>  Vi rekommenderar att du inte ställer in ett distributionslager som ska använda ADCS, om distributionslagret dessutom har en lagerplats kapacitetsprincip.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Platser** och välj sedan relaterad länk.
2.  Välj ett lager i listan som du vill aktivera för ADCS och välj **redigera**.
3. På sidan **lagerställekort** markerar du kryssrutan **använda ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Ange ett objekt för att använda ADCS  
Varje distributionslagerartiklar som ska användas med ADCS, måste tilldelas en identitetskod för att koppla den till dess artikelnummer. Du kan t.ex använda artikelns Streckkod som identitetskoden. En artikel kan också använda flera identitetskoder. Det kan vara praktisk i de fall där en artikel är disponibel i olika måttenheter, t.ex stycken och pallar. Tilldela varje en identitetskod, i det här fallet.    

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.  
2.  Markera ett objekt i listan som ingår i ADCS-lösningen och välj åtgärden **redigera**.
3. På sidan **Artikelkort** väljer du åtgärden **Identifierare**.
4. PÅ sidan **Artikelidentifierare** väljer du åtgärden **Ny**.
5. I fältet **Kod** ange identifierare för artikeln. Du kan t.ex använda artikelns Streckkod som identitetskoden.  

    Du kan även definiera ett **Variantkod** och en **Enhet** kod.  

6. Ange flera koder för varje artikel, om det behövs.
7. Välj knappen **OK**.  
8.  För att granska informationen väljer du fältet **identitetskod** för att öppna sidan **Artikelidentifierare**.

## <a name="to-add-an-adcs-user"></a>Om du vill lägga till en ADCS-användare  
Du kan lägga till användare som en användare av ett ADCS (Automatiskt datainsamlingssystem). När du gör det, måste du även ange ett lösenord. Om du vill kan du även ange en koppling som identifierar ADCS-användaren som distributionslageranvändare. ADCS-användarlösenord kan vara olika från Windows-inloggningslösenord för användaren. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **ADCS-användare** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3.  Ange ett **Namn** på användaren. Namnet kan inte innehålla fler än 20 tecken, inklusive blanksteg.  
4.  Ange ett **Lösenord** i fältet. Lösenord maskeras.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Om du vill ange att lagerpersonalen är en ADCS-användare  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Distributionslagerpersonal** och välj sedan relaterad länk.  
2.  Lägga till en ny lagerpersonalen, om det behövs. Mer information finns i [Så här skapar du dist.lager personal](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Välj åtgärden **Redigera lista**.  
4.  Välj en lagerpersonal i listan. I fältet **ADCS-användare** väljer du listpilen och sedan namnet på en ADCS-användare i listan.  

> [!NOTE]  
>  Standarddistributionslagret för den anställde ska vara en som använder ADCS.

## <a name="to-create-and-customize-miniforms"></a>Så här: Skapa och anpassa Miniformulär
Du använder miniformulär som beskriver den information som du vill presentera på en handenheter. Du kan till exempel skapa miniformulär för att hantera lageraktiviteten att plocka artiklar. När du har skapat en miniformulär, kan du lägga till funktioner för den vanliga åtgärder för en användare med handenheter, till exempel flytta uppåt eller en rad.  

> [!NOTE] 
> För att använda eller ändra funktionen i en miniformulärfunktion måste du skapa en ny kodmodul för fältet **Hantera codeunit** för att utföra lämplig åtgärd eller svar. Du kan lära dig mer om ADCS-funktioner genom att undersöka codeunit, till exempel 7705, 7706, 7712 och 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Så här skapar du en miniformulär för ADCS  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Miniformulär** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3.  I fältet **Kod** anger du en kod på Miniformuläret. Ange värden i alla övriga fält, om du vill.  

    Välj **Starta miniformulär** kryssrutan för att ange att miniformuläret är det första formulär som användaren ser i logga in.  

4.  Definiera fälten som visas på miniformuläret på **Rader** Snabbfliken. Ordningen där du anger rader, är den ordning som raderna ska visas på handenheten.  

När du har skapat en miniformulär, nästa steg är att skapa operationer och att koppla funktioner för olika tangentbord indata.  

### <a name="to-customize-miniform-functions"></a>Om du vill anpassa miniformulärfunktioner  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Miniformulär** och välj sedan relaterad länk.  
2.  Välj ett miniformulär från listan, välj åtgärden **Redigera**.  
3.  Välj åtgärden **Funktioner**.  
4.  I listrutan **Funktionskod** väljer du en kod för att representera en funktion som du vill koppla till miniformuläret. Du kan till exempel välja ESC, som associerar funktionen med att trycka på ESC-tangenten.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
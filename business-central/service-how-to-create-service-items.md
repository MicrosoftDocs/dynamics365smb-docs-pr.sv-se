---
title: Så här skapar du Serviceartiklar | Microsoft Docs
description: När du tar emot en ej registrerad artikel för service kan du registrera den som serviceartikel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5f7a95b297ef494cc3607f4550b6a0e58b18839d
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992175"
---
# <a name="create-service-items"></a>Skapa tjänsteartiklar
I [!INCLUDE[d365fin](includes/d365fin_md.md)] avser termen ”serviceartikel” den utrustning eller de artiklar som kräver service. När du skapar en serviceorder kan du ange de artiklar som behöver service. I ordern kan du länka en serviceartikel till en artikel i lagret eller en serviceartikelgrupp.    

När du tar emot en artikel för service kan du registrera den som serviceartikel. Detta kan göras på olika sätt. Du kan till exempel skapa en serviceartikel på sidan **serviceartiklar** eller som en del av en annan process, som t.ex. när du arbetar med en serviceorder.   

## <a name="to-create-a-service-item"></a>Så här skapar du en serviceartikel  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceartiklar** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Så här skapar du serviceartiklar inom serviceorder  
När du tar emot artiklar som du vill registrera som serviceartiklar kan du skapa dem som serviceartiklar på sidan **Serviceorder** eller **Serviceoffert**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Tjänsteorder** och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Välj åtgärden **Skapa serviceartikel**.  

    Ett nummer tilldelas serviceartikeln, och ett serviceartikelkort skapas. I fältet **Serviceartikelnr** fylls numret på den nya serviceartikeln i.

## <a name="to-create-a-service-item-when-shipping-items"></a>Så här skapar du en serviceartikel vid artikelutleverans  
När du levererar artiklar genom att bokföra antingen försäljningsorder eller försäljningsfakturor registreras de levererade artiklarna automatiskt som serviceartiklar om följande villkor uppfylls. Artiklarna måste höra till en serviceartikelgrupp och ha kryssrutan **Skapa serviceartikel** markerad. Om artiklarnas serienummer har registrerats på sidan Artikelspårningsrader kopieras informationen automatiskt till fältet **Serienr** på serviceartikelkortet när serviceartiklar skapas.  

Nedan förklaras hur du skapar serviceartiklar när du levererar artiklar på försäljningsorder.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Öppna den aktuella försäljningsordern.  
3. Välj åtgärden **Bokför** eller **Bokför och skriv ut**.  
4. Välj åtgärden **leverera** eller **leverera och fakturera**.  
5. Serviceartiklarna skapas automatiskt för artiklarna på ordern, förutsatt att de tillhör en serviceartikelgrupp som har definierats för att skapa serviceartiklar. Om du har registrerat serienummer på sidan **Artikelspårningsrader** kommer de att tilldelas till motsvarande serviceartiklar.  

> [!NOTE]  
>  Om en artikel är en struktur och du har expanderat strukturen behandlas de expanderade strukturartiklarna på samma sätt som vanliga artiklar. Serviceartiklar skapas utifrån serviceartikelgruppens villkor, och om du vill, serienumrens villkor. Dessutom är det så att om en serviceartikel skapas för en expanderad struktur som består av andra strukturkomponenter, skapas de här artiklarna som serviceartikelkomponenter för den expanderade strukturserviceartikeln.  
>   
>  Om en artikel är en struktur och du inte har expanderat strukturen skapas en serviceartikel för den utifrån serviceartikelgruppens villkor, och om du så vill, serienumrens villkor.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Så här infogar du uppstartskostnader för en serviceartikel
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **tjänsteuppgifter** och välj sedan relaterad länk.
2. Välj åtgärden **Artikelkalkylark**.
3. Välj serviceraden och välj sedan **Åtgärder**, **Funktioner** och sedan åtgärden **Infoga uppstartskostnad**.  

    En servicerad av typen **Kostnad** infogas automatiskt med uppstartskostnaden. Uppstartskostnaden gäller vald serviceartikel.

## <a name="see-also"></a>Se även  
[Ställa in tjänsteartiklar och tjänsteartikelkomponenter](service-how-setup-service-items.md)  
[Ställa in tjänstehantering](service-setup-service.md)  
[Servicehantering](service-service.md)  

---
title: "Så här skapar du Lagerplatser | Microsoft Docs"
description: "Det effektivaste sättet att skapa lagerplatserna i distributionslagret på är att generera grupper med liknande lagerplatser i lagerplatsuppläggningsförslaget, men du kan även skapa en lagerplats i taget genom att följa anvisningarna nedan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f8cd19f97c530397dd6b499157e13340331aa3ba
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="create-bins"></a>Skapa lagerplatser
Det effektivaste sättet att skapa lagerplatserna i distributionslagret på är att generera grupper med liknande lagerplatser i lagerplatsuppläggningsförslaget, men du kan även skapa en lagerplats i taget från lagerställekortet. Du kan också använda en funktion i fönstret **Lagerplatsuppläggning förslag** för att skapa lagerplatserna automatiskt.  

## <a name="to-create-a-bin-from-the-location-card"></a>Så här skapar du en lagerplats från lagerställekortet:  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.  
2.  Markera lagerstället som du vill skapa en lagerplats från och välj åtgärden **Lagerplatser**  
3. Välj åtgärden **Ny**.
4. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Så här skapar du enstaka lagerplatser i Lagerplatsuppläggning förslag:  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerplatsuppläggning förslag** och välj sedan relaterad länk.  
2.  På varje rad fyller du i de fält som är nödvändiga för att namnge och ange egenskaper för de lagerplatser som du skapar.  
3.  Välj åtgärden **Skapa lagerplatser**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Så här skapar du lagerplatser automatiskt i lagerplatsuppläggningsförslaget:  
Innan du börjar skapa lagerplatser automatiskt i förslaget bör du bestämma vilken typ av lagerplatser som är viktiga för driften samt vilket artikelflöde som är mest praktiskt i den fysiska strukturen i distributionslagret.  

> [!NOTE]  
>  När du använder en lagerplats inte kan du ta bort den om den inte är tom. Om du vill använda ett annat namngivningssystem för lagerplatser kan du dock använda grupperingsjournalen för att flytta artiklarna till ett nytt lagerplatssystem. Det här måste göras manuellt och är tidskrävande, så det är bättre att skapa lagerplatserna rätt från början.  

Om du vill arbeta i fönstret **Lagerplatsuppläggning förslag** måste du ställas in som en lageranställd på det lagerställe där lagerplatserna finns. Mer information finns i [Så här skapar du dist.lager personal](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerplatsuppläggning förslag** och välj sedan relaterad länk.  
2.  Välj åtgärden **Beräkna lagerplatser**.
3. Klicka på **Beräkna lagerplatser** i fältet **Lagerplatsmall kod** och välj den lagerplatsmall som du vill använda som modell när du skapar lagerplatser.
4.  Fyll i en beskrivning av de lagerplatser som du håller på att skapa.  
5.  Om du vill skapa lagerplatskoderna, fyller du i **från nr** och **Till nr.** I de tre kategorierna som visas i fönstret: **ställning**, **sektion**, och **nivå.** Lagerplatskoden kan bestå av högst 20 tecken.  

    > [!NOTE]  
    >  Det antal tecken som du har angett i de tre kategorierna för något av fälten (t.ex. de tecken som du har angett i de tre fälten **Från nr**) plus eventuella fältavgränsare, får högst vara 20.  

     Du kan använda bokstäver i koden som en kombination för identifiering, men den bokstav som du använder måste vara samma i fältet **Från nr.** och **Till nr.** . Till exempel kanske du anger ställningsdelen av koden som **Från nr. A01** och **Till nr. A10**. Programmet genererar inte koder i bokstavsordning, till exempel från A01 till F05.  

6.  Om du vill att ett tecken, t.ex. ett bindestreck, ska avgränsa de kategorifält som du har definierat som en del av lagerplatskoden, fyller du i fältet **Fältseparator** med det tecknet.  
7.  Om du inte vill att en rad ska skapas för en lagerplats om den redan finns, markerar du fältet **Kontrollera existerande lagerplats**.  
8. När du är klar med att fylla i fälten klickar du på knappen **OK**.

    En rad skapas för respektive lagerplats i förslaget. Nu kan du ta bort några av lagerplatserna, till exempel om du har en ställning med en gång genom de två första nivåerna i ett par sektioner.  

9. När du har tagit bort alla onödiga lagerplatser väljer du åtgärden **Skapa lagerplatser** så skapas lagerplatser för varje rad i förslaget.  

Upprepa processen för ytterligare en uppsättning lagerplatser tills du har skapat alla de lagerplatser som du ska ha i distributionslagret.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


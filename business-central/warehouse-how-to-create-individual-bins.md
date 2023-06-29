---
title: Skapa lagerställen
description: 'Generera grupper med liknande lagerplatser i lagerplatsuppläggningskalkylarket, skapa lagerplatser individuellt på lagerställekortet eller automatiskt i lagerplatsuppläggningskalkylarket.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="create-bins"></a><a name="create-bins"></a>Skapa lagerställen

Det effektivaste sättet att skapa lagerställena i distributionslagret på är att generera grupper med liknande lagerställen i lagerplatsuppläggningskalkylarket, men du kan även skapa en lagerplats i taget från lagerställekortet. Du kan också använda en funktion på sidan **Lagerplatsuppläggningskalkylark** för att skapa lagerställena automatiskt.  

## <a name="to-create-a-bin-from-the-location-card"></a><a name="to-create-a-bin-from-the-location-card"></a>Så här skapar du en lagerplats från lagerställekortet:

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **placeringar** och väljer sedan relaterad länk.  
2.  Markera lagerstället som du vill skapa en lagerplats från och välj åtgärden **Lagerställen**  
3. Välj åtgärden **Ny**.
4. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a><a name="the-dedicated-field"></a>Fältet Dedikerad

Fältet **Dedikerad** på sidan **Lagerplatser** anger att kvantiteterna på lagerplatsen är skyddade från att plockas för andra behov. Men kvantiteterna i lagerställena kan fortfarande reserveras. Därmed ingår antalet i dedikerade lagerställen i fältet **Totalt disponibelt antal** på sidan **Reservation**.

Att dedikera en lagerplats resulterar i en liknande funktion i grundläggande lagerstyrning att använda lagerplatstyper, som endast finns i avancerade distributionslager. Mer information finns i [Skapa lagerställen](warehouse-how-to-set-up-bin-types.md).

### <a name="example"></a><a name="example"></a>Exempel

En produktionsgrupp med en lagerplatskod i fältet **Till produktion-lagerplats-kod**. Produktionsorderkomponentrader med den här lagerställeskoden kräver att framåtriktade komponenter placeras där. Dock tills komponenterna förbrukas från den lagerplats kan andra komponentbehov väljas eller förbrukas från den lagerstället eftersom de är fortfarande tillgängligt lagerställesinnehåll. Se till att lagerställesinnehållet är bara tillgänglig för det komponentbehov som använder den till produktion-lagerplats genom att välja fältet **Dedikerad** på raden för den lagerställeskoden.

> [!Caution]
> Artiklar på dedikerade lagerställen skyddas inte när de plockas och förbrukas som produktions- eller monteringskomponenter med sidan **Lagerplockning**. Mer information finns i [Plocka för produktion eller montering i grundläggande distributionslagerkonfiguration](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a><a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Så här skapar du enstaka lagerställen i lagerplatsuppläggningskalkylark:

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lagerplatsuppläggningskalkylark** och väljer sedan relaterad länk.  
2.  På varje rad fyller du i de fält som är nödvändiga för att namnge och ange egenskaper för de lagerställen som du skapar.  
3.  Välj åtgärden **Skapa lagerställen**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a><a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Så här skapar du lagerställen automatiskt i lagerplatsuppläggningskalkylarket:

Innan du börjar skapa lagerställen automatiskt i kalkylarket bör du bestämma vilken typ av lagerställen som är viktiga för driften samt vilket artikelflöde som är mest praktiskt i den fysiska strukturen i distributionslagret.  

> [!NOTE]  
> När du använder en lagerplats inte kan du ta bort den om den inte är tom. Om du vill använda ett annat namngivningssystem för lagerställen kan du dock använda grupperingsjournalen för att flytta artiklarna till ett nytt lagerplatssystem. Det här måste göras manuellt och är tidskrävande, så det är bättre att skapa lagerställena rätt från början.  

Om du vill arbeta på sidan **lagerplatsuppläggningskalkylark** måste du ställas in som en lageranställd på det lagerställe där lagerställena finns. Mer information finns i [Så här skapar du dist.lager personal](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lagerplatsuppläggningskalkylark** och väljer sedan relaterad länk.  
2.  Välj åtgärden **Beräkna lagerställen**.
3. Klicka på **Beräkna lagerställen** i fältet **Lagerplatsmall kod** och välj den lagerplatsmall som du vill använda som modell när du skapar lagerställen.
4.  Fyll i en beskrivning av de lagerställen som du håller på att skapa.  
5.  Om du vill skapa lagerställeskoderna, fyller du i **från nr** och **Till nr.** I de tre kategorierna som visas på sidan: **ställning**, **sektion**, och **nivå.** Lagerställeskoden kan bestå av högst 20 tecken.  

    > [!NOTE]  
    >  Det antal tecken som du har angett i de tre kategorierna för något av fälten (t. ex. de tecken som du har angett i de tre fälten **Från nr**) plus eventuella fältavgränsare, får högst vara 20.  

     Du kan använda bokstäver i koden som en kombination för identifiering, men den bokstav som du använder måste vara samma i fältet **Från nr.** och **Till nr.** . Till exempel kanske du anger ställningsdelen av koden som **Från nr. A01** och **Till nr. A10**. Programmet genererar inte koder i bokstavsordning, till exempel från A01 till F05.  

6.  Om du vill att ett tecken, t. ex. ett bindestreck, ska avgränsa de kategorifält som du har definierat som en del av lagerställeskoden, fyller du i fältet **Fältseparator** med det tecknet.  
7.  Om du inte vill att en rad ska skapas för en lagerplats om den redan finns, markerar du fältet **Kontrollera existerande lagerplats**.  
8. När du är klar med att fylla i fälten klickar du på knappen **OK**.

    En rad skapas för respektive lagerplats i kalkylarket. Nu kan du ta bort några av lagerställena, till exempel om du har en ställning med en gång genom de två första nivåerna i ett par sektioner.  

9. När du har tagit bort alla onödiga lagerställen väljer du åtgärden **Skapa lagerställen** så skapas lagerställen för varje rad i kalkylarket.  

Upprepa processen för ytterligare en uppsättning lagerställen tills du har skapat alla de lagerställen som du ska ha i distributionslagret.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-new-bins/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Bryta ned volym med dirigerad artikelinförsel och plockning
description: 'Lär dig hur du aktiverar automatisk uppdelning av bulk med dirigerad artikelinförsel och plockning, samt enhetsbrytning vid i plockningar, artikelinförsel, transporter med mera.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Aktivera automatisk volymnedbrytning med dirigerad artikelinförsel och plockning

För lagerställen, som använder artikelinförsel och plockning, kan [!INCLUDE[prod_short](includes/prod_short.md)] dela upp större enheter till mindre enheter, när du skapar lagerinstruktioner hos källdokument, produktionsorder eller intern plockning och artikelinförsel. Till brytenhet kan även innebära att artiklar samlas in i mindre enheter så att antalet i en större enhet i ett källdokument eller en produktionsorder blir lika.

## <a name="breakbulk-in-picks"></a><a name="breakbulk-in-picks"></a><a name="breakbulk-in-picks"></a>Enhetsbrytning vid plockning

Om du vill lagra artiklar i flera olika måttenheter på en plats och tillåta dem att kombineras automatiskt efter behov vid plockning aktiverar du växlingsknappen på **Tillåt brytenhet** på sidan lagerställekortet. Sedan för att slutföra denna uppgift kommer [!INCLUDE [prod_short](includes/prod_short.md)] att söka efter en artikel i den begärda måttenheten. Om det inte finns något föreslår [!INCLUDE [prod_short](includes/prod_short.md)] att du delar upp en större enhet i den mått enhet som behövs.  

Om endast mindre måttenheter finns föreslår [!INCLUDE [prod_short](includes/prod_short.md)] att du samlar ihop flera artiklar för att komma upp i den kvantitet som begärs på utleverans- eller produktionsordern. Det som sedan sker är att den större måttenheten i ursprungsdokumentet bryts ned i mindre enheter för plockning.  

## <a name="breakbulk-in-put-aways"></a><a name="breakbulk-in-put-aways"></a><a name="breakbulk-in-put-aways"></a>Enhetsbrytning vid artikelinförsel

I distributionslagerinförslar föreslår [!INCLUDE [prod_short](includes/prod_short.md)] åtgärdsrader i den måttenhet som används i artikelinförseln. Det kan t.ex. få förslag på delar trots att de anländer till en annan måttenhet.  

## <a name="breakbulk-in-movements"></a><a name="breakbulk-in-movements"></a><a name="breakbulk-in-movements"></a>Enhetsbrytning vid transport

[!INCLUDE [prod_short](includes/prod_short.md)] kan också brytenhet i påfyllningstransporter om **Tillåt brytenhet** är aktiverat på **Beräkna lagerplatsåteranskaffning**.  

Du kan granska resultaten av enhetskonverteringsprocessen som övergångsrader för enhetsbrytning i instruktionerna för artikelinförsel, plockning eller transport.  

> [!NOTE]  
> Om du väljer fältet **Sätt brytenhetsfilter** i huvudet för instruktionerna för distributionslagret, döljs enhetsbrytningsraderna om det uteslutande är den större måttenheten som ska användas. Exempel: Om en lastpall består av 12 enheter och samtliga enheter kommer att användas, dirigeras du under plockningen att ta en lastpall och placera 12 enheter. Om du bara måste plocka 9 enheter är inte brytningsraderna dolda, även om du har markerat fältet **Brytenhetsfilter**. Raderna är inte dolda eftersom du måste placera de återstående tre enheterna någonstans i distributionslagret.  

> [!NOTE]  
> Om du vill att måttenheterna ska fungera så bra som möjligt i distributionslagret, också när du använder enhetsbrytning, ska du försöka:  
>
> - Ange den minsta måttenhet som du tror kommer att användas i distributionslagret som basmåttenhet för artiklar.  
> - Ange alternativa måttenheter för artiklar som multiplar av basmåttenheten.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md) 
[Monteringshantering](assembly-assemble-items.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

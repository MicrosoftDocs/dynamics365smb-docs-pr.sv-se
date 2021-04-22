---
title: Så här flyttar du artiklar i avancerad distributionslagerkonfiguration | Microsoft Docs
description: I avancerad lagerkonfiguration, dvs lagerställen som använder Dirigerad art.inf. och plockning , utförs transporter mellan lagerställen av en ansvarig anställd som förbereder Dist.lager transporterna i transportkalkylarket och sedan skapar dist.lager transporterna så att lagerpersonalen kan utföra dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e843b048c117539d077dc4a8ecba33f265a2e826
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782640"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Flytta artiklar i avancerade distributionslagerkonfigurationer
I avancerad lagerkonfiguration, dvs lagerställen som använder Dirigerad art.inf. och plockning , utförs transporter mellan lagerställen av en ansvarig anställd som förbereder Dist.lager transporterna i transportkalkylarket och sedan skapar dist.lager transporterna så att lagerpersonalen kan utföra dem.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Så här flyttar du artiklar med dist.lager transport kalkylarket
Sidan **Transportkalkylark** innehåller två funktioner som du kan använda för att fylla i raderna automatiskt. Den första är funktionen **Beräkna lagerplatsåteranskaffning** Den här funktionen använder lagerplatsrang för att föreslå påfyllning för med lagerställen med högre lagerplatsordning från lagerställen med lägre rang. Den andra funktionen är **Hämta lagerställesinnehåll** som fyller i kalkylarksraderna med hela lagerställesinnehållen, för de lagerställen du anger.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Transportkalkylark** och välj sedan relaterad länk.  
2.  Fyll i tillämplig distributionslagertransportinformation på kalkylarksraderna.  
3. Välj åtgärden **Skapa transport** om du vill skapa ett dokument för distributionslagertransport som kan registreras när distributionslagertransporten är slutförd.  

### <a name="to-register-the-warehouse-movement"></a>Så här registrerar du distributionslagertransporten:  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Förflyttningar** och välj sedan tillhörande länk.  
2.  Öppna Dist.lager transport som du vill arbeta med.  
3.  Ange var och när artikeln i fråga ska flytta genom att redigera **Zonkod**, **Lagerställeskod**, **Ant. att hantera** eller **Förfallodatum** på rader med åtgärdstypen **Plats**.  

    Om distributionslagret har ställts in så att lagerställeskoderna följer den fysiska strukturen i distributionslagret kan du ta kvantiteter av flera olika artiklar från intilliggande lagerställen och sedan placera dem på lagerställen för framåtplockning, som också kan ligga nära varandra.  
4.  Ange i **Ant. att hantera** fältet en delantal för lagerställesinnehållet som du vill flytta, på rader med åtgärdstypen **Ta**. Alla övriga fält på rader med åtgärdstypen **Ta** är skrivskyddat.  
5.  Om du vill flytta alla föreslagna antal mängder som anges i fältet **Antal** använder du åtgärden **Fyll i auto. ant. att hantera**.  
6. Välj **Registrera**.  

> [!NOTE]  
>  Om dirigerad artikelinförsel och plockning används för lagerstället, kan du inte manuellt flytta artiklar till eller från lagerställen av typen INLEVERANS. Det beror på att artiklarna måste registreras som införda innan de blir en del av det tillgängliga lagret.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Så här registrerar du transporten av en artikel som redan har skett  
Om lagerstället är inställt på dirigerad artikelinförsel och plockning, och du måste flytta artiklar till andra lagerställen utan en befintlig distributionslagerartikelinförsel, plockning eller transport, kan du registrera korrekt placering av artiklarna i distributionslagret med **Dist.lager omgrupperingsjnl**.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lagergrupperingsjnl** och välj sedan tillhörande länk.  
2.  Fyll i fälten **Artikelnr**, **Från zonkod**, **Från lagerställeskod**, **Till zonkod** och **Till lagerställeskod**.  
3.  Välj **Registrera**.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
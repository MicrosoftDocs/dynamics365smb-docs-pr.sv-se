---
title: Flytta artiklar i avancerade distributionslagerkonfiguration
description: I det här avsnittet beskrivs hur en erfaren anställd kan ordna flyttning av artiklar i avancerade distributionslager konfigurationer som gäller för lagerställen med dirigerad artikelinförsel och plockning.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7351
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 1c1f86cae4ad411efe21453d58761b436bb7470d
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532518"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Flytta artiklar i avancerade distributionslagerkonfigurationer

I avancerad lagerkonfiguration, dvs lagerställen som använder Dirigerad art.inf. och plockning , utförs transporter mellan lagerställen av en ansvarig anställd som förbereder Dist.lager transporterna i transportkalkylarket och sedan skapar dist.lager transporterna så att lagerpersonalen kan utföra dem.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Så här flyttar du artiklar med dist.lager transport kalkylarket

Sidan **Transportkalkylark** innehåller två funktioner som du kan använda för att fylla i raderna automatiskt. Den första är funktionen **Beräkna lagerplatsåteranskaffning** Den här funktionen använder lagerplatsrang för att föreslå påfyllning för med lagerställen med högre lagerplatsordning från lagerställen med lägre rang. Den andra funktionen är **Hämta lagerställesinnehåll** som fyller i kalkylarksraderna med hela lagerställesinnehållen, för de lagerställen du anger.

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Transportkalkylark** och väljer sedan relaterad länk.  
2.  Fyll i tillämplig distributionslagertransportinformation på kalkylarksraderna.  
3. Välj åtgärden **Skapa transport** om du vill skapa ett dokument för distributionslagertransport som kan registreras när distributionslagertransporten är slutförd.  

### <a name="to-register-the-warehouse-movement"></a>Så här registrerar du distributionslagertransporten:

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **transport** och väljer sedan relaterad länk.  
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

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lagergrupperingsjnl** och väljer sedan relaterad länk.  
2.  Fyll i fälten **Artikelnr**, **Från zonkod**, **Från lagerställeskod**, **Till zonkod** och **Till lagerställeskod**.  
3.  Välj **Registrera**.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

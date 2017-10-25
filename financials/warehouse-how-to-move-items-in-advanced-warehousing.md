---
title: "Så här flyttar du artiklar i avancerad distributionslagerkonfiguration | Microsoft Docs"
description: "I avancerad lagerkonfiguration, dvs lagerställen som använder Dirigerad art.inf. och plockning , utförs transporter mellan lagerplatser av en ansvarig anställd som förbereder Dist.lager transporterna i transportförslaget och sedan skapar dist.lager transporterna så att lagerpersonalen kan utföra dem."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/232017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 019d60da5611174b873d07e8adb25ed78b01467b
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-move-items-in-advanced-warehouse-configurations"></a>Så här flyttar du artiklar i avancerad distributionslagerkonfiguration
I avancerad lagerkonfiguration, dvs lagerställen som använder Dirigerad art.inf. och plockning , utförs transporter mellan lagerplatser av en ansvarig anställd som förbereder Dist.lager transporterna i transportförslaget och sedan skapar dist.lager transporterna så att lagerpersonalen kan utföra dem.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Så här flyttar du artiklar med dist.lager transport förslaget
Fönster **Transportförslag** innehåller två funktioner som du kan använda för att fylla i raderna automatiskt. Den första är funktionen **Beräkna lagerplatsåteranskaffning** Den här funktionen använder lagerplatsrang för att föreslå påfyllning för med lagerplatser med högre lagerplatsordning från lagerplatser med lägre rang. Den andra funktionen är **Hämta lagerplatsinnehåll** som fyller i förslagsraderna med hela lagerplatsinnehållen, för de lagerplatser du anger.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Transportförslag**, och välj sedan relaterad länk.  
2.  Fyll i tillämplig distributionslagertransportinformation på förslagsraderna.  
3. Välj åtgärden **Skapa transport** om du vill skapa ett dokument för distributionslagertransport som kan registreras när distributionslagertransporten är slutförd.  

### <a name="to-register-the-warehouse-movement"></a>Så här registrerar du distributionslagertransporten:  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Transporter** och välj sedan relaterad länk.  
2.  Öppna Dist.lager transport som du vill arbeta med.  
3.  Ange var och när artikeln i fråga ska flytta genom att redigera **Zonkod**, **Lagerplatskod**, **Ant. att hantera**eller **Förfallodatum** på rader med åtgärdstypen **Plats**.  

    Om distributionslagret har ställts in så att lagerplatskoderna följer den fysiska strukturen i distributionslagret kan du ta kvantiteter av flera olika artiklar från intilliggande lagerplatser och sedan placera dem på lagerplatser för framåtplockning, som också kan ligga nära varandra.  
4.  Ange i **Ant. att hantera** fältet en delantal för lagerplatsinnehållet som du vill flytta, på rader med åtgärdstypen **Ta**. Alla övriga fält på rader med åtgärdstypen **Ta** är skrivskyddat.  
5.  Om du vill flytta alla föreslagna antal mängder som anges i fältet **Antal** använder du åtgärden **Fyll i auto. ant. att hantera**.  
6. Välj **Registrera**.  

> [!NOTE]  
>  Om dirigerad artikelinförsel och plockning används för lagerplatsen, kan du inte manuellt flytta artiklar till eller från lagerplatser av typen INLEVERANS. Det beror på att artiklarna måste registreras som införda innan de blir en del av det tillgängliga lagret.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Så här registrerar du transporten av en artikel som redan har skett  
Om lagerstället är inställt på dirigerad artikelinförsel och plockning, och du måste flytta artiklar till andra lagerplatser utan en befintlig distributionslagerartikelinförsel, plockning eller transport, kan du registrera korrekt placering av artiklarna i distributionslagret med **Dist.lager omgrupperingsjnl**.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Dist.lagergrupperingsjnl** och välj sedan relaterad länk.  
2.  Fyll i fälten **Artikelnr**, **Från zonkod**, **Från lagerplatskod**, **Till zonkod** och **Till lagerplatskod**.  
3.  Välj **Registrera**.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


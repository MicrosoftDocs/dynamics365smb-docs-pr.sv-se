---
title: Skapa och publicera KPI-webbtjänster för kontouppställningar | Microsoft Docs
description: Det här avsnittet beskriver hur du visar kontouppställningen KPI-data baserat på specifika kontouppställningar.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 72687930e20f00c8a6d244cac0e8f682de2d34a4
ms.sourcegitcommit: 103d1433454dbedf8a72a292853eac3501872f24
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961533"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Skapa och publicera KPI-webbtjänster som baseras på kontouppställningar
På sidan **Installation av webbtjänst för KPI för kontouppställning** kan du konfigurera hur du visar kontouppställnings-kpi-data och vilka specifika kontouppställningar som du vill basera KPI-erna på. När du väljer knappen **Publicera webbtjänst** läggs det angivna kontouppställning-kpi-data till listan över publicerade webbtjänster på sidan **Webbtjänster**.  

> [!NOTE]
> När du använder den här webbtjänsten inkluderas inte avslutsdatum i datauppsättningen. På så sätt kan du använda filter i Power BI för att analysera olika tidsperioder.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Så här: Skapar och publicerar du en KPI-webbtjänst som är baserad på kontouppställningar  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **KPI Web Service kontouppställningsinställning** och välj sedan relaterad länk.  
2.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Allmänt**.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Start för prognostiserade värden**|Ange vid vilken tidpunkt i prognosen som värden visas på kontouppställning-kpi-grafiken.<br /><br /> De prognostiserade värdena hämtas från redovisningsbudgeten som du väljer i fältet **Redov.budgetnamn**. **Obs!** Om du vill få KPI:er att visar prognossiffror efter ett visst datum och den verkliga siffror före datumet, kan du ändra fältet **Tillåt bokföring fr.o.m.** på sidan **Redovisningsinställningar**. Mer information finns också i Tillåt bokföring fr.o.m..|  
    |**Redov.budgetnamn**|Ange namnet på den redovisningsbudget som ger prognostiserade värden till kontouppställning-kpi-webbtjänsten.|  
    |**Period**|Ange perioden som kontouppställning-KPI-webbtjänsten baseras på.|  
    |**Visa per**|Ange vid vilket tidsintervall kontouppställning-KPI visas i.|  
    |**Webbtjänstnamn**|Ange namnet på kontouppställningen-KPI-webbtjänsten.<br /><br /> Det här namn visas i fältet **Servicenamn** på sidan **Webbtjänster**.|  

    Ange en eller flera kontouppställningar som du vill publicera som en KPI webbtjänst enligt inställningarna, som du gjorde i föregående tabellen.  

3.  Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **kontouppställningar**.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kontouppställningsnamn**|Ange kontouppställningen som KPI-webbtjänsten baseras på.|  
    |**Beskrivning av kontouppställning**|Ange beskrivningen av kontouppställningen som KPI webbtjänsten baseras på.|  

4.  Upprepa moment 3 för alla kontouppställningar som du vill basera kontouppställningswebbtjänsten för kpi på.  
5.  Välj åtgärden **Redigera kontouppställning** på snabbfliken **Kontouppställning** för att visa eller redigera den valda kontouppställningen.  
6.  Om du vill visa kontouppställning-kpi-data som du har upprättat väljer du åtgärden **Webbtjänst för KPI för kontouppställning**.  
7.  Om du vill publicera kontouppställningens KPI-webbtjänst väljer du åtgärden **Publicera webbtjänst**. Webbtjänsten läggs till i listan över publicerade webbtjänster på sidan **Webbtjänster**.  

> [!NOTE]  
>  Du kan också publicera KPI webbtjänsten genom att peka på sidobjektet **KPI Web Service kontouppställningsinställning** från sidan **Webbtjänster**. Mer information finns i [Publicera en webbtjänst](across-how-publish-web-service.md).  

## <a name="see-also"></a>Se även  
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
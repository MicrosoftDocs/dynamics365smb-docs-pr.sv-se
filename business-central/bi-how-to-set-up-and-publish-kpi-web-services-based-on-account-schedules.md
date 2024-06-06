---
title: Skapa och publicera KPI-webbtjänster som baseras på ekonomiska rapporter
description: Denna artikel beskriver hur du visar KPI-data för ekonomisk rapport baserat på specifika ekonomiska rapporter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a>Skapa och publicera KPI-webbtjänster som baseras på ekonomiska rapporter

På sidan **Konfiguration av webbtjänst för KPI för ekonomisk rapport** kan du konfigurera hur du visar KPI-data för ekonomiska rapporter och vilka specifika ekonomiska rapporter som du vill basera KPI-erna på. När du väljer **Publicera webbtjänst** läggs angivna KPI-data för ekonomisk rapport till listan över publicerade webbtjänster på sidan **Webbtjänster**.

> [!NOTE]
> När du använder den här webbtjänsten inkluderas inte avslutsdatum i datauppsättningen. Du kan sedan använda filter i Power BI för att analysera olika tidsperioder.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a>Skapa och publicera en KPI-webbtjänst som baseras på ekonomiska rapporter
  
1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Installation av webbtjänst för KPI för ekonomisk rapport** och välj sedan relaterad länk.
2. På snabbfliken **Allmänt** fyller du i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Fyll i fälten på snabbfliken **Raddefinitioner**.
4. Upprepa steg 3 för alla ekonomiska rapporter som du vill basera webbtjänsten för KPI för ekonomisk rapport på.  
5. För att visa eller redigera den valda ekonomiska rapporten går du till snabbfliken **Raddefinitioner** och väljer åtgärden **Redigera raddefinition**.
6. Om du vill visa KPI-data för ekonomisk rapport som du har upprättat väljer du åtgärden **Webbtjänst för KPI för ekonomisk rapport**.
7. Om du vill publicera KPI-webbtjänst för ekonomisk rapport väljer du åtgärden **Publicera webbtjänst**.

Du kan nu skapa ekonomiska rapporter i Power BI baserat på den webbtjänst eller de tjänster som du har skapat.

> [!NOTE]  
> Du kan också publicera KPI-webbtjänsten genom att peka på sidobjektet **Installation av webbtjänst för KPI för ekonomisk rapport** från sidan **Webbtjänster**. Läs mer i [Publicera en webbtjänst](across-how-publish-web-service.md).

## <a name="see-also"></a>Se även

[Financial Business Intelligence](bi.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

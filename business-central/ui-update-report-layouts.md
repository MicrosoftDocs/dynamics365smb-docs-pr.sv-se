---
title: Uppdatera en rapportlayout kontinuerligt | Microsoft Docs
description: "Du kan behöva uppdatera en anpassad rapportlayout som används i en rapport. Det krävs när en designändring har skett för rapportens datauppsättning, till exempel att ett fält som används i layouten har tagits bort från rapportdatauppsättningen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 90fa2b52444d057149b39da87f5dfab6d91e8681
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="updating-report-or-document-layouts"></a>Uppdatera rapport- eller dokumentlayouter
Ibland kan du behöva uppdatera en anpassad rapportlayout som används i en rapport. Det krävs när en designändring har skett för rapportens datauppsättning, till exempel att ett fält som används i layouten har tagits bort från rapportdatauppsättningen. Om en rapportlayout kräver att uppdatering kommer du att få ett felmeddelande när du försöker att förhandsgranska, skriva ut eller spara rapporten.  
  
Du kan automatiskt uppdatera rapportlayouten från felmeddelandet som visas när du kör en rapport genom att välja knappen **Ja** på felmeddelandet. Eller, innan du kör rapporter, kan du uppdatera specifika rapportlayouter eller alla anpassade rapportlayouter som kan påverkas av datauppsättningsändringar.  
  
Du kan också välja att testa uppdateringarna utan att tillämpa de nödvändiga ändringarna i de anpassade rapportlayouterna. På så sätt kan du se vilka ändringar som kommer att tillämpas i rapportlayouten och identifiera eventuella fel i processen. Från testresultaten kan du öppna de anpassade rapportlayouterna direkt och åtgärda eventuella fel. Vi rekommenderar att du testar rapportlayoutuppdateringarna innan du tillämpar dem.  
  
Alla rapportdatauppsättningsändringar kan inte uppdateras automatiskt i rapportlayouter. För vissa ändringar krävs att du redigerar rapportlayouten manuellt. Mer information finns i [Begränsningar för uppdatering av anpassad rapportlayout](ui-update-report-layouts.md#UpdateLimitations).  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a>Så här uppdaterar du en eller flera anpassade rapportlayouter  
  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Rapportlayouter** och välj sedan relaterad länk.  
  
2.  I fönstret **rapportlayouter**, om du vill uppdatera in en viss layout i listan, väljer du layouten från listan och sedan åtgärden **uppdatera layouten**. Eller, om du vill uppdatera alla standardrapportlayouter för företaget, klickar du på åtgärden **uppdatera alla layouter**.  

Om inga fel uppstår tillämpas uppdateringarna för rapportlayouterna. Om fel uppstår visas ett meddelande med felen. Då måste du åtgärda felen genom att redigera den anpassade rapportlayouten manuellt. Mer information finns i [Åtgärda fel](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a>Så här testar du uppdateringar för en anpassade rapportlayout  
  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Val av rapportlayout** och välj sedan relaterad länk.  
  
2.  I fönstret **Val av rapportlayout** väljer du åtgärden **Testlayoutuppdateringar**.  
  
 Ändringar till rapportlayouterna testas men tillämpas inte på de faktiska rapportlayouterna. Fönstret **Uppdateringslogg för rapportlayout** visas med status för potentiella uppdateringar för varje rapportlayout. Om det finns fel för en rapportlayout kan du öppna rapportlayouten direkt från meddelandet och åtgärda felen. Mer information finns i [Åtgärda fel](ui-update-report-layouts.md#FixErrors).  
  
##  <a name="UpdateLimitations"></a> Begränsningar för uppdatering av anpassad rapportlayout  
 Det finns flera typer av ändringar som den automatiska uppdateringen kan tillämpa för anpassade rapportlayouter. Ett fält som används i layouten kan till exempel ha tagits bort från rapportdatauppsättningen. Däremot kan den automatiska uppdateringen inte hantera följande ändringar i en rapportdatauppsättning.  
  
1.  Borttagna fält, rubriker eller dataobjekt.  
  
2.  Dubblettfältnamn i rapportlayouten efter att namnet på fältet har ändrats i datauppsättningen. Det här ska behandlas som ett designfel.  
  
3.  Uppgraderingsscenarier där det finns flera iterationer av en rapportlayout som orsakar flera namnbytesåtgärder för samma fält, rubriker eller dataobjekt.  
  
 Om något av dessa problem identifieras i uppdateringsprocessen kan inte uppdateringen tillämpas. Du måste åtgärda problemen manuellt, till exempel genom att redigera rapportlayouten i Word eller via programmering med hjälp av kodenheter för uppgradering.  
  
##  <a name="FixErrors"></a> Åtgärda fel  
 Om du får ett felmeddelande när du uppdaterar eller testar rapportlayoutuppdateringar måste du troligtvis ändra rapportlayouten för att lösa problemet. Läs felmeddelandet för att fastställa orsaken till problemet.  
  
 De mest vanliga problemet inträffar när ett fält som användes på layout har tagits bort från rapportdatauppsättningen. I det här fallet visas en rad i felmeddelandet som anger att en artikel har tagits bort. För att lösa problemet måste du ändra layouten och ta bort fältet i fråga.  
  
 Mer information finns i [Skapa och ändra en anpassad rapportlayout](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  
  
 Försök att uppdatera layouten på nytt när du har ändrat layouten.  
  
## <a name="see-also"></a>Se även  
 [Hantera rapportlayouter](ui-manage-report-layouts.md)  
 [Arbeta med rapporter](ui-work-report.md)  

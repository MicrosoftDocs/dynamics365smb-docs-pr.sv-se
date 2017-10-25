---
title: "Bokför koncerninterna dokument och journaler | Microsoft Docs"
description: "använda koncerninterna dokument för att bokföra transaktioner med partnerföretag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: eeb070e1431d55248a762b444c2298281b0a5101
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-intercompany-documents-and-journals"></a>Så här: arbeta med koncerninterna dokument och journaler
Du använder koncerninterna dokument eller journaler för att bokföra transaktioner med koncerninterna partner. När du bokför ett koncerninternt dokument eller journalrad i företaget skapas, skapas ett motsvarande dokument eller journalrad i din koncerninterna utkorg som du kan överföra till partnern. Partnern kan sedan bokföra den koncerninterna transaktionen i sitt företag utan att behöva registrera samma data på nytt.

För försäljnings- och inköpsdokument, säkerställer koden för koncernintern partner på den involverade kunden eller leverantören att alla order och fakturor som har genererats gäller transaktioner med dessa företag kommer att producera motsvarande dokument i partnerföretaget, vilket resulterar i att räkenskaperna balanseras korrekt.

För koncerninterna redovisningsjournalrader behöver du inte ange konton för en enskild räkenskapsbok, utan helt enkelt ange moderbolaget. Motsvarande koncerninterna redovisningsjournalrader skapas sedan i partnerföretaget som resulterar i att räkenskaperna balanseras för de båda företag som är involverade i en transaktion.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Så här fyller du i och skickar en koncernintern försäljningsorder
Du kan skicka försäljnings- och inköpsorder samt returorder före bokföring. Fakturor och kreditnotor kan inte skickas förrän de är bokförda.

Följande procedur beskriver hur du fyller i och skickar en koncernintern försäljningsorder. Samma steg gäller koncerninterna inköpsorder och returorder och till bokförda koncerninterna fakturor och kreditnotor.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2. Välj **Ny** för att skapa en ny försäljningsorder. Mer information finns i [Så här säljer du produkter](sales-how-sell-products.md).  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Se till att kunden är en koncernintern partner.
5. Om du vill skicka försäljningsordern innan du bokför den, väljer du åtgärden **skicka Koncerninterna försäljningsorder**.

> [!NOTE]
> Om du utför steg 4, kommer försäljningsordern flyttas till koncerninterna utkorgen där du kan skicka den senare. Mer information finns i [så här: hantera koncerninterna inkorgen och utkorgen](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Så här fyller du i och bokför koncerninterna journaler
När du bokför ett koncernintern redovisningsjournalsrad i företaget skapas, skapas ett motsvarande journalrad i din koncerninterna utkorg som du kan överföra till partnern. Partnern kan sedan bokföra den koncerninterna transaktionen i sitt företag utan att behöva registrera samma data på nytt.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Konc.int. redovisningsjournaler** och välj sedan relaterad länk.  
2. Öppna relevant journal. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).
3. Fyll i fälten om det behövs.
4. I fältet **Redov.ktonr konc.int. partner** anger du det koncerninterna redovisningskontot som beloppet ska bokföras på i partnerns företag.

    > [!NOTE]
    > Fältet måste vara ifyllt på en rad med ett bankkonto eller redovisningskonto i antingen fältet **Kontonr.** eller **Motkonto**.  
5. Välj åtgärden **Bokföra**.

Transaktionerna som bokförs i företaget och en journal med motsvarande transaktioner skapas i koncerninterna utkorgen som du kan skicka till partnerföretaget. Mer information finns i [så här: hantera koncerninterna inkorgen och utkorgen](intercompany-how-manage-intercompany-inbox.md). 

## <a name="see-also"></a>Se även
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


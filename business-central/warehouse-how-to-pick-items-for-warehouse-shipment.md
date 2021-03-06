---
title: 'Så här: plocka artiklar för Dist.lager utleverans | Microsoft Docs'
description: När Lagerställe är inställt på att begära plockningsbearbetning så väl som utleveransbearbetning använder du plockningsdokumenten för att skapa och bearbeta plockningsinformationen innan du bokför Lagerutleveransen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7f9cc098fc414afcf015821dadbfbe438ca157ef
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771760"
---
# <a name="pick-items-for-warehouse-shipment"></a>Plocka artiklar för utleverans från dist.lager
När Lagerställe är inställt på att begära plockningsbearbetning så väl som utleveransbearbetning använder du plockningsdokumenten för att skapa och bearbeta plockningsinformationen innan du bokför Lagerutleveransen.  

Du kan inte skapa ett dokument för dist.lager plockning från grunden, eftersom en plockningsaktivitet alltid ingår i ett arbetsflöde, i ett pull-/pushscenario.  

Du kan skapa dokumentet för dist.lager plockning med ett pullmetod genom att öppna ett tomt distributionslagerdokumentet, hitta källdokument som släpps till leveransen, och sedan skapa plockningsraderna för de utleveranser. Du kan använda **Hämta källdokument** , eller **Filter för att hämta urspr.dok.** funktioner för att undersöka källdokument som är klara för utleverans.

Du kan också använda sidan **Plockningsförslag** för att flytta plockningsrader i batchläge. Mer information finns i [Planera plockningar i kalkylark](warehouse-how-to-plan-picks-in-worksheets.md).  

Du kan också skapa dokument för dist.lager plockning med pushmetod från sidan **Dist.lager utleverans**, genom att välja **Skapa plockning**.  

> [!NOTE]  
>  Plockning för distributionslagerutleverans av artiklar som är monterade till försäljningsorder som har levererats, följer samma steg för distributionslager som vanliga plockning för utleverans, enligt beskrivningen i det här avsnittet. Numret på plockningsrader per antal som ska levereras kan vara många-till-en, eftersom plockning för distributionslager är för monteringskomponenter och inte för monteringsartikeln.  
>   
>  Distributionslagerplockningsrader skapas för värdet i fältet **Återstående antal** på raderna i monteringsorder som är kopplad till försäljningsorderraden som levereras. Det gör att alla komponenter kan plockas i en åtgärd.  
>   
>  Mer information finns i avsnittet ”Hantera artiklar för montering mot kundorder i distributionslagerutleveranser”.  
>   
>  Information om hur du plockar komponenter för monteringsorder i allmänhet, inklusive situationer där monteringsartikeln inte ska betalas på en utleverans, se [Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Så här plocka artiklar för utleverans  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Plockningar** och välj sedan relaterad länk.  

    Om du vill arbeta med en viss plockning väljer du plockningen från listan eller filtrerar listan för att söka efter de plockningar som specifikt har tilldelats dig. Öppna plockningskortet.  
2.  Om **Tilldelat användar-ID** är tomt, anger du ID för att identifiera själv om det behövs.  
3.  Utför den faktiska plockning av artiklar.  

    Om distributionslagret har konfigurerats att använda lagerställen, då artikelns standardlagerställen används för att föreslå var du vill hämta artiklar från. instruktionerna visas som två separata rader, minst en för varje åtgärdstyp, en för ta och en för placera.  

    Om distributionslagret är inställt på dirigerad artikelinförsel och plockning, lagerplatsordningen används för att beräkna de bästa lagerställena som ska plockas från, och de lagerställen föreslås på plockningsraderna. instruktionerna visas som två separata rader, minst en för varje åtgärdstyp, en för ta och en för placera.  

4.  När du har utfört plockningen och placerat artiklarna i utleveransområdet eller på lagerstället för utleveranser väljer du åtgärden **Registrera plockning**.  

Den person som ansvarar för utleverans kan nu få artiklarna till ett leveransdockan och bokföra leveransen, inklusive relaterade källdokumentet, på sidan **Dist.lager utleverans**. Mer information finns i [Leverera artiklar](warehouse-how-ship-items.md).   

Förutom plockning för källdokument, som beskrivs i det här avsnittet, kan du ta och placera artiklar mellan lagerställen, utan att referera till källdokument. Mer information finns i [Plocka och föra in utan källdokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Hantera artiklar för montering mot kundorder i distributionslagerutleveranser
I montering mot kundorder-scenarier är fältet **Ant. att utleverera** på distributionslagerutleveransrader använt för att notera hur många enheter som monteras. Det angivna antalet bokförs sedan som monteringsutflöde när distributionslagerutleveransen bokförs.

För andra distributionslagerutleveransrader är värdet i **Ant. att utleverera** noll från början.

När arbetare ansvariga för slutfört monterande av komponenter för montering eller hela antalet för montering mot kundorder, registrerar de i fältet **Ant. att utleverera** på distributionslagerutleveransraden i avancerade konfigurationer och väljer åtgärden **Bokför utleverans**. Resultatet blir att det motsvarande monteringsutflödet bokförs, inklusive komponentförbrukningen. En utleverans för kvantiteterna bokförs för försäljningsordern.

Från monteringsordern kan du välja **Montering mot kundorder, dist.lager utleveransrad** för att komma åt distributionslagerutleveransraden. Det är praktiskt exempelvis för arbetare som inte använder vanligtvis sidan **Dist.lager utleverans**.

När distributionslagerutleveransen har bokförts uppdateras olika fält på försäljningsorderraden för att visa förloppet i distributionslagret. Följande fält uppdateras också för att visa hur många antal för montering mot kundorder som återstår att monteras och levereras:

- **ATO Restnot. antal i lager**
- **ATO Restnot. antal i lager (bas)**

> [!NOTE]
> I alla scenarier där en del av antalet måste först vara monterat och ett annat ska levereras från lagret, skapas ett minimum på två distributionslagerutleveransrader. En är för antal för montering mot kundorder, och en är lagerantalet.

> I så fall hanteras antal för montering mot kundorder som beskrivs i det här avsnittet, och lagerantalet behandlas som andra distributionslagerutleveransrader. Mer information om kombinationsscenarion finns i [Förstå montering mot order och montering mot lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
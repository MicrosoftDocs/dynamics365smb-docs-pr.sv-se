---
title: Ångra en bokföring genom att bokföra en mottransaktion | Microsoft Docs
description: Om du har bokfört en felaktig bokföring i den allmänna journalen, kan du använda funktionen Återför transaktion för att ångra bokföringen med ett korrekt redovisningsspårning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cdbf4b682b4ad99524ea0aace9a123283668fb43
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779103"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Återföra journalbokningar och ångra inleveranser/utleveranser
För att kunna återföra (ångra) en felaktig bokföring markerar du posten och skapar en korrigeringspost (transaktioner som är identiska med den ursprungliga transaktionen, men har ett motsatt tecken i beloppsfältet) med samma dokumentnummer och bokföringsdatum som den ursprungliga posten automatiskt. När du har återfört en post måste du skapa en korrekt post.

Du kan endast återföra poster som har bokförts från en redovisningsjournalrad. En transaktion kan endast återföras en gång.

Om du vill ångra en bokföring av inleverans eller utleverans innan de bokförs som fakturerade kan du använda funktionen **ångra** i det bokförda dokumentet. Du kan ångra kvantiteter av typen **Artikel** och **Resurs**.

Om du har bokfört fel negativt antal, till exempel om en inköpsorder med fel antal artiklar och bokfört den som inlevererad men inte fakturerad, kan du ångra bokföringen.

Om du har bokfört fel positivt antal, till exempel en utleverans eller en inköpsreturorder med fel antal artiklar och bokfört den som levererad men inte fakturerad, kan du ångra bokföringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Att återföra bokföringen av en redovisningstransaktion journal
Du kan återföra poster från alla sidor **Transaktioner**. Följande procedur baseras sidan **redovisningstransaktioner**.
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsposter** och välj sedan relaterad länk.
2. Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**. Observera att det måste komma från en journalbokföring.
3. Välj åtgärden **Återför** på sidan **Återför transaktionsposter**.
4. Välj knappen **Ja** på bekräftelsemeddelandet.

> [!NOTE]
> Du kan inte ångra transaktioner som har bokförts med information från ett projekt eller som har realiserade vinster och förluster inom samma transaktion.

## <a name="to-post-a-negative-entry"></a>Bokföra en negativ transaktion  
Använd fältet **Korrigering** för att bokföra en negativ debet istället för en kredit, eller för att bokföra en negativ kredit istället för en debet för ett konto. För att uppfylla juridiska krav visas detta fält som standard i alla journaler. Fälten **Debetbelopp** och **Kreditbelopp** innehåller både ursprungstransaktionen och den korrigerade transaktionen. Dessa fält påverkar inte kontosaldot.  

1.  Välj ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Redovisningsjournaler** och välj sedan relaterad länk.  
2.  Välj önskat batch-namn i fältet **Batch-namn**.  
3.  Ange information i relevanta fält.  
4.  På journalraden som du vill aktivera för negativa poster väljer du kryssrutan **Korrigering**.  
5.  Välj åtgärden **Bokför** och välj sedan knappen **Ja** för att bokföra journalen.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Så här ångrar du ett bokfört antal i en bokförd inköspleverans  
Nedan beskrivs hur du återställer en bokförd inleverans eller bokförda resurser. Momenten är liknande för bokförda utleveranser.

1.  Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda inköpsleveranser** och välj sedan relaterad länk.  
2.  Öppna den bokförda inleveransen som du vill ångra.  
3.  Markera de rader som du vill ångra.  
4.  Välj åtgärden **Ångra inleverans**.

En rättningsrad infogas under den valda inleveransraden. Om antalet har inlevererats i en lagerinleverans infogas en rättningsrad i den bokförda lagerinleveransen.  

Fälten **Inlevererat antal** och **Inlevrd. antal ej faktrd.** på den relaterade inköpsordern är nollställda.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Så här ångrar du ett bokfört antal i bokförda returleveranser
Nedan beskrivs hur du återställer en bokförd returutleverans av artiklar eller resurser och sedan bokför inköpsreturen med en ny kvantitet. Momenten är liknande för bokförda returinleveranser.

1.  Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda returutleveranser** och välj sedan relaterad länk.  
2.  Öppna den bokförda returutleveranser som du vill ångra.
3. Markera de rader som du vill ångra.  

4.  Välj åtgärden **Ångra returutleverans**.  

    En rättningsrad införs nu i det bokförda dokumentet och fälten **Returant. levererat** och **Retur levererat ej faktrd** på returordern ändras till noll.  

    Gå nu tillbaka till inköpsreturordern som är klar att bokföras.  

5.  Observera antalet i fältet **Returordernr** på sidan **Returordernr**. .  
6.  Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsreturordrar** och välj sedan relaterad länk.  
7.  Öppna returordern i fråga och välj åtgärden **öppna igen**.  
8.  Korrigera värdet i fältet **Antal** och bokför inköpsreturordern igen.  

## <a name="see-also"></a>Se även
[Ångra monteringsboking](assembly-how-to-undo-assembly-posting.md)  
[Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
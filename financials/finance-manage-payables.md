---
title: "Hantera leverantörsreskontra | Microsoft Docs"
description: "Introduktion till utbetalning till leverantörerna och andra typer av betalningar."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-financials
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 03b872f9507e4c96dd55e8cf0f3d1ec7417501f2
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="managing-payables"></a>Hantera Leverantörsreskontra
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] har vad du behöver för att effektivt hantera leverantörsreskontra.  

## <a name="payments"></a>Betalningar
Det är enkelt att prioritera betalningar, beräkna avgifter för förfallna betalningar och hantera rabatter för tidiga betalningar.

Du kan registrera betalningar i en redovisningsjournal och sedan skriva ut checkar innan utbetalningsjournalen bokförs.

Du kan koppla en betalning för att stänga fakturan när du bokför betalningen eller när du har bokfört den. Den **Avräkningsmetod** som anges för leverantören (på **leverantörskortet**) bestämmer om du måste göra en manuell betalning eller om det görs automatiskt. Du kan alltid koppla transaktioner manuellt. Om avräkningsmetoden för leverantören är **Koppla till äldsta faktura** och du inte anger ett dokument som betalningen ska kopplas till, kopplas den emellertid till den äldsta öppna transaktionen för leverantören.

## <a name="suggest-vendor-payments"></a>Betalningsförslag för lev.
[!INCLUDE[d365fin](includes/d365fin_md.md)] används för att ta fram olika betalningsförslag, t.ex. betalningar som snart förfaller eller betalningar för vilka en rabatt kan erhållas. Du kan ange att belopp som specificerats som tillgängliga betalningsmedel och berättigade kassarabatter ska beaktas i betalningsförslaget.

## <a name="issue-checks"></a>Utfärda checkar
[!INCLUDE[d365fin](includes/d365fin_md.md)] låter dig utfärda checkar till leverantörer elektroniskt och manuellt. Du kan utföra båda i fönstret **betalningsjournaler**, där du kan även makulera checkar och granska checktransaktioner.

## <a name="export-payments-to-a-bank-file"></a>Exportera betalningar till en bankfil
När du är redo att göra betalningar till leverantörer med hjälp av fönstret **Betalningsjournal**, kan du exportera en fil med betalningsinformation från journalraderna. Du kan sedan överföra filen till den elektroniska banken att bearbeta pengaöverföringar.

Om du inte vill bokföra en utbetalningsjournalrad för en exporterad betalning, till exempel eftersom du väntar på att banken bekräftar transaktionen, kan du bara ta bort journalraden. När du senare skapar en utbetalningsjournal för att betala återstående belopp på fakturan kan du i fältet **Totalt exporterat belopp** se hur mycket av beloppet som redan har exporterats. Du kan också söka efter detaljerad information om det exporterade totalbeloppet genom att välja knappen **Transaktioner i kreditöverföringsregister**.

Om du väntar med att bokföra betalningar till när banken bekräftar att transaktionerna har behandlats, finns det två sätt att undvika återexporterande betalningar för öppna dokument av misstag:  

* I en utbetalningsjournal med föreslagna betalningsrader kan du sortera på antingen kolumnen **Exporterat till betalningsfil** eller **Totalt exporterat belopp** och sedan ta bort betalningsförslag för öppna fakturor för vilka betalningar som redan har gjorts och du inte vill göra betalningar för.

    **Obs!** du kan behöva lägga till en kolumn i listan. Mer information finns i [Användaranpassning](ui-user-personalization.md).  
* Alternativt, på batchjobbet **Betalningsförslag för lev.**, där du anger vilka betalningar som ska inkluderas i utbetalningsjournalen, kan du ange att du inte infogar journalrader för betalningar som redan har exporterats genom att markera kryssrutan **Hoppa över exporterade betalningar**.

## <a name="see-also"></a>Se även
[Betalningssätt](finance-payment-methods.md)  
[Ekonomi](finance.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


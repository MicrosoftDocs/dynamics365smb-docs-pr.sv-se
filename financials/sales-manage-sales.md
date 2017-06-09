---
title: "Försäljning | Microsoft Docs"
description: "Beskriver hur du hanterar försäljningsaktiviteter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 04/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d8b73dcf1ee000bd13aec200c82275eb3c0f9d1d
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="sales"></a>FÖRS
Du kan skapa en försäljningsfaktura eller försäljningsorder för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.

Du måste använda försäljningsorder om din försäljningsprocess kräver att du t.ex. kan leverera delar av en orderkvantitet eftersom hela kvantiteten inte är tillgängliga på en gång. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda försäljningsorder. I alla andra aspekter fungerar försäljningsorder på samma sätt som försäljningsfakturor.

Effektiva metoder för försäljning och marknadsföring handlar om hur du fattar rätt beslut vid rätt tidpunkt. Marknadsföringsfunktionen i [!INCLUDE[d365fin](includes/d365fin_md.md)] ger en exakt överblick över din kontaktinformation när du behöver den, så att du kan arbeta effektivt med potentiella kunder och öka kundtillfredsställelsen. Mer information finns i [Kundhantering](marketing-relationship-management.md).

Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsfaktura när du instämmer om försäljningen. När kunden har bekräftat avtalet, till exempel efter en offertprocess, skickar du en orderbekräftelse för att registrera dina åtagande att leverera produkterna enligt överenskomment.

När du har levererat produkterna, antingen helt eller delvis, bokför du försäljningsfakturan eller försäljningsordern som levererade eller som levererade och fakturerade för att skapa kundreskontratransaktioner i systemet.

I affärsmiljöer där kunden måste betala för produkter i förväg måste du vänta på kvittot på betalning innan du levererar produkterna. I de flesta fall behandlar du inkommande betalningar några veckor efter leverans, genom att koppla betalningarna till dess relaterade obetalda bokförda försäljningsfakturor. Mer information finns i [Så här stämmer du av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

Det är enkelt att korrigera eller annullera en bokförd försäljningsfaktura, innan den betalas. Det är användbart om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen. Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota för att återföra försäljningen.

Försäljningsdokument kan skickas som PDF-filer kopplade till e-postmeddelande. Brödtexten för e-post ska innehålla ett utdrag av försäljningsdokumentet, till exempel produkter, totalt belopp och en länk till webbplatsen för PayPal. Mer information finns i [Så här skickar du dokument via e-post](ui-how-send-documents-email.md).

För alla försäljningsprocesser kan du t.ex. inkludera ett arbetsflöde för godkännande för att kräva att stora försäljningar till vissa kunder godkänns av redovisningschefen. Mer information finns i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| Skapa en försäljningsoffert där du erbjuder produkter med förhandlingsbara villkor, innan du omvandlar offerten till en försäljningsfaktura. |[Så här gör du erbjudanden](sales-how-make-offers.md) |
| Skapa en försäljningsfaktura för att registrera en överenskommelse med en kund om att sälja produkter till vissa leverans- och betalningsvillkor. |[Så här fakturerar du försäljning](sales-how-invoice-sales.md) |
| Behandla en försäljningsorder som rör delvis leverans eller direktleverans. |[Så här säljer du produkter](sales-how-sell-products.md) |
| Länka en försäljningsorder till en inköpsorder för att sälja ett direktutleveransobjekt som ska levereras direkt från din leverantör till kunden. |[Så här utför du direktleveranser](sales-how-drop-shipment.md) |
| Utför en åtgärd på en obetald bokförd försäljningsfaktura som automatiskt skapar en kreditnota och antingen annullerar försäljningsfakturan eller skapar den på nytt, så att du kan göra korrigeringar. |[Så här rättar eller makulera du obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md) |
| Skapa en försäljningskreditnota för att återföra en särskild bokförd försäljningsfaktura för att visa produkter som kunden returnerar och vilka belopp som du ska återbetala. |[Så här behandlar du försäljningreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md) |
| Skapa ett kundkort för varje kund som du säljer till. |[Så här registrerar du nya kunder](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Se även
[Konfigurera försäljning](sales-setup-sales.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.MD)  
[Projekthantering](projects-manage-projects.md)    
[Logistik](madeira-supply-chain.md)      
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

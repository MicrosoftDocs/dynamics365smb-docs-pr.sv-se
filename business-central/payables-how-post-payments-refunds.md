---
title: "Koppla betalningar till relaterade dokument och bokför dem | Microsoft Docs"
description: "Beskriver hur du kan registrera betalningar du gör till leverantörer och återbetalningar som du gör till kunder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: sv-se
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Registrera betalningar och återbetalningar
I fönstret **Betalningsjournal** registrerar du betalningar du gör till leverantörer och återbetalningar som du gör till kunder. När du bokför en utbetalningsjournalrad registreras det betalda beloppet för det angivna bankkontot. Du måste sedan vidta åtgärder för att utföra den faktiska överföringen pengar från relaterat bankkonto.

Om du fyller i fältet **Kopplas till ver.nr.** med den faktura eller kreditnotan som måste betalas ut eller återbetalas, är det aktuella dokumentet inställt att betalas när du bokför journalen. Det kallas för "kopplad". Som ett alternativ till att använda under betalningsbokföring kan du använda fönstret **Koppla leverantörstrans** och **Koppla kundtransaktioner** när du har gjort bokföringen av betalningen. Mer information finns i tillhörande, t.ex. [Stämma av leverantörsbetalningar manuellt](payables-how-apply-purchase-transactions-manually.md).

Funktionen **Betalningsförslag för lev.** hjälper dig att fylla i betalningsjournalraderna automatiskt enligt leverantörens prioritering och förfallodatum. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md). Med denna funktionen fylls fältet **Kopplas till ver.nr.** alltid i.

Förutom registrering att betalning har gjort kan du också använda fönstret **betalningsjournal** till att skapa betalningen för vidare behandling av din bank. Mer information finns i [Göra checkbetalningar](payables-how-work-checks.md) och [Göra elektroniska betalningar](payables-how-export-payments-bank-file.md).  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Utbetalningsjournal** och välj sedan relaterad länk.
2. Öppna den journal som ska användas för betalningar.
3. Om du vet vem som ska betala eller återbetalas, fyll i fälten manuellt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan också koppla betalningen till den relaterade fakturan eller kreditnotan, välj fältet **gäller för ver.nr** i fönstret**Koppla leverantörstrans**, välj relevant faktura eller kreditnota och tryck på knappen **OK**.

    Många fält såsom **belopp** och **förfallodatum** fylls nu i automatiskt med information från det markerade dokumentet.
5. Alternativt kan du använda funktionen **Betalningsförslag för lev.**. Alla som kopplas till information och belopp kommer sedan också anges på journalraderna. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).

    Meddelanden som hjälper dig att fylla i de obligatoriska fälten på rätt sätt.
6.  När alla betalningsjournalrader är ifyllda, välj åtgärden **Bokför**.

## <a name="see-also"></a>Se även
[Gör checkbetalning](payables-how-work-checks.md)  
[Gör elektroniska betalningar](payables-how-export-payments-bank-file.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Exportera en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


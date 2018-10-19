---
title: "Koppla betalningar till relaterade dokument och bokför dem | Microsoft Docs"
description: "Beskriver hur du kan registrera betalningar du gör till leverantörer och återbetalningar som du gör till kunder."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8f8db0bd6d12d4a633fe4ea33c732f231d798b3d
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrera betalningar och återbetalningar i betalningsjournalen

I fönstret **Betalningsjournal** registrerar du betalningar du gör till leverantörer och återbetalningar som du gör till kunder. När du bokför en utbetalningsjournalrad registreras det betalda beloppet för det angivna bankkontot. Du måste sedan vidta åtgärder för att utföra den faktiska överföringen pengar från relaterat bankkonto.  

Betalningsjournalen är en redovisningsjournal som är optimerad för att göra betalningar. Du kan snabbt skapa rader manuellt, låta [!INCLUDE[d365fin](includes/d365fin_md.md)] föreslå leverantörsbetalningar och du kan koppla betalningen till bokförda dokument. Även om du gör betalningar måste du ange ett positivt belopp i fältet **dokumentbelopp**. Beroende på dokumenttyp för journalraden omvandlas detta belopp till ett negativt belopp i de underliggande transaktionerna. På så sätt går det snabbare att lägga till journalraderna manuellt. Om du föredrar att ange negativa belopp kan du anpassa betalningsjournalen för att visa fältet **belopp** i stället.  

- Koppla betalningar till fakturor eller kreditnotor

    Om du fyller i fältet **Kopplas till ver.nr.** med den faktura eller kreditnotan som måste betalas ut eller återbetalas, är det aktuella dokumentet inställt att betalas när du bokför journalen. Det kallas för "kopplad". Som ett alternativ till att använda under betalningsbokföring kan du använda fönstret **Koppla leverantörstrans** och **Koppla kundtransaktioner** när du har gjort bokföringen av betalningen. Mer information finns i tillhörande, t.ex. [Stämma av leverantörsbetalningar manuellt](payables-how-apply-purchase-transactions-manually.md).  

- Hämta föreslagna betalningar till leverantörer eller medarbetare 

    Funktionerna **Betalningsförslag för lev.** och **Betalningsförslag för anställd** hjälper dig att fylla i betalningsjournalraderna automatiskt enligt leverantörens prioritering och förfallodatum. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md). Med denna funktionen fylls fältet **Kopplas till ver.nr.** alltid i.  

- Skriva ut checkar och skicka betalningar elektroniskt till banken

    Förutom registrering att betalning har gjort kan du också använda fönstret **betalningsjournal** till att skapa betalningen för vidare behandling av din bank. Mer information finns i [Göra checkbetalningar](payables-how-work-checks.md) och [Göra elektroniska betalningar](payables-how-export-payments-bank-file.md).  

## <a name="to-make-payments-in-the-payment-journal"></a>Göra betalningar i betalningsjournal 

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Betalningsjournal** och välj sedan relaterad länk.
2. Öppna den journal som ska användas för betalningar.
3. Om du vet vem som ska betala eller återbetalas, fyll i fälten manuellt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan också koppla betalningen till den relaterade fakturan eller kreditnotan, välj fältet **gäller för ver.nr** i fönstret**Koppla leverantörstrans**, välj relevant faktura eller kreditnota och tryck på knappen **OK**.

    Många fält såsom **dokumentbelopp** och **förfallodatum** fylls nu i automatiskt med information från det markerade dokumentet.
5. Alternativt kan du använda funktionen **Betalningsförslag för lev.**. Alla som kopplas till information och belopp kommer sedan också anges på journalraderna. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).

    Meddelanden som hjälper dig att fylla i de obligatoriska fälten på rätt sätt.
6.  När alla betalningsjournalrader är ifyllda, välj åtgärden **Bokför**.

## <a name="see-also"></a>Se även
[Gör checkbetalning](payables-how-work-checks.md)  
[Gör elektroniska betalningar](payables-how-export-payments-bank-file.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Exportera en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


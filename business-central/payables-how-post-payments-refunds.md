---
title: Registrera betalningar och återbetalningar i betalningsjournalen
description: Läs om hur du registrerar betalningar som du gör till leverantörer och återbetalningar som du gör till kunder på sidan Betalningsjournal.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/09/2021
ms.author: edupont
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a><a name="record-payments-and-refunds-in-the-payment-journal"></a><a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrera betalningar och återbetalningar i betalningsjournalen

På sidan **Betalningsjournal** registrerar du betalningar du gör till leverantörer och återbetalningar som du gör till kunder. När du bokför en utbetalningsjournalrad registreras det betalda beloppet för det angivna bankkontot. Du måste sedan vidta åtgärder för att utföra den faktiska överföringen pengar från relaterat bankkonto.  

Betalningsjournalen är en redovisningsjournal som är optimerad för att göra betalningar. Du kan snabbt skapa rader manuellt, låta [!INCLUDE[prod_short](includes/prod_short.md)] föreslå leverantörsbetalningar och du kan koppla betalningen till bokförda dokument. Även om du gör betalningar måste du ange ett positivt belopp i fältet **dokumentbelopp**. Beroende på dokumenttyp för journalraden omvandlas detta belopp till ett negativt belopp i de underliggande transaktionerna. På så sätt går det snabbare att lägga till journalraderna manuellt. Om du föredrar att ange negativa belopp kan du anpassa betalningsjournalen för att visa fältet **belopp** i stället.  

- Koppla betalningar till fakturor eller kreditnotor

    Om du fyller i fältet **Kopplas till ver.nr.** med den faktura eller kreditnotan som måste betalas ut eller återbetalas, är det aktuella dokumentet inställt att betalas när du bokför journalen. Det kallas för "kopplad". Som ett alternativ till att använda under betalningsbokföring kan du använda sidan **Koppla leverantörstrans** och **Koppla kundtransaktioner** när du har gjort bokföringen av betalningen. Mer information finns i t. ex. [Stäm av leverantörsbetalningar med betalningsjournalen eller från bokförda leverantörsreskontratransaktioner](payables-how-apply-purchase-transactions-manually.md).  

- Hämta föreslagna betalningar till leverantörer eller medarbetare

    Funktionerna **Betalningsförslag för lev.** och **Betalningsförslag för anställd** hjälper dig att fylla i betalningsjournalraderna automatiskt enligt leverantörens prioritering och förfallodatum. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md). Med denna funktionen fylls fältet **Kopplas till ver.nr.** alltid i.  

- Skriva ut checkar och skicka betalningar elektroniskt till banken

    Förutom registrering att betalning har gjort kan du också använda sidan **betalningsjournal** till att skapa betalningen för vidare behandling av din bank. Mer information finns i [Göra checkbetalningar](payables-how-work-checks.md) och [Göra elektroniska betalningar](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a><a name="to-make-payments-in-the-payment-journal"></a><a name="to-make-payments-in-the-payment-journal"></a>Göra betalningar i betalningsjournal

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.
2. Öppna den journal som ska användas för betalningar.
3. Om du vet vem som ska betala, fyll i fälten manuellt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan också koppla betalningen till den relaterade fakturan eller kreditnotan, välj fältet **gäller för ver.nr** på sidan **Koppla leverantörstrans**, välj relevant faktura eller kreditnota och tryck på knappen **OK**.

    Många fält såsom **dokumentbelopp** och **förfallodatum** fylls nu i automatiskt med information från det markerade dokumentet.
5. Alternativt kan du använda funktionen **Betalningsförslag för lev.**. Alla som kopplas till information och belopp kommer sedan också anges på journalraderna. Mer information finns i [Föreslå leverantörsbetalningar](payables-how-suggest-vendor-payments.md).

    Meddelanden som hjälper dig att fylla i de obligatoriska fälten på rätt sätt.
6. När alla betalningsjournalrader är ifyllda, välj åtgärden **Bokför**.


## <a name="to-issue-a-refund-check"></a><a name="to-issue-a-refund-check"></a><a name="to-issue-a-refund-check"></a>Så här skickar du en återbetalningscheck

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Utbetalningsjournaler** och välj sedan relaterad länk.
2. I fältet **Dokumenttyp** väljer du **Återbetalning**.  
3. I fälet **Externt dokumentnr.** använd den här som referens för återbetalningsckecken (till exempel returordernummer).  
4. I fältet **Kontotyp** väljer du **Kund**.  
5. I fältet **Kontonr** väljer du kundens konto nummer som återbetalningschecken utfärdas till.  
6. Ange det belopp som ska återbetalas i fältet **Belopp**.  
7. I fältet **Motkontotyp** väljer du **Bankkonto**.  
8. I fältet **Motkontonr.** välj bankkontot som checken kommer från.  
9. I fältet **Kopplas till ver.nr.** väljer du de dokument som kräver en återbetalning.  
10. När alla utbetalningsjournalrader är slutförda, välj åtgärden **Bokför/skriv ut** och välj åtgärden **Bokför och skriv ut** och välj **Ja**.  
  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även
[Gör checkbetalning](payables-how-work-checks.md)  
[Gör elektroniska betalningar](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Exportera en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

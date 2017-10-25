---
title: "Koppla betalningar till obetalda försäljningsdokument | Microsoft Docs"
description: "Du tillämpar belopp betalda av kunder till relaterade försäljningsdokument och bokför betalningen för att uppdatera kund, redovisning och banktransaktioner."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 94055c34b67f05faa8955fdff28f854e77d9664f
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-customer-payments-manually-from-a-list-of-unpaid-sales-documents"></a>Så här stämmer du av kundutbetalningar manuellt från en lista med obetalda försäljningsdokument
När kunderna har gjort betalningar till ditt elektroniska bankkonto, måste du koppla varje betalt belopp till det relaterade försäljningsdokumentet och sedan bokföra betalningen för att uppdatera kund-, redovisnings- och banktransaktioner.

> [!NOTE]  
>   Du kan utföra samma uppgifter inklusive leverantörsbetalningar i fönstret **Utbetalningavstämningsjournal** med hjälp av funktioner för bankutdragsimport, automatiskt koppling och bankkontoavstämning. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

Fönstret **Betalningsregistrering** fungerar som stöd för dig i uppgifter vid hantering av interna konton, genom att använda faktiska kassasiffror för att kontrollera att betalningar samlas in effektivt från kunder. Med betalningsbehandlingsverktyget kan du snabbt validera och bokföra enskilda betalningar eller betalningar av klumpsumma, bearbeta rabatterade betalningar och hitta obetalda dokument för vilka betalning görs.

Betalningar för olika kunder som har olika betalningsdatum, ska bokföras som individuella betalningar. Betalningar till samma kund som har samma betalningsdatum, kan bokföras som en klumpbetalning. Det är användbart, till exempel, när en kund har skapat en enkel betalning som täcker åtskilliga försäljningsfakturor.

## <a name="to-set-up-the-payment-registration-journal"></a>Så här lägger du upp betalningsregistreringjournal
Eftersom du kan bokföra olika betalningstyper till olika motkonton måste du välja ett motkonto i fönstret **Inställning av betalningsregistrering** innan du börjar att behandla kundbetalningar. Om du alltid bokför samma motkonto, kan du ange det konto som standard och undvika detta steg varje gång som du öppnar fönstret **Betalningsregistrering**.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inställning av betalningsregistrering**, och välj sedan relaterad länk.

    Alternativt kan du i fönstret **Betalningsregistrering** välja åtgärden **Inställning**.    
2. Fyll i fälten i fönstret **Inställning av betalningsregistrering**. Välj ett fält om du vill få en kort beskrivning av fältet eller länken till relaterad information.  

## <a name="to-reconcile-payments-individually"></a>Så här stämmer du av betalningar individuellt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.  
2. Markera kryssrutan **Utförd betalning** på raden som representerar bokfört dokument som en betalning har gjorts för.

    Om kryssrutan **Fyll i Tillbaka datum automatiskt** är markerad i fönstret **Inställning av betalningsregistrering** anges arbetsdatumet i fältet **Tillbaka datum**.  
3. I fältet **Tillbaka datum** anger du datumet då betalningen gjordes. Det datum kan skilja sig från arbetsdatumet.  
4. I fältet **Inlevererat belopp** anger du beloppet som har betalats.

    För fullständiga betalningar är detta samma som beloppet i fältet **Återstående belopp** på raden. För delbetalningar är detta lägre än beloppet i fältet **Återstående belopp** på raden.    
5. Upprepa steg 2–4 för andra rader som representerar bokförda dokument som betalningar har gjorts för.  
6. Välj åtgärden **Bokför betalningar**.  

Den angivna betalningsinformationen bokförs för de dokument som representeras av rader där kryssrutan **Utförd betalning** är markerad.  

Betalningstransaktioner bokförs på redovisningskonton, bankkonton och kundkonton. Varje betalning kopplas till det relaterade bokförda försäljningsdokumentet.  

## <a name="to-reconcile-lump-payments"></a>Stämma av betalning av klumpsumma
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.
2. Markera kryssrutan **Utförd betalning** på raderna som representerar bokförda dokument för samma kund som en klumpbetalning har gjorts för.  

    > [!NOTE]  
>   Kunden i **Namn** fältet måste vara samma på alla rader som ska bokföras som en betalning av klumpsumma.  

    Om kryssrutan **Fyll i Tillbaka datum automatiskt** är markerad i fönstret **Inställning av betalningsregistrering** fylls arbetsdatumet i fältet **Tillbaka datum**.  
3. I fältet **Tillbaka datum** anger du datumet då betalningen gjordes. Det datum kan skilja sig från arbetsdatumet.  

    > [!NOTE]  
>   Detta datum måste vara samma på alla rader som ska bokföras som en betalning av klumpsumma.  
4. Ange belopp på flera rader som summerar klumpbetalningsbeloppet i fältet **Inlevererat belopp**.  

    > [!TIP]  
>   Försök att bokföra så många fullständiga betalningar som möjligt med klumpsumman. Ange belopp som är samma som beloppet i fältet **Återstående belopp** på så många rader som möjligt.  
5. Upprepa steg 2–4 för andra rader som representerar bokförda dokument för samma kund som en klumpbetalning har gjorts för.  
6. Välj åtgärden **Bokför som en betalning av klumpsumma**. Den angivna betalningsinformationen bokförs för de dokument som representeras av rader där kryssrutan **Utförd betalning** är markerad.  

Betalningstransaktioner bokförs på redovisningskonton, bankkonton och kundkonton. Varje betalning kopplas till det relaterade bokförda försäljningsdokumentet.  

Om en betalning i banken inte representeras av raden i fönstret **Betalningsregistrering** kan det bero på att det relaterade dokumentet inte har bokförts. I så fall kan du använda en sökfunktion för att snabbt hitta dokument och bokföra det för att behandla betalningen. Mer information finns i avsnittet ”Att söka efter ett visst försäljningsdokument som inte har fakturerats helt”.  

Om en betalning i banken inte representeras av ett dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du öppna en förifylld redovisningsjournalsrad från fönstret **Betalningsregistrering** för att bokföra betalningen direkt till motkontot, utan att koppla betalningen till ett dokument. Du kan också vilja registrera betalning i journalen tills ursprunget för betalningen har fastställts. Mer information finns i avsnittet "Så här registrerar eller bokför du en betalning utan ett relaterat dokument".  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Så här behandlar du betalningar med rabatter manuellt
Om du har kommit överens om en kassarabatt med kunden, kan betalningsbeloppen bli lägre än fakturabeloppen, om betalning sker före det överenskomna kassarabattsdatumet.  

Följande procedur förklarar fyra olika sätt att bokföra rabatterade betalningar i fönstret **Betalningsregistrering**.  

* Beloppet är lika med det återstående rabatterade beloppet, och betalningsdatumet infaller före kassarabattsdatum. Du bokför betalningen som är.  
* Beloppet är lika med det återstående rabatterade beloppet, men betalningsdatumet infaller efter kassarabattsdatum. Du bokför betalningen som del. Dokumentet förblir öppen för att kräva/betala det återstående beloppet. Alternativt kan du ange ett senare rabattdatumet för att tillåta betalning i sin helhet.  
* Betalningsbeloppet är lägre än återstående rabatterade beloppet. Du bokför betalningen som del. Dokumentet förblir öppen för att kräva/betala det återstående beloppet.  
* Betalningsbeloppet är högre än återstående rabatterade beloppet. Du bokför betalningar som är. Endast det återstående beloppet bokförs. Det extra belopp krediteras till kunden.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Processa ett betalningsbelopp som är lika med det rabatterade beloppet, och där betalningsdatumet infaller före kassarabattsdatum.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.  
2. Ange betalningsbeloppet i fältet **Inlevererat belopp**. Beloppet är lika med beloppet i fältet **Återstående belopp efter rabatt**.

    Kryssrutan **Utförd betalning** markeras automatiskt, och fältet **Tillbaka datum** fylls i med arbetsdatumet.    
3. Ange betalningsdatumet i fältet **Tillbaka datum**. Datumet är före datumet i fältet **Kassarabattsdatum**.
4. Kontrollera att fältet **Återstående belopp** innehåller värdet noll (0).  
5. Välj åtgärden **Bokför betalningar** för att bokföra den fullständiga betalningen på redovisningskonto bankkontot eller kundkontot.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Processa ett betalningsbelopp som är lika med det rabatterade beloppet, men där betalningsdatumet infaller efter kassarabattsdatumet
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.  
2. Ange betalningsbeloppet i fältet **Inlevererat belopp**. Beloppet är lika med beloppet i fältet **Återstående belopp efter rabatt**.

    Kryssrutan **Utförd betalning** markeras automatiskt, och fältet **Tillbaka datum** fylls i med arbetsdatumet.
3. I fältet **Tillbaka datum** anger du ett betalningsdatum som är efter datumet i fältet **Kassarabattsdatum**. Datumfält ändras till det röda teckensnittet, och ett felmeddelande visas längst ned i fönstret.

    > [!TIP]  
>   Om du vill göra ett undantag och hur bevilja rabatt, även om betalningen är sen, följ de här stegen:
4. Välj åtgärden **Detaljer**.  
5. I fönstret **Information om betalningsregistrering** i fältet **Kassarabattsdatum** på snabbfliken **Kassarabatt** anger du ett datum som är efter datumet i fältet **Tillbaka datum** i fönstret **Betalningsregistrering**.  

    Felmeddelande och den röda teckensnittet försvinner, och du kan fortsätta att bearbeta rabatterade betalningen.    
6. Kontrollera att fältet **Återstående belopp** innehåller det belopp som återstår att betala av det helt fakturerade beloppet.  
7. Välj åtgärden **Bokför betalningar** för att bokföra delbetalning på redovisningskontot, bankkontot eller kundkontot.  

Det relaterade dokument förblir öppen.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Processa en betalning som är lägre än återstående rabatterade beloppet
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.  
2. Ange betalningsbeloppet i fältet **Inlevererat belopp**. Beloppet är lägre än beloppet i fältet **Återstående belopp efter rabatt**.

    Kryssrutan **Utförd betalning** markeras automatiskt, och fältet **Tillbaka datum** fylls i med arbetsdatumet.  
3. Ange betalningsdatumet i fältet **Tillbaka datum**. Datumet är före datumet i fältet **Kassarabattsdatum**.
4. Kontrollera att fältet **Återstående belopp** innehåller det belopp som återstår att betala av det rabatterade beloppet.  
5. Välj åtgärden **Bokför betalningar** för att bokföra delbetalning på redovisningskontot, bankkontot eller kundkontot.  

Det relaterade dokument förblir öppen.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Processa en betalning som är högre än återstående rabatterade beloppet
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.  
2. Ange betalningsbeloppet i fältet **Inlevererat belopp**. Beloppet är högre än beloppet i fältet **Återstående belopp efter rabatt**.  

    Kryssrutan **Utförd betalning** markeras automatiskt, och fältet **Tillbaka datum** fylls i med arbetsdatumet.    
3. Ange betalningsdatumet i fältet **Tillbaka datum**. Datumet är före datumet i fältet **Kassarabattsdatum**.
4. Kontrollera att fältet **Återstående belopp** innehåller värdet noll (0).  
5. Välj åtgärden **Bokför betalningar** för att bokföra den fullständiga betalningen på redovisningskonto bankkontot eller kundkontot.  

Det relaterade dokument stängs och kunden krediteras för överskottsbeloppet.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Om du vill hitta ett visst försäljningsdokument som inte har fakturerats helt
Fönstret **Betalningsregistrering** fungerar som stöd för dig i uppgifter som krävs för balansering av interna konton, genom att använda faktiska kassasiffror, för att kontrollera den effektiva samlingen från kunder och förfallna betalningar till leverantörer. Visar utestående inkommande betalningar som rader som representerar försäljningsdokument, där ett belopp har förfallit till betalning.  

Vanligtvis när en betalning har utförts, registrerats i banken eller liknande, representeras det relaterade försäljnings- eller inköpsdokumentet av en rad i fönstret **Betalningsregistrering** eftersom dokumentet i fråga väntar på att betalningen bokförs mot utestående belopp. Dock ibland motsvaras en betalning som har utförts inte av en rad i fönstret **Betalningsregistrering** vanligtvis eftersom dokumentet i fråga inte helt har fakturabokförts.

I fönstret **Dokumentsökning** kan du söka bland dokument som inte har fakturerats helt. Du kan söka baserat på en eller flera av följande kriterier:  

* Dokumentnummer  
* Belopp eller beloppsintervall  

Följande procedurer beskriver hur du hittar ett visst dokument, genom att använda både sökkriterier.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.
2. Välj avsnittet **Sök dokument** med pekaren på någon av raderna.
3. I fönstret **Dokumentsökning** anger du ett sökvärde i fältet **Dokumentnr.**  

    > [!NOTE]  
>   Värdet som du anger i detta fält, omsluts i gömda jokertecken. Det betyder att funktionen söker efter alla verifikationsnummer som innehåller det angivna värdet.    
4. I fältet **Belopp** anger du det specifika belopp som finns på den öppna dokument, som du vill hitta.  
5. Ange ett procentsatsvärde för att definiera intervallet av belopp som du vill söka för att hitta den öppna dokumentet i fältet **Beloppstolerans i %**.  

    Om du anger 10, kommer funktionen söka efter belopp i intervallet tio procent lägre och tio procent högre än värdet i fältet **Belopp**.    
6. Välj åtgärden **Sök**.  

Sökfunktionen söker bland dokument som inte är fullständigt fakturerade baserat på de angivna kriterier.  

Om ett eller flera dokument matchar sökkriterierna, öppnas fönstret **Dokumentsökningsresultat** och visar raderna som motsvarar de dokument. Varje rad innehåller ett verifikationsnummer, en beskrivning och ett belopp, så att du lätt kan hitta ett visst dokument, till exempel baserad på information i ditt bankkontoutdrag.  

Om en betalning i banken inte representeras av ett dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du öppna en förifylld redovisningsjournalsrad från fönstret **Betalningsregistrering** för att bokföra betalningen direkt till motkontot, utan att koppla betalningen till ett dokument. Du kan också vilja registrera betalning i journalen tills ursprunget för betalningen har fastställts.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Så här registrerar eller bokför du en betalning utan ett relaterat dokument
Om en betalning i banken inte representeras av ett dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du öppna en förifylld redovisningsjournalsrad från fönstret **Betalningsregistrering** för att bokföra betalningen direkt till motkontot, utan att koppla betalningen till ett dokument. Du kan också vilja registrera betalning i journalen tills ursprunget för betalningen har klargjorts.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Betalningsregistrering**, och välj sedan relaterad länk.  

Fortsätt med att registrera en odokumenterad betalning.  

1. Välj åtgärden **Redovisningsjournal**.  

    Fönstret **Redovisningsjournal** öppnas med en förifylld rad med motkonton i journalen som ställs in i fönstret **Inställning av betalningsregistrering**.  
2. Fyll i de återstående fälten på redovisningsjournalraden, till exempel kundnummer eller belopp och annan information från kontoutdraget. Mer information finns i [Så här bokför du transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md).  

Du kan bokföra journalraden för att uppdatera summan på motkontot. Alternativt kan du lämna journalraden obokförd och eventuellt koppla den till en kommentar om att betalningen behöver mer analys.  

Om du lämnar journalraden obokförd, adderas det till värdet i fältet **Ej bokförd balans** längst ned i fönstret **Betalningsregistrering**.  

## <a name="see-also"></a>Se även
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


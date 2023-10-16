---
title: Omvärdera anläggningstillgångar
description: 'Lär dig att justera värdet för anläggningstillgångar, registrera nya belopp eller uppskrivning, nedskrivning och bokföra ytterligare anskaffningskostnader.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5628, 5629, 5633'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Omvärdera anläggningstillgångar

Omvärdering av anläggningstillgångar kan bestå av uppskrivning, nedskrivning, eller allmänna värdejusteringar.

När värdet av en anläggningstillgång har ökat, bokför du en journalrad med ett högre belopp, en uppskrivning, till avskrivningsregeln. Det nya beloppet registreras som en uppskrivning enligt bokföringsinställningarna för anläggningstillgångar.

När värdet av en anläggningstillgång har minskat, bokför du en journalrad med ett lägre belopp, en nedskrivning, till avskrivningsregeln. Det nya beloppet registreras som en nedskrivning enligt bokföringsinställningarna för anläggningstillgångar.

Indexering används för att anpassa flera värden för anläggningstillgångar, t. ex. per allmänna prisändringar. Du kan använda batch-jobbet **Indexera anläggningstillgångar** när du vill ändra olika belopp, till exempel nedskrivnings- och uppskrivningsbelopp.

## Att bokföra uppskrivning från en redovisningsjournal.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov.
3. I fältet **Anskaffningskostnad** väljer du **Omvärdering**.
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av uppskrivning.

    > [!NOTE]  
    >   Steg 4 fungerar bara om du har ställt in följande: På sidan **Anl.bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Uppskrivningskonto** redovisningsdebitkontot och fältet **Uppskrivning motkonto** innehåller det redovisningskonto där du vill bokföra mottransaktioner för uppskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Välj åtgärden **Bokföra**.

## Att bokföra en nedskrivning från en redovisningsjournalen för anläggningstillgångar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.  
2. Skapa en första journalrad och fyll i fälten efter behov.
3. Välj **Anskaffningskostnad** i fältet **nedskrivning**.
4. Välj åtgärden **Infoga anl. motkonto**. En andra journalrad skapas för motkontot som ställs in för bokföring av nedskrivning.

    > [!NOTE]  
    >   Steg 4 fungerar bara om du har ställt in följande: På sidan **Anl.bokföringsmallkort** för den fasta anläggningstillgångens bokföringsmall, innehåller fältet **Nedskrivningskonto** redovisningskreditkontot och fältet **Nedskrivningskostnadskontot** innehåller det redovisningskonto där du vill bokföra mottransaktioner för nedskrivning. Mer information finns i [Så här skapar du bokföringsmallar för anläggningstillgångar](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Välj åtgärden **Bokföra**.

## Om du vill utföra allmän omvärdering av anläggningstillgångar

Indexering används för att anpassa flera värden för anläggningstillgångar, t. ex. per allmänna prisändringar. Du kan använda batch-jobbet **Indexera anläggningstillgångar** när du vill ändra olika belopp, till exempel nedskrivnings- och uppskrivningsbelopp. Kryssrutan **Tillåt indexering** p sidan **Avskrivningsregel** måste väljas.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Indexera anläggningstillgångar** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.
3. Välj **OK**.

    Omvärderingrader skapas per dina inställningar i steg 2. Raderna skapas antingen i anläggningstillgångsjournalen eller i redovisningsjournalen för anläggningstillgångar beroende på dina mallar och batch-inställning på sidan **Anl. journalinställningar**. Mer information finns i [Ställa in allmän information för anläggningstillgångar](fa-how-setup-general.md).
4. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Redovisningsjournaler för anl.tillg.** och väljer sedan relaterad länk.  
5. Markera journalen med de anläggningstillgångar som du vill omvärdera och välj sedan åtgärden **Transaktioner**.  
6. Kontrollera skapade poster och välj sedan åtgärden **Bokför** för att bokföra journalen.

    > [!TIP]  
    >   Om indexsiffrorna endast är avsedda för simulering kan du skapa en särskild avskrivningsregel där du kan lagra dem. På så sätt påverkar de här transaktionerna inte de övriga avskrivningsreglerna.

## Att bokföra ytterligare anskaffningskostnader

Du bokför ytterligare anskaffningskostnader för en anläggningstillgång på samma sätt som du bokför den ursprungliga anskaffningskostnaden, d.v.s.från en inköpsfaktura eller från en journal för anläggningstillgångar. Mer information finns i [Så här anskaffar du anläggningstillgångar](fa-how-acquire.md).  

Om avskrivningen redan har beräknats för anläggningstillgången markerar du kryssrutan **Avskr. Anskaffningskostnad** så att den tillkommande anskaffningskostnaden är mindre än det återanskaffningsvärde som avskrivs i proportion till det belopp som de tidigare anskaffade anläggningstillgången redan har avskrivits med. Detta garanterar att avskrivningsperioden inte ändras.  

Avskrivningsprocentsatsen beräknas som:  

*P = (total avskrivning × 100) / avskrivningsbas*

*Avskrivningsbelopp = (P/100) × (extra anskaffningskostnad – återanskaffningsvärde)*  

Kom ihåg att markera kryssrutan **Avskr. till Anl.bokf.datum** på fakturan, redovisningsjournalen för anläggningstillgångar eller anläggningstillgångsjournalraderna så att avskrivningen beräknas från det senaste bokföringsdatumet för anläggningstillgången till bokföringsdatumet för den tillkommande anskaffningskostnaden.

### Exempel – bokföra ytterligare anskaffningskostnader

En maskin införskaffas den 1 augusti, 2000. Anskaffningskostnader är 4 800. Avskrivningsmetoden är linjär över fyra år.

Den 31 augusti, 2000 körs batch-jobbet **Beräkna avskrivning**. Avskrivningen beräknas som:

*bokföringsvärde x antal avskrivningsdagar/totalt antal avskrivningsdagar = 4800 x 30 / 1440 = 100*  

Den 15 september, 2000 bokförs en faktura för ommålning av maskinen. Fakturabeloppet är 480.

Om du har markerat kryssrutan **Avskr. till Anl.bokf.datum** med ett "x" på fakturan innan du bokför transaktionen utförs följande beräkning:  

15 avskrivningsdagar (från 00-09-01 till 00-09-15) beräknas så här:

*bokföringsvärde x antal avskrivningsdagar/återstående antal avskrivningsdagar = (4800 – 100) x 15 / 1410 = 50*

Om du har markerat kryssrutan **Avskr. anskaffningskostnad** med ett "x" på fakturan innan du bokför transaktionen utförs följande beräkning:  

*Den tillkommande anskaffningskostnaden avskrivs med ((150 x 100) / 4800) / 100 x 480 = 15*

Avskrivningsbasen är nu *5280 = (4800 + 480)* och den ackumulerade avskrivningen är *165 = (100 + 50 + 15)* vilket motsvarar 45 avskrivningsdagar för den totala anskaffningskostnaden. Detta innebär att tillgången helt är avskriven inom den beräknade livslängden på fyra år.  

När batch-jobbet **Beräkna avskrivning** körs på 09/30/00 används följande beräkning:  

*Återstående avskrivningstid är 3 år, 10 månader och 15 dagar = 1395 dagar*  

*Bokföringsvärdet är (5280 – 165) = 5115*  

*Avskrivningsbeloppet för september 2000: 5115 x 15 / 1395 = 55,00*  

*Summan av avskrivningen = 165 + 55 = 220*  

Om du inte har markerat kryssrutan **Avskr. till Anl.bokf.datum** förlorar tillgången 15 avskrivningsdagar eftersom batch-jobbet **Beräkna avskrivning** som körs 00-09-30 beräknar avskrivningen från 00-09-15 till 00-09-30. Detta innebär att följande beräkning utförs när batch-jobbet **Beräkna avskrivning** körs 00-09-30:  

*Återstående livslängd är 3 år, 10 månader och 15 dagar = 1395 dagar*  

*Bokföringsvärdet är (4800 + 480 – 100 – 15) = 5165*

*Avskrivningsbeloppet för september 2000: 5165 x 15 / 1395 = 55,54*  

*Summan av avskrivningen = 100 +15 + 55,54 = 170,54*

## Se även

[Anläggningstillgångar](fa-manage.md)  
[Ställa in anläggningstillgångar](fa-setup.md)  
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

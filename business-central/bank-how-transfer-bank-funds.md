---
title: Överföra banktillgångar
description: 'Du kan överföra belopp från ett bankkonto, till exempel olika valutor genom att bokföra transaktionen i redovisningsjournalen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Överföra banktillgångar

Du kan ibland komma att behöva överföra ett belopp från ett bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] till ett annat. För att göra detta måste du bokföra en transaktion på sidan **Redovisningsjournal**. Uppgiften varierar beroende på om bankkontona använder samma valuta eller olika valutor.

## Så här bokför du en överföring mellan bankkonton med samma valutakod

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournal** och väljer sedan relaterad länk.
2. Fyll i fälten **Bokföringsdatum** och **Verifikationsnr** på en .
3. Ange **Bankkonto** i fältet **Kontotyp**.
4. I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.
5. Ange det belopp som ska överföras i fältet **Belopp**.

    Sedan måste du ange balanskontot. Om du inte kan se de relevanta fälten kan du välja åtgärden **Visa fler kolumner** för att visa alla tillgängliga fält.
6. I fältet **Motkontotyp** väljer du **Bankkonto**.
7. I fältet **Balanskontonr** väljer du det bankkonto som du vill överföra pengarna till.
8. Bokför journalen.

## Så här bokför du överföringar mellan bankkonton med olika valutakoder

För att överföra pengar mellan bankkonton som använder olika valutor måste du bokföra två redovisningsjournalrader.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournal** och väljer sedan relaterad länk.
2. Skapa två journalrader och fyll i fälten **Bokföringsdatum** och **Verifikationsnr**.
3. På den första journalraden anger du **Bankkonto** i fältet **Typ**.
4. I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna från.
5. I fältet **Belopp** anger du beloppet i samma valuta som bankontot, med eller utan minustecken.

    > [!TIP]
    > Ett belopp utan ett tecken är ett debetbelopp och ett belopp med ett minustecken är ett kreditbelopp.

    > [!NOTE]
    > Vissa företag föredrar att överföra mellan konton på separata journalrader. Andra företag föredrar att bokföra allt på en journalrad med hjälp av ett balanskonto. Hör med din lokala expert om du är osäker på vad du ska göra.
    >
    > Om företaget föredrar att använda ett balanskonto, ställer du in fältet **Balanskontotyp** till **Bankkonto** och ställer in fältet **Balanskontonummer** på det bankkonto som du vill överföra pengarna till. Gå sedan vidare till steg 9 eller 10.
    >
    > Om företaget föredrar att använda en separat journalrad går du vidare till nästa steg.
6. På den andra journalraden anger du **Bankkonto** i fältet **Typ**.
7. I fältet **Kontonr** väljer du det bankkonto som du vill överföra pengarna till.
8. I fältet **Belopp** anger du beloppet i samma valuta som bankontot, med eller utan minustecken.

    > [!TIP]
    > Ett belopp utan ett tecken är ett debetbelopp och ett belopp med ett minustecken är ett kreditbelopp.
9. Om de valutakurser som används i journalen inte är samma som valutakurserna på sidan **Valutakurser** skapar du en ny journalrad för valutakursvinsten eller valutakursförlusten.  

    1. Ange **Redovisningskonto** i fältet **Kontotyp**.  

    2. Ange numret för redovisningskontot för valutavinster och valutaförluster i fältet **Kontonr**.  

    3. Ange valutakursvinst eller -förlust i fältet **Belopp** med eller utan ett minustecken.

    > [!TIP]
    > Ett belopp utan ett tecken är ett debetbelopp och ett belopp med ett minustecken är ett kreditbelopp.
10. Bokför journalen.

## Se även

[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
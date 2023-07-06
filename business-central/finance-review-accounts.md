---
title: Granska redovisningskonton
description: Du kan följa upp förloppet när du granskar belopp på redovisningskonton.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
---

# <a name="review-amounts-in-general-ledger-accounts"></a><a name="review-amounts-in-general-ledger-accounts"></a><a name="review-amounts-in-general-ledger-accounts"></a>Granska belopp på redovisningskonton

Du kanske har tillgång till redovisningskonton som du ofta håller ett öga på. Du kanske vill påskynda granskningsarbetet i slutet av månaden. Om du vill ha hjälp med att hålla reda på vad du har gjort och förbättra granskningen kan du använda åtgärden **granska poster** på sidan **kontoplanen** eller **redovisningskontokort** för varje konto. 

## <a name="set-up-accounts-for-reviews"></a><a name="set-up-accounts-for-reviews"></a><a name="set-up-accounts-for-reviews"></a>Skapa konton för granskningar

På sidan **Redovisningskontokort** för varje konto anger du hur du vill tillåta granskningar i fältet **Granska policy**.

|Granska princip  |Beskrivning  |
|---------|---------|
|Ingen     | Du kan inte markera poster för kontot som granskade. Du kan t.ex. använda det här alternativet för leverantörsreskontra, kundreskontra och bankkonton, där det finns andra sätt att granska deras belopp.        |
|Tillåt granskning     | Du behöver inte ta med transaktionerna i en granskning, och beloppen i debet- och kredittransaktionerna behöver inte balansera. Du tar bort en granskning, till exempel om du har gjort fel.        |
|Tillåt granska och matcha saldo     | De totala beloppen för debet- och kredittransaktionerna i granskningen måste stämma överens. Fälten **Debit** och **Kredit** visar dessa belopp och fältet **Saldo** visar summan. Med den här inställningen kan du också ta bort en granskning. När du tar bort en granskning från en eller flera transaktioner, måste debet- och kredittransaktionerna fortfarande balansera.        |

## <a name="mark-entries-as-reviewed"></a><a name="mark-entries-as-reviewed"></a><a name="mark-entries-as-reviewed"></a>Markera poster som granskade

Välj de poster som du har granskat och använd sedan åtgärden **Ange den valda som granskad**. Varje gång du markerar en eller flera poster som granskade får posterna samma nummer i kolumnen **Granskningsidentifieraren**. Granskningsidentifieraren är ett praktiskt sätt att hålla reda på de transaktioner som granskades samtidigt. [!INCLUDE [prod_short](includes/prod_short.md)] registrerar också den användare som gjorde granskningen och när de gjorde det.

Om du markerar poster som granskade, men ångrar dig, använder du åtgärden **Ange den valda som inte granskad**.

* Om den tillåtna principen har tilldelats kontot återställer åtgärden den granskade identifieraren till 0 och tar bort personen och datumet och tiden för granskningen. 
* Om principen för tillåten och matcha saldo är tilldelad, måste krediten och debet fortfarande vara balanserade. Om t.ex. en av posterna i en granskning är av misstag kan du välja en annan post med rätt värde. Ersättningstransaktionen behöver inte ha samma granskade identifierare.

> [!TIP]
> Ett snabbt sätt att välja flera poster är att hålla ned Ctrl eller Shift medan du väljer posterna. Med Ctrl kan du välja vissa poster och sedan markera alla poster mellan de första och sista transaktionerna som du väljer.

## <a name="review-accounts-that-have-old-entries"></a><a name="review-accounts-that-have-old-entries"></a><a name="review-accounts-that-have-old-entries"></a>Granska konton som har gamla poster

Det kan hända att du har transaktioner från tidigare perioder som du redan har granskat eller inte behöver en recension. Du vill bara börja granska transaktioner från exempelvis början av året eller bokföringsperioden. Du kan lämna transaktionerna som de är. Om du vill analysera data i Excel eller i analysläge markerar du posterna som granskade. Om du vill veta mer om att analysera transaktioner, gå till [analysera transaktioner](#analyze-entries). Om du vill markera posterna som granskade lägger du till ett filter i filter rutan så att endast transaktionerna visas, och väljer sedan åtgärden **Markera valda poster som granskade**.

## <a name="filter-entries"></a><a name="filter-entries"></a><a name="filter-entries"></a>Filtrera transaktioner

För att få en tydligare bild finns det flera sätt att filtrera poster på **Granska redovisningstransaktioner**.

* Använd åtgärden **Visa granskade poster** och **Dölj granskade poster** om du endast vill visa de poster som du har eller inte har granskat. Ta bort filtren med hjälp av åtgärden **Visa alla poster**.
* Använd filterruta. Du kan t.ex. filtrera efter kontonummer eller, om du har äldre transaktioner och vill markera dem som granskade, med ett bokföringsdatum.

## <a name="analyze-entries"></a><a name="analyze-entries"></a><a name="analyze-entries"></a>Analysera transaktioner

Du kan analysera redovisningstransaktionerna som du har granskat på ett par olika sätt.

* Aktivera analysläget om du till exempel vill gruppera poster enligt deras granskade identifierare. Om du vill veta mer om analysläget går du till [Analysera data i listsidor med hjälp av dataanalysläge](analysis-mode.md).
* Exportera transaktioner till Excel.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Förstå huvudboken och kontoplanen](finance-general-ledger.md)  
[Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md)  

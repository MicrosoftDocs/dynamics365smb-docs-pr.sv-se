---
title: "Översikt över uppgifter för hantering av leverantörsskulder | Microsoft Docs"
description: "Innehåller information om hur du hanterar leverantörsreskontra, till exempel betala fordringsägare eller koppla utgående betalningar till transaktioner för att stänga fakturor eller kreditnotor."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 11/15/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9bc4eaf292c20c1525c499cde715964eb6e6631f
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="managing-payables"></a>Hantera Leverantörsreskontra

En stor del av hanteringen av leverantörsskulder betalar dina leverantörer eller återbetalar dina anställda för utgifter. Du kan använda funktioner för att lägga till betalningsrder för inköpsfakturor som förfaller till betalning på sidan **Betalningsjournal**. För att skicka transaktioner till din bank kan du exportera flera betalningsjournalrader till en fil och sedan överför du filen till din bank. Du kan också göra betalningar med check som inkluderar att överföra checkar som elektronisk betalning.

En annan typisk aktivitet är att koppla utgående betalningar till deras relaterade leverantörers eller anställdas transaktioner för att avsluta de inköpsfakturor, inköpskreditnotor eller anställdas konton som betalda. Du kan göra detta på sidan **Betalningsavstämningsjournal** genom att importera ett kontoutdrag för att snabbt registrera utbetalningarna. Betalningarna används för att öppna leverantörs-, kund- eller anställdas transaktioner genom att matcha betalningstexten och transaktionsinformation. Det finns olika sätt att visa och ändra matchningarna innan du bokför journalen. Du kan välja att avsluta alla öppna bankkontotransaktioner som relateras till kopplade transaktioner, när du bokför journalen. Bankkontot avstäms automatiskt, när alla utbetalningar kopplas.

Du kan också koppla utgående betalningar manuellt på sidan **Betalningsjournal** eller från relaterade leverantörers eller anställdas transaktioner.

I följande tabell beskrivs en serie uppgifter inom Leverantörsskulder med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| Generera förfallna leverantörsbetalningar eller återbetalningar till anställda, förbereda checkbetalningar och exportera betalningar till en bankfil när du bokför. |[Göra betalningar](payables-make-payments.md) |
| Koppla leverantörsbetalningar automatiskt till obetalda inköpsfakturor, genom att importera bankutdragsfil. |[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Ställ in mappningar mellan text på betalningar och specifika debet-, kredit- och balanskonton så att sådana betalningar bokförs på de angivna kontona när du bokför betalningar i betalningsavstämningsjournalen.|[Så här mappar du text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
| Koppla leverantörsbetalningar till obetalda inköpsfakturor manuellt. |[Stämma av leverantörsbetalningar manuellt](payables-how-apply-purchase-transactions-manually.md) |
|Tillämpa automatiskt betalningar, antingen inkommande eller utgående, som har registrerats som transaktioner på ditt onlinebankkonto till deras motsvarande öppna kund-, leverantör- och bankkontotransaktioner. Listan skapas från en bankfeed eller en fil.|[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md)|
|Hantera manuellt betalningar till ditt bankkonto som inte kan göras automatiskt, till exempel, eftersom det inte finns några dokument som kan betalningen kan kopplas till eller relaterat dokument har ett annat belopp än transaktionsbeloppet på grund av en skillnad i valuta.|[Så här stämmer du av betalningar som inte kan kopplas automatiskt](receivables-how-reconcile-payments-cannot-apply-auto.md)|
|Säkerställa korrekt värdering av lager genom att tilldela extra artikelkostnader, som till exempel frakt, fysisk hantering, försäkring och transport som förekommer vid inköp.|[Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md)|
|Om du vill betala leverantören kontant eller med check kan du bokföra betalningen när du bokför fakturan.|[Betala inköpsfakturor snabbt](finance-how-to-settle-purchase-invoices-promptly.md)|
|Återbetala anställda för privata utgifter under affärsaktiviteter genom att göra betalningen till dennes bankkonto.|[Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


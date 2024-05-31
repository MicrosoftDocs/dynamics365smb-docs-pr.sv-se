---
title: Regler för automatisk koppling av betalningar
description: Läsa om hur du ställer in regler för automatisk koppling av betalningar på sidan betalningskopplingsregler.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Definiera regler för automatisk koppling av betalningar

På sidan **Regler för betalningskoppling** anger du regler som styr hur betalningstext (på en banktransaktion) automatiskt kopplas till text på relaterade öppna (obetalda) fakturor, kreditnotor eller andra poster när du använder funktionen **Koppla automatiskt** på sidan **Betalningsavstämningsjournal**. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

Du ställer in nya betalningskopplingsregler genom att välja vilka slags data på en rad i en betalningsavstämningsjournal som måste överensstämma med data på en eller flera öppna transaktioner innan den relaterade betalningen automatiskt kopplas till de öppna transaktionerna. Kvaliteten på respektive automatisk koppling visas som värdet **Låg** till **Hög** i fältet **Matchningssäkerhet** på sidan **Betalningsavstämningsjournal** i enlighet med använd regel för betalningskoppling.

Varje rad på sidan **Betalningskopplingsregler** representerar en betalningskopplingsregel. Regler kopplas i den ordning som anges i fältet **Sorteringsordning**. Om flera regler används samtidigt används matchningssäkerheten för den högst sorterade regeln.

Den automatiska kopplingsfunktionen baseras på prioriterade matchningskriterier. Först försöker funktionen, i prioriterad ordning, att matcha texten i de fem fälten **Relaterad part** på en journalrad med text i bankkontot, namnet eller adressen för kunder eller leverantörer med obetalda dokument som representerar öppna transaktioner. Funktionen försöker sedan matcha text i fälten **Transaktionstext** och **Ytterligare transaktionsinformation** på en journalrad med text i fälten **Externt dokumentnr.** och **Dokumentnr.** på öppna transaktioner. Till sist försöker funktionen matcha beloppet i fältet **Rapportbelopp** på en journalrad med beloppet på öppna transaktioner.

> [!NOTE]
> Textmatchning är endast möjligt för text längre än fyra tecken.

Utöver matchningsvillkoret gäller följande för tecknet för betalningsbeloppet:

- För negativa belopp görs först en matchning mot öppna transaktioner som representerar kundfakturor, och sedan mot kreditnotor för leverantören.
- För positiva belopp görs först en matchning mot öppna transaktioner som representerar leverantörsfakturor, och sedan mot kreditnotor för kunden.

## Så här definierar du en regel för betalningskoppling
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningskopplingsregler** och väljer sedan relaterad länk.
2. Definiera en ny eller redigerad betalningskopplingsregel genom att fylla i fälten på en rad enligt beskrivningen i följande register.

|Fält|Beskrivning|
|-|-|
|**Matchningssäkerhet**|Anger hur mycket du förlitar dig på kopplingsregeln som du definierar på raden. <br /></br>Ett värde som du anger i det här fältet visas i fältet **Matchningssäkerhet** på sidan **Betalningsavstämningsjournal** enligt kvaliteten på den automatiska betalningskopplingen på journalraden.|
|**Prioritet**|Anger prioriteten för kopplingsregeln i förhållande till andra kopplingsregler som är definierade som rader på sidan **Regler för betalningskopplingar**. 1 motsvarar den högsta prioriteten.|
|**Matchad relaterad part**|Anger hur mycket information om kunden eller leverantören på betalningsavstämningsjournalraden – till exempel adress, ort och bankkontonummer – som måste matcha information om den öppna transaktionen för att kopplingsregeln ska användas för att automatiskt koppla betalningen till den öppna transaktionen.|
|**Matchat dok.nr/externt dok.nr**|Anger huruvida texten på raden i betalningsavstämningsjournalen måste matcha värdet i fältet **Dokumentnr.** eller fältet **Externt dokumentnr.** i den öppna transaktionen innan kopplingsregeln kan användas för att automatiskt koppla betalningen till den öppna transaktionen.|
|**Matchat belopp inkl. tolerans**|Anger hur många transaktioner för en kund eller leverantör som måste överensstämma med beloppet inklusive betalningstolerans innan kopplingsregeln används för att automatiskt koppla en betalning till den öppna transaktionen.|
|**Granskning krävs**|Anger om det automatiska betalningsprogrammet rekommenderas för manuell granskning av användaren före bokföring. Om du väljer fältet **Rader att granska** på sidan **Betalningskopplingsjournal** startar du en guidad upplevelse där du enkelt kan granska flera ansökningar i en sekvens på sidan **Granskning av betalningskoppling**.|

I följande tabell beskrivs standardreglerna för betalningsansökan i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Important]
> Betalningskopplingsreglerna kan vara olika i din implementering av [!INCLUDE[prod_short](includes/prod_short.md)].

| Matchningssäkerhet | Prioritet | Matchad relaterad part | Dok.nr/externt dok.nr. Matchningar | Matchat belopp inkl. tolerans |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Högt             | 1        | Helt                 | Ja – Flera                 | En matchning                      |
| Högt             | 2        | Helt                 | Ja – Flera                 | Flera matchningar               |
| Högt             | 3        | Helt                 | Ja                            | En matchning                      |
| Högt             | 4        | Helt                 | Ja                            | Flera matchningar               |
| Högt             | 5        | Delvis             | Ja – Flera                 | En matchning                      |
| Högt             | 6        | Delvis             | Ja – Flera                 | Flera matchningar               |
| Högt             | 7        | Delvis             | Ja                            | En matchning                      |
| Högt             | 8        | Helt                 | Nej                             | En matchning                      |
| Högt             | 9        | Nej                    | Ja – Flera                 | En matchning                      |
| Högt             | 10       | Nej                    | Ja – Flera                 | Flera matchningar               |
| Medium           | 1        | Helt                 | Ja – Flera                 | Beaktas inte                 |
| Medium           | 2        | Helt                 | Ja                            | Beaktas inte                 |
| Medium           | 3        | Helt                 | Nej                             | Flera matchningar               |
| Medium           | 4        | Delvis             | Ja – Flera                 | Beaktas inte                 |
| Medium           | 5        | Delvis             | Ja                            | Beaktas inte                 |
| Medium           | 6        | Nej                    | Ja                            | En matchning                      |
| Medium           | 7        | Nej                    | Ja – Flera                   | Beaktas inte                 |
| Medium           | 8        | Delvis             | Nej                             | En matchning                      |
| Medium           | 9        | Nej                    | Ja                            | Beaktas inte                 |
| Lågt              | 1        | Helt                 | Nej                             | Inga matchningar                     |
| Lågt              | 2        | Delvis             | Nej                             | Flera matchningar               |
| Lågt              | 3        | Delvis             | Nej                             | Inga matchningar                     |
| Låg              | 4        | Nr                    | Nr                             | En matchning                      |
| Låg              | 5        | Nr                    | Nr                             | Flera matchningar               |

## Se även
[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: 'Använda automatisk koppling för att stämma av betalningar | Microsoft Docs '
description: På regelsidan för Betalningskoppling anger du regler som styr hur betalningar/banktransaktioner automatiskt ska kopplas till sina relaterade öppna transaktioner när du använder funktionen Koppla automatiskt på sidan Betalningsavstämningsjournal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 64756cdc1a95cc0bb866fa4b7f87ecea0f1282ff
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191937"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Definiera regler för automatisk koppling av betalningar
På sidan **Regler för betalningskoppling** ställer du in regler som styr hur betalningstext (på en banktransaktion) automatiskt matchas med text på öppna transaktioner i följande två processer:
- Koppla automatiskt betalningar till deras relaterade öppna (obetalda) fakturor, kreditnotor eller andra transaktioner när du använder funktionen **Koppla automatiskt** på sidan **Betalningsavstämningsjournal**. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

- Matcha automatiskt banktransaktioner med deras relaterade, interna bankkontotransaktioner när du väljer åtgärden **Matcha automatiskt** på sidan **Kontoavstämning**. Mer information finns i [Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md).

Du ställer in nya betalningskopplingsregler genom att välja vilka slags data på en rad i en betalningsavstämningsjournal som måste överensstämma med data på en eller flera öppna transaktioner innan den relaterade betalningen automatiskt kopplas till de öppna transaktionerna. Kvaliteten på respektive automatisk koppling visas som värdet **Låg** till **Hög** i fältet **Matchningssäkerhet** på sidan **Betalningsavstämningsjournal** i enlighet med använd regel för betalningskoppling.

Varje rad på sidan **Betalningskopplingsregler** representerar en betalningskopplingsregel. Regler kopplas i den ordning som anges i fältet **Sorteringsordning**. Om flera regler används samtidigt används matchningssäkerheten för den högst sorterade regeln.

Den automatiska kopplingsfunktionen baseras på prioriterade matchningskriterier. Först försöker funktionen, i prioriterad ordning, att matcha texten i de fem fälten **Relaterad part** på en journalrad med text i bankkontot, namnet eller adressen för kunder eller leverantörer med obetalda dokument som representerar öppna transaktioner. Funktionen försöker sedan matcha text i fälten **Transaktionstext** och **Ytterligare transaktionsinformation** på en journalrad med text i fälten **Externt dokumentnr.** och **Dokumentnr.** på öppna transaktioner. Till sist försöker funktionen matcha beloppet i fältet **Rapportbelopp** på en journalrad med beloppet på öppna transaktioner.

> [!NOTE]
> Textmatchning är endast möjligt för text längre än fyra tecken.

Utöver matchningsvillkoret gäller följande för tecknet för betalningsbeloppet:

- För negativa belopp görs först en matchning mot öppna transaktioner som representerar kundfakturor, och sedan mot kreditnotor för leverantören.
- För positiva belopp görs först en matchning mot öppna transaktioner som representerar leverantörsfakturor, och sedan mot kreditnotor för kunden.

## <a name="to-set-up-a-payment-application-rule"></a>Så här definierar du en regel för betalningskoppling
1. Välj ![glödlampeikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Regler för betalningskoppling** och välj sedan relaterad länk.
2. Definiera en ny eller redigerad betalningskopplingsregel genom att fylla i fälten på en rad enligt beskrivningen i följande register.

|Fält|Beskrivning|
|-|-|
|**Matchningssäkerhet**|Anger hur mycket du förlitar dig på kopplingsregeln som du definierar på raden. <br /></br>Ett värde som du anger i det här fältet visas i fältet **Matchningssäkerhet** på sidan **Betalningsavstämningsjournal** enligt kvaliteten på den automatiska betalningskopplingen på journalraden.|
|**Prioritet**|Anger prioriteten för kopplingsregeln i förhållande till andra kopplingsregler som är definierade som rader på sidan **Regler för betalningskopplingar**. 1 motsvarar den högsta prioriteten.|
|**Matchad relaterad part**|Anger hur mycket information om kunden eller leverantören på betalningsavstämningsjournalraden - till exempel adress, ort och bankkontonummer - som måste matcha information om den öppna transaktionen för att kopplingsregeln ska användas för att automatiskt koppla betalningen till den öppna transaktionen.|
|**Matchat dok.nr/externt dok.nr**|Anger om texten på raden i betalningsavstämningsjournalen måste matcha värdet i fältet **Dokumentnr.** eller fältet **Externt dokumentnr.** i den öppna transaktionen innan kopplingsregeln kan användas för att automatiskt koppla betalningen till den öppna transaktionen.|
|**Matchat belopp inkl. tolerans**|Anger hur många transaktioner för en kund eller leverantör som måste överensstämma med beloppet inklusive betalningstolerans innan kopplingsregeln används för att automatiskt koppla en betalning till den öppna transaktionen.|

Följande register visar vilka betalningskopplingsregler som har ställts in i den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Important]
> Betalningskopplingsreglerna kan vara olika i din implementering av [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Matchningssäkerhet | Prioritet | Matchad relaterad part | Dok.nr/externt dok.nr. Matchningar | Matchat belopp inkl. tolerans |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Högt             | 1        | Helt                 | Ja - Flera                 | En matchning                      |
| Högt             | 2        | Helt                 | Ja - Flera                 | Flera matchningar               |
| Högt             | 3        | Helt                 | Ja                            | En matchning                      |
| Högt             | 4        | Helt                 | Ja                            | Flera matchningar               |
| Högt             | 5        | Delvis             | Ja - Flera                 | En matchning                      |
| Högt             | 6        | Delvis             | Ja - Flera                 | Flera matchningar               |
| Högt             | 7        | Delvis             | Ja                            | En matchning                      |
| Högt             | 8        | Helt                 | Nej                             | En matchning                      |
| Högt             | 9        | Nej                    | Ja - Flera                 | En matchning                      |
| Högt             | 10       | Nej                    | Ja - Flera                 | Flera matchningar               |
| Medium           | 1        | Helt                 | Ja - Flera                 | Beaktas inte                 |
| Medium           | 2        | Helt                 | Ja                            | Beaktas inte                 |
| Medium           | 3        | Helt                 | Nej                             | Flera matchningar               |
| Medium           | 4        | Delvis             | Ja - Flera                 | Beaktas inte                 |
| Medium           | 5        | Delvis             | Ja                            | Beaktas inte                 |
| Medium           | 6        | Nej                    | Ja                            | En matchning                      |
| Medium           | 7        | Nej                    | Ja - Flera                   | Beaktas inte                 |
| Medium           | 8        | Delvis             | Nej                             | En matchning                      |
| Medium           | 9        | Nej                    | Ja                            | Beaktas inte                 |
| Lågt              | 1        | Helt                 | Nej                             | Inga matchningar                     |
| Lågt              | 2        | Delvis             | Nej                             | Flera matchningar               |
| Lågt              | 3        | Delvis             | Nej                             | Inga matchningar                     |
| Lågt              | 4        | Nej                    | Nej                             | En matchning                      |
| Lågt              | 5        | Nej                    | Nej                             | Flera matchningar               |

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

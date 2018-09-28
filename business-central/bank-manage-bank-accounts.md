---
title: Hantera bankkonton | Microsoft Docs
description: "Du måste regelbundet stämma av banktransaktioner med relaterade banktransaktioner i dina bankkonton."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: sv-se
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a>Hantera bankkonton
Du måste regelbundet stämma av dina banktransaktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] med de relaterade transaktionerna på dina bankkonton i din bank och sedan bokföra saldot till ditt bankkonto. Du kan utföra denna aktivitet antingen som en del av bearbetning av betalningarna som representeras på kontoutdraget i **Betalningsavstämningsjournal**. Alternativt kan du utföra åtgärden separat från betalningsbehandlingen i fönstret **bankkontoavstämning** där du matchar (synkronisera) bankutdragets rader i den vänstra rutan med dina interna bankkontotransaktioner i den till höger. I båda fönstren kan du fylla i bankutdragsinformationen genom att importera en fil eller mata in och använda automatiskt matchande förslag.

> [!NOTE]  
> I Nordamerika kan du också utföra bankavstämning i fönstret **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler. Du använder det här fönstret i stället för fönstret **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** i fönstret **Redovisningsinställningar**. Mer information finns i avsnittet ”stämma av bankkonton” under Förenta staterna: lokal funktion.

Ibland kan du överföra belopp mellan bankkontot i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att visa överföringar på din bank. Du utför denna aktivitet i fönstret **redovisningsjournal** på olika sätt beroende på pengarnas valuta.

Innan du kan hantera bankkonton, måste du registrera varje bankkonto som bankkontokort. Dessutom måste du skapa elektroniska tjänster som du kan använda för kontoutdragsimport-och betalningsfilexport. Mer information finns i [Skapa bankkonton](bank-setup-banking.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Om du vill | Gå till |
| --- | --- |
| Stämma av bankkonton i samband med betalningsbehandling i fönstret **Betalningsavstämningsjournal**. |[Koppla utbetalningar automatiskt och stämma av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Du kan stämma av bankkonton inklusive checktransaktioner som en separat aktivitet i fönstret **Bankkontoavstämning**. |[Stämma av bankkonton separat](bank-how-reconcile-bank-accounts-separately.md) |
| bokföra överföringar mellan bankkonton i samma valuta eller olika valutor. |[Överföra banktillgångar](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Se även
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 


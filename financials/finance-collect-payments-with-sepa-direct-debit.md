---
title: SEPA direkt debet i Dynamics 365 | Microsoft Docs
description: "Du kan samla in betalningar direkt från kundens bankkonto enligt SEPA-formatet."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 0447e6c9f84457589df5cbc1efaecb2de24e7295
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Samla in betalningar med SEPA-autogiro
Med kundens samtycke kan du samla in betalningar direkt från kundens bankkonto enligt SEPA-formatet.  

 Först ställer du in exportformat för bankfilen som används av din bank för att utföra en autogiro. Sedan ställer du in kundens betalningsmetod. Till sist ställ in medgivande för autogiro att återspegla ditt avtal med kunden för att samla in sina betalningar under en viss avtalsperiod.  

 För instruktioner till banken för att överföra betalningsbeloppet från kundens bankkonto till ditt företags konto, skapa en autogiroinsamlingpost som innehåller information om bankkonton, de berörda försäljningsfakturorna och medgivande för autogiro. Sedan kan du exportera en XML-fil som baseras på samlingstransaktionen som du skickar till din bank för bearbetning. Alla betalningar som inte kunde behandlas meddelas till dig av din bank och du måste sedan manuellt avvisa de aktuella autogiroinsamlingsposterna.  

 Du kan ställa in standardiserade kundförsäljningskoder med metoden för autogirobetalning och obligatorisk information. Du kan sedan använda batch-jobbet **Skapa standard kundfakturor** för att generera flera försäljningsfakturor med direktdebiteringsinformationen ifylld automatiskt. Detta kan göras manuellt eller automatiskt enligt betalningens förfallodatum.  

 När betalningar har behandlas enligt din bank, kan du bokföra betalningsinleveranser antingen direkt från **Transaktioner för samlingar med autogiro** eller genom att flytta betalningsraderna i journalen när du bokför betalningsinleveranser, såsom fönstret **Inbetalningsjournal**. Beroende på processen för hantering av kontanter, kan du också vänta och använda betalningarna som en del av bankavstämning.  

> [!NOTE]  
>  För att samla in betalningar med hjälp av SEPA Autogiro måste valutan på försäljningsfakturan är EURO.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Förbered bankkontoformat, betalningssätt och kundavtal för SEPA-autogiro.|[Så här: Konfigurera SEPA Autogiro](finance-how-to-set-up-sepa-direct-debit.md)|  
|Be din bank att överföra betalningsbeloppen från kunders bankkonton till företagets konto enligt inställningarna för SEPA-autogiro.|[Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Ställ in standardiserade kundförsäljningskoder för direktdebetfakturor och generera försäljningsfakturor med direktdebiteringsinformation om fakturorna som har förfallit till betalning.|[Så här: Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md)|  
|Bokföra betalningar som SEPA-autogiro.|[Så här bokför du betalningsinleveranser för SEPA Autogiro](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Se även  
[Hantera kundreskontra](receivables-manage-receivables.md)


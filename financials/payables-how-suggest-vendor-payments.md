---
title: "Så här föreslår du leverantörsbetalningar | Microsoft Docs"
description: "Så här använder du betalningsförslag för leverantörer"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4b85fc783cdebb7c1d2e048315e48aee02a189fa
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-suggest-vendor-payments"></a>Så här använder du betalningsförslag för leverantörer
I fönstret **Betalningsjournal** kan du använda batch-jobbet **Föreslå leverantörsbetalning** för att föreslå betalningsrader. Rader för saker som t.ex. betalningar som förfaller snart eller betalningar där en kassarabatt finns tillgänglig föreslås utifrån dina inställningar.

För att dra full nytta av de föreslagna raderna, måste du prioritera leverantörerna. Mer information finns i [Så här prioriterar du leverantörer](purchasing-how-prioritize-vendors.md).  

Leverantörstransaktioner som inte är **stoppade** ingår inte.  

**Viktigt:** om du vill utnyttja kassarabatterna och har angett ett disponibelt belopp, används beloppet för:  

* Prioritera förfallna leverantörstransaktioner först efter prioritet.  
* Förfallna leverantörstransaktioner som inte prioriterats.  
* Öppna leverantörstransaktioner som är berättigade till kassarabatter, ordnade efter leverantörsnummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Om du vill använda funktionen Betalningsförslag för lev.
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Betalningsjournaler**, och väljer sedan relaterad länk.  
2. Öppna den relevanta journalen och välj sedan åtgärden **Betalningsförslag för lev.**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Välj **OK**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Så här infogar du förfallodatum som bokföringsdatum på betalningsjournalrader
När du använder **Betalningsförslag för lev.**-batchjobbet för att skapa betalningsrader för leverantörer, kan du fylla två specialfält så att de genererade raderna använder förfallodatumet för att beräkna bokföringsdatumet. Dessa fält är **Beräkna bokföringsdatum från dokumentets förfallodatum** och **Dokumentets förfallodatum är förskjutet**.  

**Viktigt:** Du kan inte använda fältet **Beräkna bokföringsdatum från dokumentets förfallodatum** tillsammans med fältet **Utnyttja kassarabatter** eller fältet **Summering per leverantör**. Om bokföringsdatumet baseras på förfallodatum, så kan vissa kassarabatter kanske inte beräknas korrekt eftersom bokföringsdatumet är efter kassarabattdatumet.  

Dessutom, om det beräknade bokföringsdatum inträffar tidigare flyttas bokföringsdatumet fram till arbetsdatumet, och en varning visas.  

Du kan även skapa betalningsrader manuellt genom att använda förfallodatum för att beräkna bokföringsdatum När du har installerat leverantörsreskontratransaktioner kan du använda åtgärden **beräkna bokföringsdatum** för att uppdatera bokföringsdatumet på journalraden med förfallodatumet för relaterad inköpsfaktura. Mer information finns i [Så här kopplar du inköpstransaktioner manuellt](payables-how-apply-purchase-transactions-manually.md).  

**Obs!** Om inköpsfakturan har förfallit kommer bokföringsdatum att anges till arbetsdatumet, och teckensnittet på raden ändras till röd färg.  

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Gör utbetalningar](payables-make-payments.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  


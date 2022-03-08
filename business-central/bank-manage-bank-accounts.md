---
title: Hantera bankkonton | Microsoft Docs
description: Du måste regelbundet stämma av banktransaktioner med relaterade banktransaktioner i dina bankkonton.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c36e906c87cb17acb85d8cde32fdc51ee501469d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381737"
---
# <a name="reconciling-bank-accounts"></a>Stämma av bankkonton

En bankavstämning bör slutföras med jämna mellanrum för alla dina bankkonton för att säkerställa att företagets kassaregister är korrekta. Du gör detta genom att jämföra och matcha poster i dina interna bankkonton med banktransaktioner på din bank och sedan bokföra saldona på dina interna bankkonton för att göra summorna tillgängliga för ekonomichefer. Bankavstämning är också ett praktiskt sätt att upptäcka och lösa problem med saknade betalningar och bokföringsfel.

Alternativt kan du utföra åtgärden på sidan **Bankkontoavstämning** där du matchar (synkroniserar) bankutdragets rader i den vänstra rutan med dina interna bankkontotransaktioner i den till höger. Alternativt kan du på sidan **Betalningsavstämningsjournal** utföra denna aktivitet som en del av bearbetningen av de betalningar som anges på kontoutdraget. På båda sidor kan du fylla i bankutdragsinformationen genom att importera en fil eller mata in och använda automatiskt matchande förslag.

> [!NOTE]  
> I Nordamerika kan du också utföra bankavstämning på sidan **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler. Du använder den här sidan i stället för sidan **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** på sidan **Redovisningsinställningar**. Mer information finns i avsnittet [stämma av bankkonton](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Förenta staterna: lokal funktion.

Innan du kan hantera dina bankkonton i [!INCLUDE[prod_short](includes/prod_short.md)] måste du registrera varje bankkonto som bankkontokort. Dessutom måste du skapa elektroniska tjänster som du kan använda för kontoutdragsimport-och betalningsfilexport. Mer information finns i [Konfigurera bank](bank-setup-banking.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.

| Till | Gå till |
| --- | --- |
| Du kan stämma av bankkonton som en separat aktivitet på sidan **Bankkontoavstämning**. |[Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md) |
| Stämma av bankkonton i samband med betalningsbehandling på sidan **Betalningsavstämningsjournal**. |[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> Med bankavstämningar kan du kontrollera att dina böcker är aktuella och inte bokföra avstämningen förrän du är nöjd med avstämningen.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Ställa in bankverksamhet](bank-setup-banking.md)  
[Stämma av bankkonton](bank-how-reconcile-bank-accounts-separately.md)  
[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Överföra banktillgångar](bank-how-transfer-bank-funds.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
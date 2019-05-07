---
title: Skapa bankkonton | Microsoft Docs
description: Du kan stämma av bankkonton med utdrag från banken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e3ccc70405b286929c9d267e76c3ba76fd2e7e4a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931491"
---
# <a name="set-up-bank-accounts"></a>Skapa bankkonton
Du använder bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att hålla reda på dina banktransaktioner. Konton kan definieras i den lokala valutan eller i en utländsk valuta. När du har skapat bankkonton kan du också använda funktionen för utskrift av checkar.

## <a name="to-set-up-bank-accounts"></a>Så här skapar du bankkonton
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bankkonto** och välj sedan relaterad länk.
2. På sidan **Bankkonton** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Så här fyller du i fältet **Saldo** med en ingående balans, du måste bokföra en bankkontotransaktion med beloppet i fråga. Du kan göra detta genom att utföra en bankkontoavstämning. Mer information finns i [Stämma av bankkonton separat](bank-how-reconcile-bank-accounts-separately.md). Alternativt kan du implementera den ingående balansen som en del av skapande av allmänna data i nya företag med hjälp av den assisterad inställningsguide **Migrera affärsdata**. Mer information finns i [Komma igång](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Så här skapar du ett bankkonto för import eller export av bankfilerna
Fälten på snabbfliken **Överför** på sidan **Bankkontokort** är relaterade till import och export av bankfeeds och filer. Mer information finns i [Så här skapar du konverteringstjänsten för bankdata](bank-how-setup-bank-data-conversion-service.md) och [Så här ställer du in tjänsten bankfeedertjänsten Envestnet Yodlee](bank-how-setup-bank-statement-service.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bankkonto** och välj sedan relaterad länk.
2. Öppna kortet för ett bankkonto som du ska exportera eller importera bankfiler.
3. I snabbfliken **Överför** fyller du i nödvändiga fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Andra filexporttjänster och deras format kräver olika inställningsvärden på sidan **bankkontokort**. Du får information om vilka inställningsvärden som är fel eller saknas när du försöker exportera filen. Så läs de korta beskrivningarna av fälten eller se relaterad procedur i närliggande ämnen. Till exempel exportera en betalningsfil för nordamerikansk elektronisk överföring kräver att både fältet **Sista kundremissnr.** och fältet **Transitnr.** fylls i. Mer information finns i [Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Så här skapar du leverantörsbankkonto för export av bankfiler
Fälten på snabbfliken **Överför** på sidan **Leveraqntörsbankkontokort** är relaterade till export av bankfeeds och filer. Mer information finns i [Så här skapar du konverteringstjänsten för bankdata](bank-how-setup-bank-data-conversion-service.md) och [Så här exporterar du betalningar till en bankfil](payables-how-export-payments-bank-file.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leverantörer** och välj sedan relaterad länk.
2. Öppna kortet för en leverantör vars bankkonto som du ska exportera betalningsbankfiler till.
3. Välj åtgärden **bankkonton**.
3. På sidan **Leverantörsbankkontokort** på snabbfliken **Överför** fyller du sedan de fält som behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se även
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Ställa in bokföringsmallar](finance-posting-groups.md)  
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

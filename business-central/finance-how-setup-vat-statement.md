---
title: Ställa in en momsrapport
description: I det här avsnittet beskrivs hur du lägger upp en momsrapportmall och momsrapportnamn för att uppfylla ändrade skattemyndighetskrav.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 317, 318, 320, 474
ms.date: 06/16/2021
ms.author: bholtorf
ms.openlocfilehash: 12b51af89894c428120ddd6c4639a397bd8a4d97
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529251"
---
# <a name="set-up-vat-statement-templates-and-vat-statement-names"></a>Ställa in momsrapportmallar och momsrapportnamn

Skattemyndigheterna kan och ändrar sina krav för bokföring av moms. Momsrapportmallar och momsrapportnamn kan hjälpa dig att förbereda dig inför kommande ändringar och göra övergången till de nya kraven smidigare. Du kan använda momsrapportmallar när du vill ställa in olika rapporter när du väljer att skriva ut rapporten. Varje momsrapportmall kan ha flera momsrapportnamn som i sin tur definierar beräkningarna, och du kan skapa ett nytt momsrapportnamn när behov ändras. Exempelvis kan ett namn beräkna moms för detta år baserat på nuvarande krav och en annan kan beräkna moms baserat på kraven för nästa år. Namn är också ett sätt att hålla en historik med momsrapportformat, till exempel så att du kan se tillbaka för att se hur du beräknar moms i föregående år.

## <a name="to-define-a-vat-statement"></a>Definiera en momsrapport

Momsrapporter låter dig beräkna momsavräkningsbeloppen för en bestämd period (t. ex. ett kvartal).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsrapporter** och väljer sedan relaterad länk.  
2. Välj fältet **namn** och välj sedan **nytt** på sidan **Momsrapportnamn**.
3. Fyll i relevanta fält. Vanligtvis vill du ha en inställning för varje kombination av Moms rörelsebokföringsmall/Moms produktbokföringsmall. För radnummer är det klokt att använda likvärdiga nummer eller koder som i den officiella momsrapporten [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Du kan filtrera informationen som utdraget innehåller, beroende på vad du väljer fältet **typ**. **Kontosummering** är användbar när du vill att moms från ett visst konto.
**Momstrans.summering** får moms från konton som är kopplade till markeringar i fälten **Typ av bokföring**, **Moms rörelsebokf.mall**, och/eller **Moms, produktbokföringsmall**. **Radsummering** kan du skriva in ett värde eller snabb filterkriterierna i fältet **Radsummering**. Mer information om sökning och filtrering finns i [Söka, filtrera och sortera data](ui-enter-criteria-filters.md). **Beskrivning** används ofta för att lägga till en anteckning i uttrycket. Exempelvis kan du använda den som en rubrik när du har använt radsummering.

## <a name="to-preview-the-vat-statement"></a>Förhandsgranska momsrapporten

När du har definierat en momsrapport kan förhandsgranska du den och kontrollera att det uppfyller dina behov.
> [!Tip]
> Det är bästa praxis att ha ett avsnitt i momsrapporten som använder **Typ** **Momstrans.summering** och ett annat avsnitt nedanför som använder **Typ** **Kontosummering** för att stämma av beloppen baserat på tabellen **Momstransaktion** jämfört med beloppet på **Redovisningskonton**. Du kan också använda rapporten **Redovisning – Momsavstämning** för detta ändamål.

1. Välj **förhandsgranskning**.
2. Du begränsar rapporten till en viss period genom att ange ett datumfilter. För mer information om hur du anpassar sidan så att datumfiltret visas,, se [Söka, filtrera och sortera data](ui-enter-criteria-filters.md).
3. Du kan välja flera olika alternativ för att definiera vilken typ av momstransaktioner som ska tas med i rapporten.
4. På de rader där fältet **Typ** innehåller **Momstrans.summering** kan du visa en lista över momstransaktioner genom att välja beloppet i fältet **Kolumnbelopp**.
5. Du kan använda anpassning för att visa fler fält på raderna. Till exempel det orealiserade nettobeloppet och det orealiserade momsbeloppet, om du använder orealiserad moms.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Ställa in moms](finance-setup-vat.md)  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

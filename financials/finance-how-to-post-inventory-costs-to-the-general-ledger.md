---
title: "Bokföra lagerkostnader i redovisningen | Microsoft Docs"
description: Beskriver hur du hanterar fysiska varor som du handlar med, till exempel hantering av lager i distributionslagret.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 07/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b71ca658374679860fae487c60d52502ce8eb243
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Stämma av lagerkostnader med redovisningen
När du bokför lagertransaktioner, till exempel försäljningsutleveranser, inköpsfakturor eller lagerjusteringar, registreras de ändrade artikelkostnaderna i artikelvärdesposter. För att återspegla denna förändring i lagervärde i din bokföring kommer lagerkostnaderna automatiskt att bokföras på relaterade lagerkonton i redovisningen. För varje lagertransaktion som bokförs, bokförs lämpliga värden på lagerkontot, justeringskontot och KSV-kontot i redovisningen.

Automatisk kostnadsbokföring definieras av fältet **Automatisk kostnadsbokföring** i fönstret **Lagerinställningar**.

Även om lagerkostnaderna automatiskt bokförs i redovisningen måste du fortsatt säkerställa att varukostnader skickas vidare till relaterade avgående försäljningstransaktioner, i synnerhet när varorna säljs innan du har fakturerat inköpet av varorna. I programmet kallas detta för Kostnadsjustering. Artikelkostnader justeras automatiskt när du bokför artikeltransaktioner, men du kan också justera projektartikelkostnader manuellt. Mer information finns i [Justera artikelkostnader](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Bokföra lagerkostnader manuellt
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokför lagerkostnad i redov.** och välj sedan relaterad länk.
2. Bokför lagerkostnader i redovisningen manuellt genom att köra batch-jobbet. När det här batch-jobbet körs skapas redovisningstransaktioner utifrån värdetransaktioner. Det går att bokföra transaktionerna så att de sammanfattas per bokföringsmall.

> [!NOTE]  
> När du kör batch-jobbet kan fel påträffas som har att göra med saknad inställning eller inkompatibel dimensionsinställning. Om fel uppstår i batch-jobbets dimensionsinställning ersätter den dessa fel och använder dimensionerna för värdetransaktionen. För andra fel hopar batch-jobbet över att bokföra värdetransaktionerna och anger dem vid slutet av rapporten i avsnittet “Transaktioner som hoppats över”. För att bokföra de här transaktionerna måste du först lösa felen.

Om en lista över felen ska visas innan batch-jobbet för bokföring ska köras kan rapporten **Bokför lagerkostnad i redovisning - test** köras. Alla fel som inträffar under testbokföringen visas i en lista i testrapporten. Därefter går det att korrigera felen och köra batch-jobbet för bokföringen av lagerkostnaden utan att transaktioner hoppas över.

Det går att visa en översikt över de värden som eventuellt bokförs i redovisningen genom att köra batch-jobbet **Bokför lagerkostnad i redov.**, utan att själva bokföringen av värdena utförs i redovisningen. Genom att avmarkera fältet **Bokför** på sidan för begäran kan översikten visas. Om batch-jobbet körs med de här inställningarna visas värdena som kan bokföras i redovisningen i rapporten, men de bokförs inte.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>För att granska avstämningen mellan inventeringen och redovisningen.
Fönstret **Avstämning lager - redovisning -** visar följande:

- Påvisar avstämningsdifferenser genom att jämföra vad som registrerats i redovisningen och vad som registrerats i lagerredovisningen (värdetransaktioner).
- Visar oavstämda kostnadsbelopp i värdetransaktionerna i lagerredovisningen om de mappas till motsvarande lagerrelaterade konton i redovisningen och jämför dessa med summorna som faktiskt registreras på samma konton i redovisningen.
- Återspeglar den dubbla transaktionsstrukturen i redovisningen genom att visuellt presentera data på det sättet. En KSV-transaktion har till exempel en motsvarande lagertransaktion.
- Låter användaren analysera och se vilka transaktioner som utgör kostnadsbeloppen.
- Omfattar filter som begränsar analyserna efter datum, artikel och lagerställe.
- Förklarar orsakerna till avstämningsdifferenser i informativa meddelanden.


I kolumnen **Namn** längst till vänster i rutnätet anges de olika typerna av redovisningskonton som associeras med lagret.

Kolumnerna **Lager**, **Lager (interim)** och **PIA-lager** innehåller de fakturerade, icke fakturerade och PIA-summorna för respektive redovisningskontotyp. Dessa beräknas från värdetransaktionerna, det vill säga de planeras till de redovisningskontotyper där de ska hamna när de slutligen bokförs i redovisningen.

I kolumnen **Summa** visas summan (i fetstil) för värdetransaktionsbeloppen i de tre lagerkolumnerna.

I kolumnen **Redovisningssumma** visas beloppen (i fetstil) för varje redovisningskontotyp som finns i redovisningen. Dessa beräknas från redovisningstransaktionerna, det vill säga de representerar lagerkostnaderna som redan har bokförts i redovisningen.

Kolumnen **Differens** representerar differensen mellan fälten **Redovisningssumma** och **Summa**.

Högst upp i fönstret **Avstämning lager - redovisning** kan du ange filter för att t.ex. begränsa den tidsperiod som du vill hämta information om.

Om du markerar fältet **Visa varning** och om det finns avvikelser mellan lagersummor och redovisningssummor, visas meddelanden i fältet **Varning** för rutnätet som förklarar avvikelsen. Om du väljer fältet Varning får du mer information om vad varningen betyder.

När du har angett alla önskade filter väljer du åtgärden **Visa matris**. Data beräknas och matrisfönstret öppnas.

I kolumnen längst till vänster i rutnätet kan du se de olika redovisningskonton som har associerats med lager. I rutnätet visas sedan de fakturerade och icke-fakturerade (interim) lagersummorna och PIA-lagersummorna för var och en av dessa kontotyper. Dessa summor beräknas utifrån värdetransaktionerna.

I de närmast följande kolumnerna visas summorna för samma kontotyper beräknade utifrån redovisningstransaktioner.

Välj värdet i något av fälten om du vill se de lagerrapporttransaktioner som användes för att beräkna summorna. För lagersummorna är lagerrapporttransaktionerna summorna av värdetransaktioner för artiklarna. För redovisningssummorna är lagerrapporttransaktionerna summorna från redovisningstransaktionerna.

## <a name="see-also"></a>Se även  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)


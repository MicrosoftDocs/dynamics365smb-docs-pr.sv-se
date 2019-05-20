---
title: Inställning av bokföringsmall | Microsoft Docs
description: Översikt av bokföringsmallar som du kan använda för att spara tid och för att undvika misstag när du bokför transaktioner.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: ee93a04f1dd4f6d7d1796a759baa4c585d943c68
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242520"
---
# <a name="setting-up-posting-groups"></a>Ställa in bokföringsmallar
Bokföringsmallar mappar enheter som t.ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. De sparar tid och undviker fel när du bokför transaktioner. Transaktionsvärdet går till de konton som anges i bokföringsmallen för den aktuella enheten. Det enda kravet är att det finns en kontoplan. Mer information finns i [Ställa in kontoplanen](finance-setup-chart-accounts.md).  

Bokföringsmallar omfattas av tre paraplyer:  

* Allmänt - definiera vem du säljer till och köper från, och vad du säljer och vad du köper. Du kan också slå ihop mallar om du vill ange bland annat resultatkontona att bokföra till eller använda mallar för att filtrera rapporter.  
* Specifik - Använda försäljningsdokument istället för att bokföra direkt till redovisningen. När du skapar transaktioner i kundreskontra används motsvarande transaktioner i redovisningen.  
* Skatt – definiera skatteprocentsatser och beräkningstyper som gäller för vem du säljer till och köper från, och vad du säljer och vad du köper.

I följande tabeller beskrivs bokföringsmallarna under varje paraply.  

| Generella bokföringsmallar | Beskrivning |
| --- | --- |
| Generella rörelsebokföringsmallar |Tilldela denna mall till kunder och leverantörer för att ange vem du säljer till och som du vill köpa från. Ställ in dessa på sidan **Rörelsebokföringsmallar**. När du gör det ska du tänka på hur många mallar som du måste bryta ned försäljning och inköp. mallara till exempel kunder och leverantörer efter geografiskt område eller efter typ av verksamhet. |
| Generella produktbokföringsmallar |Tilldela den här mallen till artiklar och resurser för att ange vad du säljer och vad du köper. Ställ in dessa på sidan **Produktbokföringsmallar**. När du gör det måste du tänka över hur många mallar du måste bryta ner försäljning per produkt (artiklar och resurser) och inköp per artikel. Dela exempelvis upp mallarna efter råmaterial, detaljhandel, resurser, kapacitet och så vidare. |
| Bokföringsinställningar |Kombinera rörelse- och produktbokföringsmallar och välj sedan konton att bokföra till. För varje kombination av rörelse- och produktbokföringsmallar kan du tilldela en specifik uppsättning redovisningskonton. Detta betyder att du till exempel kan bokföra försäljningen av samma artikel på olika försäljningskonton i redovisningen eftersom kunder tilldelas olika rörelsebokföringsmallar. Ställ in dessa på sidan **Generella bokföringsinställningar**. |

| Specifika bokföringsmallar | Description |
| --- | --- |
| Kundbokföringsmallar |Ange kontona som ska användas när du bokför transaktioner i kundreskontra. Om du använder lagret tillsammans med kundreskontra bestämmer den generella rörelsebokföringsmallen som har tilldelats till kunden och den generella produktbokföringsmallen som har tilldelats till lagerartikeln vilka konton som försäljningsorderraden ska bokföras till. Se "Generella rörelsebokföringsmallar" och "Generella produktbokföringsmallar" under **Generella bokföringsmallar** ovan. Ställ in dessa på sidan **Kundbokföringsmallar**. |
| Leverantörsbokföringsmallar |Definiera var transaktioner för leverantörsreskontrakonton, serviceavgiftskonton och kassarabattskonton ska bokföras. Detta liknar kundbokföringsmallar. Ställ in dessa på sidan **Leverantörsbokföringsmallar**. |
| Lagerbokföringsmallar |Definiera lagerbokföringsmallar som du sedan tilldelar motsvarande artikelkonton på sidan **Lagerbokföringsinställning**. På så sätt bokför systemet till det redovisningskonto som har angetts för den kombination av lagerbokföringsmall och lagerställe som har kopplats till artikeln, när du bokför transaktioner avseende artikeln. Med lagerbokföringsmallar kan du även på ett utmärkt sätt organisera ditt lager. När du genererar rapporter kan du separera artiklar efter deras bokföringsmallar. Ställ in dessa på sidan **Lagerbokföringsmallar**. |
| Bokföringsmallar för bankkonto |Definiera konton för bankkonton. Detta kan till exempel förenkla processer för att spåra transaktioner och stämma av bankkonton. Ställ in dessa på sidan **Bokföringsmallar för bankkonto**. |
| Bokföringsmallar för anläggningstillgångar |Definiera konton för olika typer av utgifter och kostnader som t.ex. förvärvskostnader, ackumulerade avskrivningsbelopp, förvärvskostnader vid avyttring, ackumulerad avskrivning vid avyttring, vinster vid avyttring, förluster vid avyttring, underhållskostnader och avskrivningsutlägg. Ställ in dessa på sidan **Anl. bokföringsmallar**. |

| Momsbokföringsmall | Description |
| --- | --- |
| Momsbokföringsmallar |Se hur du kan beräkna och bokföra moms för kunder och leverantörer. Ställ in dessa på sidan **Moms rörelsebokföringsmallar**. När du gör det ska du tänka på hur många mallar du behöver. Detta beror t.ex. på ett antal faktorer som t.ex. lokal lagstiftning och om du gör affärer både inrikes och utrikes. |
| Momsbokföringsmallar |Ange de momsberäkningar som behövs för typerna av artiklar eller resurser som du köper eller säljer. |
| Momsbokföringsinställningar |Kombinera momskombinationer av momsbokföringsmallar. När du fyller i en allmän journalrad, inköpsrad eller försäljningsrad ska vi titta på kombinationen för att identifiera kontona som ska användas. |

## <a name="example-of-linking-posting-groups"></a>Exempel på koppling av bokföringsmallar
Här är ett scenario.  

Dessa bokföringsmallar väljs på kundkortet:  

* Generell rörelsebokföringsmall
* Kundbokföringsmall  

Dessa bokföringsmallar väljs på artikelkortet:  

* Generella produktbokföringsmallar  
* Lagerbokföringsmall  

När du skapar ett försäljningsdokument använder försäljningshuvud kundkortsinformationen och försäljningsraderna använder artikelkortsinformationen.  

* Bokföringen av intäkter (resultaträkning) bestäms av kombinationen av generell rörelsebokföringsmall och generell produktbokföringsmall.  
* Bokföringen av kundreskontra (balansräkning) bestäms av kundbokföringsmallen.  
* Bokföringen av lager (balansräkning) bestäms av lagerbokföringsmallen.  
* Bokföringen av kostnad för sålda varor (resultaträkning) bestäms av kombinationen av generell rörelsebokföringsmall och generell produktbokföringsmall.  

Inställningen avgör när bokföring sker. När är exempelvis timing påverkas av periodiska aktiviteter, som till exempel bokföra lagerkostnad eller justera kost. - artikeltrans.

## <a name="copying-posting-setup-lines"></a>Kopiera bokföringsinställningsrader
Ju fler produkt- och rörelsebokföringsmallar du har desto fler rader ser du på sidan Bokföringsinställningar. Detta kan innebära att många inmatningar måste göras för att lägga upp bokföringsinställningar för företaget. Det kan finnas många olika kombinationer av rörelse- och produktbokföringsmallar, men olika kombinationer kan fortfarande bokföras till samma redovisningskonton. Om du vill begränsa andelen manuell inmatning kopierar du redovisningskontona från en befintlig rad på sidan **Generella bokföringsinställningar**.

## <a name="see-also"></a>Se även
redovisning[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

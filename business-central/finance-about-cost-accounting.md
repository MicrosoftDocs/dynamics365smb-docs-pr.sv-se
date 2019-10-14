---
title: Om kostnadsredovisning | Microsoft Docs
description: Kostnadsredovisning kan hjälpa dig förstå kostnaderna för att driva en verksamhet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 053a0ca21ff26b53cabcc8894ed1cd0e48c904b0
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302674"
---
# <a name="about-cost-accounting"></a>Om kostnadsredovisning
Kostnadsredovisning kan hjälpa dig förstå kostnaderna för att driva en verksamhet. Information om kostnadsredovisning har utformats för att analysera:  

-   Vilka typer av kostnader uppkommer när du driver en verksamhet?  
-   Var uppstår kostnaderna?  
-   Vem bär kostnaderna?  

I kostnadsredovisning fördelar du faktiska och budgeterade kostnader för avdelningar, funktioner, produkter och projekt för att analysera lönsamheten för ditt företag.  

## <a name="workflow-in-cost-accounting"></a>Arbetsflöde i kostnadsredovisning  
Kostnadsredovisning har följande huvudkomponenter:  

-   Kostnadstyper, kostnadsställen och kostnadsbärare  
-   Kostnadstransaktioner och kostnadsjournaler  
-   Kostnadsfördelningar  
-   Kostnadsbudgetar
-   Rapportering av kostnader  

Diagrammet beskriver arbetsflödet för kostnadsredovisning.  

![Kostnadsredovisningsöversikt](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Kostnadstyper, kostnadsställen och kostnadsbärare  
Du definierar kostnadstyper, kostnadsställen och kostnadsbärare för att analysera vad kostnaderna är, var kostnader kommer ifrån och vem som ska bära kostnaderna.  

Du definierar en karta över kostnadstyper med en struktur och funktion som liknar redovisningskontoplanen. Du kan överföra redovisningens resultaträkningskonton eller upprätta din egen plan för kostnadstyper.  

Kostnadsställen är avdelningar och resultatenheter som ansvarar för kostnader och intäkter. Ofta finns fler kostnadsställen i kostnadsredovisningen än i de dimensioner som finns i redovisningen. I redovisningen används normalt bara första nivåns kostnadsställen för direktkostnader och ursprungliga kostnader. I kostnadsredovisning skapas ytterligare kostnadsställen för ytterligare fördelningsnivåer.  

Kostnadsbärare är produkter, produktgrupper eller tjänster för ett företag. Det här är de färdiga varor i ett företag som bär kostnaderna.  

Du kan koppla kostnadsställen till avdelningar och kostnadsbärare till projekt i företaget. Du kan dock koppla kostnadsställen och kostnadsbärare till dimensioner i redovisningen och komplettera dem med delsummor och titlar.  

## <a name="cost-entries-and-cost-journals"></a>Kostnadstransaktioner och kostnadsjournaler  
Rörelsekostnader kan överföras från redovisningen. Du kan överföra kostnadstransaktionerna automatiskt från redovisningen till kostnadstransaktioner med varje bokföring. Du kan också använda ett batch-jobb för att överföra redovisningstransaktionerna till kostnadstransaktioner baserat på sammanfattande bokföring för dag eller månad.  

I kostnadsjournaler kan du bokföra kostnader och aktiviteter som inte finns i redovisning eller inte skapas med fördelningar. Du kan till exempel bokföra rena rörelsekostnader, internavgifter, fördelningar och rättningstransaktioner mellan kostnadstyper, kostnadsställen och kostnadsbärare enskilt eller återkommande.  

## <a name="cost-allocations"></a>Kostnadsfördelningar  
Fördelningar flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare. Omkostnader bokförs först till kostnadsställen och debiteras senare på kostnadsbärare. Till exempel kan detta utföras i en försäljningsavdelning som säljer flera produkter samtidigt. Direkta kostnader kan direkt hänföras till en kostnadsbärare, till exempel ett material som köps för en viss produkt.  

Fördelningsbasen som används och noggrannheten hos fördelningsdefinitionen påverkar resultatet av kostnadsfördelningar. Fördelningsdefinitionen används för att tilldela kostnader först från så kallade förkostnadsställen till huvudkostnadsställen och sedan från kostnadsställen till kostnadsbärare.  

Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Du kan tilldela faktiska värden eller budgeterade värden genom att använda den statiska fördelningsmetoden som är baserad på ett visst värde, till exempel kvadratmetrar, eller en fastställd fördelningskvot på 5:2:4. Du kan också koppla verkliga värden eller budgeterade värden genom att använda den dynamiska distributionsmetoden med nio fördefinierade fördelningsbaser och 12 dynamiska datumintervall.  

## <a name="cost-budgets"></a>Kostnadsbudgetar  
Du kan skapa kostnadsbudgetar efter behov. Du kan kopiera kostnadsbudgeten till redovisningsbudgeten och tvärtom. Du kan överföra budgeterade kostnader som faktiska kostnader.  

## <a name="cost-reporting"></a>Rapportering av kostnader  
De flesta rapporter och statistik baseras på de bokförda kostnadstransaktionerna. Du kan ange sortering av resultat och använda filter för att definiera vilka data som måste visas. Du kan skapa rapporter för kostnadsfördelningsanalys. Dessutom kan du använda standardkontoscheman för att ange hur dina rapporter för planen över kostnadstyper visas.  

## <a name="see-also"></a>Se även  
 [Redovisa kostnader](finance-manage-cost-accounting.md)  
 [Ekonomi](finance.md)   
 [Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

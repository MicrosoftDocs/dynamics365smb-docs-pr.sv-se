---
title: Om kostnadsredovisning
description: Kostnadsredovisning kan hjälpa dig förstå kostnaderna för att driva en verksamhet. Information om kostnadsredovisning har utformats för att analysera olika problem.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="about-cost-accounting" />Om kostnadsredovisning

Kostnadsredovisning kan hjälpa dig förstå kostnaderna för att driva en verksamhet. Information om kostnadsredovisning har utformats för att analysera:  

- De typer av kostnader som du ådrar dig på att bedriva en verksamhet  
- Var kostnaderna uppstår
- Vem som bär kostnaderna  

I kostnadsredovisning fördelar du faktiska och budgeterade kostnader för avdelningar, funktioner, produkter och projekt för att analysera lönsamheten för ditt företag.  

## <a name="workflow-in-cost-accounting" />Arbetsflöde i kostnadsredovisning

Kostnadsredovisning har följande huvudkomponenter:  

- Kostnadstyper, kostnadsställen och kostnadsbärare  
- Kostnadstransaktioner och kostnadsjournaler  
- Kostnadsfördelningar  
- Kostnadsbudgetar
- Rapportering av kostnader  

Diagrammet beskriver arbetsflödet för kostnadsredovisning.  

![Kostnadsredovisning – översikt.](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects" />Kostnadstyper, kostnadsställen och kostnadsbärare

Du definierar kostnadstyper, kostnadsställen och kostnadsbärare för att analysera vad kostnaderna är, var kostnader kommer ifrån och vem som ska bära kostnaderna.  

Först definierar du ett diagram över kostnadstyper med en struktur och funktion som liknar redovisningskontoplanen. Du kan skapa ditt eget diagram över kostnadstyper eller göra det genom att överföra redovisningens resultaträkningskonton.  

Kostnadsställen är avdelningar och resultatenheter som ansvarar för kostnader och intäkter. Ofta finns fler kostnadsställen i kostnadsredovisningen än i de dimensioner som finns i redovisningen. I redovisningen används normalt bara första nivåns kostnadsställen för direktkostnader och ursprungliga kostnader. I kostnadsredovisning skapas ytterligare kostnadsställen för ytterligare fördelningsnivåer.  

Kostnadsbärare är produkter, produktgrupper eller tjänster som ett företag erbjuder. Det här är de "färdiga varor" i ett företag som bär kostnaderna.  

Du kan koppla kostnadsställen till avdelningar och kostnadsbärare till projekt i företaget. Genom redovisningen kan du koppla kostnadsställen och kostnadsbärare till dimensioner och komplettera informationen med delsummor och titlar.  

## <a name="cost-entries-and-cost-journals" />Kostnadstransaktioner och kostnadsjournaler

Rörelsekostnader kan överföras från redovisningen. Du kan överföra kostnadstransaktionerna automatiskt från redovisningen till kostnadstransaktioner med varje bokföring. Du kan också använda ett batch-jobb för att överföra redovisningstransaktionerna till kostnadstransaktioner baserat på sammanfattande bokföring för dag eller månad.  

I kostnadsjournaler kan du bokföra kostnader och aktiviteter som inte finns i redovisning eller inte skapas med fördelningar. Du kan till exempel bokföra rena rörelsekostnader, internavgifter, fördelningar och rättningstransaktioner mellan kostnadstyper, kostnadsställen och kostnadsbärare enskilt eller återkommande.  

## <a name="cost-allocations" />Kostnadsfördelningar

Fördelningar flyttar kostnader och intäkter mellan kostnadstyper, kostnadsställen och kostnadsbärare. Omkostnader bokförs först till kostnadsställen och debiteras senare på kostnadsbärare. Till exempel kan detta utföras i en försäljningsavdelning som säljer flera produkter samtidigt. Avdelningens omkostnader, till exempel löner, leveranser och resekostnader, tilldelas till försäljningskostnadsstället, som sedan fördelas mellan de olika produkter (kostnadsbärare) som sålts, tillsammans med det material som köps (inköpskostnad) som ska användas i dem.

Fördelningsbasen som används och noggrannheten hos fördelningsdefinitionen påverkar resultatet av kostnadsfördelningar. Fördelningsdefinitionen används för att tilldela kostnader först från så kallade förkostnadsställen till huvudkostnadsställen och sedan från kostnadsställen till kostnadsbärare.  

Varje fördelning består av en fördelningskälla och en eller flera fördelningsmål. Du kan tilldela faktiska värden eller budgeterade värden genom att använda den fasta fördelningsmetoden som är baserad på ett visst värde, till exempel kvadratmetrar, eller en fastställd fördelningskvot på 5:2:4. Du kan också koppla verkliga värden eller budgeterade värden genom att använda den dynamiska distributionsmetoden med nio fördefinierade fördelningsbaser och 12 dynamiska datumintervall.  

## <a name="cost-budgets" />Kostnadsbudgetar

På samma sätt som med budgetering i redovisningen kan du skapa budgetar för att planera för kostnader under en viss period (t.ex. ett räkenskapsår) som kan kopplas till ett kostnadsställe (företagsavdelning) eller en kostnadsbärare (produkt eller tjänst). Du kan skapa kostnadsbudgetar efter behov. Du kan sedan kopiera kostnadsbudgeten till redovisningsbudgeten och tvärtom. Och du kan överföra budgeterade kostnader som faktiska kostnader.

## <a name="cost-reporting" />Rapportering av kostnader

De flesta rapporter och statistik baseras på de bokförda kostnadstransaktionerna. Du kan ange sortering av resultat och använda filter för att definiera vilka data som måste visas. Du kan skapa rapporter för kostnadsfördelningsanalys. Dessutom kan du använda ekonomiska rapporter för att ange hur dina rapporter för planen över kostnadstyper visas.  

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/paths/use-cost-accounting-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Redovisa kostnader](finance-manage-cost-accounting.md)  
[Ekonomi](finance.md)  
[Terminologi i kostnadsredovisning](finance-terminology-in-cost-accounting.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

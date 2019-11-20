---
title: Ta bort och koppla om artikeltransaktioner | Microsoft Docs
description: Du kan visa och manuellt ändra vissa artikelkopplingstransaktioner som skapas automatiskt under lagertransaktioner.
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
ms.openlocfilehash: 898548bd33bbc9a5a7ae7400c626bf7a7820bfd4
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554140"
---
# <a name="remove-and-reapply-item-ledger-entries"></a>Ta bort och koppla om artikeltransaktioner
På sidan **Kopplingsformulär** kan du visa och manuellt ändra vissa artikelkopplingstransaktioner som skapas automatiskt under lagertransaktioner.  

När du bokför en lagertransaktion som innebär att artiklar tas in i eller ut ur lagret, skapas en artikelkoppling mellan varje lagerökning och lagerminskning. Genom de här kopplingarna fastställs kostnadsflödet från varorna som tas emot i lagret till varorna som lämnar lagret. På grund av sättet som styckkostnaden beräknas på kan en felaktig artikelkoppling medföra att genomsnittskostnaden och styckkostnaden får oriktiga resultat. Mer information finns i Designdetaljer: Artikelkoppling.

Följande scenariot kan till exempel kräva att du återställ ett program eller omkopplar följande artikeltransaktioner:

- Användaren har glömt att göra en fast koppling.
- En felaktig fast koppling har gjorts.
- En artikel måste returneras som en försäljning redan har kopplats till.

Om möjligt, använda ett dokument för att koppla en artikeltransaktion. Till exempel om du måste göra en inköpsretur för en artikel som en försäljning redan har kopplats till, kan du koppla genom att skapa och bokföra inköpsreturdokumentet, med hjälp av rätt koppling i **Koppla till artikellöpnr** fältet på inköpsreturen raden. Du kan använda **Hämta bokförda dokumentrader som ska återföras** eller **Kopiera dokument** funktion i inköpsreturdokumentet för att göra det lättare. När du bokför dokumentet, återtillämpas artikeltransaktionen automatiskt. Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

Om du inte kan använda ett dokument för att koppla, som när du behöver rätta en fast koppling, använder du sidan **Kopplingsformulär** för att korrigera ett program.

> [!Warning]  
> Ta hänsyn till följande viktiga punkter i arbetet med kopplingsformulär:
    - Du bör inte lämna bortkopplade kopplingstransaktioner för långa perioder, eftersom andra användare inte kan behandla artiklarna förrän du kopplar om kopplingstransaktionerna eller stänger sidan **Kopplingsformulär**. Användare som försöker utföra åtgärder som omfattar en kopplingstransaktion som tagits bort manuellt, får felmeddelande följande: ”Du inte kan utföra den här åtgärden, eftersom transaktioner för artiklar XXX tagits bort i kopplingsformuläret av användaren XXX. ”
    - Omkopplingen av artikeltransaktionerna bör göras utanför normal arbetstid, så att eventuella konflikter med användare som bokför transaktioner med samma artiklar kan undvikas.
    - När kopplingsformuläret stängs utför [!INCLUDE[d365fin](includes/d365fin_md.md)] en kontroll för att säkerställa att alla transaktioner har kopplats. Om en antalskoppling till exempel tas bort utan att någon ny koppling skapas, skapas en ny koppling när kopplingsformuläret stängs. På så sätt förblir kostnaden intakt. Observera dock att ingen ny fast koppling skapas automatiskt i programmet när kalkylarket stängs, om en fast koppling har tagits bort. Detta måste göras manuellt genom att skapa en ny koppling i kalkylarket.
    - Det går att ta bort kopplingar från mer än en transaktion åt gången i kopplingsformuläret. Det går däremot inte att skapa en koppling för mer än en transaktion åt gången, eftersom kopplingen påverkar uppsättningen transaktioner som kan kopplas.
    - I följande fall kan ingen koppling utföras i kopplingsformuläret: Om det inte finns tillräckligt med antal i lager för kopplingen, utförs ingen koppling i kopplingsformuläret när användaren försöker att koppla en transaktion för en lagerminskning utan artikelspårningsinformation till en transaktion för en lagerökning med artikelspårningsinformation.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Ta bort en artikelkoppling med hjälp av kopplingsformulär  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplingsformulär** och välj sedan relaterad länk.  
2.  Sidan **Kopplingsformulär** öppnas och visar befintliga artikeltransaktioner för alla artiklar.  
3.  Ange filter på Snabbfliken **Allmänt** för att göra det enklare att hitta den artikeltransaktion för vilken kopplingen ska ändras.  
4.  Välj aktuell artikeltransaktion och klicka på åtgärden **Kopplade transaktioner**. Sidan **Visa kopplade transaktioner – Kopplade transaktioner** öppnas och visar de artikeltransaktioner som för närvarande är kopplade till den valda transaktionen.  
5.  Markera den artikeltransaktion för vilken kopplingen ska tas bort.  
6.  Välj åtgärden **Ta bort koppling**. Med den här åtgärden tas den artikeltransaktion bort som kopplar de två artikeltransaktionerna och i stället flyttas den till sidan **Visa kopplade transaktioner – Bortkopplade transaktioner**.  
7.  Stäng sidan **Visa kopplade transaktioner – Kopplade transaktioner**.  

 Fältet **Återstående antal** för de båda artikeltransaktionerna ökas med det antal som nu är okopplat. Den borttagna artikeltransaktionen är nu tillgänglig för koppling igen på sidan **Visa kopplade transaktioner – bortkopplade transaktioner**.  

> [!IMPORTANT]  
>  Du bör inte lämna bortkopplade kopplingstransaktioner för längre perioder, eftersom andra användare inte kan behandla de aktuella artiklarna förrän du kopplar om kopplingstransaktionerna eller stänger sidan **Kopplingsformulär**. Följande felmeddelande visas om du försöker att utföra åtgärder som omfattar en manuellt bortkopplad transaktion:  
>   
>  **Det går inte att utföra åtgärden eftersom kopplingar för transaktionerna för artikel <item> har tagits bort i Kopplingsformuläret av användaren <user>.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Koppla om en artikelkoppling med hjälp av kopplingsformuläret  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kopplingsformulär** och välj sedan relaterad länk.  
2.  Sidan **Kopplingsformulär** öppnas och visar befintliga artikeltransaktioner för alla artiklar.  
3.  Om du vill koppla om transaktioner som togs bort sedan förslaget öppnades markerar du den artikeltransaktionspost som du vill koppla om, och väljer sedan åtgärden **Omkoppla**.  

    > [!NOTE]  
    >  Denna omkoppling till det ursprungliga saldot sker också automatiskt när du stänger sidan **Kopplingsformulär**.  
4.  Markera den artikeltransaktion som du vill koppla om du vill koppla en tillgänglig öppen artikeltransaktion till en annan transaktion. Välj åtgärden **Bortkopplade transaktioner**. Sidan **Visa kopplade transaktioner – Bortkopplade transaktioner** öppnas.  
5.  Markera en eller flera artikeltransaktioner som ska kopplas till den transaktion som är markerad på sidan **Kopplingsformulär**. Klicka därefter på **OK**.  

     En artikelkopplingstransaktion skapas mellan de två artikeltransaktionerna. Fälten **Återstående antal** för de två transaktionerna minskas med det kopplade antalet.  

    > [!NOTE]  
    >  Om du valt att göra en koppling utan att veta om att kopplingen medför att en oändlig loop skapas i kostnadsjusteringsprocessen utförs inte kopplingen du föreslagit. Det här kan ske när de ursprungliga transaktionerna har genererat ett negativt lager. Kopplingen utförs inte. Därför måste du välja en annan transaktion för kopplingen.  
6.  Om fältet **Automatisk kostnadsjustering** har värdet **Alltid** i **Lagerinställningar**, körs batch-jobbet för kostnadsjustering automatiskt i programmet när en omkoppling har gjorts. Kör annars batch-jobbet **Justera kost. - artikeltrans** för att säkerställa att samtliga kostnader är aktuella.  

## <a name="see-also"></a>Se även  
[Avsluta öppna artikeltransaktioner som skapas från en fast koppling i artikeljournalen](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Behandla inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md)  
 [Hantera lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Artikelkoppling](design-details-item-application.md)  
 [Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

---
title: Definiera en PIA-metod och övervaka projektets framsteg | Microsoft Docs
description: Beskriver hur du skapar en PIA-metod och beräknar PIA för att uppskatta det ekonomiska värdet i lika jobb medan de pågår.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d88424e055d42b829da769c12382d76e0b40014d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780538"
---
# <a name="monitor-job-progress-and-performance"></a>Övervaka projektframsteg och -resultat
Allt eftersom ett projekt fortlöper används material och resurser och de, och andra kostnader, måste bokföras i projektet. Produkter i arbete (PIA) är en funktion som gör att du kan uppskatta värdet i projektet i redovisningen medan projekten pågår. I många fall kan du bokföra kostnader för ett projekt innan du fakturerar projektet. Om endast kostnader bokförts blir er finansiella rapport oriktig. Mer information finns i [Förstå PIA-metoder](projects-understanding-wip.md).

Om du vill hålla reda på värdet i redovisningen kan du beräkna PIA (Produkter i arbete) och bokföra värdet i redovisningen.

Du kan beräkna PIA baserat på:

* Kostnadsvärde
* Försäljningsvärde
* Identifierbar kostnad
* Färdigställningsgrad
* Slutfört kontrakt

Om du vill visa resultatet med någon annan metod ändrar du metoden och beräknar om PIA. Det finns ingen gräns för hur många gånger du kan beräkna PIA. PIA beräknas bara, det bokförs inte i redovisningen. När du har beräknat PIA kan du bokföra det i redovisningen.

## <a name="to-create-a-job-wip-method"></a>Skapa en PIA-metod för projektet
Du kan skapa en PIA-metoden för projektet som visar behoven i organisationen. När du har skapat detta kan du ange vilken PIA-beräkningsmetod som ska användas som standard i organisationen.  

> [!NOTE]
> När du har använt den nya metoden för att skapa PIA-transaktioner kan du inte ta bort metoden eller ändra den.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **PIA-metoder för projekt** och välj sedan tillhörande länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Stäng sidan.   
4. För att göra den nya metoden till standard väljer du ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), anger **Projektinställningar** och väljer sedan tillhörande länk.  
5. I fältet **Standard-PIA-metod** väljer du metoden i listan.

## <a name="to-define-a-wip-method-for-a-job"></a>Så här definierar du en PIA-metod för ett projekt
När du skapar ett nytt projekt måste du ange vilken PIA-metod för projektet som gäller. I vissa fall har metoden för PIA-redovisningstransaktioner för projekt, som du kan använda, ställts in för dig som standard.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan tillhörande länk.
2. Välj åtgärden **Ny**. Mer information finns i [Skapa projekt](projects-how-create-jobs.md).  
3. PÅ sidan **Projektkort**, i fältet **PIA-metod**, väljer du en PIA-metod i listan. Om en standardmetod har definierats, kan du välja ett annat alternativ vid behov.  

## <a name="to-calculate-wip"></a>Så här beräknar du PIA
Du kan fastställa PIA-beloppet som ska bokföras på balansräkningskonton för periodslutsrapporteringen. Du kan använda batch-jobbet **Projekt – Beräkna PIA** om du vill göra detta.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt – Beräkna PIA** och välj sedan tillhörande länk.  
2. Välj åtgärden **Beräkna PIA**.
3. På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.
4. Välj knappen **OK**.  

> [!NOTE]  
>   Batch-jobbet beräknar bara PIA. Detta bokförs inte i Redovisning. Om du vill bokföra måste du köra batch-jobbet **Bokför PIA i redovisning** när du har beräknat PIA. Mer information finns i följande procedur:

## <a name="to-post-wip"></a>Bokföra PIA
När du har beräknat PIA kan du bokföra det på balansräkningskonton för rapportering vid periodens slut. Använd batch-jobbet **Projekt – Bokför PIA i redovisning** om du vill göra detta.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt – Bokför PIA i redovisning** och välj sedan tillhörande länk.  
2. På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.  
3. Välj knappen **OK**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Så här visar du projektförbrukning och uppskattningar och bokföruppdateringar
Du kan visa projektförbrukningen fram till projektet avslutas i ett steg. Det gör du genom att använda batch-jobbet **Projekt – Beräkna återstående förbrukning** för alla aktiviteter fram till och med projektets slut.  

Då kan du spåra och jämföra de ursprungliga uppskattningarna mot faktiskt resultat och göra ändringar eller nya transaktioner efter behov. Du kanske till exempel har uppskattat att ett projekt kräver tio timmar, och fram till dagens datum har det tagit 15 timmar. Du kan lägga till dessa extra fem timmar på den befintliga journalraden eller skapa en ny journalrad om du vill rapportera dessa fem timmar som övertid, som är en annan arbetstyp. Rätt kostnad och pris beräknas, och du kan sedan bokföra detta i journalen.  

> [!NOTE]  
>   Artikeltransaktioner skapar artikeltransaktioner och minskar lagerkvantiteten. Batch-jobbet **Bokför lagerkostnad i redov.** överför kostnaden från lagret till redovisningen. Resurstransaktioner skapar resurstransaktioner.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projektjournaler** och välj sedan relaterad länk.  
2. Välj en relevant projektjournal och välj sedan åtgärden **Ber. återstående förbrukning**.  
3. På sidan **Ber. återstående förbrukning** anger du dokumentnumret och bokföringsdatumet som ska infogas i journalen och väljer sedan knappen **OK**.  
4. Uppdatera journalen med eventuella ändringar som kan behövas.  
5. Välj **Bokföra**.

## <a name="to-view-job-ledger-entries"></a>Så här visar du projekttransaktioner
Alla projektrelaterade transaktioner registreras i bokförda projektjournaler och numreras i ordningsföljd med start från nummer ett. I den bokförda projektjournalen kan du få en överblick över alla projekttransaktioner.    

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda projektjournaler** och välj sedan tillhörande länk.
2. Välj en relevant journal och välj sedan åtgärden **Projekttransaktioner**.

På sidan **Projekttransaktioner** kan du granska de transaktioner som är kopplade till alla projekt.  

## <a name="see-also"></a>Se även
[Hantera projekt](projects-manage-projects.md)
[hantera lagerkostnader](finance-manage-inventory-costs.md)   
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
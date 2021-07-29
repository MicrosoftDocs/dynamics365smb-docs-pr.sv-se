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
ms.openlocfilehash: 052a0ecbe3b5435a2d73f377bb4ac0f4c4373f58
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443824"
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

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **PIA-metoder för projekt** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Stäng sidan.   
4. För att göra denna nya metod till standard, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projektinställningar** och väljer sedan relaterad länk.  
5. I fältet **Standard-PIA-metod** väljer du metoden i listan.

## <a name="to-define-a-wip-method-for-a-job"></a>Så här definierar du en PIA-metod för ett projekt
När du skapar ett nytt projekt måste du ange vilken PIA-metod för projektet som gäller. I vissa fall har metoden för PIA-redovisningstransaktioner för projekt, som du kan använda, ställts in för dig som standard.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**. Mer information finns i [Skapa projekt](projects-how-create-jobs.md).  
3. PÅ sidan **Projektkort**, i fältet **PIA-metod**, väljer du en PIA-metod i listan. Om en standardmetod har definierats, kan du välja ett annat alternativ vid behov.  

## <a name="to-calculate-wip"></a>Så här beräknar du PIA
Du kan fastställa PIA-beloppet som ska bokföras på balansräkningskonton för periodslutsrapporteringen. Du kan använda batch-jobbet **Projekt – Beräkna PIA** om du vill göra detta.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt – Beräkna PIA** och väljer sedan relaterad länk.  
2. Välj åtgärden **Beräkna PIA**.
3. På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.
4. Välj knappen **OK**.  

> [!NOTE]  
>   Batch-jobbet beräknar bara PIA. Detta bokförs inte i Redovisning. Om du vill bokföra måste du köra batch-jobbet **Bokför PIA i redovisning** när du har beräknat PIA. Mer information finns i följande procedur:

## <a name="to-post-wip"></a>Bokföra PIA
När du har beräknat PIA kan du bokföra det på balansräkningskonton för rapportering vid periodens slut. Använd batch-jobbet **Projekt – Bokför PIA i redovisning** om du vill göra detta.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt – Bokför PIA i redovisning** och väljer sedan relaterad länk.  
2. På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.  
3. Välj **OK**.

## <a name="to-calculate-and-post-job-completion-entries"></a>Beräkna och bokföra slutförda projekt
När du har slutfört alla aktiviteter i ett projekt, bland annat bokföringen och faktureringen av förbrukning, måste du uppdatera projektet så att projektet får **Statusen** **Slutförd**. Sedan måste du återföra alla PIA som har bokförs i redovisningen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj ett öppet projekt och välj sedan åtgärden **Redigera**.
3. Markera **Slutförd** i fältet **Status** .
4. Följ hjälpstegen steg för att beräkna och bokföra PIA. Följ alternativt steg 5 och 6 för att göra det manuellt.  
5. Välj åtgärden **Beräkna PIA**.
6. På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.  

     De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.  
7. Välj åtgärden **Projekt – Bokför PIA i redovisning**.
8. På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.  

     De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.

## <a name="to-view-job-ledger-entries"></a>Så här visar du projekttransaktioner
Alla projektrelaterade transaktioner registreras i bokförda projektjournaler och numreras i ordningsföljd med start från nummer ett. I den bokförda projektjournalen kan du få en överblick över alla projekttransaktioner.    

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **projektjournaler** och väljer sedan relaterad länk.
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

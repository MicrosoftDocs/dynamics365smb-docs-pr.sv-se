---
title: Så här arbetar du med serviceuppgifter
description: I det här avsnittet beskrivs olika sätt att arbeta med serviceuppgifter. Sidan Serviceuppgifter där du får en översikt över alla serviceartiklar som behöver åtgärdas.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 2ca1e1d49c2d86219388493e32a1e97fd536ae96
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136827"
---
# <a name="work-on-service-tasks"></a>Arbeta med tjänsteuppgifter
När du har skapat en serviceorder eller serviceoffert, registrerat serviceartikelrader och fördelat resurser på orderns eller offertens serviceartiklar kan du börja reparera och underhålla serviceartiklarna.  

I [!INCLUDE[prod_short](includes/prod_short.md)] innehåller sidan **Serviceuppgifter** där du får en översikt över alla serviceartiklar som behöver åtgärdas. Du kan se det som en instrumentbräda för service – se vilka order som väntar på att åtgärdas, söka efter och registrera reservdelar och hålla lagret uppdaterat.  

Om du vill spåra ändringar och få en grafisk översikt över serviceverksamheten, kan du med statistikverktygen i [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt skapa en snabb analys i diagramformat.  

## <a name="to-work-on-a-service-task"></a>Så här arbetar du med serviceuppgifter  
1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Om du vill ha en lista över serviceuppgifterna som en viss resurs/resursgrupp är fördelad till, fyller du i fältet **Resursfilter**/ **Resursgruppfilter** och trycker på RETUR.  
3. Om du vill ha en lista över serviceuppgifter med ett visst svarsdatum eller svarsdatum inom en viss tidsperiod, fyller du i fältet **Svarsdatumfilter** och trycker på RETUR.  
4. Om du vill ha en lista över serviceuppgifter med en viss fördelningsstatus/reparationsstatus fyller du i fältet **Fördelningsstatusfilter** eller **Reparationsstatus kodfilter** och trycker på RETUR.  
5. Markera serviceuppgiften som du vill arbeta med. Välj åtgärden **Artikelkalkylark**. Sidan **Serviceartikeldokument** öppnas.  
6. Registrera standardtext, reservdelar, resurstid och kostnader med hjälp av motsvarande alternativ i fältet **Typ**:  \<Blank\>, **Artikel**, **Resurs**, och **Kostnad**.  
7. I fältet **Reparationsstatus** markerar du lämplig status.  

   > [!NOTE]  
   >  Fyll i fältet **Reparationsstatus** med statusvärdet **Avslutad** eller **Delvis servad** om serviceartikeln har avslutats eller om en annan resurs ska fortsätta med servicen. Statusvärdet **Avslutad** eller **Omfördelning nödvändig** väljs automatiskt för den här serviceartikelns fördelningstransaktion.  

## <a name="to-register-service-operations"></a>Så här registrerar du serviceoperationer  
När du utför en service på en serviceorder kan du registrera detaljerad information om de artiklar som använts, uppkomna kostnader och tidsåtgång. Den information som du anger lagras på sidan **Serviceartikeldokument**. Du kan uppdatera informationen när det behövs.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna serviceordern som du vill registrera service för och välj artikelrad.  
3. Välj åtgärden **Serviceartikeldokument**.  
4. På raderna anger du de artiklar som använts, uppkomna kostnader och tidsåtgång.  

   > [!NOTE]  
   >  Du kan också registrera en service direkt på de servicerader som är kopplade till serviceordern.  

## <a name="to-register-spare-parts"></a>Så här registrerar du reservdelar  
När du arbetar med serviceartiklar i serviceorder kanske du behöver använda reservdelar till servicen. Nedan beskrivs en procedur för att registrera reservdelarna som du använder på sidan **Serviceartikeldokument**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Klicka på raden som innehåller relevant serviceartikel och klicka på **Artikelkalkylark**.  
3. Ange en ny servicerad.  
4. I fältet **Typ** väljer du **Artikel**.  
5. I fältet **Nr.** markera relevant reservdel.  
6. I fältet **Antal** anger du hur många artiklar du vill använda.  

 Du kan använda en liknande procedur för att registrera reservdelarna på sidan **Servicerader** som du öppnar från sidan **Tjänsteorder**.  

## <a name="to-register-spare-parts-from-a-service-order"></a>Registrera reservdelar från en serviceorder  
1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna serviceordern som du vill registrera reservdelar för.  
3. Välj den rad som innehåller aktuell serviceartikel. Välj **Åtgärder**, välj **Order**, och sedan **Servicerader**.  
4. Ange en ny servicerad.  

## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Så här ersätter du en serviceartikel eller en Serviceartikelkomponent  
När du servar en serviceartikel som innehåller komponenter kanske du måste byta ut trasiga komponenter mot nya. När du anger en reservdel för en serviceartikel med komponenter kan du välja mellan att ersätta komponenten eller skapa en ny. Den nya artikeln registreras inte som komponent i serviceartikeln förrän du bokför serviceraden eller serviceordern.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 5.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Klicka på raden som innehåller relevant serviceartikel och klicka på **Artikelkalkylark**.  
3. Ange en ny servicerad.  
4. I fältet **Typ** väljer du **Artikel**.  
5. I fältet **Nr.** Välj komponenten som ska ersättas.  
6. Tryck på **Retur**. En dialogruta visas med tre alternativ: **Ersätt komponent**, **Ny komponent** och **Ignorera**. Alternativen beskrivs i tabellen nedan.  

    |Alternativ | Description|  
    |----------------------------------|---------------------------------------|  
    |**Ersätt komponent**|Status för den komponent som ska ersättas ändras till ej aktiv och den visas på listan över ersatta komponenter för serviceartikeln.|  
    |**Ny komponent**|Den nya komponenten infogas på komponentlistan för serviceartikeln.|  
    |**Ignorera**|Ingenting händer med serviceartikelns komponentlista.|  

7. Välj **Ersätt komponent**.  
8. Välj komponenten som ska ersättas och välj sedan **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Så här ändrar du svarstid för en serviceartikelrad  
När du registrerar en serviceartikelrad i en serviceorder eller offert om serviceartikeln finns i ett servicekontrakt anges automatiskt standardsvarstiden i timmar. Svarsdatum och svarstid beräknas därefter. Du kan ändra svarstiden i timmar och svarsdatum och svarstid om du vill.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 6.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Serviceorder** eller **Serviceofferter** och sedan väljer du relaterad länk.  
2. Välj den serviceorder eller serviceoffert som du vill öppna kortet.  
3. På den serviceartikelrad som du vill ändra svarstid för i fältet **Svarstid (timmar)** eller i fälten **Svarsdatum** och **Svarstid** anger du nya svarstimmar eller svarsdatum och svarstid.  

## <a name="to-register-faultresolution-codes"></a>Så här registrerar du fel/åtgärdskoder  
När en serviceartikel har reparerats kan du ange både felkoden och åtgärdskoden för artikeln genom att välja en kombination från de befintliga fel- och åtgärdskodssambanden. De fel- och åtgärdskoder som valts visas nu i motsvarande fält på sidan **Serviceartikeldokument**. Du kan också registrera koderna direkt i på den här sidan.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 7.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Klicka på raden som innehåller relevant serviceartikel och klicka på **Artikelkalkylark**.  
3. På sidan **Serviceartikeldokument** väljer du **Fel- och åtgärdssamband koder**. Sidan **Fel-/åtgärdssambandskoder** öppnas.  

  >  [!NOTE]
  >  Filter sätts på de samband som visas på sidan via kopiering av serviceartikelgruppen och felkoderna från sidan **Serviceartikeldokument**.  

4. Fyll i raden. Välj rätt kombination av fel- och åtgärdskoder och klicka sedan på **OK** för att kopiera den till serviceartikeln. Om någon lämplig kombination inte finns kan du skapa en ny kombination på sidan.  

## <a name="see-also"></a>Se även  
[Så här ställer du in felrapporteringsnivån](service-how-setup-fault-reporting.md)
[fördelningsstatus och reparationsstatus](service-allocation-status-and-repair-status.md)  
[Servicebokföring](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
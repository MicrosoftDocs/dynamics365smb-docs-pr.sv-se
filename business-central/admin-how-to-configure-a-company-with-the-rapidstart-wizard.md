---
title: "Så här konfigurerar du ett företag med RapidStart-guiden | Microsoft Docs"
description: "Du kan snabbt konfigurera ett nytt företag som du har skapat genom att använda konfigurationsguiden för RapidStart Services."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4dd595fabbf8e4cd2a3eef73a934922dfea92858
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Så här konfigurerar du ett företag med RapidStart-guiden
Du kan snabbt konfigurera ett nytt företag som du har skapat genom att använda konfigurationsguiden för RapidStart Services.

I följande procedur har du gett kunden ett konfigurationspaket, som sedan har installerats på en dator. Kunden öppnar det nya företaget, som inte innehåller några kunddata. Du eller kunden följer sedan stegen i RapidStart Services-guiden, som beskrivs i den här proceduren, för att ange grundläggande information om företaget. Guiden importerar konfigurationspaketet och kopplar sedan paketet till företaget.  

## <a name="to-configure-a-new-company"></a>Så här konfigurerar du ett nytt företag  
1. I implementerings-rollcentret för RapidStart Services väljer du åtgärden **RapidStart-guide**.  
2. Expandera snabbfliken **Steg 1** , som innehåller allmän information om det nya företaget. Ange lämplig information om det nya företaget i fälten. Det finns ett fält som du måste du fylla i. Fältet **Namn**. Det är frivilligt att fylla i övriga fält.  
3. Expandera snabbfliken **Steg 2**, som innehåller kommunikations- och kontaktinformation om det nya företaget. Ange lämplig information om det nya företaget i fälten.
4. Expandera snabbfliken **Steg 3**, som innehåller information om bankkonto och betalning för det nya företaget. Ange lämplig information om det nya företaget i fälten.  
5. Expandera snabbfliken **Steg 4**. Välj knappen **AssistEdit** och väljer konfigurationspaketet som du vill koppla. Namnet på konfigurationspaketet som visas. Sedan kan du utföra följande åtgärder, i den angivna ordningen:  

    1. Koppla konfigurationen genom att välja åtgärden **Koppla paket**. Då importeras konfigurationspaketet och alla paketdatabasdata kopplas på samma gång.  

    2. Granska konfigurationen när den har kopplats. Med det här alternativet kan du granska konfigurationsdetaljer och frågeformulär som tillhandahålls av partnern och importera en del huvuddata som krävs för företaget. Välj åtgärden **Konfigurationskalkylark**. Mer information finns i avsnittet ”Så här slutför du konfigurationsfrågeformuläret” i [Samla inställningsvärden för kund](admin-gather-customer-setup-values.md).  

6. Expandera snabbfliken **Steg 5**. Ange vilket rollcenter som du vill ange som standard för det nya företaget.  

    > [!IMPORTANT]  
    >  Ändra bara ditt rollcenter när du har fyllt i konfigurationen av företaget. Om du har registrerat fler detaljer som du överväger att ändra, använder du först konfigurationskalkylarket och fortsätter med arbetet. Gå sedan tillbaka till guiden för att uppdatera din rollcenterprofil, eller välj åtgärden **Slutför inställningar**.

7. Välj knappen **OK**.  
8. Om du vill kontrollera att konfigurationsinformationen har kopplats till det nya företaget väljer du ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), anger **Företagsinformation** och väljer sedan relaterad länk.

Sidan **Företagsinformation** innehåller information som du har angett.   

Du har nu konfigurerat företaget och kopplat data till det.  

## <a name="see-also"></a>Se även  
[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


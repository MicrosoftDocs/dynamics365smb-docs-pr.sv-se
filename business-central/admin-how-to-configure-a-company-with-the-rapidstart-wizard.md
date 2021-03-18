---
title: Så här konfigurerar du ett företag med RapidStart-guiden | Microsoft Docs
description: Du kan snabbt konfigurera ett nytt företag som du har skapat genom att använda konfigurationsguiden för RapidStart Services.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9fb74bcf0b124dddc14d9441cdbfb4fc9116d3e2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378429"
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Så här konfigurerar du ett företag med RapidStart-guiden
Du kan snabbt konfigurera ett nytt företag som du har skapat genom att använda konfigurationsguiden för RapidStart Services.

I följande procedur har du gett kunden ett konfigurationspaket, som sedan har installerats på en dator. Kunden öppnar det nya företaget, som inte innehåller några kunddata. Du eller kunden följer stegen i guiden RapidStart Services som beskrivs i den här proceduren, för att ange grundläggande information om företaget. Guiden importerar konfigurationspaketet och kopplar sedan paketet till företaget.  

## <a name="to-configure-a-new-company"></a>Så här konfigurerar du ett nytt företag  
1. På implementerings-rollcentret för RapidStart Services väljer du åtgärden **RapidStart-guiden**.  
2. Expandera snabbfliken **Steg 1** , som innehåller allmän information om det nya företaget. Ange lämplig information om det nya företaget i fälten. Det finns ett fält som du måste du fylla i. Fältet **Namn**. Det är frivilligt att fylla i övriga fält.  
3. Expandera snabbfliken **Steg 2**, som innehåller kommunikations- och kontaktinformation om det nya företaget. Ange lämplig information om det nya företaget i fälten.
4. Expandera snabbfliken **Steg 3**, som innehåller information om bankkonto och betalning för det nya företaget. Ange lämplig information om det nya företaget i fälten.  
5. Expandera snabbfliken **Steg 4**. Välj knappen **AssistEdit** och väljer konfigurationspaketet som du vill koppla. Namnet på konfigurationspaketet som visas. Sedan kan du utföra följande åtgärder, i den angivna ordningen:  

    1. Koppla konfigurationen genom att välja åtgärden **Koppla paket**. Då importeras konfigurationspaketet och alla paketdatabasdata kopplas på samma gång.  

    2. Granska konfigurationen när den har kopplats. Med det här alternativet kan du granska konfigurationsdetaljer och frågeformulär som tillhandahålls av partnern och importera en del huvuddata som krävs för företaget. Välj åtgärden **Konfigurationskalkylark**. Mer information finns i [Så här: Slutför konfigurationsfrågeformuläret](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Expandera snabbfliken **Steg 5**. Ange vilket rollcenter som du vill ange som standard för det nya företaget.  

    > [!IMPORTANT]  
    >  Ändra bara ditt rollcenter när du har fyllt i konfigurationen av företaget. Om du har registrerat fler detaljer som du överväger att ändra, använder du först konfigurationskalkylarket och fortsätter med arbetet. Gå sedan tillbaka till guiden för att uppdatera din rollcenterprofil, eller välj åtgärden **Slutför inställningar**.

7. Välj knappen **OK**.  
8. Om du vill kontrollera att konfigurationsinformationen har kopplats till det nya företaget väljer du ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Företagsinformation** och väljer sedan relaterad länk.

Sidan **Företagsinformation** innehåller information som du har angett.   

Du har nu konfigurerat företaget och kopplat data till det.  

## <a name="see-also"></a>Se även  
[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
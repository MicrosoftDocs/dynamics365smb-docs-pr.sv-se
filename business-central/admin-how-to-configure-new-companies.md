---
title: "Så här konfigurerar du nya företag | Microsoft Docs"
description: "Du kan konfigurera och anpassa ett nytt företag som du har skapat. Om du vill finjustera implementeringen fortsätter du i tre faser för att slutföra konfigurationen."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a52a95bf3fc96b89e664041e3d2b289b6042c046
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="configure-new-companies"></a>Konfigurera nya företag
Om du vill konfigurera ett nytt företag i din lösningsimplementering följer du vanligtvis tre faser. I den första fasen importerar du ett konfigurationspaket som är en .rapidstart-fil med konfigurationsinformation. I den andra fasen ändrar du konfigurationsinformationen och tillämpar den sedan i det nya företaget. I slutfasen granskar du och rättar eventuella fel.  

Följande procedur förutsätter att du har skapat och sparat ett konfigurationspaket. För mer information, se [Förbereda ett konfigurationspaket](admin-how-to-prepare-a-configuration-package.md).  

Följande förfaranden förutsätter att du har initialiserat och öppnat ditt nya företag, samt att du använder implementerings-rollcentret för RapidStart Services.

## <a name="to-import-a-configuration-package"></a>Så importerar du ett konfigurationspaket  
1. Öppna det nya företaget i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  
2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationspaket** och välj sedan relaterad länk.  
3. Välj åtgärden **Importera paket**.  
4. Navigera till den plats där du har sparat .rapidstart-konfigurationspaketet och välj sedan knappen **Öppna**.  
5. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Företagsinformation** och välj sedan relaterad länk. Ange information om företaget på företagsinformationskortet. Ta med information som till exempel bankdetaljer. Du kan även ange en logotyp för företaget.  

Alla tabeller som du har tilldelat för att ta med i det nya företaget importeras. I det här läget kan du koppla paketdata till databasen eller justera och ändra tabelldata för att uppfylla kundens specifikationer.  

## <a name="to-apply-package-data"></a>Så här kopplar du paketdata  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.  
2. Välj en tabell som du vill modifiera data för, och välj sedan åtgärden **Koppla data**. Välj knappen **Ja** för att bekräfta kopplingen.
3. Återgå till sidan **Konfig. kalkylblad** och välj åtgärden **Databasdata** för att bekräfta att datan nu finns i databasen och att kopplingen har lyckats.  

> [!NOTE]  
>  När du har kopplat data kan du endast se dem i databasen. De finns inte längre i paketet.  

## <a name="to-modify-and-apply-package-data"></a>så här kan du ändra och koppla paketdata  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.  
2. Välj en tabell som du vill modifiera data för, och välj sedan åtgärden **Paketera data**.  
3. På sidan **Konfig. paketposter** gör du dina ändringar. Du kan till exempel ta bort alternativ som inte används.  
4. Välj åtgärden **Koppla data** och sedan knappen **OK**.  
5. Återgå till sidan **Konfig. kalkylblad** och välj åtgärden **Databasdata** för att bekräfta att datan nu finns i databasen och att kopplingen har lyckats.  

## <a name="to-locate-and-identify-a-configuration-error"></a>så här kan du hitta och identifiera ett konfigurationsfel  
Det finns vissa typer av fel som kan uppstå när du kopplar data till en databas. Det vanligaste felet är inte att ta med alla relaterade tabeller som behövs. Du kan åtgärda felen i konfigurationskalkylbladet.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationspaket** och välj sedan relaterad länk.  
2. Markera det paket som du vill granska och välj åtgärden **Redigera**.  

    Tabeller som innehåller fel markeras. Antalet paketfel visas i fältet **Antal paketfel**.  

3. Välj fältet **Antal paketfel** för att öppna sidan **Konfig. paketposter**, som listar de poster som innehåller fel.  

### <a name="to-fix-an-error"></a>Så här kan du lösa ett fel  
1. Öppna företaget som baseras på ditt konfigurationspaket.  
2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.  
3. Korrigera fel genom att exempelvis lägga till saknade relaterade tabeller i kalkylbladet.  
4. Lägg till tabellerna i ett befintligt konfigurationspaket eller skapa ett nytt paket som innehåller endast de nya tabellerna. För mer information, se [Förbereda ett konfigurationspaket](admin-how-to-prepare-a-configuration-package.md).  
5. Öppna det nya företaget som du använder konfigurationen för igen.  
6. Importera konfigurationspaketet.  

    > [!NOTE]  
    >  Om du importerar samma paket igen kan du skriva över alla dataändringar som du redan har skapat. Därför kanske du vill lägga till nya tabeller i ett nytt paket och importera det i stället.  

7. Koppla datan till databasen enligt beskrivningen i avsnittet "Att ändra och koppla paketdata".

## <a name="see-also"></a>Se även  
[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)


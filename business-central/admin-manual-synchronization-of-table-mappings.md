---
title: Manuell synkronisering av tabellmappningar | Microsoft Docs
description: Synkroniseringen kopierar data mellan Dynamics 365 for Sales-transaktioner och Business Central så att båda systemen hålls uppdaterade.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 71284c8a2824e63c21768f2db55edb501486424d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629556"
---
# <a name="manually-synchronize-table-mappings"></a>Synkronisera manuellt tabellmappning
En integrationstabellmappning associerar en [!INCLUDE[d365fin](includes/d365fin_md.md)] tabell (posttyp), till exempel kund, med en [!INCLUDE[crm_md](includes/crm_md.md)] enhet, exempelvis ett konto. Synkronisera en mappning för integrationstabellen låter dig synkronisera data i alla poster i den [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell och [!INCLUDE[crm_md](includes/crm_md.md)]-enhet som används. Dessutom, beroende på konfigurationen av tabellmappningen, kan synkronisering skapa och koppla nya poster i destinationslösningen ej kopplade poster i källan.  

Manuellt synkroniserade integrationstabellmappningarna kan användas under den inledande inställningen av en integration och vid diagnos av synkroniseringsfel.  

Den här artikeln beskriver tre metoder för att manuellt synkronisera integrationstabellmappningar. Varje metod ger olika nivåer av synkronisering.

## <a name="run-a-full-synchronization"></a>Kör en fullständig synkronisering
En fullständig synkronisering kör alla standardintegrationssynkroniseringsjobb för synkronisering av [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster och [!INCLUDE[crm_md](includes/crm_md.md)]-enheter, enligt definitionen på sidan **Tabellmappningar för integrering**. 

En fullständig synkronisering utför följande åtgärder för [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]-poster som är:

* Inte kopplade, en ny matchande post skapas och kopplas i den andra lösningen.
Om och när en post skapas beror på synkroniseringsriktningen. Till exempel när du synkroniserar data från [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder till [!INCLUDE[crm_md](includes/crm_md.md)]-konto, om det finns en kund som inte är kopplad till ett konto, skapas ett nytt konto och läggs automatiskt till i [!INCLUDE[crm_md](includes/crm_md.md)] och kopplas till kunden [!INCLUDE[d365fin](includes/d365fin_md.md)]. Motsatsen gäller när synkroniseringsriktningen är från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)]. För varje konto som inte redan är kopplat till en kund, skapas en ny motsvarande kund i [!INCLUDE[d365fin](includes/d365fin_md.md)] och kopplas till kontot i [!INCLUDE[crm_md](includes/crm_md.md)].  

     > [!NOTE]  
     >  För att uppnå fullständig synkronisering tillfälligt tar bort alternativet **Synka endast kopplade poster** på integrationstabellmappningen som används för synkroniseringsjobbet. I slutet av den fullständiga synkroniseringsprocessen uppmanas du att om du vill hålla det här alternativet avmarkerat för alla jobb.  

* Kopplad är riktningen för synkroniseringen (t.ex från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] eller från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)]) förbestämd av integrationstabellmappningar. Mer information finns i [Standardinställd försäljningsenhetsmappningar för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization).  

Jobben körs i följande ordning för att undvika kopplingsberoenden mellan posterna.  

1.  VALUTA - Dynamics 365 for Sales synkroniseringsjobb  
2.  SÄLJARE - Dynamics 365 for Sales synkroniseringsjobb  
3.  MÅTTENHET - Dynamics 365 for Sales synkroniseringsjobb  
4.  KUND - Dynamics 365 for Sales synkroniseringsjobb  
5.  KONTAKTER - Dynamics 365 for Sales synkroniseringsjobb  
6.  RESURS-PRODUKT - Dynamics 365 for Sales synkroniseringsjobb  
7.  ARTIKEL-PRODUKT - Dynamics 365 for Sales synkroniseringsjobb  

> [!IMPORTANT]  
>  Du kan bara använda fullständig synkronisering när du från början lägger upp integration mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] och endast en av lösningarna innehåller data som du vill kopiera till den andra lösningen. En fullständig synkronisering kan vara lämplig i demonstrationsmiljöer. Eftersom den fullständiga synkroniseringen skapas automatiskt och kopplar poster mellan lösningarna går det snabbare att arbeta med synkronisering av data mellan poster. Å andra sidan bör du bara köra en fullständig synkronisering om du vill ha en post i [!INCLUDE[d365fin](includes/d365fin_md.md)] för varje post i [!INCLUDE[crm_md](includes/crm_md.md)] för en given tabellmappning. Annars kan du kan få oönskade eller dubblettposter i antingen [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)].  

### <a name="see-the-process-for-a-full-synchronization"></a>Se processen för en fullständig synkronisering
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### <a name="to-run-a-full-synchronization"></a>Kör en fullständig synkronisering  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Microsoft Dynamics 365 for Sales anslutningsinställningar** och välj sedan relaterad länk.
2.  Välj åtgärden **Kör fullständig synkronisering** och välj sedan knappen **Ja** för att bokföra journalen.  
3.  När fullständig synkronisering har utförts kan du ange om du vill tillåta att schemalagda synkroniseringsjobb ska få skapa nya poster.  

    Om du vill att alla synkroniseringsjobb ska skapa nya poster i målet för ej kopplade poster i källan väljer du **Ja**. Detta anger fältet **Synka endast kopplade poster** på tabellmappningen som används av synkroniseringsjobbet.  

    Om du vill att synkroniseringsjobb ska köras som de gjorde innan fullständig synkronisering med hänsyn till hur du skapar nya poster väljer du **Nej**. Detta anger fältet **Synka endast kopplade poster** till den inställning den hade innan den fullständiga synkroniseringen.  

Du kan visa resultatet av en fullständig synkronisering på sidan **Integreringssynkroniseringsjobb**. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synkronisera alla ändrade poster
Använd sidan **Microsoft Dynamics 365 for Sales anslutningsinställningar** om du vill synkronisera ändringar i alla integrationstabellmappningar. Detta liknar en fullständig synkronisering. Den synkroniserar data i alla kopplade poster i de [!INCLUDE[d365fin](includes/d365fin_md.md)] tabeller och [!INCLUDE[crm_md](includes/crm_md.md)] enheter som har definierats i tabellmappningarna. Som standard synkroniseras endast poster som har ändrats sedan den senaste synkroniseringen. Tabellmappningen synkroniseras i följande ordning för att undvika kopplingsberoenden mellan enheterna:  

1.  VALUTA - Dynamics 365 for Sales synkroniseringsjobb  
2.  SÄLJARE - Dynamics 365 for Sales synkroniseringsjobb  
3.  MÅTTENHET - Dynamics 365 for Sales synkroniseringsjobb  
4.  KUND - Dynamics 365 for Sales synkroniseringsjobb  
5.  KONTAKTER - Dynamics 365 for Sales synkroniseringsjobb  
6.  Synkroniseringsjobbet \-Dynamics 365 for Sales RESURS-PRODUKT  
7.  ARTIKEL-PRODUKT - Dynamics 365 for Sales synkroniseringsjobb  

Du kan visa resultatet av en synkronisering på sidan **Integreringssynkroniseringsjobb**. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Genom att ändra integrationstabellmappningen i förväg kan du konfigurera synkronisering med filter för att bestämma vilka poster som ska synkroniseras eller konfigureras för att skapa nya poster i destinationslösningen för ej kopplade poster i källan. Mer information finns i [Ändra tabellmappningar för synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Synkronisera poster för alla tabeller  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Microsoft Dynamics 365 for Sales anslutningsinställningar** och välj sedan relaterad länk.
2.  Välj åtgärden **Synkronisera ändrade poster** och sedan **Ja**.  

## <a name="synchronize-individual-table-mappings"></a>Synkronisera individuella tabellmappningar
Använd **Tabellmappningar för integrering** för att köra ett synkroniseringsjobb specifikt för tabellmappningar. Detta synkroniserar data i alla kopplade poster i den [!INCLUDE[d365fin](includes/d365fin_md.md)] tabell och [!INCLUDE[crm_md](includes/crm_md.md)] enhet som har definierats av tabellmappningarna. Som standard synkroniseras endast poster som har ändrats sedan den senaste synkroniseringen.  

Genom att ändra integrationstabellmappningen i förväg kan du konfigurera synkroniseringsjobbet för att skapa nya poster i destinationslösningen för ej kopplade poster i källan.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Synkronisera poster i en integrationstabellmappning  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Tabellmappningar för integrering** och välj sedan relaterad länk.
2.  Välj åtgärden **Synkronisera ändrade poster** och sedan **Ja**.  

## <a name="see-also"></a>Se även  
[Synkroniserar Business Central och Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Ställa in konton för integrering med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)   

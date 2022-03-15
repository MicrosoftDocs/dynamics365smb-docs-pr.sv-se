---
title: Manuell synkronisering av registermappningar | Microsoft Docs
description: Synkroniseringen kopierar data mellan Microsoft Dataverse-register och Business Central så att båda systemen hålls uppdaterade.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: fd9ff4640b23dbd58c94d9da3f95ab9670710439
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381917"
---
# <a name="manually-synchronize-table-mappings"></a>Synkronisera manuellt registermappning


En integreringsregistermappning associerar ett [!INCLUDE[prod_short](includes/prod_short.md)]-register, till exempel kund, med ett [!INCLUDE[prod_short](includes/cds_long_md.md)]-register, exempelvis ett konto. Genom att synkronisera en mappning för integreringsregister kan du synkronisera data i alla poster i det [!INCLUDE[prod_short](includes/prod_short.md)]-register och det [!INCLUDE[prod_short](includes/cds_long_md.md)]-register som kopplas. Dessutom, beroende på konfigurationen av registermappningen, kan synkronisering skapa och koppla nya poster i destinationslösningen ej kopplade poster i källan.  

Manuellt synkroniserade integreringsregistermappningarna kan användas under den inledande inställningen av en integrering och vid diagnos av synkroniseringsfel.  

Den här artikeln beskriver tre metoder för att manuellt synkronisera integreringsregistermappningar. Varje metod ger olika nivåer av synkronisering.

## <a name="run-a-full-synchronization"></a>Kör en fullständig synkronisering
En fullständig synkronisering kör alla synkroniseringsjobb för standardintegrering för synkronisering av [!INCLUDE[prod_short](includes/prod_short.md)]-poster och [!INCLUDE[prod_short](includes/cds_long_md.md)]-register, enligt definitionen på sidan **Registermappningar för integrering**. 

En fullständig synkronisering utför följande åtgärder för [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)]-poster som är:

* En ny matchande, okopplad rad skapas och kopplas i den andra lösningen.
Om och när en rad skapas beror på synkroniseringsriktningen. Till exempel när du synkroniserar data från [!INCLUDE[prod_short](includes/prod_short.md)]-kunder till [!INCLUDE[prod_short](includes/cds_long_md.md)]-konto, om det finns en kund som inte är kopplad till ett konto, skapas ett nytt konto och läggs automatiskt till i [!INCLUDE[prod_short](includes/cds_long_md.md)] och kopplas till kunden [!INCLUDE[prod_short](includes/prod_short.md)]. Motsatsen gäller när synkroniseringsriktningen är från [!INCLUDE[prod_short](includes/cds_long_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)]. För varje konto som inte redan är kopplat till en kund, skapas en ny motsvarande kund i [!INCLUDE[prod_short](includes/prod_short.md)] och kopplas till kontot i [!INCLUDE[prod_short](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  För att uppnå fullständig synkronisering tillfälligt tar bort alternativet **Synka endast kopplade poster** på integreringsregistermappningen som används för synkroniseringsjobbet. I slutet av den fullständiga synkroniseringsprocessen uppmanas du att om du vill hålla det här alternativet avmarkerat för alla jobb.  

* Kopplad är riktningen för synkroniseringen (t.ex från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[prod_short](includes/cds_long_md.md)] eller från [!INCLUDE[prod_short](includes/cds_long_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)]) förbestämd av integreringsregistermappningar. Mer information finns i [Standardinställd registermappning för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Du kan bara använda fullständig synkronisering när du från början lägger upp integrering mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] och endast en av lösningarna innehåller data som du vill kopiera till den andra lösningen. En fullständig synkronisering kan vara lämplig i demonstrationsmiljöer. Eftersom den fullständiga synkroniseringen skapas automatiskt och kopplar poster mellan lösningarna går det snabbare att arbeta med synkronisering av data mellan poster. Å andra sidan bör du bara köra en fullständig synkronisering om du vill ha en rad i [!INCLUDE[prod_short](includes/prod_short.md)] för respektive rad i [!INCLUDE[prod_short](includes/cds_long_md.md)] för en given registermappning. Annars kan du kan få oönskade eller dubblettposter i antingen [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Kör en fullständig synkronisering  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av inställningen av Dataverse** och väljer sedan relaterad länk.

    > [!NOTE]
    > Om du vill köra en fullständig synkronisering för register via Dynamics 365 Sales använder du istället sidan **Inställning av anslutningar för Microsoft Dynamics 365 Sales**.

2.  Välj åtgärden **Kör fullständig synkronisering** och välj sedan knappen **Ja** för att bokföra journalen.  
3.  När fullständig synkronisering har utförts kan du ange om du vill tillåta att schemalagda synkroniseringsjobb ska få skapa nya poster.  

    Om du vill att alla synkroniseringsjobb ska skapa nya poster i målet för ej kopplade poster i källan väljer du **Ja**. Detta anger fältet **Synka endast kopplade poster** på registermappningen som används av synkroniseringsjobbet.  

    Om du vill att synkroniseringsjobb ska köras som de gjorde innan fullständig synkronisering med hänsyn till hur du skapar nya poster väljer du **Nej**. Detta anger fältet **Synka endast kopplade poster** till den inställning den hade innan den fullständiga synkroniseringen.  

Du kan visa resultatet av en fullständig synkronisering på sidan **Integreringssynkroniseringsjobb**. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synkronisera alla ändrade poster
Använd sidan **Common Data Service anslutningsinställningar** om du vill synkronisera ändringar i alla integrationsregistermappningar. Detta liknar en fullständig synkronisering. Detta synkroniserar data i alla kopplade poster i de [!INCLUDE[prod_short](includes/prod_short.md)]- och [!INCLUDE[prod_short](includes/cds_long_md.md)]-register som har definierats i registermappningarna. Som standard synkroniseras endast data som har ändrats sedan den senaste synkroniseringen. Synkroniseringsjobb synkroniserar registermappningar i följande ordning för att undvika kopplingsberoenden mellan registren:  

1.  VALUTA  
2.  SÄLJARE  
3.  LEVERANTÖR  
4.  KUND  
5.  KONTAKTER  

Du kan visa resultatet av en synkronisering på sidan **Integreringssynkroniseringsjobb**. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Genom att ändra integreringsregistermappningen i förväg kan du skapa filter för att bestämma vilka data som ska synkroniseras, eller konfigurera mappningar i syfte att skapa nya data i destinationslösningen för ej kopplade poster eller rader i källan. Mer information finns i [Ändra registermappningar för synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables"></a>Synkronisera data för alla register  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Microsoft Dynamics 365 Sales anslutningsinställningar** och väljer sedan relaterad länk.
2.  Välj åtgärden **Synkronisera ändrade poster** och sedan **Ja**.  

## <a name="synchronize-individual-table-mappings"></a>Synkronisera individuella registermappningar
Använd sidan **Registermappningar för integrering** för att köra ett synkroniseringsjobb för registermappningar. Detta synkroniserar data för alla kopplade poster och rader i de [!INCLUDE[prod_short](includes/prod_short.md)]- och [!INCLUDE[prod_short](includes/cds_long_md.md)]-register som har definierats av registermappningarna. Som standard synkroniseras endast data som har ändrats sedan den senaste synkroniseringen.  

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Synkronisera poster i en integreringsregistermappning  
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Registermappning för integrationen** och välj sedan relaterad länk.
2.  Välj åtgärden **Synkronisera ändrade poster** och sedan **Ja**.  

## <a name="see-also"></a>Se även  
[Synkroniserar i Business Central och Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Ställa in konton för integrering med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
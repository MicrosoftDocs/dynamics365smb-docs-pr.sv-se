---
title: Så här hanterar du meddelandemallar | Microsoft Docs
description: Meddelanden skickas till arbetsflödesanvändare för att meddela dem om steg som måste vidtas eller informera dem om statusen för arbetsflödessteg. Du kan konfigurera vem som får meddelanden, och när, genom att ställa in godkännandeanvändare, användarnas meddelandeschema och relevanta arbetsflödessvaren som definierar meddelandemottagaren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: across-how-to-specify-when-and-how-to-receive-notifications
ms.openlocfilehash: 562664ad0fd443c3363d103572022e6d819ed357
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "914284"
---
# <a name="manage-notification-templates"></a>Hantera meddelandemallar
Meddelanden skickas till arbetsflödesanvändare för att meddela dem om steg som måste vidtas eller informera dem om statusen för arbetsflödessteg. Du kan konfigurera vem som får meddelanden, och när, genom att ställa in godkännandeanvändare, användarnas meddelandeschema och relevanta arbetsflödessvaren som definierar meddelandemottagaren. Mer information finns i [Ställa in meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md).  

 Meddelanden baseras på mallar som definierar innehåll och layout på meddelandet. Du kan exportera innehållet i en meddelandemall, redigerar det och importera det till samma eller en ny meddelandemall. Beskrivs i följande procedurer.  

 Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller tre meddelandemallar, en för meddelande om godkännandebegäran, en för meddelande om nya transaktioner och en för e-postmeddelande om förfallna godkännandebegäranden. De tre fördefinierade meddelandemallarna stöder meddelandemetoderna med **E-post** och **Notering**. Se avsnittet ”Innehåll i meddelandemallar” om du vill visa innehållet i de tre meddelandemallarna.

## <a name="to-create-a-new-notification-template"></a>Så här skapar du en ny meddelandemall  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **meddelandemallar** och välj sedan relaterad länk.  
2.  På sidan **Meddelandemallar** väljer du åtgärden **Ny**.  
3.  Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kod**|Identifiera meddelandemallen.|  
    |**Beskrivning**|Beskriv meddelandemallen.|  
    |**Meddelandemetod**|Ange om meddelandet ska skickas som ett e-postmeddelande eller som en kommentar.|  
    |**Typ**|Ange arbetsprocessen som meddelandet ska användas för.<br /><br /> Välj en av följande typer:<br /><br /> -   **Godkännande** anger att mallen används för att meddela användare i godkännandearbetsflöden.<br />-   **Ny post** anger att mallen ska användas för att meddela godkännare när en ny transaktion, till exempel ett kundkort, måste godkännande.<br />-   **Förfallna** anger att mallen används för att meddela användare om förfallna godkännandebegäranden.|  
    |**Standard**|Ange om meddelandemallen ska användas som standard.|  

## <a name="to-modify-a-notification-template"></a>Så här ändrar du en meddelandemall  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **meddelandemallar** och välj sedan relaterad länk.  
2.  På sidan **meddelandemallar** väljer du meddelandemallen som du vill ändra.  
3.  Välj åtgärden **Exportera mallinnehåll**.  
4.  Klicka på **Spara** på sidan **Exportera fil** och ange sedan namn och plats för HTML-filen.  
5.  Högerklicka på filen, välj **Öppna med**och välj sedan relevant program.  

    > [!NOTE]  
    >  Innehåll för meddelandemallar av typen E-post visas i HTML-format. Innehåll för meddelandemallar av typen Notering visas i TXT-format.  
6.  Redigera innehållet i meddelandemallen genom att lägga till, ändra eller ta bort parametervariabler för att definiera vilket innehåll du vill ha. Spara det sedan. Mer information finns i avsnittet ”Innehåll i meddelandemallar”.  

    Fortsätt med att importera det ändrade innehållet till samma eller en ny meddelandemall.  
7.  Om du vill ändra meddelandemallen som du exporterade markerar du mallen som du valde i steg 2 på sidan **Meddelandemallar**.  

    Alternativt kan du följa proceduren i ”Så här skapar du en ny meddelandemall” och välja den nya meddelandemallen för att importera det ändrade mallinnehållet till en ny meddelandemall.  
8.  Välj åtgärden **Importera mallinnehåll**.  
9. Om du ändrar en befintlig meddelandemall väljer du knappen **Ja** i meddelandet om överskrivning av den befintliga mallen.  
10. Välj HTML-filen som du ändrade i steg 6 och välj sedan knappen **Öppna** på sidan **Välj en fil att importera**.  

Den befintliga eller nya meddelandemallen på sidan **Meddelandemallar** uppdateras nu med det ändrade innehållet.  

### <a name="content-of-the-notification-templates"></a>Innehåll i meddelandemallarna  
De tre meddelandemalltyperna, **Ny post**, **Godkännande** och **Förfallna**, har olika innehåll.  

Parametervärden infogas automatiskt i meddelandena i enlighet med meddelandemalltypen.  

#### <a name="new-record"></a>Ny post  
 ![NAV&#95;avisering&#95;mall&#95;ny&#95;post&#95;typ](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Godkännande  
 ![NAV&#95;avsiering&#95;mall&#95;godkännande&#95;typ](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Förfallen  
 ![NAV&#95;avisering&#95;förfallen&#95;typ](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Se även  
 [Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
 [Konfigurera e-post](admin-how-setup-email.md)   
 [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)   
 [Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
 [Skapa arbetsflöden](across-how-to-create-workflows.md)   
 [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)   
 [Arbetsflöde](across-workflow.md)   

---
title: "Ställa in meddelanden för arbetsflöde | Microsoft Docs"
description: "Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på. Till exempel i en arbetsflödessteg kan händelsen vara att användare 1 begär godkännande av en ny post och åtgärden är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten och åtgärden är att ett meddelande skickas till användare 3, som ska starta en relaterad bearbetning av den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 53b063598cf21ca5b5de72d953995b48a17d64a2
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-workflow-notifications"></a>Konfigurera meddelanden för arbetsflödet
Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på. Till exempel i en arbetsflödessteg kan händelsen vara att användare 1 begär godkännande av en ny post och åtgärden är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten och åtgärden är att ett meddelande skickas till användare 3, som ska starta en relaterad bearbetning av den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
>  Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder meddelanden som e-post och interna noteringar.  

> [!IMPORTANT]  
>  Alla arbetsflödesmeddelanden skickas via en jobbkö. Se till att jobbkön i din installation är konfigurerad för att hantera arbetsflödesmeddelanden och att kryssrutan **Starta automatiskt från server** är markerad. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

Du konfigurerar andra aspekter av arbetsflödesmeddelanden på flera ställen:  

1.  För godkännande arbetsflöden konfigurerar du mottagare av arbetsflödemeddelanden genom att fylla i en rad på sidan **Användarinställningar för godkännande** för varje användare som ingår i arbetsflödet. Till exempel om användare 2 är specificerat i fältet **Godkännar-ID** på raden för användare 1 så skickas meddelandet om godkännandebegäran till användare 1. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  
2.  Du definierar när och hur användarna får arbetsflödemeddelanden genom att fylla i sidan **Meddelandeschema** för varje arbetsflödesanvändare. Mer information finns i [Så här anger du när och hur användare ska meddelas](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Om du vill kan anpassa du innehållet i e-postmeddelanden genom att ändra rapporten 1320, e-postmeddelanden. Mer information finns i [så här skapar du och ändrar en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md).  
4.  Du konfigurerar specifikt innehåll och regler för ett arbetsflödemeddelande när du skapar arbetsflödet i fråga. Du gör detta genom att välja alternativ på sidan **Alternativ för arbetsflödessvar** för de arbetsflödessvar som representerar meddelandet. Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se även  
 [Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
 [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)   
 [Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Skapa arbetsflöden](across-how-to-create-workflows.md)   
 [Så här skapar och ändrar du en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md)   
 [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)   
 [Konfigurera e-post](admin-how-setup-email.md)   
 [Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Arbetsflöde](across-workflow.md)   


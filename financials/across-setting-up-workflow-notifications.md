---
title: "Ställa in meddelanden för arbetsflöde | Microsoft Docs"
description: "Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på. Till exempel i en arbetsflödessteg kan händelsen vara att användare 1 begär godkännande av en ny post och åtgärden är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten och åtgärden är att ett meddelande skickas till användare 3, som ska starta en relaterad bearbetning av den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 351c079df25516a83de42d5fa12954b25ba5e63e
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-workflow-notifications"></a>Konfigurera meddelanden för arbetsflödet
Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på. Till exempel i en arbetsflödessteg kan händelsen vara att användare 1 begär godkännande av en ny post och åtgärden är att ett meddelande skickas till användare 2, godkännaren. I nästa arbetsflödessteg kan händelsen vara att användare 2 godkänner posten och åtgärden är att ett meddelande skickas till användare 3, som ska starta en relaterad bearbetning av den godkända posten. För arbetsflödessteg som gäller godkännande kopplas varje meddelande till en godkännandepost. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
>  Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder meddelanden som e-post och interna noteringar.  

> [!IMPORTANT]  
>  Alla arbetsflödesmeddelanden skickas via en jobbkö. Kontrollera jobbkön i lösningen. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

Du konfigurerar andra aspekter av arbetsflödesmeddelanden på flera ställen:  

1.  För godkännande arbetsflöden konfigurerar du mottagare av arbetsflödemeddelanden genom att fylla i en rad i fönstret **Användarinställningar för godkännande** för varje användare som ingår i arbetsflödet. Till exempel om användare 2 är specificerat i fältet **Godkännar-ID** på raden för användare 1 så skickas meddelandet om godkännandebegäran till användare 1. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  
2.  Du definierar när och hur användarna får arbetsflödemeddelanden genom att fylla i fönstret **Meddelandeschema** för varje arbetsflödesanvändare. Mer information finns i [Så här anger du när och hur användare ska meddelas](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Du kan skapa allmänt innehåll och layout på meddelanden, inklusive meddelanden om förfallna arbetsflödessvar, genom att ställa in meddelandemallar i fönstret **Kod för meddelandemall**. Du kan använda de standardmallar som medföljer [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4.  Du konfigurerar specifikt innehåll och regler för ett arbetsflödemeddelande när du skapar arbetsflödet i fråga. Du gör detta genom att välja alternativ i fönstret **Alternativ för arbetsflödessvar** för de arbetsflödessvar som representerar meddelandet. Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se även  
 [Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
 [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)   
 [Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Skapa arbetsflöden](across-how-to-create-workflows.md)   
 [Hantera meddelandemallar](across-how-to-manage-notification-templates.md)   
 [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)   
 [Konfigurera e-post](madeira-how-setup-email.md)   
 [Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Arbetsflöde](across-workflow.md)   


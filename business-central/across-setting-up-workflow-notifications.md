---
title: Konfigurera meddelanden för arbetsflödet
description: I den här artikeln beskrivs hur du konfigurerar arbetsflödesmeddelanden för att varna en användare om att en händelse har inträffat som de måste reagera på ett arbetsflödessvar krävs.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9405af9c52b17ab34fded263692e3294ed8aaf11
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533974"
---
# <a name="workflow-notifications"></a>Aviseringar för arbetsflöde

Konfigurera dina arbetsflöden så att användarna automatiskt meddelas när deras uppmärksamhet krävs för ett steg i det arbetsflödet. Många arbetsflödessvar handlar om att meddela en användare om att en händelse har skett som de måste agera på.

Du kan t.ex. ange användare 2, som är användare av godkännare och får ett meddelande när användare 1 begär godkännande för en ny post. I nästa steg i arbetsflödet får du ett meddelande om användare 3 när användare 2 godkänner posten för att starta en relaterad bearbetning av posten. Med arbetsflödessteg för godkännande kopplas varje meddelande till en godkännandepost. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
> Standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder meddelanden som e-post och interna noteringar.  

> [!IMPORTANT]  
> Alla arbetsflödesmeddelanden skickas via en jobbkö. Se till att jobbkön i din installation är konfigurerad för att hantera arbetsflödesmeddelanden och att kryssrutan **Starta automatiskt från server** är markerad. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Ställa in aviseringar

Du konfigurerar andra aspekter av arbetsflödesmeddelanden på flera ställen:  

* Godkännaravisering

    För godkännande arbetsflöden konfigurerar du mottagare av arbetsflödemeddelanden genom att fylla i en rad på sidan **Användarinställningar för godkännande** för varje användare som ingår i arbetsflödet.  

    Till exempel om användare 2 är specificerat i fältet **Godkännar-ID** på raden för användare 1 så skickas meddelandet om godkännandebegäran till användare 2. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  
* Meddelandescheman

    Du definierar när och hur användarna får arbetsflödemeddelanden genom att fylla i sidan **Meddelandeschema** för varje arbetsflödesanvändare. Mer information finns i [Så här anger du när och hur användare ska meddelas](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Anpassa e-postaviseringarna

    Om du vill kan anpassa du innehållet i e-postmeddelanden genom att ändra rapporten 1320, e-postmeddelanden. Mer information finns i [Skapa och ändra anpassad rapportlayouter](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Om du vill använda e-post som aviseringsmetod måste du konfigurera e-post för både avsändaren och mottagaren i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

* Svarsalternativ

    Du konfigurerar specifikt innehåll och regler för ett arbetsflödemeddelande när du skapar arbetsflödet i fråga. Välj de anpassningsalternativ på sidan **Arbetsflödessvar** för de arbetsflödessvar som representerar meddelandet. Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md#to-create-a-workflow).  

* Meddela avsändare

    För arbetsflöden för godkännande lägger du till ett arbetsflödessvarssteg för att meddela avsändaren när begäran har godkänts eller avvisats. Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se även

[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)  
[Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Skapa arbetsflöden](across-how-to-create-workflows.md)  
[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)  
[Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)  
[Konfigurera e-post](admin-how-setup-email.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Ställa in arbetsflöden | Microsoft Docs
description: Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.
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
ms.openlocfilehash: a7a0f6640b56f06b316dcd62ec77018051e12323
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240309"
---
# <a name="setting-up-workflows"></a>Konfigurera arbetsflöden
Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg. Mer information finns i [Använda arbetsflöden](across-use-workflows.md).  

 Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare och godkännaranvändare,ange hur användarna ska meddelas om arbetsflödessteg och sedan skapa arbetsflöden, eventuellt med tillämpning av föregående kodanpassning.  

 På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

 Om ett företagsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds måste en Microsoft-partner implementera dem genom att anpassa applikationskoden. Mer information finns i [Genomgång: Genomföra nya arbetsflödeshändelser och svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjälpen för utvecklare och IT-proffs.

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konfigurera arbetsflödesanvändare och användargrupper|[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)|  
|Konfigurera arbetsflödesanvändare som ingår i godkännandearbetsflöden.|[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)|  
|Ange hur arbetsflödesanvändare får meddelanden om arbetsflödessteg, inklusive godkännandebegäranden.|[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)|  
|Ange om användare ska meddelas per e-post eller anteckning och hur ofta meddelanden ska kunna skickas.|[Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Anpassa innehållet i e-postmeddelanden genom att ändra rapporten 1320, e-postmeddelanden.|[Så här skapar och ändrar du en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md)|  
|Skapa en SMTP-server för att aktivera e-postkommunikation i och utanför [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Konfigurera e-post](admin-how-setup-email.md)|
|Ange de olika stegen för ett arbetsflöde genom att koppla arbetsflödeshändelser till arbetsflödessvar.|[Skapa arbetsflöden](across-how-to-create-workflows.md)|  
|Använd arbetsflödesmallar till att skapa nya arbetsflöden|[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)|  
|Dela arbetsflöden med andra [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser.|[Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md)|  
|Se information om hur du konfigurerar ett arbetsflöde för godkännande av försäljningsdokument genom att följa en procedur från slutpunkt till slutpunkt.|[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Lägg till stöd för ett affärsscenario som kräver nya arbetsflödeshändelser eller svar genom att anpassa applikationskoden.|[Genomgång: Implementera nya arbetsflödeshändelser och svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Se även  
 [Använda arbetsflöden](across-use-workflows.md)   
 [Arbetsflöde](across-workflow.md)   
 [Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbeta med Business Central](ui-work-product.md)

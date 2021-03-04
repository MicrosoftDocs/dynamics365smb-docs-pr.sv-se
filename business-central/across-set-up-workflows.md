---
title: Konfigurera arbetsflöden
description: Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Lär dig mer om de olika åtgärder du måste utföra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: a104065d8f52ca9d1bb9221cd43917253c640ca4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754232"
---
# <a name="set-up-workflows"></a>Konfigurera arbetsflöden

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg. Mer information finns i [Använda arbetsflöden](across-use-workflows.md).  

 Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare och godkännaranvändare,ange hur användarna ska meddelas om arbetsflödessteg och sedan skapa arbetsflöden, eventuellt med tillämpning av föregående kodanpassning.  

 På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

 Om ett affärsscenario kräver en arbetsflödehändelse eller ett svar som inte stöds, måste en Microsoft-partner implementera dem genom kod, eller också kan du skapa ett arbetsflöde med hjälp av Power Automate. Mer information finns i [Använda [!INCLUDE[prod_short](includes/prod_short.md)] i ett automatiserat arbetsflöde](across-how-use-financials-data-source-flow.md) eller [Händelser i AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) i hjälpen för utvecklare.

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Konfigurera arbetsflödesanvändare och användargrupper|[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)|  
|Konfigurera arbetsflödesanvändare som ingår i godkännandearbetsflöden.|[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)|  
|Ange hur arbetsflödesanvändare får meddelanden om arbetsflödessteg, inklusive godkännandebegäranden.|[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)|  
|Ange om användare ska meddelas per e-post eller anteckning och hur ofta meddelanden ska kunna skickas.|[Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Anpassa innehållet i e-postmeddelanden genom att ändra rapporten 1320, e-postmeddelanden.|[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)|  
|Skapa en SMTP-server för att aktivera e-postkommunikation i och utanför [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurera e-post](admin-how-setup-email.md)|
|Ange de olika stegen för ett arbetsflöde genom att koppla arbetsflödeshändelser till arbetsflödessvar.|[Skapa arbetsflöden](across-how-to-create-workflows.md)|  
|Använd arbetsflödesmallar till att skapa nya arbetsflöden|[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)|  
|Dela arbetsflöden med andra [!INCLUDE[prod_short](includes/prod_short.md)]-databaser.|[Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md)|  
|Se information om hur du konfigurerar ett arbetsflöde för godkännande av försäljningsdokument genom att följa en procedur från slutpunkt till slutpunkt.|[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Exempel på ett arbetsflöde för godkännande
Den här videon visar hur du ställer in ett arbetsflöde som kräver att någon begär någon annans godkännande innan de kan ändra information om en befintlig kund eller skapa en ny kund.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Se även  
 [Använda arbetsflöden](across-use-workflows.md)   
 [Arbetsflöde](across-workflow.md)   
 [Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbeta med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
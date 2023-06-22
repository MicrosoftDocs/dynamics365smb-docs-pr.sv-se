---
title: Ställ in godkännandearbetsflödet (innehåller video)
description: 'Ställ in arbetsflöden, arbetsflödesanvändare och godkännande användare för att ansluta verksamhetsprocesser som utförs av de olika användarna.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="set-up-approval-workflows" />Konfigurera arbetsflöden för godkännande

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg. Läs mer i [Använda arbetsflöden för godkännande](across-use-workflows.md).

Innan du kan börja använda godkännandearbetsflödet måste du konfigurera arbetsflödesanvändare och godkännaranvändare,ange hur användarna ska meddelas om arbetsflödessteg och sedan skapa arbetsflöden.

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.

[!INCLUDE[workflow](includes/workflow.md)]

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|  
|Konfigurera arbetsflödesanvändare och användargrupper|[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)|  
|Konfigurera arbetsflödesanvändare som ingår i godkännandearbetsflöden.|[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)|  
|Ange hur arbetsflödesanvändare får meddelanden om arbetsflödessteg, inklusive godkännandebegäranden.|[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)|  
|Ange om användare ska meddelas per e-post eller anteckning och hur ofta meddelanden ska kunna skickas.|[Ange när och hur meddelanden ska tas emot](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Anpassa innehållet i e-postmeddelanden genom att ändra rapporten 1320, e-postmeddelanden.|[Skapa och ändra anpassade rapportlayouter](ui-how-create-custom-report-layout.md)|  
|Skapa en SMTP-server för att aktivera e-postkommunikation i och utanför [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurera e-post](admin-how-setup-email.md)|
|Ange de olika stegen för ett arbetsflöde genom att koppla arbetsflödeshändelser till arbetsflödessvar.|[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)|  
|Använd arbetsflödesmallar till att skapa nya arbetsflöden|[Skapa godkännandearbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)|  
|Dela arbetsflöden med andra [!INCLUDE[prod_short](includes/prod_short.md)]-databaser.|[Exportera och importera godkännandearbetsflöden](across-how-to-export-and-import-workflows.md)|  
|Se information om hur du konfigurerar ett arbetsflöde för godkännande av försäljningsdokument genom att följa en procedur från slutpunkt till slutpunkt.|[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow" />Exempel på ett arbetsflöde för godkännande

Den här videon visar hur du ställer in ett arbetsflöde som kräver att en användare begär någon annans godkännande innan de kan ändra information om en befintlig kund eller skapa en ny kund.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also" />Se även

[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeta med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

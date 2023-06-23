---
title: Konfigurera användare för godkännande
description: 'Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-approval-users" />Konfigurera godkännandeanvändare

Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa användare som är inblandade på sidan **användarinställningar för godkännande**. Du kan också ange beloppsgränser för olika typer av förfrågningar, definiera ersättande godkännare och skapa meddelanden.  

När du har konfigurerat godkännandeanvändare kan du skapa arbetsflödessvar för godkännandearbetsflöden. Läs mer i [Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md).  

> [!TIP]
> Du kan kräva att flera godkännare reagerar på en begäran om godkännande genom att skapa en grupp med godkännare på sidan **Arbetsflödesanvändargrupp**. Läs mer i [Konfigurera arbetsflödesanvändargrupper](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user" />Så här konfigurerar du en godkännandeanvändare

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställningar för godkännande** och väljer sedan relaterad länk.  
2. Skapa en ny rad på sidan **Användarinställningar för godkännande** och fyll i fälten enligt instruktionerna i följande tabell.  

   |Fält|Description|
   |-----|-----------|
   |**Användar-ID**|Välj användar-ID för den person som är involverad i godkännandeprocessen.|
   |**Säljare/inköpare kod**|Ange den säljar- eller inköparkod som är kopplad till användaren.<br /><br /> Du fyller vanligtvis i fältet **Säljare/Inköpare kod** om säljaren eller en inköpare som är ansvarig för kunden eller leverantören är samma person som måste godkänna försäljnings- eller inköpsbegäran.|
   |**Godkännar-ID**|Välj användar-ID för den person som måste godkänna begäranden från person som du angav i fältet **Användar-ID**.|
   |**Max. förs.belopp att godkänna**|Ange det maximala försäljningsbeloppet i lokal valuta (BVA) som den valda personen i fältet **Användar-ID** kan godkänna.|
   |**Obegränsad godkännande försäljning**|Ange att identifierade personen i fältet **Användar-ID** kan godkänna alla försäljningsbegäranden oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max. förs.belopp att godkänna**.|
   |**max. inköpsbelopp som kan godkännas**|Ange det maximala inköpsbeloppet i BVA som den identifierade personen i fältet **Användar-ID** kan godkänna.|
   |**Obegränsad godkännande för inköp**|Ange att identifierade personen i fältet **Användar-ID** kan godkänna alla inköpsbegäranden oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max. inköpsbelopp som kan godkännas**.|
   |**Max.bel godkänna ink.begäran**|Ange det maximala beloppet i BVA som den identifierade personen i fältet **Användar-ID** kan godkänna för inköpsofferter.<br /><br /> Om du vill använda detta fält måste du välja alternativet **Godkännarkedja** i fälten **Gränstyp för godkännare** på sidan **Arbetsflödessvar**.|
   |**Obegränsad godkännande inköpsbeg.**|Ange att identifierade personen i fältet **Användar-ID** kan godkänna alla inköpsofferter oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max.bel godkänna ink.begäran**.|
   |**Ersättare**|Välj användar-ID för den person som måste godkänna begäranden från den identifierade personen i fältet **Användar-ID** om användaren i **Godkännar-ID** inte är tillgänglig. <br /><br />**Obs!**  Ersättaren kan vara antingen användaren i fältet **Ersättare** en direkta godkännaren eller godkännandeadministratören, i den prioritetsordningen. Läs mer i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).|
   |**E-post**|Ange e-postadressen till person i fältet **Användar-ID**.|
   |**Administratör för godkännande**|Ange den användare som har behörighet att avblockera arbetsflöde för godkännande, till exempel genom att delegera godkännandebegäran till nya ersättande godkännare och ta bort förfallna godkännandebegäranden.<br /><br />**Obs** Endast en person kan vara administratör för godkännande.|

3. Om du vill testa konfigurationen av godkännandeanvändare väljer du åtgärden **Test av användarinställningar för godkännande**.  
4. Upprepa steg 2 och 3 för varje person som du vill konfigurera som en godkännandeanvändare.  

Nästa steg är att ange hur du vill [!INCLUDE [prod_short](includes/prod_short.md)] meddela personer om att en begäran väntar på att bli uppmärksam på deras uppmärksamhet. Läs mer på [Konfigurera aviseringar för arbetsflöde](across-setting-up-workflow-notifications.md).

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also" />Se även

[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)  
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)  
[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

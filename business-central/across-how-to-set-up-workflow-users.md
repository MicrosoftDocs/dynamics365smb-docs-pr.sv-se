---
title: Så här konfigurerar du arbetsflödesanvändare
description: Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå på sidan Användarinställningar för godkännande.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 04/04/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-a-sequence-of-workflow-users"></a>Konfigurera en sekvens av arbetsflödesanvändare

Innan du kan skapa arbetsflöde för godkännande måste du ställa in de användare som kommer att skicka förfrågningar och deras godkännare. Du kan till exempel ange vem som ska ta emot en notering för att agera på ett arbetsflödessteg. Du ställer in godkännande arbetsflödesdeltagare på sidan **Användarinställningar för godkännande**. Läs mer i [Så här skapar du användare för godkännande](across-how-to-set-up-approval-users.md).

På sidan **Arbetsflödesanvändargrupper** kan du ange var en deltagare deltar i ett godkännandearbetsflöde genom att ange ett nummer i **Sekvensnr.** . Du kan t.ex. ange att användarna ska delta i en sekventiell ordning, till exempel en kedja av godkännare. Du kan också ange en plan lista över godkännare genom att ange samma nummer. I det senare fallet måste endast en av godkännarna godkänna en begäran.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group"></a>Så här konfigurerar du en användargrupp

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflödesanvändargrupper** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflödesanvändargrupp** öppnas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Beskriv arbetsflödet i fältet **Beskrivning**.  
5. Fyll i fälten på den första raden enligt beskrivningen i följande tabell på snabbfliken **Medlemmar i arbetsflödesanvändargrupp**.  

   |Fält|Description|
   |-----|-----------|
   |**Användarnamn**|Ange användaren som ska ingå i ett arbetsflöde.<br /><br /> Användaren måste finnas på sidan **Användarinställningar**. Läs mer i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).|
   |**Sekvensnr**|Ange den ordning som arbetsflödesanvändaren agerar i ett arbetsflöde i förhållanden till andra användare. Detta fält kan användas, till exempel, för att ange när användaren godkänner i förhållande till andra godkännare när du använder alternativet **Arbetsflödesanvändargrupp** i fältet **Godkännartyp** på det relaterade arbetsflödesvaret.|

   > [!NOTE]
   > Vanligtvis är sekvensnummer sekventiella för användare i en arbetsflödesanvändargrupp. Flera användare kan dock ha samma sekvensnummer. När så är fallet måste bara en av användarna godkänna en begäran innan arbetsflödet går vidare till nästa steg. Om användare A och användare B till exempel båda är nummer två i sekvensen går arbetsflödet vidare till steg tre när antingen användare A eller användare B godkänner begäran.
6. Upprepa steg 5 för att lägga till fler arbetsflödesanvändare i arbetsflödesanvändargrupp.  

## <a name="see-also"></a>Se även

[Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

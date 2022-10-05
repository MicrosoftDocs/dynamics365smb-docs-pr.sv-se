---
title: Konfigurera användare för godkännande
description: Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade på sidan användarinställningar för godkännande.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 2654dcb68b579d90fe3218bcd0bba3bde4cb5036
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585844"
---
# <a name="set-up-approval-users"></a>Konfigurera användare för godkännande

Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen. På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande.  

> [!NOTE]  
> Godkännandeanvändare, både den som begär och den som godkänner, måste först ställas in som arbetsflödesanvändare på sidan **Arbetsflödesanvändargrupp**. Läs mer i [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md).  

När du har konfigurerat godkännandeanvändare kan du skapa arbetsflödessvar för godkännandearbetsflöden. Läs mer från steg 9 i [Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md).  

> [!NOTE]  
> Om du vill definiera att en godkännandebegäran inte godkänns förrän flera användare har godkänt den, ställer du in godkännare i en hierarki. För godkännartypen **godkännare** anger du godkännare på sidan **Användarinställningar för godkännande**. För godkännartypen **Arbetsflödesanvändargrupp** ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar hierarkin genom att tilldela inkrementella nummer till varje godkännare i fältet **Sekvensnr.** . Läs mer i [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Så här konfigurerar du en godkännandeanvändare

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användarinställningar för godkännande** och väljer sedan relaterad länk.  
2. Skapa en ny rad på sidan **Användarinställningar för godkännande** och fyll i fälten enligt instruktionerna i följande tabell.  

   |Fält|Description|
   |-----|-----------|
   |**Användar-ID**|Välj användar-ID för den person som är involverad i godkännandeprocessen.|
   |**Säljare/inköpare kod**|Ange den säljar- eller inköparkod som är kopplad till användaren.<br /><br /> Du fyller typiskt i fältet **Säljare/Inköpare kod** om säljaren eller en inköpare som är ansvarig för kunden eller leverantören är samma person som måste godkänna försäljnings- eller inköpsbegäran.|
   |**Godkännar-ID**|Välj användar-ID för den person som måste godkänna begäranden från person som identifieras i fältet **Användar-ID**.|
   |**Max. förs.belopp att godkänna**|Ange det maximala försäljningsbeloppet i lokal valuta (BVA) som den identifierade personen i fältet **Användar-ID** kan godkänna.|
   |**Obegränsad godkännande försäljning**|Ange att identifierade personen i fältet **Användar-ID** kan godkänna alla försäljningsbegäranden oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max. förs.belopp att godkänna**.|
   |**max. inköpsbelopp som kan godkännas**|Ange det maximala inköpsbeloppet i BVA som den identifierade personen i fältet **Användar-ID** kan godkänna.|
   |**Obegränsad godkännande för inköp**|Ange att identifierade personen i fältet **Användar-ID** kan godkänna alla inköpsbegäranden oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max. inköpsbelopp som kan godkännas**.|
   |**Max.bel godkänna ink.begäran**|Ange det maximala beloppet i BVA som den identifierade personen i fältet **Användar-ID** kan godkänna för inköpsofferter.<br /><br /> Om du vill använda detta fält måste du välja alternativet **Godkännarkedja** i fälten **Gränstyp för godkännare** på sidan **Arbetsflödessvar**.|
   |**Obegränsad godkännande inköpsbeg.**|Ange att identifierade personen i fältet **Användar-ID** kan godkänna alla inköpsofferter oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max.bel godkänna ink.begäran**.|
   |**Ersättare**|Välj användar-ID för den person som måste godkänna begäranden från den identifierade personen i fältet **Användar-ID** om användaren i **Godkännar-ID** inte är tillgänglig. <br /><br />**Obs!**  Ersättaren kan vara antingen användaren i fältet **Ersättare** en direkta godkännaren eller godkännandeadministratören, i den prioritetsordningen. Läs mer i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).|
   |**E-post**|Ange e-postadressen till person i fältet **Användar-ID**.|
   |**Administratör för godkännande**|Ange den användare som har rättigheter att ta bort spärrar på arbetsflöde för godkännande, till exempel genom att delegera godkännandebegäran till nya ersättande godkännare och ta bort förfallna godkännandebegäranden.|

   > [!NOTE]
   > Endast en person kan vara administratör för godkännande.

3. Om du vill testa konfigurationen av godkännandeanvändare väljer du åtgärden **Test av användarinställningar för godkännande**.  
4. Upprepa steg 2 och 3 för varje person som du vill konfigurera som en godkännandeanvändare.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se även

[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)  
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)  
[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Så här konfigurerar du godkännandeanvändare | Microsoft Docs
description: Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen. På sidan Användarinställningar för godkännande anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 66d171a2f21759f52ab472189a6bbeebac4593b6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "806873"
---
# <a name="set-up-approval-users"></a>Konfigurera användare för godkännande
Innan du kan skapa arbetsflöden som innehåller godkännandesteg, måste du skapa arbetsflödeanvändare som är inblandade i godkännandeprocessen. På sidan **Användarinställningar för godkännande** anger du även beloppsgränser för vissa typer av förfrågningar och definierar ersättande godkännare som godkännandebegäran kan delegeras till när den ursprungliga godkännaren är frånvarande.  

> [!NOTE]  
>  Godkännandeanvändare, både den som begär och den som godkänner, måste först ställas in som arbetsflödesanvändare på sidan **Arbetsflödesanvändargrupp**. Mer information finns i [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md).  

 När du har konfigurerat godkännandeanvändare kan du använda konfigurationen för att skapa arbetsflödessvar för godkännandearbetsflöden. Mer information finns i steg 9 i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Om du vill definiera att en godkännandebegäran inte godkänns förrän flera godkännare i en godkännandekedja har godkänt den, ställer du in godkännare i en hierarki. För godkännartypen **godkännare** anger du godkännare på sidan **Användarinställningar för godkännande**. För godkännartypen **Arbetsflödesanvändargrupp** ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar hierarkin genom att tilldela inkrementella nummer till varje godkännare i fältet **Sekvensnr.** . Mer information finns i detta avsnitt och i [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md).  
>   
>  Om du vill definiera att en godkännandebegäran inte godkänns förrän flera likvärdiga godkännare har godkänt den, oberoende av ett hierarki, ställer du in en plan arbetsflödesanvändargrupp. För godkännartypen **Arbetsflödesanvändargrupp**, ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar samma nummer till varje godkännare i fältet **Sekvensnr.** . Mer information finns i [Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Så här konfigurerar du en godkännandeanvändare  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användarinställningar för godkännande** och välj sedan relaterad länk.  
2. Skapa en ny rad på sidan **Användarinställningar för godkännande** och fyll i fälten enligt instruktionerna i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Användar-ID**|Välj användar-ID för den användare som är involverad i godkännandeprocessen.|  
    |**Säljare/inköpare kod**|Ange den säljar- eller inköparkod som är kopplad till användaren i fältet **Säljare/Inköpare kod**.<br /><br /> Du fyller typiskt i fältet **Säljare/Inköpare kod** om säljaren eller en inköpare som är ansvarig för kunden eller leverantören är samma person som måste godkänna försäljnings- eller inköpsbegäran.|  
    |**Godkännar-ID**|Välj användar-ID för den användare som måste godkänna begäranden från användaren i fältet **Användar-ID**.|  
    |**Max. förs.belopp att godkänna**|Ange det maximala försäljningsbeloppet i BVA som användaren i fältet **User ID** kan godkänna.|  
    |**Obegränsad godkännande försäljning**|Ange att användaren i fältet **Användar-ID** kan godkänna alla försäljningsbegäranden oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max. förs.belopp att godkänna**.|  
    |**max. inköpsbelopp som kan godkännas**|Ange det maximala inköpsbeloppet i BVA som användaren i fältet **User ID** kan godkänna.|  
    |**Obegränsad godkännande för inköp**|Ange att användaren i fältet **Användar-ID** kan godkänna alla inköpsbegäranden oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max. förs.belopp att godkänna**.|  
    |**Max.bel godkänna ink.begäran**|Ange det maximala beloppet i BVA som användaren i fältet **Användar-ID** kan godkänna för inköpsofferter.<br /><br /> Om du vill använda detta fält måste du välja alternativet **Godkännarkedja** i fälten **Gränstyp för godkännare** på sidan **Arbetsflödessvar**.|  
    |**Obegränsad godkännande inköpsbeg.**|Ange att användaren i fältet **Användar-ID** kan godkänna alla inköpsofferter oavsett belopp.<br /><br /> Om du markerar den här kryssrutan kan du inte fylla i fältet **Max.bel godkänna ink.begäran**.|  
    |**Ersättare**|Välj användar-ID för den användare som måste godkänna begäranden från användaren i fältet **Användar-ID** om användaren i **Godkännar-ID** inte är tillgänglig. **Obs!**  Ersättaren kan vara antingen användaren i fältet **Ersättare** en direkta godkännaren eller godkännandeadministratören, i den prioritetsordningen. Mer information finns i [Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md).|  
    |**E-post**|Ange e-postadressen till användaren i fältet **Användar-ID**.|  
    |**Administratör för godkännande**|Ange den användare som har rättigheter att ta bort spärrar på godkännandearbetsflöden, till exempel genom att delegera godkännandebegäran till nya ersättande godkännare och ta bort förfallna godkännandebegäranden.|  

    > [!NOTE]  
    >  Funktionen hos **Gränstyp för godkännare** gäller bara för moduler där begränsningar kan definieras, dvs godkännande av försäljning och inköp. Andra typer av godkännande där begränsningar inte gäller kommer alltid fungerar enligt beskrivningen för alternativet **direkt godkännare**.  

3. Om du vill testa konfigurationen av godkännandeanvändare väljer du åtgärden **Test av användarinställningar för godkännande**.  
4. Upprepa steg 2 och 3 för varje användare som du vill konfigurera som en godkännandeanvändare.  

## <a name="see-also"></a>Se även  
[Konfigurera arbetsflödesanvändare](across-how-to-set-up-workflow-users.md)   
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
[Skapa arbetsflöden](across-how-to-create-workflows.md)   
[Konfigurera arbetsflöden](across-set-up-workflows.md)   
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Arbetsflöde](across-workflow.md)   

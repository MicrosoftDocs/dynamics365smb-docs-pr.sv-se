---
title: Så här tar du bort arbetsflöden för godkännande
description: Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det. Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '1500,'
ms.date: 09/08/2022
ms.author: edupont
---
# Ta bort arbetsflöden för godkännande

Om du är säker på att ett arbetsflöde inte längre används kan du ta bort det. Alla arbetsflödessteginstanser som har definierats i arbetsflödet måste ha status **Avslutat**.

> [!CAUTION]
> När du tar bort ett arbetsflöde, kommer all information i arbetsflödet förloras.

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Läs mer i [Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md).

## Ta bort arbetsflödet

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.
2. Välj arbetsflödet som du vill ta bort.
3. Välj åtgärden **Radera**.
4. Eller öppna arbetsflödet som du vill ta bort.
5. På sidan **Kopiera arbetsflöde** väljer du åtgärden **Radera**.

> [!NOTE]
> Om du vill ta bort ett arbetsflöde måste det inaktiveras. Om du vill inaktivera ett arbetsflöde öppnar du det på sidan **arbetsflöden** och stänger sedan av den **aktiverade** växlingen.

## Se även

[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Aktivera arbetsflöden för godkännande](across-how-to-enable-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

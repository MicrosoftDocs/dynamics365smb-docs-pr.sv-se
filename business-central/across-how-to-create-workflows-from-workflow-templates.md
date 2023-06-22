---
title: Så här skapar du arbetsflöden från arbetsflödesmallar
description: Om du vill spara tid när du skapar nya arbetsflöde för godkännande kan du skapa icke-redigerbara arbetsflöden från arbetsflödesmallar med prefixet "MS".
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="create-workflows-from-workflow-templates" />Skapa arbetsflöden från arbetsflödesmallar

Du kan spara tid när du skapar nya arbetsflöde för godkännande kan du använda arbetsflödesmallar.  

Arbetsflödesmallar representerar icke-redigerbara arbetsflöden som finns i den förinställda versionen av [!INCLUDE[prod_short](includes/prod_short.md)]. Koderna för arbetsflödesmallar som skapas av Microsoft har prefixet ”MS-”.  

Ett annat sätt att snabbt att skapa ett arbetsflöde är att importera ett befintligt arbetsflöde som du har i en fil utanför [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md).  

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template" />Så här skapar du ett arbetsflöde från en arbetsflödesmall

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Nytt arbetsflöde från mallen**. Sidan **arbetsflödesmallar**.  
3. Markera en arbetsflödesmall och välj sedan **OK**.  

   Sidan **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen. Värdet i fältet **Kod** utökas med till exempel ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen.  
4. Fortsätt med att skapa arbetsflödet genom att redigera arbetsflödesstegen, eller lägg till nya steg. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## <a name="see-also" />Se även

[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Exportera och importera godkännandearbetsflöden](across-how-to-export-and-import-workflows.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Ta bort arbetsflöden för godkännande](across-how-to-delete-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

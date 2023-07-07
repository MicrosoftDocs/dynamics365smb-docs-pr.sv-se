---
title: 'Gör så här: Exportera och importera arbetsflöden för godkännande'
description: 'För att överföra arbetsflöden till andra Business Central-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="export-and-import-approval-workflows"></a>Exportera och importera godkännandearbetsflöden

För att överföra arbetsflöden till andra [!INCLUDE[prod_short](includes/prod_short.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.  

Ett annat sätt att snabbt skapa arbetsflöden är att använda arbetsflödesmallar. Läs mer på [Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a>Exportera ett arbetsflöde

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.  

## <a name="import-a-workflow"></a>Importera ett arbetsflöde

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Importera från fil**.  
3. På sidan **Importera**, välj **Välj**, välj XML-filen som innehåller arbetsflödet och välj sedan **Öppna**.  

> [!CAUTION]  
> Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.  

## <a name="see-also"></a>Se även

[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Ta bort arbetsflöden för godkännande](across-how-to-delete-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: 'Gör så här: Exportera och importera arbetsflöden | Microsoft Docs'
description: För att överföra arbetsflöden till andra Business Central-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a52d4b4bff0f96023b6206e6cb8cad3d9e59276
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129936"
---
# <a name="export-and-import-workflows"></a>Exportera och importera arbetsflöden

För att överföra arbetsflöden till andra [!INCLUDE[prod_short](includes/prod_short.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.  

Ett annat sätt att snabbt skapa arbetsflöden är att skapa arbetsflöden från arbetsflödesmallar. Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).  

På sidan **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Så här exporterar du ett arbetsflöde

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.  

## <a name="to-import-a-workflow"></a>Så här importerar du ett arbetsflöde

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Importera från fil**.  
3. På sidan **Importera** väljer du knappen **Välja**, välj XML-filen som innehåller arbetsflödet och välj sedan **Öppna**.  

> [!CAUTION]  
> Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.  

## <a name="see-also"></a>Se även

[Skapa arbetsflöden](across-how-to-create-workflows.md)  
[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Ta bort arbetsflöden](across-how-to-delete-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden](across-set-up-workflows.md)  
[Använd arbetsflöden](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
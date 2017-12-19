---
title: "Gör så här: Exportera och importera arbetsflöden | Microsoft Docs"
description: "När du överför arbetsflöden till andra Dynamics 365-databaser kan du exportera och importera arbetsflöden, t.ex för att spara tid när du skapar nya arbetsflöden."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: sv-se
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a>Gör så här: Exportera och importera arbetsflöden
För att överföra arbetsflöden till andra [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, t.ex för att spara tid när du skapar nya arbetsflöden, kan du exportera och importera arbetsflöden.  

 Ett annat sätt att snabbt skapa arbetsflöden är att skapa arbetsflöden från arbetsflödesmallar. Mer information finns i [Så här skapar du arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).  

 I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. (Mer information finns i [Så här skapar du arbetsflöde](across-how-to-create-workflows.md).)  

## <a name="to-export-a-workflow"></a>Så här exporterar du ett arbetsflöde  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.  
2.  Markera ett arbetsflöde, och välj sedan åtgärden **Exportera till fil**.  
3.  I fönstret **Exportera fil** väljer du knappen **Spara**.  
4.  Välj en filplats i fönstret **Exportera** och välj sedan knappen **Spara**.  

## <a name="to-import-a-workflow"></a>Så här importerar du ett arbetsflöde  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.  
2.  Välj åtgärden **Importera från fil**.  
3.  I fönstret **Importera** väljer du den XML-fil som innehåller arbetsflödet och sedan knappen **Öppna**.  

> [!CAUTION]  
>  Om arbetsflödekoden redan finns i databasen skrivs arbetsflödesstegen över med stegen i det importerade arbetsflödet.  

## <a name="see-also"></a>Se även  
 [Så här skapar du arbetsflöden](across-how-to-create-workflows.md)   
 [Så här skapar du arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)   
 [Så här visar du arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)   
 [Så här tar du bort arbetsflöden](across-how-to-delete-workflows.md)   
 [Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Konfigurera arbetsflöden](across-set-up-workflows.md)   
 [Använda arbetsflöden](across-use-workflows.md)   
 [Arbetsflöde](across-workflow.md)   


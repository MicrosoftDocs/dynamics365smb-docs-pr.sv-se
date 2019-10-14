---
title: Använda arbetsflöden | Microsoft Docs
description: Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6535523fb34504a4f964971f41d4803bdc7b2117
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304762"
---
# <a name="using-workflows"></a>Använda arbetsflöden
Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

 Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare, skapa arbetsflöden, eventuellt tillämpa föregående kodanpassning och ange hur användarna ska meddelas. Mer information finns i [Konfigurera arbetsflöden](across-set-up-workflows.md).  

> [!NOTE]  
>  Vanliga arbetsflödessteg är när användare begär godkännande av aktiviteter och godkännare accepterar eller avvisar godkännandebegäranden. Därför handlar många avsnitt om hur du använder arbetsflöden i godkännande.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Ange ett arbetsflöde för att starta när den första instegshändelsen inträffar.|[Så här aktiverar du arbetsflöden](across-how-to-enable-workflows.md)|  
|Begär godkännande för en aktivitet, som en godkännare, acceptera, avvisa eller delegera godkännanden och skicka eller visa godkännandemeddelanden.|[Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md)|  
|Skapa arbetsflödessteg som begränsar en viss posttyp från att användas innan en viss händelse uppstår, till exempel att posten godkänns.|[Begränsa och tillåt användningen av en post](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Visa avslutade arbetsflödessteginstanser med statusen Avslutat.|[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)|  
|Ta bort ett arbetsflöde som du vet inte ska användas längre.|[Ta bort arbetsflöden](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a>Se även  
[Konfigurera arbetsflöden](across-set-up-workflows.md)   
[Arbetsflöde](across-workflow.md)   
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

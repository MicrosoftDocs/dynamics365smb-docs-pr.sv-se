---
title: Hantera, ta bort eller komprimera dokument | Microsoft Docs
description: "Behåll historiska data eller ta bort dessa."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 10524be6bcfdc99672496b54903e4f04c33108ce
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="manage-documents"></a>Hantera dokument
En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.  

## <a name="delete-documents"></a>Ta bort dokument
I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder som inte raderats. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolleras att borttagna inköpsorder har fakturerats helt. Du kan inte ta bort order som inte har fakturerats och inlevererats helt.  

Returorder tas vanligtvis bort när de har fakturerats. När du bokför en faktura överförs den till fönstret **Bokförd inköpskreditnota**. Om du har markerat kryssrutan **Returutleverans i kreditnota** i fönstret **Inköpsinställningar** överförs fakturan till fönstret **Bokförd returutleverans**. Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**. Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.  

Avropsorder tas inte bort när du har behandlat och fakturerat alla relaterade inköpsorder. Du kan ta bort avropsorder med batch-jobbet **Ta bort fakturerade avropsorder**.  

Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt. När en faktura bokförs skapas en motsvarande transaktion i fönstret **Bokförda servicefakturor**. Det bokförda dokumentet kan visas från fönstret **Bokförd servicefaktura**.  

Serviceordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från fönstret **Servicefaktura**, gäller följande. Då kan du behöva ta bort fakturerade order som inte har tagits bort. Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.  

## <a name="see-also"></a>Se även  
[Installation och administration i Dynamics 365 for Financials](admin-setup-and-administration.md)  


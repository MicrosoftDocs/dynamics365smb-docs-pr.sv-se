---
title: "Så här konfigurerar du dokumentutskicksprofiler | Microsoft Docs"
description: "Så här konfigurerar du dokumentutskicksprofiler"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d42de516efcc866fcfb04f36fb9c3cbffd3a667d
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-document-sending-profiles"></a>Så här konfigurerar du dokumentutskicksprofiler
Du kan skapa varje kund med en föredragen metod för att skicka försäljningsdokument så att du inte behöver välja alternativ varje gång som du väljer åtgärden **Bokför och skicka**.

I fönstret **Dokumentutskicksprofiler** konfigurerar du olika utskicksprofiler som du kan välja bland i fältet **Dokumentutskicksprofil** på ett kundkort. Du kan markera kryssrutan **Standard** om du vill ange att dokumentutskicksprofilen är standardprofilen för alla kunder förutom för kunder som har fältet **Dokumentutskicksprofil** ifyllt med en annan utskicksprofil.

När du väljer åtgärden **Bokför och skicka** i ett försäljningsdokument visar dialogrutan **Bekräftelse för bokför och utskick** den utskicksprofil som använts, antingen den som angetts för kunden eller standardinställningen för alla kunder. I dialogrutan kan du ändra utskicksprofilen för det specifika försäljningsdokumentet. Mer information finns i [Så här fakturerar du försäljning](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Så här konfigurerar du en dokumentutskicksprofil
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Dokumentutskicksprofiler**, och välj sedan relaterad länk.
2. I fönstret **Dokumentutskicksprofiler** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Så här anger du en utskicksprofil på ett kundkort
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kunder**, och välj sedan relaterad länk.
2. Öppna kortet för kunden som du vill skapa en utskicksprofil för.
3. I fältet **Dokumentutskicksprofil** väljer du en profil som du har konfigurerat enligt beskrivningen i föregående procedur.

## <a name="see-also"></a>Se även
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


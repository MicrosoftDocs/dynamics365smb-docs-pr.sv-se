---
title: Konfigurera föredragna metoder för att skicka försäljningsdokument | Microsoft Docs
description: Beskriver hur du ställer in respektive kunds standardmetod för att skicka dokument, till exempel e-transaktion, PDF, elektroniska dokument och så vidare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b91a1c0566b6fb4736093ca9617a5a1566bf2bf
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436682"
---
# <a name="set-up-document-sending-profiles"></a>Skapa dokumentutskicksprofiler
Du kan skapa varje kund med en föredragen metod för att skicka försäljningsdokument så att du inte behöver välja alternativ varje gång som du väljer åtgärden **Bokför och skicka**.

På sidan **Dokumentutskicksprofiler** konfigurerar du olika utskicksprofiler som du kan välja bland i fältet **Dokumentutskicksprofil** på ett kundkort. Du kan markera kryssrutan **Standard** om du vill ange att dokumentutskicksprofilen är standardprofilen för alla kunder förutom för kunder som har fältet **Dokumentutskicksprofil** ifyllt med en annan utskicksprofil.

När du väljer åtgärden **Bokför och skicka** i ett försäljningsdokument visar dialogrutan **Bekräftelse för bokför och utskick** den utskicksprofil som använts, antingen den som angetts för kunden eller standardinställningen för alla kunder. I dialogrutan kan du ändra utskicksprofilen för det specifika försäljningsdokumentet. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a>Så här konfigurerar du en dokumentutskicksprofil
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Dokumentutskicksprofiler** och väljer sedan relaterad länk.
2. På sidan **Dokumentutskicksprofiler** väljer du åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Så här anger du en utskicksprofil på ett kundkort
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna kortet för kunden som du vill skapa en utskicksprofil för.
3. I fältet **Dokumentutskicksprofil** väljer du en profil som du har konfigurerat enligt beskrivningen i föregående procedur.

## <a name="see-also"></a>Se även
[Konfigurera försäljning](sales-setup-sales.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
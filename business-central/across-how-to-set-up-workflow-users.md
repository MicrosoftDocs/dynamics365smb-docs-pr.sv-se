---
title: Så här konfigurerar du arbetsflödesanvändare
description: Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå på sidan Arbetsflödesanvändargrupp.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 187ff9bad2fb8bf320872759115e98b326b689c8
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130206"
---
# <a name="set-up-workflow-users"></a>Konfigurera arbetsflödesanvändare

Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå i arbetsflödena. Det behövs för att ange till exempel vem som ska ta emot en notering för att agera på ett arbetsflödessteg.  

Konfigurera användare under arbetsflödesanvändargrupper på sidan **Arbetsflödesanvändargrupp** och ange användarna i ordningsföljd i till exempel en godkännarkedja.  

Arbetsflödesanvändare som fungerar som godkännandeanvändare, både den som begär och den som godkänner, måste också ställas in på sidan **Användarinställningar för godkännande**. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Om du vill definiera att en godkännandebegäran inte godkänns förrän flera godkännare i en godkännandekedja har godkänt den, ställer du in godkännare i en hierarki. För godkännartypen **godkännare** anger du godkännare på sidan **Användarinställningar för godkännande**. För godkännartypen **Arbetsflödesanvändargrupp** ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar hierarkin genom att tilldela inkrementella nummer till varje godkännare i fältet **Sekvensnr.** . Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md) och följande avsnitt.  
>
> Om du vill definiera att en godkännandebegäran inte godkänns förrän flera likvärdiga godkännare har godkänt den, oberoende av ett hierarki, ställer du in en plan arbetsflödesanvändargrupp. För godkännartypen **Arbetsflödesanvändargrupp**, ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar samma nummer till varje godkännare i fältet **Sekvensnr.** . Mer information finns i följande avsnitt:  

## <a name="to-set-up-a-workflow-user"></a>Så här konfigurerar du en arbetsflödesanvändare

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflödesanvändargrupper** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflödesanvändargrupp** öppnas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Beskriv arbetsflödet i fältet **Beskrivning**.  
5. Fyll i fälten på den första raden enligt beskrivningen i följande tabell på snabbfliken **Medlemmar i arbetsflödesanvändargrupp**.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Användarnamn**|Ange användaren som ska ingå i arbetsflöden.<br /><br /> Användaren måste finnas på sidan **Användarinställningar**. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).|  
    |**Sekvensnr**|Ange den ordning som arbetsflödesanvändaren agerar i ett arbetsflöde i förhållanden till andra användare. Detta fält kan användas, till exempel, för att ange när användaren godkänner i förhållande till andra godkännare när du använder alternativet **Arbetsflödesanvändargrupp** i fältet **Godkännartyp** på det relaterade arbetsflödesvaret.<br /><br /> **Tips!** Om du vill definiera att en godkännandebegäran krävs att flera användare har godkänt den, oavsett plats i en hierarki, ställer du in en plan arbetsflödeanvändargrupp genom att tilldela samma sekvensnumret till de relevanta godkännarna.|  
6. Upprepa steg 5 för att lägga till fler arbetsflödesanvändare i användargruppen.  
7. Upprepa steg 2 till 6 för att lägga till fler arbetsflödesanvändargrupper.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Se även

[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Konfigurera arbetsflöden](across-set-up-workflows.md)  
[Använd arbetsflöden](across-use-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
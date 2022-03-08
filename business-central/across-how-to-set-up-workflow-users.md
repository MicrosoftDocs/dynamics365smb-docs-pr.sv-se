---
title: Så här skapar du arbetsflödesanvändare | Microsoft Docs
description: Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå i arbetsflödena. Det behövs för att ange till exempel vem som ska ta emot en notering för att agera på ett arbetsflödessteg.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ee8080689c948daa14d05e8b970de63da749746e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305218"
---
# <a name="set-up-workflow-users"></a>Konfigurera arbetsflödesanvändare
Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå i arbetsflödena. Det behövs för att ange till exempel vem som ska ta emot en notering för att agera på ett arbetsflödessteg.  

Konfigurera användare under arbetsflödesanvändargrupper på sidan **Arbetsflödesanvändargrupp** och ange användarna i ordningsföljd i till exempel en godkännarkedja.  

Arbetsflödesanvändare som fungerar som godkännandeanvändare, både den som begär och den som godkänner, måste också ställas in på sidan **Användarinställningar för godkännande**. Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
>  Om du vill definiera att en godkännandebegäran inte godkänns förrän flera godkännare i en godkännandekedja har godkänt den, ställer du in godkännare i en hierarki. För godkännartypen **godkännare** anger du godkännare på sidan **Användarinställningar för godkännande**. För godkännartypen **Arbetsflödesanvändargrupp** ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar hierarkin genom att tilldela inkrementella nummer till varje godkännare i fältet **Sekvensnr.** . Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-approval-users.md) och i detta avsnitt.  
>   
>  Om du vill definiera att en godkännandebegäran inte godkänns förrän flera likvärdiga godkännare har godkänt den, oberoende av ett hierarki, ställer du in en plan arbetsflödesanvändargrupp. För godkännartypen **Arbetsflödesanvändargrupp**, ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar samma nummer till varje godkännare i fältet **Sekvensnr.** . Mer information finns i det här avsnittet.  

### <a name="to-set-up-a-workflow-user"></a>Så här konfigurerar du en arbetsflödesanvändare  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Arbetsflödesanvändargrupper** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflödesanvändargrupp** öppnas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Beskriv arbetsflödet i fältet **Beskrivning**.  
5. Fyll i fälten på den första raden enligt beskrivningen i följande tabell på snabbfliken **Medlemmar i arbetsflödesanvändargrupp**.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Användarnamn**|Ange användaren som ska ingå i arbetsflöden.<br /><br /> Användaren måste finnas på sidan **Användarinställningar**. Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).|  
    |**Sekvensnr**|Ange den ordning som arbetsflödesanvändaren agerar i ett arbetsflöde i förhållanden till andra användare. Detta fält kan användas, till exempel, för att ange när användaren godkänner i förhållande till andra godkännare när du använder alternativet **Arbetsflödesanvändargrupp** i fältet **Godkännartyp** på det relaterade arbetsflödesvaret. **Tips!** Om du vill definiera att en godkännandebegäran inte godkänns förrän flera godkännare har godkänt den, oavsett plats i en hierarki, ställer du in en plan arbetsflödeanvändargrupp genom att tilldela samma sekvensnumret till de relevanta godkännarna.|  
6. Upprepa steg 5 för att lägga till fler arbetsflödesanvändare i användargruppen.  
7. Upprepa steg 2 till 6 för att lägga till fler arbetsflödesanvändargrupper.  

## <a name="see-also"></a>Se även  
[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
[Konfigurera arbetsflöden](across-set-up-workflows.md)   
[Använda arbetsflöden](across-use-workflows.md)   
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Arbetsflöde](across-workflow.md)   

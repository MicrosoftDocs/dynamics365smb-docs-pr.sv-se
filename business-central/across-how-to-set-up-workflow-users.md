---
title: Så här konfigurerar du arbetsflödesanvändare
description: Innan du kan skapa arbetsflöden måste du ställa in de användare som ska ingå på sidan Arbetsflödesanvändargrupp.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
---
# Konfigurera arbetsflödesanvändare

Innan du kan skapa arbetsflöde för godkännande måste du ställa in de användare som ska ingå i arbetsflödena. Det behövs för att ange till exempel vem som ska ta emot en notering för att agera på ett arbetsflödessteg.  

Konfigurera användare under arbetsflödesanvändargrupper på sidan **Arbetsflödesanvändargrupp** och ange användarna i ordningsföljd i till exempel en godkännarkedja. 

Arbetsflödesanvändare som fungerar som godkännandeanvändare, både den som begär och den som godkänner, måste också ställas in på sidan **Användarinställningar för godkännande**. Läs mer i [Så här skapar du användare för godkännande](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Om du vill definiera att en godkännandebegäran inte godkänns förrän flera användare har godkänt den, ställer du in godkännare i en hierarki. För godkännartypen **godkännare** anger du godkännare på sidan **Användarinställningar för godkännande**. För godkännartypen **Arbetsflödesanvändargrupp** ställer du in godkännare på sidan **Arbetsflödesanvändargrupper** och definierar hierarkin genom att tilldela inkrementella nummer till varje godkännare i fältet **Sekvensnr.** . Läs mer i [Så här skapar du användare för godkännande](across-how-to-set-up-approval-users.md). 

## Så här konfigurerar du en arbetsflödesanvändare

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflödesanvändargrupper** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Sidan **Arbetsflödesanvändargrupp** öppnas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Beskriv arbetsflödet i fältet **Beskrivning**.  
5. Fyll i fälten på den första raden enligt beskrivningen i följande tabell på snabbfliken **Medlemmar i arbetsflödesanvändargrupp**.  

   |Fält|Description|
   |-----|-----------|
   |**Användarnamn**|Ange användaren som ska ingå i arbetsflöden.<br /><br /> Användaren måste finnas på sidan **Användarinställningar**. Läs mer i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).|
   |**Sekvensnr**|Ange den ordning som arbetsflödesanvändaren agerar i ett arbetsflöde i förhållanden till andra användare. Detta fält kan användas, till exempel, för att ange när användaren godkänner i förhållande till andra godkännare när du använder alternativet **Arbetsflödesanvändargrupp** i fältet **Godkännartyp** på det relaterade arbetsflödesvaret.| 

   > [!TIP]
   > Tips! Om du vill definiera att en godkännandebegäran krävs att flera användare har godkänt den, oavsett plats i en hierarki, ställer du in en plan arbetsflödeanvändargrupp genom att tilldela samma sekvensnumret till de relevanta godkännarna.

6. Upprepa steg 5 för att lägga till fler arbetsflödesanvändare i arbetsflödesanvändargrupp.  
7. Upprepa steg 2 till 6 för att lägga till fler arbetsflödesanvändargrupper.  

## Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## Se även

[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

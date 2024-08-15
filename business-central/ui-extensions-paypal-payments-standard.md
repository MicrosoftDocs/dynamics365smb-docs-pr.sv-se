---
title: Använda tillägget för PayPal Payments Standard
description: Denna artikel beskriver hur du kan använda standardtillägget får att låta kunderna betala med PayPal.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Tillägget PayPal Payments Standard

Tillägget PayPal Payments Standard kan hjälpa dig att öka kundservicenivån genom att göra det enklare för dina kunder att betala sina räkningar.

Som ett alternativ till att samla in betalningar via banköverföring eller kredit Kort kan kunderna betala via sitt PayPal konto. När du skickar en försäljningsfaktura per e-post, finns en PayPal-länk i e-postbrödtexten och i det bifogade PDF-dokumentet. Om kunden väljer länken öppnas servicesidan för det PayPal kontot och betalningsinformationen visas. Då kan kunden betala fakturan som en PayPal-betalning.

Tjänsten för PayPal Payments Standard ger följande förmåner:

* Kundutbetalningar anländer snabbare till ditt bankkonto.
* Kunder har flera sätt att betala fakturor.
* PayPal har en trovärdig betalningtjänst, som kunder föredrar istället för att ange information om kreditkort på webbplatser.
* PayPal erbjuder flera sätt för att hantera betalningar, inklusive bearbetning av kreditkort, PayPal-konton och andra källor.
* PayPal-länken kan läggas till automatiskt till försäljningsdokument eller manuellt av användaren.
* Tjänsten för PayPal Payments Standard har inte månatliga avgifter eller installationsavgifter.
* Eftersom det är ett tillägg, kan du enkelt aktivera tjänsten för PayPal Payment Standard när din verksamhet kräver det.  

Mer information om hur du konfigurerar tillägget finns i [Aktivera kundbetalning via PayPal](sales-how-enable-payment-service-extensions.md).

## Registrera betalningar automatiskt för företagskonton

[!INCLUDE [prod_short](includes/prod_short.md)] kan registrera betalningar automatiskt om du har ett företagshandelskonto för PayPal Commerce Platform. När dina kunder använder länken PayPal för att betala en faktura [!INCLUDE [prod_short](includes/prod_short.md)]  bokför transaktionerna och stänger dokumentet.

Om du vill använda den här funktionen aktiverar du växlingsknappen **Registrera betalningar automatiskt** på sidan Inställningar för betalningsregistrering [!INCLUDE [prod_short](includes/prod_short.md)] i **och verifierar vilka konton du ska använda för betalningarna.**  Om du bestämmer dig för att du inte vill registrera betalningar automatiskt kan du stänga av betalningen igen.

> [!TIP]
> Utvecklare kan använda sandbox-konton för att testa konfigurationen. Det gör du genom att ändra URL:en för PayPal till **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] använder PayPals Instant Payment Notification (IPN) via notify_url.

## Se även

[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

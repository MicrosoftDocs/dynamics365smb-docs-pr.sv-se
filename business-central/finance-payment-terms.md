---
title: Konfigurera betalningsvillkor
description: Använd betalningsvillkor för att hantera förfallodatum och betalningar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Konfigurera betalningsvillkor

Betalningsvillkor avgör hur du hanterar förfallodatum och kassarabatter. Du kan använda datumformler för att definiera betalningsvillkoren. När du registrerar dig för [!INCLUDE [prod_short](includes/prod_short.md)] för första gången erbjuder demonstrationsföretaget några betalsätt som företagen ofta använder. Du kan emellertid lägga till hur många rader du vill.  

Om du tilldelar betalningsvillkor till kunder och leverantörer så att samma villkor alltid används i de försäljnings- inköpsdokument som du skapar för dem. Dokumentdatumen på försäljnings- och inköpsdokument, inte deras bokföringsdatum, används för att beräkna förfallodatum för betalningar. Om det behövs kan du ändra villkoren för försäljnings- eller inköpsdokument. Till exempel om du vill att en viss kund ska betala dig inom sju dagar i stället för standardvärdet 14 dagar. Om du ändrar villkoren i dokumentet ändras inte standardbetalningsvillkoret som tilldelats kunden. Samma betalningsvillkor finns för försäljnings- och inköpsdokument.

När du sedan bokför en faktura beräknar [!INCLUDE [prod_short](includes/prod_short.md)] kassarabatterna baserat på betalningsvillkoren. Datum för betalningsrabatt är det sista datum då kunden kan få rabatt. Datumet beräknas också när du bokför en faktura.  

När du bokför en kreditnota kommer på samma sätt [!INCLUDE [prod_short](includes/prod_short.md)] att beräkna kassarabatter som baseras på betalningsvillkoren. Den beräknar rabatten på kreditnotor på samma sätt som rabatter på fakturor. När du kopplar en kreditnota till en faktura [!INCLUDE [prod_short](includes/prod_short.md)] minskar rabattbeloppet för fakturan med kreditnotans rabattbelopp.  

Om du vill skicka påminnelser om förfallna betalningar måste du ange nivåer och villkor för betalningspåminnelser. Om du vill veta mer om påminnelser, gå till [Konfigurera villkor och nivåer för betalningspåminnelser](finance-setup-reminders.md).  

## Så här definierar du betalningsvillkor

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **betalningsvillkor** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

När du har ställt in betalningsvillkoren tilldelar du dem till kunder och leverantörer. Du kan också tilldela betalningsvillkor till dina betalsätt.  

> [!TIP]
> I basversionen av [!INCLUDE [prod_short](includes/prod_short.md)] stöds inte betalningsvillkor med delbetalningar. Istället måste du använda funktionen för förskottsbetalning. Om du vill veta mer om förskottsbetalningar, gå till [Konfigurera förskottsbetalningar](finance-set-up-prepayments.md).
>
> I vissa länder/regioner *kan* du ställa in betalningsvillkor med delbetalningar. För att ta reda på om ditt land/din region stöder denna funktion, gå till avsnittet **Lokal funktionalitet** i innehållsförteckningen till vänster i en artikel [Microsoft Learn](about-localization.md).

## Se även

[Konfigurera betalningssätt:](finance-payment-methods.md)  
[Konfigurera förskottsbetalningar](finance-set-up-prepayments.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

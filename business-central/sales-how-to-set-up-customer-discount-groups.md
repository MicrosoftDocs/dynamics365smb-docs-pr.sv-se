---
title: Ställ in kundrabattgrupper
description: Lär dig hur du ställer in kundrabattgrupper och skapar försäljningsrabatter för dessa grupper.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: bholtorf
---
# <a name="set-up-customer-discount-groups"></a>Ställ in kundrabattgrupper

Du kan definiera försäljningsradrabatter för en grupp med kunder i stället för att använda dem var för sig.

**Kundrabattgrupper** fungerar på samma sätt som [kundprisgrupper](sales-how-to-set-up-customer-price-groups.md) men kan kombineras med artikelrabattgrupper för att snabbt sätta radrabatter på många varor för utvalda kunder.

## <a name="create-sales-line-discounts-for-a-customer-group"></a>Skapa försäljningsrabatter för en kundgrupp

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kundrabattgrupper** och väljer sedan relaterad länk.
2. På sidan **Kundrabattgrupper**, välj **Ny** för att skapa en ny rabattgrupp och ge den ett namn under kolumnen **kod** och lägger till en beskrivning.
3. Välj åtgärden **Navigera** och välj **Försäljningsradrabatter**.
4. Fyll i kolumnen **försäljningskoden** med rabattgruppen skapad på föregående sida.
5. Fyll i fälten på raderna med **Typ** (artikel eller artikelrabattgrupp), **Kod**, **Unit of Measure Code** och **Radrabatt %**.
6. Om kundgruppen måste köpa ett lägsta antal för att erhålla rabatten fyller du i fältet **Minimiantal**.
7. Ange vid behov **Startdatum** och **Slutdatum** för rabattgruppen.
8. Om det behövs kan du även ange **valutakod** eller **variantkod**efter [att du har anpassat kolumnerna](ui-personalization-user.md).

Upprepa steg 4–8 för varje artikel eller artikelrabattgrupp som du vill skapa en försäljningsradrabatt för.

## <a name="assign-a-customer-to-a-discount-group"></a>Tilldela en kund till en rabattgrupp

När du har skapat kundrabattgrupperna kan du ange koderna för kundrabattgrupp på kundkorten.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna  **kundkortet** för en kund som du vill ska ingå i en kundrabattgrupp.
3. På snabbfliken **Fakturering** i fältet **Kundrabattgrupp** väljer du gruppkod.

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Registrera speciella försäljningspriser och rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  
[Ställ in kundprisgrupper](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

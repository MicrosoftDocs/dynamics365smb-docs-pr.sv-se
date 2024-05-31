---
title: Ställ in kundprisgrupper
description: Lära dig hur du lägger upp kundprisgrupper och skapar försäljningspriser för dessa grupper.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customer price groups, discounts, sales prices'
ms.date: 09/30/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-customer-price-groups"></a>Ställ in kundprisgrupper
  
Försäljningspriser kan skapas beroende på vilken kundgrupp du säljer till. Dessa grupper kallas kundprisgrupper.

Innan du skapar kundprisgrupper måste du bestämma hur många grupper du vill skapa och vilka kunder som ska tillhöra varje grupp.  

## <a name="how-to-create-sales-prices-for-a-group-of-customers"></a>Så här skapar du försäljningspriser för kundgrupper

När du och kunderna har kommit överens om vilka priser som kundgruppen ska betala för specifika artiklar, registrerar du dessa för de enskilda artiklarna på raderna på sidan **Förs.priser**.

### <a name="to-create-sales-prices-for-a-group-of-customers"></a>Så här skapar du försäljningspriser för kundgrupper

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kundprismallar** och väljer sedan relaterad länk.  

2. Markera raden med önskad kundprisgrupp. Om en rad inte redan finns kan du skapa en ny rad. Välj **nytt** om du vill skapa en ny entitet och ge den ett namn.  
    
    Kontrollera att innehållet i fälten **Tillåt radrabatt**, **Tillåt fakturarabatt**, **Pris inklusive moms** och **Moms rörelsebokf.mall prisgr (pris)**. 
  
3. Välj åtgärden **Navigera** och välj **Försäljningspriser**. Sidan **Försäljningspris** visas. Fältet **förs.typ** är ifyllt med **Kund prisgrupp**.  
  
4. Fyll i **försäljningskoden** med den försäljningskod som du valde på föregående sida.  
  
5. Fyll i fälten på raderna med **Artikelnr**, **Enhetskod** och överenskommet **A-pris**. Du kan även visa kolumnen **Variantkod** och ange **Variantkod** om det finns flera olika varianter av artikeln.  
  
6. Om kundgruppen måste köpa ett visst minsta antal för att överenskommet pris ska gälla, fyller du i fältet **Minimiantal**.  

7. Ange vid behov **Startdatum** och **Slutdatum** för prisavtalet.  
  
8. Om detta är relevant anger du **Valutakod**.

Upprepa steg 4 till och med 8 för alla artiklar som du vill skapa ett försäljningspris för.

## <a name="how-to-enter-customer-price-group-codes-on-customer-cards"></a>Så här anger du koder för kundprisgrupper på kundkort

När du har skapat kundprisgrupperna kan du ange koderna för kundprisgrupperna på kundkorten.

### <a name="to-enter-customer-price-group-codes-on-a-customer-card"></a>Så här anger du koder för kundprisgrupper på kundkort

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.  

2. Öppna  **kundkortet** för en kund som du vill ska ingå i en kundprisgrupp.  

3. På snabbfliken **Fakturering**, i fältet **Kundprisgrupp**. öppna kod **Kundprisgrupp**.  


## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Registrera speciella försäljningspriser och rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  
[Ställ in kundrabattgrupper](sales-how-to-set-up-customer-discount-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

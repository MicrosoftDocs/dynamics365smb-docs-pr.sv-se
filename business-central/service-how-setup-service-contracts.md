---
title: Skapa servicekontrakt
description: 'Så här skapar du servicekontrakt med nödvändiga förutsättningar, inklusive servicekontraktgrupper, kontraktmallar och kundmallar.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'service, cost, service order'
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-service-contracts"></a>Skapa servicekontrakt
Innan du kan arbeta med kontrakt, måste du ställa in följande: 

* **Servicekontraktsgrupper**, som innehåller grupper med servicekontrakt som har vissa gemensamma egenskaper.
* **Servicekontraktskontogrupper**, som används för att gruppera olika konton för servicekontrakt för servicefakturor som skapas för servicekontrakt. Du kan tilldela dessa grupper servicekontrakt.  
* **Kontraktsmallar** som definierar kontrakslayouter av kontrakt som innehåller de vanligaste kontraktuppgifterna. Du kan skapa servicekontraktsofferter genom att använda mallar. När du skapar en kontraktsoffert innehållet fälten mallfälten automatiskt.
* **Kundmallar** låter dig skapa serviceofferter för kontakter eller potentiella kunder som inte är registrerade som kunder i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Så här skapar du en servicekontraktsgrupp
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontraktgrupper** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Markera kryssrutan **Endast rabatt på kont.order** om du vill att kontrakts- eller servicerabatter endast ska gälla för kontraktserviceorder, t. ex. underhåll.  

## <a name="to-set-up-a-service-contract-account-group"></a>Så här skapar du servicekontraktskontogrupper
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serv.kontrakt redov.konton** och väljer sedan relaterad länk.  
2. Skapa en ny servicekontraktskontomall.   
3. Fyll i fälten **Kod** och **Beskrivning**. Dessa fält beskriver servicekontogruppen.  
4. Fyll i fältet  **Ej förutbetalt kontrakt**. Det här fältet innehåller redovisningskontonumret för det konto som inte är förutbetalt.  
5. Fyll i fältet **Ej förutbetalt kontrakt**. Det här fältet innehåller redovisningskontonumret för det konto som inte är förutbetalt.  

## <a name="to-set-up-a-contract-template"></a>Så här skapar du en kontraktsmall
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontraktmallar** och väljer sedan relaterad länk.  
2. Skapa en ny servicekontraktsmall.  
3. I fältet **Nr.** Skriv numret på den artikel som har beställts i kontraktmallen.  
  
     Om du har skapat en nummerserie för kontraktsmallar på sidan **Serviceinställningar** kan du trycka på <kbd>Retur</kbd> om du vill ange nästa lediga kontraktmallsnummer. Fyll i resterande fält om det behövs.  
  
4. På snabbfliken **Faktura** fyller du i fältet **Serv.kontrakt kontomall kod** i **Fakturaperiod**, osv. Fyll i resterande fält om det behövs.  
5. Välj åtgärden **Servicerabatter** om du vill lägga till kontraktsrabatter.  

## <a name="to-set-up-a-customer-template"></a>Så här skapar du en kundmall
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kundmallar** och väljer sedan relaterad länk.  
2. Skapa ett nytt kundmallskort.  
3. Skriv en kod och en beskrivning av kundmallen på snabbfliken **Allmänt** i fälten **Kod** respektive **Beskrivning**. 
4. Om du vill definiera sökvillkor fyller du i de andra fälten, till exempel **Lands-/regionkod**, **Distriktskod** och **Språkkod**.  
5. Fyll i fälten  **Rörelsebokföringsmall** och  **Kundbokföringsmall**.  

## <a name="see-also"></a>Se även
[Ställa in tjänstehantering](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

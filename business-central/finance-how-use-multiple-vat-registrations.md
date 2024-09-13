---
title: Flera momsregistreringsnummer
description: Lär dig mer om funktionerna för flera (alternativa) momsregistreringsnummer.
author: altotovi
ms.topic: conceptual
ms.reviewer: null
ms.search.keywords: 'VAT, multiple, alternative, customer, tax, value-added tax'
ms.search.form: '212, 301,'
ms.date: 08/21/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Flera momsregistreringsnummer 

För företag med lager i flera EU-länder kan det vara svårt att hantera moms (Value Added Tax), eftersom varje lagerställe kräver olika momsregistreringsnummer för att följa de specifika reglerna i varje land. Den här artikeln innehåller information om det här kravet och förklarar funktionerna för flera momsregistreringsnummer. Med den här funktionen kan användare ställa in momsregistreringsnummer för kunder i olika länder/regioner.  

> [!NOTE]
> Funktionen *Flera momsregistreringsnummer för kunder* är endast tillgänglig från Business Central 2024 utgivningscykel 2 (version 25).

## Så här ställer du in alternativa momsregistreringsnummer  

Så här ställer du in alternativa momsregistreringsnummer för olika länder/regioner: 

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") Anger du **Momsregistrering** för alternativ kund och Välj sedan relaterad länk. 
2. Lägg till kunden i **fältet Kundnr** och land/region som är relaterat till momsregistreringen i **momskoden för land/region**.  
3. Du måste lägga till momsregistreringsnumret i **momsregistreringsnumret.** fält. Du måste hålla dig till formatet när du använder **Lands-/regionkod**. 
4. Om du vill använda olika moms- eller bokföringsmallar kan du alternativt lägga till dem i inställningarna i fälten **Moms rörelsebokföringsmall** och **Gen. bussbokföringsmall** . 
5. Stäng sidan.   

Så här skapar du en alternativ adress till kunden:  

1. Öppna **Kund**  kort för den kund som du vill lägga till ny **leveransadress**. 
2. Välj **Kund** och välj **åtgärden Leveransadresser** .   
3. Sidan **Leveransadresslista** öppnas och väljer **Ny**. 
4. Fyll i informationen om kundens leveransdestination.  
5. Välj rätt **lands-/regionkod**.   
6. Om du redan har konfigurerat ett nytt **momsregistreringsnr.** i momsregistreringen **för alternativa kunder i det** här landet eller den här regionen kommer ingenting att hända. 
7. Men om du inte konfigurerade **momsregistreringsnumret.** Följande meddelande visas tidigare i Momsregistrering **för alternativa** kunder i det här landet eller den här regionen: **Klicka på Lägg till om du vill infoga den alternativa momsregistreringen för den här landskoden för leverans.** 
8. Ett meddelande visas som en varning om att du bör lägga till ett nytt momsregistreringsnummer. Om du vill göra det måste du välja **åtgärden Lägg till** i meddelandet så **öppnas sidan Momsregistrering** för alternativ kund. 
9. På den här sidan fylls ditt **kundnummer i.** Och momskoden **för** land/region. Så du behöver bara lägga till inställningar som du vill använda. 

## Arbeta med försäljningsdokumenten   

Du kan skapa en ny försäljningsfaktura eller [försäljningsorder](sales-how-invoice-sales.md) . [...](sales-how-sell-products.md)  [!INCLUDE[prod_short](includes/prod_short.md)] Om du behöver använda en leveransadress som skiljer sig från kundens adress och som finns i ett annat land följer du stegen:  

### Alternativ leveransadress  

1. Expandera **snabbfliken Leverans och fakturering** .   
2. I fältet Leveransadress väljer du alternativet **Alternativ leveransadress** . 
3. Sidan **Leveransadresslista** med tillgängliga alternativa adresser visas. 
4. Välj en av adresserna med en annan **lands-/regionkod**. 
5. Dialogrutan **Bekräfta momsregistrering** för alternativ kund visas med en lista med fält som du har ändrat på grund av ändringen av inställningarna för registrering av **alternativ kundmoms** . 
6. Välj **OK** att bekräfta.   

> [!NOTE]
> Om du inte vill bekräfta ett sådant val längre kan du Välj fältet **Visa inte igen** och i framtiden kommer du inte att se den här typen av meddelanden om ändringar. Men om du vill aktivera det igen kan du göra det genom att aktivera **fältet Bekräfta alternativ momsregistrering** i **momsinställningen**.  
   
7. När du har bekräftat skrivs värdena över med värdena från inställningarna för momsregistrering **för** alternativ kund. Du kan kontrollera alla momsrelaterade fält som finns på snabbfliken **Fakturadetaljer** .  
8. Bokför dokumentet.  

### Anpassad adress  

Om du inte har konfigurerat leveransadressen men ändå vill använda en annan adress för leverans kan du använda det här alternativet.  

1. Expandera **snabbfliken Leverans och fakturering** .   
2. I fältet Leveransadress väljer du alternativet **Anpassad adress** .  
3. Ändra land i fältet **Land/region** .  
4. När du har ändrat lands-/regionkoden så att den **matchar momskoden** för **den alternativa kundens momsregistrering** **visas dialogrutan Bekräfta momsregistrering** för alternativ kund med en lista över fält som har ändrats. 
5. [!INCLUDE[prod_short](includes/prod_short.md)] kommer också att ändra alla momsrelaterade fält som finns under snabbfliken **Fakturadetaljer** .  

### Arbeta utan leverans 

Om Dit inte är någon leverans som en process kan du fortfarande utnyttja inställningarna för momsregistrering **för** alternativa kunder.

På försäljningsordern eller fakturan **hittar du momskoden** för land/region under **snabbfliken Fakturadetaljer** och anger det värde som matchar inställningarna för registrering av **alternativ kundmoms.**  Och du bör se samma bekräftelsedialogsida som ovan. 

I det här fallet kan du bokföra en försäljningsfaktura med rätt **momsregistreringsnr.** för kunden, även om du inte levererar artiklar med det här dokumentet. 

### Arbeta med försäljningskreditnotan  

När du bokför fakturan med en leveransadress eller momskod **för land/region som har andra bokföringsdata,**  **hämtas värdena från det** bokförda försäljningsfakturahuvudet **där dessa värden hämtas från momsregistreringen**  för **alternativ kund, så inga andra åtgärder krävs.**  **·** 

## Se även

[Översikt över momshantering](finance-manage-vat.md)    
[Ställa in moms](finance-setup-vat.md)    
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)    
[Rapportera moms till en skattemyndighet](finance-how-report-vat.md)    
[Lokal funktionalitet i Business Central](about-localization.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]

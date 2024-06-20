---
title: Så här fördelar du resurser | Microsoft Docs
description: Du kan ändra det årliga beloppet på ett servicekontrakt eller en kontraktsoffert om du vill korrigera det årliga faktureringsbeloppet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Så här tilldelar du resurser
Nyckelelementen i tjänstehantering är de personer som tillhandahåller servicen. Du kan ställa in [!INCLUDE[prod_short](includes/prod_short.md)] till att tilldela rätt personer till rätt projekt. Fördelningarna kan baseras på servicezoner där personerna finns eller där servicen ska utföras. Dessutom kan du gruppera resurser tillsammans när du tar hand om en serviceförfrågan. Mer information finns i [Så här skapar du resursfördelning](service-how-setup-resource-allocation.md).

Du kan fördela resurser (till exempel tekniker) med hjälp av **Beordringstavla**, eller från en serviceorder. Du kan använda resursdisposition för att fördela resurser som ska utföra serviceuppgifterna i order eller offerter.

Fördela samma resurs, till exempel en tekniker eller resursgrupp, till alla serviceartiklar på en serviceorder. Fördelningstransaktioner skapas för de andra serviceartiklarna på ordern med samma resursnummer och fördelningsdatum som den rad du har tilldelat. De fördelade timmarna är de timmar som du har tilldelat, delat med antalet serviceartiklar på ordern. Fältet **Status** uppdateras automatiskt till **Aktiv** för alla transaktioner som har skapats.

## Så här visar du en översikt över serviceorder/serviceofferter  
Du kan ofta behöva titta på listan över serviceorder och/eller serviceofferter som uppfyller vissa krav så att du kan utföra särskilda åtgärder för var och en av dem. Du kan till exempel behöva fördela resurser till serviceorder som tillhör en viss kund.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Beordringstavla** och väljer sedan relaterad länk.  
2. Välj den dokumenttyp du vill visa i fältet **Dokumentfilter**.
3. Om du vill ha en lista över dokument som innehåller de serviceuppgifter som en viss resurs/resursgrupp är allokerade till fyller du i fälten **Resursfilter** och **Resursgruppfilter** och trycker på <kbd>Retur</kbd>.  
4. Om du vill ha en lista över dokument med ett visst svarsdatum eller med svarsdatum inom en viss period fyller du i fältet **Svarsdatumfilter** och trycker på <kbd>Retur</kbd>.  
5. Om du vill ha en lista över dokument med en viss fördelningsstatus eller dokumentstatus fyller du i fältet **Fördelningsfilter/statusfilter** och trycker på <kbd>Retur</kbd>.  
6. Om du vill ha en lista över dokument som tillhör ett visst kontrakt eller en viss kund eller zon fyller du i fältet **Kontraktsfilter/kundfilter/zonfilter** och trycker på <kbd>Retur</kbd>.  
7. Välj en rad som motsvarar en serviceorder eller serviceoffert och klicka på åtgärd **visa dokument**.  

    Sidan **Tjänsteorder** eller **Serviceoffert** öppnas, och du kan arbeta med dokumentet. Återgå till sidan **Beordringstavla** väljer **OK**.

## Så här fördelar du resurser med hjälp av Resursgruppsdisposition    
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Beordringstavla** och väljer sedan relaterad länk.  
2. Välj serviceordern och välj sedan åtgärd **Resursfördelningar**.  
3. Välj den transaktion som innehåller den serviceuppgift som du vill tilldela resurser till.  
4. Välj antingen åtgärd **resurstillgänglighet** eller **Resursgruppsdisposition**.  
5. På sidan **Res.disposition (Service)** väljer du **Visa matris**.  
6. Välj en resurs att fördela. Du kan basera valet på om resursen är utbildad för uppgiften, om den finns i kundzonen och/eller om den föredras av kunden.  
7. Välj ett datum då resursen har tillräckligt med timmar för uppgiften och som ligger nära svarsdatum för serviceordern.  
8. I fältet **Antal att fördela** anger du hur många timmar som ska tilldelas resursen för serviceuppgiften.  
9. Välj åtgärden **Fördela** för att fördela den valda resursen på det valda datumet.  

     Fältet **Status** anges automatiskt till **Aktiv**.  

 Upprepa de här stegen för varje datum när du vill tilldela resurser till serviceuppgiften.  

> [!NOTE]  
>  För serviceartiklar på en serviceorder kan det bara finnas **aktiva** fördelningstransaktioner med en resurs eller resursgrupp i taget.  

## Så här fördelar du resurser med hjälp av en serviceorder  
När du har skapat och fyllt i en serviceorder eller serviceoffert kan du fördela resurser, t. ex. tekniker som ska utföra serviceuppgifter som registrerats som serviceartikelrader i dokumentet.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Välj serviceorder, och sedan **Redigera**.  
3. Välj den serviceartikelrad som motsvarar den serviceuppgift som du vill fördela en resurs till.  
4. Välj **Resursfördelningar**.
5. Markera en inaktiv fördelningspost med den serviceuppgift som du vill fördela resursen till på sidan **Resursfördelningar**. Om den inaktiva fördelningsposten inte finns kan du skapa en ny med **Ny**.  
7. Ange serviceuppgiften genom att fylla i fältet **Serviceartikelnr** på samma rad.  
8. I fältet **Resursnr** väljer du önskad resurs. Om resursen ingår i en resursgrupp anges resursgruppens nummer automatiskt i fältet **Resursgruppnr**. .  
9. Fyll i fälten **Fördelningsdatum** och **Fördelade timmar**. Fältet **Status** ställs in på **Aktiv**. Det innebär att resursen fördelas till serviceuppgiften.  
10. Dessutom kan du välja om du vill tilldela resursen till alla artiklar med **fördela till alla serviceartiklar**.

> [!NOTE]  
>  För en serviceartikel på en serviceorder kan det endast finnas aktiva fördelningstransaktioner för en resurs eller resursgrupp åt gången.

## Så här omfördelar du resurser med hjälp av en serviceorder:  
Du kan omfördela resurser direkt från en serviceorder eller serviceoffert när du arbetar med den. Den ursprungliga transaktionen finns fortfarande kvar, men transaktionens status har uppdaterats:  

* Om servicen startade när fördelningen var **Aktiv**, dvs. om serviceartikelns reparationsstatus ändrats till **Pågående**, ändras fördelningsstatus från **Omfördelning nödvändig** till **Avslutad**.  
* Om servicen inte påbörjades när fördelningen var **Aktiv** ändras fördelningsstatus från **Omfördelning nödvändig** till **Inställd**.  
* Om du omfördelar en serviceorder som du har konverterat från en offert ändras alltid statusen för de fördelningstransaktioner som angetts på offerten till **Avslutad** när du omfördelar serviceartiklarna på serviceordern.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna relevant serviceorder.  
3. Markera den serviceartikelrad som motsvarar den serviceuppgift som du vill fördela en resurs till och välj sedan åtgärden **Resursfördelningar**.  
4. Markera en allokeringspost som innehåller den serviceuppgift som du vill omfördela resursen till på sidan **Resursfördelningar**. I fältet **Resursnr** väljer du önskad resurs. Detta gör att resursnumret som redan finns i fältet skrivs över.  
5. Välj <kbd>Retur</kbd>. En dialogruta öppnas där det frågas om du vill omfördela transaktionen. Fyll vid behov i fältet **Orsakskod** och klicka på **Ja** för att bekräfta omfördelningen.  
6. Fyll i fälten **Fördelningsdatum** och **Fördelade timmar**. Transaktionen innehåller nu den nya resursen vars status nu är **Aktiv**.

## Så här omfördelar du resurser genom att använda beordringstavlan  
Om en resurs som har fördelats till en serviceuppgift inte kan slutföra arbetet innebär det att denna serviceuppgift måste omfördelas. Vanligtvis omfördelar du resurser till en serviceuppgift med hjälp av **Beordringstavlan**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Beordringstavla** och väljer sedan relaterad länk.  
2. I fältet **Fördelningsfilter** markerar du **Omfördelning nödvändig**. Sidan **Beordringstavla** visar nu en lista med de serviceorder som inkluderar serviceuppgifter som behöver omfördelas.  
3. Välj relevant serviceorder och välj sedan åtgärd **Resursfördelningar**. Sidan **Resursfördelningar** visas.  
4. Välj fördelningstransaktionen med den serviceuppgift som du vill omfördela en resurs till.  
5. I fältet **Resursnr** väljer du önskad resurs. Resursnumret som redan finns i fältet skrivs över.  
6. Välj <kbd>Retur</kbd>. Dialogrutan **Omfördelningstrans. orsaker** öppnas med en fråga om du vill omfördela transaktionen. Fyll vid behov i fältet **Orsakskod** och klicka på **Ja** för att bekräfta omfördelningen.  
7.  Fyll i fälten **Fördelningsdatum** och **Fördelade timmar**. Transaktionen innehåller nu den nya resursen vars status är **Aktiv**.  

    > [!NOTE]  
    >  Den gamla transaktionen finns fortfarande kvar, men transaktionens status har uppdaterats på följande sätt:  
    >   
    >  * Om servicen startade när fördelningen var **Aktiv**, dvs. om serviceartikelns reparationsstatus ändrats till **Pågående**, ändras fördelningsstatus från **Omfördelning nödvändig** till **Avslutad**.  
    > * Om servicen inte påbörjades när fördelningen var **Aktiv**, ändras fördelningsstatus från **Omfördelning nödvändig** till **Inställt**.  
    > * Om du omfördelar en serviceorder som du har konverterat från en offert ändras alltid statusen för de fördelningstransaktioner som angetts på offerten till **Avslutad** när du omfördelar serviceartiklarna på serviceordern.  

## Så här registrerar du resurstimmar  
När du arbetar med serviceartiklar på en serviceorder måste du registrera de resurstimmar som läggs på servicen. Nedan beskrivs en procedur för att registrera resurstimmarna på sidan **Serviceartikeldokument**.  

Du kan använda en liknande procedur för att registrera timmarna på sidan **Servicerader** som du öppnar från sidan Tjänsteorder. Öppna relevant servicekort och välj sedan åtgärden **Servicerader**.  

Om samma resurs arbetar med alla serviceartiklar på serviceordern kan du registrera det totala antalet resurstimmar för endast en serviceartikel och sedan dela resursraden så att resurstimmarna tilldelas andra serviceartiklar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceuppgifter** och väljer sedan relaterad länk.
2. Klicka på raden som innehåller relevant serviceartikel och klicka på **Artikelkalkylark**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Så här fördelar du resurser till alla serviceartiklar på en serviceorder:
Om samma resurs (t. ex. en tekniker) arbetar med en serviceorders alla serviceartiklar kan du registrera det totala antalet resurstimmar på en enda serviceartikel och sedan dela resursraderna för att fördela resurstimmarna på de andra serviceartiklarnas resursrader.  

Följande visar hur man delar resursrader på sidan **Servicefakturarader**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Öppna relevant serviceorder.  
3. På snabbfliken **Rader** klickar du på åtgärden **Servicerader**. Sidan **Servicerader** öppnas.  
4. Klicka på den resursrad som du vill dela. Innehållet i fältet **Antal** delas mellan orderns alla serviceartiklar.  
5. Välj åtgärden **Dela resursrader**. Välj **Ja** för att bekräfta.  

    Resursrader skapas automatiskt för de andra serviceartiklarna på ordern med samma resursnummer som den rad du har delat. Antalet är antalet för den rad du delar dividerat med antalet serviceartiklar på ordern.  

## Så här annullerar du fördelningar  
Du kan avbryta resursfördelningar för serviceuppgifter utan att omfördela uppgifterna.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Beordringstavla** och väljer sedan relaterad länk.  
2. Välj serviceordern och välj sedan åtgärd **Resursfördelningar**.  
3. Välj den fördelningstransaktion som innehåller den serviceuppgift som du vill rätta fördelningen för.  
4. Välj åtgärden **Avbryt fördelningar**.  
5. I fältet **Orsakskod** klickar du på lämplig orsakskod.  
6. Klicka på knappen **Ja** för att bekräfta annulleringen.  

    > [!NOTE]  
    > Alternativet **Omfördelning nödvändig** väljs automatiskt i fältet **Status**. Om reparationsstatus för serviceartikeln är **Initial** ändras reparationsstatus till **Hänvisad** (ingen service har inletts). Om reparationsstatus är **Pågående** ändras reparationsstatus till **Delvis servad** (viss service har utförts).

## Se även
[Så här skapar du resursfördelningar](service-how-setup-resource-allocation.md)  
[Fördelningsstatus och reparationsstatus](service-allocation-status-and-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
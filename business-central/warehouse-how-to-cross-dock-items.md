---
title: Beräkna direktutleverans av artiklar
description: Lära dig hur du tar emot och levererar artiklar utan att lägga dem i lager.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# <a name="cross-dock-items"></a>Beräkna direktutleverans av artiklar

Artiklar för direktutleverans är artiklar som du tar emot och levererar utan att de tas bort. Processerna för artikelinförsel och plockning kräver begränsad hantering av artiklar. Du kan direktutleverera artiklar för utleveranser och för produktionsorder.

## <a name="cross-dock-bins-and-zones"></a>Lagerplatser och zoner för direktutleverans

Om du använder lagerplatser registrerar du minst en lagerplats för direktutleverans och anger lagerplatsen i fältet **Direktutleverans lagerställeskod** på lagerställena. Om du använder dirigerad artikelinförsel och plockning ställer du in en zon för direktutleverans.

När du förbereder en utleverans eller plockar artiklar i produktionssyfte, och använder lagerställen, plockas artikeln automatiskt från en lagerplats för direktutleveranser före någon annan lagerplats. Du måste kontrollera området för direktutleveranser och se om de artiklar som behövs är tillgängliga där, innan du hämtar artiklarna från det vanliga lagringsområdet.  

Om du har beräknat kvantiteter för direktutleverans, skapas automatiskt artikelinförselrader i lagerstället för direktutleveranser för beräkning av direktutleveranser när inleveransen bokförs. Övriga artikelinförselrader skapas som vanligt.  

## <a name="cross-dock-select-lines-for-a-receipt"></a>Direktutleverans markera rader för en inleverans

Om du vill bokföra artiklarna för direktutleverans direkt, så att de blir tillgängliga för plockning, måste du även registrera en artikelinförsel för de övriga artiklarna som kommer från inleveransraden, nämligen de som måste lagras. Om endast några av artiklarna på en inleveransrad direktutlevereras måste du därför försöka införa de återstående artiklarna så snabbt som möjligt. Alternativt kan lagerprincipen vara att uppmuntra direktutleverans av hela inleveransrader närhelst det är möjligt.

I instruktionen för artikelinförsel tar du bort instruktionsraderna för ta och placera för varje inleveransrad för artiklarna som ska föras in. Du kan återskapa instruktionsraderna senare eftersom artikelinförselrader från artikelinförselförslaget eller den bokförda inleveransen. När du har tagit bort instruktionsraderna kan du föra in och registrera raderna för artiklar för direktutleverans.  

## <a name="about-the-put-away-worksheet-page"></a>Sidan Om artikelinförselförslag

Om du aktiverar växlingsknappen **Använd artikelinförselkalkylark** på sidan **Lagerställekort** och bokförde inleveransen med beräknade direktutleveranser, blir samtliga inleveransrader tillgängliga i kalkylarket. Informationen om direktutleveranserna försvinner och kan inte återskapas. Därför bör du, om du vill använda funktionerna för direktutleverans, lägga om rader till artikelinförselkalkylarket genom att ta bort instruktioner för artikelinförseln i stället för att använda motsvarande automatiska funktion i fältet **Använd artikelinförselkalkylark**.  

Om du bokför lagerinleveransen, och växlingsknappen **Använd artikelinförselkalkylark** är inaktiverad, visas artiklarna som ska direktutlevereras som separata rader i artikelinförselinstruktionen. Fältet **Direktutleverans information** på varje artikelinförselrad visar om raden innehåller följande:

* Direktutleverans av artiklar.
* Alla artiklar från en inleverans måste lagras.
* En del artiklar från en inleverans måste lagras och en del ska direktutlevereras.

[!INCLUDE [prod_short](includes/prod_short.md)] håller inte separata poster för direktutlevererade artiklar. De registreras som vanliga artikelinförsel instruktioner.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Så här konfigurerar du lagret för direktutleveranser:

1. Ange minst en lagerplats för direktutleverans, om du använder lagerplatser. Om du använder dirigerad artikelinförsel och plockning ställer du in en zon för direktutleverans.  

    En direktutleveranslagerplats har **Direktutlevns lagerplats** fältet markerat och måste ha både **Inleverera** och **Plockning** lagerplatstyper valda. Om du vill lära dig mer om lager platser går du till [skapa lagerplatser](warehouse-how-to-create-individual-bins.md) och [skapar lagerplatstyper](warehouse-how-to-set-up-bin-types.md).  

    Om du använder zoner, skapa en zon för dina direktutleveranslagerställen och välj **Direktutlevns lagerplatszon** fältet. Om du vill ha mer information om zoner går du till [Registrera lagerställen för att använda lagerställen](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Plats** och väljer sedan relaterad länk.  
3. På sidan **Lagerställe** väljer du vilket lagerställe som du vill ställa in direktutleverans för och väljer sedan åtgärden **Redigera**.  
4. På snabbfliken **Distributionslager** på växlingsknappen **Använd direktutleverans** och fyll i fältet **Direktutlev. förfalloberäkning** med tidsperiod att söka efter direktutleveransmöjligheter.

    Alternativet **Använd direktutleverans** är bara tillgängligt om du har markerat fälten **Begär inleveranser**, **Begär utleverans**, **Begär plockning** och **Begär artikelinförsel**.  

5. Om du använder lagerställen fyller du i fältet **Direktutleverans lagerställeskod** på snabbfliken **Lagerställen** med koden för den lagerplats du vill använda som standardlagerplats för direktutleveranser.  
6. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Lagerställeenhet** och väljer sedan relaterad länk.  
7. För varje artikel eller lagerställeenhet som du vill kunna direktutleverera till markerar du artikeln och väljer åtgärden **Redigera**.
8. På sidan **lagerställeenhetskort** markerar du kryssrutan **Använd direktutleverans**.  

> [!NOTE]  
>  Du kan bara använda direktutleveranser om lagerstället är inställt på inleverans- och artikelinförselbearbetning för distributionslagret.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Så här direktutlevererar du artiklar utan att visa möjligheterna:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lager inleveranser** och väljer sedan relaterad länk.  
2. Skapa distributionslagerinleverans för en artikel som har anlänt och som eventuellt kan komma att direktutlevereras. För att lära dig mer om mottagning, gå till [Ta emot artiklar](warehouse-how-receive-items.md).  
3. Fyll i fältet **Ant. att inlevereras** och välj åtgärden **Beräkna direktutleverans**.  

    utgående ursprungsdokument som söker efter de artiklar som inplanerats att lämna lagret inom angiven tidsperiod identifieras. [!INCLUDE[prod_short](includes/prod_short.md)] beräknar antal så att du kan direktutleverera så mycket som möjligt och undvika att införa artiklar, men utan att alltför många artiklar samlas i direktutleveransområdet. Värdet i fältet **Ant. för direktutlevns** utgör således summan av alla utgående rader som begär artikeln inom angiven tidsperiod minus det artikelantal som redan har placerats i området för direktutleveranser, eller så är det värdet i fältet **Ant. att inlevereras** på inleveransraden, beroende på vilket som är lägst. Du kan inte direktutleverera mer än vad som har inlevererats.  

4. Om du vill direktutleverera föreslaget antal bokför du inleveransen. Du kan också välja att ändra antalet till ett högre eller lägre värde och därefter bokföra inleveransen.  

    Det antal som ska direktutlevereras visas nu som rader i artikelinförselinstruktionen, förutsatt att fältet **Använd artikelinförselkalkylark** inte är markerat. Icke direktutlevererade kvantiteter resulterar också i rader i artikelinförselinstruktionen.  

    Om du använder lagerställen har de direktutlevererade artiklarna tilldelats den standardlagerplats för direktutleveranser som angetts på lagerställekortet.  

5. Ta bort raderna **Ta** och **Placera** för artiklar som inte ska direktutlevereras överhuvudtaget.  
6. Skriv ut artikelinförselinstruktionen för återstående rader och placera det antal av inleveransen som ska lagras på lämpliga lagerställen eller i lämpligt lagerområde. Placera artiklarna för direktutleverans i lämpligt område eller lagerplats enligt gällande lagerprincip. Ibland kan det krävas att de bara ska lämnas i inleveransområdet.  
7. Välj åtgärden **Registrera** för att registrera de direktutlevererade artiklarna som införda och tillgängliga för plockning.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Så här direktutlevererar du artiklar när du har visat möjligheterna:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Dist.lager inleveranser** och väljer sedan relaterad länk.  
2. Skapa distributionslagerinleverans för en artikel som har anlänt och som eventuellt kan komma att direktutlevereras.  

    Du vill visa källdokumentrader som kräver artikeln innan du bokför Inleveransen.  
3. Välj åtgärden **Beräkna direktutleverans**.  

   PÅ sidan **Direktutleveransmöjligheter** visas de viktigaste detaljerna om raderna som begär artikeln, t. ex. dokumenttyp, begärt antal och förfallodatum. Med hjälp av den här informationen kan du enklare bestämma hur mycket som ska direktutlevereras, var artiklarna ska placeras i området för direktutleveranser och hur de ska grupperas.  

4. Välj **Autofyll Ant. för direktutlevns** för att visa hur antalen på inleveransraderna har beräknats. När du ändrar antalet artiklar i **Ant. för direktutlevns** på varje rad uppdateras beräkningen. Uppdateringen innebär inte att leverans-eller produktionsordern kommer att få de artiklar som föreslås för direktutleverans. Den är endast avsedd för teständamål. Processen kan emellertid ge viktig information i de fall flera enheter är inbegripna.  
5. För att reservera en kvantitet av artikeln för en orderrad, välj raden och välj sedan åtgärden **reservera**. Sidan **Reservera** reserverar tillgänglig kvantitet av artikeln. Reservationen är som andra reservationer och har ingen högre prioritet för att den skapades med direktutleverans. För att lära dig mer om reserver, gå till [reservera artiklar](inventory-how-to-reserve-items.md).   
6. När du har utfört önskade beräkningar eller reservationer klickar du på knappen **OK** för att infoga den slutgiltiga beräkningen i fältet **Ant. för direktutlevns** på inleveransraden. Alternativt klickar du på knappen **Avbryt** om du vill gå tillbaka till lagerinleveransen för att beräkna direktutleveransen på nytt.  
7. Bokför inleveransen. Bokför nu inleveransen, och du kan fortsätta i artikelinförselinstruktionen enligt beskrivningen i steg 3 till 7 i avsnittet [Så här direktutlevererar du artiklar utan att visa möjligheterna](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > Vid lagerartikelinförseln kan du fortsätta att ändra antalet artiklar som direktutlevereras eller förs in i lager alltefter behov. Till exempel kanske du bestämmer dig för att direktutleverera ytterligare artiklar för att expediera registreringen av direktutleveransen.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Så här visar du direktutlevererade artiklar i utleveranser eller plockningskalkylark

Om du använder lagerplatser, när du öppnar en försändelse eller plockningsarket, uppdateras kvantiteten av varje artikel i lagerplatserna för direktutleveranser. När du ser att artikeln är tillgänglig på lagerstället för direktutleveranser kan du sedan skapa en plockning för artiklarna i utleveransen. I plockningskalkylarket kan du redigera raderna efter behov.  

När en produktionsorder släpps är raderna tillgängliga i plockningskalkylarket och fältet **Ant. på direktutlevns lagerplats** visar om artikeln har anlänt och placerats på lagerställena för direktutleveranser. När du skapar en plockningsinstruktion, [!INCLUDE [prod_short](includes/prod_short.md)] föreslås automatiskt att du först plockar artiklarna för direktutleverans på motsvarande lagerställen. Artiklar i lagerplatser föreslås efteråt.  

Om du inte använder lagerställen måste du komma ihåg att då och då kontrollera området för direktutleveranser eller förlita dig på meddelanden från inleveranser om att artiklar för produktion har anlänt.  

## <a name="see-also"></a>Se även

[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

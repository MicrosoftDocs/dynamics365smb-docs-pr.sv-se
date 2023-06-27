---
title: Flytta artiklar i distributionslager som använder dirigerad artikelinförsel och plockning
description: I den här artikeln beskrivs hur du flyttar artiklar på distributionslager som använder dirigerad artikelinförsel och plockning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# <a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick" />Flytta artiklar i avancerad distributionslagerkonfigurationer med dirigerad plockning och artikelinförsel

Du kanske vill flytta artiklar mellan lagerplatser utan behov från ett källdokument. Du kanske till exempel vill göra det som en del av följande aktiviteter:

* Omorganisera distributionslagret.
* Flytta artiklar till ett kontrollområde.
* Ta ut artiklar från distributionslagrets lagerställen tillfälligt, kanske för att ta som modeller i försäljningspresentationer.
* Flytta extra artiklar till produktionsmodulen för komponenter som har konfigurerats med vissa bokföringsmetoder.
* Flytta producerade eller monterade artiklar från produktions- eller monteringsområde till distributionslager.
* Flytta artiklar från området för masslagring till lagerplatser som du använder för plockning.

Hur du flyttar artiklar beror på hur distributionslagret har ställts in som lagerställe. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).

I distributionslagerkonfiguration där växlingsknappen **Dirigerad art.inf. och plock.** aktiveras för lagerställen kan du registrera oplanerade rörelser på följande sidor:  

* Transportkalkylark
* Interna plockningar för distributionslager
* Interna artikelinförslar för distributionslager
* Lageromgrupperingsjournalen

Sidorna **Transportkalkylark** , **Interna plockningar för distributionslager** och **Interna artikelinförslar för distributionslager** fungerar på samma sätt. Använd sidorna för att förbereda distributionslageraktivitet för lagerpersonalen. Skillnaden beror på de avancerade funktioner som är kopplade till varje sida och de olika typer av lageraktiviteter som troligen utförs av olika anställda:

* Transportkalkylark för att fylla i plocklagerställen med högre rangordning med artiklar från andra lagerplatser
* Artikelinförsel använd mallar för artikelinförsel
* Plockning använder lagerplats rangordning och disposition

## <a name="warehouse-movement-worksheet" />Kalkylark för dist.lager transport

### <a name="to-move-items-with-the-warehouse-movement-worksheet" />Så här flyttar du artiklar med dist.lager transport kalkylarket

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Transportkalkylark** och väljer sedan relaterad länk.  
2. Fyll i fälten på kalkylarket manuellt eller använd någon av följande åtgärder för att automatiskt fylla i raderna:

    * **Hämta lagerställesinnehåll** fyller i kalkylbladets rader med innehållet i den eller de lagerplatser som du anger.
    * **Beräkna lagerplatsåteranskaffning** använder lagerplatserna för att föreslå påfyllning av högrankade lagerplatser från lågrankade lagerplatser.

    > [!NOTE]  
    > Om artikeln uppfyller kriterierna i listan nedan är fälten **från zon** och **från lagerplats** tomma. [!INCLUDE [prod_short](includes/prod_short.md)] beräknar från varifrån artiklarna ska flyttas när du använder åtgärden **Skapa transport**.  
    >  
    > * artikeln har ett utgångsdatum,  
    > * Växlingsknappen **Plocka enligt FEFO** aktiveras för lagerstället.  
    > * Du använder funktionen **Beräkna lagerplatsåteranskaffning**.  

3. Välj åtgärden **Skapa transport** för att skapa förflyttningen. När flytten är färdig kan du registrera den.  

### <a name="to-register-the-warehouse-movement" />Så här registrerar du distributionslagertransporten:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **transport** och väljer sedan relaterad länk.  
2. Öppna transportdokumentet att registrera.  
3. På rader **Plats**, ange var, vilket och när artikeln ska flyttas genom att välja värden i fälten **Zonkod**, **Lagerplatskod**, **Ant. att hantera** eller **Förfallodatum**.  
4. På rader **Ta** i fältet **Ant. att hantera** ange en antal för lagerställesinnehållet som du vill flytta. Du kan endast redigera det här fältet på rader **Ta**. 

    > [!NOTE]
    > Om du måste placera artiklar för en rad på flera lagerställen, t.ex. om den utsedda lagerplatsen är full, använder du funktionen **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.
 
5. Om du vill flytta alla föreslagna antal som anges i fältet **Antal** använder du åtgärden **Fyll i auto. ant. att hantera**.  
6. Välj **Registrera**.  

> [!NOTE]  
> För lagerställen som använder dirigerad artikelinförsel och plockning kan du inte manuellt flytta artiklar på lagerplatser av typen**INLEVERERA** eftersom de ännu inte anses vara tillgängliga lager. Du måste föra in artiklarna på de här lagerplatserna innan de är tillgängliga för transport.

## <a name="internal-pick" />Intern plockning

### <a name="to-create-an-internal-pick" />Skapa en intern plockning

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lager intern plockning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i fälten **Nr.** fältet **Lagerställekod** och fältet **Till lagerplatskod** på snabbfliken **Allmänt**. Fältet **Till lagerställeskod** anger den lagerplats där du vill placera plockade artiklar. För produktion skulle den här lagerstället vara den inkommande produktionslagerstället eller den öppna fabrikslagerstället. För andra typer av aktiviteter väljer du en lagerplatskod för en lagerplatstyp som inte används för plockning, troligtvis en etapplagerplats, leveranslagerplats eller speciallagerplats.  
4. Välj en artikel i fältet **Artikelnr** och fyll i den kvantitet som du vill plocka.  
5. Välj åtgärden **Skapa plockning**. En plockinstruktion är nu klar att utföras av lagerpersonalen. Alternativt kan du välja åtgärden **Frisläppning** och skapa distributionslagerplockningar med hjälp av **Plockförslaget**. Om du vill lära dig mer om plockningsförslag kan du gå till [ Skapa plockningsdokument i bulk med plockningsförslaget](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. När plockningen är färdig kan du registrera den.  

### <a name="to-register-the-warehouse-pick" />Så här registrerar du dist.lager plockning

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **plockningar** och väljer sedan relaterad länk.  

    Om du vill arbeta med en viss plockning väljer du plockningen från listan eller filtrerar listan för att söka efter de plockningar som tilldelats dig.  
2. Om fältet **Tilldelat användar-ID** är tomt, anger du ID för att identifiera själv om det behövs.  
3. Plocka artiklar.  

    Om lagret är distributionslager för att använda riktad borttagning och plockning, används lagerplatsordning för att bestämma lagerplatserna att plocka från. Dessa lagerplatser föreslås på plockningsraderna. Instruktionerna innehåller minst två separata rader för Ta och placera-åtgärder.  

4. När du har utfört plockningen och placerat artiklarna i utleveransområdet eller på lagerstället för utleveranser väljer du åtgärden **Registrera plockning**.  

## <a name="internal-put-away" />Intern artikelinförsel

### <a name="to-create-an-internal-put-away" />Skapa en intern art.införsel

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Dist.lager intern art.införsel** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. Fyll i fälten **Nr.** och fältet **Lagerställekod**.
4. Fyll i en rad för varje artikel som du vill flytta till distributionslagerstället. Fältet **Artikelnr.** och **Antal** måste anges.

    > [!NOTE]  
    > När du väljer artikeln i fältet **Artikelnr.** öppnas sidan **Lagerplatsinnehåll** istället för **Artikel**. Detta beror på att du vill föra in en artikel som finns på en viss lagerplats kommer*lagerplatsinnehåll* – och inte bara en artikel, och du vet redan vilken lagerplats som artikeln ska tas ifrån. Om du har fyllt i fältet **från lagerplatskod** filtreras lagerplatsinnehållet med det värdet.

5. Om du vill fylla raderna med hela lagerplatsinnehållet eller det filtrerade lagerplatsinnehållet från lagerplatser på platsen, väljer du åtgärden **Hämta lagerplatsinnehåll**.  
6. Välj åtgärden **Skapa artikelinförsel**. En artikelinförselinstruktion är nu klar för lagerpersonalen. Alternativt kan du välja åtgärden **Frisläppning** och skapa distributionslagerinförslar med hjälp av sidan **Artikelinförselförslag**. Om du vill lära dig mer om artikelinförselkalkylark kan du gå till [ Skapa artikelinförseldokument i bulk med artikelinförselkalkylark](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. När artikelinförsel är färdig kan du registrera den.  

### <a name="to-register-the-warehouse-put-away" />Fortsätt med att registrera artikelinförsel för distributionslager

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **artikelinförsel** och väljer sedan relaterad länk.
2. Öppna dist.lager artikelinförsel som är klara att hantera.  
3. Om det krävs anger du ditt användar-ID när du börjar arbeta med artikelinförsel.  

    Om du vill optimera artikelinförseln kan du sortera artikelinförselraderna efter olika kriterier. Till exempel per artikel, hyllnummer eller förfallodatum.

    * Om raderna för Ta och Placera för varje inleveransrad inte visas direkt efter varandra och det är så du vill att de ska visas, kan du sortera raderna genom att välja **Artikel** i fältet **Sorteringsmetod**.  
    * Om lagerplatsordning återspeglar lagrets fysiska layout, använd sorteringsmetoden **Lagerplatsordning** för att organisera arbetet med lagerplatser.  

4. Utför artikelinförseln.

    Varje intern inleveransrad har omvandlats till minst två rader i lagerartikelinförseln.  

    * Den första raden, med **Ta** i fältet **Åtgärdstyp**, anger var artiklarna finns i inleveransområdet. Du kan inte ändra zon- och lagerplatsfältet på den här raden.  
    * Nästa rad, med fältet **Plats** i **Åtgärdstyp**, anger var du måste placera artiklarna i distributionslager. Om du har fått ett stort antal artiklar på en enda inleveransrad, kanske artiklarna måste föras in på flera lagerställen, så det finns en Plats rad för varje lagerplats.  

5. När du har placerat alla artiklarna på lagerställen enligt anvisningarna, välj åtgärden **Registrera artikelinförsel**.  

## <a name="to-register-a-movement-that-has-already-happened" />Så här registrerar du en transport som redan har hänt

Om du måste registrera det faktum att artiklar redan har flyttats till andra lagerplatser utan att ha lagt undan, plocka eller flytta, kan du använda **Dist.lagergrupperingsjnl** för att registrera transporten.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Dist.lagergrupperingsjnl** och väljer sedan relaterad länk.  
2. Fyll i fälten **Artikelnr**, **Från zonkod**, **Från lagerställeskod**, **Till zonkod** och **Till lagerställeskod**.  
3. Välj **Registrera**.  

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also" />Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

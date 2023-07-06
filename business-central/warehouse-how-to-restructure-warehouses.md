---
title: Omstrukturera lager
description: Lär dig hur du omstrukturerar distributionslagret med nya lagerplatskoder och nya lagerplatsegenskaper för att uppnå eller upprätthålla en effektivare operation.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9813, 9814'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="restructure-warehouses"></a><a name="restructure-warehouses"></a><a name="restructure-warehouses"></a>Omstrukturera lager
Du kanske vill omstrukturera distributionslagret med nya lagerställeskoder och nya lagerplatsegenskaper. Den typen av aktivitet utförs inte särskilt ofta, men det kan uppstå situationer när en omgruppering är nödvändig för att åstadkomma en effektivare drift. Som exempel:  

- Du kanske vill växla till lagerställeskoder som stöder automatisk datainsamling, exempelvis med handenheter.  
- Distributionslagret kanske har köpt in nya ställningar som ger andra möjligheter att lagra artiklar.  
- Företaget kanske har ändrat sitt artikelsortiment och flyttat distributionslagret till en ny plats för att kunna hantera förändringen.  

Om distributionslagret är inställt på lagerställen, men inte dirigerad artikelinförsel och plockning, strukturera om distributionslagret genom att skapa nya lagerställen du vill använda.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a><a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a><a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a>Om du vill omstrukturera en vanlig dist.lager som använder lagerställen bara
1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2.  På snabbfliken **lager** anger du fältet **Standardlagerplatsval** till **Senaste lagerplats**.  
3.  Flytta allt innehåll på de nuvarande lagerställena till de nya lagerställena som du precis har skapat.  

    1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelgrupperingsjournal** och väljer sedan relaterad länk.  
    2.  Markera en rad och välj sedan åtgärden **Hämta lagerställesinnehåll**.  
    3.  På Snabbfliken **Lagerställesinnehåll** , ställer du in filter i **Lagerställekod**, **Lagerställeskod**, och **Artikelnr** fältet för att ange innehållet som du vill flytta.  
    4.  Välj den **OK** på för att fylla i en journalrad.  
    5.  Markera den lagerplats till vilken artiklarna ska flyttas i fältet **Ny lagerställeskod**.  
    6.  Upprepa steg b till e för allt lagerställesinnehåll som du vill flytta.  
    7.  Välj åtgärden **Bokföra**.  

Du har nu tömt lagerställen där artiklarna användes. Standardlagerställena för artiklarna har nu ändrats till de nya lagerställen.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a><a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a><a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a>Omstrukturera en avancerad lager som använder dirigerad artikelinförsel och plockning

1.  Ska de nya lagerställena som du vill använda i framtiden. Mer information finns i [Skapa lagerställen](warehouse-how-to-create-individual-bins.md).  
2.  Flytta allt innehåll på de nuvarande lagerställena till de nya lagerställena som du precis har skapat.  

    1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Dist.lager grupperingsjnl** och väljer sedan relaterad länk.  
    2.  För de lagerställen där det inte sker någon transport av artiklar skapar du en rad för varje aktuell lagerplats i **Dist.lager omgrupperingsjnl** med den gamla lagerställeskoden, **Från lagerställeskod** och den nya lagerställeskoden, **Till lagerställeskod**.  
    3.  Om vissa transporter innefattar fysiska transporter som du vill att lagerpersonalen ska utföra använder du **Transportkalkylark** för att förbereda transportinstruktioner i stället för att använda lagergrupperingsjournalen. Mer information finns i [Flytta artiklar i avancerade distributionslagerkonfigurationer](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  När de gamla lagerställena är tomma gruppera om dem som **KS** typ av lagerstället, för att se till att de inte inkluderas i artikelflöden.  

    1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
    2.  Markera raden med lagerstället, och välj sedan åtgärden **Lagerställen**.  
    3.  På sidan **Lagerställen** i fältet **Lagerplatstyp kod**, ange **KS** för var och en av de gamla lagerställena som du tömde i steg 3 i föregående process.  

Du har nu tagit bort lagerställena från lagerflödet och har omklassificerat dem, som KS-lagerställen. KS-lagerställen har inte några av aktivitetsfälten på sidan **Lagerplatstyper** valda och därför inte beaktas av objektflödet. Mer information finns i [Skapa lagerställen](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin"></a><a name="to-delete-a-bin"></a><a name="to-delete-a-bin"></a>Så här tar du bort en lagerplats

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2.  Markera lagerstället där du vill ta bort lagerställen väljer du åtgärden **Lagerställen**.  
3.  Markera raderna för de lagerställen som du vill ta bort.  
4.  Välj åtgärden **Radera**.  

Om du klickar på **Ja** tas lagerstället bort för framtida användning, men lagerställeskoden finns kvar i alla distributionslagertransaktioner.  

Om du vill byta namn på en lagerplats så att alla poster som tillhör lagerstället också får det nya namnet kan du göra det på sidan **Lagerställen**, inklusive lagerställesinnehåll, aktivitetsrader för distributionslager, registrerade aktivitetsrader för distributionslager, kalkylarksrader för distributionslager, inleveransrader för distributionslager, bokförda inleveransrader för distributionslager, utleveransrader för distributionslager, bokförda utleveransrader för distributionslager och distributionslagertransaktioner.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a><a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a><a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a>Så här byter du namn på en lagerplats och ändrar lagerställeskoden i alla poster

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2.  Välj lagerstället där du vill byta namn på en lagerplats eller ändra lagerställeskoden och klicka på åtgärden **Lagerställen**.  
3.  I **Kod** fältet, ange lagerstället du vill ändra och ange en ny lagerställeskod.  
4.  Välj **Ja**.  

> [!NOTE]  
>  Om du väljer **ja** , och det finns många transaktioner som rör den här lagerstället, till exempel, eftersom du inte har tagit bort de dokument för en tid, kan det ta en stund byta namn på samtliga transaktioner. Använd batch-jobbet **Ta bort reg. dist.lagerdok.** innan du startar bytanamnprocessen, om du använder den här metoden. Observera också att det enda dokumenten som tas bort i det här batch-jobbet är artikelinförsel, plockning och transport.  
>   
>  Om du byter namn på en inleveranslagerplats eller en leveranslagerplats, alla bokförd inleveranser och utleveranser som gäller för lagerstället, byts namn på.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även
[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

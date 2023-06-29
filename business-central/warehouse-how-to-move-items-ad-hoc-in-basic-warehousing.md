---
title: Flytta artiklar oplanerat i grundläggande lagerkonfigurationer
description: I den här artikeln beskrivs oplanerade interna transporter mellan lagerplatser utan behov från ett källdokument.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# <a name="move-items-internally-in-basic-warehouse-configurations"></a><a name="move-items-internally-in-basic-warehouse-configurations"></a>Flytta artiklar internt i grundläggande distributionslagerkonfigurationer

Du kanske vill flytta artiklar mellan lagerplatser utan behov från ett källdokument. Som en del av följande aktiviteter:

* Omorganisera distributionslagret.
* Flytta artiklar till ett kontrollområde.
* Flytta extra artiklar till och från ett produktionsområde. 

Hur du flyttar artiklar beror på hur distributionslagret har ställts in som lagerställe. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).

I distributionslagerkonfiguration där växlingsknappen **Lagerplats ska finnas** aktiveras men inte **Dirigerad art.inf. och plock.** kan du registrera oplanerade rörelser på följande sidor:  

* Med sidan **Internförflyttning**.
* På sidan **Artikelgrupperingsjournal**.  

## <a name="internal-movements"></a><a name="internal-movements"></a>Internförflyttningar

På sidan **Internförflyttning** kan du ange ta och placera rader när det inte finns något behov från ett källdokument. Sidan Internförflyttning fungerar som ett kalkylblad där du kan organisera saker. Du kan inte hantera den faktiska transporten direkt från den. När en rad fylls i använder du åtgärden **Skapa lagerförflyttning** för att skicka raden till sidan **Lagerförflyttning**, där du bearbetar och registrerar transporten.

### <a name="to-move-items-as-an-internal-movement"></a><a name="to-move-items-as-an-internal-movement"></a>Så här flyttar du artiklar som en internförflyttning

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **internförflyttning** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. Kontrollera att fältet **Nr.** fälten på snabbfliken **Allmänt** fylls i.
3. I **Lagerställekod** fältet, ange det lagerställe där transporten ska utföras.  

    Om lagerstället är din standardplats som distributionslageranvändare, läggs lagerställekod till automatiskt.  
4. I fältet **Till lagerplatskod**, ange en kod för den lagerplats som du vill flytta artikeln till.

    Till exempel för produktionen kan lagerplatsen vara en öppen produktionslagerplats som har definierats på lagerställekortet eller i produktionsgruppen.  
5. I fältet **Förfallodatum**, ange det datum då transporten måste ha slutförts.  
6. På varje rad fyller du i fälten efter behov. Internförflyttningsdokumentet har en rad per transport. Raden innehåller både ta och placera-åtgärderna.
7. Välj fältet **Artikelnr.** för att öppna sidan **Lista för lagerplatsinnehåll**. Välj artikeln att flytta baserat på dess tillgänglighet i papperskorgar. Du kan också välja åtgärden **Hämta lagerställesinnehåll** för att fylla i internförflyttningsrader baserat på dina filter.  

    När du har valt artikel fylls fältet **Från lagerställeskod** i automatiskt enligt det valda lagerplatsinnehållet. Du kan välja vilken lagerplats där artikeln är tillgänglig. Fältet **Artikelnr.** och **Från lagerplatskod** är relaterade. Om du ändrar värdet i ett fält kan värdet i det andra fältet ändras.  

    Fältet **Till lagerställeskod** fylls i med det värde som du angav i huvudet. Du kan ändra den på raden till en annan lagerplatskod som inte är spärrad eller avsedd för särskilda ändamål. Läs mer i [Det dedikerade fältet](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Ange det antal som ska flyttas i **Antal** fältet, när du har definierat de lagerplatser som du vill flytta artikeln till och från.  

    > [!NOTE]  
    > Kvantiteten måste vara tillgänglig på den lager plats som anges i fältet **Från lagerplatskod**.  

9. Är du klar att bearbeta transport, välj åtgärden **Skapa lagerförflyttning**.  

    > [!NOTE]  
    >  När du har skapat transporten, tas rad för internförflyttning bort.  

Du utför resten av oplanerade transporter på sidan **lagerförflyttning**, på samma sätt som du skulle för en transport baserat på källdokument.

### <a name="to-record-the-inventory-movement"></a><a name="to-record-the-inventory-movement"></a>När du vill registrera lagerförflyttning

1.  På sidan **lagerförflyttning** öppnar du dokumentet för att registrera transporten för.  
2. I fältet **Lagerplatskod** på transportraderna, är lagerplatsen där artiklarna måste plockas där det finns tillgängliga artiklar. Du kan ändra lagerplats vid behov.
3. Utför transporten och ange information för den faktiska kvantiteten i fältet **Ant. att hantera**. Värdet för Ta och Placera raderna måste vara samma. Annars kan du inte registrera transporten.

    Om du måste ta artiklar för en rad på flera lagerplatser, t.ex. om hela antalet inte finns på lagerplatsen använder du åtgärden **Dela rad**, på snabbfliken **Rader**. Åtgärden skapar en rad för återstående antal att hantera.  
4. Välj åtgärden **Registrera lagertransport**.  

Följande händer under bokföringsförfarandet:

* Dist.lager transaktioner anger att antalet överförs från lagerplatserna ta till placera.

## <a name="to-move-items-with-the-item-reclassification-journal"></a><a name="to-move-items-with-the-item-reclassification-journal"></a>Så här flyttar du artiklar med artikelgrupperingsjournalen

Istället för att använda transportdokument kan du registrera transport genom att gruppera lagerställeskoder för artiklar. Läs mer på [Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Transporter som bokförts med grupperingsjournaler gör inte transportdokumenten klara att flytta.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artikelgrupperingsjournal** och väljer sedan relaterad länk.  
2. Definiera vilka lagerplatser som du vill flytta artiklar till och från på varje journalrad, genom att fylla i fälten **Lagerställeskod** och **Ny lagerställeskod**.  

    1. Om du vill flytta hela innehållet från en lagerplats till en annan lagerplats väljer du åtgärden **Hämta lagerställesinnehåll**.  
    2. Använd filter för att hitta den lagerplats vars artiklar du vill flytta och klicka på **OK**. Journalraderna fylls i med innehållet av lagerstället.  
3. Fyll i de återstående fälten på varje journalrad.
4. Bokför Grupperingsjournalen  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

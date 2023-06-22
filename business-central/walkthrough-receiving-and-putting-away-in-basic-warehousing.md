---
title: 'Genomgång: Inleverans och utflöde i grundläggande lagerkonfigurationer'
description: Lära dig mer om olika sätt att hantera inkommande processer för inleverans och artikelinförsel.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations" />Genomgång: Inleverera och införa utflöde i grundläggande lagerkonfigurationer

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du ta emot objekt och lägga undan dem med någon av fyra metoder, enligt beskrivningen i följande tabell.

|Metod|inkommande behandling|Begär inleverans|Begär artikelinförsel|Komplexitetsnivå (mer information på [Warehouse Management – översikt](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokföra inleverans och lagerinförsel från orderraden|||Ingen tilldelad distributionslageraktivitet.|  
|B|Bokföra inleverans och lagerinförsel från ett lagerinförseldokument||Aktiverat|Grundläggande: Order för order|  
|A|Bokföra inleverans och lagerinförsel från ett distributionslagerinleveransdokument|Aktiverat||Grundläggande: Konsoliderad inleverans-/utleveransbokföring för flera order.|  
|D|Bokföra inleverans från ett distributionslagerinleveransdokument och bokföra införsel i ett distributionslagerinförseldokument|Aktiverat|Aktiverat|Avancerat|  

Läs mer i [Inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md).

Efterföljande genomgången visar metod B i föregående tabellen.  

## <a name="about-this-walkthrough" />Om den här genomgången

För grundläggande lagerkonfiguration där lagerstället har konfigurerats att kräva artikelinförselbearbetning men inte mottagningsbearbetning, använder du sidan **Lagerinförsel** för att registrera och bokföra artikelinförsel- och mottagningsinformation för dina inkommande källdokument. Följande dokument är inkommande källdokument:

* Inköpsorder
* Försäljningreturorder
* inkommande överföringsorder
* Produktionsorder med utflöde som är redo att föras in

> [!NOTE]
> Även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel**, kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.  

I den här genomgången tas följande aktiviteter upp:  

* Konfigurera lagerstället SILVER för lagerinförsel.  
* Konfigurera lagerstället SILVER för lagerplatshantering.  
* Definiera en standardlagerplats för artikeln LS-81. (LS-75 redan inställd i CRONUS.)  
* Skapa en inköpsorder för leverantör 10000 på 40 högtalare.  
* Kontrollera att införsel-lagerställena förinställs av inställningarna.  
* Släppa inköpsordern för lagerhantering.  
* Skapa en lagerinförsel som baseras på ett släppt källdokument.  
* Kontrollera att införsel-lagerställena hämtas från inköpsorder.  
* Registrera lagerrörelsen till lagret och bokföra inköpsinleveransen för källinköpsorder.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles" />Roller

Följande användarroller utför de uppgifter som denna genomgång visar:  

* Dist.lagerchef  
* Inköpsagent  
* Lagerarbetare  

## <a name="prerequisites" />Förutsättningar

För att kunna utföra den här genomgången behöver du:  

* CRONUS International Ltd. data  
* Att vara distributionslagerarbetare på lagerstället SILVER. Följ dessa steg för att konfigurera dig själv:  

    1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
    2. Välj fältet **Användar-ID** och välj ditt eget användarkonto på sidan **Användare**.  
    3. I fältet **Lagerställekod**, välj **SILVER**.  
    4. Markera kryssrutan **Standard**.  

## <a name="story" />Situation

Alicia, inköpsagenten i CRONUS, skapar en inköpsorder för 10 enheter av artikeln LS-75 och 30 enheter av artikeln LS-81 från leverantör 10000 som ska levereras till distributionslagret SILVER. När leveransen inlevereras till lagret placerar Anders, lagerarbetaren, artiklarna i standardlagerställen som definieras för artiklarna. När Anders bokför artikelinförseln, bokförs artiklarna som inlevererade till lagret och som tillgängligt för försäljning eller andra behov.  

## <a name="setting-up-the-location" />Lägger upp lagerstället

Inställningen av sidan **Lagerställekort** definierar företagets lagerflöden.  

### <a name="to-set-up-the-location" />Så här lägger du upp lagerställen

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2. Öppna lagerställekortet SILVER.  
3. Aktivera växlingsknappen **Kräver artikelinförsel**.  

    Lägga upp en standardlagerplats för de två artikelnumren för att styra var de ska föras in.  

4. Välj åtgärden **Lagerställen**.  
5. Markera den första raden för lagerplatsen **S-01-0001**, och välj sedan åtgärden **innehåll**.  

    Lägg märke till att på sidan **Lagerställesinnehåll** har artikeln **LS-75** redan lagts upp som innehåll i lagerstället S-01-0001.  

6. Välj åtgärden **Ny**.  
7. Markera fälten **Fast** och **Standard**.  
8. I fältet **Verifikationsnr.** anger du **LS-81**.  

## <a name="create-the-purchase-order" />Skapa inköpsordern

Inköpsorder är den vanligaste typen för inkommande källdokumentet.  

### <a name="to-create-the-purchase-order" />Skapa inköpsordern

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Skapa en inköpsorder för leverantör 10000 på arbetsdatumet (23 januari) med följande inköpsorderrader.  

    |Artikel|Lagerställekod|Lagerställeskod|Antal|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SILVER|S-01-0001|10|  
    |LS-81|SILVER|S-01-0001|30|  

    > [!NOTE]  
    > Lagerställeskoden anges automatiskt i överensstämmelse med de inställningar som du har gjort i avsnittet [Konfigurera lagerstället](#setting-up-the-location).  

    Meddela sedan lagret att inköpsordern är klar för lagerhantering när leverans anländer.  

4. Välj åtgärden **Släppa**.  

    Leverans av högtalare från leverantör 10000 har anlänt till SILVERLAGRET, och Anders fortsätter att föra in dem.  

## <a name="receive-and-put-the-items-away" />Ta emot och för in artiklar

På sidan **Lagerinförsel** kan du hantera alla ingående distributionslageraktiviteter för ett särskilt källdokument, t.ex. en inköpsorder.  

### <a name="to-receive-and-put-the-items-away" />Så här tar du emot och för in artiklar

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **lager, artikelinförsel** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Välj fältet **Källdokument** och sedan **Inköpsorder**.  
4. Välj fältet **Källnr.** markera raden för köpet från leverantör 10000 och välj sedan knappen **OK**.  

    Välj alternativt åtgärden **Hämta källdokument** och välj sedan inköpsordern.  

5. Välj åtgärden **Fyll i auto. ant. att hantera**.  

    Alternativt, ange 10 respektive 30 i fältet **Ant. att hantera** på de två lagerinförselraderna.  

6. Välj åtgärden **bokför**, välj åtgärden **inleverera**, och välj sedan **OK**-knappen.  

    De 40 högtalarna har nu registrerats som införda på lagerställen S-01-0001 och en positiv artikeltransaktion skapas som återspeglar den bokförda inköpsinleveransraden.  

## <a name="see-also" />Se även

[Föra in artiklar med lagerartikelinförsel](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Ställa in grundläggande dist.lager med verksamhetsområden](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Plocka för produktion eller montering](warehouse-how-to-pick-for-production.md)  
[Flytta artiklar ad hoc i grundläggande lagerkonfigurationer](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetaljer: inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

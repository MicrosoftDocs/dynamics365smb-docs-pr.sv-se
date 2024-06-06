---
title: Mappa e-dokument mot inköpsorderrader med Copilot
description: Lär dig mer om hur du använder Copilot för att mappa e-dokument till inköpsorderrader.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/10/2024
ms.custom: bap-template
---

# Mappa e-dokument mot inköpsorderrader med Copilot (förhandsversion)

När anskaffningsprocesser blir mer digitala spelar e-dokumentfunktionen i Business Central en nyckelroll för att automatisera mottagning och bearbetning av leverantörsfakturor. Copilot kan hjälpa till i denna process genom att förbättra mappningen och matchningen av leverantörsfakturor till inköpsorder. Detta minskar tidskrävande uppgifter som normalt skulle omfatta omfattande sökning, uppslag och datainmatning. Fördelen förstärks av det faktum att leverantörsfakturor ofta inte överensstämmer exakt med inköpsorder, vilket innebär att Copilot är bättre positionerad att identifiera de motsvarande inköpsorder. Förbättrade matchningsfunktioner gynnar särskilt små och medelstora organisationer som behöver effektiv dokumentspårning för inköpsorderrader. Copilot är den AI-drivna assistenten för arbete som ökar kreativiteten och förbättrar produktiviteten för Business Central-användare.

> [!IMPORTANT]
> - Det här är en funktion för produktionsklar förhandsgranskning för produktionsmiljöer och miljöer i begränsat läge i alla länder, med undantag för Kanada.
> - Produktionsklara förhandsvisningar är föremål för kompletterande användarvillkor. Mer information: [Kompletterande användningsvillkor för förhandsversionen av Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - AI-genererat innehåll kan vara felaktigt.

I den första versionen av appen **e-dokument** introducerade vi grundläggande scenarier för e-dokument för hela försäljningsprocessen. Det finns emellertid ett behov av förbättringar och automatisering vid hanteringen av mottagna dokument, särskilt i samband med inköpsprocesser. Copilot förfinar hur du hanterar e-dokument i inköpsprocessen, särskilt när det gäller inköpsorder. Med ramverket för e-dokument kan du ange vilken typ av inköpsdokument som ska skapas för varje leverantör när du tar emot e-fakturor från dem. Tidigare var det enda alternativet att skapa en inköpsfaktura, antingen som ett dokument eller en redovisningsjournal.

Du kan nu uppdatera en befintlig inköpsorder i Business Central med den information som tas emot i e-fakturan.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->

## Så här aktiverar du Copilot  

Om du inte har aktiverat Copilot för **Matchningshjälp för e-dokument** måste du göra det manuellt. För att aktivera copilot för **Matchningshjälp för e-dokument** följer du stegen nedan: 

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Copilot och AI-funktioner** och väljer sedan relaterad länk. 
2. I listan över funktioner väljer du **Matchningshjälp för e-dokument** och ändrar status till **Aktiv**.  

Du kan börja använda Copilot så snart den är aktiverad. 

## Identifiera inköpsorder

Först kan du identifiera de inköpsorder som du kan matcha automatiskt. Om din **Leverantör** har konfigurerat fältet **Ta emot e-dokument till** så att det fungerar med **Inköpsorder**, när ett elektroniskt dokument har skapats i [!INCLUDE[prod_short](includes/prod_short.md)] (manuellt eller från en extern slutpunkt), [!INCLUDE[prod_short](includes/prod_short.md)] gör du följande:

1. Om **Inköpsorder** för denna leverantör *finns och det finns ett inköpsordernummer* i den mottagna filen **E-dokument** kommer [!INCLUDE[prod_short](includes/prod_short.md)] att koppla detta **E-dokument** automatiskt till den angivna **Inköpsordern**. **Dokumentstatusen** för det här **e-dokumentet** kommer att vara **pågår** och **Status för e-dokument** på undersidan **Servicestatus** kommer att vara **Order kopplad**.  
Den här länken kommer att visas i fältet **Dokument** på det specifika **e-dokumentet**. Om du behöver ändra den länkade **inköpsordern** automatiskt kan du göra det med åtgärden **Uppdatera inköpsorderlänk** och manuellt välja en av befintliga inköpsorder för den här leverantören. Du kan bara göra det innan du matchar raderna mellan **E-dokument** och **Inköpsorder**.  
2. Om **inköpsordern** för just den här leverantören *finns men det inte finns något inköpsordernummer* i den mottagna filen **E-dokument** kan du med [!INCLUDE[prod_short](includes/prod_short.md)] välja en av befintliga inköpsorder om du öppnar listan **Inköpsorder** från de order som du fick från leverantören som endast innehåller **E-dokument** där du måste välja den **Inköpsorder** du vill ha och sedan välja **OK**. Om du inte valde rätt **inköpsorder** eller om du fick **e-dokumentet** automatiskt från en extern slutpunkt med hjälp av **jobbkön** kommer det nya **e-dokumentet** inte att länkas till något inköpsdokument och **dokumentstatusen** kommer att vara **fel** och **e-dokumentstatus** på undersidan **Servicestatus** kommer att vara **Bearbetningsfel för importerat dokument**. När du vill slutföra länkningen till **inköpsordern** väljer du åtgärden **Uppdatera inköpsorderlänk** och väljer en av befintliga inköpsorder för leverantören.  

## Definitionsrader

Copilot hjälper dig att automatiskt matcha e-fakturarader med inköpsorderrader och erbjuder extra matchningsinformation för att förbättra matchningarna.

När de har matchats och mappats uppdaterar [!INCLUDE [prod_short](includes/prod_short.md)] den matchade inköpsordern med relevant inleveransinformation för att säkerställa att rätt antal tas emot på orderraderna.

Du kan matcha dina mottagna elektroniska dokument med inköpsorderrader från två olika ställen, från sidan **E-dokument** eller från sidan **Inköpsorder**. Det enklaste sättet att hitta de redan länkade **inköpsordrarna** är att använda panelen **Länkade inköpsorder** som en del av **e-dokumentaktiviteterna**. Alla icke-länkade dokument kan hittas med hjälp av panelen **Väntar på e-fakturor** där du har en lista med **e-dokument** som du behöver granska.  

> [!NOTE]
> **E-dokumentaktiviteterna** med dessa två paneler finns i följande rollcenter: **Chefsutvärdering**, **Chef**, **Revisor**, **Lagerchef** och **Leverans och inleverans**.

Om du vill köra matchningen från inköpsordern väljer du åtgärden **Mappa e-dokumentrader**, som finns både på inköpsordern och listsidorna för inköpsordern. Men om du vill köra matchning från sidan **E-dokument** väljer du åtgärden **Matcha inköpsorder** på den här sidan. Följ dessa steg för att bearbeta med matchning:

1. Välj åtgärden **Mappa e-dokumentrader** eller **Matcha inköpsorder** för redan länkade dokument.  
2. Du kan se att prompten **Matcha e-dokument mot orderrader med Copilot** fungerar och du har sidan **Matchning av inköpsorder** i bakgrunden. Det betyder att samma process händer men med automatiskt stöd från **Copilot**, som kör matchningsprocessen istället för dig. 
3. Efter några sekunder kommer **Matcha e-dokument mot orderrader med Copilot** att föreslå rader för matchning med ytterligare information: 

    1. I prompthuvudet hittar du följande information: 

    |Fältnamn |Description |
    |--------|-----------------|
    |Automatiskt matchade | Anger antalet matchningar som föreslås automatiskt. Detta är baserat på en strängjämförelse och om det finns 80 % eller mer beskrivningar som överlappar, matchar systemet dessa beskrivningar automatiskt utan att använda GPT-funktioner. |
    |Copilot-matchad | Anger antalet matchningar som föreslås av Copilot med hjälp av både sträng- och semantisk jämförelse. |
    |E-dokumentnummer | Anger det länkade numret för e-dokumentet. |
    |Faktura med totalt belopp exkl. moms | Anger det totala fakturabeloppet, exklusive moms. |
    |Matchat totalt belopp inkl. moms | Anger det matchade beloppet exklusive moms. |
    
    2. Om alla rader är matchade visas den gröna texten i det övre högra hörnet: **Alla rader (100 %) matchas. Granska matchningsförslag**.  
    3. På raderna **Matchat förslag** hittar du följande information:  

    |Fältnamn |Description |
    |--------|-----------------|
    |E-dokumentradnr | Anger radnumret för e-dokumentet (som kommer från den ursprungliga e-dokumentfilen). |
    |Beskrivning av e-dokumentrad | Anger beskrivning av för e-dokumentet (som kommer från den ursprungliga e-dokumentfilen). |
    |Matchad kvantitet | Anger antalet som ska kopplas till inköpsorderraden. |
    |Förslag | Anger den åtgärd som AI föreslår och de föreslagna åtgärderna är relaterade till matchningen av inköpsorderraderna. |

    4. Alla helt föreslagna och matchade linjer är markerade med grön färg. Om det finns något problem, dvs. ett annat pris, men i det tillåtna prisintervallet markeras den här raden som gul färg, och om det finns någon likhet mellan beskrivningsfälten men prisskillnaden är större än tillåten, markeras den här raden som röd färg. 
    5. Om du inte är nöjd med vissa förslag kan du ta bort dem med åtgärden **Ta bort rad**.  
    6. Om du vill se förslagsmatchningar kan du klicka på länken i kolumnen **Förslag** för att öppna sidan **Matchningsdetaljer för e-dokument**. 
    7. På sidan **Matchningsdetaljer för e-dokument** kan du jämföra uppgifter från **e-dokumentet** och **inköpsordern** för att vara säker på den föreslagna matchningen innan du bekräftar den. 
    8. Stäng sidan efter granskningen.   

4. Om du inte är nöjd med de flesta förslagen, eller om du inte vill använda funktionen **Matcha orderrader för e-dokument med Copilot** väljer du **Ignorera** det så kan du fortsätta med den manuella matchningen enligt [manuella matchningen](finance-how-use-edocuments-purchase.md).  
5. Om du vill behålla förslag väljer du knappen **Behåll** så sparas alla förslag från **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] stänger Copilot-prompten och raderna på sidan **Matchning av inköpsorder** markeras som gröna, eftersom de redan är matchade.  
7. Från och med nu kan du fortsätta att arbeta som du gör manuell matchning och det betyder att du kan ta bort matchningar, manuella matchningar, återställa matchning eller om det inte finns några ändringar du vill göra, välj bara åtgärden **Koppla till inköpsorder** och fortsätt arbeta med **inköpsordern**. 

> [!NOTE]
> Om du vill kan du välja åtgärden **Matcha med Copilot** på sidan **Matchning av inköpsorder**, men i så fall blir du tillfrågad om du vill skriva över de befintliga matchningarna, eftersom alla rader redan har matchats.  

> [!NOTE]
> Pris/kostnadsanalys och kontroll av tillgänglig kvantitet är en del av förbearbetningsaktiviteten. 

## Se även

[Översikt över e-dokument](finance-edocuments-overview.md)    
[Använd e-dokument inom försäljning](finance-how-use-edocuments.md)    
[Använd e-dokument vid inköp](finance-how-use-edocuments-purchase.md)   
[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)    
[Ansvarig AI vanliga frågor för bankavstämningshjälp](faqs-bank-reconciliation.md)    

---
title: Använda e-dokument i inköpsprocessen
description: Lär dig hur du använder e-dokumentfunktioner som är relaterade till försäljningsfakturor och order.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 04/03/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-purchases-process"></a>Använda e-dokument i inköpsprocessen

Du kan använda konfigurerade elektroniska dokument (e-dokument) med inköpsdokument.

Du kan använda följande inköpsdokument med funktionen för e-dokument:  

- Inköpsfakturor
- Inköpsorder (från version 24.0)
- Inköpskreditnotor
- Redovisningsjournaler

> [!NOTE]
> Från [!INCLUDE[prod_short](includes/prod_short.md)] version 24.0 är det möjligt att ansluta **inköpsorder** till mottagna **e-dokument**.  

## <a name="e-documents-in-purchases"></a>E-dokument vid köp

Inleveransen av elektroniska inköpsdokument i Dynamics 365 Business Central kan göras som ett batchjobb eller manuellt.  

### <a name="how-to-set-up-vendors-to-work-with-different-purchase-documents"></a>Så här ställer du in leverantörer så att de kan arbeta med olika inköpsdokument

Följ stegen för att konfigurera leverantörer så att de fungerar korrekt med inkommande elektroniska fakturor: 

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk. 
2. Välj den leverantör som du vill konfigurera.   
3. På snabbfliken In the **Mottagande** hittar du fältet **Ta emot e-dokument** för att ange standardinköpsdokumentet som ska genereras från det mottagna e-dokumentet. 

> [!NOTE]
> I fältet **Ta emot e-dokument till** kan användare antingen välja en **inköpsfaktura** eller **inköpsorder** baserat på vad de vill skapa från den mottagna e-fakturan. Detta val påverkar inte skapandet av korrigerande dokument. I båda scenarierna genererar systemet en **kreditnota**.  

> [!NOTE]
> Om användaren väljer alternativet **Inköpsorder** i fältet **Ta emot e-dokument till** kommer systemet försöka uppdatera ett av befintliga inköpsorder, men om inköpsordern för en leverantör i det mottagna **E-dokumentet** inte existerar kommer [!INCLUDE[prod_short](includes/prod_short.md)] att skapa en ny **Inköpsorder**, med samma metod som när den skapar nya **Inköpsfakturor** som beskrivs på den här sidan senare.  

4. Välj ett av alternativen som du vill använda för den valda leverantören. 
5. Stäng sidan.   

### <a name="to-work-with-purchase-invoices"></a>Arbeta med inköpsfakturor

#### <a name="run-the-batch-job"></a>Kör batch-jobbet

> [!NOTE]
> Det här batchjobbet används för automatisk insamling av dina inkommande fakturor. Det kan bara fungera i ett land eller en region där funktionen finns.  

Varje gång som en **jobbkö** väljs att köras och den externa tjänsten har inkommande fakturor som har skickats från din leverantör, samlar systemet in och importerar dessa fakturor. Följ dessa steg för att slutföra processen. 

1. När batch-jobbet har körts visas de nyligen importerade fakturorna på sidan **E-dokument** tillsammans med grundläggande detaljinformation. 
2. Om du vill visa mer information öppnar du ett särskilt e-dokument.   
3. Om det inte fanns några fel eller problem i e-dokumentet mappar fältet **Post** dokumentnumret på inköpsfakturan om detta är konfigurerat på sidan **Leverantörskort** (systemet skapade automatiskt). Välj länken för att öppna dokumentet.
 
> [!NOTE]
> Det här systemskapade dokumentet är inte det bokförda dokumentet. 

1. Om du vill gå direkt till inköpsdokumentet markerar du fältet **Post**. När du har öppnat sidan **Inköpsfaktura** kontrollerar du dokumentet. Sedan, om allt är korrekt, bokför dokumentet.  
1. När du bokför inköpsdokumentet uppdateras fältet **Post** i **e-dokumentet** från **Faktura** till **Inköpsfaktura** och numret på det bokförda inköpsdokumentet är tillgängligt. Du kan välja numret för att öppna den bokförda inköpsfakturan. 

Detaljer om loggar är desamma som i försäljningsprocessen för e-dokument.  

Eftersom fel i försäljningsprocessen oftast beror på tjänstens tillgänglighet kan det inkommande dokumentet ha flera orsaker. Den vanligaste orsaken till ett fel är att systemet inte kan känna igen raderna på e-dokumentet som du har fått från leverantören. Därför kan den inte ange rader på inköpsfakturan. 

Det finns två vanliga fel:  

- Om du vill använda den här specifika raden från leverantörsfakturan som bokfördes direkt på redovisningskontot måste du ha konfigurerat värdet **Mappningstext** korrekt. För att kringgå det här felet om du vill använda huvudkonton, välj **Mappa text till konto** för att skapa en specifik mappningsvärde **Mappningstext** med värde **Debetkontonr.** som du vill använda. 
- Om du vill spåra inventeringen och använda rader från din leverantörsfaktura för att fylla i artiklar på dina dokumentrader, måste du ha konfigurerat korrekt **Artikelreferensnummer.** värde. Om du vill kringgå det här felet mappar du den externa artikeln med dina artikelnummer med hjälp av artikelreferenslistan. Mer information finns i [Använd artikelreferenser](inventory-how-use-item-cross-refs.md). 

När du har åtgärdat felen och varningarna kan du manuellt ange när systemet ska skapa en inköpsfaktura baserat på dina inställningar genom att välja **Skapa dokument**.   

#### <a name="manually-import-invoices"></a>Manuellt importera fakturor

Så här importerar du externa e-dokument manuellt:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **E-dokumenttjänst** och väljer sedan relaterad länk. 
2. På sidan **E-dokumenttjänst** väljer du den aktiva tjänsten.   
3. Välj **Inleverera** och överför e-dokumentfilen som du fick från leverantören. 
4. Om ett felmeddelande visas öppnar du e-dokumentet för att åtgärda problemet. 
5. När du har åtgärdat problem, i **Importera manuellt**, välj **Skapa dokument**.  
6. När dokumentet har skapats i [!INCLUDE[prod_short](includes/prod_short.md)] ändras inte sättet du visar det på när du använder ett batch-jobb. 

### <a name="e-documents-with-purchase-orders"></a>E-dokument med inköpsorder

#### <a name="to-link-purchase-orders-with-the-received-e-documents"></a>För att koppla inköpsorder med mottagna e-dokument

Om din **Leverantör** har konfigurerat fältet **Ta emot e-dokument till** så att det fungerar med **Inköpsorder**, när ett elektroniskt dokument har skapats i [!INCLUDE[prod_short](includes/prod_short.md)] (manuellt eller från en extern slutpunkt), [!INCLUDE[prod_short](includes/prod_short.md)] gör du följande:  

1. Om **inköpsordern** för just den här leverantören finns och det finns ett inköpsordernummer i den mottagna filen **E-dokument** kommer [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt länka detta **E-dokument** till den nämnda **inköpsordern** och **dokumentstatus** för detta **E-dokument** kommer att vara **Pågående** och **E-dokumentstatus** på undersidan **Servicestatus** kommer att vara **Ordern länkad**. Den här länken kommer att visas i fältet **Dokument** på det specifika **e-dokumentet**. Om du behöver ändra den länkade **inköpsordern** automatiskt kan du göra det med åtgärden **Uppdatera inköpsorderlänk** och manuellt välja en av befintliga inköpsorder för den här leverantören. Du kan bara göra det innan du matchar raderna mellan **E-dokument** och **Inköpsorder**.  
2. Om **inköpsordern** för just den här leverantören finns men det inte finns något inköpsordernummer i den mottagna filen **E-dokument** kommer [!INCLUDE[prod_short](includes/prod_short.md)] kommer att erbjuda möjligheter att välja en av befintliga inköpsorder när och om du laddade upp detta dokument manuellt, öppna listan **Inköpsorder** endast för leverantören i **E-dokument**, där du måste välja den **inköpsorder** du vill ha och välja **OK**. Om du inte valde rätt **inköpsorder** eller om du fick **e-dokumentet** automatiskt från en extern slutpunkt med hjälp av **jobbkön** kommer det nya **e-dokumentet** inte att länkas till något inköpsdokument och **dokumentstatusen** kommer att vara **fel** och **e-dokumentstatus** på undersidan **Servicestatus** kommer att vara **Bearbetningsfel för importerat dokument**. När du vill slutföra länkningen till **inköpsordern** väljer du åtgärden **Uppdatera inköpsorderlänk** och väljer en av befintliga inköpsorder för leverantören. 
3. Om **inköpsordern** för den här leverantören inte finns när ett nytt **e-dokument** skapas kommer [!INCLUDE[prod_short](includes/prod_short.md)] att skapa en ny **inköpsorder** med hjälp av samma modell för skapande som redan finns för nya **inköpsfakturor**. **Dokumentstatusen** för det här **e-dokumentet** kommer att vara **behandlad** och **Status för e-dokument** på undersidan **Servicestatus** kommer att vara **Importerat dokument har skapats**. Den här länken kommer att visas i fältet **Dokument** på det specifika **e-dokumentet**.   

#### <a name="matching-lines-from-received-e-document-with-purchase-order"></a>Matcha rader från mottaget e-dokument med inköpsorder

Du kan matcha dina mottagna elektroniska dokument med inköpsorderrader från två olika ställen, från sidan **E-dokument** eller från sidan **Inköpsorder**. Det enklaste sättet att hitta de redan länkade **inköpsordrarna** är att använda panelen **Länkade inköpsorder** som en del av **e-dokumentaktiviteterna**. Alla icke-länkade dokument kan hittas med hjälp av panelen **Väntar på e-fakturor** där du har en lista med **e-dokument** som du behöver granska.  

> [!NOTE]
> **E-dokumentaktiviteterna** med dessa två paneler finns i följande **Rollcenter**: Chefsutvärdering, Chef, Revisor, Lagerchef och Leverans och inleverans.  

> [!NOTE]
> Om momsprocenten skiljer sig mellan det inkommande dokumentet och företagets momsprocent kan matchande dokument inte användas i miljöer med flera länder.  

##### <a name="matching-lines-from-purchase-order"></a>Matcha rader från inköpsorder

Du kan matcha raderna från listan **Inköpsorder** eller från en av de öppnade **inköpsorderna**. För att börja med detta använder du följande steg:  

1. Välj panelen **Länkade inköpsorder** i rollcentret om det finns något nummer. 
2. Eftersom det finns två alternativ för matchning, välj ett av dem: 

    1. Om du vill matcha raderna i listan **Inköpsorder** markerar du raden **Inköpsorder** som du vill matcha och väljer åtgärden **Mappa e-dokumentrader**.  
    2. Om du först vill öppna **inköpsordern** öppnar du dokumentet och väljer sedan åtgärden **Mappa e-dokumentrader**. 

3. Eftersom båda alternativen har samma process öppnar du sidan **Matchning av inköpsorder** med följande innehåll: 

    1. I sidhuvudet hittar du följande information, som kan hjälpa dig att mappa raderna lättare: 

    |Fältnamn |Description |
    |--------|-----------------|
    |Leverantörsnamn |Anger leverantörsnamnet på det elektroniska dokumentet. |
    |E-dokumentnummer |Anger numret på det länkade elektroniska dokumentet. |
    |Datum för e-dokument |Anger datumet för det länkade elektroniska dokumentet.  |
    |E-dokumentbelopp |Anger det länkade e-dokumentets totala belopp inklusive moms. |

    2. På raderna hittar du de rader som importerats från filen **E-dokument** till vänster och raderna från den befintliga **inköpsordern** till höger.  
    3. Alla rader på båda sidor har artikelnummer och beskrivningar, tillsammans med **Inköpspris** och **Radrabatt %**.  
    4. På sidan **Importerade rader** kan du också leta reda på fältet **Antal** som ett totalt antal från e-fakturan och fältet **Matchat antal** som anger det antal som redan matchat inköpsorderraderna. 
    5. På sidan **Inköpsorderrader** kan du också hitta **Disponibelt antal** som det antal som kan matchas med den här raden (mottaget, men inte fakturerat antal) och **Ant. att fakturera**, med det antal som redan matchar den här raden. 
    6. Om du vill matcha rader markerar du raderna på båda sidor som du vill matcha och väljer åtgärden **Matcha manuellt**. De matchade raderna markeras med den gröna färgen. 
    7. Det är möjligt att matcha en till en, men det är också möjligt att matcha många till en eller en till många, välja fler rader på en eller annan sida innan du väljer åtgärden **Matcha manuellt**. 
    8. Du kan också välja åtgärden **Matcha automatiskt** om du automatiskt vill matcha alla rader med samma **typ**, **nr**, **enhetspris**, **rabatt och **måttenhet**. 
    9. Om du gör ett misstag kan du välja åtgärden **Ta bort matchning** om du vill ta bort de matchade raderna på inköpsordersidan eller välja åtgärden **Återställ matchning** om du vill återställa allt som matchar. 
    10. Om ditt **e-dokument** innehåller många rader kan du under matchningsprocessen välja åtgärden **Visa väntande rader** för att ta bort alla e-dokumentrader om de redan är helt matchade. Om du behöver visa alla rader kan du alltid välja åtgärden **Visa alla rader**. 

4. När du är klar med matchningen måste du välja åtgärden **Koppla till inköpsorder**.   
5. När du har kopplat matchningen till **inköpsordern** [!INCLUDE[prod_short](includes/prod_short.md)]  uppdateras följande fält:

    1. **Leverantörsfakturanr.** och **Dokumentdatum** i dokumenthuvudet uppdateras med värden från det elektroniska dokument som du har tagit emot och länkat. 
    2. **Antal att fakturera** på rader uppdateras med värdena från kolumnen **Ant. att fakturera** på sidan **Inköpsordermatchning** baserat på vilken matchning du gjorde. 
    3. Nu kan du bokföra dokumentet genom att välja åtgärden **Bokför**.  
    4. När du har bokfört dokumentet ändras värdet i fältet **Dokument** på sidan **E-dokument** och det relateras till den **bokförda inköpsfakturan**. 
    5. Stäng sidan.  

> [!IMPORTANT]
> Som standard kan du bara matcha rader som har samma totalbelopp i båda dokumenten. Det betyder att den **Enhetspris senaste inköp** tillsammans med den tillämpade **radrabatten %** måste vara densamma, eftersom du i ett dokument kan ha ett belopp utan rabatt och i ett annat med rabatt.  

Om du vill lägga till lite tolerans och tillåta skillnaden mellan rader i **E-faktura** och **Inköpsorder** följer du stegen:   

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inköpsinställningar** och väljer sedan relaterad länk.  
2. Du vill tillåta tolerans i fältet **Matchningsdifferens i % för e-dokument**, ange den högsta tillåtna procentandelen av kostnadsskillnaden vid matchning av inkommande rad för **E-dokument** med raden **Inköpsorder**. 
3. Den här inställningen gäller för alla matchande rader, men återigen beaktas toleransen för det totala beloppet, som för **Enhetspris senaste inköp** tillsammans med tillämpad **radrabatt %**.  
4. Stäng sidan.   

##### <a name="to-match-lines-from-e-document"></a>Så här matchar du rader från e-dokument

Du kan matcha raderna på sidan **E-dokument**. För att börja med detta använder du följande steg:  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **E-dokument** och väljer sedan relaterad länk. 
2. Välj de **E-dokument** som du vill matcha.   
3. Välj åtgärden **Matcha inköpsorder** för att öppna sidan **Matchning av inköpsorder**.  
4. Upprepa samma steg som du använde när du började matcha från inköpsorder.

### <a name="e-document-matching-assistance-copilot"></a>Copilot för matchningshjälp för e-dokument

> [!NOTE]
> För närvarande har copilot **Matchningshjälp för e-dokument** statusen Produktionsklar förhandsversion och är tillgänglig globalt utom i Kanada. Men det fungerar bara på engelska. 

> [!NOTE]
> Copilot är en AI-driven assistent som hjälper användare i hela organisationen att arbeta kreativt och automatisera rutinmässiga uppgifter. Copilot för **Matchningshjälp för e-dokument** hjälper användare att enkelt matcha sina mottagna elektroniska fakturor med befintliga inköpsorderrader, med hjälp av LLM-modellen för att matcha rader mellan två olika dokument. 

#### <a name="to-activate-the-copilot"></a>Så här aktiverar du copilot

Om du inte har aktiverat copilot för **Matchningshjälp för e-dokument** måste du göra det manuellt. För att aktivera copilot för **Matchningshjälp för e-dokument** följer du stegen nedan: 

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Copilot och AI-funktioner** och väljer sedan relaterad länk. 
2. I listan över funktioner väljer du **Matchningshjälp för e-dokument** och ändrar status till **Aktiv**.  

När Copilot är aktiverad kan du börja använda den.

#### <a name="use-the-e-document-matching-assistance-copilot"></a>Använd copilot för matchningshjälp för e-dokument

Om Copilot är aktiverad kommer befintliga åtgärder **Mappa e-dokumentrader** på inköpsorder och **Matcha inköpsorder** på sidan **E-dokument** kommer att få olika ikoner, som symboliserar AI-funktionen. Du kan köra dessa åtgärder (precis som i tidigare exempel i listan över inköpsorder), från en av **inköpsorderna** eller från **E-dokument**. Alla steg för körning är desamma, men när du kör den här åtgärden blir resultatet annorlunda och du måste följa stegen:  

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

    4. Alla helt föreslagna och matchade linjer är markerade med grön färg. Om det finns något problem, dvs. ett annat pris, men i det tillåtna prisintervallet markeras den här raden som gul, och om det finns någon likhet mellan beskrivningsfälten men prisskillnaden är större än tillåten, markeras den här raden som röd. 
    5. Om du inte är nöjd med vissa förslag kan du ta bort dem med åtgärden **Ta bort rad**.  
    6. Om du vill se förslagsmatchningar kan du klicka på länken i kolumnen **Förslag** för att öppna sidan **Matchningsdetaljer för e-dokument**. 
    7. På sidan **Matchningsdetaljer för e-dokument** kan du jämföra uppgifter från **e-dokumentet** och **inköpsordern** för att vara säker på den föreslagna matchningen innan du bekräftar den. 
    8. Stäng sidan efter granskningen.   

4. Om du inte är nöjd med de flesta förslagen, eller om du inte vill använda funktionen **Matcha orderrader för e-dokument med Copilot**, väljer du **Ignorera** det så kan du fortsätta med den manuella matchningen enligt beskrivningen ovan.  
5. Om du vill behålla förslag väljer du knappen **Behåll** så sparas alla förslag från **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] stänger Copilot-prompten och raderna på sidan **Matchning av inköpsorder** markeras som gröna, eftersom de redan är matchade.  
7. Från och med nu kan du fortsätta att arbeta som du gör manuell matchning och det betyder att du kan ta bort matchningar, manuella matchningar, återställa matchning eller om det inte finns några ändringar du vill göra, välj bara åtgärden **Koppla till inköpsorder** och fortsätt arbeta med **inköpsordern**. 

> [!NOTE]
> Om du vill kan du välja åtgärden **Matcha med Copilot** på sidan **Matchning av inköpsorder**, men i så fall blir du tillfrågad om du vill skriva över de befintliga matchningarna, eftersom alla rader redan har matchats.  

> [!NOTE]
> Pris/kostnadsanalys och kontroll av tillgänglig kvantitet är en del av förbearbetningsaktiviteten.   

## <a name="overview-of-e-document-statuses"></a>Översikt över status för e-dokument

Om du vill få en bättre överblick över alla e-dokument i företaget kan du välja det rollcenter för **Revisor** där det finns e-dokumentstatus. Där kan du hitta e-dokumentaktiviteter som har följande status:

- **Inkommande e-dokument:**

    - Bearbetade
    - Pågår
    - Fel


## <a name="see-also"></a>Se även

[Hur man ställer in e-dokument i [!INCLUDE[prod_short](includes/prod_short.md)]](finance-how-setup-edocuments.md)    
[Så här använder du e-dokument i försäljningsprocessen](finance-how-use-edocuments.md)   
[Hur man utökar e-dokument i [!INCLUDE[prod_short](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Ekonomihantering](finance.md)    
[Fakturaförsäljning](sales-how-invoice-sales.md)    
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]


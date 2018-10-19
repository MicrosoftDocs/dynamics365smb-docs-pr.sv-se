---
title: "Behandla försäljningsreturer eller annulleringar | Microsoft Docs"
description: "Beskriver hur du skapar en kreditnota direkt eller genom en försäljningsreturorder om du vill bearbeta en retur, annullering eller ersättning för artiklar eller tjänster som du har blivit mottagen betalning för."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0945ffb9a8eb9482883d5c524b0d7f7eea46b5b2
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="process-sales-returns-or-cancellations"></a>Behandla försäljningsreturer eller annulleringar
Om en kund vill returnera artiklar eller få återbetalning för artiklar eller tjänster du har sålt och få betalning för detta, måste du skapa och bokföra en försäljningskreditnota som anger begärd ändring. Du kan skapa försäljningskreditnotan direkt från den bokförda försäljningsfakturan med rätt fakturainformation, eller skapa en ny försäljningskreditnota med kopierad fakturainformation.

Om du behöver mer kontroll över försäljningsreturprocessen, till exempel distributionslagerdokument för artikelhantering eller bättre överblick när du tar emot artiklar från flera försäljningsdokument med en försäljningsretur, kan du skapa försäljningsreturorder. En försäljningsreturorder utför automatiskt den relaterade försäljningskreditnotan och andra returrelaterade dokument, till exempel en ersättningsförsäljningsorder, om detta behövs. Mer information finns i avsnittet ”Att skapa en försäljningsreturorder baserat på minst ett bokfört försäljningsdokument”.

> [!NOTE]  
>   Om en bokförd försäljningsfaktura ännu inte har betalts, kan du använda funktionen **Korrigera** eller **Avbryt** på den bokförda försäljningsfakturan för att återföra transaktioner. Dessa funktioner fungerar bara för obetalda fakturor, och de har inte stöd delleveranser returer eller annulleringar. Mer information finns i [Så här kan du korrigera eller annullera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md).

En retur eller en återbetalning kan relatera till endast några av artiklarna eller tjänsterna på den ursprungliga försäljningsfakturan. I så fall måste du redigera information på raderna i försäljningskreditnotan eller försäljningsreturorden. När du bokför försäljningskreditnotan eller försäljningsreturorden, kan försäljningsdokumenten, som påverkas av ändringen återföras, och en återbetalning skapas för kunden. Mer information finns i [Gör betalningar](payables-make-payments.md).  

Förutom den ursprungliga bokförda försäljningsfakturan kan du koppla försäljningskreditnotan eller försäljningsreturorden till andra försäljningsdokument, t.ex en annan bokförd försäljningfaktura, eftersom kunden också returnerar artiklarna som har levererats med den fakturan.

Du kan skicka den bokförda försäljningskreditnotan till kunden för att bekräfta returen eller avbryt och att meddela att det relaterade värdet ska ersättas, till exempel när artiklar returneras.

Bokföringen av kreditnota återställer även eventuella kostnader som har tilldelats det bokförda dokumentet så att artikelns värdetransaktioner är samma som innan artikelkostnaden har tilldelats.

## <a name="inventory-costing"></a>Lagerkostnad
Om du vill behålla rätt lagervärdering vill du vanligtvis föra tillbaka de returnerade artiklarna i lagret till den styckkostnad som de såldes för, inte till deras aktuella styckkostnad. I programmet kallas detta för exakt kostnadsåterföring.

Två funktioner finns för att fördela exakt kostnadsåterföring automatiskt.   

|Funktion|Beskrivning|  
|------------------|---------------------------------------|  
|Funktionen **Hämta bokförda dokumentrader som ska återföras** i fönstret **Försäljningsreturorder**|Kopiera rader för en eller flera bokförda dokument som ska återföras till försäljningsreturorden. Mer information finns i avsnittet ”Att skapa en försäljningsreturorder och relaterad försäljningskreditnota på minst en bokförd försäljningsfaktura”.|  
|Funktionen **Kopiera dokument** i fönstret **Försäljningskreditnota** och **Försäljningsreturorder**|Kopierar både huvudet och raderna av ett bokfört dokument som ska återföras.<br /><br /> Kräver att kryssrutan **exakt kostnadsåterföring** är markerad i fönstret **Försäljningsinställningar**.|

För att tilldela exakt kostnadsåterföring manuellt, måste du välja fältet **Koppla från artikellöpnr** på alla typer av rader för returdokument och välj sedan numret på den ursprungliga försäljningstransaktionen. Då länkas försäljningskreditnota till den ursprungliga försäljningstransaktionen och säkerställs att artikeln värderas till ursprunglig styckkostnad.

Mer information finns i [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Skapa en ny försäljningskreditnota från en bokförd försäljningsfaktura.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförd försäljningsfakturor** och välj sedan relaterad länk.  
2. I fältet **Bokförda försäljningsfakturor** väljer du den bokförda försäljningsfakturan som du vill återföra och väljer sedan åtgärden **Skapa korrigerande kreditnota**.

    Försäljningskreditnotans huvud innehåller information från den bokförda försäljningsfakturan. Du kan redigera detta, till exempel med ny information som behövs för returavtalet.  
3. Redigera information på raderna enligt avtalet, till exempel antal artiklar som har returnerats, eller beloppet som ska ersättas.
4. Välj åtgärden **Koppla transaktioner**.
5. I fönstret **Koppla kundtrans.** markerar du raden med det bokförda försäljningsdokumentet som du vill koppla försäljningskreditnota till, och väljer sedan åtgärden **Koppla till ID**.

    Identifieraren för försäljningskreditnotan visas i fältet **Koppla till ID**.
6. I fältet **Belopp att koppla** anger du det belopp som du vill koppla om det är mindre än det ursprungliga beloppet.  

    Längst ned i fönstret **Koppla kundtrans.** kan du se det totala beloppet för att koppla för att återföra alla berörda transaktioner, nämligen när värdet i fältet **Saldo** är noll.
7. Välj **OK**. När du bokför försäljningskreditnotan kopplas den till de bokförda säljdokumenten.

    När du har skapat eller redigerat de försäljningskreditnotarader som krävs och ett eller flera program anges, kan du bokföra försäljningskreditnotan.   
8. Välj åtgärden **Bokför och skicka.**.  

Dialogrutan **Bekräftelse för bokför och utskick** öppnas och visar kundens önskad utskicksmetod. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).  

De bokförda försäljningsdokumenten som du vill koppla kreditnotan till återförs nu, och en betalningsåterbetalning kan skapas för kunden. Försäljningskreditnotan tas bort och ersätts med ett nytt dokument i listan över bokförda försäljningskreditnotor.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Skapa en ny försäljningskreditnota genom att kopiera en bokförd försäljningsfaktura.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningskreditnotor** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** för att öppna en ny tom försäljningskreditnota.
3. Ange namnet på en befintlig kund i fältet **Kund**.
4. Välj åtgärden **kopiera dokument**.
5. I fönstret **Kopiera försäljningsdokument** i fältet **Dokumenttyp** väljer du **Bokförd faktura**.
6. Välj fältet **Dokumentnr** för att öppna fönstret **Bokförda försäljningsfakturor** och välj den bokförda försäljningsfakturan som innehåller rader som du vill återföra.
7. Markera kryssrutan **Beräkna om rader** om du vill att de kopierade bokförda försäljningsfakturaraderna ska uppdateras med ändringar av artikelpris och styckkostnad sedan fakturan bokfördes.
8. Välj **OK**. De kopierade fakturaraderna infogas i säljkreditnotan.
9. Slutför försäljningskreditnotan enligt vad som förklaras i avsnittet "Att skapa en försäljningskreditnota från en bokförd försäljningsfaktura" i det här ämnet.

## <a name="to-create-a-sales-return-order-based-on-one-or-more-a-posted-sales-documents"></a>Att skapa en försäljningsreturorder baserat på minst ett bokfört försäljningsdokument.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsreturorder** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
4. På snabbfliken **rader** fyller du i raderna manuellt eller kopierar information från andra dokument för att fylla i raderna automatiskt:

    - Du kan använda funktionen **Hämta bokförda dokumentrader som ska återföras** för att kopiera en eller flera bokförda dokumentrader från ett eller flera bokförda dokument. Den här funktionen återför alltid de exakta kostnaderna från den bokförda dokumentraden. Funktionen beskrivs i följande steg.    
    - Du kan använda funktionen **Kopiera dokument** för att kopiera ett befintligt dokument till returordern. Använd den här funktionen för att kopiera hela dokumentet. Det kan antingen röra sig om ett bokfört dokument eller ett dokument som inte har bokförts ännu. Du kan bara aktivera exakt kostnadsåterföring när kryssrutan **Kräv exakt kost.återföring** är markerad i fönstren **Försäljningsinställningar**.  

5. Välj åtgärden **Hämta bokförda dokumentrader som ska återföras**.
6. Högst upp i fönstret **Bokförda försäljningsdokumentrader** markerar du kryssrutan **Visa endast rader som kan återföras** om du bara vill visa rader med antal som ännu inte har returnerats. Exempel: om antalet på en bokförd försäljningsfaktura redan har returnerats kanske du inte vill returnera antalet i ett nytt försäljningsreturdokument.

    > [!NOTE]  
    >  Det här fältet fungerar endast för bokförda utleveranser och bokförda fakturarader, inte för bokförda retur- eller kreditnoterader.

    Till vänster i fönstret visas olika dokumenttyper, och siffran inom parentes visar hur många tillgängliga dokument det finns av respektive dokumenttyp.

7. Välj i fältet **Dokumenttypfilter** vilken typ av bokförda dokumentrader som du vill använda.  
8. Markera de rader som du vill kopiera till det nya dokumentet.  

    > [!NOTE]  
    >  Om du använder Ctrl+A för att markera alla rader kopieras alla rader inom det filter som du har angett, men filtret **Visa endast rader som kan återföras** ignoreras. Exempel: Du har filtrerat raderna efter ett angivet dokumentnummer med två rader, där den ena raden redan har returnerats. Även om fältet **Visa endast rader som kan återföras** markerats kopieras båda raderna om du trycker på Ctrl+A för att kopiera alla rader, i stället för bara den rad som inte har återförts.  

9. Klicka på **OK** om du vill kopiera raderna till det nya dokumentet.  

    Följande processer inträffar:  

    -   För bokförda dokumentrader av typen **Artikel** skapas en ny dokumentrad som är en kopia av den bokförda dokumentraden, med det antal som ännu inte har återförts. Fältet **Koppla från artikellöpnr** fylls i efter behov med numret på artikeltransaktionen för den bokförda dokumentraden.  

    -   För bokförda dokumentrader som inte är av typen **Artikel**, t.ex. artikelomkostnader, skapas en ny dokumentrad som är en kopia av den ursprungliga bokförda dokumentraden.  

    -   Fältet **Styckkostnad (BVA)** på den nya raden beräknas utifrån kostnaderna på motsvarande artikeltransaktioner.  

    -   Om det kopierade dokumentet är en bokförd utleverans, inleverans, returinleverans eller returutleverans beräknas à-priset automatiskt från artikelkortet.  

    -   Om det kopierade dokumentet är en bokförd faktura eller kreditnota kopieras à-priset, fakturarabatterna och radrabatterna från den bokförda dokumentraden.  

    -   Om den bokförda dokumentraden innehåller artikelspårningsrader fylls fältet **Koppla från artikellöpnr** på artikelspårningsraderna i automatiskt med de tillämpliga artikeltransaktionsnumren från de bokförda artikelspårningsraderna.  

     När du kopierar från en bokförd faktura eller kreditnota kopieras eventuella fakturarabatter och radrabatter, som var giltiga vid den tidpunkt då dokumentet bokfördes, från den bokförda dokumentraden till den nya dokumentraden. Observera dock att om alternativet **Beräkna fakturarabatt** är aktiverat i fönstret **Försäljningsinställningar** beräknas fakturarabatten på nytt när du bokför den nya dokumentraden. Det kan därför hända att radbeloppet för den nya raden inte är detsamma som radbeloppet för den bokförda dokumentraden, beroende på den nya beräkningen av fakturarabatten.  

     > [!NOTE]  
     >  Om en del av antalet på den bokförda dokumentraden redan har återförts, sålts eller förbrukats skapas en rad bara för det antal som finns kvar i lager eller som inte har returnerats. Om hela antalet på den bokförda dokumentraden har återförts skapas ingen ny dokumentrad.  
     >   
     >  Om varuflödet i det bokförda dokumentet är detsamma som i det nya dokumentet skapas en kopia av den ursprungliga bokförda dokumentraden i det nya dokumentet. Fältet **koppla-från artikellöpnr** fylls inte i eftersom exakt kostnadsåterföring inte är möjligt i det här fallet. T.ex. om du använder funktionen **Hämta bokförda dokumentrader som ska återföras** för att hämta en bokförd försäljningskreditnotarad för en ny försäljningskreditnota kopieras endast den ursprungliga bokförda kreditnotaraden till den nya kreditnotan.  

10. I fönstret **Förs.returorder** i fältet **Returorsakskod** för varje rad väljer du orsaken till returen.
11. Välj åtgärden **Bokföra**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Så här skapar du en ersättningsförsäljningsorder från en försäljningsreturorder
Du kan behöva gottgöra kunden för någon försåld artikel genom att den ersätts med en annan. Artikeln kan ersättas med en likadan eller någon annan. Den här situationen kan exempelvis uppstå om fel artikel av misstag har levererats till kunden.  

1. I fönstret **Förs.returorder** för en aktiv returprocess på en tom rad skapar du en negativ transaktion för ersättningsartikeln genom att ange ett negativt belopp i fältet **Antal**.  
2. Välj åtgärden **Flytta negativa rader**.
3. I fönstret **Flytta negativa förs.rader** fyller du i fälten efter behov.
4. Välj knappen **OK**. Den negativa raden för ersättningsartikeln bort från försäljningsreturordern och infogas i ett nytt fönster **Försäljningsorder**. Mer information finns i [Sälja produkter](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Så här skapar du returrelaterade dokument från en försäljningsreturorder
Du kan skapa ersättningsförsäljningsorder, inköpsreturorder och ersättningsförsäljningsorder automatiskt under försäljningsreturprocessen. Detta är användbart i situationer där du vill hantera artiklar med garantier från leverantörer.

1. I fönstret **Förs.returorder** för en aktiv returprocess, väljer du åtgärden **Skapa returrelaterade dokument**.
2. I fältet **Leverantörsnr** anger du numret på en leverantör om du vill skapa leverantörsdokument automatiskt.
3. Om en returnerad artikel måste returneras till leverantören markerar du kryssrutan **Skapa inköpsreturorder**.
4. Om returnerad en artikel måste beställas från leverantören markerar du kryssrutan **Skapa inköpsorder**.
5. Om du måste skapa en ersättningsförsäljningsorder markerar du kryssrutan **Skapa förs.order**.

## <a name="to-create-a-restock-charge"></a>Så här skapar du en återlagringsavgift
Du kan behöva debitera kunder återlagringsavgift för att täcka hanteringskostnader för retur av någon artikel. Det kan till exempel inträffa om någon kund av misstag beställt fel artikel eller ändrat sig när artikeln tagits emot.

Du kan bokföra den ökade kostnaden som en artikelomkostnad i en kreditnota eller en returorder och koppla den till den bokförda leveransen. Följande tabell beskriver en försäljningsreturorder, men samma steg gäller för en försäljningskreditnota.

1. Öppna fönstret **Förs.returorder** för en aktiv returprocess.
2. På en ny rad , i fältet **Typ** väljer du **Omkostnad (artikel)**.  
3. Fyll i fälten för varje artikelomkostnadsrad. För mer information, se [Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md)  

När du bokför försäljningsreturordern läggs återlagringsavgiften till det aktuella försäljningstransaktionsbeloppet. På det här sättet kan du hålla lagervärderingen aktuell.  

## <a name="to-create-a-sales-allowance"></a>Så här skapar du ett förs. tillägg
Du kan skicka en kreditnota med ett prisavdrag till en kund om de varor som levererats till kunden är skadade eller om artiklarna inte levererades i tid.  
Du kan bokföra det reducerade priset som en artikelomkostnad i en kreditnota eller en returorder och koppla den till den bokförda leveransen. Följande tabell beskriver en försäljningskreditnota, men samma steg gäller för en försäljningsreturorder.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningskreditnotor** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** för att öppna en ny tom försäljningskreditnota.
3. Fyll i kreditnotahuvudet med information om den kund som ska erhålla förs.tillägget.  
4. På snabbfliken **Rader** i fältet **Typ** markerar du **Debitering (artikel)**.  
5.  I fältet **Nr.** markerar du lämpligt värde för artikelomkostnaden.  
     Om du vill kan du skapa ett särskilt artikelomkostnadsnummer för förs.tillägg.  
6.  Ange **1** i fältet **Antal**.  
7.  Ange förs.tilläggets belopp i fältet **A-pris**.  
8.  Koppla prisavdraget som en artikelomkostnad till artiklarna i den bokförda leveransen. För mer information, se [Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md) När du har kopplat prisavdraget går du tillbaka till **Försäljningskreditnota**.  

När du bokför försäljningsreturordern läggs förs.tillägget till det aktuella försäljningstransaktionsbeloppet. På det här sättet kan du hålla lagervärderingen aktuell.

## <a name="to-combine-return-receipts"></a>Så här kombinerar du returinleveranser
Du kan kombinera returinleveranser om kunden returnerar flera artiklar som finns på olika försäljningsreturorder.  

När artiklarna tas emot i lagret bokför du aktuella förs.returorder som mottagna. Bokförda returinleveranser upprättas.  

När du är klar att fakturera kunden kan du, i stället för att fakturera varje förs.returorder separat, skapa en försäljningskreditnota och automatiskt kopiera de bokförda returinleveransraderna till detta dokument. Därefter kan du bokföra försäljningskreditnotan och på vanligt sätt fakturera alla öppna förs.returorder omgående.  

Om du vill kombinera inleveranser måste kryssrutan **Samlingsfakturering** markeras i fönstret **Kundkort**.  

### <a name="to-manually-combine-return-receipts"></a>Så här kombinerar du returinleveranser manuellt  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningskreditnota** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.  
4. Välj åtgärden **Hämta returinleveransrader**.  
5. Markera de returinleveransrader som ska ingå på kreditnotan:  

    -   Markera alla rader och klicka på **OK** om du vill infoga alla rader.  

    -   Markera raderna i fråga och klicka på **OK** om du vill infoga särskilda rader.  

6.  Om du har markerat fel leveransrad eller om du vill börja om kan du ta bort raderna på kreditnotan och köra funktionen **Hämta returinleveransrader** på nytt.  
7.  Bokföra fakturan  

### <a name="to-automatically-combine-return-receipts"></a>Så här kombinerar du returinleveranser automatiskt  
Du kan ange att returinleveranser ska kombineras automatiskt och dessutom välja att bokföra kreditnotor automatiskt med hjälp av funktionen **Samlingsreturnering**.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Samlingsreturnering** och välj sedan relaterad länk.
2. I fönstret **Samlingsreturnering** fyller du i fälten för att välja relevanta returinleveranser.
3. Markera kryssrutan **Bokför kreditnotor**. I annat fall måste du manuellt bokföra de resulterande inköpskreditnotorna.
4.  Välj knappen **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Så här tar du bort en inlevererad och fakturerad returorder  
När du fakturerar returinleveranser på det här sättet finns de returorder som returinleveranserna bokfördes från kvar, även om de har tagits emot och fakturerats i sin helhet.  

När returinleveranser har kombinerats på en kreditnota och bokförts, skapas en bokförd försäljningskreditnota för de krediterade raderna. Innehållet i fältet **Fakturerat antal** på den ursprungliga förs.returordern uppdateras utifrån det fakturerade antalet.   
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort fakturerade försäljningsreturorder** och välj sedan relaterad länk.  
2.  Fälten **Serienr** . vilka returorder som ska tas bort.  
3.  Välj **OK**.  

Du kan också ta bort enskilda försäljningsreturorder manuellt.   

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


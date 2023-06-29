---
title: Behandla försäljningsreturer eller annulleringar
description: 'Beskriver hur du skapar en kreditnota om du vill bearbeta en retur, annullering eller ersättning för artiklar eller tjänster som du har blivit mottagen betalning för.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: edupont
---
# <a name="process-sales-returns-or-cancellations"></a><a name="process-sales-returns-or-cancellations"></a>Behandla försäljningsreturer eller annulleringar

Om en kund vill returnera artiklar eller få återbetalning för artiklar eller tjänster du har sålt och få betalning för detta, måste du skapa och bokföra en försäljningskreditnota som anger begärd ändring. Om du vill inkludera rätt fakturainformation kan du göra följande:  

- Skapa en försäljningskreditnota direkt från en bokförd försäljningsfaktura.
- Skapa en ny försäljningskreditnota med kopierad fakturainformation.

Om du behöver mer kontroll över försäljningsreturprocessen, till exempel distributionslagerdokument för artikelhantering eller bättre överblick när du tar emot artiklar från flera försäljningsdokument med en försäljningsretur, kan du skapa försäljningsreturorder. En försäljningsreturorder utför automatiskt den relaterade försäljningskreditnotan och andra returrelaterade dokument, till exempel en ersättningsförsäljningsorder, om detta behövs. Mer information finns i [Bearbeta försäljningsreturorder](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Om en bokförd försäljningsfaktura ännu inte har betalts, kan du använda funktionen **Korrigera** eller **Avbryt** på den bokförda försäljningsfakturan för att återföra transaktioner. Dessa funktioner fungerar bara för obetalda fakturor, och de har inte stöd delleveranser returer eller annulleringar. Mer information finns i [Så här kan du korrigera eller annullera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md).

En retur eller en återbetalning kan relatera till endast några av artiklarna eller tjänsterna på den ursprungliga försäljningsfakturan. I så fall måste du redigera information på raderna i försäljningskreditnotan eller försäljningsreturorden. När du bokför försäljningskreditnotan eller försäljningsreturorden, kan försäljningsdokumenten, som påverkas av ändringen återföras, och en återbetalning skapas för kunden. Mer information finns i [Gör betalningar](payables-make-payments.md).  

Bokföringen av kreditnota återställer även eventuella kostnader som har tilldelats det bokförda dokumentet så att artikelns värdetransaktioner är samma som innan artikelkostnaden har tilldelats.

> [!NOTE]
> De bokföringsaspekter som gäller för försäljningsreturer, till exempel betalningar till kunder som återbetalning, betraktas som bokföringsarbete och beskrivs inte här. Mer information finns i [Hantera leverantörsskulder](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Skapa en ny försäljningskreditnota från en bokförd försäljningsfaktura.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokförda försäljningsfakturor** och väljer sedan relaterad länk.  
2. På sidan **Bokförda försäljningsfakturor** väljer du den bokförda försäljningsfakturan som du vill återföra och väljer åtgärden **Avbryt** och åtgärden **Skapa korrigerande kreditnota**.

    Försäljningskreditnotans huvud innehåller information från den bokförda försäljningsfakturan. Du kan redigera detta, till exempel med ny information som behövs för returavtalet.  
3. Redigera information på raderna enligt avtalet, till exempel antal artiklar som har returnerats, eller beloppet som ska ersättas.
4. Välj åtgärden **Förbereda** och välj sedan åtgärden **Koppla transaktioner**.
5. På sidan **Koppla kundtrans.** markerar du raden med det bokförda försäljningsdokumentet som du vill koppla försäljningskreditnota till, och väljer sedan åtgärden **Koppla till ID**.

    Identifieraren för försäljningskreditnotan visas i fältet **Koppla till ID**.
6. I fältet **Belopp att koppla** anger du det belopp som du vill koppla om det är mindre än det ursprungliga beloppet.  

    Längst ned på sidan **Koppla kundtrans.** kan du se det totala beloppet för att koppla för att återföra alla berörda transaktioner, nämligen när värdet i fältet **Saldo** är noll.
7. Välj **OK**. När du bokför försäljningskreditnotan kopplas den till de bokförda säljdokumenten.

    När du har skapat eller redigerat de försäljningskreditnotarader som krävs och ett eller flera program anges, kan du bokföra försäljningskreditnotan.  
8. Välj åtgärden **bokföra** och välj sedan åtgärden **Bokför och skicka**.  

Dialogrutan **Bekräftelse för bokför och utskick** öppnas och visar kundens önskad utskicksmetod. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).  

De bokförda försäljningsdokumenten som du vill koppla kreditnotan till återförs nu, och en betalningsåterbetalning kan skapas för kunden. Försäljningskreditnotan tas bort och ersätts med ett nytt dokument i listan över bokförda försäljningskreditnotor.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a><a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Skapa en ny försäljningskreditnota genom att kopiera en bokförd försäljningsfaktura.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningskreditnotor** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** för att öppna en ny tom försäljningskreditnota.
3. Ange namnet på en befintlig kund i fältet **Kundnamn**.
4. Välj åtgärden **Förbereda** och välj sedan åtgärden **kopiera dokument**.
5. På sidan **Kopiera försäljningsdokument** i fältet **Dokumenttyp** väljer du **Bokförd faktura**.
6. Välj fältet **Dokumentnr** för att öppna sidan **Bokförda försäljningsfakturor** och välj den bokförda försäljningsfakturans post som innehåller rader som du vill återföra.
7. Markera kryssrutan **Beräkna om rader** om du vill att de kopierade bokförda försäljningsfakturaraderna ska uppdateras med ändringar av artikelpris och styckkostnad sedan fakturan bokfördes.
8. Välj **OK**. De kopierade fakturaraderna infogas i säljkreditnotan.
9. Slutför försäljningskreditnotan enligt vad som förklaras i [Att skapa en försäljningskreditnota från en bokförd försäljningsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-allowance"></a><a name="to-create-a-sales-allowance"></a>Så här skapar du ett förs. tillägg
Du kan skicka en kreditnota med ett prisavdrag till en kund om de varor som levererats till kunden är skadade eller om artiklarna inte levererades i tid.  
Du kan bokföra det reducerade priset som en artikelomkostnad i en kreditnota eller en returorder och koppla den till den bokförda leveransen. Följande tabell beskriver en försäljningskreditnota, men samma steg gäller för en försäljningsreturorder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningskreditnotor** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny** för att öppna en ny tom försäljningskreditnota.
3. Fyll i kreditnotahuvudet med information om den kund som ska erhålla förs.tillägget.  
4. På snabbfliken **Rader** i fältet **Typ** markerar du **Debitering (artikel)**.  
5. I fältet **Nr.** markerar du lämpligt värde för artikelomkostnaden.  
     Om du vill kan du skapa ett särskilt artikelomkostnadsnummer för förs.tillägg.  
6. Ange **1** i fältet **Antal**.  
7. Ange förs.tilläggets belopp i fältet **Enhetspris exkl. moms**.  
8. Koppla prisavdraget som en artikelomkostnad till artiklarna i den bokförda leveransen. För mer information, se [Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md) När du har kopplat prisavdraget går du tillbaka till sidan **Försäljningskreditnota**.  

När du bokför försäljningsreturordern läggs förs.tillägget till det aktuella försäljningstransaktionsbeloppet. På det här sättet kan du hålla lagervärderingen aktuell.

## <a name="to-combine-return-receipts"></a><a name="to-combine-return-receipts"></a>Så här kombinerar du returinleveranser
Du kan kombinera returinleveranser om kunden returnerar flera artiklar som finns på olika försäljningsreturorder.  

När artiklarna tas emot i lagret bokför du aktuella förs.returorder som mottagna. Bokförda returinleveranser upprättas.  

När du är klar att fakturera kunden kan du, i stället för att fakturera varje förs.returorder separat, skapa en försäljningskreditnota och automatiskt kopiera de bokförda returinleveransraderna till detta dokument. Därefter kan du bokföra försäljningskreditnotan och på vanligt sätt fakturera alla öppna förs.returorder omgående.  

Om du vill kombinera inleveranser måste kryssrutan **Samlingsfakturering** markeras på sidan **Kundkort**.  

### <a name="to-manually-combine-return-receipts"></a><a name="to-manually-combine-return-receipts"></a>Så här kombinerar du returinleveranser manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **försäljningskreditnotor** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.  
4. Välj åtgärden **Hämta returinleveransrader**.  
5. Markera de returinleveransrader som ska ingå på kreditnotan:  

    - Markera alla rader och klicka på **OK** om du vill infoga alla rader.  

    - Markera raderna i fråga och klicka på **OK** om du vill infoga särskilda rader.  
6.  Om du har markerat fel leveransrad eller om du vill börja om kan du ta bort raderna på kreditnotan och köra funktionen **Hämta returinleveransrader** på nytt.  
7.  Bokföra fakturan  

### <a name="to-automatically-combine-return-receipts"></a><a name="to-automatically-combine-return-receipts"></a>Så här kombinerar du returinleveranser automatiskt

Du kan ange att returinleveranser ska kombineras automatiskt och dessutom välja att bokföra kreditnotor automatiskt med hjälp av funktionen **Samlingsreturnering**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Samlingsreturnering** och väljer sedan relaterad länk.
2. På sidan **Samlingsreturnering** fyller du i fälten för att välja relevanta returinleveranser.
3. Markera kryssrutan **Bokför kreditnotor**. I annat fall måste du manuellt bokföra de resulterande inköpskreditnotorna.
4. Välj knappen **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a><a name="to-remove-a-received-and-invoiced-return-order"></a>Så här tar du bort en inlevererad och fakturerad returorder

När du fakturerar returinleveranser på det här sättet finns de returorder som returinleveranserna bokfördes från kvar, även om de har tagits emot och fakturerats i sin helhet.  

När returinleveranser har kombinerats på en kreditnota och bokförts, skapas en bokförd försäljningskreditnota för de krediterade raderna. Innehållet i fältet **Fakturerat antal** på den ursprungliga förs.returordern uppdateras utifrån det fakturerade antalet.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Ta bort fakturerade försäljningsreturorder** och väljer sedan relaterad länk.  
2. Fälten **Serienr** . vilka returorder som ska tas bort.  
3. Välj **OK**.  

Du kan också ta bort enskilda försäljningsreturorder manuellt.  

## <a name="inventory-costing"></a><a name="inventory-costing"></a>Lagerkostnad

Om du vill behålla rätt lagervärdering vill du vanligtvis föra tillbaka de returnerade artiklarna i lagret till den styckkostnad som de såldes för, inte till deras aktuella styckkostnad. I programmet kallas detta för exakt kostnadsåterföring.

Två funktioner finns för att fördela exakt kostnadsåterföring automatiskt:  

|Funktion|Beskrivning|  
|------------------|---------------------------------------|  
|Funktionen **Hämta bokförda dokumentrader som ska återföras** på sidan **Försäljningsreturorder**|Kopiera rader för en eller flera bokförda dokument som ska återföras till försäljningsreturorden. Mer information finns i avsnittet [Skapa en försäljningsreturorder baserat på minst ett bokfört försäljningsdokument](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Funktionen **Kopiera dokument** på sidan **Försäljningskreditnota** och **Försäljningsreturorder**|Kopierar både huvudet och raderna av ett bokfört dokument som ska återföras.<br /><br /> Kräver att kryssrutan **exakt kostnadsåterföring** är markerad på sidan **Försäljningsinställningar**.|

För att tilldela exakt kostnadsåterföring manuellt, måste du välja fältet **Koppla från artikellöpnr** på alla typer av rader för returdokument och välj sedan numret på den ursprungliga försäljningstransaktionen. Då länkas försäljningskreditnota till den ursprungliga försäljningstransaktionen och säkerställs att artikeln värderas till ursprunglig styckkostnad.

Mer information finns i [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Behandla inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

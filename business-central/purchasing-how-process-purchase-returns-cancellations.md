---
title: Behandla returer eller annulleringar | Microsoft Docs
description: Förklarar hur du skapar och bokför en inköpskreditnota när du returnerar artiklar till en leverantör eller avbryter köpta tjänster.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: fc2a3a372ac82ce936418f793cdd33eb3b0ea4b9
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193992"
---
# <a name="process-purchase-returns-or-cancellations"></a>Behandla inköpsreturer eller annulleringar
Om du vill returnera artiklar till leverantören eller annullera tjänster som du har köpt, kan du skapa och bokföra en inköpskreditnota som anger begärd ändring med hänsyn till den ursprungliga inköpfakturan. Du kan skapa inköpskreditnotan direkt från den bokförda inköpsfakturan med rätt fakturainformation, eller skapa en ny inköpskreditnota med kopierad fakturainformation.

Om du behöver mer kontroll över inköpsreturprocessen, till exempel distributionslagerdokument för artikelhantering eller bättre överblick när du returnerar artiklar från flera inköpsdokument med en inköpsretur, kan du skapa inköpsreturorder. En inköpsreturordern utfärdar automatiskt relaterad inköpskreditnota. Mer information finns i avsnittet [Att skapa en inköpsreturorder baserat på minst ett bokfört inköpsdokument](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
>   Om en bokförd inköpsfaktura ännu inte har betalts, kan du använda funktionen **Korrigera** eller **Avbryt** på den bokförda inköpsfakturan för att automatiskt återföra relevanta transaktioner. Dessa funktioner fungerar bara för obetalda fakturor, och de har inte stöd delleveranser returer eller annulleringar. Mer information finns i [Korrigera eller annullera obetalda inköpssfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Vanligtvis skapar du en inköpskreditnota eller inköpsreturorder som reaktion på en kreditnota som skickas till dig av en leverantör. Funktionerna för inköpskreditnotan eller i inköpsreturordern som din interna dokumentation för processen för kreditnota för bokföring eller för att styra leverans av relaterade artiklar.

Ändring kan vara kopplad till alla produkter på den ursprungliga inköpfakturan eller bara till vissa av produkterna. Därmed kan du delvis returnera mottagna artiklar eller begära delvis återbetalning av mottagna tjänster. I så fall måste du redigera information på inköpskreditnotan eller inköpsreturorden.

Förutom den ursprungliga bokförda inköpsfakturan kan du koppla inköpskreditnotan eller inköpsreturordern till andra inköpsdokument, t.ex en annan bokförd inköpsfaktura, eftersom du också returnerar artiklarna som har levererats med den fakturan.

Bokföringen av kreditnota återställer även eventuella kostnader som har tilldelats det bokförda dokumentet så att artikelns värdetransaktioner är samma som innan artikelkostnaden har tilldelats.

## <a name="inventory-costing"></a>Lagerkostnad
Om du vill behålla rätt lagervärdering vill du vanligtvis plocka returartiklar från lagret till den styckkostnad som de köptes för, inte till deras aktuella styckkostnad. I programmet kallas detta för exakt kostnadsåterföring.

Två funktioner finns för att fördela exakt kostnadsåterföring automatiskt.  

|Funktion|Description|  
|------------------|---------------------------------------|  
|Funktionen **Hämta bokförda dokumentrader som ska återföras** på sidan **Inköpsreturorder**|Kopiera rader för en eller flera bokförda dokument som ska återföras till inköpsreturorden. Mer information finns i avsnittet [Att skapa en inköpsreturorder baserat på minst ett bokfört inköpsdokument](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|Funktionen **Kopiera från dokument** på sidorna **Inköpskreditnota** och **Inköpsreturorder**|Kopierar både huvudet och raderna av ett bokfört dokument som ska återföras.<br /><br /> Kräver att kryssrutan **exakt kostnadsåterföring** är markerad på sidan **Inköpsinställningar**.|

För att tilldela exakt kostnadsåterföring manuellt, måste du välja fältet **Koppla från artikellöpnr** på alla typer av rader för returdokument och välj sedan numret på den ursprungliga inköpstransaktionen. Då länkas inköpskreditnota eller inköpsreturorder till den ursprungliga inköpstransaktionen och säkerställs att artikeln värderas till ursprunglig styckkostnad.

Mer information finns i [Designdetaljer: Lagerkostnad](design-details-inventory-costing.md)

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Skapa en ny inköpskreditnota från en bokförd inköpsfaktura.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda inköpsfakturor** och välj sedan relaterad länk.  
2. På sidan **Bokförda inköpsfakturor** väljer du den bokförda inköpsfakturan som du vill återföra och väljer sedan åtgärden **Skapa korrigerande kreditnota**.

    De flesta fält på inköpskreditnotans huvud fylls i med informationen från den bokförda inköpsfakturan. Du kan redigera alla fält, till exempel med ny information som behövs för returavtalet.
3. Redigera information på raderna enligt avtalet, till exempel antal artiklar som har returnerats, eller beloppet som ska ersättas.
4. Välj åtgärden **Koppla transaktioner**.
5. På sidan **Koppla leverantörstrans.** markerar du raden med det bokförda inköpsdokumentet som du vill koppla inköpskreditnota till, och väljer sedan åtgärden **Koppla till ID**. Numret på inköpskreditnotan infogas i fältet **Koppla till ID**.
6. I fältet **Belopp att koppla** anger du det belopp som du vill koppla om det är mindre än det ursprungliga beloppet.

    Längst ned på sidan **Koppla leverantörstrans.** kan du se det totala beloppet för att koppla för att återföra alla berörda transaktioner, nämligen när värdet i fältet **Saldo** är noll.
7. Välj **OK**. När du bokför inköpskreditnotan kopplas den till de angivna bokförda inköpsdokumenten.

    När du har skapat eller redigerat de inköpskreditnotarader som krävs och ett eller flera program anges, kan du fortsätta att bokföra inköpskreditnotan.
8. Välj åtgärden **Bokföra**.

De bokförda inköpsfakturorna som du koppla kreditnotan till återförs nu. Om du redan har betalt den ursprungliga fakturan ska leverantören nu återbetala betalningen till dig. Om kreditnotan endast är för en del av produkten på den ursprungliga fakturan, kan du endast betala återstående belopp på den ursprungliga inköpsfakturan för att stänga den.

Inköpskreditnotan tas bort och ersätts med ett nytt dokument i listan över bokförda inköpskreditnotor.

## <a name="to-create-a-purchase-credit-memo-by-copying-a-posted-purchase-invoice"></a>Skapa en ny inköpskreditnota genom att kopiera en bokförd inköpsfaktura.
1. Välj ![glödlampeikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpskreditnota** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** för att öppna en ny tom inköpskreditnota.
3. Ange namnet på en befintlig leverantör i fältet **Leverantör**.
4. Välj åtgärden **Kopiera från dokument**.
5. På sidan **Kopiera inköpsdokument** i fältet **Dokumenttyp** väljer du **Bokförd faktura**.
6. Välj fältet **Dokumentnr** för att öppna sidan **Bokförda inköpsfakturor** och välj den bokförda inköpsfakturan som innehåller rader som du vill återföra.
7. Markera kryssrutan **Beräkna om rader** om du vill att de kopierade bokförda inköpsfakturaraderna ska uppdateras med ändringar av artikelpris och styckkostnad sedan fakturan bokfördes.
8. Välj **OK**. De kopierade fakturaraderna infogas i inköpskreditnotan.
9. Slutför inköpskreditnotan enligt vad som förklaras i [Att skapa en inköpskreditnota från en bokförd inköpsfaktura](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

## <a name="to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents"></a>Att skapa en inköpsreturorder baserat på minst ett bokfört inköpsdokument.
1. Välj ![glödlampeikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsreturordrar** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
4. På snabbfliken **rader** fyller du i raderna manuellt eller kopierar information från andra dokument för att fylla i raderna automatiskt:

    - Du kan använda funktionen **Hämta bokförda dokumentrader som ska återföras** för att kopiera en eller flera bokförda dokumentrader från ett eller flera bokförda dokument. Den här funktionen återför alltid de exakta kostnaderna från den bokförda dokumentraden. Funktionen beskrivs i följande steg.    
    - Du kan använda funktionen **Kopiera från dokument** för att kopiera ett befintligt dokument till returordern. Använd den här funktionen för att kopiera hela dokumentet. Det kan antingen röra sig om ett bokfört dokument eller ett dokument som inte har bokförts ännu. Du kan bara aktivera exakt kostnadsåterföring när kryssrutan **Kräv exakt kost.återföring** är markerad på sidan **Försäljningsinställningar**.  

4. Välj åtgärden **Hämta bokförda dokumentrader som ska återföras**.
5. Högst upp på sidan **Bokförda inköpsdokumentrader** markerar du kryssrutan **Visa endast rader som kan återföras** om du bara vill visa rader med antal som ännu inte har returnerats. Exempel: om antalet på en bokförd inköpsfaktura redan har returnerats kanske du inte vill inkludera antalet i ett nytt inköpsreturdokument.

    > [!NOTE]  
    >  Det här fältet fungerar endast för bokförda inleveranser och bokförda fakturarader, inte för bokförda retur- eller kreditnoterader.  

    Till vänster på sidan visas olika dokumenttyper, och siffran inom hakparentes visar hur många tillgängliga dokument det finns av respektive dokumenttyp.

6. Välj i fältet **Dokumenttypfilter** vilken typ av bokförda dokumentrader som du vill använda.  
7. Markera de rader som du vill kopiera till det nya dokumentet.  

    > [!NOTE]  
    >  Om du använder Ctrl+A för att markera alla rader kopieras alla rader inom det filter som du har angett, men filtret **Visa endast rader som kan återföras** ignoreras. Exempel: Du har filtrerat raderna efter ett angivet dokumentnummer med två rader, där den ena raden redan har returnerats. Även om fältet **Visa endast rader som kan återföras** markerats kopieras båda raderna om du trycker på Ctrl+A för att kopiera alla rader, i stället för bara den rad som inte har återförts.  

8. Klicka på **OK** om du vill kopiera raderna till det nya dokumentet.  

    Följande processer inträffar:  

    -   För bokförda dokumentrader av typen **Artikel** skapas en ny dokumentrad som är en kopia av den bokförda dokumentraden, med det antal som ännu inte har återförts. Fältet **Koppla till artikellöpnr** fylls i efter behov med numret på artikeltransaktionen för den bokförda dokumentraden.  

    -   För bokförda dokumentrader som inte är av typen **Artikel**, t.ex. artikelomkostnader, skapas en ny dokumentrad som är en kopia av den ursprungliga bokförda dokumentraden.  

    -   Fältet **Styckkostnad (BVA)** på den nya raden beräknas utifrån kostnaderna på motsvarande artikeltransaktioner.  

    -   Om det kopierade dokumentet är en bokförd utleverans, inleverans, returinleverans eller returutleverans beräknas à-priset automatiskt från artikelkortet.  

    -   Om det kopierade dokumentet är en bokförd faktura eller kreditnota kopieras à-priset, fakturarabatterna och radrabatterna från den bokförda dokumentraden.  

    -   Om den bokförda dokumentraden innehåller artikelspårningsrader fylls fältet **Koppla till artikellöpnr** på artikelspårningsraderna i automatiskt med de tillämpliga artikeltransaktionsnumren från de bokförda artikelspårningsraderna.  

     När du kopierar från en bokförd faktura eller kreditnota kopieras eventuella fakturarabatter och radrabatter, som var giltiga vid den tidpunkt då dokumentet bokfördes, från den bokförda dokumentraden till den nya dokumentraden. Observera dock att om alternativet **Beräkna fakturarabatt** är aktiverat på sidan **Inköpsinställningar** beräknas fakturarabatten på nytt när du bokför den nya dokumentraden. Det kan därför hända att radbeloppet för den nya raden inte är detsamma som radbeloppet för den bokförda dokumentraden, beroende på den nya beräkningen av fakturarabatten.  

    > [!NOTE]  
    >  Om en del av antalet på den bokförda dokumentraden redan har återförts, sålts eller förbrukats skapas en rad bara för det antal som finns kvar i lager eller som inte har returnerats. Om hela antalet på den bokförda dokumentraden har återförts skapas ingen ny dokumentrad.  
    >   
    >  Om varuflödet i det bokförda dokumentet är detsamma som i det nya dokumentet skapas en kopia av den ursprungliga bokförda dokumentraden i det nya dokumentet. Fältet **koppla-från artikellöpnr** fylls inte i eftersom exakt kostnadsåterföring inte är möjligt i det här fallet. T.ex. om du använder funktionen **Hämta bokförda dokumentrader som ska återföras** för att hämta en bokförd inköpskreditnotarad för en ny inköpskreditnota kopieras endast den ursprungliga bokförda kreditnotaraden till den nya kreditnotan.  

8. På sidan **Inköpsreturorder** i fältet **Returorsakskod** för varje rad väljer du orsaken till returen.
9. Välj åtgärden **Bokföra**.

## <a name="to-create-a-replacement-purchase-order-from-a-purchase-return-order"></a>Skapa en ersättningsinköpsorder från en inköpsreturorder
Du kan komma överens med leverantören om att de ska kompensera dig för en inköpt artikel genom att ersätta den. Ersättningsartikeln kan vara likadan eller annorlunda. Detta kan inträffa om leverantören av misstag har skickat fel artikel.  
1.  På sidan **Inköpsreturorder** för en aktiv returprocess på en tom rad skapar du en negativ transaktion för ersättningsartikeln genom att ange ett negativt belopp i fältet **Antal**.  
2. Välj åtgärden **Flytta negativa rader**.  
3. På sidan **Flytta negativa inköpsrader** fyller du i fälten efter behov.
4. Välj knappen **OK**. Den negativa raden tas bort från inköpsreturordern, och en ny inköpsorder skapas. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).  

## <a name="to-create-a-purchase-allowance"></a>Så här skapar du ett prisavdrag vid inköp:  
Om en leverantör skickar artiklar som på något sätt inte motsvarar din beställning, t.ex. om varorna är skadade eller har fel färg eller storlek, erbjuds du förmodligen någon form av ersättning eller avdrag på priset.  

Du kan bokföra den reducerade inköpskostnaden som en artikelomkostnad på en kreditnota eller returorder och koppla den till den bokförda inleveransen. Följande tabell beskriver en inköpsreturorder, men samma steg gäller för en inköpskreditnota.

1. Välj ![glödlampeikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpskreditnota** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** för att öppna en ny tom inköpskreditnota.  
3.  Fyll i kreditnotahuvudet med information om den leverantör som du erhållit prisavdraget från.  
4. På snabbfliken **Rader** i fältet **Typ** markerar du **Debitering (artikel)**.  
5.  I fältet **Nr.** markerar du lämpligt värde för artikelomkostnaden.  

    Om du vill kan du skapa ett särskilt artikelomkostnadsnummer som avser prisavdrag.  
6.  Ange **1** i fältet **Antal**.  
7.  Ange beloppet för avdraget i fältet **Inköpspris**.  
8.  Koppla prisavdraget som en artikelomkostnad till artiklarna i den bokförda inleveransen. För mer information, se [Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md) När du har kopplat prisavdraget går du tillbaka till sidan **Inköpskreditnota**.

När du bokför inköpsreturordern läggs inköpstillägget till det aktuella inköpstransaktionsbeloppet. På det här sättet kan du hålla lagervärderingen aktuell.  

## <a name="to-combine-return-shipments"></a>Så här kombinerar du returutleveranser  
Om du vill skicka tillbaka artiklar som täcks av olika inköpsreturorder till samma leverantör kan du använda funktionen **Kombinera returutleveranser**.  

När du levererar artiklarna bokför du relevanta inköpsreturorder som levererade och skapar därmed bokförda inköpsreturutleverans.  

När du är beredd att fakturera de här artiklarna, kan du i stället för att fakturera varje inköpsreturorder för sig skapa en inköpskreditnota och automatiskt kopiera raderna i inköpsreturutleveransen till det här dokumentet. Sedan kan du bokföra inköpskreditnotan och enkelt fakturera alla öppna inköpsreturorder på en gång.  

När returutleveranser kombineras på en kreditnota och sedan bokförs skapas en bokförd inköpskreditnota för de fakturerade raderna. Fältet **Fakturerat antal** på den ursprungliga inköpsreturordern uppdateras utifrån det fakturerade antalet. Emellertid tas den ursprungliga inköpsreturordern inte bort, även om den är helt inlevererad och fakturerad, och därför måste du ta bort inköpsreturordern manuellt.

> [!NOTE]  
> Den här proceduren utgår från ett exempel där det finns flera inköpsreturorder till leverantören, och att dessa har blivit bokförda som levererade.     

1.  Välj ![glödlampeikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpskreditnota** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.  
4. Välj åtgärden **Hämta returutleveransrader**.  
5.  Välj flera returutleveransrader som du vill inkludera på fakturan.  

    Om du har valt en ogiltig returutleveransrad eller du vill börja om från början, behöver du bara ta bort raderna från inköpskreditnotan och använda funktionen **Hämta returutleveransrader** igen.  
6.  Välj åtgärden **Bokföra**.  

### <a name="to-remove-open-purchase-return-orders-after-combined-return-shipment-posting"></a>Så här tar du bort öppna inköpsreturorder efter kombinerad returutleverans bokföring  

1.  Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ta bort fakturerade inköpsreturordrar** och välj sedan relaterad länk.  
2.  Fyll i fälten på efter behov och välj sedan knappen **OK**.  
3.  Du kan också ta bort enskilda inköpsreturorder manuellt.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Korrigera eller annullera obetalda inköpsfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

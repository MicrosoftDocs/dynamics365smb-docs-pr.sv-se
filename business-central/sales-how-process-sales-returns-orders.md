---
title: Behandlar säljreturordrar
description: 'Beskriver hur du skapar en försäljningsreturorder om du vill bearbeta en retur, annullering eller ersättning för artiklar eller tjänster som du har blivit mottagen betalning för.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: edupont
---
# <a name="process-sales-return-orders"></a>Behandlar säljreturordrar

Om du behöver mer kontroll över försäljningsreturprocessen, till exempel distributionslagerdokument för artikelhantering eller bättre överblick när du tar emot artiklar från flera försäljningsdokument med en försäljningsretur, kan du skapa försäljningsreturorder. En försäljningsreturorder utför automatiskt den relaterade försäljningskreditnotan och andra returrelaterade dokument, till exempel en ersättningsförsäljningsorder, om detta behövs.

Förutom den ursprungliga bokförda försäljningsfakturan kan du koppla försäljningskreditnotan eller försäljningsreturorden till andra försäljningsdokument, t.ex en annan bokförd försäljningfaktura, eftersom kunden också returnerar artiklarna som har levererats med den fakturan.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Skapa en försäljningsreturorder baserat på minst ett bokfört försäljningsdokument.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **säljreturordrar** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.  
3. I snabbfliken **Allmänt** fyller du i nödvändiga fält.
4. På snabbfliken **rader** fyller du i raderna manuellt eller kopierar information från andra dokument för att fylla i raderna automatiskt:

    - Du kan använda funktionen **Hämta bokförda dokumentrader som ska återföras** för att kopiera en eller flera bokförda dokumentrader från ett eller flera bokförda dokument. Den här funktionen återför alltid de exakta kostnaderna från den bokförda dokumentraden. Funktionen beskrivs i följande steg.    
    - Du kan använda funktionen **Kopiera från dokument** för att kopiera ett befintligt dokument till returordern. Använd den här funktionen för att kopiera hela dokumentet. Det kan antingen röra sig om ett bokfört dokument eller ett dokument som inte har bokförts ännu. Du kan bara aktivera exakt kostnadsåterföring när kryssrutan **Kräv exakt kost.återföring** är markerad på sidan **Försäljningsinställningar**.  

5. Välj åtgärden **bearbeta** och välj sedan åtgärden **Hämta bokförda dokumentrader som ska återföras**.
6. Högst upp på sidan **Bokförda försäljningsdokumentrader** markerar du kryssrutan **Visa endast rader som kan återföras** om du bara vill visa rader med antal som ännu inte har returnerats. Exempel: om antalet på en bokförd försäljningsfaktura redan har returnerats kanske du inte vill returnera antalet i ett nytt försäljningsreturdokument.

    > [!NOTE]  
    >  Det här fältet fungerar endast för bokförda utleveranser och bokförda fakturarader, inte för bokförda retur- eller kreditnoterader.

    Till vänster på sidan visas olika dokumenttyper, och siffran inom hakparentes visar hur många tillgängliga dokument det finns av respektive dokumenttyp.

7. Välj i fältet **Dokumenttypfilter** vilken typ av bokförda dokumentrader som du vill använda.  
8. Markera de rader som du vill kopiera till det nya dokumentet.  

    > [!NOTE]  
    >  Om du använder <kbd>Ctrl</kbd>+<kbd>A</kbd> för att markera alla rader kopieras alla rader inom det filter som du har angett, men filtret **isa endast rader som kan återföras** ignoreras. Exempel: Du har filtrerat raderna efter ett angivet dokumentnummer med två rader, där den ena raden redan har returnerats. Även om fältet **Visa endast rader som kan återföras** markerats, om du trycker på<kbd>Ctrl</kbd>+<kbd>A</kbd> för att kopiera alla rader kopieras båda raderna i stället för bara den rad som inte har återförts.  

9. Klicka på **OK** om du vill kopiera raderna till det nya dokumentet.  

    Följande processer inträffar:  

    -   För bokförda dokumentrader av typen **Artikel** skapas en ny dokumentrad som är en kopia av den bokförda dokumentraden, med det antal som ännu inte har återförts. Fältet **Koppla från artikellöpnr** fylls i efter behov med numret på artikeltransaktionen för den bokförda dokumentraden.  

    -   För bokförda dokumentrader som inte är av typen **Artikel**, t. ex. artikelomkostnader, skapas en ny dokumentrad som är en kopia av den ursprungliga bokförda dokumentraden.  

    -   Fältet **Styckkostnad (BVA)** på den nya raden beräknas utifrån kostnaderna på motsvarande artikeltransaktioner.  

    -   Om det kopierade dokumentet är en bokförd utleverans, inleverans, returinleverans eller returutleverans beräknas à-priset automatiskt från artikelkortet.  

    -   Om det kopierade dokumentet är en bokförd faktura eller kreditnota kopieras à-priset, fakturarabatterna och radrabatterna från den bokförda dokumentraden.  

    -   Om den bokförda dokumentraden innehåller artikelspårningsrader fylls fältet **Koppla från artikellöpnr** på artikelspårningsraderna i automatiskt med de tillämpliga artikeltransaktionsnumren från de bokförda artikelspårningsraderna.  

     När du kopierar från en bokförd faktura eller kreditnota kopieras eventuella fakturarabatter och radrabatter, som var giltiga vid den tidpunkt då dokumentet bokfördes, från den bokförda dokumentraden till den nya dokumentraden. Observera dock att om alternativet **Beräkna fakturarabatt** är aktiverat på sidan **Försäljningsinställningar** beräknas fakturarabatten på nytt när du bokför den nya dokumentraden. Det kan därför hända att radbeloppet för den nya raden inte är detsamma som radbeloppet för den bokförda dokumentraden, beroende på den nya beräkningen av fakturarabatten.  

     > [!NOTE]  
     >  Om en del av antalet på den bokförda dokumentraden redan har återförts, sålts eller förbrukats skapas en rad bara för det antal som finns kvar i lager eller som inte har returnerats. Om hela antalet på den bokförda dokumentraden har återförts skapas ingen ny dokumentrad.  
     >   
     >  Om varuflödet i det bokförda dokumentet är detsamma som i det nya dokumentet skapas en kopia av den ursprungliga bokförda dokumentraden i det nya dokumentet. Fältet **koppla-från artikellöpnr** fylls inte i eftersom exakt kostnadsåterföring inte är möjligt i det här fallet. t. ex. om du använder funktionen **Hämta bokförda dokumentrader som ska återföras** för att hämta en bokförd försäljningskreditnotarad för en ny försäljningskreditnota kopieras endast den ursprungliga bokförda kreditnotaraden till den nya kreditnotan.  

10. På sidan **Förs.returorder** i fältet **Returorsakskod** för varje rad väljer du orsaken till returen.
11. Välj åtgärden **Bokföra**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Så här skapar du en ersättningsförsäljningsorder från en försäljningsreturorder
Du kan behöva gottgöra kunden för någon försåld artikel genom att den ersätts med en annan. Artikeln kan ersättas med en likadan eller någon annan. Den här situationen kan exempelvis uppstå om fel artikel av misstag har levererats till kunden.  

1. På sidan **Förs.returorder** för en aktiv returprocess på en tom rad skapar du en negativ transaktion för ersättningsartikeln genom att ange ett negativt belopp i fältet **Antal**.  
2. Välj åtgärden **Flytta negativa rader**.
3. På sidan **Flytta negativa förs.rader** fyller du i fälten efter behov.
4. Välj knappen **OK**. Den negativa raden för ersättningsartikeln bort från försäljningsreturordern och infogas på en ny **Försäljningsorder**-sida. Mer information finns i [Sälja produkter](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Så här skapar du returrelaterade dokument från en försäljningsreturorder
Du kan skapa ersättningsförsäljningsorder, inköpsreturorder och ersättningsförsäljningsorder automatiskt under försäljningsreturprocessen. Detta är användbart i situationer där du vill hantera artiklar med garantier från leverantörer.

1. På sidan **Förs.returorder** för en aktiv returprocess, väljer du åtgärden **Skapa returrelaterade dokument**.
2. I fältet **Leverantörsnr** anger du numret på en leverantör om du vill skapa leverantörsdokument automatiskt.
3. Om en returnerad artikel måste returneras till leverantören markerar du kryssrutan **Skapa inköpsreturorder**.
4. Om returnerad en artikel måste beställas från leverantören markerar du kryssrutan **Skapa inköpsorder**.
5. Om du måste skapa en ersättningsförsäljningsorder markerar du kryssrutan **Skapa förs.order**.

## <a name="to-create-a-restock-charge"></a>Så här skapar du en återlagringsavgift
Du kan behöva debitera kunder återlagringsavgift för att täcka hanteringskostnader för retur av någon artikel. Det kan till exempel inträffa om någon kund av misstag beställt fel artikel eller ändrat sig när artikeln tagits emot.

Du kan bokföra den ökade kostnaden som en artikelomkostnad i en kreditnota eller en returorder och koppla den till den bokförda leveransen. Följande tabell beskriver en försäljningsreturorder, men samma steg gäller för en försäljningskreditnota.

1. Öppna sidan **Förs.returorder** för en aktiv returprocess.
2. På en ny rad , i fältet **Typ** väljer du **Omkostnad (artikel)**.  
3. Fyll i fälten för varje artikelomkostnadsrad. För mer information, se [Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader](payables-how-assign-item-charges.md)  

När du bokför försäljningsreturordern läggs återlagringsavgiften till det aktuella försäljningstransaktionsbeloppet. På det här sättet kan du hålla lagervärderingen aktuell.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  
[Behandla inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]

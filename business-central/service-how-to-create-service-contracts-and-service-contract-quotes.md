---
title: Så här arbetar du med servicekontrakt och servicekontraktsofferter | Microsoft Docs
description: 'Du kan skapa ett servicekontrakt manuellt eller utifrån en servicekontraktsoffert. Så här skapar du ett servicekontrakt eller en servicekontraktsoffert:'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="work-with-service-contracts-and-service-contract-quotes"></a><a name="work-with-service-contracts-and-service-contract-quotes"></a>Så här arbetar du med servicekontrakt och servicekontraktsofferter
Du kan skapa ett servicekontrakt manuellt eller utifrån en servicekontraktsoffert. Du kan använda en servicekontraktsoffert som förslag till ett servicekontrakt, där ditt företag lämnar en offert till kunden och får kundens godkännande innan du kan omvandla den till ett servicekontrakt. Det fungerar ungefär likadant om du vill skapa ett servicekontrakt eller en servicekontraktsoffert.  

## <a name="to-create-a-service-contract-or-service-contract-quote"></a><a name="to-create-a-service-contract-or-service-contract-quote"></a>Så här skapar du ett servicekontrakt eller en servicekontraktsoffert
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Servicekontrakt** eller **Servicekontraktsofferter** och sedan väljer du relaterad länk.  
2. Så här skapar du ett servicekontrakt eller en servicekontraktsoffert:  
3. Fyll i fälten **Nr.** . En dialogruta öppnas där du får en fråga om du vill använda allmänna data från en kontraktsmall. Om du vill skapa ett sådant servicekontrakt eller en servicekontraktsoffert klickar du på **Ja**. Sidan **Servicekontraktsmall** öppnas.  
4. Markera önskad mall och klicka sedan på **OK** för att skapa servicekontraktet eller servicekontraktsofferten.  
5. I fältet **Kundnr.** väljer du kunden.  
6. Om du inte vill att ett årligt differensbelopp ska fördelas automatiskt markerar du kryssrutan **Tillåt ej balanserade belopp**. Värdena i **Årligt belopp** och **Beräknat årligt belopp** kvittas inte automatiskt. Om du vill att detta ska göras automatiskt, med distribution av ett valfritt årligt differensbelopp som eventuellt härrör från en ändring i servicekontraktet, lämnar du kryssrutan **Tillåt ej balanserade belopp** tom.  
7. Lägg till kontraktsrader i servicekontraktet eller servicekontraktsofferten.  
8. Det är frivilligt att fylla i övriga fält.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a><a name="to-convert-a-service-contract-quote-to-service-contract"></a>Så här omvandlar du en servicekontraktsoffert till ett servicekontrakt
När en kund har accepterat en servicekontraktsoffert kan du omvandla den till ett servicekontrakt. Samtidigt kan du skapa en servicefaktura för kontraktets startperiod om kontraktets startdatum är före början av nästa faktureringsperiod.

När du har slutfört följande steg skapas ett servicekontrakt med statusen **signerat**. Om en servicefaktura skapas för kontraktets startperiod beräknas det fakturerade beloppet så här, beroende på om kontraktet är detaljerat eller inte.  

För detaljerade kontrakt beräknas fakturabeloppet så här:  

* Fakturerat belopp = summan av det fakturerade beloppet på varje kontraktsrad.  
* Fakturerat belopp på varje kontraktsrad = ((offertvärde ÷ 12) × antalet månader under startperioden) + ((offertvärde ÷ antalet dagar under året) × antalet återstående dagar av startperioden).  
* Om kontraktsraden utgår innan startperioden avslutas blir utgångsdatumet slutdatum till startperioden för raden.  

För kontrakt som inte är detaljerade beräknas fakturabeloppet så här:  

* Fakturerat belopp = (årsbelopp ÷ antalet dagar under året) × antalet dagar under startperioden.  
* Om kontraktet utgår innan startperioden avslutas blir utgångsdatumet slutdatum för startperioden.    

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontraktsofferter** och väljer sedan relaterad länk.  
2. Öppna den servicekontraktsoffert som du vill omvandla till ett servicekontrakt.  
3. Välj åtgärden **Skapa kontrakt**.  
4. Du kan skapa en faktura för kontraktets startperiod om kontraktets startdatum är före början av nästa faktureringsperiod. Välj **Ja**.  

 Servicefakturan bokförs till kontraktets servicekonto även om kontraktet är förutbetalt.

## <a name="to-create-contract-service-credit-memos"></a><a name="to-create-contract-service-credit-memos"></a>Så här skapar du servicekreditnotor för kontrakt:
Du kan använda servicekreditnotor för kontrakt då en kund avbeställer ett förutbetalt servicekontrakt eller tar bort en serviceartikel från ett förutbetalt kontrakt. Du kan också använda det för att korrigera en felaktig servicefaktura  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekreditnotor** och väljer sedan relaterad länk.  
2. Skapa en ny servicekreditnota.  
3. Fyll i fälten **Nr.** .  
4. I fältet **Kundnr.** anger du numret på kunden i servicekontraktet.  

     På snabbfliken **Fakturering** kan du se information som har kopierats från kortet **Kund**. Om du vill bokföra kreditnotan till en annan kund än den som angetts på snabbfliken **Allmänt** anger du den kundens nummer i fältet **Faktureringskundnr** . .  

    > [!NOTE]  
    >  Du kan jämföra kreditnotan med det bokförda originaldokumentet på sidan **Bokförda servicefakturor**. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda servicefakturor** och väljer sedan relaterad länk.  

5. Fyll i fälten **Bokföringsdatum** och **Dokumentdatum** .  
6. Ange information om artiklarna som har returnerats eller flyttats, eller ersättning som ska skickas, på kreditnoteraderna. Du kan även använda batch-jobbet **Hämta förutbetalda kont.trans**.  

 På sidan **Servicekontrakt** på snabbfliken **Fakturadetaljer** kan du markera kryssrutan **Automatiska kreditnotor** om du vill att en kreditnota automatiskt ska skapas när rader tas bort från ett servicekontrakt.  

 För att skapa en kreditnota manuellt när kontraktsrader tas bort från ett servicekontrakt väljer du åtgärden **Kreditnota** på sidan **Servicekontrakt**.  

## <a name="updating-and-evaluating-contracts"></a><a name="updating-and-evaluating-contracts"></a>Uppdatera och utvärdera kontrakt
Ibland måste du ändra villkoren i ett kontrakt efter att det har skapats. I de flesta fall öppnar du önskat kontrakt på sidan **Servicekontrakt** och gör ändringarna som behövs.  

Du kan ändra status för kontraktet, som från början ställts in som **Låst**, lägga till och ta bort kontraktsrader samt makulera ett kontrakt. Om du vill ta reda på om verksamheten går med vinst eller förlust kan du göra en snabb affärsanalys med hjälp av funktionen Kontrakt Trendscape.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a><a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Så här lägger du till en kontraktsrad i ett servicekontrakt eller en kontraktsoffert
När en kund köper en ny artikel och vill ha med den i ett befintligt servicekontrakt eller en kontraktsoffert, kan du registrera artikeln som serviceartikel och sedan lägga till den som en ny kontraktsrad i kontraktet eller kontraktsofferten.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk.  
2. Öppna önskat servicekontrakt eller servicekontraktsoffert där du vill lägga till en ny kontraktsrad.  
3. Välj åtgärden **Öppna kontrakt** om du vill öppna och redigera servicekontraktet eller servicekontraktsofferten.  
4. Gå till snabbfliken **Fakturadetaljer** och markera fältet **Tillåt ej balanserade belopp** om du vill ändra det årliga beloppet och distribuera differensen för det årliga beloppet manuellt på kontraktsraderna. Annars kan du avmarkera kryssrutan i fältet **Tillåt ej balanserade belopp**. Då distribueras differensen för det årliga beloppet automatiskt på kontraktsraderna efter att du ändrat det årliga beloppet.  
5. På snabbfliken **Rader** lägger du till en serviceartikel eller artikel, eller en textbeskrivning på varje kontraktsrad. Du kan också lägga till kontraktsoffertrader. Observera att det går att skapa flera kontrakt per serviceartikel om du vill infoga dem i olika servicekontrakt eller kontraktsofferter samtidigt.  
6. Kontrollera och korrigera siffrorna i **Radrabatt %**, **Radrabattbelopp**, **Svarstid**, **Serviceperiod** och andra fält om det behövs.

## <a name="to-remove-contract-lines"></a><a name="to-remove-contract-lines"></a>Så här tar du bort kontraktsrader
Du kanske måste ta bort kontraktsraderna från servicekontraktet när du tar bort motsvarande serviceartiklar från servicekontraktet. För det mesta tar du bort kontraktsrader som har utgått eller som motsvarar serviceartikeln som har delats upp.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk.  
2. Öppna det servicekontrakt som du vill ta bort kontraktsrader från.  
3. Välj åtgärden **Öppna kontrakt** om du vill öppna och redigera servicekontraktet eller servicekontraktsofferten.  
4. Välj den kontraktsrad som du vill ta bort. Fyll i fältet **Kontrakt utgångsdatum** med datumet då du vill ta bort raden. Det kan till exempel vara den dag då serviceartikeln delades upp.  
5. Välj åtgärden **ta bort kontraktsrader**. Sidan **Ta bort rader från kontrakt** visas.  
6. Fyll i standardfiltren: **Kontraktnr**, filtret **Serviceartikelnr** och filtret **Kontraktstyp**. Om det behövs kan du använda flera filter eller ändra befintliga filter.  
7. Fyll i fälten på snabbfliken **Alternativ** och välj sedan åtgärden **Ta bort rader**.  

> [!NOTE]  
>  Om kontraktet inte är detaljerat måste du uppdatera värdet i fältet **Årligt belopp** på snabbfliken **Fakturadetaljer** på sidan **Servicekontrakt** för att visa att serviceartikeln har tagits bort från kontraktet.  
>   
>  Om kontraktet är detaljerat och förutbetalt, och du har bokfört fakturor för det, kan du skapa en kreditnota för kontraktet. Välj åtgärden **Skapa kreditnota**. Detta är onödigt om kryssrutan i fältet **Automatiskt kreditnotor** på snabbfliken **Fakturadetaljer** är markerad. Här skapas en kreditnota skapas automatiskt när du tar bort en kontraktsrad.

## <a name="service-line-cost-and-value"></a><a name="service-line-cost-and-value"></a>Kostnaden för serviceraden och värde
På servicekontraktsraderna beräknas beloppen i **Radkostnad** och **Radvärde** enligt beskrivningen i följande tabell.

| Alternativ för Radkostnad | Description|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | Kostnaden hämtas automatiskt från fältet **Standardkontraktskostnad** i tabellen **Serviceartikel** och kopieras till fältet **Radkostnad**. Följande formel används då radkostnaden beräknas:<br /><br /> Förs.styckkostnad × Kontraktsvärde % ÷ 100|  
|**Artikel** | Kostnaden hämtas automatiskt från fältet **Styckkostnad** i tabellen **Artikel** och fältet **Kontraktsvärde %** i tabellen **Serviceinställningar**. Följande formel används då radkostnaden beräknas:<br /><br /> Styckkostnad × Kontraktsvärde % ÷ 100|  
|**Textbeskrivning** | Värdet i fältet **Radkostnad** kommer att vara noll.|  

| Alternativ för radvärde | Description|
|----------------------------------|---------------------------------------|  
|**Serviceartikel** | Priset hämtas automatiskt från fältet **Standard kontraktsvärde** i tabellen **Serviceartikel** och kopieras till fältet **Radvärde**.|  
|**Artikel** | Värdet hämtas från fältet **A-pris** eller fältet **Styckkostnad** i tabellen **Artikel** beroende på värdet i fältet **Kontraktsvärde beräkningsmetod** i tabellen **Serviceinställningar**. Därefter multipliceras värdet med innehållet i fältet **Kontraktsvärde %** i tabellen **Serviceinställningar** och divideras med 100. Beloppet kopieras till fältet Radvärde. Beloppet kopieras till fältet **Radvärde**.<br /><br /> **OBS!** Om fältet **Kontraktsvärde beräkningsmetod** är **Ingen**  beräknas inte innehållet i fältet **Radvärde** är inte beräknade.|  
|**Textbeskrivning** | Ffältet **Radvärde** är förinställt på noll.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a><a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Så här lägger du till kontraktsrabatter för servicekontraktsofferter
Du kan lägga till kontraktsrabatt på service för kontraktsofferter och servicekontrakt. Rabatterna kan gälla reservdelar till enskilda serviceartikelgrupper, resurstimmar för enskilda resursgrupper eller enskilda servicekostnader.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontraktsofferter** och väljer sedan relaterad länk.  
2. Välj den offert som du vill lägga till rabatter för.  
3. Välj åtgärden **Servicerabatter**. Sidan **Kontrakt/service rabatter** öppnas.  
4. Välj **Ny** för att ange en ny kontraktsrabatt.  
5. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Om du vill lägga till kontraktsrabatter direkt i ett servicekontrakt utför du en liknande procedur från sidan **Servicekontraktlista**.  

## <a name="to-change-the-owner-of-a-service-contract"></a><a name="to-change-the-owner-of-a-service-contract"></a>Så här ändrar du ägare till servicekontrakt
Du kanske behöver ändra ägaren till servicekontraktet. Om en serviceartikel i ett servicekontrakt är registrerad i flera kontrakt som inte har makulerats och som ägs av samma kund, ändras ägaren automatiskt för alla servicekontrakt som innehåller denna serviceartikel och alla andra serviceartiklar som finns i dessa kontrakt.  

> [!NOTE]  
>  Det här fallet gäller bara för kontrakt som inte har makulerats. Kontraktsoffertens status beaktas inte.  

> [!IMPORTANT]  
>  Serviceartiklar och kontrakt kan vara relaterade. Ändra ägare till ett servicekontrakt kan påverka dessa relationer.  
>   
>  Serviceartikel nr 8 ingår till exempel i flera kontrakt, SC00003 och SC00015. Kontrakt SC00015 innehåller också serviceartikel nr 15, som också ingår i kontrakt SC00080. I det här fallet ändras ägaren för alla tre kontrakt och serviceartiklarna.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk. Öppna relevant servicekontrakt där du vill ändra ägare.  
2. Välj åtgärden **Öppna kontrakt** om du vill öppna och redigera kontraktet.  
3. Välj åtgärden **Ändra kund**. Sidan **Ändra kund i kontrakt** visas.  
4. I fältet **Kontraktnr.** och **Serviceartikelnr** visas numren för de kontrakt och serviceartiklar som ägs av den valda kunden. Om kunden äger flera kontrakt med flera serviceartiklar, blir värdet av dessa fält **Flera**. Om du vill se listan över relaterade kontrakt eller serviceartiklar väljer du dessa fältvärden.  
5. I fältet **Nytt kundnr.** väljer du den nya kunden.  
6. I fältet **ny leveranskod** väljer du adressen.  
7. Klicka på **OK** om du vill ändra kund- och/eller leveranskod för servicekontrakten.  
8. Välj åtgärden **Lås kontrakt** om du vill låsa kontraktet och se till att ändringarna förs in i kontraken.  

## <a name="to-update-a-service-contract-price"></a><a name="to-update-a-service-contract-price"></a>Så här uppdaterar du ett servicekontraktspris
Du kan uppdatera priserna i servicekontrakt genom att ange ett procenttal för prisuppdatering.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Uppdatera servicekontraktspriser** och väljer sedan relaterad länk.
2. Välj servicekontraktet.  
3. Skriv datum i fältet **Uppdatera till datum**. I batch-jobbet uppdateras priserna i kontraktet med datum för nästa prisuppdatering, på eller före detta datum.  
4. I fältet **Prisuppd. %** anger du det procenttal som du vill uppdatera priserna med.  
5. I fältet **Åtgärd** väljer du **Uppdatera kontraktpriser**.  

## <a name="to-post-prepaid-contract-entries"></a><a name="to-post-prepaid-contract-entries"></a>Så här bokför du förutbetalda kontraktstransaktioner
Om du arbetar med förutbetalda servicekontrakt måste du regelbundet bokföra förutbetalda transaktioner och därmed överföra de förutbetalda beloppen från kontona för förutbetalda kontrakt till vanliga kontraktskonton.  

Innan du kan bokföra förutbetalda kontraktstransaktioner måste du ange en nummerserie i fältet **Förutbet. bokf.dok. nr-serie** på sidan **Serviceinställningar**.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Bokför förutbet. kont.trans.** och välj sedan relaterad länk.  
2. Ange ett datum i fältet **Bokför tills datum**. Batch-jobbet bokför förutbetalda kontraktstransaktioner med bokföringsdatum fram till det här datumet.  
4. I fältet **Bokföringsdatum** anger du det datum som du vill använda som bokföringsdatum på den allmänna journalraden.  
5. I fältet **Åtgärd** klickar du på **Bokför förutbet. kont.trans.**  
6. Klicka på **OK** för att bokföra transaktionerna.

## <a name="changing-the-service-contract-status"></a><a name="changing-the-service-contract-status"></a>Ändra servicekontraktstatus
När servicekontraktet är signerat anges värdet i fältet **Ändra status** automatiskt till **Låst**. Om du vill ändra information i servicekontraktet eller i servicekontraktsofferten måste du först ändra statusen för kontraktet eller kontraktsofferten från **Låst** till **Öppen**. Tänk på att du inte kan skapa servicefakturor för ett servicekontrakt med ändringsstatusen **Öppen**. När kontraktet eller kontraktsofferten har modifierats måste du ändra tillbaka statusen till **Låst** för att åter kunna skapa servicefakturor och transaktioner för servicekontraktet, inklusive de ändringar som du har gjort i kontraktet/kontraktsofferten.  

> [!NOTE]  
>  Fältet **Ändra Status** är inte kopplat till fältet **Släppningsstatus**  i huvudet på serviceordern, som styr lagerhanteringen av serviceartiklar.  

## <a name="to-cancel-a-service-contract"></a><a name="to-cancel-a-service-contract"></a>Så här makulerar du kontrakt
Du kanske måste makulera ett servicekontrakt i programmet när detta kontrakt har upphört eller har sagts upp av dig och/eller kunden.  

> [!NOTE]  
>  Du kan inte öppna ett kontrakt efter att det har annullerats.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk.  
2. Öppna relevant servicekontrakt som du vill makulera.  
3. Välj åtgärden **Öppna kontrakt** om du vill öppna och redigera servicekontraktet eller servicekontraktsofferten.  
4. Välj önskad uppföljningskod i fältet **Uppföljningskod för avbryt**. Om du vill lägga till fler uppföljningskoder, väljer du åtgärden **Avancerat**.  

     Om kryssrutan i fältet **Använd kontrakt makulerat** på sidan **Serviceinställningar** är markerad, måste du ange en uppföljningskod för makulerat när du makulerar kontrakt.  

5. Markera **Rättad** i fältet **Status** .  
6. Om det finns icke bokförda fakturor eller kreditnotor eller öppna förutbetalda transaktioner för kontraktet visas ett bekräftelsemeddelande. Klicka på **Nej** i meddelanderutan om du vill gå tillbaka till kontraktet och bokföra dokumenten, eller klicka på **Ja** om du vill fortsätta att makulera.  

## <a name="filing-a-service-contract-or-contract-quote"></a><a name="filing-a-service-contract-or-contract-quote"></a>Så här arkiverar du servicekontrakt och kontraktsofferter
Du kan arkivera servicekontrakt och kontraktsofferter när som helst för att registrera och arkivera en kopia av kontraktet eller kontraktsofferten. [!INCLUDE[prod_short](includes/prod_short.md)]-filernas servicekontrakt arkiveras automatiskt när du omvandlar kontraktsofferter till servicekontrakt eller makulerar kontrakt. Du kan arkivera ett kontrakt eller offert själv genom att välja åtgärden **Arkivera kontrakt** på sidorna **avseende** eller **servicekontraktsofferter**. Om du vill visa arkiverade kontrakt eller offerter söker du efter **arkiverade kontrakt**.

## <a name="see-also"></a><a name="see-also"></a>Se även
[Skapa servicekontrakt](service-how-setup-service-contracts.md)  
[Servicehantering](service-service.md)  
[Så här omvandlar du servicekontrakt som innehåller momsbelopp](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

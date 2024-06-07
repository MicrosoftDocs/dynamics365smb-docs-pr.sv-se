---
title: 'Spåra artiklar med serie-, parti-och paketnummer'
description: 'Du kan lägga till serie-, parti- och paketnummer till alla utgående och inkommande dokument och visa de bokförda artikelspårningstransaktionerna i de associerade artikeltransaktionerna.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 03/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Spåra artiklar med serie-, parti- eller paketnummer

Du kan tilldela serie-, parti- och paketnummer till alla utgående och inkommande dokument och visa de bokförda artikelspårningstransaktionerna i de associerade artikeltransaktionerna. Du spårar objekt på sidan **Artikelspårningsrader** som du öppnar från ett inkommande eller utgående dokument.

I antalsfält längst upp på fönstret **Artikelspårningsrader** visas antalen och summorna för artikelspårningsnummer som anges på raderna i fönstret. Antalen måste stämma överens med antalen på dokumentraderna, som anges med 0 i fälten **Odefinierad**.

[!INCLUDE [prod_short](includes/prod_short.md)] uppdaterar tillgänglighetsinformationen på sidan **Artikelspårningsrader** när du öppnar sidan. Om det inte uppdaterar informationen under tiden som sidan är öppen, även om ändringar sker i lagret eller i andra dokument.

> [!NOTE]  
> För att funktionerna som beskrivs i den här artikeln ska fungera måste du ställa in artikelspårning. Mer information finns i [Ställa in artikelspårning med serie-, parti- eller paketnummer](inventory-how-setup-item-tracking.md).

## Disposition av artikelspårning

När du arbetar med serie-, parti- eller paketnummer beräknar [!INCLUDE[prod_short](includes/prod_short.md)] dispositionsinformationen och visas på de olika artikelspårningssidorna. Det visar hur mycket av ett parti-, paket eller serienummer som används i andra dokument. Denna information hjälper till att minska fel och osäkerhet som orsakas av dubbla fördelningar.

På sidan **Artikelspårningsrader** kan en varningsikon visas i fältet **Disposition, partinr.** or **Tillgänglighet, serienr.** av följande orsaker:

* Om en del av eller hela det valda antalet redan används i andra dokument.
* Om parti- eller serienumret inte är tillgängligt.

Sidorna **partinummer-/serienummerlista**, **partinummer-/serienummerdisposition** och **Artikelspårning – Markera transaktioner** visar kvantiteten av en artikels som utnyttjas. Följande register anger relevanta fält.

|Fält|Description|
|-----|-----------|  
|**Totalt antal**|Det totala antalet artiklar som för närvarande finns i lager.|
|**Totalt begärt antal**|Det totala antalet artiklar som har begärts i det här dokumentet och i andra dokument.|
|**Aktuellt pågående antal**|Antalet artiklar som har begärts i det aktuella dokumentet men som inte har bokförts.|
|**Aktuellt begärt antal**|Antalet artiklar som har begärts i det aktuella dokumentet.|
|**Totalt disponibelt antal**|Det totala antalet artiklar i lager, minus artikelantalet som har begärts i det här dokumentet och i andra dokument (totalt begärt antal) och minus antalet som har begärts, men ännu inte bokförts, i det här dokumentet (aktuellt pågående antal).|

Om du arbetar på sidan **Artikelspårningsrader** under en lång tidsperiod eller om det pågår mycket aktivitet för den artikel som du arbetar med kan du välja åtgärden **Uppdatera tillgänglighet**. Dispositionen för artikeln kontrolleras automatiskt på nytt när sidan stängs, så att eventuella dispositionsproblem kan upptäckas.

## Så här tilldelar du serie-/partinummer vid inkommande transaktioner

Du kanske vill spåra artiklar från det ögonblick de anländer. Då är inköpsordern ofta det centrala dokumentet. Du kan emellertid göra artikelspårning från alla inkommande dokument och visa de bokförda transaktionerna i de associerade artikeltransaktionerna.

Spårningsnumren överförs automatiskt till alla utgående lageraktiviteter.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2. Antingen kan du öppna en befintlig inköpsorder eller skapa en ny inköpsorder.
3. Markera dokumentrad och klicka på snabbfliken **Rader**, välj åtgärden **Rad** och sedan åtgärden **Artikelspårningsrader** för att öppna sidan **Redigera – Artikelspårningsrader**.  

   Du kan tilldela serie- eller partinummer på följande sätt:  
   * Automatiskt, genom att välja **Bearbeta**, sedan **Tilldela serienr** eller **Tilldela partinr** så att serie-/partinummer tilldelas utifrån fördefinierade nummerserier.  
   * Automatiskt, genom att välja **Bearbeta**, sedan **Skapa anpassat SN** så att serie-/partinummer tilldelas utifrån nummerserier som du specifikt definierar för de inkommande artiklarna.  
   * Manuellt, genom att ange serie- eller partinummer direkt, t. ex. leverantörens nummer.  
   * Manuellt, genom att ange ett särskilt nummer för varje artikelenhet.  

4. Tilldela automatiskt genom att välja åtgärden **skapa anpassad SN**.  
5. I fältet **Anpassat SN** anger du startnumret för en beskrivande serienummerserie. Till exempel **S/N-Vend0001**.  
6. I fältet **Öka** skriver du 1 för att ange att varje påföljande nummer ökar med ett.  

    Fältet **Antal att skapa** innehåller radantalet som standard, men detta går att ändra.  

7. Markera kryssrutan **Skapa nytt partinr** för att ordna in de nya serienumren i ett annat parti.  
8. Välj **OK**.  

[!INCLUDE [prod_short](includes/prod_short.md)] skapar ett partinummer med individuella serienummer enligt artikelkvantiteten på dokumentraden. Numret föregås av det värde du angav i fältet **Anpassat SN**. Till exempel, med början **S/N-Vend0001**.  

I antalsfält i huvudet visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalen måste stämma överens med antalen på dokumentraderna, som anges med **0** i fälten **Odefinierad**.  

När du bokför dokumentet överförs artikelspårningsposterna till artikeltransaktioner.

### Så här hanterar du serie- och partinummer när du hämtar inleveransrader från en inköpsfaktura

När du använder hämtar bokförd inleverans eller utleveransrader från relaterade fakturor eller kreditnotor, överförs artikelspårningsrader i distributionslagerdokumenten automatiskt. Men de behandlas på ett speciellt sätt.

Funktionen stöder följande processer för inkommande:  

* **Hämta inleveransrader** – från en inköpsfaktura.  
* **Hämta returleveransrader** – från en inköpskreditnota.  

Funktionen stöder följande processer för utgående:  

* **Hämta leveransrader** – från en försäljningsfaktura eller kombinerade utleveranser.  
* **Hämta returinleveransrader** – från en försäljningskreditnota.  

I dessa fall överförs artikelspårningsraderna till fakturan eller kreditnotan, men sidan **Artikelspårningsrader** låter dig inte ändra serie- eller partinummer. Du kan bara ändra kvantiteterna.  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Öppna en inköpsfaktura för artiklar som är inköp med serie- eller partinummer.  
3. Från en inköpsfaktura på snabbfliken **Rader** väljer du **Hämta inleveransrader**.  
4. Välj inleveransrader, som har artikelspårningsrader, och välj sedan **OK** på sidan **Hämta inleveransrader**.  

    Källdokumentet kopieras till inköpsfakturan som en ny rad och artikelspårningsraderna kopieras till den underliggande sidan **Artikelspårningsrader**.  

5. Välj den överförda inleveransraden i inköpsfakturan.  
6. Klicka på **Rad** och välj **Artikelspårningsrader** på snabbfliken **Rader** om du vill visa de överförda artikelspårningsraderna.  

Du kan inte ändra fälten **serienr.** och **partinr.**. Du kan dock ta bort hela rader eller ändra kvantiteten så att den stämmer med de ändringar som görs av ursprungsraden.  

## Så här tilldelar du serie- eller partinummer vid utgående transaktioner

utgående hantering av serie- eller partinummer är en vanlig uppgift i olika lagerprocesser. Det finns två sätt att lägga till serie- och partinummer på utgående transaktioner:  

- Välj du bland befintliga serie-/partinummer. Detta gäller om artikelspårningsnummer redan har tilldelats vid en inkommande transaktion.
- Tilldela nya serie- eller partinummer vid utgående transaktioner. Detta gäller om artikelspårningsnummer inte ska tilldelas till artiklar förrän de säljs och är klara för utleverans.

### Så här väljer du bland befintliga serie-/partinummer  

När du arbetar med artiklar som kräver artikelspårning och du skapar utgående transaktioner, måste du vanligtvis välja parti- eller serienummer som redan finns.

1. I avgående dokument ska den rad markeras som serie- eller partinummer ska väljas för.  
2. På snabbfliken **Rader** väljer du åtgärden **Rad**, sedan **Relaterad information** och väljer sedan **Artikelspårningsrader**.  
3. På sidan **Artikelspårningsrader** finns det tre alternativ för att ange parti- eller serienummer:  

   * Välj fältet **Serienr** och välj sedan ett nummer på sidan **Lista med serienr**.
   * Välj fältet **Partinr** och välj sedan ett nummer på sidan **Lista med partinr**. Välj fältet **Serienr** och välj sedan ett nummer på sidan **Lista med serienr**.
   * Välj åtgärden **Bearbeta** och välj sedan **Välj poster**. På sidan **Välj poster** visas alla parti ochserienummer tillsammans med den tillgängliga informationen.

4. I fältet **Valt antal** anger du antalet av varje parti – eller serienummer som du vill använda.
5. Välj **OK**. Artikelspårningsinformationen överförs till sidan **Artikelspårningsrader**.  

I antalsfält i huvudet visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalen måste stämma överens med antalen på dokumentraden, som anges med **0** i fälten **Odefinierad**.  

När dokumentraden bokförs överförs artikelspårningsinformationen till de associerade artikeltransaktionerna.

### Tilldela nya serie- eller partinummer  

Den här processen tillämpas när artiklar inte har serie- eller partinummer när de finns i lager. Istället tilldelar du artikelspårningsnummer när artiklar är sålda och redo att skickas. I det här fallet tilldelar du vanligtvis nummer från en fördefinierad nummerserie.

1. Markera det relevanta dokumentet, till exempel en försäljningsfaktura eller försäljningsorder, och välj åtgärden **Rad** på snabbfliken **Rader**, sedan **Relaterad information** och välj sedan åtgärden **Artikelspårningsrader**.  

    Du kan tilldela artikelspårningsnummer på följande sätt:  
    * Automatiskt utifrån fördefinierade nummerserier: gå till fliken **Tilldela serienr** eller **Tilldela partinr.**.  
    * Automatiskt, baserat på parametrar du definierar särskilt för den utgående artikeln: Välj åtgärden **Skapa anpassat SN**.  
    * Manuellt, genom att ange serie- eller partinummer oberoende av nummerserierna.  

2. Tilldela ett serienummer automatiskt genom att välja **Tilldela serienr**för den här proceduren  

    Fältet **Antal att skapa** innehåller radantalet som standard, men detta går att ändra.  
3. Markera fältet **Skapa nytt partinr** för att ordna in de nya serienumren i ett annat parti.  
4. Klicka på **OK** om du vill att ett partinummer och nya, enskilda serienummer ska skapas enligt "antal att hantera" på den associerade dokumentraden.  

I antalsfält längst upp visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalen måste stämma överens med antalen på dokumentraden, som anges med **0** i fälten **Odefinierad**.  

När du bokför dokumentet överförs artikelspårningsposterna till artikeltransaktioner.

### Tilldela spårningsnummer på källdokument

Vissa företag definierar specifika serie- eller partinummer i källdokument, till exempel försäljningsorder. Till exempel om en kund begär ett visst objekt. När du skapar lagerplock- eller lagerplockdokumentet från ett utgående källdokument där serie- eller partinummer redan är definierade, kan du inte ändra några fält på sidan **Artikelspårningsrader** under lagerplockningen. Det enda undantaget är fältet **Ant. att hantera**. I detta fall anger lagerplockningsraderna artikelspårningsnumren på enskilda ta- och placerarader. Kvantiteten är redan uppdelad på unika kombinationer av serienummer eller partinummer eftersom de artikelspårningsnummer som ska levereras är specificerade på försäljningsordern.

## Så här hanterar du serie-/partinummer på överföringsorder

Rutinerna för hantering av serie- och partinummer som överförs mellan olika lagerställen påminner om procedurerna vid artikelinköp och -försäljning.  

Överföringsordern är emellertid unik eftersom både utleveransen och inleveransen utförs från samma överföringsrad, vilket innebär att samma instans på sidan **Artikelspårningsrader** används. Artikelspårningsnummer som levereras från ett lagerställe måste inlevereras oförändrade till det andra lagerstället.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **överföringsorder** och väljer sedan relaterad länk.  
2. Öppna den order som du vill bearbeta. På snabbfliken **Rader** välj åtgärden **Rad**, **Artikelspårningsrader** och sedan **Utleverans**.  
3. På sidan **Artikelspårningsrader** tilldelar eller väljer du serie-/partinummer för eventuella övriga utgående artikeltransaktioner.  

    När du hanterar serie- och partinummer för överför du artiklar är nummer vanligtvis redan tilldelade nummer. Därför väljer du ofta bland befintliga serie- eller partinummer.  

4. Bokför överföringsordern, först ut- och sedan inleverans, för att ange att artiklarna överförs med artikelspårningstransaktionerna.  

Under överföringen kan du inte ändra värden på **Artikelspårningsrader**.  

## Så här registrerar du ytterligare information om serie- eller partinummer

Om du behöver koppla särskild information till ett artikelspårningsnummer, till exempel för kvalitetssäkring, kan du göra det på ett informationskort för serienummer eller partinummer.

1. Öppna ett dokument som har serie-/partinummer tilldelas.
2. Öppna sidan **Artikelspårningsrader** för den artikel som du vill ange information för.
3. Välj åtgärden **Rad** och sedan exempelvis åtgärden **Serienr informationskort**.  
4. Välj plustecknet **(+)** överst i listan för att skapa en ny post. Fälten **Serienr** och **Partinr** fylls i på förhand med information från artikelspårningsraden.
5. Ange kortfattad information i fältet **Beskrivning**, t. ex. om villkoret för artikeln.  
6. Välj åtgärden **Relaterad**, välj åtgärden **Serienr** och sedan åtgärden **Kommentar** för att skapa en separat kommentarpost.  
7. Markera fältet **Spärrad** om du vill utesluta serie- eller partinummer från alla transaktioner.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Du kan ändra skapade serie- eller partiinformationskort senare.

## Så här ändras befintlig information om serie-/partinummer

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Markera en artikel som har en artikelspårningskod och serienr eller partinr information.
3. Från sidan **artikelkort** väljer du åtgärden **transaktioner** och väljer **transaktioner**.
4. Välj fältet **Partinr** , eller **Serienr**. Om information för artikelspårningsnumret finns öppnas sidan **Lista med partinr.information** eller **Lista med serienr.information**.  
5. Välj ett kort och välj sedan åtgärden **Partinrinfo.kort/Serienr informationskort**.  
6. Ändra den korta beskrivningstexten, kommentarsposten eller fältet **Spärrad**.  

Du kan inte ändra serie- eller partinummer eller antal. För att kunna göra det måste du gruppera artikeltransaktionen. För att lära dig mer om omklassificering, gå till [Omgruppera parti- eller serienummer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## Gruppera parti- eller serienummer

Att gruppera artikelspårningen för en artikel innebär att ett parti- eller serienummer ändras till ett nytt parti- eller serienummer eller att utgångsdatumet ändras till ett nytt utgångsdatum. Om du använder partier kan du också slå ihop flera partier till en. Använd en artikelgrupperingsjournal för att utföra dessa uppgifter.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] verifierar att varje rad har en unik kombination av serie-, parti- och/eller paketnummer. Om du vill dela upp ett parti, ett paket eller ett parti och paketera det i flera partier eller paket måste du använda flera journalrader.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikelgrupperingsjournal** och väljer sedan relaterad länk.  
2. Fyll i raden med relevant information. Mer information finns i [Beräkna lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md) eller [Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).
3. Välj åtgärden **artikelspårningsrader**.  
4. I fälten **Serienr** eller **Partinr** väljer du aktuellt serie- eller partinummer.  
5. Om ett nytt artikelspårningsnummer behöver anges kan fälten **Nytt serienr** eller **Nytt partinr** användas. Det går även att koppla ett eller flera partier till ett nytt parti eller ett befintligt parti.  

    > [!NOTE]  
    > Observera att när utgångsdatum grupperas föreslås artiklarna med de tidigaste utgångsdatumen för de utgående transaktionerna först. För mer information, gå till [Hämtas av FEFO](warehouse-picking-by-fefo.md).  

6. För att ange nytt utgångsdatum för serie- eller partinumret kan fältet **Nytt utgångsdatum** användas.  

    > [!IMPORTANT]  
    > * Om ett parti grupperas till samma partinummer, men med ett annat utgångsdatum, måste hela partiet grupperas på en artikelgrupperingsjournalrad.
    > * Om mer än ett parti grupperas till ett nytt partinummer, d.v.s. att mer än ett parti kopplas till ett nytt parti, måste samma nya utgångsdatum anges för samtliga partier. 
    > * Om ett befintligt parti grupperas till ett annat befintligt parti, som inte har samma utgångsdatum, måste utgångsdatumet för det andra partiet användas. 
    > * Om inga värden anges i fältet **Nytt utgångsdatum** grupperas parti- eller serienumret med ett tomt utgångsdatum.  

7. Om det finns befintlig information om det gamla serie- eller partinumret går det att kopiera informationen till det nya serie- eller partinumret.  

    1. På sidan **Artikelspårningsrader**, välj **Ny serienr-information** eller **Ny partinr-information**.  
    2. Om du vill kopiera information från det gamla parti- eller serienumret väljer du åtgärden **Kopiera info**.  
    3. Klicka på knappen **OK** när det parti- eller serienummer har valts som informationen ska kopieras ifrån. Detta görs i på sidan med informationslistor.  

8. Genom att registrera information om parti- eller serienummer kan den befintliga informationen om parti- eller serienumret ändras.  
9. Bokför journalen för att koppla de nya artikelspårningsnumren eller utgångsdatumen till den associerade artikeltransaktionen.

## Skanna streckkoder med Business Central-mobilappen

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Om sidan **Artikelspårningsrader**, om du vill skanna flera serie-, parti- eller paketstreckkoder kan du använda **Skanna flera**. När du har skannat en streckkod anges dess värde i fältet på sidan och nästa snabbinmatningsfält blir tillgängligt. Du kan också använda streckkodsläsarens ikon för att fylla i specifika fält.

I följande tabeller visas de sidor som stöder streckkodsskanning för artikelspårning från mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Sida  |Fältvärden som du kan skanna  |
|---------|---------|
|Artikelspårningsrader     |* Serienummer<br><br>* Nytt serienummer<br><br>* Partinummer<br><br>* Nytt partinummer<br><br>* Paketnummer<br><br>* Nytt paketnummer|
|Dist.lager. Artikelspårningsrader     |* Serienummer<br><br>* Nytt serienummer<br><br>* Partinummer<br><br>* Nytt partinummer<br><br>* Paketnummer<br><br>* Nytt paketnummer|
|Artikelspårning     |* Serienrfilter<br><br>* Partinrfilter<br><br>* Paketnummer Filtrera |
|Artikeljournal     |* Serienummer<br><br>* Partinummer<br><br>* Paketnummer     |
|Dist.lageraktivitet rad     |* Serienummer<br><br>* Partinummer<br><br>* Paketnummer<br><br>**Obs**! På följande sidor används sidan Lageraktivitetsrad:<br><br>* sidan 5780 "Dist.lager. Välj underformulär"<br><br>* sidan 7378 "Invt. Välj underformulär"<br><br>* sidan 5771 "Dist.lager. Artikelinförsel subformulär"<br><br>* sidan 7316 "Subformulär för lagertransport"<br><br>* sidan 7376 "Subformulär för lagerinförsel"<br><br>* sidan 7383 "Subformulär för lagertransport"        |
|Dist.lager. Inventeringsjournal     |* Serienummer<br><br>* Partinummer<br><br>* Paketnummer         |

## Se även

[Konfigurera artikelspårning med serie-, parti- eller paketnummer](inventory-how-setup-item-tracking.md)  
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

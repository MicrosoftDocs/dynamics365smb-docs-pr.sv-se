---
title: Spåra artiklar med serie-, parti-och paketnummer
description: Du kan lägga till serie-, parti- och paketnummer till alla utgående och inkommande dokument och visa de bokförda artikelspårningstransaktionerna i de associerade artikeltransaktionerna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/31/2021
ms.author: edupont
ms.openlocfilehash: d9197f158423fa969dd6270c20dd43c26ae75b99
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482253"
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Spåra artiklar med serie-, parti-och paketnummer

Du kan tilldela serie-, parti- och paketnummer till alla utgående och inkommande dokument och visa de bokförda artikelspårningstransaktionerna i de associerade artikeltransaktionerna. Du utför arbetet på sidan **Artikelspårningsrader** som du öppnar från ett inkommande eller utgående dokument.

I matrisen med antalsfält längst upp på fönstret **Artikelspårningsrader** visas antalen och summorna för artikelspårningsnummer som anges på raderna i fönstret. Antalen måste stämma överens med antalen på dokumentraden, som anges med 0 i fälten **Odefinierad**.

För att ge bättre prestanda samlas tillgänglighetsinformationen på sidan **Artikelspårningsrader** endast en gång när du öppnar sidan. Detta innebär att informationen om tillgänglighet inte uppdateras under tiden som sidan är öppen, även om ändringar sker i lagret eller i andra dokument.

> [!NOTE]  
>  För att funktionerna som beskrivs i den här artikeln ska fungera måste du först ställa in artikelspårning. Mer information finns i [Ställa in artikelspårning med serie-, parti- eller paketnummer](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Disposition av artikelspårning

När du arbetar med serie-, parti- eller paketnummer beräknar [!INCLUDE[prod_short](includes/prod_short.md)] dispositionsinformationen och visas på de olika artikelspårningssidorna. På så sätt kan du visa hur mycket av ett parti-, paket eller serienummer som för närvarande används i andra dokument. Det minskar fel och osäkerhet som orsakas av dubbla fördelningar.

På sidan **Artikelspårningsrader** visas en varningsikon i fälten **Disposition, partinr** eller **Disposition, serienr** om en del av eller hela antalet som har valts redan används i andra dokument eller om parti- eller serienumret inte är disponibelt.

På sidorna **partinummer-/serienummerlista**, **partinummer-/serienummerdisposition** och **Artikelspårning – Markera transaktioner** finns information om hur stor del av en artikels antal som utnyttjas. Följande information inkluderas.

|Fält|Description|
|-----|-----------|  
|**Totalt antal**|Det totala antalet artiklar som för närvarande finns i lager.|
|**Totalt begärt antal**|Det totala antalet artiklar som har begärts i det här dokumentet och i andra dokument.|
|**Aktuellt pågående antal**|Antalet artiklar som har begärts i det aktuella dokumentet, men som ännu inte har allokerats till databasen.|
|**Aktuellt begärt antal**|Antalet artiklar som har begärts i det aktuella dokumentet.|
|**Totalt disponibelt antal**|Det totala antalet artiklar i lager, minus artikelantalet som har begärts i det här dokumentet och i andra dokument (totalt begärt antal) och minus antalet som har begärts, men ännu inte allokerats, i det här dokumentet (aktuellt pågående antal).|

Om du arbetar på sidan **Artikelspårningsrader** under en lång tidsperiod eller om det pågår mycket aktivitet för den artikel som du arbetar med kan du välja åtgärden **Uppdatera tillgänglighet**. Dispositionen för artikeln kontrolleras automatiskt på nytt när sidan stängs, så att eventuella dispositionsproblem kan upptäckas.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Så här tilldelar du serie-/partinummer vid inkommande transaktioner

Ibland vill man i ett företag kunna spåra artiklar från det ögonblick då de ankommer till företaget. I detta fall utgör ofta inköpsordern det centrala dokumentet, även om du kan hantera artikelspårning från vilket inkommande dokument som helst och visa dokumentets bokförda transaktioner i de associerade artikeltransaktionerna.

På så sätt överförs numren automatiskt för alla utgående lageraktiviteter utan interaktion av lagerarbetare.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  
2. Antingen kan du öppna en befintlig inköpsorder eller skapa en ny inköpsorder.
3. Markera önskad dokumentrad och klicka på snabbfliken **Rader**, välj åtgärden **Rad** och sedan åtgärden **Artikelspårningsrader** för att öppna sidan **Redigera – Artikelspårningsrader**.  

    Du kan tilldela serie- eller partinummer på följande sätt:  
    -   Automatiskt, genom att välja **Bearbeta**, sedan **Tilldela serienr** eller **Tilldela partinr** så att serie-/partinummer tilldelas utifrån fördefinierade nummerserier.  
    -   Automatiskt, genom att välja **Bearbeta**, sedan **Skapa anpassat SN** så att serie-/partinummer tilldelas utifrån nummerserier som du specifikt definierar för de inkommande artiklarna.  
    -   Manuellt, genom att ange serie- eller partinummer direkt, t. ex. leverantörens nummer.  
    -   Manuellt, genom att ange ett särskilt nummer för varje artikelenhet.  

4. Tilldela automatiskt genom att välja åtgärden **skapa anpassad SN**.  
5. I fältet **Anpassat SN** anger du startnumret för en beskrivande serienummerserie, till exempel **S/N-Vend0001**.  
6. I fältet **Öka** skriver du 1 för att ange att varje påföljande nummer ökar med ett.  

    Fältet **Antal att skapa** innehåller radantalet som standard, men detta går att ändra.  

7. Markera kryssrutan **Skapa nytt partinr** för att ordna in de nya serienumren i ett annat parti.  
7. Välj knappen **OK**.  

Nu skapas ett partinummer som innehåller enskilda serienummer enligt artikelantalet på dokumentraden, med början från **S/N-Vend0001**.  

I matrisen med antalsfält i huvudet visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalen måste stämma överens med antalen på dokumentraden, som anges med 0 i fälten **Odefinierad**.  

När dokumentet bokförs överförs artikelspårningstransaktionerna till de associerade artikeltransaktionerna.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Så här hanterar du serie- och partinummer när du hämtar inleveransrader från en inköpsfaktura

När du använder funktionen för att hämta bokförd inleverans, eller utleveransrader från relaterade fakturor eller kreditnotor, överförs artikelspårningsrader i distributionslagerdokumenten automatiskt. Men de behandlas på ett speciellt sätt.

Funktionen stöder följande processer för inkommande:  
-   **Hämta inleveransrader** – från en inköpsfaktura.  
-   **Hämta returleveransrader** – från en inköpskreditnota.  

Funktionen stöder följande processer för utgående:  
-   **Hämta leveransrader** – från en försäljningsfaktura eller kombinerade utleveranser.  
-   **Hämta returinleveransrader** – från en försäljningskreditnota.  

I de här situationerna kopieras befintliga artikelspårningsrader automatiskt till fakturan eller kreditnotan, men på sidan **Artikelspårningsrader** tillåts inga ändringar av serienummer eller partinummer. Endast kvantiteter kan ändras.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Öppna en inköpsfaktura för artiklar som är inköp med serie- eller partinummer.  
3. Från en inköpsfaktura på snabbfliken **Rader** väljer du **Hämta inleveransrader**.  
4. Välj inleveransrader, som har artikelspårningsrader, och välj sedan **OK** på sidan **Hämta inleveransrader**.  

    Källdokumentet kopieras till inköpsfakturan som en ny rad och artikelspårningsraderna kopieras till den underliggande sidan **Artikelspårningsrader**.  

5. Välj den överförda inleveransraden i inköpsfakturan.  
6. Klicka på **Rad** och välj **Artikelspårningsrader** på snabbfliken **Rader** om du vill visa de överförda artikelspårningsraderna.  

Innehållet i fälten **Serienr** Och **Partinr** går inte att redigera. Du kan dock ta bort hela rader eller ändra kvantiteten så att den stämmer med de ändringar som görs av ursprungsraden.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Så här tilldelar du serie- eller partinummer vid utgående transaktioner

utgående hantering av serie- eller partinummer är en vanlig uppgift i olika lagerprocesser. Det finns två sätt att lägga till serie- och partinummer på utgående transaktioner:  

-   Välja bland befintliga serie- eller partinummer. Detta gäller om artikelspårningsnummer redan har tilldelats vid en inkommande transaktion.
-   Tilldela nya serie- eller partinummer vid utgående transaktioner. Detta gäller om artikelspårningsnummer inte ska tilldelas till artiklar förrän de säljs och är klara för utleverans.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Så här väljer du bland befintliga serie-/partinummer  

Vanligtvis måste redan befintliga parti- eller serienummer i lagret väljas för artiklarna som kräver artikelspårning. Denna regel gäller även när utgående transaktioner skapas, d.v.s. när artiklarna tas bort ur lagret.

1. I utgående dokument ska den rad markeras som serie- eller partinummer ska väljas för.  
2. På snabbfliken **Rader** väljer du åtgärden **Rad**, sedan **Relaterad information** och väljer sedan **Artikelspårningsrader**.  
3. På sidan **Artikelspårningsrader** finns det tre alternativ för att ange parti- eller serienummer:  

    - Välj fältet **Serienr** och välj sedan ett nummer på sidan **Lista med serienr**.
    - Välj fältet **Partinr** och välj sedan ett nummer på sidan **Lista med partinr**. Välj sedan fältet **Serienr** och välj sedan ett nummer på sidan **Lista med serienr**.
    - Välj åtgärden **Bearbeta** och välj sedan **Välj poster**. På sidan **Välj poster** visas alla parti ochserienummer tillsammans med den tillgängliga informationen.

4. I fältet **Valt antal** anger du antalet av varje parti – eller serienummer som du vill använda.
5. Klicka på **OK** så överförs den valda artikelspårningsinformationen till sidan **Artikelspårningsrader**.  

I matrisen med antalsfält i huvudet visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalet måste stämma överens med antalet på dokumentraden, som anges med **0** i fälten **Odefinierad**.  

När dokumentraden bokförs överförs artikelspårningsinformationen till de associerade artikeltransaktionerna.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Tilldela nya serie- eller partinummer  

Det här alternativet gäller när lagerartiklarna inte har serie- eller partinummer utan i stället artikelspårningsnummer när artiklarna säljs och är klara att levereras. I scenariot tilldelas nummer vanligtvis från en fördefinierad nummerserie.

1. Markera det relevanta dokumentet, till exempel en försäljningsfaktura eller försäljningsorder, och välj åtgärden **Rad** på snabbfliken **Rader**, sedan **Relaterad information** och välj sedan åtgärden **Artikelspårningsrader**.  

    Du kan tilldela artikelspårningsnummer på följande sätt:  
    -   Automatiskt utifrån fördefinierade nummerserier: gå till fliken **Tilldela serienr** eller **Tilldela partinr.**.  
    -   Automatiskt, baserat på parametrar du definierar särskilt för den utgående artikeln: Välj åtgärden **Skapa anpassat SN**.  
    -   Manuellt, genom att ange serie- eller partinummer oberoende av nummerserierna.  

2. Tilldela ett serienummer automatiskt genom att välja **Tilldela serienr** för den här proceduren  

    Fältet **Antal att skapa** innehåller radantalet som standard, men detta går att ändra.  
3. Markera fältet **Skapa nytt partinr** för att ordna in de nya serienumren i ett annat parti.  
4. Klicka på **OK** om du vill att ett partinummer och nya, enskilda serienummer ska skapas enligt "antal att hantera" på den associerade dokumentraden.  

I matrisen med antalsfält längst upp visas dynamiskt antalen och summorna för de artikelspårningsnummer du anger på sidan. Antalet måste stämma överens med antalet på dokumentraden, som anges med **0** i fälten **Odefinierad**.  

När dokumentet bokförs överförs artikelspårningstransaktionerna till de associerade artikeltransaktionerna.

### <a name="assign-tracking-numbers-on-source-documents"></a>Tilldela spårningsnummer på källdokument

I vissa situationer i lager med serie – eller partinummer definieras specifika serie- eller partinummer i källdokumentet, till exempel försäljningsorder, som lagerarbetaren måste respektera under den utgående lagerhanteringen. Det kan bero på att kunden valde ett visst parti under orderprocessen. När lagerplockningen eller dokumentet för dist.lager plockning skapas från ett utgående källdokument där serie- eller partinummer redan är definierade, är alla fält på sidan **Artikelspårningsrader** under lagerplockningen skrivskyddade, utom fältet **Ant. att hantera**. I detta fall anger lagerplockningsraderna artikelspårningsnumren på enskilda ta- och placerarader. Kvantiteten är redan uppdelad på unika kombinationer av serienummer eller partinummer eftersom de artikelspårningsnummer som ska levereras är specificerade på försäljningsordern.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Så här hanterar du serie-/partinummer på överföringsorder

Rutinerna för hantering av serie- och partinummer som överförs mellan olika lagerställen påminner om procedurerna vid artikelinköp och -försäljning.  

Överföringsordern är emellertid unik eftersom både utleveransen och inleveransen utförs från samma överföringsrad, vilket innebär att samma instans på sidan **Artikelspårningsrader** används. Detta innebär också att artikelspårningsnummer som levereras från ett lagerställe måste inlevereras oförändrade till det andra lagerstället.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **överföringsorder** och väljer sedan relaterad länk.  
2. Öppna den order som du vill bearbeta. På snabbfliken **Rader** välj åtgärden **Rad**, **Artikelspårningsrader** och sedan **Utleverans**.  
3. På sidan **Artikelspårningsrader** tilldelar eller väljer du serie-/partinummer för eventuella övriga utgående artikeltransaktioner.  

    Vid hanteringen av serie- och partinummer för överföringsartiklar, har artiklarna vanligtvis redan tilldelats nummer. Förloppet består därför oftast bara av att du väljer bland befintliga serie- eller partinummer.  

4. Bokför överföringsordern, först ut- och sedan inleverans, för att ange att artiklarna överförs med artikelspårningstransaktionerna.  

Sidan **Artikelspårningsrader** är skrivskyddat under överföringen.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Så här registrerar du ytterligare information om serie- eller partinummer

Om du behöver koppla särskild information till ett visst artikelspårningsnummer, till exempel för kvalitetssäkring, kan du göra det på ett informationskort för serienummer eller partinummer.

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

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Så här ändras befintlig information om serie-/partinummer

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Markera en artikel som har en artikelspårningskod och serienr eller partinr information.
3. Från sidan **artikelkort** väljer du åtgärden **transaktioner** och väljer **transaktioner**.
4. Välj fältet **Partinr** , eller **Serienr**. Om information för artikelspårningsnumret finns öppnas sidan **Lista med partinr.information** eller **Lista med serienr.information**.  
5. Välj ett kort och välj sedan åtgärden **Partinrinfo.kort/Serienr informationskort**.  
6. Ändra den korta beskrivningstexten, kommentarsposten eller fältet **Spärrad**.  

Du kan inte ändra serie- eller partinummer eller antal. För att kunna göra det måste du gruppera artikeltransaktionen i fråga. Mer information finns i [Omgruppera parti- eller serienummer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Gruppera parti- eller serienummer

Att gruppera artikelspårningen för en artikel innebär att ett parti- eller serienummer ändras till ett nytt parti- eller serienummer eller att utgångsdatumet ändras till ett nytt utgångsdatum. Vid arbete med partier går det även att koppla flera partier till ett enda. De här aktiviteterna utförs med hjälp av artikelgrupperingsjournalen.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artikelgrupperingsjournal** och väljer sedan relaterad länk.  
2. Fyll i raden med relevant information. Mer information finns i [Beräkna lager med hjälp av dokument](inventory-how-count-inventory-with-documents.md) eller [Inventera, justera och gruppera lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).
3. Välj åtgärden **artikelspårningsrader**.  
4. I fälten **Serienr** eller **Partinr** väljer du aktuellt serie- eller partinummer.  
5. Om ett nytt artikelspårningsnummer behöver anges kan fälten **Nytt serienr** eller **Nytt partinr** användas. Det går även att koppla ett eller flera partier till ett nytt parti eller ett befintligt parti.  

    > [!NOTE]  
    >  Observera att när utgångsdatum grupperas föreslås artiklarna med de tidigaste utgångsdatumen för de utgående transaktionerna först. Mer information finns i [Plocka enligt FEFO](warehouse-picking-by-fefo.md).  

6. Om ett nytt utgångsdatum behöver anges för serie- eller partinumret kan fältet **Nytt utgångsdatum** användas.  

    > [!IMPORTANT]  
    >  Om ett parti grupperas till samma partinummer, men med ett annat utgångsdatum, måste hela partiet grupperas på en artikelgrupperingsjournalrad. Om mer än ett parti grupperas till ett nytt partinummer, d.v.s. att mer än ett parti kopplas till ett nytt parti, måste samma nya utgångsdatum anges för samtliga partier. Om ett befintligt parti grupperas till ett annat befintligt parti, som inte har samma utgångsdatum, måste utgångsdatumet för det andra partiet användas. Om inga värden anges i fältet **Nytt utgångsdatum** grupperas parti- eller serienumret med ett tomt utgångsdatum.  

7. Om det finns befintlig information om det gamla serie- eller partinumret går det att kopiera informationen till det nya serie- eller partinumret.  

    1. På sidan **Artikelspårningsrader**, välj **Ny serienr-information** eller **Ny partinr-information**.  
    2. Om du vill kopiera information från det gamla parti- eller serienumret väljer du åtgärden **Kopiera info**.  
    3. Klicka på knappen **OK** när det parti- eller serienummer har valts som informationen ska kopieras ifrån. Detta görs i på sidan med informationslistor.  

8. Genom att registrera information om parti- eller serienummer kan den befintliga informationen om parti- eller serienumret ändras.  
9. Bokför journalen för att koppla de nya artikelspårningsnumren eller utgångsdatumen till den associerade artikeltransaktionen.

## <a name="see-also"></a>Se även

[Ställa in artikelspårning med serie-, parti- eller paketnummer](inventory-how-setup-item-tracking.md)  
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Artikelkoppling](design-details-item-tracking.md)  
[Designdetaljer: Artikelkoppling och reservationer](design-details-item-tracking-and-reservations.md)  
[Reservera artiklar](inventory-how-to-reserve-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
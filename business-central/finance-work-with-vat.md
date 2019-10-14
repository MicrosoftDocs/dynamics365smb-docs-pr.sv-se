---
title: Så här arbetar du med moms på försäljning och inköp | Microsoft Docs
description: Det här avsnittet beskriver hur du utför uppgifter som att rätta bokförd moms i EU-länder/regioner, där varje försäljnings- och inköptransaktion är momspliktiga. Det här avsnittet beskriver hur.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: ab408bbef4e2fc9535eaa64e61a9e93d2d87378c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301570"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbeta med moms på försäljning och inköp
Om ditt land eller din region kräver att du beräknar moms (VAT) på försäljnings- och inköpstransaktioner så att du kan rapportera beloppen till en skattemyndighet, kan du ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)] till att automatiskt beräkna moms på försäljnings- och inköpsdokument. Mer information finns i [ställa in beräkningar och bokföring av metoder för moms](finance-setup-vat.md).

Det finns emellertid vissa momsrelaterade uppgifter som du kan göra manuellt. Du kan t.ex. behöva korrigera ett bokfört belopp om du upptäcker att en leverantör använder en annan avrundningsmetod.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Beräkna och visa momsbelopp i försäljnings- och inköpsdokument  
Du kan beräkna och visa momsbelopp i försäljnings- och inköpsdokument på olika sätt beroende på vilken typ av kund eller leverantör som du handlar med. Du kan också åsidosätta det momsbelopp som har beräknats för att matcha det momsbelopp som har beräknats av leverantören för en given transaktion.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Enhetspris och radbelopp inklusive/exklusive moms på försäljningsdokument  
När du väljer ett artikelnummer i fältet **Nr**. i ett försäljningsdokument fyller även [!INCLUDE[d365fin](includes/d365fin_md.md)] i fältet **Enhetspris**. Enhetspriset kommer antingen från kortet **Artikel** eller från artikelpriserna för artikeln och kunden. [!INCLUDE[d365fin](includes/d365fin_md.md)]beräknar **Radbelopp** när du anger en kvantitet för raden.  

Om du säljer till återförsäljare kan du vilja att priserna på försäljningsdokument inkluderar moms. Gör detta genom att markera kryssrutan **Priser inkl. moms** på dokumentet.  

### <a name="including-or-excluding-vat-on-prices"></a>Inklusive eller exklusive moms på priser
Om kryssrutan **Priser inklusive moms** är markerad på ett försäljningsdokument inkluderar **Enhetspris** och **Radbelopp** moms och detta visas även i fältnamnen. Som standard ingår moms inte i de här fälten.  

Om fältet inte är markerat fylls fälten **Enhetspris** och **Radbelopp** automatiskt i exklusive moms och detta visas även i fältnamnen.  

Du kan lägga upp en standarduppsättning av **Priser inklusive moms** för alla försäljningsdokument för en kund i fältet **Priser inklusive moms** på **Kund**-kortet. Du kan också lägga upp att artikelpriser ska anges inklusive eller exklusive moms. Vanligtvis anges artikelpriser på artikelkortet exklusive moms. Informationen i fältet **Pris inklusive moms** på **artikelkortet** används för att ange enhetsprisbeloppet för försäljningsdokument.  

Följande tabell innehåller en översikt över hur enhetsprisbeloppen för ett försäljningsdokument beräknas när du inte har lagt upp priser på sidan **Försäljningspriser**:  

|**Fältet Försäljningspris inklusive moms på artikelkortet**|**Fältet Priser inklusive moms i försäljningshuvudet**|**Utförd åtgärd**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ingen markering|Ingen markering|**Enhetspriset** på artikelkortet kopieras till fältet **Enhetspris exkl. moms** på försäljningsraderna.|  
|Ingen markering|Markering|Momsbeloppet beräknas per enhet och läggs till **enhetspriset** på artikelkortet. Det totala enhetspriset anges sedan i **fältet Enhetspris inkl. moms** på försäljningsraderna.|  
|Markering|Ingen markering|Programmet beräknas momsbeloppet som inkluderas i **A-pris** på artikelkortet med hjälp av den momssats % i förhållande till moms rörelsebokföringsmall och moms produktbokföringsmall. **A-pris** på artikelkortet, minus momsbeloppet, anges sedan i **Enhetspris exl. moms** på försäljningsraderna.|  
|Markering|Markering|**Enhetspriset** på artikelkortet kopieras till fältet **Enhetspris inkl. moms**.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Manuellt korrigera momsbelopp i försäljnings- och inköpsdokument  
Det går att göra  korrigeringar av bokförda momstransaktioner. Detta gör det möjligt att ändra de totala försäljnings- eller inköpsmomsbeloppen utan att ändra nettobeloppet. Detta kan vara nödvändigt om t.ex. en leverantör skickar en faktura med felberäknad moms.  

Även om du har ställt in en eller flera kombinationer för hantering av importmoms, måste du skapa minst en produktbokföringsmall för moms. Du kan till exempel ge det namnet **KORREKT** för korrigeringssyfte, om du inte kan använda samma redovisningskonto i **Ingående moms** på momsbokföringsinställningsraden. Mer information finns i [ställa in beräkningar och bokföring av metoder för moms](finance-setup-vat.md).

Om en kassarabatt har beräknats utifrån ett fakturabelopp inklusive moms kan du återställa den del av momsbeloppet som utgörs av kassarabatten när kassarabatten beviljas. Observera att du måste aktivera fältet **Justering för kassarabatt** i både redovisningsinställningarna generellt och i momsbokföringsinställningarna för särskilda kombinationer av rörelsebokföringsmallar för moms och produktbokföringsmallar för moms.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Så här ställer du in systemet för manuell momsregistrering i försäljningsdokument
Nedan beskrivs hur du aktiverar manuella momsändringar för försäljningsdokument. Stegen är liknande på sidan **Inköpsinställningar**.

1. På sidan  **Redovisningsinställningar** ange en  **Max. tillåten momsdifferens** mellan det belopp som har beräknats automatiskt och det manuella beloppet.  
2. På sidan **Tillåt momsdifferens** i fönstret **Försäljningsinställningar** .  

### <a name="to-adjust-vat-for-a-sales-document"></a>Så här justerar du moms för ett försäljningsdokument  
1. Öppna den aktuella försäljningsordern.  
2. Välj åtgärden **Statistik**.  
3. På snabbfliken **Fakturering** väljer du värde i fältet **Antal momsrader**.
4. Redigera fältet **Momsbelopp**.   

> [!NOTE]  
> Det totala momsbeloppet för fakturan visas på raderna grupperade per moms-ID. Du kan justera beloppet i fältet **Momsbelopp**på raderna för varje moms-ID. När du ändrar fältet **Momsbelopp** utförs en kontroll för att undersöka att du inte har ändrat momsen med mer än det belopp som du har angett som maximal tillåten differens. Om beloppet ligger utanför intervallet i **Max. tillåten momsdifferens** visas en varning som anger den maximala tillåtna differensen. Du kommer inte att kunna fortsätta förrän beloppet justeras inom godkända parametrar. Klicka på **OK** och ange ett annat **Momsbelopp** som ligger inom det tillåtna intervallet. Om momsdifferensen är lika med eller lägre än den maximala tillåtna differensen fördelas momsen proportionellt över dokumentraderna som har samma moms-ID.  

## <a name="calculating-vat-manually-using-journals"></a>Manuell momsberäkning med hjälp av journaler  
Du kan också justera momsbelopp i redovisnings-, försäljnings- och inköpsjournaler. Detta kan vara nödvändigt när du anger en leverantörsfaktura i journalen och det förekommer en differens mellan det momsbeloppet som [!INCLUDE[d365fin](includes/d365fin_md.md)] beräknade och momsbeloppet på den leverantörsfaktura du har tagit emot.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Så här ställer du in systemet för manuell momsregistrering i redovisningsjournaler
Du måste utföra följande steg innan du kan ange moms manuellt i en redovisningsjournal.  

1. På sidan  **Redovisningsinställningar** ange en  **Max. tillåten momsdifferens** mellan det belopp som har beräknats automatiskt och det manuella beloppet.  
2. På sidan **Redovisningsjournalmallar** markerar du kryssrutan **Tillåt momsdifferens** för den relevanta journalen.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Så här ställer du in systemet för manuell momsregistrering i försäljnings- och inköpsjournaler
Du måste utföra följande steg innan du kan ange moms manuellt i en försäljnings- och inköpsjournal.

1. På sidan **Inköpsinställningar** markerar du kryssrutan **Tillåt momsdifferens**.  
2. Upprepa steg 1 för sidan **Försäljningsinställningar**.
3. När du har slutfört den inställning som beskrivs ovan kan du justera fältet **Momsbelopp** i redovisningsjournalraden eller fältet **Momsbelopp bal.** i försäljnings- eller inköpsjournalen så att det motsvarar momsbeloppet på fakturan. [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer att kontrollera att differensen inte är större än det angivna maxbeloppet.  

    > [!NOTE]  
    > Om differensen är större visas en varning som anger den maximala tillåtna differensen. Innan du fortsätter måste du justera beloppet. Klicka på **OK** och ange ett annat belopp som ligger inom det tillåtna intervallet. Om momsdifferensen är lika med eller lägre än den maximala tillåtna differensen visar [!INCLUDE[d365fin](includes/d365fin_md.md)] differensen i fältet **Momsdifferens**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Bokföra du importmoms med inköpsfakturor
I stället för att använda journaler för att bokföra en importmomsfaktura, kan du använda en inköpsfaktura.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Konfigurera inköp för bokföring av fakturor med specificerad importmoms  
1. Skapa ett leverantörskort för den importavdelning som skickar importmomsfakturan till dig. **Gen. rörelsebokföringsmall** och **Moms rörelsebokföringsmall** måste ställas in på samma sätt som redovisningskontot för importmomsen.  
2. Skapa en **produktbokföringsmall** för importmomsen och skapa **produktbokf.mall för standardmoms** för den kopplade **produktbokföringsmallen** för importmomsen.  
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontoplan** och välj sedan relaterad länk.  
4. Välj redovisningskonto för importmomsen och sedan på, fliken **Start** i gruppen **Hantera**, välj **Redigera**.  
5. På snabbfliken **Bokföring**  i fältet **Produktbokföringsmall** för importmomsen. [!INCLUDE[d365fin](includes/d365fin_md.md)] fyller automatiskt i **Moms, produktbokföringsmall**.  
6. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokföringsinställningar** och välj sedan relaterad länk.  
7. Skapa en kombination av **Gen. rörelsebokföringsmall** för skattemyndigheterna och **Produktbokföringsmall** för importmoms. Välj importmervärdeskattredovisningskontot för den här nya kombinationen i fältet **Inköpskonto**.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Så här skapar du en ny faktura för leverantören när du har slutfört inställningen  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Inköpsfakturor** och välj sedan relaterad länk.  
2. Skapa en ny inköpsfaktura.  
3. I fältet **Inköpsleverantörsnr** markerar du leverantören och klickar på **OK**.  
4. I inköpsraden, i fältet **Typ** välj **Redovisningskonto**, och i fältet **Nr.** markera redovisningskontot för importmoms.  
5. I fältet **Antal** anger du **1**.  
6. I fältet **Inköpspris exkl. moms** skriver du in momsbeloppet.  
7. Bokföra fakturan  

## <a name="processing-certificates-of-supply"></a>Behandla leveransintyg
När du säljer varor till en kund i ett annat EU-land/region, måste du skicka kunden ett leveransintyg som kunden måste signera och returnera till dig. Följande tillvägagångssätt används för att behandla leveransintyg för försäljningsutleveranser, men samma moment gäller för serviceleveranser av artiklar och returutleveranser till leverantörer.  

### <a name="to-view-certificate-of-supply-details"></a>Så här visar du information om leveransintyg  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda försäljningsutleveranser** och välj sedan relaterad länk.  
2. Välj den relevanta försäljningsutleveransen till en kund i ett annat EU-land/-region.  
3. Välj **Information om leveransintyg**.  
4. Som standard, om den momsbokföringsmall som har ställts in för kunden har kryssrutan **Leveransintyg krävs** markerad, så är fältet **Status** angett till **Obligatoriskt**. Du kan uppdatera fältet för att visa om intyget har tagits emot från kunden.  

    > [!Note]  
    >  Om inställningen av momsbokföringsmallen inte har kryssrutan **Leveransintyg krävs** markerad skapas en post, och fältet **Status** får värdet **Ej tillämpbart**. Du kan uppdatera fältet för att visa rätt information om status. Du kan manuellt ändra statusen från **Ej tillämpbart** till **Obligatoriskt**och från **Obligatoriskt** till **Ej tillämpbart** efter behov.  

   När du uppdaterar fältet **Status** till **Obligatoriskt**, **Inlevererat**eller **Ej inlevererat**, skapas ett certifikat.  

    > [!TIP]  
    >  Du kan använda sidan **Leveransintyg** för att få en vy över alla bokförda utleveranser som ett leveransintyg har skapats för.  

5. Välj **Skriv ut leveransintyg**.  

    > [!Note]  
    >  Du kan granska och skriva ut dokumentet. När du väljer **Skriv ut leveransintyg** och skriver ut dokumentet, väljs kryssrutan **Utskrivet** automatiskt. Dessutom, om den inte redan har angetts, uppdateras statusen för intyget till **Obligatoriskt**. Du inkluderar det utskrivna intyget med utleveransen.  

### <a name="to-print-a-certificate-of-supply"></a>Så här skriver du ut ett leveransintyg  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda försäljningsutleveranser** och välj sedan relaterad länk.  
2. Välj den relevanta försäljningsutleveransen till en kund i ett annat EU-land/-region.  
3. Välj **Skriv ut leveransintyg**.  

    > [!NOTE]  
    >  Alternativt kan du skriva ut ett intyg från fönstret **Leveransintyg**.  

4. Välj kryssrutan **Utskriftsradinformation** om du vill inkludera information från raderna i utleveransdokumentet på leveransintyget.  
5. Välj kryssrutan **Skapa leveransintyg om de inte redan skapats** om du vill att [!INCLUDE[d365fin](includes/d365fin_md.md)] ska skapa intyg för bokförda leveranser som inte har något vid utförandet. När du markerar kryssrutan upprättas nya certifikat för alla bokförda utleveranser som inte har intyg i det valda intervallet  
6. Som standard gäller filterinställningarna för utleveransdokumentet som du har valt. Fyll i information om filter för att välja ett visst leveransintyg som du vill skriva ut.  
7. På sidan **Leveransintyg** väljer du åtgärden **Skriv utPrint** för att skriva ut rapporten eller välja åtgärden **Förhandsgranska** för att visa den på skärmen.  

    > [!Note]  
    > Fältet **leveransintygstatus** och **Utskrivet** är uppdaterade för leveransen på sidan **leveransintyg**.  

8. Du måste skicka det utskrivna leveransintyget till kunden för signatur.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Så här uppdaterar du statusen för ett leveransintyg för en utleverans  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokförda försäljningsutleveranser** och välj sedan relaterad länk.  
2. Välj den relevanta försäljningsutleveransen till en kund i ett annat EU-land/-region.  
3. I fältet **Status** väljer du önskat alternativ.  

   Om kunden har returnerat det undertecknade leveransintyget väljer du **Inlevererat**. Fältet **Inleveransdatum** uppdateras. Som standard anges inleveransdatumet till aktuellt arbetsdatum.  

   Du kan ändra datumet för att visa datumet då du fick kundens signerade leveransintyg. Du kan också lägga till en länk till det undertecknade intyget med hjälp av standardkoppling för [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Om kunden inte returnerar det undertecknade leveransintyget väljer du **Ej inlevererad**. Du måste sedan skicka kunden en ny faktura som omfattar moms, eftersom den ursprungliga fakturan inte kommer att accepteras av skattemyndigheten.  

Om du vill visa en grupp av certifikat startar du från på sidan **Leveransintyg** och uppdaterar sedan information om status för utestående intyg när du tar emot dem från kunderna. Det kan vara användbart när du vill söka efter alla intyg som har en viss status, till exempel **Obligatoriskt**, för vilka du vill uppdatera statusen till **Ej inlevererat**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Så här uppdaterar du statusen för en grupp med leveransintyg  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Leveransintyg** och välj sedan relaterad länk.  
2. Filtrera fältet **Status** fältet till värdet som du vill ha för att skapa listan över intyg som du vill hantera.  
3. Om du vill uppdatera information om status, Välj **Redigera lista**.  
4. I fältet **Status** väljer du önskat alternativ.  

   Om kunden har returnerat det undertecknade leveransintyget väljer du **Inlevererat**. Fältet **Inleveransdatum** uppdateras. Som standard anges inleveransdatumet till aktuellt arbetsdatum.  

   Du kan ändra datumet för att visa datumet då du fick det signerade leveransintyget. Du kan också lägga till en länk till det undertecknade intyget med hjälp av standarddokumentkoppling för [!INCLUDE[d365fin](includes/d365fin_md.md)].  

    > [!NOTE]  
    >  Du kan inte skapa ett nytt leveransintyg på sidan **Leveransintyg** när du navigerar till den med den här proceduren. Om du vill skapa ett intyg för en leverans som inte var inställd för att kräva en öppnar du den bokförda försäljningsutleveransen och använder någon av de två procedurer som beskrivs ovan:  
    >   
    > * Så här skapar du manuellt ett leveransintyg  
    > * Så här skriver du ut ett leveransintyg.

## <a name="see-also"></a>Se även  
[Förbereda för beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)   
[Så här: rapportera moms till skattemyndigheterna](finance-how-report-vat.md)   

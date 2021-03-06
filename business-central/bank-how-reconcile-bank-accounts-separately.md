---
title: Stämma av bankkonton | Microsoft Docs
description: Beskriver hur ditt lagervärde stäms av med redovisningen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1049043da0fd4cd5db2dc76f41a3c3df0402bbfc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786813"
---
# <a name="reconcile-bank-accounts"></a>Stämma av bankkonton

Du utför bankavstämning för att se till att dina olika affärstransaktioner och utgifter återspeglas korrekt i företagets böcker. Du gör detta genom att jämföra och matcha poster i dina interna bankkonton med banktransaktioner på din bank och sedan bokföra saldona på dina interna bankkonton för att göra summorna tillgängliga för ekonomichefer. Bankavstämning är också ett praktiskt sätt att upptäcka och lösa problem med saknade betalningar och bokföringsfel.

Nedanstående beskriver hur du utför bankavstämning med sidan **Bankkontoavstämning**.

> [!TIP]
> Du kan också stämma av bankkonton på sidan **Betalningsavstämningsjournal** när du bearbetar betalningar. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för de betalningar som du bokför med journalen. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I Nordamerika kan du också utföra detta arbete på sidan **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler. Du använder den här sidan i stället för sidan **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** på sidan **Redovisningsinställningar**. Mer information finns i avsnittet [stämma av bankkonton](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Förenta staterna: lokal funktion.

Raderna på sidan **Bankkontoavstämning** är uppdelade i två rutor. Rutan **Bankkontoavstämning** visar antingen importerade banktransaktioner eller transaktioner med utestående utbetalningar. Rutan **Bankkontotransaktioner** visar transaktionerna på det interna bankkontot.

Att avstämma banktransaktioner med interna banktransaktioner kallas *matchning*. Du kan välja att utföra matchning automatiskt genom att använda funktionen **Matcha automatiskt**. Alternativt kan manuellt välja rader i båda fönster för att koppla varje kontoutdragrad till en eller flera motsvarande bankkontotransaktioner och sedan använda **Matcha manuellt** funktionen. Kryssrutan **Kopplad** markeras på rader där transaktioner matchas. Mer information finns i [Konfigurera regler för automatiska betalningskopplingar](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Om kontoutdragsrader berör checktransaktioner kan du inte använda matchningsfunktionerna. I stället måste du välja åtgärden **Koppla trans.** och sedan välja den relevanta checktransaktionen att matcha kontoutdragraden med.

När värdet i fältet **Totalt saldo** i rutan **Kontoutdragsrader** är lika med värdet i fältet **Saldo att stämma av** i rutan **Bankkontotransaktioner** kan du välja åtgärden **Bokför**. Alla icke-matchade bankkontotransaktioner kommer att finnas kvar på sidan, vilket indikerar en viss avvikelse som du bör lösa för att stämma av bankkontot.

Alla rader som inte kan matchas, vilket anges med ett värde i fältet **Skillnad**, finns kvar på sidan **Bankkontoavstämning** efter bokföring. De representerar någon form av avvikelse som du måste lösa innan du kan slutföra bankkontoavstämningen. Typiska affärssituationer som kan orsaka skillnader:

| Skillnad | Orsak: | Upplösning |
|------------|--------|------------|
| En transaktion i det interna bankkontot finns inte med på kontoutdraget. | Banktransaktionen har inte skett trots att en bokföring gjordes i [!INCLUDE[prod_short](includes/prod_short.md)]. | Utför den saknade penningtransaktionen (eller be en gäldenär att utföra den), och återimportera sedan bankutdragsfilen igen eller ange transaktionen manuellt. |
| En transaktion på kontoutdraget finns inte som ett dokument eller en journalrad i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaktion gjordes utan motsvarande bokföring i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en journalradsbokföring för en utgift. | Skapa och bokför den saknade transaktionen. Information om ett snabbt sätt att initiera detta finns i [Så här skapar du saknade transaktioner för att matcha banktransaktioner med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with). |
| En transaktion i det interna bankkontot motsvarar en banktransaktion, men viss information är för annorlunda för att ge en matchning. | Information, till exempel belopp eller kundnamn, angavs på olika sätt i samband med banktransaktionen eller den interna bokföringen. | Granska informationen och matcha sedan de två manuellt. Du kan också korrigera informationsmatchningsfelet. |

Du måste lösa skillnaderna, till exempel genom att skapa saknade poster och korrigera icke-matchande information, eller genom att utföra saknade penningtransaktioner, tills bankkontoavstämningen är slutförd och bokförd.

Du kan fylla i rutan **Kontoutdragrader** på sidan **Bankkontoavstämning** på följande sätt:

* Automatiskt: Genom att använda funktionen **Import kontoutdrag** för att fylla i rutan **Kontoutdragsrad** med bankkontotransaktioner som baseras på en importerad fil eller ström som tillhandahålls av banken.
* Manuellt: Genom att använda funktionen **Föreslå rader** för att fylla i rutan **Kontoutdragsrader** i enlighet med fakturor i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalningar.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Så här fyller du i bankavstämningrader genom att importera ett kontoutdrag

Fönstret **Kontoutdragsrader** fylls med banktransaktioner enligt en importerad fil eller ström som tillhandahålls av banken.

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera Envestnet Yodlee Bank Feeds-tjänsten och sedan länka dina bankkonton till relaterade onlinebankkonton. Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan också importera bankutdragsfiler i komma- eller semikolonavgränsat format (.CSV). Använd **Konfigurera importformat för en kontoutdragsfil** assisterad installation för att definiera importformat för kontoutdrag och bifoga formatet till ett bankkonto. Du kan sedan använda dessa format när du importerar bankutdrag på sidan **Bankkontoavstämning**.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkontoavstämning** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Välj ett bankkonto i fältet **Bankkontonr**. Bankkontotransaktionerna som finns på bankkonto, visas i rutan **Bankkontotransaktioner**.
4. Ange datumet på kontoutdraget från banken i fältet **Kontoutdragets datum**.
5. Ange saldot på kontoutdraget från banken i fältet **Kontoutdragets slutsaldo**.
6. Om du har en bankutdragsfil väljer du åtgärden **Importera bankutdrag**.
7. Leta upp filen och välj sedan knappen **Öppna** för att importera banktransaktionerna till rutan **Kontoutdragsrader** på sidan **Bankkontoavstämning**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Så här fyller du i bankavstämningrader med funktionen Föreslå rader

Rutan **Kontoutdragsrader** fylls i enligt fakturorna i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalningar.  

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Föreslå rader**.
2. Ange det tidigaste bokföringsdatumet för transaktionsavstämningen i fältet **Startdatum**.
3. Ange det senaste bokföringsdatumet för transaktionsavstämningen i fältet **Slutdatum**.
4. Om du vill att föreslå checktransaktion istället för bankkontotransaktioner markerar du kryssrutan **Ta med checkar**.
5. Välj **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Så här matchar du automatiskt kontoutdragrader med bankkontotransaktioner

Sidan **Bankkontoavstämning** erbjuder automatiskt matchande funktioner baserade på en textmatchning på en kontoutdragsrad (vänster ruta) med text på en eller flera redovisningstransaktioner för bankkontot (höger ruta). Observera att du kan skriva över de föreslagna automatiska matchningarna, och du kan också välja att inte använda automatisk matchning alls. För mer information, se [Så här matchar du kontoutdragrader med bankkontotransaktioner manuellt](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Matcha automatiskt**. Sidan **Matcha banktransaktioner** öppnas.
2. Ange antalet dagar före och efter bankkontotransaktionbokföringsdatumet som funktionen ska söka i för att matcha bokföringsdatum i bankkontoutdraget i fältet **Bokföringsdatumtolerans (dagar)**.

    Om du anger 0 eller lämnar fältet tomt kommer funktionen **Matcha automatiskt** endast söka efter matchande bokföringsdatum på bankkontotransaktionbokföringsdatumet.
3. Välj **OK**.

    Alla kontoutdragrader och bankkontotransaktioner som kan matchas ändrar till grönt teckensnitt och **Kopplat** kryssrutan markeras.
4. Markera kontoutdragraden och välj sedan åtgärden **Ta bort matchning**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Så här matchar du manuellt bankutdragsrader med bankkontotransaktioner

1. På sidan **Bankkontoavstämning** markerar du en okopplad rad i rutan **Kontoutdragrader**.
2. I rutan **Bankkontotransaktioner** markerar du en eller flera bankkontotransaktioner som kan matchas med den valda kontoutdragraden. Om du vill välja flera rader, tryck och håll ned CTRL-tangenten.
3. Välj åtgärden **Matcha manuellt**.

    Den valda kontoutdragraden och de valda bankkontotransaktionerna ändrar till grönt teckensnitt och **Kopplat** kryssrutan i det högra fönstret markeras.
4. Upprepa moment 1 till och med 3 för alla kontoutdragrader som inte matchas.
5. Markera kontoutdragraden och välj sedan åtgärden **Ta bort matchning**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Så här skapar du saknade transaktioner att matcha med banktransaktioner

Ibland kan det hända att ett kontoutdrag från banken innehåller belopp som motsvarar en avgift eller räntekostnad. Sådana banktransaktionsrader kan inte matchas eftersom inga relaterade transaktioner finns i [!INCLUDE[prod_short](includes/prod_short.md)]. Du måste sedan bokföra en journalrad för varje transaktion för att skapa en artikelrelaterad transaktion som den kan matchas med.

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Överföring till redovisningsjournal**.  
2. På sidan **Bankavst. trans. åt redov.jnl** anger du vilka redovisningsjournalen om du vill använda och klickar på knappen **OK**.

    Sidan **Redovisningsjournal** öppnas med nya journalrader för alla bankrapportrader med saknade transaktioner.
3. Fyll i journalraden med information, till exempel motkonton. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).  
4. Välj åtgärden **Testrapport** – om du vill granska resultatet av bokföringen innan du bokför. Rapporten **bankkontoutdrag** öppnas och visar samma fält som rubrik på sidan **Bankkontoavstämning**.
5. Välj åtgärden **Bokföra**.

    När transaktionen har bokförts går du vidare och matchar kontoutdragsraden med den.
6. Uppdatera eller öppna sidan **Bankkontoavstämning** igen. Den nya transaktionen ska visas i fönstret **Bankkontotransaktioner**.
7. Matcha kontoutdragraden till bankkontotransaktionen, antingen manuellt eller automatiskt.

## <a name="undo-a-bank-account-reconciliation"></a>Ångra en bankkontoavstämning
Om du upptäcker ett misstag i en bokförd bankavstämning kan du använda åtgärden **Ångra** på sidan **Bankkontoutdrag** för att korrigera misstaget. När du ångrar en bokförd bankavstämning flyttas transaktionerna till sidan **Bankavstämning** och markeras som **Öppna**, vilket innebär att de inte stämts av. Du kan sedan rätta bankavstämningen och bokföra den igen.

> [!NOTE]
> I den Nordamerikanska versionen måste du aktivera brytaren **Bankavstämn. med auto-matchning** på sidan **Redovisningsinställning** om du vill använda funktionen Ångra för bokförda bankavstämningar och kontoutdrag. Funktionen Ångra är inte tillgänglig för kontoutdrag som har bokförts från kalkylblad för bankavstämning.

### <a name="reusing-the-bank-statement-number"></a>Återanvända kontoutdragsnumret
Det kontoutdragsnummer som används för den nya bankavstämningen tas från bankkontot, precis som saldot för senaste kontoavstämning. Du kan ändra dessa värden innan du börjar en ny bankavstämning. När du skapar en ny bankavstämning kontrollerar emellertid [!INCLUDE[d365fin](includes/d365fin_md.md)] om utdragsnumret redan har tilldelats ett bokfört kontoutdrag. Om numret redan används men du vill att det nya kontoutdraget ska använda det istället, kan du använda åtgärden **Ändra dokumentnr.** på sidan **Bankkontoavstämn.**.

### <a name="examples"></a>Exempel
Nedan följer några exempel på hur du kan korrigera ett misstag i en bokförd bankavstämning med eller utan att använda samma utdragsnummer.

#### <a name="example-1"></a>Exempel 1
Du utförde bankavstämningar för januari, februari och mars. Kontoutdragsnumret var 100 för mars. Senare upptäcker du att mars bara inkluderade transaktioner fram till och med den 30, vilket innebär att transaktionerna för den 31 saknas. Därför måste du göra om bankavstämningen för mars. I det här fallet öppnar vi fönstret **Kontoutdrag**, väljer utdraget för mars och väljer sedan **Ångra**. 

Den nya bankavstämningen erhåller utdragsnummer 101. Om du vill tilldela om numret 100 väljer du **Ändra utdragsnr.** och ange **100**. 

> [!TIP]
> Glöm inte att ange lämpligt slutdatum för utdrag (i detta exempel: den 31 mars) och redigera fältet **Saldo för senaste kontoavstämning**. 

#### <a name="example-2"></a>Exempel 2
Du utförde bankavstämningar för januari, februari, juni och juli. Du upptäcker att februari var felaktigt. Vi antar att det hade utdragsnummer 100. På samma sätt som i Exempel 1 använder du fältet Ångra och Ändra utlåtandenr. åtgärder för att ändra utdragsnumret på samma sätt som i Exempel #1 ovan, och du kan nu göra om bankavstämningen för februari.  

Efter att du har bokfört den korrigerade bankavstämningen för februari kommer, på motsvarande bankkontokort, fältet **Senaste utdragsnr.** att ange **100**, och fältet **Saldo för senaste kontoavstämning** att ange slutsaldot för februariutlåtandet. 

Om nästa bankavstämning du gör är för mars kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] att tilldela 101 som utdragsnummer och ge den rätt **Saldo för senaste kontoavstämning**.

Om nästa bankavstämning du gör är för augusti bör du överväga att ändra värdena i fälten **Senaste utdragsnr.** och **Saldo för senaste kontoavstämning** på kortet **Bankkonto** innan du upprättar nästa bankavstämning, eller använd åtgärden Ändra utdragsnr och ändra även värdet i fältet "Saldo för senaste kontoavstämning" på sidan för bankavstämning.

> [!NOTE]
> Utdrags numret är viktigt när du gör bankavstämningar med importerade CAMT-filer som innehåller utdragsnummer eller när du stämmer av baserat på utskrivna kontoutdrag. Om du bara hämtar en serie banktransaktioner från internetbanken är utdragsnumret vanligen oviktigt. 
>
>Saldot för senaste kontoavstämning lagras på bankkontot för att minimera misstag vid bankavstämningar, men det kan också redigeras, så att du kan utföra dina bankavstämningar i valfri ordning. Detta innebär också att om du ångrar ett kontoutdrag kanske det nya slutsaldot inte är saldot för den senaste kontoavstämningen på nästa kontoutdrag. Det finns ingen funktion som gör att du kan flytta ett saldo framåt till alla efterföljande kontoutdrag, så tänk på detta när du använder Ångra. 

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Jämka bankkonton](bank-manage-bank-accounts.md)  
[Tillämpa betalningar automatiskt och jämka bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Definiera regler för automatisk koppling av betalningar](receivables-how-set-up-payment-application-rules.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
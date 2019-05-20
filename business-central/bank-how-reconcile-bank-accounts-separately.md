---
title: Stämma av bankkonton separat | Microsoft Docs
description: Beskriver hur ditt lagervärde stäms av med redovisningen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 60b3e0d732125f60b092a0e089cabc2b82ad71ef
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245102"
---
# <a name="reconcile-bank-accounts-separately"></a>Stämma av bankkonton separat
Stämma av bankkonton i [!INCLUDE[d365fin](includes/d365fin_md.md)] med rapporter har fått från banken, börjar du med att fylla i den vänstra rutan på sidan **bankkontoavstämning** med bankutdragsinformation som måste matcha (synkronisera) med redovisningstransaktioner för bankkontot i den högra rutan. Ett smart sätt att fylla i bankutdragsrader är genom att importera en bankkontoutdragsfil eller feed.

> [!NOTE]  
> I Nordamerika kan du också utföra detta arbete på sidan **Bank poster kalkylblad** som passar bättre för kontroller och inlåning men inte erbjuder import av bankutdragsfiler. Du använder den här sidan i stället för sidan **bankkontoavstämning**, avmarkera fälten **Bankavstämning med auto. match** på sidan **Redovisningsinställningar**. Mer information finns i avsnittet ”stämma av bankkonton” under Förenta staterna: lokal funktion.

> [!TIP]  
> Du kan också stämma av bankkonton på sidan **Betalningsavstämningsjournal**. Eventuella öppna bankkontotransaktioner som relateras till kopplade kund- eller leverantörsreskontratransaktionerna kommer att avslutas när du väljer **Bokför betalningar och stäm av bankkonton**. Detta betyder att bankkontot stäms av automatiskt för betalningar som du bokför med journalen. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

Om du vill aktivera import av bankutdrag som en bankfeed måste du först skapa och aktivera Envestnet Yodlee Bank Feeds-tjänsten och sedan länka dina bankkonton till relaterade onlinebankkonton. Mer information finns i [Konfigurera du Envestnet Yodlee Bank Feeds-tjänsten](bank-how-setup-bank-statement-service.md).

Raderna på sidan **Bankkontoavstämning** är uppdelade i två rutor. Rutan **Bankkontoavstämning** visar antingen importerade banktransaktioner eller transaktioner med utestående utbetalningar. Rutan **Bankkontotransaktioner** visar transaktionerna på bankkontot.

Aktiviteten att hitta och koppla transaktioner som ska stämmas av benämns som *matchning*. Du kan välja att utföra matchning automatiskt genom att använda funktionen **Matcha automatiskt**. Alternativt kan manuellt välja rader i båda fönster för att koppla varje kontoutdragrad till en eller flera motsvarande bankkontotransaktioner och sedan använda **Matcha manuellt** funktionen. Kryssrutan **Kopplad** markeras på rader där transaktioner matchas.

Du kan fylla i rutan **Kontoutdragrader** på sidan **Bankkontoavstämning** på följande sätt:

* Automatiskt, genom att använda funktionen **Importera bankutdrag** för att fylla i raderna enligt faktiska bankkontotransaktioner som baseras på en fil som tillhandahålls i banken.
* Manuellt genom att använda funktionen **Föreslå rader** för att fylla i raderna med transaktioner för fakturor som har utestående utbetalningar.

När värdet i fältet **Totalt saldo** i rutan **Bankutdragsrader** är lika med värdet i fältet **Saldo att stämma av** i rutan **Bankkontotransaktioner** kan du välja åtgärden **Bokför** för att stämma av de kopplade bankkontotransaktionerna. Alla icke godkända bankkontotransaktioner kommer att stå kvar på sidan vilket innebär att betalningar som ska bearbetas för bankkonto inte återspeglas i det senaste bankkontoutdraget eller att några betalningar mottogs via checkar.

> [!NOTE]  
>   Om kontoutdragrader hör till checktransaktioner, kan du inte använda de matchningsfunktionerna. I stället måste du välja åtgärden **Koppla trans.** och sedan välja den relevanta checktransaktionen att matcha kontoutdragraden med.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Så här fyller du i bankavstämningrader genom att importera ett kontoutdrag
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bankkontoavstämning** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Välj ett bankkonto i fältet **Bankkontonr**. Bankkontotransaktionerna som finns på bankkonto, visas i rutan **Bankkontotransaktioner**.
4. Ange datumet på kontoutdraget från banken i fältet **Kontoutdragets datum**.
5. Ange saldot på kontoutdraget från banken i fältet **Kontoutdragets slutsaldo**.
6. Om du har en bankutdragsfil väljer du åtgärden **Importera bankutdrag**.
7. Leta upp filen och välj sedan knappen **Öppna** för att importera banktransaktionerna till raderna på sidan **Bankkontoavstämning**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Så här fyller du i bankavstämningrader med funktionen Föreslå rader
1. På sidan **Bankkontoavstämning** väljer du åtgärden **Föreslå rader**.
2. Ange det tidigaste bokföringsdatumet för transaktionsavstämningen i fältet **Startdatum**.
3. Ange det senaste bokföringsdatumet för transaktionsavstämningen i fältet **Slutdatum**.
4. Om du vill att föreslå checktransaktion istället för bankkontotransaktioner markerar du kryssrutan **Ta med checkar**.
5. Välj **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Så här matchar du automatiskt kontoutdragrader med bankkontotransaktioner
Sidan erbjuder automatiska matchande funktioner som ska användas för betalningar till deras relaterade öppna transaktioner på en matchande text på bankutdragsraden (vänster ruta) med text på en eller flera redovisningstransaktioner för bankkontot (höger ruta). Observera att du kan skriva över de föreslagna automatiska applikationerna och du kan välja att inte använda automatiska applikationer alls. Mer information finns i nästa procedur:

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

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Så här skapar du saknade transaktioner för att matcha med banktransaktioner
Ibland kan det hända att ett kontoutdrag från banken innehåller belopp som motsvarar en avgift eller räntekostnad. Sådana banktransaktioner kan inte matchas, eftersom inga relaterade transaktioner finns i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du måste sedan bokföra en journalrad för varje transaktion för att skapa en artikelrelaterad transaktion som den kan matchas med.

1. På sidan **Bankkontoavstämning** väljer du åtgärden **Överföring till redovisningsjournal**.  
2. På sidan **Bankavst. trans. åt redov.jnl** anger du vilka redovisningsjournalen om du vill använda och klickar på knappen **OK**.

    Sidan **Redovisningsjournal** öppnas med nya journalrader för alla bankrapportrader med saknade transaktioner.
3. Fyll i journalraden med information, till exempel motkonton. Mer information finns i [Arbeta med Redovisningsjournaler](ui-work-general-journals.md).  
4. Välj åtgärden **Testrapport** - om du vill granska resultatet av bokföringen innan du bokför. Rapporten **bankkontoutdrag** öppnas och visar samma fält som rubrik på sidan **Bankkontoavstämning**.
4. Välj åtgärden **Bokföra**.

    När transaktionen har bokförts går du vidare och matchar bankkontotransaktionen med den.
5. Uppdatera eller öppna sidan **Bankkontoavstämning** igen. Den nya transaktionen ska visas i fönstret **Bankkontotransaktioner**.
6. Matcha kontoutdragraden till bankkontotransaktionen, antingen manuellt eller automatiskt.

## <a name="see-also"></a>Se även
[Hantera bankkonton](bank-manage-bank-accounts.md)  
[Ställa in bankverksamhet](bank-setup-banking.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

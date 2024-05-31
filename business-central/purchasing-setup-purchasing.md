---
title: Översikt över uppgifter för att ställa in inköp
description: Beskriver uppgifterna för att definiera företagets inköppolicyer och registrerar inköpsprocesserna.
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Ställa in inköp

Innan du kan hantera inköpsprocesser måste du konfigurera reglerna och värdena som definierar företagets inköpspolicyer.

Du måste definiera den allmänna konfigurationen på sidan **Konfiguration av inköp och leverantörsreskontra**, som vanligtvis utförs en gång under den första implementeringen. Läs mer i följande avsnitt, [Konfiguration av inköp och leverantörsreskontra](#purchases-and-payables-setup).

En separat serie uppgifter relaterade till att registrera nya leverantörer är att registrera alla specialpriser eller rabattavtal som du har med varje leverantör.

Finansrelaterade inköp, till exempel betalningssätt och valutor, beskrivs i avsnittet för finanskonfiguration. Läs mer i [Ställa in finanser](finance-setup-finance.md). På samma sätt kan lagerrelaterade inköpsinställningar, till exempel enheter och artikelspårningskoder, finnas i [avsnittet lagerinställningar](inventory-setup-inventory.md).

## Konfiguration av inköp och leverantörsreskontra

Innan du arbetar med inköp och leverantörsreskontra går du till sidan **Konfiguration av inköp och leverantörsreskontra** och anger hur inköpsvärden bokförs och de nummerserier som används för dokument om leverantörer och inköp.

### Allmänna inställningar

På snabbfliken **Allmänt** väljer du alternativ för t.ex. hur rabatter ska beräknas och bokföras samt hur fakturor ska avrundas. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Vissa fält kräver särskild uppmärksamhet, till exempel fältet **Beräkna fakturarabatt per moms/moms-ID**, vilket anger om fakturarabatten beräknas enligt skatteidentifieraren eller fakturasumman. Läs mer på [Kombinera momsbokföringsmallar i momsbokföringsinställningarna](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

På samma sätt kan fältet **Appln. mellan valutor** leda till små avrundningsskillnader vid koppling av transaktioner i olika valutor till varandra. Läs mer på [Aktivera koppling av kundreskontratransaktioner till olika valutor](finance-how-enable-application-ledger-entries-different-currencies.md)

Vissa fält ändrar också beteendet eller beror på hur andra fält är inställda. Till exempel påverkas funktionen **Kontrollera förskottsbetalning vid bokföring** av hur fältet **Automatisk uppdatering av förskottsbetalning** är inställt för kontroll av väntande förskottsbetalningar.

Läs mer om fälten [**Ext. Dok.nr obligatoriskt**](#external-document-number) och [**Exakt kostnadsåterföring**](#exact-cost-reversing) nedan.

### Inställningar för nummerserier

På snabbfliken **Nummerserier** måste du definiera unika identifieringskoder som ska användas för leverantörer, fakturor och andra inköpsdokument. Numrering är viktig inte enbart för interna processer, men kan också behöva följa lokala regler. Det kan vara värt att ställa in alla serier på sidan **Nr-serier** på förhand, istället för att skapa nya från **Konfiguration av inköp och leverantörsreskontra**. Läs mer i [Skapa nummerserier](ui-create-number-series.md).

## Externt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Exakt kostnadsåterföring

Funktionen **Exakt kostnadsåterföring** bidrar till att säkerställa att returnerade varor värderas till samma kostnad som när de ursprungligen togs ur lagret, med hjälp av en fast applikation istället för att följa ett genomsnitt eller en först in, först ut-metod. Mer information finns i avsnittet [Designdetaljer: Fast applikation](design-details-item-application.md#fixed-application). Om en extra kostnad senare läggs till det ursprungliga inköpet uppdateras värdet på inköpsreturen i enlighet därmed.

Med funktionen aktiverad kan en returtransaktion endast bokföras genom att ange löpnumret för artikeltransaktionen i fältet **Koppla till artikellöpnr** på inköpsreturorderraden. Som standard visas inte fältet på snabbfliken **Rader**. Lär dig hur du lägger till fält till sidor i avsnittet [Anpassa arbetsytan](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Fler inköpsinställningar

| Till | Gå till |
| --- | --- |
| Skapa ett leverantörskort för varje leverantör som du har köpt av. |[Registrera nya leverantörer](purchasing-how-register-new-vendors.md) |
| Prioritera leverantörer. |[Prioritera leverantörer](purchasing-how-prioritize-vendors.md) |
| Ange bankkontoinformation&mdash;inklusive IBAN (International Bank Account Number) och SWIFT-koder&mdash;på leverantörens kort. | [Skapa bankkonton för leverantörer](purchasing-how-set-up-vendors-bank-accounts.md) |
| Skapa inköpare, tilldela leverantörer och koder för att spåra statistik. |[Konfigurera inköpare](purchasing-how-setup-purchasers.md) |
| Ange de olika rabatterna och specialpriserna som leverantörerna beviljar dig beroende på artikel, kvantitet och/eller datum. |[Registrera inköpspris, rabatt och betalningsavtal](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definiera vad du betalar för de artiklar och tjänster som köpts av ditt företag.  | [Ställa in priser och rabatter](across-prices-and-discounts.md) |
| Skapa standardrader som ska infogas på återkommande inköpsdokument. | [Ställ in återkommande inköpsrader](purchasing-how-work-recurring-purchase-lines.md) |
| Skapa sekvenser av uppgifter för att ansluta processer som utförs av olika användare, till exempel begära och godkänna inköpsorder. | [Konfigurera arbetsflöden för godkännande av inköp](across-set-up-workflows.md) |
| Hantera affärsinteraktion med leverantörerna, importera mottagna fakturadokument och registrera nya leverantörer med hjälp av e-postklienten för Outlook. | [Konfigurera Business Central-tillägget för Outlook](admin-outlook.md) |
| Granska utgiftskvitton, konvertera papper och elektroniska dokument till journalrader och digitala pappersfakturor från leverantörer. | [Ställa in inkommande dokument](across-how-setup-income-documents.md) |
| Ange standardrapporter som ska användas för olika dokumenttyper. |[Rapportval i Business Central](across-report-selections.md)|
|Ange om användare tillåts bokföra inköpsfakturor och om de måste bokföra tillsammans med en leverans. |[Definiera en bokföringspolicy för faktura för användare](admin-setup-invoice-posting-policy.md)|

## Se även

[Inköp](purchasing-manage-purchasing.md)  
[Översikt över installation](setup.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

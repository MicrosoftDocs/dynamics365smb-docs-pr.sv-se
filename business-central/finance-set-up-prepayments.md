---
title: Ställa in förskottsbetalningar | Microsoft Docs
description: Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen. Du kan till exempel kräva en deposition innan du tillverkar artiklar mot order eller också kan du kräva betalning innan du levererar artiklar till en kund. Med hjälp av funktionen för förskottsbetalning kan du fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer. På så sätt kan du se till att alla betalningar bokförs mot en faktura.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: prepayment
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: e8a6e0834b259358de5c07d3f83a7b5477a0d3a7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931989"
---
# <a name="set-up-prepayments"></a>Konfigurera förskottsbetalningar
Om du vill att din kund ska betala innan ni levererar till dem eller om er leverentör kräver att ni betalar innan dem levererar till er kan du använda Förskottsbetalningsfunktionen Funktionen låter dig fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer och för att säkerställa att alla delbetalningar bokförs mot en faktura. För mer information, se [Skapa förskottsfakturor](finance-how-to-create-prepayment-invoices.md).

Innan du kan bokföra förskottsfakturor måste du skapa bokföringskonton i redovisningen och ange nummerserier för förskottsbetalningsdokument.  

Du kan ange procentandelen av radbeloppet som ska faktureras som förskottsbetalning, för en kund eller leverantör, för alla artiklar eller valda artiklar. När du har gjort de nödvändiga inställningarna kan du skapa förskottsfakturor från försäljnings- och inköpsorder. Du kan använda standardprocentandelarna för varje försäljnings- eller inköpsrad eller ändra beloppet om det behövs. Till exempel, en totalsumma för hela ordern.  

Eftersom det förutbetalda beloppet hör till köparen ända tills han/hon har mottagit varan eller tjänsten måste du lägga upp redovisningskonton för förskottsbetalningarna tills slutfakturan är bokförd. Förskottsbet. för försäljning måste registreras på ett skuldkonto tills artiklarna är levererade. Förskottsbet. för inköp måste registreras på ett tillgångskonto tills artiklarna är levererade. Du måste dessutom skapa ett separat redovisningskonto för varje moms-ID.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Så här lägger du till konton för förutbetalda poster i bokföringsinställningarna  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Bokföringsinställningar** och välj sedan relaterad länk.
2. På sidan **Bokföringsinställningar** fyller du i följande fält:  

    - **Förskottsbet.konto, försäljning**  
    - **Förskottsbet.konto, inköp**  

Om du redan inte har konfigurerat redovisningskonton för förskottsbetalningarna kan du göra detta på sidan **Redovisningskontolista**.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Så här skapar du nummerserier för dokument för förskottsbetalning  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsinställningar** och välj sedan relaterad länk.
2. På sidan **Försäljningsinställningar** fyller du i följande fält:  

   - **Försk.fakt.nr.serie (bokförd)**
   - **Försk.kredit.nr.serie (bokförd)**

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Inköpsinställningar** och välj sedan relaterad länk.
2. På sidan **Inköpsinställningar** fyller du i följande fält:

    - **Försk.fakt.nr.serie (bokförd)**
    - **Försk.kredit.nr.serie (bokförd)**

> [!NOTE]  
>  Du kan använda samma nummerserier för förskottsfakturor och vanliga fakturor eller använda olika nummerserier. Om du använder olika serier får dessa inte överlappa, d.v.s. det får inte finnas några nummer som finns med i båda serierna.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Ställa in Procentandelar, förskottsbetalning för artiklar, kunder och leverantörer  
Du kan ställa in en artikels standardprocentandel för alla kunder, en specifik kund eller en kundprisgrupp.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Välj en artikel och välj sedan åtgärden **Procentandel för förskottsbet**.  
3. På sidan **Procentandelar, förskottsbetalning för försäljning** fyller du i följande fält: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan ställa in en kunds eller leverantörs standardprocentandel för förskottsbet. för alla artiklar och alla typer av försäljningsrader. Ange detta på kundkortet eller leverantörskortet.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kunder** och välj sedan relaterad länk.
2. Öppna kort för en kund.
3. Fyll i fältet **Förskottsbetalning %**.
4. Upprepa stegen för andra kunder eller för leverantörer.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Så här fastställer du vilken förskottsbetalda procentandel som har första prioritet  
En order kan ha en procentandel för en förskottsbet. i försäljningshuvudet och i olika procentandelar för artiklarna på raderna. Om du vill fastställa vilken förskottsbetald procentandel som kopplas till varje försäljningsrad letar systemet efter den förskottsbetalda procentandelen i följande ordning, och använder den första standardinställda det hittar:  
1. En procentandel för förskottsbet. för artikeln på raden och kunden som ordern är till.  
2. En procentandel för förskottsbet. för artikeln på raden och kundprisgruppen som kunden hör till.  
3. En procentandel för förskottsbet. för artikeln på raden för alla kunder.  
4. Procentandelen för förskottsbet. i försäljnings- eller inköpshuvudet.  

Procentandelen för förskottsbet. på kundkortet kommer således endast att användas om det inte finns en inställd procentandel för förskottsbet. för artikeln. Om du ändrar innehållet i fältet **Förskottsbetalning %** i försäljnings- eller inköpshuvudet efter att du har skapat raderna uppdateras den procentuella förskottsbetalningen. Detta gör det enkelt att upprätta en order med en fast procentandel för förskottsbet., utan att ta hänsyn till procentandelen som ställts in för artiklar.

## <a name="see-also"></a>Se även  

[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Beräkna moms på varor och tjänster på förskottsbetalningar i Australien](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Beräkna moms på varor och tjänster på förskottsbetalningar i Nya Zeeland](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Så här fungerar i redovisningen och kontoplanen](finance-general-ledger.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

---
title: Registrera inköp med inköpsfakturor
description: Beskriver hur du köper lager, icke-lagerartiklar eller andra resurser genom att skapa och bokföra inköpsfakturor eller order.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 09/07/2021
ms.author: edupont
ms.openlocfilehash: 18aef7bfc5324d17d2af9f4aa4ff0ba2602c70e0
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482403"
---
# <a name="record-purchases-with-purchase-invoices"></a>Registrera inköp med inköpsfakturor

Du skapar en inköpsfaktura eller inköpsorder för att registrera kostnaden för inköp och för att spåra leverantörsskulder. Om du vill kontrollera ett lager används inköpsfakturor eller inköpsorder också för att uppdatera lagernivåer dynamiskt, så att du kan minimera lagerkostnader och ge bättre service. Inköpskostnaderna, inklusive serviceutgifter, och lagervärde som kommer från bokföring av inköpsfakturor eller order bidrar till vinstsiffror och övriga ekonomiska nyckeltal i rollcentret.

## <a name="create-purchase-invoices"></a>Skapa inköpsfakturor

Förutom att köpa fysiska artiklar (artikeltypen **Lager**), som påverkar lagervärderingen, kan du köpa tjänster som representeras av tidsenheter. Du kan göra detta med antingen artikeltypen **Service** eller med radtypen **Resurs**.

När du tar emot lagerartiklarna, eller när den inköpta tjänsten avslutas, bokför du inköpsfakturan eller ordern för att uppdatera lager och finansiella transaktioner, samt för att aktivera betalning till leverantören utifrån betalningsvillkoren. Mer information finns i [Bokföra inköp](ui-post-purchases.md) och [Utföra betalningar](payables-make-payments.md).

> [!CAUTION]  
> Bokför inte en inköpsfaktura för fysiska artiklar förrän du tar emot artiklarna och vet slutkostnaden för inköpet, inklusive eventuella extrakostnader. Annars kan lagervärdet och vinstsiffrorna ha oriktiga resultat.

### <a name="to-create-a-purchase-invoice"></a>Skapa en inköpsfaktura

Nedan beskrivs hur du skapar en inköpsfaktura. Momenten är liknande för en inköpsorder. Den största skillnaden är att inköpsorder har ytterligare fält och åtgärder för fysisk hantering av artiklar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Ange namnet på en befintlig leverantör i fältet **Leverantör**.

    Andra fält på sidan **Inköpsfaktura** fylls nu i med standardinformation om den valda leverantören. Om leverantören inte är registrerad, gör så här:

    1. Ange namnet på en ny leverantör i fältet **leverantör**.
    2. Välj knappen **ja** i dialogrutan om registrering av den nya leverantören.
    3. Mer information om hur du fyller i leverantörskortet finns i [Registrera nya leverantörer](purchasing-how-register-new-vendors.md).  
    4. Välj **OK** för att gå tillbaka till sidan **Inköpsfaktura**, när du har slutfört leverantörskortet.

3. På sidan **Inköpsfaktura** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Fortsätt nu med att fylla inköpsfakturaraderna med artiklar eller resurser som du har köpt från leverantören.

    > [!NOTE]  
    > Om du har ställt in återkommande inköpsrader för leverantöre, till exempel en månatlig återanskaffningsorder, kan du infoga dessa rader på fakturan, genom att välja knappen **Hämta återkommande inköpsrader**.
4. Ange numret på en lagerförd artikel eller service på snabbfliken **Rader** Snabbfliken, i **Artikelnr** fältet.
5. Ange hur många artiklar som ska införskaffas i fältet **Antal**.

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Inköpspris** multiplicerat med värdet i fältet **Kvantitet**.

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på leverantörskortet.

    Fälten för summor under raderna uppdateras automatiskt när du skapar eller ändrar rader för att visa de belopp som ska bokföras i redovisningen.

6. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms** längst ned på fakturan.

    > [!NOTE]  
    > Om du har ställt in fakturarabatter för leverantören, då infogas det angivna procentsatsvärdet automatiskt i fältet **Leverantörsfakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Fakturarabattbelopp**.
7. Välj **Bokför** när du tar emot de beställda artiklarna eller tjänster.

Inköpet visas nu i lager, resurstransaktioner och ekonomiska transaktioner, och leverantörsbetalningen aktiveras. Inköpsfakturan tas bort från listan över inköpsfakturor och ersätts med ett nytt dokument i listan över bokförda inköpsfakturor.  

> [!NOTE]
> I sällsynta fall kan de bokförda beloppen avvika från vad som visas i fälten för summor. Det beror vanligtvis på att du avrundar beräkningar när det gäller moms.
>
> Om du vill kontrollera vilka belopp som faktiskt bokförs, kan du använda sidan **Statistik** sidan som tar hänsyn till de avrundade beräkningarna. Om du väljer åtgärden **Släpp** kommer fälten för summor dessutom att uppdateras så att de omfattar de avrundade beräkningarna.

## <a name="when-to-use-purchase-orders"></a>När inköpsorder ska användas

Du måste använda inköpsorder om din inköpsprocess kräver att du t. ex. kan registrera delleveranser av en orderkvantitet eftersom hela kvantiteten inte var tillgänglig hos leverantören. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda inköpsorder. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar inköpsorder på samma sätt som inköpsfakturor. Följande procedur är baserad på en inköpsfaktura. Momenten är liknande för en inköpsorder.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="selling-non-inventory-items"></a>Sälja artiklar som inte finns i lager

Artiklarna på en inköpsorder kan vara av typen **Lager**, **Service**, **Resurs** eller **Inte i lager** för att ange om artikeln är en fysisk lagerenhet, en arbetstidsenhet eller en fysisk enhet som inte hålls i lager. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md). Inköpsfakturaprocessen är samma för alla tre artikeltyper.

> [!NOTE]
> Med inköpsradtypen **Resurs** kan du också köpa externa resurser, till exempel i syfte att fakturera en leverantör för utfört arbete. Mer information finns i [Ange resurser](projects-how-setup-resources.md).
>
> Om du vill använda en inköpt resurs kan du komma att behöva ange resursens kapacitet och tilldela denna manuellt till ett projekt. När du köper en resurs skapas reskontratransaktion – reskontratransaktioner för resurs spåras emellertid inte för mängd och värde på samma sätt som för exempelvis artiklar. Om antals- och värdespårning krävs kan du använda andra radartikeltyper.

## <a name="posted-invoices"></a>Bokförda fakturor

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Det är enkelt att korrigera eller annullera en bokförd inköpsfaktura innan du betalar leverantören. Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen. Mer information finns i [Korrigera eller annullera obetalda inköpssfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Om du redan har betalt för artiklar eller tjänster på den bokförda inköpsfakturan måste du skapa en inköpskreditnota för att återföra köpet. Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

[Öppna listan **bokförda inköpsfakturor**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Externt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Konfigurera resurser](projects-how-setup-resources.md)  
[Bokföra inköp](ui-post-purchases.md)  
[Begär offerter](purchasing-how-request-quotes.md)  
[Köpa artiklar för en försäljning](purchasing-how-purchase-products-sale.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Förbereda direktutleveranser](sales-how-drop-shipment.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
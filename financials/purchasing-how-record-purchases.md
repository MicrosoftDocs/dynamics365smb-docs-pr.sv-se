---
title: "Skapa en inköpsfaktura och registrera inköp | Microsoft Docs"
description: "Beskriver hur du köper lager- och serviceartiklar genom att skapa och bokföra inköpsfakturor eller order."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e0d7908509879bec6890b9791e420fc90b0026d2
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="record-purchases"></a>Registrera inköp
Du skapar en inköpsfaktura eller inköpsorder för att registrera kostnaden för inköp och för att spåra leverantörsskulder. Om du vill kontrollera ett lager används inköpsfakturor eller inköpsorder också för att uppdatera lagernivåer dynamiskt, så att du kan minimera lagerkostnader och ge bättre service. Inköpskostnaderna, inklusive serviceutgifter och lagervärden som kommer från bokföring av inköpsfakturor eller order bidrar till vinstsiffror och övriga ekonomiska nyckeltal på din startsida.

> [!NOTE]  
>   Du måste använda inköpsorder om din inköpsprocess kräver att du t.ex. kan registrera delleveranser av en orderkvantitet eftersom hela kvantiteten inte var tillgänglig hos leverantören. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda inköpsorder. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md). I alla andra aspekter fungerar inköpsorder på samma sätt som inköpsfakturor. Följande procedur är baserad på en inköpsfaktura. Momenten är liknande för en inköpsorder.

När du tar emot lagerartiklarna, eller när den inköpta tjänsten avslutas, bokför du inköpsfaktura eller order för att uppdatera lager och finansiella transaktioner och för att aktivera betalning till leverantören utifrån betalningsvillkoren. Mer information finns i [Gör betalningar](payables-make-payments.md).

> [!CAUTION]  
>   Bokför inte en inköpsfaktura förrän du tar emot artiklarna och vet slutkostnaden för inköpet, inklusive eventuella extrakostnader. Annars kan lagervärdet och vinstsiffrorna ha oriktiga resultat.

Det är enkelt att korrigera eller annullera en bokförd inköpsfaktura innan du betalar leverantören. Det är användbart om du vill rätta till ett skrivfel eller om du vill ändra inköpet tidigt i orderprocessen. Mer information finns i [Korrigera eller annullera obetalda inköpssfakturor](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Om du redan har betalt för artiklarna på den bokförda inköpsfakturan, måste du skapa en inköpskreditnota för att återföra köpet. Mer information finns i [Så här behandlar du inköpsreturer eller annulleringar](purchasing-how-process-purchase-returns-cancellations.md).

Artiklar kan vara av typen **lager** eller **tjänst**. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md). Inköpsfakturaprocessen är samma för båda artikeltyper.

Du kan fylla i leverantörsfälten på inköpsfakturan på två sätt, beroende på om leverantören redan har registrerats.

## <a name="to-create-a-purchase-invoice"></a>Skapa en inköpsfaktura
1. Välj åtgärden **Inköpsfaktura** på startsidan.  
2. Ange namnet på en befintlig leverantör i fältet **Leverantör**.

    Andra fält i fönstret **Inköpsfaktura** fylls nu i med standardinformation om den valda leverantören. Om leverantören inte är registrerad, gör så här:
3. Ange namnet på en ny leverantör i fältet **leverantör**.
4. Välj knappen **ja** i dialogrutan om registrering av den nya leverantören.
5. Välj en mall det nya leverantörskortet ska baseras på i fönstret **Välj en mall för en ny leverantör** och välj sedan knappen **OK**.
6. Ett nytt leverantörskort öppnas med förifylld information från den markerade leverantörsmallen. Fältet **Namn** förifylls med nya leverantörens namn som du har angett på inköpsfakturan.
7. Fortsätt att fylla de återstående fälten på leverantörskortet. Mer information finns i [Registrera nya leverantörer](purchasing-how-register-new-vendors.md).  
8. Välj **OK** för att gå tillbaka till fönstret **Inköpsfaktura**, när du har slutfört leverantörskortet.

    Flera fält i fönstret **Inköpsfaktura** är ifyllda med information som du har angett på det nya leverantörskortet.
9. I fönstret **Inköpsfaktura** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Fortsätt med att fylla inköpsfakturaraderna med lagerförda artiklar eller tjänster som du har köpt från leverantören.

    > [!NOTE]  
>   Om du har ställt in återkommande inköpsrader för leverantöre, till exempel en månatlig återanskaffningsorder, kan du infoga dessa rader på fakturan, genom att välja knappen **Hämta återkommande inköpsrader**.
10. Ange numret på en lagerförd artikel eller service på snabbfliken **Rader** Snabbfliken, i **Artikelnr** fältet.
11. Ange hur många artiklar som ska införskaffas i fältet **Antal**.

    > [!NOTE]  
>   För artiklar av typen **Tjänst** är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden.

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Inköpspris** multiplicerat med värdet i fältet **Kvantitet**.

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på leverantörskortet.
12. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms** längst ned på fakturan.

    > [!NOTE]  
>   Om du har ställt in fakturarabatter för leverantören, då infogas det angivna procentsatsvärdet automatiskt i fältet **Leverantörsfakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Fakturarabattbelopp**.
13. Välj **Bokför** när du tar emot de beställda artiklarna eller tjänster.

Inköpet visas nu i lager och ekonomiska transaktioner, och leverantörsbetalning aktiveras. Inköpsfakturan tas bort från listan över inköpsfakturor och ersätts med ett nytt dokument i listan över bokförda inköpsfakturor.

## <a name="see-also"></a>Se även
[Inköp](purchasing-manage-purchasing.md)  
[Ställa in inköp](purchasing-setup-purchasing.md)  
[Begär offerter](purchasing-how-request-quotes.md)  
[Köpa artiklar för en försäljning](purchasing-how-purchase-products-sale.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Förbereda direktutleveranser](sales-how-drop-shipment.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


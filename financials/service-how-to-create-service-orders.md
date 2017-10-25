---
title: "Så här skapar du Serviceorder | Microsoft Docs"
description: "Du kan använda fönstret **Serviceorder** för att skapa dokument där du anger information om service, som reparation och underhåll, på serviceartiklar efter kundkrav."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cb514fe04fd70836f640d3db4ea592680ab0fa1a
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-orders"></a>Så här skapar du serviceorder
Du kan använda fönstret **Serviceorder** för att skapa dokument där du anger information om service, som reparation och underhåll, på serviceartiklar efter kundkrav.  
  
När du skapar en serviceorder, behöver du bara fylla i några fält. En del fält är valfria och många fylls i automatiskt, när du fyller i fälten.  
  
## <a name="to-create-a-service-order"></a>Så här skapar du en serviceorder    
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceorder** och välj sedan relaterad länk.  
2. Skapa en ny serviceorder.  
3. I fältet **Nr.** anger du ett nummer för serviceordern.  
  
     Om du har angett nummerserier för serviceorder i fönstret **Serviceinställningar** trycker du på Retur, så väljs nästa tillgängliga serviceordernummer.  
  
4. I fältet **Kundnr.** välj relevant kund i listan. Relevanta fält för kunden fylls då i automatiskt med information från tabellen **Kund**.  
  
5. Beroende på inställningarna på snabbfliken **Obligatoriska fält** om ska finnas i fönstret **Serviceinställningar** kanske du måste fylla i fältet **Serviceordertyp** på fältet **Säljarkod**.  
6. Det är frivilligt att fylla i övriga fält.  
7. Registrera serviceartikelraderna.  

## <a name="to-create-a-service-order-from-a-contract"></a>Så här skapar du en serviceorder från ett kontrakt  
Du kan automatiskt skapa serviceorder för underhåll av serviceartiklar baserat på ett servicekontrakt.  
  
1. Välj ikonen ![söka efter sida eller rapport](media/ui-search/search_small.png "ikonen söka efter sida eller rapport"), ange **Skapa serviceorder** och välj sedan relaterad länk.  
2. På snabbfliken **Servicekontraktshuvud** anger du de filter som du vill koppla.  
3. Gå till snabbfliken **Alternativ** och fyll i fälten **Startdatum** och **Slutdatum** med startdatum och slutdatum för den period du vill skapa kontraktserviceorder för. I batch-jobbet skapas serviceorder som omfattar serviceartiklar i servicekontrakt med nästa planerade servicedatum inom den här perioden.  
  
    > [!NOTE]  
    >  Det finns en gräns för det maximala antalet dagar du kan använda som datumintervall när du kör batch-jobbet. Du anger den här gränsen i **Kontrakt serv.order max. dagar** i fönstret **Serviceinställningar**.  
  
4. I fältet **Åtgärd** klickar du på **Skapa serviceorder**.  

## <a name="to-convert-a-service-quote-to-a-service-order"></a>Så här omvandlar du serviceofferter till serviceorder
När en kund har accepterat en serviceoffert kan du omvandla den till en serviceorder. Offerten tas bort från fönstret och en ny serviceorder skapas med samma beskrivning som serviceofferten. Svarsdatum och svarstid räknas om för serviceordern och dess status anges som **Förestående**. Reparationsstatus för serviceartiklarna i ordern ändras till **Initial**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] En sökning görs efter  för alla serviceartiklar i serviceofferten som har statusen **Aktiv**. Om sådana fördelningstransaktioner hittas ändras deras fördelningsstatus till **Omfördelning nödvändig**. När du omfördelar serviceartiklarna på serviceordern ändras status för de fördelningstransaktioner som är registrerade för offerten till **Avslutad**.   

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Servicekontraktsofferter** och välj sedan relaterad länk.  
2. Välj den serviceoffert som du vill omvandla till en serviceorder.  
3. Välj åtgärden **Skapa order**.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>Så här kontrollerar du artikeldisposition för en eller flera order  
Du kan kontrollera om en artikel som du behöver för att uppfylla en order finns i lager. Om inte kan du se när artikeln finns i lager. Dessutom, om en artikel är disponibel att reservera kan du reservera den för att se till att den är tillgänglig för dig. Du kan kontrollera tillgängligheten för en viss order eller för alla order.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Beordringstavla** och välj sedan relaterad länk.  
2. Gör något av följande:  
  
    * Välj ordningen för en viss order och välj åtgärden **Behovsöversikt**.  
    * Välj för alla order **visa dokument**. Fönstret **Serviceorder** öppnas.  
  
3. Expandera artikelgruppen och visa information om tillgänglig kvantitet av artikeln på sidan **Behovsöversikt**. Du kan t.ex. se hur många artiklar som finns i lager. Du kan också se om och när en artikel blir tillgänglig, om den är restnoterad, dvs. ursprungstyp = inköp eller om den har reserverats. 

## <a name="to-reserve-an-item-for-a-service-order"></a>Så här reserverar du artiklar för serviceorder
Om du behöver vara säker på att en artikel är tillgänglig för en serviceorder kan du reservera artikeln. 

1. I rutan **Sök** anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Välj serviceorder, och sedan **Redigera**.  
3. Välj **Åtgärder**, välj **Order**, och sedan **Servicerader**.  
4. På sidan **servicerader** väljer du artikeln som ska reserveras och väljer sedan åtgärden **reservera**.  
5. På sidan **Reservation** väljer du **reservera från aktuell rad**. 

## <a name="to-insert-lines-based-on-standard-service-codes"></a>Så här infogar du standardservicerader:  
Om du har ställt in standardservicekoder och tilldelat dem till serviceartikelgrupper kan du infoga de standardrader som är kopplade till standardservicekoderna i servicedokument. Mer information finns i [Så här skapar du en standardservicekod](service-how-setup-service-coding.md).   

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceorder** och välj sedan relaterad länk.  
2. Skapa en ny serviceorder.  
3. Fyll i fälten om det behövs.  
4. Fyll i serviceartikelraderna med den obligatoriska informationen.  
5. Markera raden med den serviceartikel som du vill skapa servicerader för och välj **Hämta std.servicekoder**. Fönstret **Standardgruppkoder för serviceartiklar** öppnas med standardkoderna för serviceartikelgruppen på raden.  
6. Välj lämplig kod och klicka på **OK** för att ange standardserviceraderna.  
  
> [!NOTE]  
>  Om fältet **Serviceartikelgruppkod** på serviceartikelraden i dokumentet är tomt, betyder det att serviceartikeln inte tillhör någon serviceartikelgrupp. I det här fallet innehåller fönstret **Standardgruppkoder för serviceartiklar** en lista över alla standardservicekoder. Du bör välja från listan för att automatiskt infoga standardservicerader i dokumentet. Du kan också välja från en lista över standardservicekoder som en viss serviceartikelgrupp tilldelats. Välj relevant kod i fältet **Serviceartikelgruppkod** i fönstret **Standardgruppkoder för serviceartiklar** om du vill visa listan.  

## <a name="to-register-internal-or-public-comments"></a>Så här registrerar du interna eller offentliga kommentarer
Du kan lägga till kommentarer som ska skrivas ut på serviceorder och serviceofferter för att ange ytterligare information. Du kan ange upp till 80 tecken inklusive blanksteg. Om du behöver fylla i fler tecken kan du göra det på nästa rad. Om du vill registrera en kommentar, väljer du en rad och väljer sedan åtgärden **kommentarer**.  

## <a name="to-delete-invoiced-service-orders"></a>Så här tar du bort fakturerade serviceorder  
Vanligtvis tas en order bort från programmet när den har fakturerats helt. När en faktura bokförs skapas en motsvarande transaktion i fönstret **Bokförda servicefakturor**. Det bokförda dokumentet kan visas från sidan **Bokförd servicefaktura**.  
  
Serviceordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från fönstret **Servicefaktura**, gäller följande. Då kan du behöva ta bort fakturerade order som inte har tagits bort. Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Ta bort fakturerade serviceorder** och välj sedan relaterad länk. Fönstret för batch-jobbsbegäran **Ta bort fakturerade serviceorder** öppnas.  
2. För att ange vilka order som ska tas bort kan du ställa in filter i fälten **Nr.**, **Kundnr.**, and **Faktureringskundnr.** .  
3. Välj **OK**.  


## <a name="see-also"></a>Se även  
[Servicebokföring](service-service-posting.md)  
[Så här bokför du serviceorder](service-how-to-post-service-orders.md)  
[Ställa in servicehantering](service-setup-service.md)  
[Så här arbetar du med serviceuppgifter](service-how-to-work-on-service-tasks.md)  
[Så här fördelar du resurser:](service-how-to-allocate-resources.md)  


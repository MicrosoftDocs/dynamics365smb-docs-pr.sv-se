---
title: Så här inlevererar du artiklar | Microsoft Docs
description: När artiklar tas emot i ett distributionslager som använder inleveransbearbetning måste du hämta raderna för det släppta källdokument som utlöste inleveransen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 038ecb0122e58cfdca3ff62ac93554fab01dcdb6
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786602"
---
# <a name="receive-items"></a>Ta emot artiklar

När artiklarna tas emot i ett distributionslager som har ställts in för distributionslagerinleveransen kan du bara registrera inleveransen med relaterade dokument, till exempel en inköpsorder, en försäljningsreturorder eller en order för ankommande överföringar.

När artiklar tas emot i ett distributionslager som använder inleveransbearbetning måste du hämta raderna för det släppta källdokument som utlöste inleveransen. Om du använder lagerplatser kan du antingen godta den standardlagerplats som fylls i eller, om artikeln inte har använts i det här lagret tidigare, fylla i den lagerplats där artikeln ska placeras. Sedan måste du fylla i antalet artiklar som har tagits emot och bokföra inleveransen.  

## <a name="to-receive-items-with-a-purchase-order"></a>För att inleverera artiklar med en inköpsorder.

Nedan beskrivs hur du inlevererar artiklar med en inköpsorder. Stegen är liknande för försäljningsreturorder och överföringsorder.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsorder** och välj sedan relaterad länk.
2. Öppna en befintlig inköpsorder eller skapa en ny. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).
3. Ange hur många enheter som har inlevererats i fältet **Inlevereras antal**.

  > [!NOTE]
  > Om mottagen kvantitet överstiger den som angetts i fältet **Kvantitet** på inköpsordern, och om leverantören har godkänt överskridande inleveranser, kan du använda fältet **Överskr. inleverans** för att hantera överskottet. Mer information finns i [Så här tar du emot fler artiklar än vad som beställts](warehouse-how-receive-items.md#to-receive-more-items-than-ordered).

4. Välj åtgärden **Bokföra**.

  Värdet i fältet **Inlevererat antal** uppdateras i enlighet därmed. Om detta är en delinleverans och värdet är lägre än värdet i fältet **antal**.

> [!NOTE]
> Om du använder ett distributionslagerdokument för att bokföra inleveransen kan du inte använda åtgärden **Publicera** på inköpsordern. I stället har en distributionslagerarbetare redan bokfört inköpsordermängden som inlevererad. För mer information, se [Ta emot artiklar med lagerinbetalning](warehouse-how-receive-items.md#to-receive-items-with-a-warehouse-receipt).

## <a name="to-receive-items-with-a-warehouse-receipt"></a>För att inleverera artiklar med en lagerinleverans.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Dist.lager inleveranser** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  

    Fyll i fälten på snabbfliken **Allmänt**. När du hämtar källdokumentrader, kopieras delar av informationen i huvudet till varje rad.  

    För dirigerad artikelinförsel och plockning: om lagerstället har en standardzon och standardlagerplats för inleveranser fylls fälten **Zonkod** och **Lagerplatskod** i automatiskt. Du kan dock ändra fälten vid behov.  

    > [!NOTE]  
    > Om du vill ta emot artiklar med klasskoder för distributionslager som skiljer sig från klasskoderna för lagerplatsen i fältet **Lagerplatskod** i dokumenthuvudet, måste du ta bort innehållet i fältet **Lagerplatskod** i huvudet innan du hämtar källdokumentets rader för artiklarna.  
3. Välj åtgärden **Hämta källdokument**. Sidan **Källdokument** öppnas.

    Från en ny eller öppen lagerinleverans eller lagerutleverans kan du använda sidan **Filter att hämta ursprungsdok.** för att hämta de släppta källdokumentraderna som anger vilka artiklar som ska in - eller utlevereras.

    1. Välj åtgärden **Filter för att hämta urspr.dok.**.  
    2. Du skapar ett nytt filter genom att ange en beskrivande kod i fältet **Kod** och väljer sedan åtgärden **Ändra**.  
    3. Definiera vilken typ av källdokumentrader som du vill hämta genom att fylla i relevanta filterfält.  
    4. Välj åtgärden **Kör**.  

    Alla relaterat källdokumentrader, som uppfyller filtervillkorna, infogas nu på sidan **Dist.lager inleverans** som du aktiverade från filterfunktionen.  

    Filterkombinationerna, vilka du definierar, sparas på sidan **Filter att hämta ursprungsdok.** tills nästa gång du behöver den. Du kan skapa ett obegränsat antal filterkombinationer. Du kan ändra villkor när som helst, genom att välja åtgärden **Ändra**.

4. Välj det källdokument som du vill inleverera artiklar för och klicka på knappen **OK**.  

    Raderna i källdokumentet visas på sidan **Distributionslagerinleverans**. **Ant. att inlevereras** är ifyllt med utestående antal på respektive rad, men du kan ändra antalet som behövs. Om du tar bort innehållet i fältet **Lagerplatskod** på snabbfliken **Allmänt** innan du hämtar raderna måste du fylla i en lämplig lagerplatskod på varje inleveransrad.  

    > [!NOTE]  
    >  Om du vill fylla i fältet **Ant. att inlevereras** på alla rader med noll, väljer du åtgärden **Ta bort ant. att inleverera**. Välj åtgärder **Fyll i auto. ant. att inleverera** för att fylla i det igen med det utestående antalet.  

    > [!NOTE]  
    >  Det går inte att inleverera fler artiklar än antalet, i **Utestående ant.** på källdokumentraden. Om du vill hämta fler artiklar, hämtar du ett annat källdokument som innehåller en rad för artikeln, genom att använda filterfunktionen för att hämta källdokument med aktuell artikel.  

5. Bokför lagerinleveransen. Fälten med antal i källdokumenten uppdateras automatiskt och artiklarna registreras som en del av företagets lager.  

Om du använder artikelinförsel för distributionslagret skickas inleveransraderna automatiskt till funktionen för artikelinförsel för distributionslager. Även om artiklarna har inlevererats kan de inte plockas förrän de har blivit införda. De inlevererade artiklarna identifieras som disponibelt lager först efter att artikelinförseln har registrerats.  

Om du inte använder artikelinförsel för distributionslagret utan i stället använder lagerplatser registreras artiklarnas införsel på den lagerplats som anges på källdokumentraden.  

> [!NOTE]  
> Om du använder funktionen **Bokför och skriv ut** både bokför du inleveransen och skriver ut en instruktion för artikelinförsel som talar om var artiklarna ska lagras.  
>
> Om du använder dirigerad artikelinförsel och plockning i ditt lagerställe används artikelinförselmallarna för att beräkna den bästa platsen för artiklarna. Detta skrivs sedan ut på artikelinförselinstruktionen.

## <a name="to-receive-more-items-than-ordered"></a>Så här tar du emot fler artiklar än vad som beställts

När du tar emot fler varor än vad du har beställt vill du kanske ta emot dem i stället för att annullera inleveransen. Det kan t.ex. vara billigare att behålla överskottet på lagret än att returnera det, eller så kan du erbjuda en rabatt för att behålla det.

### <a name="to-set-up-over-receipts"></a>Så här lägger du upp överinleveranser

Du måste definiera en procentsats som tillåter att den beställda kvantiteten överskrids vid inleverans. Du definierar detta under en överinleveranskod som innehåller procent satsen i fältet **Tolerans för överinleverans %**. Du kan sedan tilldela koden till korten för relevanta artiklar och/eller leverantörer.  

Nedan beskrivs hur du lägger upp och tilldelar en kod för överinleverans till en artikel. Momenten är liknande för en leverantör.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan tillhörande länk.
2. Öppna kortet för en artikel som du misstänker ibland kan levereras i större mängd än vad som har beställts.
3. Välj sökknappen i fältet **Kod för överinleverans**.
4. Välj åtgärden **Ny**.
5. På sidan **Koder för överinleverans** skapar du en eller flera nya rader som definierar olika principer för överinleverans. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Markera en rad och välj sedan knappen **OK**.

Koden för överinleverans tilldelas till artikeln. En inköpsorder eller distributionslagerinleverans för artikeln tillåter nu att du tar emot mer än det beställda antalet enligt den angivna toleransprocenten för överinleverans.

> [!NOTE]
> Du kan ställa in ett arbetsflöde för godkännande för att kräva att överinleveranser måste godkännas innan de kan hanteras. I så fall måste du markera kryssrutan **Godkännande krävs** på sidan **Koder för överinleverans**. Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).

### <a name="to-perform-an-over-receipt"></a>Så här utför du en överinleverans

På inköpsrader och distributionslagerrader används **Överinleveransmängd** för att registrera överlevererade kvantiteter, vilket innebär antal som överstiger värdet i fältet **Antal**, den beställda mängden.

När du hanterar ett överinleverans kan du antingen öka värdet i fältet **Ant. att inlevereras** till den faktiska inlevererade kvantiteten. Fältet **Överinleveranskvantitet** uppdateras då för att visa överskjutande antal. Du kan också ange överskjutande antal i fältet **Överinleveranskvantitet**. Fältet **Ant. att inlevereras** uppdateras då för att visa beställt antal plus överskjutande antal. Följande procedur beskriver hur du fyller i fältet **Ant. att inlevereras**.  

1. På en inköpsorder eller ett lagerinleveransdokument där inlevererad mängd överstiger den beställda anger du den faktiskt inlevererade mängden i fältet **Ant. att inlevereras**.

    Om ökningen ligger inom den tolerans som anges av den tilldelade koden för överinleverans uppdateras fältet **Överleveranskvantitet** för att visa det antal med vilket värdet i fältet **Antal** överskrids.

    Om ökningen överskrider den angivna toleransen är överinleverans inte tillåten. I så fall kan du undersöka om det finns en annan kod för överinleverans som gör detta möjligt. Annars kan endast den beställda kvantiteten tas emot, och den överskjutande kvantiteten måste hanteras på annat sätt, till exempel genom att returnera den till leverantören.

2. Bokför inleveransen på samma sätt som andra inleveranser.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller inte funktioner som automatiskt initierar den ekonomiska administrationen av överinleveranser. Du måste hantera detta manuellt i samråd med leverantören, till exempel genom att leverantören skickar en ny eller uppdaterad faktura.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Se även

[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

---
title: Tilldela artikelomkostnader till försäljning och inköp | Microsoft Docs
description: Om du vill att dina lagerartiklar ska läggas på extra kostnader, som till exempel frakt, fysisk hantering, försäkring och transport som förekommer vid inköp eller försäljning av artiklar, kan du använda funktionen för artikelomkostnader.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost, landed cost
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dbf96c4f09c82bf409c0e082b6df116f3563402f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773786"
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Använda artikelomkostnader till kontot för ytterligare verksamhetskostnader
Om du vill säkerställa korrekt värderingmåste dina lagerartiklar läggas på extra kostnader, som till exempel frakt, fysisk hantering, försäkring och transport som förekommer vid inköp eller försäljning av artiklar. För inköp kommer lossningsavgiften för en inköpt artikel bestå av leverantörens inköpspris och samtliga artikelomkostnader som kan kopplas till enskilda inleveranser eller returutleveranser. För försäljning kan det vara lika betydelsefullt för företaget att känna till leveranskostnader för sålda artiklar som att veta inköpskostnader inklusive hemtagningskostnader för inköpta artiklar.

Förutom att registrera den ökade kostnaden till ditt lagervärde kan du använda funktionen artikelomkostnader för följande:

- Identifiera lossningsavgiften för en artikel för att kunna fatta bättre beslut om hur distributionsnätverket ska optimeras.
- Bryta ned och analysera en artikels styckkostnad/styckpris.
- Inkludera prisavdrag i inköpspris och försäljningspris.

Innan du kan tilldela artikelomkostnader måste du ställa in artikelomkostnadsnummer för de olika typerna av artikelomkostnader, inklusive på vilka konton kostnader som är knutna till försäljning, inköp och lagerjusteringar ska bokföras. Ett artikelomkostnadsnummer definierar du en kombination av produktbokföringsmall, skattegruppskod, artikelomkostnad och produktbokföringsmall för moms. När du skriver in det här artikelomkostnadsnumret i ett inköps- eller försäljningsdokument hämtas ett relevant redovisningskonto baserat på inställningen av artikelomkostnadsnumret och den information som lagrats i respektive dokumentet.

För både inköps- och försäljningsdokument, kan du tilldela en artikelomkostnad på två sätt:
- På det ursprungliga försäljningsdokumentet där artiklarna som artikelomkostnaden är kopplad till listas. Detta gör du vanligtvis för dokument som inte ännu har bokförts helt.
- På en separat faktura genom att koppla artikelomkostnaden till bokförda inleveranser eller utleveranser där de artiklar som artikelomkostnaden är kopplad till visas.

> [!NOTE]  
>   Du kan tilldela artikelomkostnader till order, fakturor och kreditnotor för försäljning och inköp. I följande procedurer beskrivs hur du arbetar med artikelomkostnader för en inköpsfaktura. Stegen är liknande för alla andra ingående och utgående dokument.

## <a name="example"></a>Exempel
Det här videoklippet visar hur du hanterar ytterligare leveranskostnader som en del av lagerkostnad.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Så här skapar du artikelomkostnadsnummer
Artikelomkostnadsnummer används för att skilja mellan olika typer av artikelomkostnader som används för inköpsdokument i företaget.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **artikelomkostnader** och välj sedan relaterad länk.
2. På sidan **Artikelomkostnader** väljer du åtgärden **Ny** åtgärder för att skapa en ny rad.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>För att tilldela artikelomkostnader direkt till inköpsfakturan för artikeln
Om du vet artikelomkostnaderna vid den tidpunkten när du bokför en inköpsfaktura för artikeln, följer du nedanstående instruktioner.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan relaterad länk.
2. Skapa en ny inköpsfaktura. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).
3. Kontrollera att inköpsfakturan har en eller flera rader av typen artikel.
4. På en ny rad , i fältet **Typ** väljer du **Omkostnad (artikel)**.
5. Ange hur många enheter av artikelomkostnaden som du fakturerats för i fältet **Antal**.
6. Ange beloppet för artikelomkostnaden i fältet **Inköpspris**.
7. Fyll i återstående fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    I följande steg gör du den faktiska fördelningen. Tills artikelomkostnaden tilldelas helt, är värdet i fältet **Ant. att distribuera** i rött.
8. På fliken **Rader** väljer du **Art.omkost.fördelning**.

    Sidan **art.omkost.fördelning** öppnas med en rad för varje rad av typartikel på försäljningsfakturan. Om du vill tilldela artikelomkostnaden till en eller flera rader, använder du en funktion som tilldelar och distribuerar den automatiskt eller manuellt fyller i fältet **Ant. att distribuera**. Följande steg beskriver hur du använder funktionen Föreslå art.omkost.fördelning.

9. På sidan **art.omkost.fördelning** väljer du åtgärden **Föreslå art.omkost.fördelning**.
10. Om det finns flera fakturarader av typen artikel, väljer du ett av fyra distributionsalternativ.  

Om artikelomkostnaden tilldelas helt, är värdet i fältet **Ant. att distribuera** på inköpsfakturan noll.

Artikelomkostnaderna har nu tilldelats till inköpsfakturan. När du bokför inleveransen av inköpsfakturan uppdateras artiklarnas lagervärden med kostnaden för artikelomkostnaden.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>För att tilldela artikelomkostnader från en separat faktura till inköpsfakturan för artikeln
Om du har fått en faktura för artikelomkostnaden när du har bokfört ursprungligt inleverans, följer du nedanstående instruktioner.
1. Upprepa steg 1 till och med 8 i [Koppla artikelomkostnader direkt till inköpsfakturan för artikeln](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. På sidan **Art.omkost.fördelnin** väljer du åtgärden **Hämta inleveransrader**.
3. På sidan **Inköp inleveransrader** väljer du artikelomkostnaden till bokförda inleveransen av artiklar som ska tilldelas artikeln och klickar på knappen **OK**.
4. Välj åtgärden **Föreslå art.omkost.fördelning**.

Artikelomkostnader på den separata inköpsfakturan har nu tilldelats till artikeln på den bokförda inleveransraden, därför uppdateras artikelns lagervärde med kostnaden för artikelomkostnaden.

## <a name="see-also"></a>Se även
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
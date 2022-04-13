---
title: Hantera projektleveranser
description: Beskriver olika sätt hur du hanterar försörjning och inköp av material och tjänster för projekt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.search.form: 98, 1020
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 5683baf005fe8dc89cf5f133f790e5682fb5c173
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516594"
---
# <a name="manage-job-supplies"></a>Hantera projektleveranser
Att hantera projektleveranser av artiklar, tjänster och utgifter är en viktig del och aspekt av allt projektgenomförande. Du kan använda lagerantal eller göra projektspecifika inköp med hjälp av inköpsorder eller inköpsfakturor. Ett servicejobb för en dator kan till exempel kräva en ny hårddisk. Du skapar då en inköpsfaktura för att köpa en ny hårddisk och registrerar det i projektet.

Om inköpsprocessen inte kräver att den fysiska transaktionen registreras separat kan ett inköp registreras endast i en inköpsfaktura eller på sidan **Projektredovisningsjournal**. Mer information finns i [Så här bokför du en projektrelaterad utgift](projects-how-manage-project-supplies.md#to-post-a-job-related-expense).

## <a name="to-purchase-items-or-services-for-a-job"></a>Köpa artiklar eller tjänster till ett projekt
Efterföljande procedur visar hur du använder en inköpsfaktura för att köpa produkter till ett projekt. Samma steg gäller när du använder en inköpsorder.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll i fälten efter behov. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).
3. I fälten **Projektnr.** och **Projektaktivitetsnr.** väljer du informationen för det projekt som du vill köpa artiklar eller tjänster för. Använd anpassningsverktygen om ett fält inte syns. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

    Värdet som du väljer i fältet **Projektradtyp** definierar om en planeringsrad skapas när du bokför artikelförbrukningen. Om fältet innehåller **Fakturerbart** skapas projektplaneringsrader som är klara att faktureras till kunden. Mer information finns i [Så här fakturerar du projekt](projects-how-invoice-jobs.md).
4. Välj åtgärden **Bokföra**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Visa värdet på inköp till ett projekt
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.
2. Öppna ett relevant projektkort.

    På snabbfliken **Uppgifter** visar fältet **Utestående order** det totala utestående beloppet, i lokal valuta, för lagerartiklar och tjänster för inköpsdokument för projektaktivitetsraden.  

    Fältet **Inlevererat bel. ej faktrd** visar värdet för artiklarna som har levererats på inköpsdokument, men ännu inte har fakturerats.  
3. Välj något av fälten för att öppna sidan **Inköpsrader** där du kan granska information om relaterade inköpsdokumentrader, bland annat vilka artiklar eller tjänster som har inlevererats.

## <a name="to-post-a-job-related-expense"></a>Så här bokför du en projektrelaterad utgift
Om du ådrar dig extraordinära eller engångsutgifter för projekt kan du använda sidan **Projektredovisningsjournal** för att bokföra dem direkt till det relevanta projektkontot.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projektredovisningsjournaler** och väljer sedan relaterad länk.  
2. Skapa en ny rad och registrera information om utgiften, bland annat information i fälten **Projektnr** och **Projektaktivitetsnr**.  
3. När journalen är slutförd väljer du åtgärden **Bokföra**.

## <a name="see-also"></a>Se även
[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

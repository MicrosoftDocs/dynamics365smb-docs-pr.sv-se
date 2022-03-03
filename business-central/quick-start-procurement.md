---
title: Snabb start för inköp (innehåller video)
description: Lär dig hur du fyller i de första kritiska fälten för leverantörer i Business Central så att du kan börja köpa produkter och tjänster.
author: jill-kotel-andersson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: 26, 27, 50, 56
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: d5ec92099a7439bfb9a059105b0f1ce377534117
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8128745"
---
# <a name="procurement-quick-start"></a>Snabbstart för inköp

För att kunna köpa produkter och tjänster måste du först lägga upp leverantörer. När du är klar kan du börja registrera inköpsorder och ta emot fakturor.  

## <a name="set-up-vendors"></a>Ange leverantörer

I följande video visas hur du konfigurerar en leverantör i [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### <a name="set-up-a-new-vendor"></a>Skapa en ny leverantör

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Mer information och andra åtgärder du kan utföra när du registrerar leverantörer finns i [registrera nya leverantörer](purchasing-how-register-new-vendors.md).  

## <a name="create-new-purchase-orders"></a>Skapa en ny inköpsorder

När du köper något från en leverantör finns det två alternativ. Det första är att bara skapa en inköpsfaktura. Du måste använda inköpsorder om din inköpsprocess kräver att du t. ex. kan registrera delleveranser av en orderkvantitet eftersom hela kvantiteten inte var tillgänglig hos leverantören.

I följande video visas hur du skapar en inköpsorder i [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-order"></a>Skapa en inköpsorder  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.  

2. På sidan **inköpsorder**, välj åtgärden **Ny** för att skapa en ny inköpsorder.

3. Ange namnet på en befintlig leverantör i fältet **Leverantörsnamn**.

    Andra fält på sidan **Inköpshuvud** fylls nu i med standardinformation om den valda leverantören.  

4. På sidan **Inköpsorder** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Fortsätt nu med att fylla inköpsorder med artiklar eller resurser som du har köpt från leverantören.

5. Ange numret på en lagerförd artikel eller service på snabbfliken **Rader** Snabbfliken, i **Artikelnr** fältet.

6. Ange hur många artiklar som ska införskaffas i fältet **Antal**.

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Inköpspris** multiplicerat med värdet i fältet **Kvantitet**.

7. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms** längst ned på order.

8. Välj **Bokför** när du tar emot de beställda artiklarna eller tjänster.

Mer information och andra åtgärder du kan utföra när du skapar en inköps order finns i [inköp](purchasing-manage-purchasing.md).  

## <a name="create-a-purchase-invoice"></a>Skapa en inköpsfaktura  

Du skapar en inköpsfaktura för att registrera kostnaden för inköp och för att spåra leverantörsskulder. Att skapa en inköpsfaktura påminner om att skapa en inköpsorder.

### <a name="how-to-create-and-post-a-purchase-invoice"></a>Så här skapar och bokför du inköpsfaktura  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. På sidan **inköpsfaktura**, välj åtgärden **Ny** för att skapa en ny inköpsfaktura.
3. Ange namnet på en befintlig leverantör i fältet **Leverantör**.

    Andra fält på sidan **Inköpsfaktura** fylls nu i med standardinformation om den valda leverantören.

4. På sidan **Inköpsfaktura** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Fortsätt nu med att fylla inköpsfakturaraderna med artiklar eller resurser som du har köpt från leverantören.

5. Ange numret på en lagerförd artikel eller service på snabbfliken **Rader** Snabbfliken, i **Artikelnr** fältet.
6. Ange hur många artiklar som ska införskaffas i fältet **Antal**.

    Fältet **Radbelopp** uppdateras och visar värdet i fältet **Inköpspris** multiplicerat med värdet i fältet **Kvantitet**.

7. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms** längst ned på fakturan.

8. Välj **Bokför** när du tar emot de beställda artiklarna eller tjänster.

Inköpet visas nu i lager, resurstransaktioner och ekonomiska transaktioner, och leverantörsbetalningen aktiveras. Inköpsfakturan tas bort från listan över inköpsfakturor och ersätts med ett nytt dokument i listan över bokförda inköpsfakturor.  

Mer information och andra åtgärder du kan utföra när du skapar en inköpsfaktura finns i [Registrera inköp med inköpsfakturor](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Se även

[Snabbstart för Business Central](quick-start-business-central.md)  
[Inköpsöversikt](Purchasing-manage-purchasing.md)  
[Registrera inköp med inköpsfakturor](purchasing-how-record-purchases.md)  

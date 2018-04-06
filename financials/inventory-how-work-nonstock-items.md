---
title: "Skapa och hantera Ej lagerförda artiklar | Microsoft Docs"
description: Beskriver hur du byter icke inventeringsbara artiklar eller artiklar som inte finns kvar i lagret.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2969b3168f063e636455dd67457c01ed89a0727d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-nonstock-items"></a>Arbeta med ej lagerförda artiklar
Du kan erbjuda vissa artiklar till dina kunder för deras bekvämlighet, som du inte vill hålla i lager, tills du börjar sälja dem. När du vill börja hålla sådana artiklar i lager, kan du konvertera dem till vanliga artikelkort på två sätt.

* Från en ej lagerförd artikel skapar du ett nytt lagerkort baserat på en mall.
* Från en försäljningsorderrad av typen **Artikel** med ett tomt fält **Nr* väljer du en ej lagerförd artikel. Ett artikelkort automatiskt för den ej lagerförda artikeln.

> [!NOTE]  
>   Du kan inte välja en ej lagerförd artikel från fönstret **Försäljningsfaktura**. Du kan välja en ej lagerförd artikel från fönstret **Försäljningsoffert** men den ej lagerförda artikeln kommer inte att omvandlas till en vanlig artikel när du använder funktionen **Gör beställning**.

En ej lagerförd artikel har vanligtvis artikelnumret från den leverantör som levererar den. Om du vill aktivera konvertering av ett kort för en ej lagerförd artikel till ett vanligt artikelkort måste du först ställa in hur leverantörens artikelnumrering konverteras till din egen artikelnumrering.   

## <a name="to-create-a-nonstock-item"></a>Så här skapar du en ej lagerförd artikel
Kort för ej lagerförd artikel har mycket mindre information än normala artikelkort, eftersom du bara använder dem för att erbjuda på offerter och på andra sätt. Därför måste de konverteras till normala artikelkort, innan du kan bokföra försäljningstransaktioner för dem.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Ej lagerförda artiklar**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a>Så här ställer du in hur ej lagerförda artikelnummer konverteras till ditt eget nummer
Om du vill aktivera konvertering av ett kort för en ej lagerförd artikel till ett vanligt artikelkort måste du först ställa in hur leverantörens artikelnumrering konverteras till dit eget nummerformat.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Inställningar för ej lagerförda artiklar**, och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a>Om du vill omvandla en ej lagerförd artikel till en normal artikel
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Ej lagerförda artiklar**, och välj sedan relaterad länk.
2. Öppna kortet för den ej lagerförda artikeln som du vill konvertera till en normalt artikel.
3. I fönstret **Ej lagerförd artikelkort** väljer du åtgärden **Skapa artikel**.

Ett nytt artikelkort förifyllt med information från den ej lagerförda artikeln och en relevant artikelmall skapas. Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a>Om du vill sälja en ej lagerförd artikel och konvertera den till en normal artikel
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**. Fyll i övriga fält på snabbfliken **Allmänt** som för alla andra försäljningsorder. Mer information finns i [Sälja produkter](sales-how-sell-products.md).
3. På en ny försäljningsrad i fältet **Typ** väljer du **Artikel**, men lämnar **Nr.** tomt.
4. Välj åtgärden **Rad** och välj sedan åtgärden **Välj Ej lagerförda artiklar**.

    Den ej lagerförda artikeln omvandlas till en normal artikel. Ett nytt artikelkort förifyllt med information från den ej lagerförda artikeln och en relevant artikelmall skapas.
5. Markera den ej lagerförda artikel som du vill visa i fönstret **Ej lagerförda artiklar** och klicka på **OK**.
6. När försäljningsordern är slutförd väljer du åtgärden **Bokföra**.

Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

> [!NOTE]  
>   En korsreferenspost för artikel skapas automatiskt för den leverantör som levererar artikeln mellan leverantörens artikelnummer och det nya artikelnumret.

## <a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Skapa specialorder](sales-how-to-create-special-orders.md)|  
[Lagersaldo](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


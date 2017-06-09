---
title: "Så här arbetar du med Ej lagerförda artiklar | Microsoft Docs"
description: Beskriver hur du hanterar artiklar som inte finns i lager
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae4710c0771d2b10c691f878ad6532e95f3b2912
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-nonstock-items"></a>Så här arbetar du med Ej lagerförda artiklar
Du kan erbjuda vissa artiklar till dina kunder för deras bekvämlighet, som du inte vill hålla i lager, tills du börjar sälja dem. När du vill börja hålla sådana artiklar i lager, kan du konvertera dem till vanliga artikelkort på två sätt.

* Från en ej lagerförd artikel skapar du ett nytt lagerkort baserat på en mall.
* Från en försäljningsorderrad av typen **Artikel** med ett tomt fält **Nr* väljer du en ej lagerförd artikel. Ett artikelkort automatiskt för den ej lagerförda artikeln.

**Obs**: Du kan inte välja en ej lagerförd artikel från fönstret **Försäljningsfaktura**. Du kan välja en ej lagerförd artikel från fönstret **Försäljningsoffert** men den ej lagerförda artikeln kommer inte att omvandlas till en vanlig artikel när du använder funktionen **Gör beställning**.

En ej lagerförd artikel har vanligtvis artikelnumret från den leverantör som levererar den. Om du vill aktivera konvertering av ett kort för en ej lagerförd artikel till ett vanligt artikelkort måste du först ställa in hur leverantörens artikelnumrering konverteras till din egen artikelnumrering.   

## <a name="to-create-a-nonstock-item"></a>Så här skapar du en ej lagerförd artikel
Kort för ej lagerförd artikel har mycket mindre information än normala artikelkort, eftersom du bara använder dem för att erbjuda på offerter och på andra sätt. Därför måste de konverteras till normala artikelkort, innan du kan bokföra försäljningstransaktioner för dem.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Ej lagerförda artiklar**, och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a>Så här ställer du in hur ej lagerförda artikelnummer konverteras till ditt eget nummer
Om du vill aktivera konvertering av ett kort för en ej lagerförd artikel till ett vanligt artikelkort måste du först ställa in hur leverantörens artikelnumrering konverteras till dit eget nummerformat.

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Inställningar för ej lagerförda artiklar**, och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs.

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a>Om du vill omvandla en ej lagerförd artikel till en normal artikel
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Ej lagerförda artiklar**, och väljer sedan relaterad länk.
2. Öppna kortet för den ej lagerförda artikeln som du vill konvertera till en normalt artikel.
3. I fönstret **Ej lagerförd artikelkort** väljer du åtgärden **Skapa artikel**.

Ett nytt artikelkort förifyllt med information från den ej lagerförda artikeln och en relevant artikelmall skapas. Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a>Om du vill sälja en ej lagerförd artikel och konvertera den till en normal artikel
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **försäljningsorder**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**. Fyll i övriga fält på snabbfliken **Allmänt** som för alla andra försäljningsorder. Mer information finns i [Så här säljer du produkter](sales-how-sell-products.md).
3. På en ny försäljningsrad i fältet **Typ** väljer du **Artikel**, men lämnar **Nr.** tomt.
4. Välj åtgärden **Rad** och välj sedan åtgärden **Välj Ej lagerförda artiklar**.

    Den ej lagerförda artikeln omvandlas till en normal artikel Ett nytt artikelkort förifyllt med information från den ej lagerförda artikeln och en relevant artikelmall skapas.
5. Markera den ej lagerförda artikel som du vill visa i fönstret **Ej lagerförda artiklar** och klicka på **OK**.
6. När försäljningsordern är slutförd väljer du åtgärden **Bokföra**.

Du kan sedan ange eller redigera fält på det nya artikelkortet vid behov. Mer information finns i [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).

**Obs!**: En korsreferenspost för artikel skapas automatiskt för den leverantör som levererar artikeln mellan leverantörens artikelnummer och det nya artikelnumret.

## <a name="see-also"></a>Se även
[Så här registrerar du nya objekt](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
title: Så här konfigurerar du måttenheter för artiklar | Microsoft Docs
description: Du kan ange flera enheter för en artikel, så att du kan tilldela måttenheter till artikeln.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: 47d59af91af7c043c98a4db2a5c103b0052e32e2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "919251"
---
# <a name="set-up-item-units-of-measure"></a>Ställa in måttenheter för artikel
Du kan ange flera enheter för en artikel, så att du kan tilldela enheter till artikeln för efterföljande avsikter:

- Tilldela en basmåttenhet på artikelns artikelkort för att definiera hur den lagras i lager och för att tjäna som konverteringsbasen för alternativa måttenheter.
- Tilldela alternativa måttenheter till inköps-, produktions- eller försäljningsdokument för att ange hur många enheter av basenheten du hanterar samtidigt i dessa processer. Du kan till exempel köpa artikeln på pallar och endast använda enstaka enheter i produktionen.

Om en artikel lagerförs med en enhet men tillverkas med en annan, kan du skapa en produktionsorder som använder enheten för produktionsbatch för att beräkna rätt antal komponenter under batch-jobbet **Uppdatera produktionsorder**. Ett exempel på beräkning med en enhet för produktionsbatch är när tillverkade artiklar lagerförs styckvis, men tillverkas tonvis. Mer information finns i [Arbeta med måttenheter för produktionbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Så här ställer du in en enhet
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för artikeln som du vill ange alternativa enheter för.
3. Välj åtgärden **Enheter**. Sidan **Artikelenheter** visas.
4. Om fältet **Basmåttenhet** är ifyllt på artikelkortet har denna måttenhet redan ställts in.
5. Välj åtgärden **Ny**. En ny tom rad infogas.
6. Ange namnet på enheten i fältet **Kod**. Du kan också välja fältet om du vill välja mellan de enhetskoder som finns i databasen.
7. I fältet **Antal per måttenhet** anger du hur många enheter av basmåttenheten som den nya måttenheten innehåller.
8. Upprepa steg 5 till 7 för att lägga upp alla alternativa enheter som du vill använda i olika processer för artikeln.

Nu kan du använda de alternativa enheter för inköp, produktion och försäljningsdokument. Mer information finns i Ange standardenheter för enhetskoder för inköpstransaktioner och försäljningstransaktioner, eller Använda måttenheten för produktionsbatch.

## <a name="to-set-up-unit-of-measure-translations"></a>Så här skapar du enhetsöversättningar
När du säljer varor till utländska kunder, kan det hända att du vill ange enheten på kundens eget språk. Det kan du göra om du har skapat de enhetsöversättningar som behövs.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Enheter** och välj sedan relaterad länk.
2. Välj den kod som du vill skapa översättningar för och välj sedan åtgärden **Översättningar**.
3. I fältet **Språkkod** klickar du på listpilen om du vill visa en lista över tillgängliga språkkoder. Markera den språkkod som du vill ange en översättning för och klicka sedan på OK så kopieras koden till fältet.
4. Skriv den aktuella texten i fältet **Beskrivning**.
5. Upprepa steg 2-4 för varje måttenhetskod och de språk som du vill ange översättningar för.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Så här anger du en standardenhet för en enhetskod för försäljnings- och inköpstransaktioner
Om du brukar köpa eller sälja artiklar i andra enheter än basenheten, kan du ange särskilda enheter för inköp och försäljning. För att du ska kunna göra det, måste du ha skapat sidan **Artikelenheter**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Artiklar** och välj sedan relaterad länk.
2. Bläddra fram till det artikelkort där du vill ange en standardenhetskod för försäljning eller inköp.
3. För försäljning: På Snabbfliken **Fakturering**, i fältet **Måttenhet för försäljning**, öppna sidan **Måttenheter för artikel**.
4. För inköp: På snabbfliken **Återanskaffning** i fältet **Måttenhet för inköp** öppnar du sidan **Måttenheter för artikel**.
5. Välj den kod som du vill ange som standardenhet för försäljning respektive inköp, och välj sedan knappen **OK**.

## <a name="see-also"></a>Se även
[Arbeta med måttenheter för produktionsbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Hantera lager](inventory-manage-inventory.md)  
[Hantera inköp](purchasing-manage-purchasing.md)  
[Hantera försäljning](sales-manage-sales.md)    
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

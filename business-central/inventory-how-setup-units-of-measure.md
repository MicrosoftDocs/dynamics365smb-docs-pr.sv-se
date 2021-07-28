---
title: Så här konfigurerar du måttenheter för artiklar | Microsoft Docs
description: Du kan ange flera enheter för en artikel, så att du kan tilldela måttenheter till artikeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92fc62cf5b1e2db5d1eb34ab2aa9f86823cfe3bb
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435553"
---
# <a name="set-up-units-of-measure"></a>Ställa in måttenheter

När du skapar en inställning [!INCLUDE [prod_short](includes/prod_short.md)] anger du allmänna måttenheter på sidan **enhet**. När du sedan registrerar nya artiklar anger du basenheten på **artikelkortet**. Du kan också lägga till enheter senare.  

Du kan ange flera enheter för en artikel, så att du kan tilldela enheter till artikeln för efterföljande avsikter:

- Tilldela en basmåttenhet på artikelns artikelkort för att definiera hur den lagras i lager och för att tjäna som konverteringsbasen för alternativa måttenheter.
- Tilldela alternativa måttenheter till inköps-, produktions- eller försäljningsdokument för att ange hur många enheter av basenheten du hanterar samtidigt i dessa processer. Du kan till exempel köpa artikeln på pallar och endast använda enstaka enheter i produktionen.

Om en artikel lagerförs med en enhet men tillverkas med en annan, kan du skapa en produktionsorder som använder enheten för produktionsbatch för att beräkna rätt antal komponenter under batch-jobbet **Uppdatera produktionsorder**. Ett exempel på beräkning med en enhet för produktionsbatch är när tillverkade artiklar lagerförs styckvis, men tillverkas tonvis. Mer information finns i [Arbeta med måttenheter för produktionbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

## <a name="to-set-up-units-of-measure"></a>Ställa in måttenheter

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **måttenhet** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**. En ny tom rad infogas.  
3. Fyll i fälten. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Om du vet att organisationen kommer att sälja artiklar med den här enheten till kunder i andra länder kan du lägga till översättningar.  
    1. Välj den kod som du vill skapa översättningar för och välj sedan åtgärden **Översättningar**.
    2. I fältet **Språkkod** klickar du på listpilen om du vill visa en lista över tillgängliga språkkoder. Markera den språkkod som du vill ange en översättning för och klicka sedan på OK så kopieras koden till fältet.
    3. Skriv den aktuella texten i fältet **Beskrivning**.
5. Upprepa föregående steg för de övriga enheter som du vill lägga till.  

När du registrerar en ny artikel kan du välja basenheten från listan över enheter som du nu har lagt upp. Du kan också lägga upp flera enheter för en artikel.  

## <a name="to-set-up-multiple-item-units-of-measure"></a>För att ställa in flera måttenheter

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Öppna kortet för artikeln som du vill ange alternativa enheter för.
3. Välj åtgärden **Enheter**. Sidan **Artikelenheter** visas.
4. Om fältet **Basmåttenhet** är ifyllt på artikelkortet har denna måttenhet redan ställts in.
5. Välj åtgärden **Ny**. En ny tom rad infogas.
6. Ange namnet på enheten i fältet **Kod**. Du kan också välja fältet om du vill välja mellan de enhetskoder som finns i databasen.
7. I fältet **Antal per måttenhet** anger du hur många enheter av basmåttenheten som den nya måttenheten innehåller.
8. Du kan även i fälten **Höjd**, **Bredd**, **Längd** och **Vikt** anger du exakt information om storleken på en enhet så att antalet enheter så att [!INCLUDE [prod_short](includes/prod_short.md)] antalet enheter som ryms per lagerplats kan beräknas. Fältet **Kubik** beräknas automatiskt utifrån **Höjd**, **Bredd** och **Längd**.

    Om något av fälten innehåller ett annat värde än 0, används den här åtgärden vid alla processer som inbegriper placering av artiklar på lagerställen: artikelinförsel, transporter, inleveranser, utleveranser, plockningar och justeringar. [!INCLUDE [prod_short](includes/prod_short.md)] kontrollerar summan av varje fysiskt mått på föremål som tas bort och objekten som redan finns i papperskorgen mot den maximala volym som lagerstället kan inrymma, enligt de kapacitetsregler som du har angett på lagerställekortet. Med andra ord måste du använda samma enhetsmått för varje dimension över alla måttenheter, användningspriser eller pund för vikt, t. ex.
9. Upprepa steg 5 till 7 för att lägga upp alla alternativa enheter som du vill använda i olika processer för artikeln.

    I fältet **basenhet** längst ned i fönstret, kan du visa eller ändra artikelns basenhet. Du kan också ändra basenhet i fältet **basenhet** på artikelkortet. På sidan **måttenheter för artikel** måste basenheten ha värdet **1** i fältet **Antal per måttenhet**.

Du kan nu använda de alternativa enheterna i inköps-, produktions- och försäljningsdokument enligt beskrivningen i [och ange en standardenhetskod för försäljnings-och inköpstransaktioner](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## <a name="to-set-up-unit-of-measure-translations"></a>Så här skapar du enhetsöversättningar

När du säljer varor till utländska kunder, kan det hända att du vill ange enheten på kundens eget språk. Det kan du göra om du har skapat de enhetsöversättningar som behövs.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **måttenhet** och väljer sedan relaterad länk.
2. Välj den kod som du vill skapa översättningar för och välj sedan åtgärden **Översättningar**.
3. I fältet **Språkkod** klickar du på listpilen om du vill visa en lista över tillgängliga språkkoder. Markera den språkkod som du vill ange en översättning för och klicka sedan på OK så kopieras koden till fältet.
4. Skriv den aktuella texten i fältet **Beskrivning**.
5. Upprepa steg 2-4 för varje måttenhetskod och de språk som du vill ange översättningar för.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Så här anger du en standardenhet för en enhetskod för försäljnings- och inköpstransaktioner

Om du brukar köpa eller sälja artiklar i andra enheter än basenheten, kan du ange särskilda enheter för inköp och försäljning. För att du ska kunna göra det, måste du ha skapat sidan **Artikelenheter**.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.
2. Bläddra fram till det artikelkort där du vill ange en standardenhetskod för försäljning eller inköp.
3. För försäljning: På Snabbfliken **Fakturering**, i fältet **Måttenhet för försäljning**, öppna sidan **Måttenheter för artikel**.
4. För inköp: På snabbfliken **Återanskaffning** i fältet **Måttenhet för inköp** öppnar du sidan **Måttenheter för artikel**.
5. Välj den kod som du vill ange som standardenhet för försäljning respektive inköp, och välj sedan knappen **OK**.

## <a name="see-also"></a>Se även

[Arbeta med måttenheter för produktionsbatch](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Hantera lager](inventory-manage-inventory.md)  
[Hantera inköp](purchasing-manage-purchasing.md)  
[Hantera försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
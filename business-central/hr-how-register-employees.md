---
title: Ställ in medarbetare och ändra Information
description: Beskriver hur du använder funktionen personal för att registrera ny personal eller redigera personalinformation för en befintlig personal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personnel, people, employee, staff, HR
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9f25ea61c41bfeb08b9283153a96b8a78ce7c9b7
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589288"
---
# <a name="register-employees"></a>Registrera personal
Om du vill använda funktionen personal måste du först lägga till varje medarbetare genom att fylla i fälten på sidan **personalkort** .

## <a name="adding-new-customers"></a>Lägga till nya kunder
Du kan lägga till nya anställda manuellt, genom att fylla i fälten på sidan för **Personalkort** eller använda mallar som innehåller fördefinierad information. Du kan t.ex. skapa mallar för olika typer av personalprofiler. När du använder mallar sparar du tid när du lägger till nya medarbetare och ser till att informationen är korrekt varje gång. Om du skapar mallar för fler än en typ av medarbetare kan du välja vilken mall du vill använda när du lägger till en medarbetare. Om du bara skapar en mall kommer den att användas för alla nya medarbetare. När du har skapat en mall kan du använda åtgärden **tillämpa mall** för att tillämpa den på en eller flera valda medarbetare. Om du vill skapa en mall fyller du i den information som du vill använda på personalkortsidan och sparar den som en mall.

> [!TIP]
> Det kan vara användbart att anpassa sidan för **personalmall** när du skapar en mall. Du kanske till exempel vill lägga till ett fält som inte redan visas på sidan. Mer information finns i [Anpassa din arbetsyta](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan när som helst ändra informationen om en anställd. Uppdaterade medarbetarregister underlättar personalrelaterade uppgifter. Om en anställd till exempel byter adress kan du registrera den nya informationen på hans eller hennes personalkort.

> [!NOTE]  
> Du kan återbetala en medarbetare för deras utgifter under affärsaktiviteter. Av den anledningen måste du fylla i fälten på snabbfliken **Betalningar** på sidan **Personalkort**. Mer information finns i [Så här registrerar du och återbetalar personalens utgifter](finance-how-record-reimburse-employee-expenses.md).

## <a name="to-set-up-an-employee"></a>Så här registrerar du personal
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **personal** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. På sidan **Personalkort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-a-picture-of-an-employee"></a>Infoga en bild av den anställde
Om du har en bild av en anställd kan du infoga den på personalkortet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **personal** och väljer sedan relaterad länk.
2. Öppna kortet för relevant anställd.
3. I faktaboxen **Personalbild** väljer du listruteknappen och väljer sedan **Importera**.
4. På sidan **Välj en bild att ladda upp** kan välja knappen **Välj**.
5. Välj filen, och välj sedan **Öppna**.

Bilden infogas i faktaboxen **Personalbild**.

## <a name="to-register-various-information-about-an-employee"></a>Så här registrerar du information om en anställd
Du kan ställa in information, till exempel medlem i fackföreningen, anhöriga och anställningsavtal på personalkortet. Nedan beskrivs hur du ställer in en alternativ adress. Stegen är liknande för alla andra uppgifter som du kan ställa in på ett personalkort.

Du kan använda alternativa adresser för att hålla reda på var de anställda befinner sig, om de t. ex. är stationerade utomlands, befinner sig på en längre affärsresa eller vistas i sommarstuga.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **personal** och väljer sedan relaterad länk.
2. Öppna kortet för relevant anställd.
3. Välj åtgärden **alternativa adresser**.
4. På sidan **Alternativ adresslista** fyller du i fälten efter behov.
5. Upprepa steg 4 för varje alternativ adress.

## <a name="see-also"></a>Se även
[Skapa och återbetala de anställdas utgifter](finance-how-record-reimburse-employee-expenses.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
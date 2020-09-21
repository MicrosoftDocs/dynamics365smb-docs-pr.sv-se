---
title: Slå samman dubelttposter för kund eller leverantör | Microsoft Docs
description: Beskriver hur du skapar ett kundkort för att registrera information om varje ny kund eller klienten som du säljer till.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f789c5caf0f59b1fdf3b3b10d42210152f32dc97
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781666"
---
# <a name="merge-duplicate-records"></a>Slå samman dubblettposter
När olika användare skapar nya kunder, leverantörer eller kontaktkort med tiden eller nya poster skapas automatiskt vid migrering kan kund, leverantör eller kontakt visas på system med mer än en post. I så fall kan du använda sidan **slå samman dubletter** från kortet för den post som du vill behålla. Den här sidan innehåller en översikt över dubbla fältvärden och innehåller funktioner för att välja vilka värden som ska behållas eller ignoreras när du slår samman två poster i en.

> [!NOTE]
> Endast användare med behörigheten SLÅ SAMMAN DUBBLETTER kan använda den här funktionen.

> [!TIP]
> Sidan **slå samman dubbletter** visar alla fält där värdena är olika för de två poster som jämförs. Därför visas en kopia av sidan med mycket få fält. Om sidan innehåller flera fält är den misstänkta posten förmodligen inte en dubblett.

Följande procedur baseras på ett kundkort. Momenten är liknande för en leverantör och kontaktkort.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.
2. Välj den kund som du vet eller misstänker har dubblettposter och välj sedan åtgärden **redigera**.
3. På sidan **Kundkort** väljer du åtgärden **Slå samman med**.
4. På sidan **Slå samman dubbletter** i fältet **slå samman med** markerar du den kund som du tror är en dubblett av den som du har öppnat som anges i fältet **aktuell**.

    Snabbfliken **fält** visar var värdena är olika för de två kunderna. Det innebär att om den valda kunden verkligen är en dubblett kommer endast mycket få fält att visas, till exempel skrivfel och andra datainmatningsfel.

    Snabbfliken **relaterade tabeller** innehåller tabeller där det finns fält som har en relation till båda kunder. Fälten **Aktuellt antal** och **Duplicera antal** visar antalet fält i relaterade tabeller där värdet **Nr.** för både aktuell och dubblettkund används. På sidan **Slå samman dubblett** i det här avsnittet finns endast information, men om det finns sammanslagningskonflikter kan du åtgärda dem på sidan **Slå samman dubblettkonflikter**. Se steg 8 till 12.   

5. För varje fält där du vill använda ett annat värde än det aktuella markerar du kryssrutan **åsidosätta**. Värdet i fältet **alternativt värde** kommer därefter att överföras till den aktuella posten när du slutför processen.
6. När du är klar med att välja vilka värden som du vill behålla eller åsidosätta, väljer du åtgärd **slå samman**.

    Systemet kontrollerar om kopplingen av värden för dubblettkunden i den aktuella kunden orsakar några konflikter. En konflikt finns om ett värde i åtminstone ett primärnyckelfält är detsamma för både kunder när värdet i fältet **Nej** är olika för de två kunderna.

7. Om inga konflikter finns väljer du knappen **Ja** i bekräftelsemeddelanderutan.

    Dubblettkunden får ett nytt namn så att all användning av dess värde **Nr.** i alla fält med relationer i kundtabellen ersätts med värdet **Nr.** för den aktuella kunden.
8. Om det finns konflikter, väljer du åtgärden **Lös (xx) konflikter före sammanslagning.** på snabbfliken **konflikter** som visas om det finns konflikter.
9. På sidan **Slå samman dubblettkonflikter** markerar du raden för en relaterad tabell med en konflikt och väljer sedan åtgärden **Visa detaljer**.

    På sidan **Slå samman dubbletter** visas nu fält i den valda tabellen som orsakar en kopplingskonflikt mellan de två kundposterna. Observera i båda summerade värdena i fälten **aktuell** och **konflikter med** och på raderna där minst ett primärnyckelfält är samma för både kunder och värdet för fältet **Nr.** är olika för de två kunderna.   
10. Om du inte vill behålla dubblettkundposten väljer du åtgärden **ta bort dubblett** och väljer sedan knappen **Stäng**.

    Identiska fältvärden, andra än värdet i fältet **Nr.** tas bort från dubblettposten och infogas på den aktuella posten.
11. Om du vill behålla dubblettkundposten efter kopplingen, väljer du **Byt namn på dubblett**.
12. På rader, inte för fältet **Nr.** ändrar du värdet i fältet, om fältet har samma värde på båda posterna, ändrar du värdet i **alternativt värde** och välj sedan knappen **Stäng**.

    Konflikten mellan fältvärdet uppdateras på dubblettposten så att den kan slås samman med den aktuella posten. Dubblettposten kvarstår fortfarande efter kopplingen.
13. Upprepa steg 8 till och med 12 tills alla konflikter har lösts. Snabbfliken **konflikter** försvinner.
14. På sidan **Slå samman dubblett**, välj åtgärden **slå samman** och välj sedan **Ja** i rutan Bekräfta meddelandet.

> [!NOTE]
> För kontakter kan du använda funktionen för att söka efter dubbletter av kontakter innan du använder sidan **slå samman dubbletter**. Mer information finns i [söka efter dubblettkontakter](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Ställa in kontakter](marketing-setup-contacts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

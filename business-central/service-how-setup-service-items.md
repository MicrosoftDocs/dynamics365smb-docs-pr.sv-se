---
title: Konfiguration serviceartiklar och serviceartikelkomponenter | Microsoft Docs
description: Mer information om saker som du måste ställa in innan du kan använda serviceartiklar, inklusive standardvärden, till exempel svarstid, kontraktrabatt i procent och serviceprisgrupp.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed02fb95e2f700f1cc5083472b668f49fab7d916
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775381"
---
# <a name="set-up-service-items-and-service-item-components"></a>Ställa in tjänsteartiklar och tjänsteartikelkomponenter
Om du vill arbeta med serviceartiklar måste du ställa in följande

* Serviceartikelgrupper
* Valfritt

## <a name="to-set-up-service-item-groups"></a>Så här skapar du serviceartikelgrupper:
Du anger grupper med artiklar som hör ihop med avseende på reparation och underhåll. Du kan ange standardvärden för serviceartiklar i serviceartikelgruppen, t. ex. svarstid, kontraktrabatt i procent och serviceprisgrupp. För artiklar i en serviceartikelgrupp kan du välja om du vill att de ska registreras automatiskt som serviceartiklar då de säljs..  

Du tilldelar serviceartikelgrupper till artiklar på **Artikelkortet** och till serviceartiklar på **serviceartikelkortet**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Serviceartikelgrupper** och välj sedan relaterad länk.  
2. Skapa en ny serviceartikelgrupp.  
3. Fyll i fälten **Kod** och **Beskrivning**.  
4. I fältet **Standard kontraktsrabatt %** anger du standardrabatten i procent för kontrakt som du vill att serviceartiklarna i gruppen ska ha.  
5. I fältet **Standard serviceprisgruppskod** anger du den förvalda serviceprisgruppskoden som du vill att serviceartiklarna i gruppen ska ha.  
6. I fältet **Standard svarstid (timmar)** anger du standardsvarstiden som du vill att serviceartiklarna i gruppen ska ha, i timmar.  
7. Om du vill att artiklarna i gruppen ska registreras som serviceartiklar då de säljs, väljer du fältet **Skapa serviceartikel**.  

## <a name="to-set-up-service-item-components"></a>Så här ställer du in serviceartikelkomponenter
En serviceartikel kan bestå av flera komponenter, som kan ersättas med reservdelar då artikeln är servad. Komponenterna läggs upp på sidan **Serviceartikelkomponent lista**. Om du vill skapa komponenter för serviceartiklar som är strukturer kan du låta kopiera strukturartiklarna automatiskt och skapa dem som serviceartikelkomponenter.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceartiklar** och välj sedan relaterad länk.
2. Öppna serviceartikeln som du vill skapa komponenter för.  
3. Välj åtgärden **Komponenter**. Sidan **Serviceartikelkomponent lista** öppnas.  
4. Lägg till en ny komponent.  
5. I fältet **Typ** väljer du **Serviceartikel** om själva komponenten är en registrerad serviceartikel. Välj annars **Artikel**.  
6. I fältet **Nr.** väljer du den artikel eller serviceartikel som utgör en serviceartikelkomponent.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Så här ställer du in serviceartikelkomponenter från en struktur
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **serviceartiklar** och välj sedan relaterad länk.  
2. Öppna den serviceartikel som du vill skapa komponenter från en struktur för.  
3. Välj åtgärden **Komponenter**. Sidan **Serviceartikelkomponent lista** öppnas.  
4. Välj fältet **Kopiera från struktur**  

    Om artikeln som serviceartikeln är kopplad till är en struktur skapas automatiskt komponenter för alla artiklarna i strukturen.  

## <a name="to-set-up-a-service-shelf"></a>Så här skapar du en servicehylla
Du kan lägga upp servicehyllor som hjälper till att identifiera där du lagrar dina serviceartiklar. Du tilldelar servicehyllor till serviceartiklar på sidan **Tjänsteorder** och i fönstret **Serviceartikel arbetsblad**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Servicehyllor** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.

## <a name="see-also"></a>Se även
[Skapa koder för standardtjänst](service-how-setup-service-coding.md)   
[Ställa in felsökning](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
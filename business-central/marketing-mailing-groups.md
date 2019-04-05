---
title: Ställa in utskicksgrupper för kontakter | Microsoft Docs
description: Du kan använda utskicksgrupper för att identifiera grupper av kontakter som ska få samma information, t.ex. för en marknadsföringskampanj.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6c089b772c139d0c0e9465f383ab39bd3c125dca
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807291"
---
# <a name="set-up-mailing-groups-for-contacts"></a>Skapa utskicksgrupper för kontakter
Utskicksgrupper används för att definiera kontaktgrupper som du vill ge samma information. Du kan till exempel skapa en utskicksgrupp med de kontakter du vill skicka flyttkort till eller en annan grupp för att skicka julklappar.

Att använda utskicksgrupper på kontakter är en två-stegsprocess. Först definierar du utskicksgruppkoden. Du måste bara utföra den här steget en gång för varje utskicksgrupp. När du har en utskicksgrupp kan du börja koppla koden till kontaktföretag.

## <a name="to-define-mailing-group-codes"></a>Definiera utskicksgruppkoder
Utskicksgruppkoden definierar typen eller kategorin för den gruppen, till exempel FLYTTA för kontorsflyttning eller GÅVA för julklappar. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du sidan **Utskicksgrupper**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utskicksgrupper** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="AssignMailGroupContact"></a> Så här tilldelar du utskicksgrupp till en kontakt
1. Öppna kontakten .
2. Välj åtgärden **Utskicksgrupper**. Sidan **Kontakt Utskicksgrupper** öppnas.
3. I fältet **Utskicksgruppskod**, markera den utskicksgrupp du vill tilldela.

Upprepa stegen för varje utskicksgrupp du vill tilldela. Utskicksgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet utskicksgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal utskicksgrupper** på avsnittet **Segmentering** på **Kontakt**-sidan.

När du har tilldelat kontakterna utskicksgrupp kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapar kontakter](marketing-create-contact-companies.md)  
[Arbeta med Business Central](ui-work-product.md)

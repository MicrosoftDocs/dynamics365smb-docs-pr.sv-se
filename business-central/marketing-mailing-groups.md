---
title: "Ställa in utskicksgrupper för kontakter | Microsoft Docs"
description: "Du kan använda utskicksgrupper för att identifiera grupper av kontakter som ska få samma information, t.ex. för en marknadsföringskampanj."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a7b9c39b1f213bf2b09ee24e3e6172df027e042c
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Skapa utskicksgrupper för kontakter
Utskicksgrupper används för att definiera kontaktgrupper som du vill ge samma information. Du kan till exempel skapa en utskicksgrupp med de kontakter du vill skicka flyttkort till eller en annan grupp för att skicka julklappar.

Att använda utskicksgrupper på kontakter är en två-stegsprocess. Först definierar du utskicksgruppkoden. Du måste bara utföra den här steget en gång för varje utskicksgrupp. När du har en utskicksgrupp kan du börja koppla koden till kontaktföretag.

## <a name="to-define-mailing-group-codes"></a>Definiera utskicksgruppkoder
Utskicksgruppkoden definierar typen eller kategorin för den gruppen, till exempel FLYTTA för kontorsflyttning eller GÅVA för julklappar. Du kan ha flera branschgruppkoder. För att definiera branschgrupperna använder du fönstret **utskicksgrupper**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Utskicksgrupper** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

## <a name="AssignMailGroupContact"></a> Så här tilldelar du utskicksgrupp till en kontakt
1. Öppna kontakten .
2. Välj åtgärden **Utskicksgrupper**. Fönstret **Kontakt utskicksgrupp** öppnas.
3. I fältet **Utskicksgruppskod**, markera den utskicksgrupp du vill tilldela.

Upprepa stegen för varje utskicksgrupp du vill tilldela. Utskicksgrupper kan också tilldelas i Kontaktlista på samma sätt.

Antalet utskicksgrupper som du har tilldelat kontakter anges automatiskt i fältet **Antal utskicksgrupper** på avsnittet **Segmentering** på **Kontakt**-fönstret.

När du har tilldelat kontakterna utskicksgrupp kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeta med Business Central](ui-work-product.md)


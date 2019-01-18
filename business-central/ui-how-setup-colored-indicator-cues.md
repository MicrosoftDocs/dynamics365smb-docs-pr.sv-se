---
title: Anpassa visuella signaler om en stack-ikons aktivitet | Microsoft Docs
description: "Skapa en färgindikator på en stack-ikon för att ge en anpassad visuell signal på stack-ikonens aktivitet."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 366d762fbfbd2a61253b087577ef2810194e2c35
ms.contentlocale: sv-se
ms.lasthandoff: 11/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a>Skapa en färglagd indikator på stack-ikoner
Du kan konfigurera stack-ikoner som visas i användarens rollcenter för att inkludera en indikator som ändrar färg baserat på datavärdena i stack-ikonerna.

Indikatorn visas som en kulört stapel längs den övre kanten på stack-ikon-panelen. Den ger en visuell signal över statusen för stack-ikonaktivitet, som kan ange gynnsamma eller ofördelaktiga förhållanden för att meddela användaren att vidta åtgärd. Om t.ex. en stack-ikon visar pågående försäljningsfakturor kan du ställa in indikatorn för att visa grönt (positivt) när totala antalet pågående försäljningsfakturor är under 10, och röd (negativt) när antalet är större än 20.

Från sidan **Inställning av stack-ikon** ställer du in indikatorer för alla stack-ikoner som är tillgängliga i företagsdatabasen.

För att ställa in indikatorn, anger du upp till två tröskelvärden som definierar tre intervall av datavärden (låg, medel och hög) som du kan koppla en annan färg (eller stil).

## <a name="to-set-up-colored-indicators-on-cues"></a>Så här ställer du in kulörta indikatorer på stack-ikoner
1. Under **Aktiviteter** på ditt Rollcenter väljer du **Inställning av stack-ikon**.  
   Sidan **Inställning av stack-ikon** visas. Sidan anger indikatorerna som för närvarande är inställda på stack-ikoner.
2. För att ändra en indikator redigerar du fälten och för att ändra till exempel,värdena för de olika trösklarna.  

Efterföljande tabeller listar de bakgrundsfärger som motsvarar alternativen för fälten **Lågt intervallformat**, **Medelintervallformat** och **Högt intervallformat**.

| Alternativ | Färg |
| --- | --- |
| **Ingen** |Ingen färg (samma färg som stack-ikonen)|
| **Positiv** |Grön |
| **Negativ** |Röd |
| **Tvetydigt** |Gul |
| **Underordnad** |Grått |

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


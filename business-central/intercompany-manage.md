---
title: Hantera koncerninterna transaktioner
description: Med de koncerninterna funktionerna förenklar du affärsprocesser och transaktioner mellan företag inom samma organisation.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/02/2021
ms.author: edupont
ms.openlocfilehash: 0a69507b32f8782fe876458adb590529bfd64b20
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184430"
---
# <a name="managing-intercompany-transactions"></a>Hantera koncerninterna transaktioner

Organisationen kan bestå av flera företag, men kanske inte har motsvarande antal team inom redovisning och administration. När du använder koncerninterna funktioner kan du göra affärer med dina dotterbolag och interna partnerorganisationer på samma sätt som att arbeta med externa leverantörer och kunder. Du anger bara koncernintern information en gång i tillämpliga dokument. Du kan använda funktioner som du redan känner till, t. ex. hantering av leverantörsreskontra och kundreskontra. Genom att koppla funktioner för kontoplanen och dimensioner kan du försäkra dig om att informationen visas på rätt plats.  

Det finns fyra huvudsakliga fördelar med koncerninterna funktioner:  

- Ökad produktivitet till följd av tidsbesparingar och förenklade transaktioner  
- Minimerad felpotential eftersom informationen endast behöver registreras en gång och automatiserade processer över hela systemet.  
- Fullständig redovisningsspårning och full insyn i affärsaktiviteter och transaktionshistorik  
- Effektiva, kostnadseffektiva transaktioner med dotterbolag  

Du har full kontroll över alla transaktionsdokument. Du kan t. ex. avvisa ett dokument som har skickats till dig och därmed återföra bokföringar och ångra inleveranser/utleveranser som är inkorrekta. När du gör ett inköp från en partner eller ett dotterbolag kan du uppdatera inköpsordern så länge som det säljande bolaget inte har levererat några varor.  

När du skapar en transaktion behöver du inte ange konton för en enskild räkenskapsbok, utan helt enkelt ange moderbolaget. De koncerninterna funktionerna skapar rader i redovisningsjournaler resulterar i att räkenskaperna balanseras för de båda företag som är involverade i en transaktion. I Kundreskontra och Leverantörsreskontra tilldelar du en koncernintern partnerkod till kunder och leverantörer. Alla order och fakturor som sedan genereras och som gäller transaktioner med dessa företag resulterar i att motsvarande dokument skapas i partnerföretaget och att konton balanseras korrekt.  

När du har ställt in affärspartner som kunder och leverantörer i systemet och tilldelat dem koncerninterna partnerkoder, är det möjligt att utbyta koncerninterna inköps – och försäljningsdokument, inklusive artiklar och artikelomkostnader. [!INCLUDE [prod_short](includes/prod_short.md)] har stöd för koncerninterna transaktioner mellan flera databaser, t.ex. i olika länder/regioner samt flera valutor, olika kontoplaner, olika dimensioner och olika artikelnumrering.  

> [!NOTE]
> Det går inte att byta ut alla typer av data mellan företag på det här sättet. Inköpsfakturor skickas inte till affärspartner via koncerninterna processer. Men försäljningsfakturor som skickas via koncerninterna processer kommer att skapas som inköpsfakturor i det mottagande företaget.

Att konsolidera ekonomiska data kan vara särskilt användbart för koncerninterna processer. Mer information finns i [Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|Till |Gå till|
|---|---|
|Skapa dina koncerninterna leverantörer och kunder som så kallade koncerninterna partners och konfigurera en koncernintern kontoplan.|[Koncerninterna inställningar](intercompany-how-setup.md)|
|Du använder koncerninterna dokument eller journaler för att bokföra transaktioner med koncerninterna partner.|[Arbeta med koncerninterna dokument och journaler](intercompany-how-work-documents-journals.md)|
|Ordna och bearbeta ingående och utgående transaktioner som du skickar till din koncerninterna partner.|[Hantera koncerninterna in- och utkorgar](intercompany-how-manage-intercompany-inbox.md)|
|Använd koncerninterna bokföringar för att fördela kostnader mellan partnerföretag.|[Fördela kostnader till koncerninterna partner](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 30214f3fdd02343b064432a0f4f621e7a87765e9
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104291"
---
I följande tabell beskrivs några av de viktigaste rapporterna inom jobbrapportering.

|Rapportera |Objekt-ID|Beskrivning  |
|---------|---------|---------|
|**Projektanalys**|1008|Analyserar projektet med hjälp av inställningar som du anger. Du kan t.ex. skapa en rapport som innehåller budgeterade priser, förbrukningspriser, fakturerbara priser och sedan en jämförelse mellan de tre uppsättningarna av priserna.<br>Använd en kombination av de tillgängliga **Belopp**-fälten för att skapa en egen analys. För varje fält väljer du ett av följande värden för priser, kostnader eller vinst: Schema, Förbrukning, Kontrakt och Fakturerat. <br>Välj om valutan anges i lokal valuta eller utländsk valuta. |
|**Projektplaneringsrader**|1006|I den här rapporten visas de olika projektplanerings- och projektaktivitetsraderna – inklusive radtyp, antal, enhet, totalkostnader o.s.v.|
|**Projekt - utfall jmf. budget**|1009|Jämför planerade och förbrukade belopp för valda projekt. På alla rader för det valda projektet visas antal, totalkostnad och radbelopp. <br>Den här rapporten är avsedd för slutförda projekt, även om du kan använda den när som helst under ett projekt.<br>I USA, Kanada och Mexiko är inte den här rapporten tillgänglig. I stället använder du **Projet - utfall jmf. budget (kostnad)** (10210) eller **Projekt - utfall jmf. budget (pris)** (10211).|
|**Projekt - faktureringsförslag**|1011|Visar en lista över alla projekt, grupperade per kund, hur mycket kunden redan har fakturerats och hur mycket som återstår att faktureras, d.v.s. föreslagen fakturering. <br>I USA, Kanada och Mexiko är inte den här rapporten tillgänglig. Använd i stället rapporten **Projektkostnad - faktureringsförslag** (10219).|
|**Projekt per kund**|1012|Visar en lista över alla projekt, grupperade per kund. Med hjälp av rapporten kan du jämföra det planerade priset, färdigställningsgrad, det fakturerade priset och procentandel av fakturerade belopp för varje **faktureringskund**.|
|**Artiklar per projekt** eller **projekt per artikel**|1013 eller 1014|En översikt över de använda artiklarna i ett projekt. Beroende på vilken rapport du vill använda för att få en översikt över de planerade artiklarna för ett projekt, kan du ange ett ytterligare filter. I rapporten visas relevanta artiklar och ett ackumulerat värde för kostnaderna.|
|**Projekt - trans.detaljer**|1007|I den här rapporten får du en översikt över bokförda projektaktiviteter som resurser och artiklar. Innehåller detaljerad information om de totala kostnaderna och de totala priserna plus information om radrabatter o.s.v. Rapporten visar data från projekttransaktionerna.|
|**Projekt - PIA jmf. redovisning**|1010|Visar värdet för produkter i arbete för de projekt du väljer jämfört med det belopp som har bokförts i redovisningen.|
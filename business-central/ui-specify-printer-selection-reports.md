---
title: Skapa rapporter som ska skrivas ut på en viss skrivare | Microsoft Docs
description: Lär dig att ange en skrivare för en rapport och använda sidan Skrivarval.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/17/2020
ms.author: edupont
ms.openlocfilehash: 4bf794dd423a2049887eb1a4fe725a091fdbd190
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781191"
---
# <a name="set-up-printers"></a>Ställa in skrivare
Eftersom [!INCLUDE[prodshort](includes/prodshort.md)] är en molntjänst kan den inte nå lokala skrivare som är anslutna till användarnas datorer. Den kan emellertid ansluta till molnbaserade skrivare. I den generiska versionen av [!INCLUDE[prodshort](includes/prodshort.md)] har en molnskrivare med namnet **E-postskrivare** installerats som ett tillägg och är klar att användas efter den ursprungliga installationen.

Om en molnskrivare inte har installerats eller konfigurerats, eller om en installerad skrivare havererar, kommer utskriften att ske via webbläsarens standardalternativ för utskrift. Detta anges med det här värdet i fältet **Skrivare** på sidan för rapportförfrågan: *(ingen, hanteras av webbläsaren)*.

På sidan **Utskriftshantering** kan du se vilka skrivare som är inställda. När du har skapat en eller flera skrivare kan du öppna sidan **Skrivarhantering** och ange vilka specifika rapporter som ska skrivas ut för ditt användarkonto.

När du har skapat en skrivare och tilldelat denna till specifika rapporter kan du skriva ut en rapport genom att välja knappen **Skriv ut** på sidan för rapportbegäran. Mer information finns i [Skriva ut en rapport](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Ändra storlek på utskriftsjobb
Molnutskrift är utformat för dokument av rimligt storlek. De flesta molntjänster, inklusive PrintNode och HP ePrint, har en gräns på 10 MB per jobb. Om du behöver skriva ut större rapporter måste du kanske dela upp dem i flera utskrifter.

## <a name="to-set-up-a-printer"></a>Så här ställer du in en skrivare
På sidan **Skrivarhantering** kan du se de skrivare som har konfigurerats, och du kan även öppna sidan **Inställningar** för respektive skrivare i syfte att redigera en befintlig konfiguration eller installera en ny skrivare.

I följande procedur beskrivs hur du installerar den befintliga skrivaren **E-postskrivare**, som är ett förinstallerat tillägg.

> [!NOTE]
> Om du vill använda e-postutskrift måste du installera e-postfunktionen. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Skrivarhantering** och välj sedan relaterad länk.
2. Markera raden för **E-postskrivare** och välj sedan åtgärden **Redigera skrivarinställningar**.
3. På sidan **Inställningar** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du måste manuellt välja rätt pappersstorlek för en skrivare eftersom det varken finns någon lokal skrivare eller några användarinställningar som kan lagras.
    >
    > Tänk på att tillägget för e-postskrivare som standard är inställt på pappersformatet **A4**, vilket exempelvis inte lämpar sig för Nordamerika.
4. Om du vill göra en skrivare till standardskrivare får du till sidan **Utskriftshantering** och väljer **Ange som standardskrivare**.

### <a name="privacy-notice"></a>Sekretesspolicy
Om du använder tillägget för e-postskrivare skickas alla eller vissa utskriftsjobb till den e-postadress som du angav när du konfigurerade skrivaren. Vi rekommenderar starkt att ett unikt e-transaktion-ID kopplas till en skrivarenhet endast med de officiella tjänster som tillhandahålls av maskinvarutillverkaren, till exempel HP ePrint, KonicaMinolta EveryonePrint eller Epson Email Print.

Du måste vidta alla nödvändiga sekretessåtgärder, inklusive att se till lösningen för e-postutskrift har korrekt konfigurerade behörigheter, sekretessinställningar och lagringsmetoder. Det är ditt ansvar att skapa en korrekt, verifierad och fungerande e-postadress. Mer information finns i [Microsofts sekretesspolicy](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>För att välja vilka skrivare som ska skriva ut vilka rapporter

På sidan **Skrivarhantering** kan du för ditt användarkonto ange vilka rapporter som ska skrivas ut av vilken skrivare. Detta är användbart om du arbetar med olika rapporter som kräver olika skrivare på grund av sin placering i företaget eller deras utskriftskapacitet.

> [!IMPORTANT]
> För [!INCLUDE[prodshort](includes/prodshort.md)] lokalt kan sidan **Skrivarval** endast användas för skrivare som definieras av skrivartillägg. Det kan inte användas för lokala skrivare.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Skrivarhantering** och välj sedan relaterad länk. Du kan också välja sidan **Skrivarhantering** och sedan välja åtgärden **Skrivarhantering**.
2. Välj åtgärden **Ny** om du vill lägga till ett Skrivarhantering för en specifik rapport.
3. Fyll i fälten om det behövs.

Den angivna rapporten är nu konfigurerad för att skriva ut på den valda skrivaren som standard.

> [!NOTE]
> När du skriver ut rapporten i fråga kan du åsidosätta installationen genom att välja en annan skrivare på sidan för begäran om **Utskriftsinställningar**.

> [!NOTE]
> Om du inte anger en rapport för en viss skrivare på sidan **Skrivarhantering** kommer den att skrivas ut till företagets standardskrivare enligt definitionen på sidan **Skrivarhantering**.

Du eller administratören kan också använda sidan **Skrivarhantering** för att definiera andra utskriftsvariationer för användare och rapporter. I följande tabell beskrivs kombinationen av värdena för att ange olika utskriftsinställningar för en rapport.

|Till                                                 |Ange följande värden                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Skriv ut en rapport till en viss skrivare för alla användare |Ange värden i fälten **Rapport-ID** och **Skrivarnamn** och lämna fältet **Användar-ID** tomt.|
|Skriv ut alla rapporter till en viss skrivare för en specifik användare|Ange värden i fälten **Användar-ID** och **Skrivarnamn** och lämna fältet **Rapport-ID** tomt.|
|Ange standardskrivaren för alla rapporter|Ange ett värde i fälten **Skrivarnamn** och lämna fälten **Användar-ID** och **Rapport-ID** tomma.|
|Skriv ut en viss rapport till användarens standardskrivare|Ange ett värde i fältet **Rapport-ID** och lämna fälten **Skrivarnamn** och **Användar-ID** tomma.|
|Skriv ut en specifik rapport till en viss skrivare för en viss användare|Ange värden i samtliga tre fält.|

> [!NOTE]
> Mer specifika skrivarval har företräde framför mer allmänna skrivarval. Ett skrivarval som exempelvis har värden i fälten **Användar-ID**, **Rapport-ID** och **Skrivarnamn** har företräde framför ett skrivarval som innehåller tomma poster i fälten **Användar-ID** och **Rapport-ID**.

## <a name="see-also"></a>Se även
[Skriva ut en rapport](ui-work-report.md#PrintReport)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Kör batchjobb](ui-how-run-batch-jobs.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  

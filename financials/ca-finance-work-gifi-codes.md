---
title: GIFI-koder i Kanada | Microsoft Docs
Description: "I Kanada kan du ställa in General Index of Financial Information (GIFI)-koder och tilldela dem till redovisningskonton"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Så här arbetar du med GIFI-koder i Kanada
Skatteinformation kan inkludera redovisningskonton, rapporter, resultaträkningar, balansräkningar och rapporter över balanserad vinst och förlust. Skatteinformation grupperas med hjälp av koder. Hanteringen av koder hjälper regeringen att bearbeta information, förbereda sig för elektronisk arkivering och validera skatteinformation elektroniskt. Hanteringen av koder hjälper också statistiska organisationer att arbeta mer effektivt, eftersom den ekonomiska informationen är mer lättillgänglig. Mer information finns i [Webbplatsen för Canada Revenue Agency](http://www.cra-arc.gc.ca/).

Canada Revenue Agency använder det allmänna indexet av koder för ekonomisk information (GIFI) för att elektroniskt samla, verifiera och bearbeta ekonomisk information och skatteinformation. Det är bäst att endast tilldela GIFI-koder för bokföringskonton så att all summering görs av ditt skattförberedelseprogram.

När ett konto är kopplat till en GIFI-kod, rapporteras den till Revenue Agency med den koden. Flera konton kan använda samma GIFI-kod, men varje konto kan endast ha en GIFI-kod.

Du kan exportera information om saldo per GIFI-kod och spara den exporterade filen i Excel, vilket är användbart för att överföra information till ditt skattförberedelseprogram.

## <a name="to-set-up-gifi-codes"></a>Så här skapar du GIFI-koder:
I Dynamics NAV måste du lägga upp GIFI-koder för redovisningskonton, rapporter, balansräkningar, inkomstark och rapporter över balanserad vinst och förlust.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **GIFI-koder** och välj sedan relaterad länk.
2. I fönstret **GIFI-koder** väljer du åtgärden **Ny**.
3. Skapa GIFI-koder, genom att fylla i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>Om du vill koppla GIFI-koder med redovisningskonton
Om du vill rapportera ekonomiska information med GIFI-kod, måste varje GIFI-kod vara kopplad till korrekta konton i kontoplanen.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.
2. Välj ett relevant redovisningskonto och välj sedan åtgärden **Redigera**.
3. På snabbfliken **Kostnadsredovisning** i fältet **GIFI-kod** väljer du lämplig GIFI-kod.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Om du vill visa kontosaldon som använder GIFI-kodrapport
Du kan granska kontosaldon per GIFI-kod, genom att använda rapporten **kontosaldon per GIFI-kod**.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **kontosaldon per GIFI-kod** och välj sedan relaterad länk.
2. Ange vad som ska ingå i rapporten genom att fylla i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj knappen **Skriv ut** eller **Förhandsgranska**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Så här exporterar du saldoinformation med hjälp av GIFI-koder
Du kan exportera saldoinformation med hjälp av GIFI-koder och spara den exporterade filen i Excel. Du kan ändra, spara eller ta bort filen. Du kan använda den för att överföra information till ditt skattförberedelseprogram.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **GIFI-koder** och välj sedan relaterad länk.
2. Ange vad du vill exportera till Excel, genom att fylla i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Välj **OK**.

> [!NOTE]  
>   Excel-filen har följande egenskaper:

* Saldot avrundas till den närmaste procentsatsen, men cellvärdet behåller samma procentsats som i redovisningen.
* Negativa nummer representeras av positiva nummer i hakparenteser. -123 anges därför som (123).

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)   
[Ställa in Finance](finance-setup-finance.md)


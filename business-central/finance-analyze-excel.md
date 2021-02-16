---
title: Arbeta med finansiella rapporter i Excel
description: Lär dig mer om hur du öppnar de ekonomiska rapporterna i Microsoft Excel från Business Central för bättre analyser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 58c1d9bba8942dbd400a3ed0837ef7a39fd2bb13
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747147"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analysera finansiella rapporter i Microsoft Excel

I [!INCLUDE [prod_short](includes/prod_short.md)], kan du se KPI: er och få en översikt över företagets ekonomiska status. Du kan också öppna listor i Excel och analysera data där. Men du kan också exportera ekonomiska bokslut som balansräkningen eller resultaträkningen till Excel, analysera data och skriva ut rapporterna.  

Du kan välja vilka finansiella rapporter som ska visas i Excel från listrutan i avsnittet rapporter på menyfliken i Business Manager och rollcenter för redovisare. När du väljer en rapport öppnas den i Excel eller Excel Online. Ansluter data med ett tillägg på [!INCLUDE [prod_short](includes/prod_short.md)]. Men du måste logga in med samma konto som du använder med [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Få en översikt och detaljer i Excel

Välj önskad Excel-rapport på menyfliken och låt den öppnas så att du får en översikt som du söker efter. I den här versionen av [!INCLUDE [prod_short](includes/prod_short.md)], erbjuder vi följande Excel-rapporter:

- Balansräkning  
- Resultaträkning  
- Kassaflödesrapport  
- Balanserad vinst/förlust-rapport  
- Lev.skulder – ålder  
- Kundfordringar – ålder  

Anta att du vill expandera ämneslistan till kassaflödet. Du kan öppna rapporten **Kassaflödesanalys** i Excel från Business Manager eller rollcentret Revisor, men vad som händer egentligen är att vi exporterar aktuella data och skapar en Excel-arbetsbok baserat på en fördefinierad mall. Beroende på din webbläsare, kan du uppmanas att öppna eller spara arbetsboken.  

I Excel kan se du en flik där data placeras automatiskt i det första kalkylbladet. Alla data som har exporterats finns också i andra kalkylblad om du skulle behöva. Du kan skriva ut rapporten direkt eller ändra det tills du har översikten och den information som du vill använda. Använd [!INCLUDE [prod_short](includes/prod_short.md)] Excel-tillägg för att ytterligare filtrera och analysera data.  

### <a name="understanding-the-excel-templates"></a>Förstå Excel-mallarna

De fördefinierade Excel-rapporterna baseras på informationen i det aktuella företaget. Demonstrationsföretaget har till exempel lagt upp kontoplanen för att visa tre kassakonton under *Omsättningstillgångar*: 10100 **Checkräkningskonto**, 10200 **Sparkonto** och 10300 **Handkassa**. Kontona har fältet **Konto-underkategori** inställt på *Kontanter* och det är deras sammanlagda belopp som visas som *Kontanter* i Excel-rapporten **Balansräkning**.  

De övriga bladen i Excel-arbetsboken visar de data som ligger bakom rapporten. Men om du vill ta reda på vad som döljer sig bakom grupperingarna i Excel-rapporterna, kanske du måste gå tillbaka till [!INCLUDE [prod_short](includes/prod_short.md)] och tillämpa filter på listorna.  

## <a name="the-prod_short-excel-add-in"></a>[!INCLUDE [prod_short](includes/prod_short.md)] Excel tillägg

Din [!INCLUDE [prod_short](includes/prod_short.md)]-upplevelse inkluderar ett tillägg för Excel. Beroende på din prenumeration loggas du in automatiskt eller anger samma inloggningsinformation som används för [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Visa och redigera i Excel från Business Central](across-work-with-excel.md).  

Med tillägget, kan du uppdatera data från [!INCLUDE [prod_short](includes/prod_short.md)], och du kan skicka ändringar till [!INCLUDE [prod_short](includes/prod_short.md)]. Däremot inaktiveras sjkuta tillbaka till databasen för ekonomiska Excel-rapporterna i listan ovan.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Visa och redigera i Excel från Business Central](across-work-with-excel.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med Business Central](ui-work-product.md)  

---
title: Arbeta med finansiella rapporter i Excel
description: Lär dig mer om hur du öppnar de ekonomiska rapporterna i Microsoft Excel från Business Central för bättre analyser.
author: edupont04
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="analyzing-financial-statements-in-microsoft-excel" />Analysera finansiella rapporter i Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] tillhandahåller KPI:er och får översikter över ditt företags ekonomi. Nedan följer exempel på hur du kan analysera KPI:er och översikter i Excel:

* Öppna listor i Excel och analysera data. 
* Exportera ekonomiska bokslut som balansräkningen eller resultaträkningen till Excel, analysera data och skriva ut rapporterna.  

> [!TIP]
> Som standard är rapporterna som du kan visa i Excel utformade för att hjälpa dig att analysera det aktuella året. Rapporten resultaträkning är emellertid ett undantag. Med hjälp av rapporten kan du filtrera data så att de inkluderar föregående år i analyserna.

## <a name="getting-the-overview-and-the-details-in-excel" />Få en översikt och detaljer i Excel

I rollcenter för Chef och Revisor kan du med åtgärden **Rapporter** välja finansiella rapporter för att visa i Excel. När du väljer en rapport öppnas den i Excel eller Excel Online. Ansluter data med ett tillägg på [!INCLUDE [prod_short](includes/prod_short.md)]. Men du måste logga in med samma konto som du använder med [!INCLUDE [prod_short](includes/prod_short.md)]. I följande tabell visas rapporterna och var de är tillgängliga.  


|Rapportera  |Rollcenter  |
|---------|---------|
|Balansräkning                 | Chef, revisor |
|Resultaträkning              | Chef, revisor |
|Rapport över kassaflöden       | Chef, revisor |
|Rapport över balanserad vinst och förlust| Chef, revisor |
|Moms inbetalt         | Chef, revisor |
|Kundkontoutdrag           | Chef, revisor |
|Lev.skulder – ålder         | Revisor |
|Kundfordringar – ålder      | Revisor |

Anta att du vill expandera ämneslistan till kassaflödet. Du kan öppna rapporten **Rapport över kassaflöden** i Excel från Business Manager eller rollcentret Revisor, men vad som händer egentligen är att vi exporterar aktuella data och skapar en Excel-arbetsbok baserat på en fördefinierad mall. Beroende på din webbläsare, kan du uppmanas att öppna eller spara arbetsboken.  

I Excel kan se du en flik där data placeras automatiskt i det första kalkylbladet. Alla data som har exporterats finns också i andra kalkylblad om du skulle behöva. Du kan skriva ut rapporten direkt eller ändra det tills du har översikten och den information som du vill använda. Använd [!INCLUDE [prod_short](includes/prod_short.md)] Excel-tillägg för att ytterligare filtrera och analysera data.  

### <a name="understanding-the-excel-templates" />Förstå Excel-mallarna

De fördefinierade Excel-rapporterna baseras på informationen i det aktuella företaget. Demonstrationsföretaget har till exempel lagt upp kontoplanen för att visa tre kassakonton under *Omsättningstillgångar*: 10100 **Checkräkningskonto**, 10200 **Sparkonto** och 10300 **Handkassa**. Kontona har fältet **Konto-underkategori** inställt på *Kontanter* och det är deras sammanlagda belopp som visas som *Kontanter* i Excel-rapporten **Balansräkning**.  

De övriga bladen i Excel-arbetsboken visar de data som ligger bakom rapporten. Om du vill ta reda på vad som ligger bakom grupperingarna i Excel-rapporterna måste du kanske filtrera listorna i [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="the--excel-add-in" />[!INCLUDE [prod_short](includes/prod_short.md)] Excel tillägg

Din [!INCLUDE [prod_short](includes/prod_short.md)]-upplevelse inkluderar ett tillägg för Excel. Beroende på din prenumeration loggas du in automatiskt eller måste ange inloggningsinformation för [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Visa och redigera i Excel från Business Central](across-work-with-excel.md).  

Med tillägget, kan du uppdatera data från [!INCLUDE [prod_short](includes/prod_short.md)], och du kan skicka ändringar till [!INCLUDE [prod_short](includes/prod_short.md)]. Däremot inaktiveras skjuta tillbaka till databasen är inte tillgängligt för de finansiella rapporter du kan se i Excel.  

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Se även

[Visa och redigera i Excel från Business Central](across-work-with-excel.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Arbeta med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

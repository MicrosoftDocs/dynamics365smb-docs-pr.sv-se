---
title: Exportera dina Business Central-data till Excel
description: 'Du kan exportera dina finansiella rapporter och affärsinformationsdata från Business Central till Excel, eller också öppna dina data i Excel.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="export-your-business-data-to-excel" />Exportera dina affärsdata till Excel

Excel är ett kraftfullt verktyg för att arbeta med data. Du kan öppna valfri lista i Excel inifrån [!INCLUDE[prod_short](includes/prod_short.md)]. You can even modify data in Excel and then submit it back to [!INCLUDE [prod_short](includes/prod_short.md)]. På samma sätt kan du enkelt ta med dig dina data om du väljer att avbryta prenumerationen.

## <a name="opening-lists-in-excel" />Öppna listor i Excel

Du kan öppna data i Excel från valfri journal, lista eller kalkylblad. Öppna bara den sida som du vill använda och välj **öppna i Excel**. Öppna till exempel en lista över kunder (sök efter **kunder**) och välj sedan **öppna i Excel**. Din webbläsare uppmanar dig att öppna eller spara den genererade Excel-arbetsboken.  

> [!NOTE]
> Använd det här alternativet om du inte vill ändra och publicera ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)].  

Varje lista innehåller några kolumner. Exporten till Excel innehåller kolumner som är i den aktuella vyn. Ändra kolumnerna genom att öppna snabbmenyn för valfri kolumn och ange sedan vilka kolumner som ska visas. Listan över kolumner skiljer sig åt i de flesta listor. Kolumnerna återspeglar strukturen i databasen där dina data lagras. Om du är osäker på vilken typ av data en viss kolumn innehåller lägger du till den i vyn. Du kan alltid ta bort den igen.  

### <a name="edit-data-in-excel" />Redigera data i Excel

Din [!INCLUDE[prod_short](includes/prod_short.md)]-upplevelse omfattar ett tillägg för Excel som låter dig redigera data i Excel. Mer information finns i [analys av finansiella rapporter i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems" />Exportera data till andra finanssystem

Om du vill avbryta prenumerationen på [!INCLUDE[prod_short](includes/prod_short.md)], kan du på samma sätt exportera data till Excel så att du kan ta den med dig.  

Du kan exportera alla sidor, men det kan vara mer än vad du verkligen behöver. Så överväg att exportera följande viktiga sidor och kom ihåg att lägga till alla kolumner som beskrivits tidigare:  

* Kontoplan  
* Kunder  
* Leverantör  
* Banker  
* Artiklar  

Om du även vill ha med alla dina ekonomiska transaktioner, är detta stora mängder data, så exporten tar ofta mer än några minuter. De finansiella transaktionerna visas på sidan **redovisningstransaktioner**.  

Vi rekommenderar att du också överväger att exportera data från följande sidor:  

* Kundreskontratransaktioner  
* Lev.reskontratransaktioner  
* Bankkontotransaktioner  
* Artikeltransaktioner  
* Bokföringsinställningar  
* Kundbokföringsmallar  
* Leverantörsbokföringsmallar  
* Objektbokföringsmallar  
* Bankbokföringsmall  
* Redovisningsbudgetar  
* Redov.budgettransaktioner  
* Försäljningsofferter  
* Försäljningsfakturor  
* Inköpsfakturor  
* Kontakter  
* Säljare  

> [!NOTE]  
> Om du har ställt in flera företag i [!INCLUDE[prod_short](includes/prod_short.md)] måste du exportera aktuella data från båda företagen.

> [!NOTE]
> Du måste ha minst en av följande behörigheter för att kunna öppna eller redigera data i Excel:
>
> * Behörighetsgrupp *D365 Excel-export åtgärd*  
> * Systembehörighet 6110 *Tillåt åtgärd exportera till Excel*.  

Mer information finns i avsnittet [Så här får du en översikt en användares behörigheter](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics--business-centralindex" />Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Se även
[Avbryta prenumerationen på [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Ekonomi](finance.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

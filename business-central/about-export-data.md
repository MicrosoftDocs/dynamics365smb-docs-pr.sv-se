---
title: Exportera dina Business Central-data till Excel | Microsoft Docs
description: Du kan exportera dina finansiella rapporter och affärsinformationsdata från Business Central till Excel, eller också öppna dina data i Excel.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4a6bfb8d20c13019807b2308737380c4fd31dcc6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776503"
---
# <a name="exporting-your-business-data-to-excel"></a>Exportera affärsdata till Excel
Om du vill arbeta med data från [!INCLUDE[prod_short](includes/prod_short.md)] i Excel kan du öppna alla listor i Excel och arbeta med den där. Om du vill avbryta prenumerationen på [!INCLUDE[prod_short](includes/prod_short.md)], kan du på samma sätt exportera data till Excel så att du kan ta den med dig.

## <a name="opening-lists-in-excel"></a>Öppna listor i Excel
Du kan öppna data i Excel från valfri journal, lista eller kalkylblad. Öppna bara den sida som du vill använda och välj **öppna i Excel**. Öppna till exempel en lista över kunder (sök efter **kunder**) och välj sedan **öppna i Excel**. Din webbläsare uppmanar dig att öppna eller spara den genererade Excel-arbetsboken.  

> [!NOTE]
> Använd det här alternativet om du inte vill ändra och publicera ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)].  

Alla listor inkluderar ett antal kolumner och exportering till Excel inkluderar alla kolumner i den aktuella vyn. Om du vill lägga till eller ta bort kolumner innan du öppnar listan i Excel öppnar du bara snabbmenyn för en kolumn och anger sedan vilka kolumner som du vill visa. Denna lista över kolumner är olika för de flesta listor och återspeglar strukturen i databasen där data lagras. Om du inte vet vilken typ av data som en viss kolumn, kan du lägga till den i din vy och sedan bestämma dig för om du vill ta bort den igen.  

### <a name="edit-data-in-excel"></a>Redigera data i Excel
Din [!INCLUDE[prod_short](includes/prod_short.md)]-upplevelse omfattar ett tillägg för Excel som låter dig redigera data i Excel. Mer information finns i [analys av finansiella rapporter i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Exportera data till andra finanssystem
Om du vill avbryta prenumerationen på [!INCLUDE[prod_short](includes/prod_short.md)], kan du på samma sätt exportera data till Excel så att du kan ta den med dig.  

Du kan självklart exportera alla sidor, men det kan vara mer än vad du verkligen behöver. Så överväg att exportera följande viktiga sidor och kom ihåg att lägga till alla kolumner som beskrivits tidigare:  

* Kontoplan  
* Kunder  
* Leverantör  
* Banker  
* Artiklar  

Om du även vill ha med alla dina ekonomiska transaktioner, och är detta stora mängder data, tar exporten ofta mer än några minuter. De finansiella transaktionerna visas på sidan **redovisningstransaktioner**.  

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
>    - Behörighetsgrupp *D365 Excel-export åtgärd*  
>    - Systembehörighet 6110 *Tillåt åtgärd exportera till Excel*.  

Mer information finns i avsnittet [Så här får du en översikt en användares behörigheter](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Avbryta prenumerationen på [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Ekonomi](finance.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
---
title: Visa och redigera i Excel från Business Central (innehåller video)
description: Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 82d08e1c072f74434ad50943a97baf77712cb171
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529413"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Visa och redigera i Excel från Business Central

Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du exportera listan till Microsoft Excel och visa den här. Beroende på sidan finns det två alternativ för att visa i Excel. Båda alternativen är tillgängliga på **delning** ikonen ![dela en sida i ett annat program.](media/share-icon.png) högst upp på sidan. Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan. I den här artikeln beskrivs skillnaderna mellan de två åtgärderna.

## <a name="open-in-excel"></a>Öppna i Excel

Med instruktionen **Öppna i Excel** kan du göra ändringar i posterna i Excel, men du kan inte publicera tillbaka ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bara spara ändringarna i Excel-filen utan att påverka data i [!INCLUDE[prod_short](includes/prod_short.md)].

- Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas. Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prod_short](includes/prod_short.md)].

- Den här åtgärden fungerar både i Windows och macOS.

- Från och med uppdatering 18.3 kan du även visa listor som visas i sid delar, till exempel raderna i en försäljningsorder. 

> [!NOTE]
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard. Om du däremot ställer in [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Redigera i Excel

Åtgärden **redigera i Excel** är tillgänglig i de flesta listor, men inte för alla. Med instruktionen **Redigera i Excel** kan du göra ändringar i posterna i Excel, men du kan inte publicera tillbaka ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)]. När Excel öppnas visas rutan **Excel-tillägg** till höger.

- Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar posterna som visas, varför Excel-arbetsboken kommer att innehålla nästan samma poster och kolumner.

- Om du vill hämta senaste data från [!INCLUDE[prod_short](includes/prod_short.md)] väljer du **uppdatera** i fönstret Excel-tillägg.

- Du kan växla företaget som du arbetar med. Om du vill byta företag väljer du ikonen **alternativ** för ![Excel-tillägget.](media/cogwheel.png "Alternativ för Excel-tillägg") i fönstret Excel-tillägg markerar du företaget från fältet **företag**.  

    > [!IMPORTANT]
    > Kontrollera att fältet **Miljö** fältet inte är tomt när du byter företag. Om så är fallet gör du det till ett av de tillgängliga alternativen, annars kommer tillägget inte att fungera korrekt.  

Om du gör ändringar i tillägget måste du ladda det på nytt för att uppdatera anslutningen. Om du vill läsa in på nytt använder du ![menyn tilläggsprogram för Excel](media/excel-addin-menu.png "Meny Excel tillägg") i det övre högra hörnet i tillägget. Om du inte kan läsa in tillägget, kontakta administratören. Om du är administratör, se [Hämta Business Central-tillägget för Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Tillägget fungerar med Excel för webben (online) från alla enheter, så länge som det finns stöd för webbläsare som stöds. Det fungerar även med Excel-appen för Windows (PC) men inte för macOS.
>
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören, och det är då endast tillgängligt för webbklienten. För administratörer: Om du vill veta hur du installerar Excel-tillägget, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Första inloggningen

Åtgärden **redigera i Excel** kräver att Business Central-tillägget är installerat i Excel. I vissa fall kan din administratör ha konfigurerat tillägget så att det installeras automatiskt åt dig. I det här fallet behöver du bara logga in i rutan Business Central i **Excel-tillägget** med ditt användarnamn och lösenord. I annat fall öppnas fönstret **nytt Office-tillägg**. För att du ska kunna installera tillägget väljer användaren att **lita på det här tillägget**, som i sin tur installerar tillägget direkt från Office Store.

Om tillägget av någon anledning inte installeras kontaktar du administratören eller försöker installera det manuellt. För mer information, se [installera tillägget manuellt för egen användning](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Se skillnaden mellan alternativen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med Business Central](ui-work-product.md)  
[Förbättringar av Excel-integrering i 2019 års utgivningscykel 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

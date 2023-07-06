---
title: Visa och redigera i Excel från Business Central (innehåller video)
description: Lär dig mer om hur du öppnar sidor i Microsoft Excel från Business Central för bättre dataanalyser.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><a name="viewing-and-editing-in-excel-from-business-central"></a><a name="viewing-and-editing-in-excel-from-business-central"></a>Visa och redigera i Excel från Business Central

Med sidor som visar en lista över poster i rader och kolumner som en lista över kunder, försäljningsorder eller fakturor, kan du exportera listan till Microsoft Excel och visa den här. Beroende på sidan finns det två alternativ för att visa i Excel. Båda alternativen är tillgängliga på **delning** ikonen ![dela en sida i ett annat program.](media/share-icon.png) högst upp på sidan. Du kan antingen markera åtgärden **öppna i Excel** eller **redigera i Excel** på sidan. I den här artikeln beskrivs de två åtgärderna.

## <a name="open-in-excel"></a><a name="open-in-excel"></a><a name="open-in-excel"></a>Öppna i Excel

Med instruktionen **Öppna i Excel** kan du göra ändringar i posterna i Excel, men du kan inte publicera tillbaka ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bara spara ändringarna i Excel-filen utan att påverka data i [!INCLUDE[prod_short](includes/prod_short.md)].

- Med den här åtgärden respekterar Excel eventuella filter som begränsar poster som visas. Excel-arbetsboken innehåller samma rader och kolumner som visas på sidan i [!INCLUDE[prod_short](includes/prod_short.md)].

- Den här åtgärden fungerar både i Windows och macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

> [!IMPORTANT]
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Öppna i Excel** tillgänglig som standard. Om du däremot ställer in [!INCLUDE[prod_short](includes/prod_short.md)] lokalt för redigering av data i Excel, ersätts åtgärden **Öppna i Excel** av åtgärden **Redigera i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> I Excel får heltal i kolumner en decimalsymbol (som punkt `.` eller komma `,`) även om decimaltecknet inte visas i Business Central. Decimaltecknet beror på enhetens regionsinställningar. Till exempel i `10` i Business Central visas som `10.` eller `10,` i Excel. Du kan ändra formatet i Excel genom att markera värdena och sedan välja <kbd>Ctrl</kbd>+<kbd>1</kbd>. Om du vill veta mer om hur du ändrar nummerformatet i Excel går du till [formatera nummer](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).


## <a name="edit-in-excel"></a><a name="edit-in-excel"></a><a name="edit-in-excel"></a>Redigera i Excel

Åtgärden **redigera i Excel** är tillgänglig i de flesta listor, men inte för alla. Med instruktionen **Redigera i Excel** kan du göra ändringar i posterna i Excel, men du kan inte publicera tillbaka ändringarna till [!INCLUDE[prod_short](includes/prod_short.md)]. När Excel öppnas visas rutan **Excel-tillägg** till höger.

- Med den här åtgärden respekterar Excel de flesta filter på sidan som begränsar posterna som visas, varför Excel-arbetsboken kommer att innehålla nästan samma poster och kolumner.

- Om du vill hämta senaste data från [!INCLUDE[prod_short](includes/prod_short.md)] väljer du **Uppdatera** i fönstret Excel-tillägg.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### <a name="first-time-sign-in"></a><a name="first-time-sign-in"></a><a name="first-time-sign-in"></a>Första inloggningen

Åtgärden **redigera i Excel** kräver att Business Central-tillägget är installerat i Excel. I vissa fall kan din administratör ha konfigurerat tillägget så att det installeras automatiskt åt dig. I det här fallet behöver du bara logga in i rutan Business Central i **Excel-tillägget** med ditt användarnamn och lösenord. I annat fall öppnas fönstret **nytt Office-tillägg**. För att du ska kunna installera tillägget väljer användaren att **lita på det här tillägget**, som i sin tur installerar tillägget direkt från Office Store.

Om tillägget inte installeras kontaktar du administratören eller försöker installera det manuellt. För mer information, se [installera tillägget manuellt för egen användning](admin-deploy-excel-addin.md#install).

### <a name="work-across-environments-and-companies"></a><a name="work-across-environments-and-companies"></a><a name="work-across-environments-and-companies"></a>Arbeta i flera miljöer och företag

Du kan växla företaget som du arbetar med. Om du vill byta företag väljer du ikonen **alternativ** för ![Excel-tillägget.](media/cogwheel.png "Alternativ för Excel-tillägg") i fönstret Excel-tillägg markerar du företaget från fältet **företag**.  

> [!IMPORTANT]
> Kontrollera att fältet **Miljö** fältet inte är tomt när du byter företag. Om så är fallet gör du det till ett av de tillgängliga alternativen, annars kommer tillägget inte att fungera korrekt.  

Om du gör ändringar i tillägget måste du ladda det på nytt för att uppdatera anslutningen. Om du vill läsa in på nytt använder du ![menyn tilläggsprogram för Excel](media/excel-addin-menu.png "Meny Excel tillägg") i det övre högra hörnet i tillägget. Om du inte kan läsa in tillägget, kontakta administratören. Om du är administratör, se [Hämta Business Central-tillägget för Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Tillägget fungerar med Excel för webben (online) från alla enheter, så länge som det finns stöd för webbläsare som stöds. Det fungerar även med Excel-appen för Windows (PC) men inte för macOS.
>
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokalt är åtgärden **Redigera i Excel** endast tillgänglig om Excel-tillägget har konfigurerats av administratören, och det är då endast tillgängligt för webbklienten. För administratörer: Om du vill veta hur du installerar Excel-tillägget, se [Ställa in Excel-tillägget för redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="limits-when-using-excel-for-the-web"></a><a name="limits-when-using-excel-for-the-web"></a><a name="limits-when-using-excel-for-the-web"></a>Begränsningar när du använder Excel för webben

När **Redigera i Excel** används på listsidor för tabeller med många kolumner, kan det hända att den resulterande arbetsboken har för många kolumner i filen som visas i Excel för webben. [!INCLUDE[prod_short](includes/prod_short.md)] begränsar automatiskt den exporterade arbetsboken till 100 kolumner när OneDrive är konfigurerad för systemfunktioner. 

## <a name="see-the-differences-between-the-options"></a><a name="see-the-differences-between-the-options"></a><a name="see-the-differences-between-the-options"></a>Se skillnaden mellan alternativen
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med Business Central](ui-work-product.md)  
[Förbättringar av Excel-integrering i 2019 års utgivningscykel 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Business Central och OneDrive för företag-integration
description: 'Du kan använda OneDrive för företag för att lagra, hantera och dela filer, t.ex. rapporter eller bifogade filer. Även om du stavar det One Drive.'
author: jswymer
ms.topic: overview
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central och OneDrive för företag-integration

OneDrive för företag är en molnlagringstjänst som ingår i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] med är det enkelt att lagra, hantera och dela filer med andra människor via OneDrive. När en fil finns i din OneDrive kan du använda de omfattande samarbetsfunktionerna från online-versioner av Microsoft-produkter, till exempel Word, Excel och PowerPoint. Du kan t.ex. dela ett Word-dokument och sedan och dina kollegor kan redigera det tillsammans i realtid. OneDrive kan du också öppna andra typer av filer, till exempel PDF-filer. 

## <a name="get-started-with-onedrive-features"></a>Kom igång med OneDrive-funktioner

Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] online har vi redan skapat anslutningen mellan [!INCLUDE[prod_short](includes/prod_short.md)] online och OneDrive, så det är lätt att komma igång. Det enda kravet är att användare har öppnat OneDrive minst en gång. Med [!INCLUDE[prod_short](includes/prod_short.md)] lokalt måste en administratör konfigurera anslutningen innan du kan komma igång. Läs mer i [Hantera OneDrive-integrering med Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### <a name="open-and-share-in-onedrive"></a>Öppna och dela i OneDrive

På de flesta sidor där det finns filer, t.ex. Rapportinkorgen eller filer som är bifogade till poster, finns åtgärderna **Öppna i OneDrive** och **Dela**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för bilagor":::

|Markera...|Till...|Mer info...|
|---------|-----|----------------|
|Öppna i OneDrive|Kopiera filen till Business Central-mapp i din OneDrive och öppna filen.|[Öppna i OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Andel|Kopiera filen till din OneDrive och dela den med andra användare.|[Dela i OneDrive](across-share-onedrive.md#share) |

### <a name="save-excel-workbooks-and-report-files-in-onedrive"></a>Spara Excel-arbetsböcker och rapportera filer i OneDrive

Med OneDrive-integrering konfigurerad använder ett par andra välbekanta funktioner automatiskt OneDrive för att spara filer istället för att spara filer på enheten:

- Åtgärderna **Öppna i Excel** och **Redigera i Excel** på listsidor kopierar automatiskt Excel-filen till OneDrive och öppnar den sedan i Excel Online. Mer information finns i [Visa och redigera i Excel](across-work-with-excel.md).
- När du skickar en rapport till en Excel- eller Word-fil kopieras filen automatiskt till OneDrive och öppnas sedan i Excel eller Word online. Mer information finns i [Spara en rapport till en fil](ui-work-report.md#saving-a-report-to-a-file).

Dessa funktioner är inte aktiverade som standard. Men som administratör kan du enkelt aktivera dem med hjälp av guiden för assisterad konfiguration **OneDrive-konfiguration**.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Du kan också ansluta lokala [!INCLUDE[prod_short](includes/prod_short.md)] platser till OneDrive. Det finns dock några saker du bör göra för att det ska fungera. Mer information finns i [Konfigurera Business Central lokalt](admin-onedrive-integration-onpremises.md).

## <a name="see-also"></a>Se även

[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)  

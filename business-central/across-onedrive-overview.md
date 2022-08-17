---
title: Business Central och OneDrive för företag-integration
description: Du kan använda OneDrive för företag för att lagra, hantera och dela filer, t.ex. rapporter eller bifogade filer. Även om du stavar det One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 06adf2a30a7487fa3bc66e1aebec42e6c55184e2
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227425"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central och OneDrive för företag-integration

OneDrive för företag är en molnlagringstjänst som ingår i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] med är det enkelt att lagra, hantera och dela filer med andra människor via OneDrive. När en fil finns i din OneDrive kan du använda de omfattande samarbetsfunktionerna från online-versioner av Microsoft-produkter, till exempel Word, Excel och PowerPoint. Du kan t.ex. dela ett Word-dokument och sedan och dina kollegor kan redigera det tillsammans i realtid. OneDrive kan du också öppna andra typer av filer, till exempel PDF-filer. 

## <a name="get-started"></a>Kom i gång

Vi har skapat anslutningen mellan [!INCLUDE[prod_short](includes/prod_short.md)] online och OneDrive så är det lätt att komma igång. Det enda kravet är att användare har öppnat OneDrive minst en gång. 

På de flesta sidor där det finns filer, t.ex. Rapportinkorgen eller filer som är bifogade till poster, finns åtgärderna **Öppna i OneDrive** och **Dela**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för bilagor":::

|Markera...|Till...|Mer info...|
|---------|-----|----------------|
|Öppna i OneDrive|Kopiera filen till Business Central-mapp i din OneDrive och öppna filen.|[Öppna i OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Andel|Kopiera filen till din OneDrive och dela den med andra användare.|[Dela i OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Du kan också ansluta lokala [!INCLUDE[prod_short](includes/prod_short.md)] platser till OneDrive. Det finns dock några saker du bör göra för att det ska fungera. Mer information finns i [Konfigurera Business Central lokalt](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Se även

[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)
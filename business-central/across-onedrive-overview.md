---
title: Business Central och OneDrive för företag-integration
description: Du kan använda OneDrive för företag för att lagra, hantera och dela filer, t.ex. rapporter eller bifogade filer.
author: brentholtorf
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 522bf01d08e77e52b4fbcf32f2652c53208cf8ec
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381835"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central och OneDrive för företag-integration
OneDrive för företag är en molnlagringstjänst som ingår i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] med är det enkelt att lagra, hantera och dela filer med andra människor via OneDrive. När en fil finns i din OneDrive kan du använda de omfattande samarbetsfunktionerna från online-versioner av Microsoft-produkter, till exempel Word, Excel och PowerPoint. Du kan t.ex. dela ett Word-dokument och sedan och dina kollegor kan redigera det tillsammans i realtid. OneDrive kan du också öppna andra typer av filer, till exempel PDF-filer. 

## <a name="getting-started"></a>Komma igång
Vi har skapat anslutningen mellan [!INCLUDE[prod_short](includes/prod_short.md)] online och OneDrive så är det lätt att komma igång. Det enda kravet är att användare har öppnat OneDrive minst en gång. 

På de flesta sidor där det finns filer, t.ex. en rapport från inkorgen eller filer som är bifogade till poster, finns det en åtgärd **öppen i OneDrive**.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="Öppen i OneDrive åtgärd":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Dela bifogade filer i OneDrive":::

När du använder åtgärden **Öppna i OneDrive** första gången [!INCLUDE[prod_short](includes/prod_short.md)] gör följande i OneDrive:

1. Skapar en mapp som heter [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. I [!INCLUDE[prod_short](includes/prod_short.md)] mappen skapas en annan mapp med samma namn som det företag som du arbetar i. Om du arbetar i mer än ett företag skapas en mapp för det företag som du arbetar i när du använder åtgärden **öppna i OneDrive**. 
3. Placerar en kopia av filen som du markerade i mappen och öppnar sedan filen. Nästa gång du använder åtgärden kopieras bara filen och öppnas. 

Mappen och dess innehåll är privata tills du bestämmer dig för att dela dem med andra. Du kanske till exempel vill dela med dig av innehållet till en eller flera medarbetare eller till och med personer utanför organisationen. Mer information finns i [Dela OneDrive-filer och mappar](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Du kan också ansluta lokala [!INCLUDE[prod_short](includes/prod_short.md)] platser till OneDrive. Det finns dock några saker du bör göra för att det ska fungera. Mer information finns i [Konfigurera Business Central lokalt](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Se även
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)
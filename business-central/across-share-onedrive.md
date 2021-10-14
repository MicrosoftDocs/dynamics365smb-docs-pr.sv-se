---
title: Använda OneDrive för företag med Business Central
description: Du kan använda OneDrive för företag för att lagra, hantera och dela filer, t.ex. rapporter eller bifogade filer.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 92896af6888ef5c39288d511e61d343d3e384a83
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589527"
---
# <a name="opening-business-central-files-in-onedrive"></a>Öppna Business Central-filer i OneDrive
[!INCLUDE[prod_short](includes/prod_short.md)] med är det enkelt att lagra, hantera och dela filer med andra människor via OneDrive för företag. På de flesta sidor där det finns filer, t.ex. en rapport från inkorgen eller filer som är bifogade till poster, finns det en åtgärd **öppen i OneDrive**.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="Öppen i OneDrive åtgärd":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Dela bifogade filer i OneDrive":::

## <a name="working-with-different-types-of-files"></a>Arbeta med olika typer av filer
När du väljer **Öppna i OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifierar Excel, Word och PowerPoint filer och öppnar dem i sina onlineappar, det vill säga, Excel online, Word online och PowerPoint online. Du kan kommentera, redigera och samarbeta med andra utan att lämna webbläsaren. 

För andra populära filtyper, till exempel PDF-filer, textfiler och bilder, OneDrive finns det fil visningsprogram som erbjuder funktioner för att skriva ut, dela med mera. Om det inte går att visa en fil i OneDrive kan du bli ombedd att hämta den. 

## <a name="managing-multiple-copies-of-a-file"></a>Hantera flera kopior av en fil
När du väljer **Öppna i OneDrive** kopieras filen från [!INCLUDE[prod_short](includes/prod_short.md)] till mappen i OneDrive. Om du redigerar filen i blir OneDrive kopiorna av filen olika. Om du vill uppdatera [!INCLUDE[prod_short](includes/prod_short.md)] med den senaste filen tar du bort den befintliga filen [!INCLUDE[prod_short](includes/prod_short.md)] och överför sedan den senaste kopian.

När du använder åtgärden öppna i OneDrive och en fil med det namnet redan finns i OneDrive, [!INCLUDE[prod_short](includes/prod_short.md)] kan du välja mellan att ersätta filen eller att behålla båda filerna. Om du väljer att behålla båda filerna kopieras den nya filen till OneDrive och dess filnamn ges ett suffix, till exempel "objekt (2). xlsx" och originalfilen ändras inte. 

Om du väljer att ersätta filen kommer den nya filen att läggas till i versionshistoriken för filen. Den ursprungliga filen förloras inte och du kan visa eller återställa tidigare versioner av filen. 

## <a name="accessing-your-onedrive"></a>Komma åt din OneDrive
Du kan öppna på sidan OneDrive från **mina inställningar** genom att välja länken i fältet **molnlagring**.

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Fältet för molnlagring i mina inställningar":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Se även
[Business Central och OneDrive integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)
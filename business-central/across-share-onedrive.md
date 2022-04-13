---
title: Öppna Business Central-filer i OneDrive
description: Lär dig hur du kan dela Business Central-data genom OneDrive för företag.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516427"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Öppna och dela Business Central-filer i OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] med är det enkelt att lagra, hantera och dela filer med andra människor via OneDrive för företag. På de flesta sidor där det finns filer, t.ex. Rapportinkorgen eller filer som är bifogade till poster, finns åtgärderna **Öppna i OneDrive** och **Dela**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för bilagor":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Öppna i OneDrive

Med åtgärden **Öppna i OneDrive** kopieras filen till din OneDrive och öppnas i deras online-program, till exempel Excel Online, Word Online och PowerPoint Online. 

<!--## Working with Different Types of Files-->

När du väljer **Öppna i OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifierar Excel, Word och PowerPoint filer och öppnar dem i sina onlineappar, det vill säga, Excel online, Word online och PowerPoint online. Du kan kommentera, redigera och samarbeta med andra utan att lämna webbläsaren.

För andra populära filtyper, till exempel PDF-filer, textfiler och bilder, erbjuder OneDrive filvisningsprogram med funktioner för att skriva ut, dela med mera. Om det inte går att visa en fil i OneDrive kan du bli ombedd att hämta den.

## <a name="share"></a>Andel

Med åtgärden **Dela** kopierar du filen till din OneDrive, kan dela filen med andra användare och ser vem du redan har delat filen med. När du väljer åtgärden **Dela** öppnas följande sida.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Dela fil i OneDrive":::

Om du känner till OneDrive kanske du känner igen sidan. Du kan dela filen på två olika sätt: **Skicka länk** och **Kopiera länk**.

- **Skicka länk** gör att du kan dela filer med vissa personer. De personer som du delar filen med får ett e-postmeddelande med en länk till filen. Filen kommer också att visas i avsnittet **Delat** i deras OneDrive. Börja med att skriva in e-postadresser eller kontaktnamn i **fältet Namn, Grupp eller E-postadress**.

- **Kopiera länk** kopierar en länk till filen på din OneDrive så sätt att du kan använda länken på andra platser, t.ex. Facebook, Twitter eller i e-post. 

Innan du skickar eller kopierar länken bör du ställa in den behörighet för filen som du vill att andra ska ha. Du kan se aktuell inställning under **Skicka länk** och **Kopiera länk**. I de flesta fall är detta **Alla med länken som kan redigera för att öppna länken**, beroende på vilka inställningar som har angetts av administratören. Om du vill ändra behörigheterna markerar du länken och gör ändringar på sidan **Länkinställningar**.

Delningsfunktionen i Business Central baseras på OneDrive. Mer information om delning och behörigheter finns i [Dela OneDrive-filer och -mappar](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Åtgärden **Dela** är inte tillgänglig i Business Central-appen för mobila enheter.

## <a name="first-time-sign-in-from-business-central"></a>Första gången du loggar in från Business Central

När du använder åtgärden **Öppna i OneDrive** eller **Dela** för första gången gör [!INCLUDE[prod_short](includes/prod_short.md)] följande:

1. Öppnar sidan **Läs igenom regler och villkor**. Läs sidan och godkänn regler och villkor genom att välja **Godkänn** för att fortsätta.
2. Öppnar sidan **Välj ett konto** . Välj ditt konto eller **använd ett annat konto** - om du inte ser ditt eget konto anger du användarnamn och lösenord när du ombeds göra det.
3. Skapar en mapp kallad [!INCLUDE[prod_short](includes/prod_short.md)] i OneDrive. 
4. I [!INCLUDE[prod_short](includes/prod_short.md)] mappen skapas en annan mapp med samma namn som det företag som du arbetar i. Om du arbetar i mer än ett företag skapas en mapp för företaget du jobbar för när du använder åtgärderna **Öppna i OneDrive** och **Dela**. 
5. Placerar en kopia av filen som du markerade i mappen och öppnar sedan filen. Nästa gång du använder åtgärden kopieras bara filen och öppnas. 

## <a name="managing-multiple-copies-of-a-file"></a>Hantera flera kopior av en fil

När du väljer **Öppna i OneDrive** eller **Dela** kopieras filen från [!INCLUDE[prod_short](includes/prod_short.md)] till din mapp i OneDrive. Om du redigerar filen i blir OneDrive kopiorna av filen olika. Om du vill uppdatera [!INCLUDE[prod_short](includes/prod_short.md)] med den senaste filen tar du bort den befintliga filen [!INCLUDE[prod_short](includes/prod_short.md)] och överför sedan den senaste kopian.

När en fil med samma namn redan finns i OneDrive kommer [!INCLUDE[prod_short](includes/prod_short.md)] dessutom att tillhandahålla ett val att antingen byta ut filen eller behålla båda filer. Om du väljer att behålla båda filerna kopieras den nya filen till OneDrive och tilldelas ett filnamn med suffix, t.ex. "Objekt (2).xlsx". Den ursprungliga filen har inte ändrats. 

Om du väljer att ersätta filen kommer den nya filen att läggas till i versionshistoriken för filen. Den ursprungliga filen förloras inte och du kan visa eller återställa tidigare versioner av filen. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Om din Business Central-mapp på OneDrive

Mappen och dess innehåll är privata tills du bestämmer dig för att dela dem med andra. Du kanske till exempel vill dela med dig av innehållet till en eller flera medarbetare eller till och med personer utanför organisationen. Du kan öppna på sidan OneDrive från **mina inställningar** genom att välja länken i fältet **molnlagring**. Mer information finns i [Dela OneDrive-filer och mappar](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Fältet för molnlagring i mina inställningar":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Se även
[Business Central- och OneDrive-integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)
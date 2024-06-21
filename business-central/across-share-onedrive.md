---
title: Öppna Business Central-filer i OneDrive
description: Lär dig hur du kan dela Business Central-data genom OneDrive för företag.
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a>Öppna och dela Business Central-filer i Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] gör det enkelt att lagra, hantera och dela filer med andra människor via Microsoft OneDrive för företag. På de flesta sidor där det finns filer, t.ex. Rapportinkorgen eller när filer är bifogade till poster, finns åtgärderna **Öppna i OneDrive** och **Dela**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Åtgärderna Öppna i OneDrive och Dela för bilagor":::


## <a name="open-in-onedrive"></a>Öppna i OneDrive

Med åtgärden **Öppna i OneDrive** kopieras filen till OneDrive och sedan öppnas filen i ett program som Microsoft Excel online, Microsoft Word online eller Microsoft PowerPoint online. 

<!--## Working with different types of files-->

När du väljer **Öppna i OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifierar Excel, Word och PowerPoint filer och öppnar dem i sina onlineappar, det vill säga, Excel online, Word online och PowerPoint online. 

Med online-versionerna av de här programmen kan du anteckna, redigera och samarbeta med andra utan att lämna webbläsaren.

För andra populära filtyper, till exempel PDF-filer, textfiler och bilder, OneDrive finns det fil visningsprogram som erbjuder funktioner för att skriva ut, dela med mera. Om det inte går att visa en fil i OneDrive kan du bli ombedd att hämta den.

## <a name="share"></a>Dela

Med åtgärden **Dela** kopierar du filen till din OneDrive, så att du kan se vilka du redan har delat den med samt dela filen med andra användare. När du väljer åtgärden **Dela** öppnas följande sida.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Dela fil i OneDrive":::

Om du känner till OneDrive kanske du känner igen den ovannämnda sidan. Du ser att du kan dela filen på två olika sätt: **Skicka länk** och **Kopiera länk**.

- **Skicka länk** gör att du kan dela filer med vissa personer. De personer som du delar filen med får ett e-postmeddelande med en länk till filen. Filen kommer också att visas i avsnittet **Delat** i deras OneDrive. Börja med att skriva in e-postadresser eller kontaktnamn i **fältet Namn, Grupp eller E-postadress**. Inkludera ett meddelande under  **Namn, grupp eller epostfält** om du vill.

  > [!TIP]
  > Om du vill skriva meddelandet i Outlook väljer du **Outlook**-knappen. Länken infogas i ett utkast-e-postmeddelande och alla som du har angett att dela med finns i listan **Till**. Med det här alternativet kan du skriva e-postmeddelanden med hjälp av alla funktioner i Outlook, t.ex. formatera text, lägga till andra bifogade filer, infoga bilder eller tabeller och lägga till mottagare av kopia eller hemlig kopia.

- **Kopiera länk** kopierar en fillänk du kan använda för att dela filen via program som Facebook, Twitter eller e-post. 

Innan du skickar eller kopierar en fillänk bör du ställa in den behörighetsnivå som du vill att andra ska ha. Du kan se aktuell inställning under **Skicka länk** eller **Kopiera länk**. I de flesta fall är detta **Alla med länken som kan redigera**, beroende på administratörens inställningar. Om du vill ändra behörigheterna markerar du länken och gör ändringar på sidan **Länkinställningar**.

Delningsfunktionen i Business Central baseras på OneDrive. Läs mer om OneDrive-delning och -behörigheter på [Dela OneDrive-filer och -mappar](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Åtgärden **Dela** är inte tillgänglig i Business Central-appen för mobila enheter.

## <a name="first-time-sign-in-from-business-central"></a>Första gången du loggar in från Business Central

När du använder åtgärden **Öppna i OneDrive** eller **Dela** för första gången gör [!INCLUDE[prod_short](includes/prod_short.md)] följande:

1. Öppnar sidan **Läs igenom regler och villkor**. Läs sidan och godkänn regler och villkor genom att välja **Godkänn** för att fortsätta.
2. Skapar en mapp kallad [!INCLUDE[prod_short](includes/prod_short.md)] i OneDrive. 
3. I [!INCLUDE[prod_short](includes/prod_short.md)]-mappen skapas en mapp med samma namn som det företag som du arbetar i. Om du arbetar i mer än ett företag skapar [!INCLUDE[prod_short](includes/prod_short.md)] en mapp för varje företag du jobbar för när du använder åtgärden **Öppna i OneDrive** eller **Dela**. 
4. Placerar en kopia av filen som du valde i företagsnamnmappen och öppnar sedan filen. 

Nästa gång du använder åtgärden **Öppna i OneDrive** eller **Dela** kopierar och öppnar [!INCLUDE[prod_short](includes/prod_short.md)] filen. 

## <a name="managing-multiple-copies-of-a-file"></a>Hantera flera kopior av en fil

När du väljer **Öppna i OneDrive** eller **Dela** kopieras filen från [!INCLUDE[prod_short](includes/prod_short.md)] till din mapp i OneDrive. Om du redigerar filen i OneDrive blir den filen annorlunda mot [!INCLUDE[prod_short](includes/prod_short.md)]-filen. Om du vill uppdatera [!INCLUDE[prod_short](includes/prod_short.md)] med den senaste filversionen tar du bort den befintliga filen från [!INCLUDE[prod_short](includes/prod_short.md)] och överför sedan den senaste kopian.

Om en fil med samma namn redan finns i OneDrive får du följande alternativ:

- **Använd befintlig**

  Det här alternativet öppnar eller delar filen som redan är lagrad i OneDrive, i stället för att kopiera filen från Business Central.
  
- **Byt ut**
  
  Det här alternativet ersätter den befintliga filen i OneDrive med den fil som du valde från Business Central. Den ursprungliga filen är inte förlorad&mdash;du kan se och återställa den med versionshistoriken i OneDrive. Läs mer i [Återställ en tidigare version av en fil som lagras i OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive-159cad6d-d76e-4981-88ef-de6e96c93893).

- **Behåll båda**

  Det här alternativet behåller den befintliga filen som den är och sparar filen du valde från Business Central under ett annat namn. Det nya namnet liknar det befintliga namnet, utom med ett suffixnummer som "Artiklar (2).xlsx".

## <a name="about-your-business-central-folder-on-onedrive"></a>Om din Business Central-mapp på OneDrive

Mappen och dess innehåll är privata tills du bestämmer dig för att dela dem med andra. Du kanske vill dela med dig av innehållet till en eller flera medarbetare eller till och med personer utanför organisationen. 

Du kan öppna på sidan OneDrive från **mina inställningar** genom att välja länken i fältet **molnlagring**. Läs mer i [Dela OneDrive-filer och -mappar](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Fältet för molnlagring i mina inställningar":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Se även

[Business Central- och OneDrive-integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)

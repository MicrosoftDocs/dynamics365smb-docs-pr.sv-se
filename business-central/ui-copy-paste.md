---
title: Kopiera och klistra in data
description: Kopiera fält och rader från Business Central-sidorna och klistra in någon annanstans.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 6f731940714a754275611026749afa4d79a94443
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/19/2019
ms.locfileid: "853077"
---
# <a name="copying-and-pasting"></a>Kopiera och klistra in
Du kan kopiera en eller flera rader i en lista eller ett enda fält på en sida och klistra in det du kopierade till samma sida, en annan sida eller ett externt dokument (såsom Microsoft Excel och Outlook e-post). Kortfattat, för att kopiera trycker du på CTRL + C (cmd + C i macOS) på tangentbordet. Klistra in genom att trycka på CTRL + V (cmd + V i macOS).

Det finns flera andra kortkommandon för kopiera och klistra in som hjälper dig att spara tid när du anger data. Mer information om detta finns i [Kortkommandon](keyboard-shortcuts.md#CopyRows).

Den här artikeln besvarar vanliga frågor som du kanske har om att kopiera och klistra in.  

## <a name="what-can-i-copy-and-paste"></a>Vad kan jag kopiera och klistra in?
-   Kopiera en eller flera rader i [!INCLUDE[d365fin](includes/d365fin_md.md)] samma lista eller en lista med samma kolumner.
-   Kopiera en eller flera rader i [!INCLUDE[d365fin](includes/d365fin_md.md)] och klistra in i Excel eller andra program.
-   Kopiera en eller flera rader i Excel och klistra in i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-lista.
-   Kopiera värdet för ett enskilt fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] och klistra in det var som helst.

## <a name="how-do-i-copy-rows"></a>Hur kopierar rader?
Om du vill kopiera en rad, markerar du den och trycker du på Ctrl + C.

Om du vill kopiera fler rader kan du:
-   Tryck på Ctrl och klicka på en ny rad eller tryck på Skift + klicka för att markera raden och alla rader mellan. Se [kortkommandon](keyboard-shortcuts.md#CopyRows) för flera kombinationer av mus och tangentbord för att markera rader.
-   Välj ![Visa fler alternativ](media/show-more-options-icon.png "ikonen Visa fler alternativ") i den första kolumnen i en rad, välj **markera flera**, markera kryssrutan bredvid varje rad som du vill kopiera och tryck på Ctrl + C.

## <a name="how-do-i-paste-rows"></a>Hur klistrar man in rader?
Markera en tom rad och tryck på CTRL + V. Om du vill ersätta befintliga rader markerar du raderna och trycker på CTRL + V. I det här fallet kan du bara klistra in samma antal rader som du har valt.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email-or-onenote"></a>Kan jag klistra in rader i ett e-postmeddelande i Outlook och OneNote?
Ja. Detta klistras in som en snyggt formaterad tabell som bevarar indrag, numerisk justering och färg, på samma sätt som visas i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="does-copy-and-paste-work-with-tiles"></a>Fungerar kopiera och klistra in med paneler?
Nej. Listan måste visas som rader (listvy) som du kan kopiera och klistra in.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>I vilken lista kan jag kopiera och klistra in rader?
Du kan kopiera rader i alla typer av lista som innehåller kalkylblad, faktaboxar eller lista som är inbäddad på en sida (till exempel rader på en försäljningsorder). För att klistra in rader måste listan vara redigerbar.

På vissa sidor kan utformningen göra att du inte kan klistra in rader. Kontakta administratören eller programutvecklare för att ändra den [redigerbar egenskap](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) på sidan eller [PasteIsValid egenskap](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) i källtabellen.

## <a name="on-which-clients-is-copy-and-paste-available"></a>På vilka klienter finns kopiera och klistra in?
Kopiera och klistra in är tillgängliga i webbläsaren eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-appen för Windows-10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Vad är det maximala antalet rader som kan kopieras?
Du kan kopiera så många rader som du har rullat in i vyn. Om du till exempel vill kopiera alla 1000 rader på en sida, måste du först bläddra längst ned på sidan och vänta tills raderna visas innan du kopierar. Det maximala antalet rader som du kan kopiera begränsas endast av enhetens minne.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Måste jag ha exakt samma antal kolumner när jag klistrar in rader?
Ja. Om du kopierar från [!INCLUDE[d365fin](includes/d365fin_md.md)], från Excel eller från någon annan tabellkälla måste raderna du vill klistrar ha exakt matchande kolumner – inte fler och inte färre.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Varför visas fel när du klistrar in rader?
När du klistrar in i [!INCLUDE[d365fin](includes/d365fin_md.md)], kontrolleras varje rad för att se till att värdena i varje kolumn är giltiga. Om en kolumn innehåller ett värde som inte är giltigt stoppas klistra in och ett felmeddelande visas. Du undviker detta genom att se till att kolumnerna har värdet innan du klistrar in dem.


## <a name="see-also"></a>Se även
[Hjälpmedelsfunktioner](ui-accessibility.md)  
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vanliga frågor och svar](across-faq.md)  

---
title: Anpassade och inbyggda layouts för rapporter och dokument | Microsoft Docs
description: Använd rapportlayouter för att anpassa dokument, till exempel för att anpassa teckensnitt, logotyp eller inställningar för de PDF-filer som du skickar till kunder.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f64397d41eb4002221d9967b5b61145882aee0d6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315162"
---
# <a name="managing-report-and-document-layouts"></a>Hantera rapport- och dokumentlayouter
En rapportlayout kontrollerar rapportens format och innehåll, som vilka datafält i en rapportdatauppsättning som visas i rapporten och hur de ordnas, textstil, bilder och mycket annat. Från [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du ändra vilken layout som används på en rapport, skapa en ny layout eller ändra befintliga layouter.

> [!NOTE]  
>   I [!INCLUDE[d365fin](includes/d365fin_md.md)], omfattar termen "rapporter" även externa dokument som t.ex. fakturor och bekräftelser av inköpsorder som du skickar till kunder som PDF-filer.

En rapportlayout ställer i synnerhet in följande:

* Rubrik- och datafälten som ska inkluderas från datauppsättningen för [!INCLUDE[d365fin](includes/d365fin_md.md)]-rapporten.
* Textformatet, till exempel teckensnittstyp, storlek och färg.
* Företagslogotypen och dess position.
* Allmänna sidinställningar, till exempel marginaler och bakgrundbilder.

En rapport kan ställas in med åtskilliga rapportlayouter, som du kan växla mellan. Du kan använda en av de inbyggda rapportlayouterna, eller så kan du skapa anpassade rapportlayouter och tilldela dem till dina rapporter efter behov. Mer information finns i [Så här skapar du en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md).

Det finns två typer av rapportlayouter som du kan använda i rapporter, Word och RDLC.

## <a name="word-report-layout-overview"></a>Översikt över Word-rapportlayout
En Word-rapportlayout är baserad på Word-dokument (filtypen .docx). Word-rapportlayouter aktiverar du för att utforma rapportlayouter, med hjälp av Microsoft Word 2013 eller senare. En Word-rapportlayout bestämmer rapportens innehåll - styr hur innehållselement organiseras och hur de ser ut. Ett Word-dokument med rapportlayout använder vanligtvis tabeller för att ordna innehållet, där cellerna kan innehålla datafält, text eller bilder.

 ![Exempel på en rapportlayoutdokumentet för NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Översikt över RDLC-layout
RDLC-layouter baseras på layouter för klientrapportdefinition (.rdlc- eller .rdl-filtyper). Dessa layouter skapas och ändras genom att använda SQL Server Report Builder. Designbegreppet för RDLC-layouter liknar Word-layouter, där layouten definierar det allmänna formatet på rapporten och bestämmer vilka fält från datauppsättningen som ska inkluderas. Att utforma RDLC-layouter är mer avancerat än Word-layouter. Mer information finns i [Designa RDLC rapportlayouter](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Inbyggda och anpassade rapportlayouter
[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller flera inbyggda layouter. Inbyggda layouter är fördefinierade layouter som har utformats för särskilda rapporter. [!INCLUDE[d365fin](includes/d365fin_md.md)]-rapporter ska ha en inbyggd layout som antingen en RDLC-rapportlayout, Word-rapportlayout eller i vissa fall både och. Du kan inte ändra en inbyggd rapportlayout från [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten, men du kan använda dem som utgångspunkt för att skapa egna anpassade rapportlayouter.

Anpassa layouter är rapportlayouter som du designar för att ändra utseendet på en rapport. Du skapar vanligtvis en anpassad layout baserad på en inbyggd layouten, men du kan skapa dem från noll eller från en kopia av en befintligt anpassad layout. Anpassa layouter göra att du kan ha flera layouter för samma rapport som du kan växla mellan när det behövs. Du kan till exempel ha olika layouter för varje [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag, eller så kan du ha olika layouter för samma företag för vissa tillfällen eller händelser, som en viss kampanj eller semesterperiod.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Avgöra om du ska använda en Word- eller RDLC-rapportlayout
En rapportlayout kan baseras på antingen ett Word-dokument eller en RDLC-fil. Att bestämma om du vill använda en Word-rapportlayout eller RDLC-rapportlayout beror på hur du vill att den genererade rapporten ska se ut, och din kunskap om Word och SQL Server Report Builder.

De allmänna designbegreppen för Word- och RDLC-layouter är mycket lika varandra. Däremot har varje typ vissa designfunktioner som påverkar hur den genererade rapporten visas i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det betyder att samma rapport kan se olika ut när du använder Word-rapportlayouten jämfört med RDLC-rapportlayouten.

Processen för att skapa Word-rapportlayouter och RDLC-rapportlayouter i rapporter är densamma. Den huvudsakliga skillnaden är det sätt som du ändrar layouterna. Word-rapportlayouter är oftast lättare att skapa och ändra än RDLC-rapportlayouter, eftersom du kan använda Word. RDLC-rapportlayouter ändras genom att använda SQL Server Report Builder som är till för mer avancerade användare.

Information om hur du ändrar vilken layout som ska användas finns i [Ändra aktuell layout](ui-how-change-layout-currently-used-report.md)

## <a name="see-also"></a>Se även
[Uppdatera rapport- eller dokumentlayouter](ui-update-report-layouts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Så här skapar och ändrar du en anpassad rapport eller dokumentlayout](ui-how-create-custom-report-layout.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  

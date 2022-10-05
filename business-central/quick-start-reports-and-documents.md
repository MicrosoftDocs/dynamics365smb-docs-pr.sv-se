---
title: Grundläggande rapporter och dokument snabbstart för utdata
description: Business Central innehåller inbyggda mallar för rapporter och dokument, med många anpassningsalternativ som du kan använda för att anpassa dem efter företagets behov.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: ''
ms.date: 08/15/2022
ms.author: a-reishima
ms.openlocfilehash: e2ff5bab1e1641e071f7113d369d5c05a7269b2d
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9586096"
---
# <a name="basic-reports-and-documents-output-quick-start"></a>Grundläggande rapporter och dokument snabbstart för utdata

Om du vill anpassa [!INCLUDE[prod_short](includes/prod_short.md)] efter företagets behov kan du ange och använda rapporter och anpassade dokument som passar företagets processer och visuella identiteter.

## <a name="add-your-company-logo-to-documents"></a>Lägg till företagslogotyp till dokument

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller mallar som använder företagets logotyp för att spara tid anpassa dokument som fakturor, order och utdrag.

1. Välja ![Kugghjulsikon för att öppna menyn Inställningar.](media/ui-experience/settings_icon_small.png) och sedan åtgärden **Företagsinformation**.
2. Välj åtgärden **Bild** och välj sedan **Välj**.
3. Markera bild filen på enheten.

Du kan se ovanstående instruktioner i [den här YouTube videon](https://www.youtube.com/watch?v=AatXbKF1NGg). När bilden väl visas i fältet **Bild** kan du stänga sidan **Företagsinformation**.

## <a name="run-reports"></a>Kör rapporter

I rapporter kan du ordna information från olika källor i [!INCLUDE[prod_short](includes/prod_short.md)] och presentera den på ett läsligt sätt som är lätt att skriva ut eller dela digitalt. Rapporter finns på de sidor som de associeras sammanhangsbaserat med. På sidan **artiklar** visas t.ex. en lista över rapporter som är relaterade till lagernivåer, inköp, försäljning med mera.

1. Öppna sidan som är kopplad till den begärda rapporten, till exempel sidan **artiklar**.
2. Välj rapporten **Lager - Topp 10 lista** på menyn **Rapporter**.
3. På sidan för rapport förfrågan kan du ange filter för att begränsa datum intervallet eller ändra den referens enhet som används i rapporten.
4. Välj åtgärd **utskrift** och följ instruktionerna för enhetens utskrift.
    1. Du kan också välja åtgärden **förhandsgranskning** om du vill visa rapporten på skärmen.

Lär dig mer om att filtrera data, schemalägga rapporter och mer vid [Kör- och skriv ut-rapporter](ui-work-report.md).

## <a name="save-reports-as-pdf-excel-or-word-documents"></a>Spara rapporter som PDF-, Excel- eller Word-dokument

Om du snabbt vill dela rapporter kan du spara [!INCLUDE[prod_short](includes/prod_short.md)] rapporter direkt i PDF Microsoft Excel eller Microsoft Word dokument.

1. Upprepa steg 1 till 3 i avsnittet [kör rapporter](#run-reports) ovan.
2. Välj åtgärden **Skicka till**.
3. Välj filen, och välj sedan **OK**.
R den genererade rapport filen sparas automatiskt i webbläsarens nedĺaddningsmapp.

### <a name="change-report-and-document-layouts"></a>Ändra rapport- och dokumentlayouter

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller många inbyggda layouter för rapporter och andra genererade dokument, till exempel försäljningsfakturor. Med hjälp av program som Microsoft Word eller Excel kan du redigera layoutinställningarna för dokument och rapporter enligt följande exempel:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Rapportlayouter** och väljer sedan relaterad länk.
2. På sidan **Rapportlayouter**, välj åtgärden **Sök** layout *StandardSalesInvoice.docx*, välj åtgärden **Exportera layout** för att ladda ned layoutmallfilen.

    Ett Word-dokument sparas på enheten med samma fil namn som visas på sidan **rapportlayout**.
3. Öppna filen i Microsoft Word och redigera dokumentet, t.ex. genom att flytta datum fältet ( *DocumentDate*) eller logotypen, eller genom att ändra tecken storlek och sedan spara filen.
4. Gå tillbaka till **rapportlayouter** genom att välja **ny layout**-åtgärden.
5. På sidan **Lägg till ny layout för en rapport** anger du ett namn och en beskrivning för fälten **Layoutnamn** och **Beskrivning**, för att göra layouten lätt att hitta.
6. Välj alternativet **Word** i fältet **formatalternativ** och klicka sedan på **OK**.
7. På sidan **Välj ordlayout**, välj **Välj** för att öppna den redigerade layoutfilen på din enhet.
8. Testa den nya layouten genom att välja instruktionen **Kör rapport**.

Mer information om hur du anpassar rapporter och dokument till ditt företags behov vid [rapport- och dokumentlayout](ui-manage-report-layouts.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/work-with-reports/).

## <a name="see-also"></a>Se även

[Använd rapporter i det dagliga arbetet](reports-use-reports.md)  
[Tillgängliga rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Val av dokumentrapport](across-report-selections.md)  
[Snabbstart för Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

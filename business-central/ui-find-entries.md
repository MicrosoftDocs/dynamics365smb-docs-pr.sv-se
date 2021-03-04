---
title: Hitta transaktioner | Microsoft Docs
description: I den här artikeln beskrivs dokument och transaktioner relaterar till varandra
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 870cd32dc2408236ed8997e1f939c00d1bf519e4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927737"
---
# <a name="finding-related-entries-for-posted-documents"></a>Hitta relaterade transaktioner för bokförda dokument 

I den här artikeln får du lära dig att söka efter dokument och transaktioner som är relaterade till varandra baserat på en gemensam information, t.ex.:

- Verifikationsnummer eller bokföringsdatum
- Typ av företagskontakt, nummer eller externt dokumentnummer
- Artikelns serienummer eller partinummer

Funktionen är användbar för att hitta redovisningstransaktionerna som har skapats som ett resultat av vissa transaktioner. När du söker efter verifikationsnummer kan du skriva ut sammanfattningen i rapporten Dokumentposter.

## <a name="get-started"></a>Kom igång

Funktionen Hitta transaktioner är tillgänglig på de flesta sidor som innehåller bokförda dokument eller bokförda dokumenttransaktioner – för både listor och kort. Det första steget är att öppna en av de här sidorna. Välj sedan antingen åtgärden **Hitta transaktioner** eller tryck på Alt + G.

På sidan **Hitta transaktioner** finns alla relaterade dokument och transaktioner baserade på dokumentnr och bokföringsdatum. Sidan är uppdelad i tre delar:

- I det övre avsnittet visas fält och åtgärder som du använder för att filtrera sökningen.
- I mitten-avsnittet visas relaterade dokument baserat på sökningen.
- I den nedre delen visas information om källdokumentet som hittades vid sökning.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Söka efter transaktioner

Du kan söka efter transaktioner som bygger på information om antingen dokument, affärskontakt eller artikel. Om du vill ändra sökningen väljer du **Åtgärder**, **Sök efter** och sedan en av följande åtgärder:

|Åtgärd|Beskrivning|
|------|-----------|
|Sök efter dokument|Visa transaktioner baserat på ett visst verifikationsnummer eller bokföringsdatum.|
|Affärskontakt |Visa transaktioner baserat på en viss kontakttyp, ett visst kontaktnummer och/eller externt dokumentnummer. Du kan ange dokumentinformation som tilldelats av en leverantör eller en kund. Använd de tillgängliga fälten för att söka efter leverantörsdokument genom att använda numren som leverantören tilldelade dokumenten.|
|Artikelreferens|Visa transaktioner baserat på ett serienummer eller partinummer. Du kan ange partinumret eller serienumret, eller ett filter för det parti- eller serienummer som du vill söka efter. Denna åtgärd är användbar när du vill veta var ett specifikt artikelspårningsnummer har använts, vilken leverantör det kom ifrån eller till vilken kund det såldes.|

När du har gjort ett val anger du relevant sökningsinformation i fälten längst upp. Använd knappbeskrivningarna i fälten för att få hjälp. När du är klar väljer du **Sök** för att starta sökningen. Om du ändrar något av filtren, måste du välja **Sök** igen.

> [!TIP]
> Ett par exempel på hur du använder **Hitta transaktioner** finns i [Spåra artikel-spårade artiklar](inventory-how-to-trace-item-tracked-items.md) och [Genomgång: spåra serie-/partinummer](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Arbeta med Business Central](ui-work-product.md)  
[Lägga till en sidåtgärd i ditt rollcenter](ui-bookmarks.md)  
[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
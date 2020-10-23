---
title: Lägg till bifogade filer, länkar och anteckningar på poster | Microsoft Docs
description: Koppla en hyperlänk till ett dokument eller en webbplats till en viss post, till exempel en kund eller ett dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 447012a66e75e1acf03f2aff1ba6b6922164312f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918569"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Hantera bifogade filer, länkar och anteckningar på kort och dokument

I faktaboxen för de flesta kort och dokument kan du bifoga filer, lägga till länkar och skriva anteckningar. För länkar och noteringar kan du också göra det på listsidan genom att först välja den relaterade raden.

Om du vill visa eller ändra dessa kopplade informationstyper måste du först öppna fliken **bifogade filer** i faktaboxen. Numret bakom flikens rubrik visar hur många bifogade filer, länkar eller anteckningar som finns för kortet eller dokumentet.

Bilagor, länkar och anteckningar förblir kopplade till ett kort eller dokument, till exempel från en pågående försäljningsorder till en bokförd försäljningsfaktura. Ingen av de bifogade filtyperna skrivs emellertid ut från systemet, till exempel vid utskrift eller vid sparande i fil.

> [!NOTE]
> När du delvis levererar och fakturerar en försäljningsorder eller en inköpsorder, kopplas den bifogade filen endast till den slutgiltiga fakturan för ordern. På samma sätt, när du fakturerar med hjälp av funktionen för uppskov, kopplas den bifogade filen endast till redovisningstransaktionerna för dokumentet, men inte till periodiseringsposter.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Så här bifogar du en fil till en inköpsfaktura
Du kan bifoga alla typer av filer, som innehåller text, bilder och video, till ett kort eller dokument. Detta är användbart om du t.ex. vill lagra en leverantörs faktura som en PDF-fil på den relaterade inköpsfakturan i [!INCLUDE[d365fin](includes/d365fin_md.md)]i.

> [!NOTE]
> Filer som bifogas med funktionen inkommande dokument finns inte på fliken **bifogade filer**. Mer information finns i [inkommande dokument](across-income-documents.md).

Följande procedur är baserad på en inköpsfaktura. Stegen är liknande för alla andra dokument och kort som stöds.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan relaterad länk.
2. Öppna försäljningsorder som du vill bifoga en fil till.
3. Öppna fliken **bifogade filer** i faktaboxen.
4. Välj värdet bakom fältet **dokument**, till exempel "0".
5. På sidan **Bifogade dokument** i fältet **bilaga**, välj åtgärden **Välj en fil**.
5. Markera en fil varifrån som helst och välj sedan knappen **öppna**.

Filen är nu bifogad inköpsfakturan.

## <a name="to-view-an-attached-file"></a>Visa den bifogade filen
1. Öppna fliken **bifogade filer** i faktaboxen.
2. Välj värdet bakom fältet **dokument**, till exempel "1".
3. På sidan **Bifogade dokument** väljer du åtgärden **Förhandsgranskning**.
4. Öppna den hämtade filen.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Så här sparar du ett dokument som en bifogad PDF-fil
När du behöver spara ett dokument som en fil kan du använda åtgärden **Bifoga som PDF** för att överföra det aktuella dokumentinnehållet som en PDF-fil som är kopplad till faktaboxen för dokumentet. Detta är användbart exempelvis när dokument följer flera steg i en procedur, t.ex. ett arbetsflöde för försäljning eller godkännande, och du vill referera till en utskrift av föregående steg.

Följande procedur är baserad på en försäljningsorder. Stegen är liknande för samtliga dokument som stöds.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Markera en försäljningsorder och välj åtgärden **Bifoga som PDF**.

En PDF-fil med det aktuella innehållet på försäljningsordern läggs till på fliken **Bilagor** i faktaboxen.

## <a name="to-add-a-link-from-an-item-card"></a>Att lägga till länk från ett artikelkort
Du kan lägga till en länk från ett kort eller dokument till en URL eller sökväg. Detta är användbart om du t.ex. vill koppla ett artikelkort till leverantörens artikelkatalog.

Följande procedur baseras på ett artikelkort. Stegen är liknande för alla andra kort och dokument.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan relaterad länk.
2. Välj den artikel som du vill lägga till en länk från och välj sedan fliken **bifogade filer** i faktaboxen.
3. Välj ikonen **länkar**, välj ikonen **+**.
4. I fältet **länkadresser** anger du länken.

    Länken måste vara en giltig URL för Internet eller intranätet.

5. I fältet **Beskrivning**, ange information om länken.  
6. Välj **OK**.

Länken kopplas nu till artikelkortet.  

## <a name="to-write-a-note-on-a-sales-order"></a>Skriva en notering på en försäljningsorder
Du kan skriva en notering på ett dokument eller kort, t.ex. om du vill skicka särskilda instruktioner till andra användare av dokumentet eller kortet. Du kan ta med fillänkar och URL:er i anteckningar.

> [!NOTE]
> Anteckningarna på fliken **bifogade filer** är inte relaterade till interna anteckningsfunktioner, som i huvudsak används för att kommunicera mellan arbetsflödesanvändare. Mer information finns i [Ställa in meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md).

Följande procedur är baserad på en försäljningsorder. Stegen är liknande för alla andra dokument och kort som stöds.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.
2. Välj den försäljningsorder som du vill skriva en anteckning på och välj sedan fliken **bifogade filer** i faktaboxen.
3. Välj avsnittet **anteckningar**, välj ikonen **+**.
4. I fältet **Anteckning** skriv någon text, t.ex. "detta är en brådskande order.".
5. Välj **OK**.

Noteringen är nu kopplad till försäljningsordern.

## <a name="see-also"></a>Se även  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Inkommande dokument](across-income-documents.md)  
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)  

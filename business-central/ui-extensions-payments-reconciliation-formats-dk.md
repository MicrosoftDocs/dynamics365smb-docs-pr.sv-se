---
title: Använda tillägg för betalningar och avstämning (DK) | Microsoft Docs
description: Det här tillägget gör det enkelt att exportera filer som är förformaterade för att uppfylla bankkraven för elektroniska inlagor.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: aa738f326782bacdc5450bbd78ea0dffb5646fa5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194073"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a>Tillägg för betalningar och avstämning (DK).
Gör snabba, felfria betalninger genom att exportera filer som är specifikt formaterade för utbyte med din leverantör eller bank. Filerna påskyndar processerna för betalning och avstämning och undviker fel som kan inträffa när du manuellt anger information på en bankwebbplats.  

Det här tillägget stöder filformat för flera danska banker. När du exporterar betalningsinformation till en fil, packar tillägget data i det format som krävs av din bank. Formaten omfattar till exempel Bankdata-vl, V3, BEC, SDC och FIK som många olika banker använder och några som är mer specialiserade för vissa banker, till exempel Danske Bank och Nordea. Tillägget innehåller dessutom vissa format för import och avstämning av bankutdrag.  

> [!Note]
> Om du vill använda tillägget måste du känna till det format som banken eller leverantör kräver. Vissa banker eller leverantörer tillhandahåller denna information på sina webbplatser; Du kan dock behöva kontakta deras kundservice för att hämta önskad information.  

## <a name="supported-bank-formats"></a>Bankformat som stöds
Det här tillägget använder följande format för betalningsfiler:  

* BANKDATA-V3  
* BEC INDLAND  
* BEC-CSV  
* DANSKEBANK CMKV  
* DANSKEBANK CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC CSV  

## <a name="to-set-up-the-extension"></a>Så här ställer du in tillägget
Det finns några steg för att komma igång.  

* Tillåt betalningsdataexport. För att skydda dina data, är detta inte är tillgänglig.  
* Skapa inköpsorder och leverantörsreskontra så att du inte behöver externa verifikationsnummer på fakturor. Om det behövs kan använda du referensnumret för att referera till en viss faktura.  
* Ange betalningssätt för varje leverantör. Betalningssätt definierar hur du vill betala fakturor från leverantören. Till exempel bank, kontanter, check eller konto.  
* Ange vilket format som ska användas för var och en av dina bankkonton. Det kan t.ex. vara NORDEA, DANSKEBANK, SDC.  

Dessutom måste du tilldela leverantörer till en inhemsk **Gen. rörelsebokföringsmall** och en **Leverantörsbokföringsmall**. Inställningen av Land/Region måste för leverantören vara Danmark (DK). Mer information finns i [Ställa in bokföringsmallar](finance-posting-groups.md).  

### <a name="to-allow-d365fin-to-export-payment-data"></a>För att tillåta betalningsdataexport från [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Utbetalningsjournal** och välj sedan relaterad länk.  
2. På sidan **Redigera betalningsjournal**, välj journalen **Bank**.  
3. Markera kryssrutan **Tillåt betalningsexport**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Ange betalningssätt för en leverantör
I följande tabell visas kombinationerna av betalningssätten FIK och GIRO som [!INCLUDE[d365fin](includes/d365fin_md.md)] stödjer.

||Typ 01 | Typ 04 | Typ 71 | Typ 73 |
|----|---|---|---|---|
|Postgiro eller FIK fordringsägarenr? | Postgiro | Postgiro | FIK Fordringsägarenr. | FIK Fordringsägarenr.|
|Tillåta meddelande till mottagare? | Ja |Nej |Nej | Ja |
|Innehåller betalningsreferensnummer? | Nr | Ja, 16 siffror. | Ja, 15 siffror. | Nej|

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.  
2. Öppna kortet, expandera fliken **betalningar** i fältet **betalningssätt** och välj betalningssätt.  
3. I vissa fall måste du fylla i andra fält. Se tabellen ovan för mer information om kombinationer.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Ange formaten som ska användas för ett bankkonto
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.  
2. Öppna kortet för bankkontokort.  
3. I fältet **Format för betalningsexport**, välj format för exportfilen.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Välja FIK eller Giro betalningsinformation för leverantörsfakturor
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan relaterad länk.
2. Välj Leverantören. Kom ihåg att detta måste en dansk leverantör med adress i Danmark.
3. Skapa en faktura. Fälten **betalningssätt** och **leverantörsnummer** fylls i baserat på inställningarna på leverantörskortet. Du kan ändra dem om du vill.
4. I fältet **betalningsreferens** anger du det 15-siffriga numret på leverantörens faktura.  

    > [!Tip]
    > Du behöver bara lägga till de senaste 11 siffrorna. [!INCLUDE[d365fin](includes/d365fin_md.md)] lägger till fyra nollor i början av numret.  

5. Bokföra fakturan

## <a name="to-use-the-extension-to-export-payment-data"></a>Du använder tillägget för att exportera betalningsdata
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Utbetalningsjournaler** och välj sedan relaterad länk.  
2. Välj åtgärden **Föreslå betalningsjournaler för leverantör**.  

    > [!Tip]
    > Om du endast vill exportera specifika betalningar kan du använda alternativen för filtrering av data.  

3. Om det behövs kan du lägga till filter om du endast vill exportera specifika betalningar.  
4. I fältet **Bankbetalningstyp** väljer du **Elektronisk betalning.**  
5. Välj åtgärden **Exportera**.  

## <a name="see-also"></a>Se även
[Anpassning av Business Central för [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  

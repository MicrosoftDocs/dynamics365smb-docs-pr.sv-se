---
title: Ta emot och omvandla elektroniska dokument
description: Detta ämne beskriver hur du kan ta emot elektroniska dokument direkt från handelspartner eller en OCR-tjänst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: bba45239906820f4c56b948d80a46c8ca427a342
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435090"
---
# <a name="receive-and-convert-electronic-documents"></a>Ta emot och omvandla elektroniska dokument
Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder mottagning av elektroniska fakturor och kreditnotor i PEPPOL-format, som stöds av de största leverantörerna av dokumentväxlingstjänster. Om du vill ta emot en faktura från en leverantör som ett elektroniskt PEPPOL-dokument behandlar du dokumentet på sidan Inkommande dokument för att konvertera det till en inköpsfaktura eller redovisningsjournalsrad i [!INCLUDE[prod_short](includes/prod_short.md)].

 Förutom att ta emot elektroniska dokument direkt från handelspartners kan du ta emot elektroniska dokument från en ocr-service som har omvandlat dina PDF eller bildfiler till elektroniska dokument.  

 Innan du kan ta emot elektroniska dokument via dokumentutbytestjänsten, måste du lägga upp olika huvuddata, som företagsinformation, leverantörer, artiklar och enheter. Dessa används för att identifiera dina affärspartners och artiklar vid konvertering av data i element i den utgående dokumentfilen till fält i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Konfigurera en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md).  

 Innan du kan ta emot elektroniska dokument genom OCR-servicen, måste du skapa och aktivera den förkonfigurerade serviceanslutningen. Mer information finns i [Skapa inkommande dokument](across-how-setup-income-documents.md).  

 Trafiken av elektroniska dokument in och ut ur [!INCLUDE[prod_short](includes/prod_short.md)] hanteras av jobbköfunktionen. Innan du kan ta emot elektroniska dokument, måste den relevanta jobbkön startas.  

 Du kan antingen starta omvandlingen av elektroniska dokument manuellt, enligt beskrivningen i denna procedur, eller så kan du aktivera ett arbetsflöde för att konvertera elektroniska dokument automatiskt, när de har tagits emot. Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] innehåller en arbetsflödesmall, *Arbetsflödet Från inkommande elektroniskt via OCR till Öppna inköpsfaktura*, som är klar att kopieras till ett arbetsflöde och aktiveras. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
>  När du konverterar elektroniskt dokumentet som har tagits emot från OCR-tjänsten av dokument – eller journalrader i [!INCLUDE[prod_short](includes/prod_short.md)], sammanfattas raderna i källdokumentet på en rad. Enkelraden ska vara av typen redovisningskonto och fälten **Beskrivning** och (redovisningskonto) **Nr.** ska vara tomma. Värdet i fältet **Belopp** ska vara detsamma som det totala beloppet exklusive moms för alla rader i källdokumentet.  
>   
>  För att säkerställa att fälten **Beskrivning** och **Nr.** fylls i kan du välja knappen **Mappa text till konto** på sidan **Inkommande dokument** för att definiera att en viss fakturatext alltid mappas till ett visst debet- eller kreditkonto i redovisningen. Vidare fylls fältet **Beskrivning** på dokument – eller journalrader som skapas från ett elektroniskt dokument för den leverantören eller kunden i med texten i fråga och (redovisningskontots) **Nr.** med kontot.  
>   
>  I stället för mappning till ett redovisningskonto kan du också mappa till ett bankkonto. Det är praktiskt, till exempel, för elektroniska dokument för kostnader som redan har betalts, där du vill skapa en redovisningsjournalrad som är klar för bokföring på ett bankkonto.  

 Efterföljande procedur beskriver hur du tar emot en leverantörsfaktura och den omvandlas till en inköpsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Proceduren är samma, när du omvandlar en leverantörsfaktura till en redovisningsjournalrad.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Så här tar du emot och omvandlar en elektronisk faktura till en inköpsfaktura  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Inkommande dokument** och väljer sedan relaterad länk.  

2.  Välj raden för den inkommande dokumentposten som representerar en ny inkommande elektronisk faktura och välj åtgärden **Redigera**.  

     På sidan **Dokumentkort** är den relaterade xml-filen bifogad, och de flesta fälten är förifyllda med information från den elektroniska fakturan. Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).  

3.  I fältet **Typ av dataintegrering**, välj **PEPPOL – faktura** eller **OCR – faktura** beroende på ursprunget till det elektroniska dokumentet i fältet  

4.  Om du vill mappa text på leverantörsfakturan till ett visst debetkonto väljer du på fliken **Åtgärder** i gruppen **Allmänt** och väljer **Mappa text till konto** och fyller sedan i **Mappning av text-till-konto**.  

5.  Välj åtgärden **Skapa dokument**.  

     En inköpsfaktura skapas i [!INCLUDE[prod_short](includes/prod_short.md)] baserat på informationen i det elektroniska dokumentet.  

     Eventuella valideringfel som vanligtvis beror på fel eller saknade huvuddata i [!INCLUDE[prod_short](includes/prod_short.md)], visas på snabbfliken **Felmeddelanden**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även  
[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Inkommande dokument](across-income-documents.md)  
[Konfigurera utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Utbyta data elektroniskt.](across-data-exchange.md)   
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
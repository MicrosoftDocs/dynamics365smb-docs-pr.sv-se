---
title: Ta emot och omvandla elektroniska dokument | Microsoft Docs
description: "Du kan ta emot elektroniska dokument direkt från handelspartner eller en OCR-tjänst."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 14849dbb74f608f78e0ad8a317307ec1bf649cf8
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-receive-and-convert-electronic-documents"></a>Så här tar du emot och omvandlar elektroniska dokument
Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder mottagning av elektroniska fakturor och kreditnotor i PEPPOL-format, som stöds av de största leverantörerna av dokumentväxlingstjänster. Om du vill ta emot en faktura från en leverantör som ett elektroniskt PEPPOL-dokument behandlar du dokumentet i fönstret Inkommande dokument för att konvertera det till en inköpsfaktura eller redovisningsjournalsrad i [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Förutom att ta emot elektroniska dokument direkt från handelspartners kan du ta emot elektroniska dokument från en ocr-service som har omvandlat dina PDF eller bildfiler till elektroniska dokument.  

 Innan du kan ta emot elektroniska dokument via dokumentutbytestjänsten, måste du lägga upp olika huvuddata, som företagsinformation, leverantörer, artiklar och enheter. Dessa används för att identifiera dina affärspartners och artiklar vid konvertering av data i element i den utgående dokumentfilen till fält i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Så här konfigurerar du en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md).  

 Innan du kan ta emot elektroniska dokument genom OCR-servicen, måste du skapa och aktivera den förkonfigurerade serviceanslutningen. Mer information finns i [Så här skapar du inkommande dokument](across-how-setup-income-documents.md).  

 Trafiken av elektroniska dokument in och ut ur [!INCLUDE[d365fin](includes/d365fin_md.md)] hanteras av jobbköfunktionen. Innan du kan ta emot elektroniska dokument, måste den relevanta jobbkön startas.  

 Du kan antingen starta omvandlingen av elektroniska dokument manuellt, enligt beskrivningen i denna procedur, eller så kan du aktivera ett arbetsflöde för att konvertera elektroniska dokument automatiskt, när de har tagits emot. Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller en arbetsflödesmall, *Arbetsflödet Från inkommande elektroniskt via OCR till Öppna inköpsfaktura*, som är klar att kopieras till ett arbetsflöde och aktiveras. Mer information finns i [Arbetsflöden](across-workflow.md).  

> [!NOTE]  
>  När du konverterar elektroniskt dokumentet som har tagits emot från OCR-tjänsten av dokument - eller journalrader i [!INCLUDE[d365fin](includes/d365fin_md.md)],  sammanfattas raderna i källdokumentet på en rad. Enkelraden ska vara av typen redovisningskonto och fälten **Beskrivning** och (redovisningskonto) **Nr.** ska vara tomma. Värdet i fältet **Belopp** ska vara samma som det totala beloppet exklusive moms, för alla rader i källdokumentet.  
>   
>  Att säkerställa att de **beskrivning** och **nr.** För att se till att fälten fylls i kan du välja knappen **Mappa text till konto** i fönstret **Inkommande dokument** för att definiera att en viss fakturatext alltid mappas till ett visst debet- eller kreditkonto i redovisningen. Vidare fylls fältet **Beskrivning** på dokument - eller journalrader som skapas från ett elektroniskt dokument för den leverantören eller kunden i med texten i fråga och (redovisningskontots) **Nr.** med kontot.  
>   
>  I stället för mappning till ett redovisningskonto kan du också mappa till ett bankkonto. Det är praktiskt, till exempel, för elektroniska dokument för kostnader som redan har betalts, där du vill skapa en redovisningsjournalrad som är klar för bokföring på ett bankkonto.  

 Efterföljande procedur beskriver hur du tar emot en leverantörsfaktura och den omvandlas till en inköpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Proceduren är samma, när du omvandlar en leverantörsfaktura till en redovisningsjournalrad.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Så här tar du emot och omvandlar en elektronisk faktura till en inköpsfaktura  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inkommande dokument** och välj sedan relaterad länk.  

2.  Välj raden för den inkommande dokumentposten som representerar en ny inkommande elektronisk faktura och välj sedan **Redigera** på fliken **Start** i gruppen **Hantera**.  

     I fönstret **Dokumentkort** är den relaterade xml-filen bifogad, och de flesta fälten är förifyllda med information från den elektroniska fakturan. Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).  

3.  I fältet **Typ av dataintegration**, välj **PEPPOL - faktura** eller **OCR – faktura** beroende på ursprunget till det elektroniska dokumentet i fältet  

4.  Om du vill mappa text på leverantörsfakturan till ett visst debetkonto väljer du på fliken **Åtgärder** i gruppen **Allmänt** och väljer **Mappa text till konto** och fyller sedan i **Mappning av text-till-konto**.  

5.  Gå till fliken **Åtgärder**, gruppen **Allmänt**, och välj **Skapa dokument**.  

     En inköpsfaktura skapas i [!INCLUDE[d365fin](includes/d365fin_md.md)] baserat på informationen i det elektroniska dokumentet.  

     Eventuella valideringfel som vanligtvis beror på fel eller saknade huvuddata i [!INCLUDE[d365fin](includes/d365fin_md.md)], visas på snabbfliken **Felmeddelanden**.  

## <a name="see-also"></a>Se även  
[Hantera likviditet](payables-manage-payables.md)  
[Inkommande dokument](across-income-documents.md)  
[Så här konfigurerar du utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Utbyta data elektroniskt.](across-data-exchange.md)   
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


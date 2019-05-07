---
title: Skicka elektroniska dokument | Microsoft Docs
description: Så här skickar du fakturor elektroniskt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8cb28db63e977cf02b81daa7043b64838406161f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "919970"
---
# <a name="send-electronic-documents"></a>Skicka elektroniska dokument
Den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder utskick av elektroniska fakturor och kreditnotor i PEPPOL-format, som stöds av de största leverantörerna av dokumentväxlingstjänster En leverantör av dokumentväxlingstjänster skickar dokument elektroniskt mellan handelspartners. För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.  

 I den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] finns en förkonfigurerad dokumentväxlingstjänst som är inställningsklar för företaget. Mer information finns i [Konfigurera en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md).  

 Om du vill skicka en försäljningsfaktura som ett elektroniskt PEPPOL-dokument väljer du alternativet **Elektroniskt dokument** i dialogrutan **Bokför och skicka**, där du även kan ställa in kundens standardprofil för dokumentutskick. Först måste du skapa olika huvuddata, som företagsinformation, kunder, artiklar och enheter. Dessa används för att identifiera dina affärspartners och artiklar vid konvertering av data i fält i [Så här konfigurerar du utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Så här kan du skicka en elektronisk försäljningsfaktura  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Försäljningsfakturor** och välj sedan relaterad länk.  

2.  Skapa en ny försäljningsfaktura.  

3.  Välj **Bokför och skicka** på fliken **Åtgärder** i gruppen **Bokföring** när försäljningsfakturan är klar att faktureras.  

     Om kundens standardutskicksprofil är **Elektroniskt dokument** visas det i dialogrutan **Bekräftelse för bokför och utskick** och du behöver bara välja **Ja** för att bokföra och skicka fakturan elektroniskt i det valda formatet.  

4.  Välj knappen AssistEdit till höger om fältet **Skicka dokument till** i dialogrutan **Bekräftelse för bokför och utskick**.  

5.  Välj **Genom dokumentväxlingstjänst** i dialogrutan **Skicka dokument till** dialogrutan i fältet **Genom dokumentväxlingstjänst**.  

6.  Välj **PEPPOL** i fältet **Format**.  

7.  Välj **OK**. Dialogrutan **Bekräftelse för bokför och utskick** visas. **Elektroniskt dokument (PEPPOL)** läggs till i fältet **Skicka dokument till**.  

8.  Välj **Ja**.  

     Försäljningsfakturan bokförs och skickas till kunden som ett elektroniskt dokument i PEPPOL-format.  

    > [!NOTE]  
    >  Du kan även skicka en bokförd försäljningsfaktura som ett elektroniskt dokument. Proceduren är samma som har beskrivits i det här avsnittet för icke-bokförda försäljningsdokument. På sidan **Aktivitetslogg** för att visa status för elektroniskt dokument på fliken **Åtgärder**, i gruppen **Allmänt**, i fönstret **Bokförd försäljningsfaktura**. Mer information finns i **Aktivitetslogg**  

## <a name="see-also"></a>Se även  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Skapa dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md)  
[Konfigurera utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Konfigurera en tjänst för dokumentutbyte](across-how-to-set-up-a-document-exchange-service.md)  
[Skapa dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Utbyta data elektroniskt](across-data-exchange.md).  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  

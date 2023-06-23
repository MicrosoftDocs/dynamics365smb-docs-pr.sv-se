---
title: Skicka elektroniska dokument
description: Lär dig använda Business Central för att skicka elektriska fakturor och kredit notor i PEPPOL-format.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="send-electronic-documents" />Skicka elektroniska dokument

Den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] stöder utskick av elektroniska fakturor och kreditnotor i PEPPOL-format, ett format som stöds av de största leverantörerna av dokumentutbytestjänster. En leverantör av dokumentväxlingstjänster skickar dokument elektroniskt mellan handelspartners. För att få stöd för andra elektroniska dokumentformat använder du ramverket för datautbyte.  

 I den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] finns en förkonfigurerad dokumentväxlingstjänst som är inställningsklar för företaget. Mer information finns i [Konfigurera en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md). I vissa fall måste du dock installera en app. Mer information finns i [Vanliga frågor om elektronisk fakturering](faq-electronic-invoicing.yml).  

 Om du vill skicka en försäljningsfaktura som ett elektroniskt PEPPOL-dokument väljer du **Elektroniskt dokument** i dialogrutan **Bokför och skicka**. Från denna dialogruta kan du även konfigurera kundens standardprofil för dokumentutskick. Först måste du skapa olika huvuddata, som företagsinformation, kunder, artiklar och enheter. Dessa används för att identifiera dina affärspartners och artiklar vid konvertering av data i fält i [Så här konfigurerar du utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice" />Så här kan du skicka en elektronisk försäljningsfaktura

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.  

2. Skapa en ny försäljningsfaktura.  

3. När försäljningsfakturaraderna är klara att faktureras väljer du åtgärden **Bokföra och skicka**.  

     Om kundens standardprofil för utskick är **Elektroniskt dokument** visas denna i dialogrutan **Bokför och skicka bekräftelse**. På så sätt behöver du bara välja **Ja**-knappen för att bokföra och skicka fakturan elektroniskt i det valda formatet.  

4. Välj knappen AssistEdit till höger om fältet **Skicka dokument till** i dialogrutan **Bekräftelse för bokför och utskick**.  

5. Välj **Genom dokumentväxlingstjänst** i dialogrutan **Skicka dokument till** dialogrutan i fältet **Genom dokumentväxlingstjänst**.  

6. Välj **PEPPOL** i fältet **Format**.  

7. Välj **OK**. Dialogrutan **Bekräftelse för bokför och utskick** visas. **Elektroniskt dokument (PEPPOL)** läggs till i fältet **Skicka dokument till**.  

8. Välj **Ja**.  

     Försäljningsfakturan bokförs och skickas till kunden i PEPPOL-format.  

    > [!NOTE]  
    >  Du kan även skicka en bokförd försäljningsfaktura som ett elektroniskt dokument. Proceduren är samma som har beskrivits i det här avsnittet för icke-bokförda försäljningsdokument. På sidan **Bokförd försäljningsfaktura** väljer du åtgärden **Aktivitetslogg** för att visa status för det elektroniska dokumentet.  

## <a name="see-related-microsoft-trainingtrainingmoduleselectronic-documents-dynamics-365-business-centralindex" />Se relaterad [Microsoft utbildning](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also" />Se även

[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Skapa dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md)  
[Konfigurera utskick och mottagning av elektroniska dokument](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Konfigurera en tjänst för dokumentutbyte](across-how-to-set-up-a-document-exchange-service.md)  
[Skapa dataintegreringsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Utbyta data elektroniskt](across-data-exchange.md)  
[Vanliga frågor och svar om elektronisk fakturering](faq-electronic-invoicing.yml)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

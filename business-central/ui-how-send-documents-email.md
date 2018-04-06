---
title: "Konfigurera dokumentspecifikt e-postinnehåll | Microsoft Docs"
description: "Du kan definiera innehåll som ska infogas i brödtexten i ett e-postmeddelande, till exempel en PayPal-länk. Du kan också koppla dokument till e-postmeddelanden."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ed2ffa433c2bee2b29971aacd25430d2148ecc56
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="send-documents-by-email"></a>Skicka dokument som e-post
För att meddela innehållet i affärsdokument snabbt till dina affärspartners, till exempel betalningsinformationen på försäljningsdokument till kunder, kan du använda funktionen Rapportlayout för att definiera dokumentspecifikt innehåll som infogas i e-postbrödtexter automatiskt. Mer information finns i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md).

Om du vill aktivera e-post i [!INCLUDE[d365fin](includes/d365fin_md.md)] startar du den assisterade konfigurationen för **Konfigurera e-post** i ditt rollcenter.

Du kan e-posta praktiskt taget alla dokumenttyper som bilagor till e-postmeddelanden direkt från fönstret som visar dokumentet. Förutom bilagan kan du skapa dokumentspecifika e-postbrödtexter med viktig information från dokumentet föregås av standardtext som hälsar e-postmottagaren och introducerar själva dokumentet. Om du vill erbjuda dina kunder att betala elektroniskt för försäljningar med en utbetalningtjänst, till exempel PayPal, kan du också ha PayPal-information och hyperlänk infogade i e-postbrödtexten.

Från alla dokument som stöds börjar du att e-posta genom att välja åtgärden **Skicka** på bokförda dokument, eller åtgärden **Bokför och skicka** på ej bokförda dokument.

Om fältet **E-posta** i fönstret **Skicka dokument till** anges till **Ja (fråga efter inställningar)** och sedan öppnas fönstret **Skicka e-post** med kontaktperson ifylld i fältet **Till:** och dokument som är bifogat som en PDF-fil. I fältet **brödtext** kan du antingen skriva in en text manuellt, eller också kan du fylla i fältet med en dokumentspecifik e-postbrödtext som du har ställt in.

Efterföljande procedur beskriver hur du ställer in rapporten **Försäljning - faktura** att användas för dokumentspecifika e-postbrödtexter, när du e-postar bokförda försäljningsfakturor.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Så här skapar du en dokumentspecifik e-postbrödtext för försäljningsfakturor
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Rapportval, försäljning** och välj sedan relaterad länk.
2. I fönstret **Rapportval, försäljning** i fältet **Användning** väljer du **Faktura**.
3. På en ny rad i fältet **Rappport-ID** väljer du t.ex. standardrapport 1306.
4. Markera kryssrutan **Använd för e-postbrödtex**.
5. Välj fältet **Layoutkod för brödtext i e-post** och välj sedan en layout från den nedrullningsbara listan.

    Rapportlayouter definierar både formatet och innehållet i e-postbrödtexten, inklusive standardtexten som föregår den centrala dokumentinformationen i e-postbrödtexten. Alla tillgängliga rapportlayouter visas om du väljer knappen **Välj från fullständig lista** i den nedrullningsbara listan.
6. Om du vill visa eller redigera den layout som e-postbrödtexten baseras på väljer du layout i fönstret **Redigera layouter** och väljer sedan **Redigera layout**.
7. Om du vill erbjuda dina kunder att betala elektroniskt för försäljningar kan du konfigurera relaterad utbetalningtjänst, till exempel PayPal, och sedan ha PayPal-information och hyperlänk infogade i e-postbrödtexten. Mer information finns i [Så här aktiverar du kundbetalningar via PayPal](sales-how-enable-payment-service-extensions.md).
8. Välj knappen **OK**.

Nu när du till exempel väljer åtgärden **Skicka** i fönstret **Bokförd försäljningsfaktura** kommer e-postbrödtexten att innehålla information om dokumentet i rapport 1306 som föregås av utformad standardtext enligt den rapportlayout du valde i steg 5.

Efterföljande procedur beskriver hur du skickar en bokförd försäljningsfaktura som ett e-postmeddelande med dokumentet bifogat som en PDF-fil och med dokumentspecifik e-postbrödtext.

## <a name="to-send-documents-by-email"></a>Så här skickar du dokument som e-post
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Bokförda försäljningsfakturor** och välj sedan relaterad länk.
2. Markera den relevanta bokförda försäljningsfakturan och välj åtgärden **Skicka**. Fönstret **Skicka dokument till** öppnas.
3. I fältet **E-post** väljer du **Ja (fråga efter inställningar)**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).
4. Välj knappen **OK**. Fönstret **Skicka e-post** öppnas.
5. I fältet **Till:** anger du en giltig e-postadress. Standardvärdet är kundens e-postadress.
6. Ange ett beskrivande ämnestext i fältet **Ämne**. Standardvärdet är kundnamnet och fakturanumret.
7. I fältet **Bilaga** är den genererade fakturan bifogad som standard som en PDF-fil. Välj uppslagningknappen för att öppna filen eller bifoga en annan.
8. Ange ett kort meddelande till mottagaren i fältet **Text**.

    Om en dokumentspecifik e-postbrödtext anges i fönstret **Rapportval - försäljning** kommer fältet **Brödtext** att fyllas i automatiskt. Mer information finns i avsnittet “Så här skapar du en dokumentspecifik e-postbrödtext för försäljningsfakturor” i detta ämne.
9. Välj knappen **OK** för att skicka e-postmeddelandet.

> [!NOTE]  
>   Om du inte vill ange e-postinställningar varje gång du e-postar ett dokument, kan du välja alternativet **Ja (använd standardinställningar)** i fältet **E-post** i fönstret **Skicka dokument till**. I så fall kommer inte fönstret **Skicka e-post** att öppnas. Se steg 4. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Se även
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Konfigurera e-post](admin-how-setup-email.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


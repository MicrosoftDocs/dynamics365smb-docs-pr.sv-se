---
title: Konfigurera dokumentspecifikt e-postinnehåll | Microsoft Docs
description: Du kan definiera innehåll som ska infogas i brödtexten i ett e-postmeddelande, till exempel en PayPal-länk. Du kan också koppla dokument till e-postmeddelanden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8e22efc92cba6d9a59cc06c66422387d5b35f227
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389630"
---
# <a name="send-documents-and-emails"></a>Skicka dokument och e-post
Du kan enkelt dela information och dokument, till exempel försäljnings- och inköpsorder och fakturor, via e-post direkt från [!INCLUDE[prod_short](includes/prod_short.md)]] utan att behöva öppna en e-postapp. 

Du kan skicka nästan alla typer av dokument som bifogade PDF-filer. Du kan också skapa en rapportlayout som innehåller information från dokumentet i e-postmeddelandets brödtext, tillsammans med text som gör e-postmeddelandet mer användarvänligt, till exempel en standardhälsning. Mer information finns i [Hantera rapporter och dokumentlayouter](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

När du skickar fakturor kan du göra det enklare för kunder att göra betalningar via en betaltjänst, till exempel PayPal, genom att automatiskt lägga till information och en länk till tjänsten i e-postmeddelandet. Mer information finns i [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).

Om du vill aktivera e-post i [!INCLUDE[prod_short](includes/prod_short.md)] startar du den assisterade inställningsguiden för **Konfigurera e-post**. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]] stöder endast utgående e-postkommunikation. Du kan inte heller ta emot svar inom appen.

## <a name="to-send-documents-by-email"></a>Så här skickar du dokument som e-post
Den här proceduren beskriver hur du kopplar en bokförd försäljningsfaktura till ett e-postmeddelande som en PDF-fil, samt med och med dokumentspecifik e-posttext. <!--update this-->

1. Välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda försäljningsfakturor** och välj sedan relaterad länk.
2. Markera fakturan och välj sedan åtgärden **Skriv ut/Skicka**.
3. I fältet **E-post** väljer du **Ja (fråga efter inställningar)**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).
    
    Om fältet **E-post** på sidan **Skicka dokument till** anges som **Ja (fråga efter inställningar)**, öppnas sidan **Skicka e-post** med kontaktpersonen förifylld i fältet **Till:** och dokumentet bifogat som en PDF-fil. I fältet **brödtext** kan du antingen skriva in en text manuellt, eller också kan du fylla i fältet med en dokumentspecifik e-postbrödtext som du har ställt in.

4. Välj **OK**.
5. I fältet **Till:** anger du en giltig e-postadress. Standardvärdet är kundens e-postadress.
6. Ange ett beskrivande ämnestext i fältet **Ämne**. Standardvärdet är kundnamnet och fakturanumret.
7. I fältet **Bilaga** är den genererade fakturan bifogad som standard som en PDF-fil.
8. Ange ett kort meddelande till mottagaren i fältet **Text**.

    Om en dokumentspecifik e-postbrödtext anges på sidan **Rapportval - Försäljning** kommer fältet **Brödtext** att fyllas i automatiskt. Mer information finns i [Konfigurera återanvändbara e-posttexter och -layouter för försäljnings- och inköpsdokument](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Välj knappen **OK** för att skicka e-postmeddelandet.

> [!NOTE]  
> Om du inte vill ange e-postinställningar varje gång du e-postar ett dokument, kan du välja alternativet **Ja (använd standardinställningar)** i fältet **E-post** på sidan **Skicka dokument till**. I så fall kommer inte sidan **Skicka e-post** att öppnas. Se steg 4. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).  

## <a name="to-compose-and-send-an-email"></a>Skriva och skicka ett e-postmeddelande
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **E-postkonton** och välj sedan tillhörande länk.
2. Välj det konto som du vill skicka e-postmeddelandet från och välj sedan åtgärden **Skriv e-post**.

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Dokument markerade som utskrivna ut när de skickas
Vissa dokument i [!INCLUDE[prod_short](includes/prod_short.md)] har ett fält som anger hur många gånger dokumentet har skrivits ut. Numret i fältet <!--"that field?" need a name...--> uppdateras också om du skickar dokumentet med e-post, detta eftersom en PDF-fil genereras för det. Numret uppdateras även om du inte skickar e-postmeddelandet. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Skickade e-postmeddelanden och din utkorg för e-post
[!INCLUDE[prod_short](includes/prod_short.md)]] lagrar e-postmeddelanden som du skickar på sidan **Skickade objekt**. Det gör att du kan skicka e-post på nytt eller vidarebefordra dem till någon annan. Om du inte hittar något e-postmeddelande bland dina skickade objekt kan du söka efter det på sidan **Utkorg för e-post**. 

> [!NOTE]
> Beroende på vilket tillägg företaget använder för e-post kan administratörer se en lista över alla meddelanden som har skickats, men inte innehållet i meddelandena

I **Utkorgen för e-post** finns de e-postmeddelanden som du har sparat som utkast samt e-postmeddelanden som inte skickades, till exempel om e-postadressen var ogiltig. För meddelanden som inte gick att skicka kan du välja **Visa fel** eller **Undersök fel** för att felsöka problemet.

## <a name="see-also"></a>Se även
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Konfigurera e-post](admin-how-setup-email.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
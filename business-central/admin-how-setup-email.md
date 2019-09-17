---
title: Skapa ett e-postkonto i Business Central | Microsoft Docs
description: Beskriver hur du använder företagets SMTP-server för att skicka och ta emot e-postmeddelanden inom Business Central, alternativt hur du använder e-postserverinställningarna som skapats med Office 365-prenumerationen.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 09/09/2019
ms.author: edupont
ms.openlocfilehash: b9a443072d13e3cbf5f8e07006bea5477c275968
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985940"
---
# <a name="set-up-email"></a>Konfigurera e-post
För att skicka och ta emot e-postmeddelanden inifrån [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du fylla i fälten på sidan SMTP-postinställning.

I stället för att ange information för SMTP-server manuellt kan du använda funktionen **Använd Office 365-serverinställningar** för att mata in information från din Office 365-prenumeration.

Du kan antingen skapa e-post skapar du manuellt eller också kan du få hjälp med hjälp av assisterad inställningsguide för **e-post**. Mer information finns i [Komma igång med att göra affärer](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Konfigurera e-post
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **SMTP-postinställningar** och välj sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Om du använder ett konto som kräver tvåfaktorautentisering måste lösenordet som du anger fältet **Lösenord** vara samma som du använder för Office 365-prenumerationen och det måste vara av typen **applösenord**.
3. Du kan också välja åtgärden **Använd Office 365-serverinställningar** för att infoga information som redan har definierats för din Office 365-prenumeration.
4. När alla fälten är korrekt ifyllda, väljer du åtgärden **Testa e-postinställningar**.
5. När testet lyckas stänger du sidan.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Använda en ersättningsavsändaradress i utgående e-postmeddelanden
Alla utgående e-postmeddelanden från [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer att använda standardadressen för det konto som du har angett på sidan SMTP-e-postinställning, som beskrivs ovan. Du kan emellertid använda funktionerna **Skicka som** eller **Skicka på uppdrag av** på Exchange-servern för att ändra avsändaradressen för utgående meddelanden. [!INCLUDE[d365fin](includes/d365fin_md.md)] använder standardkontot för att autentisera till Exchange, men kommer antingen att ersätta avsändarens adress med den som du anger eller ändra den med "för".

Nedan följer exempel på hur skicka och skicka för ombud används i [!INCLUDE[d365fin](includes/d365fin_md.md)].:

 * När du skickar dokument som inköps- eller försäljningsorder till leverantörer och kunder vill du kanske visa dem för att komma från adressen _noreply@yourcompanyname.com_.
 * När arbetsflödet skickar en godkännandeförfrågan via e-post med hjälp av e-postadressen till den som efterfrågar meddelandet.

> [!Note]
> Du kan bara använda ett konto för att ersätta avsändaradresser. Det innebär att du inte kan ha en ersättningsadress för att inköpsprocesser, och en annan för försäljningsprocesser.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Att ange ersättningsavsändaradress för alla utgående e-postmeddelanden
1. I **administrationscenter för Exchange** för ditt Office 365 konto hittar du den postlåda som ska användas som ersättningsadress, kopiera sedan eller gör ennotering av adressen. Om du behöver en ny adress går du till administrationscentret för Microsoft 365 för att skapa en ny användare och ställa in postlådan.
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] väljer du den ![glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **SMTP-postinställningar** och välj sedan relaterad länk.
3. I fältet **Skicka som** anger du ersättningsadressen.
4. Kopiera eller anteckna adressen i fältet **användar-ID**.
5. I **administrationscenter för Exchange** hittar du postlådan som ska användas som ersättningsadress och anger sedan adressen från fältet **Användar-ID** i **Skicka som**. Mer information finns i [Hantera behörigheter förmottagare](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Så här använder du ersättningsadressen i arbetsflöde för godkännande
1. I [!INCLUDE[d365fin](includes/d365fin_md.md)] väljer du den ![glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **SMTP-postinställningar** och välj sedan relaterad länk.
2. Kopiera eller anteckna adressen i fältet **användar-ID**.
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användarinställningar för godkännande** och välj sedan relaterad länk.
4. I **administrationscenter för Exchange** hittar du postlådan för varje användare som finns på sidan **Användarinställningar för godkännande** och i fältet **Skicka som** anger du adressen från fältet **Användar-ID** för sidan **SMTP-postinställningar** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Hantera behörigheter förmottagare](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. I [!INCLUDE[d365fin](includes/d365fin_md.md)] väljer du den ![glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **SMTP-postinställningar** och välj sedan relaterad länk.
6. Aktivera ersättning genom att aktivera växling **Tillåt avsändarens ersättning**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] avgör vilken adress som ska visas i följande ordning: <br><br> 1. Adressen som anges i fältet **e-post** på sidan **Användarinställningar för godkännande** för meddelanden i ett arbetsflöde. <br> 2. Adressen som anges i fältet **skicka som** på sidan **SMTP-postinställningar**. <br> 3. Adressen som anges i fältet **Användar-ID** på sidan **SMTP-postinställningar**.


## <a name="see-also"></a>Se även  
[Delade postlådor i Exchange Online](https://docs.microsoft.com/en-us/exchange/collaboration-exo/shared-mailboxes)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som din företagsinkorg i Outlook](admin-outlook.md)  
[Få [!INCLUDE[d365fin](includes/d365fin_md.md)] på min mobila enhet](install-mobile-app.md)

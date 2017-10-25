---
title: "Gör så här: Kontrollera momsregistreringsnummer | Microsoft Docs"
description: "Du kan använda en EU-webbtjänst för att kontrollera att de momsregistreringsnummer som du anger på kund-, leverantörs- eller kontaktkort är giltiga."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a>Gör så här: Kontrollera momsregistreringsnummer
Du kan använda en EU-webbtjänst för att kontrollera att de momsregistreringsnummer som du anger på kund-, leverantörs- eller kontaktkort är giltiga.  

 När du ändrar fältet **Momsregistreringsnummer** på ett kort där värdet i **Land-/regionskod** är ett EU-land/-region loggas sedan det nya momsregistreringsnumret och ditt användar-ID i fönstret **Momsregistreringslogg**. Du validerar ett momsregistreringsnummer genom att välja knappen **Kontrollera registreringsnr** i fönstret **momsregistreringslogg**. En ny rad skapas varje gång du använder verifikationsfunktionen. Om numret kan verifieras innehåller fältet **Status** **Giltigt**. Om numret inte kan verifieras innehåller fältet **Status** **Ogiltig** och du måste då ändra numret i fältet **Momsregistreringsnr** på kortet och starta verifikationsfunktionen igen.  

 Webbadressen för standardwebbtjänsten ställs in i fältet **Validerings-URL för momsreg.nr** i fönstret **Redovisningsinställningar**.  

 I tabellen **Momsregistreringsnr format** kan du för varje land/region ändra de olika format för momsregistreringsnummer som användare tillåts ange i fältet **Momsregistreringsnr**.  

> [!WARNING]  
>  Den här webbtjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.  

> [!NOTE]  
>  Du kan drabbas av stilleståndstid, vilket inte är Microsofts ansvar, för den här tjänsten eftersom den ingår i ett omfattande EU-nätverk av nationella mervärdeskattregister.  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a>Så här verifierar du ett momsregistreringsnummer från ett kundkort  
Nedan beskrivs hur du kontrollerar momsregistreringsnummer för en kund. Momenten är liknande för en leverantör och en kontakt.   
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kunder** och välj sedan relaterad länk.  

2.  Öppna kortet för en kund du vill kontrollera momsregistreringsnumret för.  

    > [!NOTE]  
    >  Fältet **Lands-/regionkod** på kundkortet måste innehålla ett land/en region i EU.  
3.  På snabbfliken **Fakturering** väljer du knappen **Momsregistreringsnr**.  

    Fönstret **Momsregistreringslogg** öppnas och visar en rad där fältet **Status** innehåller **Ej verifierad**.  
4.  Välj åtgärd **Kontrollera registreringsnr**.  

     En ny rad skapas när fältet **Status** antingen innehåller **Giltigt** eller **Ogiltigt**.  
5.  Om fältet **Status** innehåller **Ogiltig**, ändrar du numret i fältet **Momsregistreringsnr.** på kortet och upprepar sedan steg 3 till 4.  

## <a name="see-also"></a>Se även  
[Ekonomi](finance.md)  
[Så här registrerar du nya kunder](sales-how-register-new-customers.md)  
[Så här registrerar du nya leverantörer](purchasing-how-register-new-vendors.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


---
title: Validera ett momsregistrerings nummer | Microsoft Docs
description: Validera ett momsregistreringsnummer
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 4b282d8819851fd6529f901f44a39777a8b8e74c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183074"
---
# <a name="validate-a-vat-registration-number"></a>Validera ett momsregistreringsnummer

## <a name="to-verify-vat-registration-numbers"></a>Kontrollera momsregistreringsnummer
Det är viktigt att momsregistreringsnummer för kunder, leverantörer och kontakter är giltiga. Till exempel ändrar företag sin skatteskuldstatus och i vissa länder kan skattemyndigheterna be dig lämna rapporter som t.ex. EG-försäljningslisterapport som anger de momsregistreringsnummer som du använder när du gör affärer.

Europeiska kommissionen har en tjänst för VIES momsnummervalidering på sin webbplats som är offentlig och kostnadsfri. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan spara dig det steget och låter dig använda VIES-tjänsten för verifiering och spåra momsregistreringsnummer för kunder, leverantörer och kontakter direkt från kund-, leverantörs- och kontaktkort. Tjänsten i [!INCLUDE[d365fin](includes/d365fin_md.md)] heter **Valideringstjänst för EU momsreg.nr.**. Den är tillgänglig på sidan **Anslutningar till tjänst**, och du kan börja använda den direkt. Registrering behövs inte och tjänsten är gratis.

För att aktivera **Valideringstjänst för EU momsreg.nr.** öppnar du posten på sidan **Anslutning till tjänst**. Fältet **Tjänstslutpunkt** ska redan vara ifyllt. Om så inte är fallet kan du använda åtgärden **Ställ in standardslutpunkt**. Ange sedan fältet **Aktiverad** och du är redo att sätta igång.

> [!Note]
> Om du vill aktivera valideringstjänsten för EU momsreg.nr. måste du ha administratörsrättigheter.

När du använder vår tjänst registrerar vi en historik över momsregistreringsnummer och kontroller för varje kund, leverantör eller kontakt i **momsregistreringslogga**, så att du enkelt kan spåra dem. Loggen är unik för varje kund. Loggen är användbar för att verifierat att det aktuella momsregistreringsnumret är korrekt. När du verifierar ett momsregistreringsnummer kommer kolumnen **begär ID** i loggen att visa att du har vidtagit åtgärder.

Du kan se momsregistreringsloggen på kund-, leverantör- eller kontaktkorten på snabbfliken **fakturering** genom att välja sökknappen i **Momsregistreringsnr.**  

Tjänsten kan också spara tid när du skapar en kund eller leverantör. Om du känner till kundens momsregistreringsnummer kan du ange det i fältet **Momsregistreringsnr** på korten för kunden eller leverantören, och vi ska fylla i kundens namn åt dig. Vissa länder har dessutom företagsadresser i ett strukturerat format. I dessa länder fyller vi även i addressen.  

Det finns ett par saker att komma ihåg om tjänsten VIES momsnummervalidering:

* Den här tjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.  
* Det kan uppstå avbrott för den här tjänsten som inte Microsoft ansvarar för. Tjänsten är en del av ett omfattande EU-nätverk av nationella register för moms.

## <a name="see-also"></a>Se även  
[Ställa in moms](finance-setup-vat.md)  
[Ställa in orealiserad mervärdesskatt (moms)](finance-setup-unrealized-vat.md)      
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)

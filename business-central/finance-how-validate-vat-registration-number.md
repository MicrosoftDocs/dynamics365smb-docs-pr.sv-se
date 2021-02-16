---
title: Validera momsregistreringsnummer
description: Låt Business Central använda VIES-tjänsten för att validera momsregistrerings nummer automatiskt.
author: kielkenny
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 80e955e96a64c5a0bd91d0a72297b32d67ff4ab6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750567"
---
# <a name="validate-vat-registration-numbers"></a>Validera momsregistreringsnummer

Det är viktigt att momsregistreringsnummer för kunder, leverantörer och kontakter är giltiga. Till exempel ändrar företag sin skatteskuldstatus och i vissa länder kan skattemyndigheterna be dig lämna rapporter som t.ex. EG-försäljningslisterapport som anger de momsregistreringsnummer som du använder när du gör affärer.

Europeiska kommissionen har en tjänst för VIES momsnummervalidering på sin webbplats som är offentlig och kostnadsfri. [!INCLUDE[prod_short](includes/prod_short.md)] kan spara dig det steget och låter dig använda VIES-tjänsten för verifiering och spåra momsregistreringsnummer för kunder, leverantörer och kontakter direkt från kund-, leverantörs- och kontaktkort. Tjänsten i [!INCLUDE[prod_short](includes/prod_short.md)] heter **Valideringstjänst för EU momsreg.nr.**. Den är tillgänglig på sidan **Anslutningar till tjänst**, och du kan börja använda den direkt. Registrering behövs inte och tjänsten är gratis.

## <a name="to-verify-vat-registration-numbers"></a>Kontrollera momsregistreringsnummer

För att aktivera **Valideringstjänst för EU momsreg.nr.** öppnar du posten på sidan **Anslutning till tjänst**. Fältet **Tjänstslutpunkt** ska redan vara ifyllt. Om så inte är fallet kan du använda åtgärden **Ställ in standardslutpunkt**. Ange sedan fältet **Aktiverad** och du är redo att sätta igång.

> [!NOTE]
> Om du vill aktivera valideringstjänsten för EU momsreg.nr. måste du ha administratörsrättigheter.

När du använder vår tjänst registrerar vi en historik över momsregistreringsnummer och kontroller för varje kund, leverantör eller kontakt i **momsregistreringslogga**, så att du enkelt kan spåra dem. Loggen är unik för varje kund. Loggen är användbar för att verifierat att det aktuella momsregistreringsnumret är korrekt. När du verifierar ett momsregistreringsnummer kommer kolumnen **begär ID** i loggen att visa att du har vidtagit åtgärder.

Du kan se momsregistreringsloggen på kund-, leverantör- eller kontaktkorten på snabbfliken **fakturering** genom att välja sökknappen i **Momsregistreringsnr.**  

Tjänsten kan också spara tid när du skapar en kund eller leverantör. Om du känner till kundens momsregistreringsnummer kan du ange det i fältet **Momsregistreringsnr** på korten för kunden eller leverantören, och vi ska fylla i kundens namn åt dig. Vissa länder har dessutom företagsadresser i ett strukturerat format. I dessa länder fyller vi även i addressen.  

Det finns ett par saker att komma ihåg om tjänsten VIES momsnummervalidering:

* Den här tjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.  
* Det kan uppstå avbrott för den här tjänsten som inte Microsoft ansvarar för. Tjänsten är en del av ett omfattande EU-nätverk av nationella register för moms.

> [!IMPORTANT]
> Det är ditt ansvar att kontrollera att alla data är giltiga. Ibland returneras data med fel av tjänsten VIES momsnummervalidering. Om valideringen misslyckas validerar du momsregistreringsnumren på [webbplatsen](https://ec.europa.eu/taxation_customs/vies/), skriver ut resultatet eller sparar det på en delad plats och lägger sedan till länken till posten för kunden, leverantören eller kontakten. För mer information, se [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).

## <a name="see-also"></a>Se även

[Ställa in moms](finance-setup-vat.md)  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  

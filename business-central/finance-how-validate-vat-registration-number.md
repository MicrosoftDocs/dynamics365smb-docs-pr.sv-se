---
title: Validera momsregistreringsnummer
description: 'Låt Business Central validera momsregistreringsnummer för dina kontakter, kunder och leverantörer, baserat på EU:s VIES-valideringstjänst för momsnummer.'
author: jswymer
ms.topic: conceptual
ms.reviewer: jswymer
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Validera momsregistreringsnummer

Det är viktigt att dina momsregistreringsnummer för kunder, leverantörer och kontakter är giltiga om du använder [!INCLUDE [prod_short](includes/prod_short.md)] i ett land/region som använder moms. Till exempel ändrar företag ibland sin skatteskuldstatus, och i vissa länder/regioner kan skattemyndigheterna be dig att lämna in rapporter, t. ex. rapporten **EC försäljningslista**, som anger de momsregistreringsnummer som du använder när du bedriver din verksamhet.

Europeiska kommissionen har en tjänst för VIES momsnummervalidering på sin webbplats som är offentlig och kostnadsfri. [!INCLUDE [prod_short](includes/prod_short.md)] kan bespara dig det steget, och låter dig använda VIES-tjänsten för att verifiera och spåra momsregistreringsnummer och annan företagsinformation för kunder, leverantörer och kontakter. Tjänsten i [!INCLUDE [prod_short](includes/prod_short.md)] heter **Valideringstjänst för EU momsreg.nr.**. Den är tillgänglig på sidan **Anslutningar till tjänst**, och du kan börja använda den direkt. Serviceanslutningen är kostnadsfri, och ytterligare registrering behövs inte.

## Konfigurera tjänsten för att verifiera momsregistreringsnummer automatiskt

För att aktivera **Valideringstjänst för EU-momsreg.nr.** öppnar du posten på sidan **Anslutning till tjänst**. Om fältet **Tjänsteslutpunkt** inte redan är ifyllt använder du åtgärden **Ange standardslutpunkt**. Ange sedan fältet **Aktiverad**, och du är redo att sätta igång.  

> [!IMPORTANT]
> Du måste ha administratörsrättigheter för att kunna aktivera valideringstjänsten.

Du kan också skapa mallar för de typer av momsrelaterade data som du vill att tjänsten också ska kontrollera. Mer information finns i avsnittet [Valideringsmallar](#validation-templates).

När du använder vår tjänst registrerar vi en historik över momsregistreringsnummer och kontroller för varje kund, leverantör eller kontakt i **momsregistreringslogga**, så att du enkelt kan spåra dem. Loggen är unik för varje kund. Loggen är användbar för att verifierat att det aktuella momsregistreringsnumret är korrekt. När du verifierar ett momsregistreringsnummer kommer kolumnen **begär ID** i loggen att visa att du har vidtagit åtgärder.

Du kan se momsregistreringsloggen på kund-, leverantör- eller kontaktkorten på snabbfliken **fakturering** genom att välja sökknappen i **Momsregistreringsnr.**  

Det finns ett par saker att komma ihåg om tjänsten VIES momsnummervalidering:

* Den här tjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.  
* Det kan uppstå avbrott för den här tjänsten som inte Microsoft ansvarar för. Tjänsten är en del av ett omfattande EU-nätverk av nationella register för moms.

> [!IMPORTANT]
> Det är ditt ansvar att kontrollera att alla data är giltiga. Ibland returneras data med fel av tjänsten VIES momsnummervalidering. Om valideringen misslyckas validerar du momsregistreringsnumren på [webbplatsen](https://ec.europa.eu/taxation_customs/vies/), skriver ut resultatet eller sparar det på en delad plats och lägger sedan till länken till posten för kunden, leverantören eller kontakten. För mer information, se [Hantera bifogade filer, länkar och anteckningar på kort och dokument](ui-how-add-link-to-record.md).

## Valideringsmallar

Du kan använda VIES-tjänsten för att även kontrollera annan företagsinformation, till exempel adressen, samt momsregistreringsnumret. På sidan **Valideringsmallar för momsregistreringsnr.** skapar du en post för varje land/region som du vill få ytterligare validering för, och anger sedan den information som du vill få validerad automatiskt.  

Lägg till exempel till en post för Spanien där du vill få validering för namn, gata, ort och postnummer, och sedan ytterligare en post för Tyskland, där du bara vill ha validering för exempelvis postnummer. På sidan **Konfigurering av EU:s valideringstjänst för momsregistreringsnr.** anger du sedan standardmallen.  

> [!NOTE]
> Se alltid till att standardmallen fungerar för dina behov. Du kan ändra standardvärdet så att det matchar dina behov, till exempel för att hämta validering för alla fält eller inga fält.

Nästa gång du anger ett momsregistreringsnummer validerar tjänsten numret och eventuella ytterligare data som bestäms av valideringsmallarna. Om de angivna värdena skiljer sig från de värden som returneras av tjänsten visas informationen på sidan **Valideringsinformation** där du kan acceptera eller återställa värdena.  

## Se även

[Ställa in moms](finance-setup-vat.md)  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)  
[Rapportera moms till skattemyndigheterna](finance-how-report-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

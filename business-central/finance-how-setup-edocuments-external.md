---
title: Konfigurera anslutningsprogrammet för e-dokument med externa slutpunkter
description: Den här artikeln förklarar hur du ställer in funktioner för e-dokument när den är ansluten till externa slutpunkter.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-the-e-documents-connector-with-external-endpoints"></a>Konfigurera anslutningsprogrammet för e-dokument med externa slutpunkter

Den här artikeln förklarar hur du ställer in funktioner för e-dokument när den är ansluten till externa slutpunkter.

Innan du använder funktionen som beskrivs i den här artikeln, installera appen **anslutningsprogrammet för e-dokument med externa slutpunkter** ovan på den globala appen **Grundläggande e-dokument**. Denna app kan användas för standardintegration med externa (tredje parts) åtkomstpunkter för att automatisera e-dokumentflödet. Eftersom den här appen endast representerar några av de valda anslutningsprogrammen är du inte begränsad till befintliga integrationer i den. De flesta av anslutningsprogrammet kommer att finnas tillgängliga på AppSource i framtiden.

## <a name="set-up-the-connection"></a>Ställer in anslutningsprogram

För att påbörja din installation, följ stegen i [Grundläggande e-dokument](finance-how-setup-edocuments.md). När du har slutfört dessa steg, gå tillbaka till den här artikeln och slutför följande steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **E-dokumenttjänst** och väljer sedan relaterad länk.
2. I fältet **Tjänstintegration** välj en av integrationskoderna som erbjuds för slutpunktstjänsten.
3. Välj **Konfigurera tjänstintegration**.
4. På sidan **Konfiguration av extern anslutning för e-dokument** välj **Begär auktoriseringskod**. Du omdirigeras till webbsidan för extern tjänstauktorisering och tillfrågas om dina inloggningsuppgifter.
5. Kopiera auktoriseringskoden till fältet **Ange behörighetskod**.
6. Välj **Uppdatera åtkomsttoken** för att se till att du kan uppdatera token.

    > [!NOTE]
    > Denna anslutning kräver kommunikation med externa tjänsteleverantörer som kan bli föremål för ytterligare betalning och kräver kontrakt med dem. För att få alla nödvändiga referenser, kontakta tjänsteleverantörerna.

7. På sidan **Konfiguration av extern anslutning för e-dokumentp** fyller du i följande fält:

    | Fältnamn | Beskrivning |
    |---|---|
    | URL för FileAPI | Ange filens API-URL. |
    | URL för fildelar | Ange fildelens URL. |
    | URL för DocumentAPI | Ange dokumentets API-URL. |
    | Företags-ID | Ange företags-ID. |
    | Sändningsläge | Ange sändningsläge. Du kan välja **Produktion**, **Test** eller **Certifiering**. |

    > [!NOTE]
    > Be din tjänsteleverantör om alla tidigare detaljer för att upprätta en anslutning till sin åtkomstpunkt.

## <a name="set-up-company-information"></a>Konfigurera företagsinformation

Innan du börjar använda e-dokument, uppdatera sidan **företagsinformation** genom att utföra följande steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Företagsinformation** och väljer sedan relaterad länk.
2. Förutom att fylla i de vanliga fälten måste du även fylla i följande fält:

    | Fältnamn | Beskrivning |
    |---|---|
    | SWIFT-kod | Ange SWIFT-koden (internationellt bank-id) för din primära bank. |
    | Bankfilialnr | Ange bankens fyrsiffriga kontorsnummer. |
    | Momsregistreringsnr | Ange företagets momsregistreringsnummer. |

3. Stäng sidan.

## <a name="set-up-customers-to-receive-e-documents"></a>Ställ in kunder att ta emot e-dokument

För att göra det möjligt för kunder att ta emot dina e-dokument, utför följande steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Öppna **kundkortet**.
3. Förutom att fylla i de vanliga fälten, i fältet **GLN**, ange kunden i samband med att elektroniska dokument skickas.
4. Markera fältet **Använd GLN i elektroniska dokument** för att ange om det globala lokaliseringsnumret (GLN) används som partsidentifikationsnummer i elektroniska dokument.
5. Stäng sidan.

## <a name="other-setup"></a>Annan konfiguration

Innan du börjar arbeta med e-dokument, ställ in e-dokument **arbetsflöden** och **dokumentutskicksprofil** till använda dina arbetsflöden. Efter att tjänstanslutningen har upprättats kan du börja använda din e-dokumentlösning.

## <a name="available-service-providers"></a>Tillgängliga tjänsteleverantörer

Microsoft vill uppmuntra åtkomstpunktsleverantörer att lägga till sina kontakter ovanpå vårt ramverk **Grundläggande e-dokument**.

För närvarande är Pagero den enda åtkomstpunktsleverantören som omfattas av detta system. Microsoft har inga avtalsenliga skyldigheter med Pagero. Därför måste du göra ett kontrakt med dem för att få alla nödvändiga autentiseringsuppgifter.

Vi kommer att uppdatera den här listan när vi får nya åtkomstpunktsleverantörer av e-dokumentutbyte.

## <a name="see-also"></a>Se även

[Hur man ställer in e-dokument i Business Central](finance-how-setup-edocuments.md)  
[Hur man använder e-dokument i Business Central](finance-how-use-edocuments.md)  
[Hur man utökar e-dokument i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Ekonomihantering](finance.md)  
[Fakturera försäljning](sales-how-invoice-sales.md)  
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]

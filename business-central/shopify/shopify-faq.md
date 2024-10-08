---
title: FAQ för teknisk information
description: Implementeringsinformation för Shopify kopplingen.
ms.date: 05/01/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="faq-for-technical-details"></a>FAQ för teknisk information

Den här artikeln svarar på vanliga frågor om Shopify-anslutningsprogrammet.

## <a name="what-is-shopify"></a>Vad är Shopify?

Shopify är ett paketbaserade program som gör att vem som helst kan ställa in en onlinebutik och sälja sina produkter. Shopify plattformen erbjuder online återförsäljare en serie tjänster för betalningar, marknadsföring, leverans och kundengagemang.

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>Vad är Microsoft Dynamics 365 Business Central Shopify-anslutningsprogrammet?

Med Shopify-anslutningsprogrammet kan företag ansluta sina Shopify butik med [!INCLUDE[prod_short](../includes/prod_short.md)] för att maximera företagets produktivitet. Genom att använda Shopify-anslutningsprogrammet kan de få åtkomst till och hantera insikter från sin verksamhet och sina Shopify online butik som en enhet.

### <a name="capabilities"></a>Funktioner

- Stöd för fler än en Shopify-butik
  - Varje butik har sina egna inställningar, inklusive en samling produkter, platser som används för att beräkna lager och prislistor.  
- Synkronisering av artiklar eller produkter med dubbel riktning
  - Kopplingen synkroniserar bilder, artikelvarianter, streckkoder, leverantörens artikelnummer, utökade och marknadsföringstexter och taggar.  
  - Exportera artikelattribut till Shopify.  
  - Använd valda kundprisgrupper och -rabatter för att definiera priser som exporteras till Shopify.
  - Definiera priser och rabatter för produktkataloger kopplade till B2B-företag.
  - Bestäm om artiklar kan skapas automatiskt eller tillåta uppdateringar av befintliga produkter.
- Synkronisera lagernivåer
  - Välj några av eller alla tillgängliga platser i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Uppdatera lager nivåer på flera lagerställen i Shopify.  
- Synkronisering av kunder och företag med dubbel riktning
  - Smartmappa kunder via telefon och e-post.  
  - Använd land-//regionsspecifika mallar när du skapar kunder, vilket säkerställer att skatteinställningarna är korrekta.  
- Importera order från Shopify
  - Inkludera beställningar som skapats i olika försäljningskanaler, såsom webbutik, **Shopify POS** eller **B2B**.
  - Leverans kostnader, presentkort, tips, leverans- och betalningsmetoder, transaktioner och risk för bedrägerier.  
  - Under importen kan du automatiskt skapa kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestämma dig för att hantera kunderna i Shopify.  
  - Ta emot utbetalnings information från Shopify Payments.
- Spåra uppfyllelse information
  - Om du vill kan du välja att överföra artikelspårningsinformation från [!INCLUDE [prod_short](../includes/prod_short.md)] till Shopify.
- Fjärradministrerad integration
  - Aktivera automatisk synkronisering av produkter, lager, order, uppfyllelse med mera.

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>Varför lät Microsoft och Shopify bilda det här partnerskapet?

[!INCLUDE[prod_short](../includes/prod_long.md)] har ett samarbete med Shopify för att hjälpa våra kunder att skapa en bättre kundupplevelse. När Shopify ger handlare en lättanvänd handelslösning, [!INCLUDE[prod_short](../includes/prod_short.md)] erbjuder omfattande företagsledning över ekonomi-, försäljnings-, service- och driftteam. Använd den sömlösa anslutningen mellan programmen för att synkronisera order, lager och kundinformation så att butikerna kan uppfylla beställningar snabbare och betjäna kunderna bättre.

## <a name="which-microsoft-products-work-with-the-shopify-connector"></a>Vilka Microsoft-produkter är Shopify-anslutningsprogrammet tillgängliga för?

Anslutningsprogrammet är endast tillgängligt för [!INCLUDE[prod_short](../includes/prod_short.md)] online, som börjar med version 20.1. Det stöds inte i lokala installationer. Anslutningsprogrammet är förinstallerat för nya miljöer. Organisationer med befintliga miljöer kan hämta och installera anslutningsprogrammet från AppSource. Organisationen måste ha både en [!INCLUDE [prod_short](../includes/prod_short.md)]-licens och en Shopify-licens för att kunna använda anslutningsprogram. Mer information om länder/regioner som stöds, språk och utgåvor för [!INCLUDE[prod_short](../includes/prod_short.md)] finns i [Shopify-anslutningsprogram på AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-anslutningen fungerar inte för [inbäddad app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), där klient-URL har formatet: `https://[application name].bc.dynamics.com`.

Shopify anslutningsprogram fungerar inte med andra produkter i Dynamics 365-portföljen.

## <a name="what-support-is-offered-for-the-shopify-connector"></a>Vilket stöd erbjuds för Shopify-anslutningsprogrammet?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify-anslutningsprogrammet täcks av den aktuella stöd modellen. Mer information finns i [Teknisk support](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (finns endast på engelska).

Få hjälp från en konsult som känner till Shopify anslutningsprogram för [!INCLUDE[prod_short](../includes/prod_short.md)], för att uppfylla dina unika företagsspecifika krav. Sök i [konsulttjänster](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Om du vill ha hjälp med Shopify, från [Allmänt Shopify hjälpcenter](https://help.shopify.com/) eller från [24/7 support för din butik som en Shopify handlarens](https://help.shopify.com/questions#/).

Du kan också utforska [Expertmarknaden](https://experts.shopify.com/) och hitta rätt experter som erbjuder tjänster för Shopify handlare.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them"></a>Funktioner som inte stöds, men vi följer upp dem och kan tänka på att lägga till dem

- Marknader
  - Flera översättningar av huvuddata. Du kan välja ett språk som ska användas för export av produktinformation.
  - Priser per land/region. En prislista är tillgänglig för den valda valutan. Shopify hanterar omvandlingen till andra valutor.
- Utkastorder

## <a name="is-the-shopify-connector-extensible"></a>Kan Shopify-anslutningsprogrammet utökas?

Ja Shopify-anslutningsprogrammet kan utökas. Kontrollera GitHub för att komma åt [listan över utökningsbarhetspunkter](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) och utforska några [exempel](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify).

## <a name="is-the-shopify-connector-open-for-contribution"></a>Är Shopify-anslutningsprogrammet öppen för bidrag?

Det här tillägget är öppet för bidrag från vår community. Du hittar [källkoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i databasen Microsoft Al arkiv för programtillägg.

## <a name="building-your-version-of-the-shopify-connector"></a>Skapa din version av anslutningsprogrammet för Shopify

Enligt Shopify, om du vill skapa och publicera en anslutningsapp på Shopify marknadsplats som har det primära syftet att överföra eller dela säljardata till en tredje part ([!INCLUDE [prod_short](../includes/prod_short.md)]) måste du ha skriftligt medgivande från Shopify. Som en del av den här processen måste du få medgivande från Microsoft i "Formulär för databekräftelse för slutmottagare". Vi måste be dig att hantera ärendet med Shopify eftersom Microsoft inte kan teckna tredjepartsavtal.

### <a name="what-to-do"></a>Vad du gör

Kontrollera Shopify kraven eftersom du fortfarande kanske kan ha en olistad app.

Alternativt får anslutningsprogrammet för Shopify för [!INCLUDE [prod_short](../includes/prod_short.md)] ständigt nya funktioner och nya kunder. Om du upptäcker en specifik lucka kan du överväga att [skicka in ett produktförslag](https://aka.ms/bcideas) eller ett kodbidrag till [!INCLUDE [prod_short](../includes/prod_short.md)]. Om du vill ha krav som kanske inte är relevanta för en majoritet av kunderna och som inte enkelt kan hanteras av den aktuella utökningsbarhetsmodellen kontaktar du [!INCLUDE [prod_short](../includes/prod_short.md)] utvecklingsteamet för att diskutera användningsfallet. Vi borde kunna hitta en genomförbar lösning.

## <a name="see-also"></a>Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

---
title: FAQ för teknisk information
description: Implementeringsinformation för Shopify kopplingen.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# FAQ för teknisk information

Den här artikeln svarar på vanliga frågor om Shopify-kopplingen.

## Vad är Shopify? 

Shopify är ett paketbaserade program som gör att vem som helst kan ställa in en onlinebutik och sälja sina produkter. Shopify plattformen erbjuder online-detaljister en serietjänster som omfattar verktyg för betalningar, marknadsföring, leverans och kund engagemang. 

## Vad är Microsoft Dynamics 365 Business Central Shopify-anslutning? 

Med Shopify-anslutning kan företag ansluta sina Shopify butik (eller butiker) med [!INCLUDE[prod_short](../includes/prod_short.md)] för att maximera företagets produktivitet. Genom att använda Shopify-anslutning kan de hantera och se insikter från sin verksamhet och sina Shopify online butik som en enhet. 

### Funktioner

- Stöd för fler än en Shopify-butik
  - Varje butik har sina egna inställningar, inklusive en samling produkter, platser som används för att beräkna lager och prislistor.  
- Synkronisering av artiklar eller produkter med dubbel riktning
  - Kopplingen synkroniserar bilder, artikelvarianter, streckkoder, leverantörens artikel nummer, extratexter och taggar.  
  - Exportera artikelattribut till Shopify.  
  - Använd valda kundprisgrupper och -rabatter för att definiera priser som exporteras till Shopify.  
  - Bestäm om artiklar kan skapas automatiskt eller tillåta uppdateringar av befintliga produkter.  
- Synkronisera lagernivåer
  - Välj några av eller alla tillgängliga platser i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Uppdatera lager nivåer på flera lagerställen i Shopify.  
- Synkronisering av kunder med dubbel riktning
  - Smartmappa kunder via telefon och e-post.  
  - Använd landsspecifika mallar när du skapar kunder, vilket säkerställer att skatteinställningarna är korrekta.  
- Importera order från Shopify
  - Inkludera beställningar som skapats i olika försäljningskanaler, såsom webbutik eller **Shopify POS**. 
  - Leverans kostnader, presentkort, tips, leverans- och betalningsmetoder, transaktioner och risk för bedrägerier.  
  - Under importen kan du automatiskt skapa kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestämma dig för att hantera kunderna i Shopify.  
  - Ta emot utbetalnings information från Shopify Payments. 
- Spåra uppfyllelse information
  - Om du vill kan du välja att överföra artikelspårningsinformation från [!INCLUDE [prod_short](../includes/prod_short.md)] till Shopify.  

## Varför lät Microsoft och Shopify bilda det här partnerskapet? 

[!INCLUDE[prod_short](../includes/prod_long.md)] har ett samarbete med Shopify för att hjälpa våra kunder att skapa en bättre kundupplevelse. När Shopify ger handlare en lättanvänd handelslösning, [!INCLUDE[prod_short](../includes/prod_short.md)] erbjuder omfattande företagsledning över ekonomi-, försäljnings-, service- och driftteam inom en enda app. Med sömlös anslutning mellan de två systemen synkroniseras order, lager och kund information så att butikerna kan uppfylla beställningar snabbare och betjäna kunderna bättre.

## Vilka Microsoft-produkter är Shopify-anslutningen tillgängliga för?

Den här funktionen är endast tillgänglig [!INCLUDE[prod_short](../includes/prod_short.md)] online, som börjar med version 20.1. Det stöds inte i lokala installationer. Appen med anslutning är förinstallerad för nya miljöer. Organisationer med befintliga miljöer kan hämta och installera appen från AppSource. Organisationen måste ha både en Business Central-licens och en Shopify-licens för att kunna använda anslutning. Mer information om länder som stöds, språk och utgåvor för [!INCLUDE[prod_short](../includes/prod_short.md)] finns i [Shopify-anslutningen på AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-anslutningen fungerar inte för [inbäddad app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), där klient-URL har formatet: `https://[application name].bc.dynamics.com`. 

## Vilket stöd erbjuds för Shopify-anslutningen?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify kopplingen täcks av den aktuella stöd modellen. Mer information finns i [Teknisk support](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (finns endast på engelska). 

Få hjälp från en konsult som känner till Shopify anslutningsprogram för [!INCLUDE[prod_short](../includes/prod_short.md)], för att uppfylla dina unika företagsspecifika krav.
 
Sök i [konsulttjänster](https://aka.ms/BCShopifyConsultant).

### Shopify

Om du vill ha hjälp med Shopify, starta med [Allmänt Shopify hjälpcenter](https://help.shopify.com/) eller [24/7 Support för din butik som en Shopify handlarens](https://help.shopify.com/questions#/). 

Du kan också utforska [Expertmarknaden](https://experts.shopify.com/) och hitta rätt experter som erbjuder tjänster för Shopify handlare.

## Funktioner som inte stöds, men vi följer upp dem och kan tänka på att lägga till dem i framtiden:

- B2B-funktioner, inklusive företag, företagsprislistor, betalningsvillkor
- Marknader
  - Flera översättningar av huvuddata. Du kan välja ett språk som ska användas för export av produktinformation.
  - Priser per land/region. En prislista är tillgänglig för den valda valutan. Konverteringen till andra valutor kommer att hanteras av Shopify.

## Kan Shopify-anslutningen utökas?

För närvarande är den här appen icke-utökningsbar med planer för att göra den utökningsbar i 2023. 

## Är Shopify-anslutningen öppen för bidrag

Ja, detta tillägg är öppet för bidrag från communityn. Du hittar [källkoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i databasen Microsoft Al arkiv för programtillägg.


## Se även

[Kom igång med kopplingen för Shopify](get-started.md)  

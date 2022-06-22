---
title: Komma igång med kopplingen för Shopify
description: Första stegen när du konfigurerar anslutningen mellan Business Central och Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 64fae9efdda832f14593564b9a19101d120c9712
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808939"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom igång med Shopify-kopplingen

Anslut din Shopify butik (eller butiker) med [!INCLUDE [prod_short](../includes/prod_short.md)] och maximera företagets produktivitet. Hantera och visa insikter från ditt företag och din Shopify butik som en enhet. 

Shopify-anslutningen innehåller följande funktioner:

- Stöd för fler än en Shopify-butiker  

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

  - Under importen kan du automatiskt skapa kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller bestämma dig för att hantera kunderna i Shopify.  
  - Ta med order som skapats i andra kanaler, till exempel Shopify POS eller Amazon.  
  - Leverans kostnader, presentkort, tips, leverans- och betalningsmetoder, transaktioner och risk för bedrägerier.  
  - Ta emot utbetalnings information från Shopify Payments.  
- Enkel spårning av uppfyllelse information  

  - Om du vill kan du välja att skriva artikelspårningsinformation från [!INCLUDE [prod_short](../includes/prod_short.md)] till Shopify.  

Om du vill använda Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)] kan du först göra detta. Den här artikeln används som vägledning för att slutföra integrationen av Shopify-butiken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Förutsättningar för Shopify

Du måste ha följande:

- Ett Shopify-konto
- En onlinebutik med Shopify

Om du vill skapa ett nytt Shopify-konto eller registrera dig för en kostnadsfri 14-dagars utvärderingsversion går du till [Shopify](https://www.shopify.com/). Mer information om hur du skapar och anpassar onlinebutiken finns i [Shopifys hjälpcenter](https://help.shopify.com/).
  
Andra försäljningskanaler stöds, såsom Shopify POS.

### <a name="recommended-settings"></a>Rekommenderade inställningar

- Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för [**kassan**](https://www.shopify.com/admin/settings/checkout) i **administrationsdelen för Shopify**.

Mer information om Shopify-Inställningar för demo- och utvärderingsversioner finns i [Test- och utbildningsscenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Förutsättningar för Business Central

- Kontrollera att **[Shopify anslutning](https://go.microsoft.com/fwlink/?linkid=2196238)**-appen för har installerats.

Appen är förinstallerad för alla nya registreringar och utvärderingsversioner. Läs mer om att installera appar från marknadsplatsen på [Installera och avinstallera tillägg](../ui-extensions-install-uninstall.md#install). Följ instruktionerna nedan om du inte har [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installera **Dynamics 365 Business Central** appen till din Shopify onlinebutik

För befintlig [!INCLUDE[prod_short](../includes/prod_short.md)] är det här steget valfritt och kan hoppas över.

1. Leta upp [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) appen på [Shopify AppStore](https://apps.shopify.com/)
2. Välj knappen **Lägg till app**. Logga in på ditt Shopify konto om du uppmanas. Välj önskad onlinebutik om du har fler än en.
3. När du har granskat sekretess och behörighet väljer du knappen **Installera app**.
  Du kan söka efter och öppna den installerade **Dynamics 365 Business Central** appen i avsnittet **Appar** på panelen **Shopify admin**.
4. Välj **Registrera dig nu** om du vill starta [!INCLUDE[prod_short](../includes/prod_short.md)] utvärderingsversion eller **Logga in** om du redan har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du kommer att omdirigeras till din [!INCLUDE[prod_short](../includes/prod_short.md)] din [Business Central](https://businesscentral.dynamics.com).
5. Nästa steg ska utföras i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Ansluta Business Central till onlinebutiken på Shopify

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj åtgärden **Ny**.  
3. Ange den efterfrågade koden i fältet **Kod**.  
4. I fältet **Shopify URL** anger du URL:en till din onlinebutik, som måste vara ansluten. Använd följande format: `https://{shop}.myshopify.com/`.
5. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.
6. Om du uppmanas till det, loggar du in på ditt Shopify-konto, granskar sekretess och behörigheter och trycker sedan på knappen **Installera app**.

Upprepa steg 2–6 för alla onlinebutiker som du vill ansluta.

### <a name="next-steps"></a>Nästa steg

Nu är din onlinebutik ansluten till [!INCLUDE[prod_short](../includes/prod_short.md)]. I nästa steg ska du definiera vad som ska synkroniseras och hur.

- [Synkronisera artiklar](synchronize-items.md)
- [Synkronisera kunder](synchronize-customers.md)
- [Synkronisera order](synchronize-orders.md)

## <a name="see-also"></a>Se även

[Test- och utbildningsscenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).


---
title: Komma igång med kopplingen för Shopify
description: Första stegen när du konfigurerar anslutningen mellan Business Central och Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768202"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom igång med Shopify-kopplingen

[!INCLUDE [prod_short](../includes/prod_short.md)] ger dig flexibiliteten att ansluta din Shopify-butik (eller butiker) för att maximera företagets produktivitet. Du kan hantera och visa insikter från företaget och din Shopify-butik online som en enhet med hjälp av Shopify-kopplingen. Du måste följa stegen för att använda Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)]. Den här sidan används som vägledning för att slutföra integrationen av Shopify-butiken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Förutsättningar för Shopify

Du måste ha följande:

- Ett Shopify-konto
- En onlinebutik med Shopify

Om du vill skapa ett nytt Shopify-konto eller registrera dig för en kostnadsfri 14-dagars utvärderingsversion går du till [Shopify](https://www.shopify.com/). Mer information om hur du skapar och anpassar onlinebutiken finns i [Shopifys hjälpcenter](https://help.shopify.com/).
  
- Andra försäljningskanaler stöds, såsom Shopify POS.

### <a name="recommended-settings"></a>Rekommenderade inställningar

- Inaktivera **Arkivera order automatiskt** i avsnittet **Orderbehandling** av inställningarna för [**kassan**](https://www.shopify.com/admin/settings/checkout) i **administrationsdelen för Shopify**.

Mer information om Shopify-Inställningar för demo- och utvärderingsversioner finns i [Test- och utbildningsscenarier](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Förutsättningar för Business Central

- Kontrollera att **Anslut till Shopify för tillägget [!INCLUDE[prod_short](../includes/prod_short.md)]** har installerats.

Tillägget är förinstallerat för alla nya registreringar och utvärderingsversioner. Om du behöver installera tillägg från marknadsplatsen kan du gå till [Installera och avinstallera tillägg](../ui-extensions-install-uninstall.md#install). Följ instruktionerna nedan om du inte har [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Ansluta Business Central till onlinebutiken på Shopify

1. Gå till ikonen med ![glödlampan som öppnar funktionen Berätta](../media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj åtgärden **Ny**.  
3. Ange den efterfrågade koden i fältet **Kod**.  
4. I fältet **Shopify URL** anger du URL:en till din onlinebutik, som måste vara ansluten.
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


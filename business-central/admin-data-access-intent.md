---
title: Hantera åtkomstmetoden för databas i Business Central | Microsoft-dokument
description: Ändra åtkomstmetoden för databaser för rapporter, API-sidor och frågor.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/30/2020
ms.author: jswymer
ms.openlocfilehash: b46786b60d7c5799b056c49188785bd595db57ff
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333914"
---
# <a name="managing-database-access-intent"></a>Hantera åtkomstmetod för databas 

Som Super-användare eller administratör kan du ändra åtkomstmetoden för databaser med avseende på rapporter, sidor av typen API och frågor för att förbättra tjänstens prestanda.

## <a name="overview"></a>Översikt

[!INCLUDE[d365fin](includes/d365fin_md.md)] kan konfigureras för att använda skrivskyddade kopior av den primära (skrivskyddade) databasen. Användning av en databaskopia minskar belastningen på den primära databasen. I vissa fall förbättras också prestandan när du visar data på klienten. Kopior är fördelaktiga för objekt, t.ex. rapporter, frågor och API-sidor, som används för att enbart visa (men inte ändra) data.

När objekt körs bestämmer databasens åtkomstmetod huruvida en skrivskyddad kopia ska användas, om någon finns tillgänglig, eller om den primära databasen ska användas. Rapporter, API-sidor och frågor utvecklas med en fördefinierad metod för databasåtkomst (se [egenskapen DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Sidan **Metodlista för databasåtkomst** kan du åsidosätta den fördefinierade metoden för databasåtkomst för objekt när de körs.

Inom databasterminologin kallas denna funktion vanligen för *läsningsskalning*. Mer information om avläsning och metoder för dataåtkomst i [!INCLUDE[prodshort](includes/prodshort.md)] finns i [Använda Läsningsskalning för bättre prestanda](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prodshort](includes/prodshort.md)]-hjälp för utvecklare och administration.

## <a name="to-change-the-database-access-intent"></a>Så här ändrar du åtkomstmetod för databaser

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Metodlista för databasåtkomst** och välj sedan relaterad länk.

    På sidan visas alla rapporter, sidor och frågor. I kolumnen **Åtkomstmetod** finns ett av följande värden:

    |**Inställning**|**Beskrivning**|  
    |------------|-------------|  
    |**Standard**|Anger att objektet använder den fördefinierade metoden för databasåtkomst.|
    |**Ej skrivskydd**|Anger att objektet ska använda den primära databasen så att användaren kan ändra data.|
    |**Skrivskyddad**|Anger att objektet ska använda databaskopian, vilket innebär att användaren endast kan visa men inte ändra data.|

2. Välj åtgärden **Redigera lista**.

3. På sidan **Redigera - Metodlista för databasåtkomst** kan du ändra fältet **Åtkomstmetod** för objekten.

    > [!NOTE]
    > Om ett objekt som är redigerbart, exepelvis kundkortet, är **Skrivskyddat**, kommer den primära databasen fortfarande att användas oavsett vilken behörighet som används, vilket gör att användarna kan göra ändringar som vanligt.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se även
[Affärsfunktion](across-business-functionality.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Komma igång](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

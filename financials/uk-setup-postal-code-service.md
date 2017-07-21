---
title: "Sår här: Ställ in tillägget GetAddress.io för postnummer i Storbritannien | Microsoft Docs"
description: "Beskriver de allmänna funktionerna som du använder för att arbeta med data i Financials, ange värden, sortera data och ändra vyer."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a>Så här: Ställ in tillägget GetAddress.io för postnummer i Storbritannien
Det här tillägget gör det enkelt att ange adresser i Storbritannien för enheter som kunder, kontakter, anställda, leverantörer, bankkonton och så vidare. 

Tillägget GetAddress.io för postnummer i Storbritannien använder getAddress API för att hitta adresser i postnummer i Storbritannien. Om du vill använda tillägget, måste du ha en plan och en API-nyckel för för getAddress API. Det är enkelt och vi hjälper dig att göra detta när du ställer in tillägget GetAddress.io för postnummer i Storbritannien. Planer baseras på användning eller vilka som ibland kallas samtal. Ett samtal är i detta fall när [!INCLUDE[d365fin](includes/d365fin_md.md)] visar en lista med adresser i ett postnummer. Välj det schema som passar dig bäst beroende på hur ofta du vill lägga till adresser. Om du väljer **få API-nyckel** på sidan ska du använda planen **gratis** som låter dig lägga till 20 adresser per dag och är endast giltig i 30 dagar. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Ställ in tillägget GetAddress.io för postnummer i Storbritannien 
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Anslutningar till tjänst** och välj sedan relaterad länk.  
2. I fönstret **Anslutningar till tjänst** väljer du **Storbritannien postnummertjänst**.
3. På sidan **Postnummerproviderkonfiguration** väljer du **inaktiverad**.
4. I fönstret **Val av postnummertjänst** väljer du **GetAddress.io**.
5. I fönstret **GetAddress.io konfiguration** väljer du **hämta API-nyckeln** för att öppna sidan **planer** på webbplatsen för getAddress API.  

    > [!NOTE]  
>   Du kanske måste tillåta popup-fönster i webbläsaren.
6. Köp en plan eller välj **få API-nyckeln**, och ange din e-postadress.
7. Öppna e-postmeddelandet från getAddress.io och kopiera API-nyckeln. Nyckeln är under rubriken **din API-nyckel**.
8. I fönstret **GetAddress.io konfig** klistrar du in API-nyckel i fältet **API-nyckel** och väljer sedan **OK**.
9. På sidan **Tjänstanslutningar** kontrollerar du att fältet **adressleverantör** visar **GetAddress.io**. Om det gör detta är tjänsten aktiverad.

## <a name="see-also"></a>Se även
[GetAddress.io brittiska postnr](ui-extensions-getaddressio.md)
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

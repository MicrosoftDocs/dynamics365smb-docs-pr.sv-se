---
author: edupont04
ms.topic: include
ms.date: 04/01/2022
ms.author: edupont
ms.openlocfilehash: 646bc51e0b7b6aa6dbce22dcbcdcd9d8688f433d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514341"
---
[!INCLUDE[prod_short](prod_short.md)]-användarna kan ibland stödja mer än en avdelning eller underorganisation inom en affärsenhet. Ett företag kan till exempel ha försäljningskontor i olika städer och länder och har därför skapat en separat affärsenhet för respektive kontor. De kontor som tillhör samma land upprättas som separata *företag* i en delad *miljö*. Andra kontor skapas som företag i olika miljöer eftersom de är geografiskt baserade i andra länder.  

* Vad är ett företag?  

  Betrakta ett *företag* som en behållare som innehåller information om en juridisk person. Med hjälp av exemplet ovan har företaget ett försäljningskontor i Stockholm och ett annat i Göteborg, så att det skapas ett företag i [!INCLUDE[prod_short](prod_short.md)] för varje kontor så att det kan hantera operationer för varje kontor separat.  
* Vad är en miljö?  

  Företag i [!INCLUDE[prod_short](prod_short.md)] online finns i vad som kallas *miljöer*. Det finns två typer av miljöer, **produktion** och **begränsat läge**. I korthet innehåller produktionsmiljöer aktiverade affärsdata och miljöer i begränsat läge används som ett säkert ställe för att testa saker som nya affärsprocesser eller funktioner. Mer information finns i [Miljötyper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (finns endast på engelska). Om du har tillgång till ett företag har du tillgång till den miljö det finns i. Om du har tillgång till fler än ett företag och de företagen finns i olika miljöer, [!INCLUDE[prod_short](prod_short.md)] måste du ange vilken miljö du vill arbeta med. Miljöer är specifika för ett visst land, så om organisationen arbetar i flera länder måste du ha olika miljöer för varje land. Mer information finns i [Miljöer och företag](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (finns endast på engelska).  

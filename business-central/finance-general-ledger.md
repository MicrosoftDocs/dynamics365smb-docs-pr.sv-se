---
title: Så här fungerar i redovisningen och kontoplanen
description: Beskriver redovisningen, kontoplanen och kontokategorierna. På sidan Redovisningsinställningar anger du hur du vill hantera vissa bokföringsfrågor i företaget som t. ex.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: 183aa0cee83c826d51f582faead9d3a53b02ce71
ms.sourcegitcommit: 4223484b0eeceb0258dae5abfd04e1a9a4a0990d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7889800"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Förstå redovisningen och kontoplanen

Redovisningen lagrar dina ekonomiska data, och kontoplanen visar de konton som alla redovisningstransaktioner bokförs på. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Redovisningsinställning och bokföringingsinställning

Inställningarna för redovisningen är kärnan i ekonomiska processer eftersom den definierar hur du bokför data.  

På sidan **Redovisningsinställningar** anger du hur du vill hantera vissa bokföringsfrågor i företaget som t. ex.:  

* Öresutjämning  
* Adresslayout  
* Ekonomisk rapportering  

> [!TIP]
> Sidan **redovisningsinställning** innehåller allmänna fält och fält som är specifika för ditt land eller din region. Om du är osäker på innebörden av ett fält föreslår vi att du arbetar med revisorn för att avgöra om det är relevant för organisationen.  

På liknande sätt p sidan **Bokföringsinställningar** anger du hur du vill ange kombinationer av allmän bokföringsmallar och allmäna produktbokföringsmallar. Bokföringsmallar mappar enheter som t. ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. Du fyller i en rad för varje kombination av rörelse- och produktbokföringsmall. Du kan emellertid också öppna varje enskild rad i dess kort för bokföringsinställning. Mer information finns i [Inställning av bokföringsmall](finance-posting-groups.md).  

> [!TIP]
> Om fälten du söker inte visas på sidan **Bokföringsinställningar** kan du använda den vågräta rullningslisten längst ned på sidan för att rulla åt höger.  

## <a name="the-chart-of-accounts"></a>Kontoplanen

Kontoplanen visar alla redovisningskonton. Från kontoplanen, kan du göra sådant som:  

* Visa rapporter som visar transaktioner och saldon.  
* Avslut av resultatkonton.  
* Öppna redovisningkontokortet om du vill lägga till eller ändra inställningar.  
* Visa en lista med bokföringsmallar som bokför på det konto.
* Visa separatea debet- och kreditsaldon för ett enskilt konto  

Du kan lägga till, ändra eller ta bort konton i redovisningen. Men för att undvika avvikelser bör du inte ta bort ett redovisningskonto om dess data används i kontoplanen.  

## <a name="account-categories"></a>Kontokategorier

Med kontokategorier kan du mappa redovisningskonton till kategorier som en anpassning av strukturen på din redovisning.  

Sidan **Redovisningskontokategorier** visar de kategorierna och delkategorierna och redovisningskontona som har tilldelats dem. Du kan skapa nya delkategorier och tilldela de kategorierna till befintliga konton.  

Du skapar en kategorigrupp, genom att dra in andra delkategorier under en rad på sidan **redovisningskontokategorier**. Detta gör det lätt för dig att få en översikt, eftersom varje journal visar ett totalt saldo. Du kan till exempel skapa delkategorier för andra typer av anläggningstillgångar och sedan skapa kategorigrupper för t. ex. anläggningstillgångar jämfört med omsättningstillgångar.  

För varje delkategori kan du ange om konton för den kategorin måste tas med i vissa typer av ekonomiska rapporter. Du kan använda kontokategorier för att ändra layout på din redovisning.  

### <a name="example"></a>Exempel

Till exempel har det standardinställda saldo vid kontoavstämning en enkelt transaktion för *kontanter* under *tillgångar*. Om du vill att saldot överväger handkassa och check, kan du göra följa steg:  

1. Lägga till två nya underkategorierna:

    * Ett för handkassa  
    * En för ditt checkkonto  
2. Ange ytterligare rapportdefinitionen **kassakonton** för dessa underkategorier.  
3. Dra in dem under underkategorin **kontant**.  

Nästa gång du har genererat kontouppställningar kommer saldot visa ett totalt saldo för kontanter och två rader med saldon för handkassa och checkräkningskontot.  

## <a name="getting-a-quick-overview"></a>Få en snabb översikt
På sidan kontoplan visas de konton i en hierarkisk lista som ger snabb åtkomst till nyckelinformation för varje konto. Listan är dock statisk och om du har många konton måste du kanske göra en del av en bläddring för att kunna visa information för olika konton. Om du bara vill ha en snabb överblick över grunderna, till exempel nettoförändringar och saldon, är sidan **Kontoplansöversikt** ett användbart alternativ. Kolumnlayouten på sidan är nu densamma som på sidan kontoplan (det finns bara färre), så du behöver inte omorientera dig själv, och du kan expandera eller dölja de hierarkiska nivåerna för att kondensera vyn. För att det ska bli lättare att växla mellan sidorna är sidan **Kontoplansöversikt** tillgänglig på sidan kontoplan.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Åtkomst för att skapa och redigera konton och kontokategorier

I en liten organisation, t.ex. CRONUS demonstrationsföretaget, kan de flesta användare redigera kontoplanen, utom användare med en licens från en gruppmedlem. I större organisationer begränsas till gång till redigering av kontoplanen av roller och behörigheter. Om du är administratör eller har rollen *företagschef* eller *revisor* kan du kontrollera att alla användare har till gång till de aktuella tabellerna med behörighet. Mer information finns i avsnittet [Så här får du en översikt en användares behörigheter](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md)  
[Affärsstöd](bi.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
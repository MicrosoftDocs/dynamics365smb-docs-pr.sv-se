---
title: Så här fungerar i redovisningen och kontoplanen
description: Beskriver redovisningen, kontoplanen och kontokategorierna. På sidan Redovisningsinställningar anger du hur du vill hantera vissa bokföringsfrågor i företaget som t. ex.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: bb94f725c57f538f9d8704ba66e3d66e120d41d2
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079148"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Förstå redovisningen och kontoplanen

Redovisningen lagrar dina ekonomiska data, och kontoplanen visar de konton som alla redovisningstransaktioner bokförs på. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Redovisningsinställning och bokföringsinställning

Inställningarna för redovisningen är kärnan i ekonomiska processer eftersom den definierar hur du bokför data. Två sidor spelar en viktig roll när det är att konfigurera ekonomiprocesserna:  

* Sidan **Redovisningsinställningar**

    På sidan **Redovisningsinställningar** anger du hur du vill hantera vissa bokföringsfrågor i företaget som t. ex.:  

    * Öresutjämning  
    * Adresslayout  
    * Ekonomisk rapportering  

    > [!TIP]
    > Sidan **redovisningsinställning** innehåller allmänna fält och fält som är specifika för ditt land eller din region. Om du är osäker på innebörden av ett fält föreslår vi att du arbetar med revisorn för att avgöra om det är relevant för organisationen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Öppna sidan [här](https://businesscentral.dynamics.com/?page=118)
* Sidan **Bokföringsinställningar**

    På liknande sätt p sidan **Bokföringsinställningar** anger du hur du vill ange kombinationer av allmän bokföringsmallar och allmäna produktbokföringsmallar. Bokföringsmallar mappar enheter som t. ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. Du fyller i en rad för varje kombination av rörelse- och produktbokföringsmall. Du kan emellertid också öppna varje enskild rad i dess kort för bokföringsinställning. Mer information finns i [Inställning av bokföringsmall](finance-posting-groups.md).  

    > [!TIP]
    > Om fälten du söker inte visas på sidan **Bokföringsinställningar** kan du använda den vågräta rullningslisten längst ned på sidan för att rulla åt höger.  

    Öppna sidan [här](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Kontoplanen

Kontoplanen visar alla redovisningskonton. Från kontoplanen, kan du göra sådant som:  

* Visa rapporter som visar transaktioner och saldon.  
* Avslut av resultatkonton.  
* Öppna redovisningkontokortet om du vill lägga till eller ändra inställningar.  
* Visa en lista med bokföringsmallar som bokför på det konto.
* Visa separatea debet- och kreditsaldon för ett enskilt konto  

Du kan lägga till, ändra eller ta bort konton i redovisningen. I syfte att undvika avvikelser kan du emelelrtid inte ta bort ett redovisningskonto om dess data används i kontoplanen. Från och med 2022 års utgivningscykel 2 kan du också spärra oavsiktlig borttagning av konton under känsliga perioder. Mer information finns i [Ta bort konton](finance-setup-chart-accounts.md#delete-accounts).  

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
2. Ange den andra rapportdefinitionen **Kassakonton** för dessa underkategorier.  
3. Dra in dem under underkategorin **kontant**.  

Nästa gång du har genererat kontouppställningar kommer saldot visa ett totalt saldo för kontanter och två rader med saldon för handkassa och checkräkningskontot.  

## <a name="get-a-quick-overview"></a>Få en snabböversikt

På sidan **Kontoplan** visas i en hierarkisk lista de konton som ger snabb åtkomst till nyckelinformation för respektive konto. Listan är dock statisk, och om du har många konton måste du kanske bläddra en del för att kunna visa information för olika konton. Om du bara vill ha en snabb överblick över grunderna, till exempel nettoförändringar och saldon, är sidan **Kontoplansöversikt** ett användbart alternativ. Kolumnlayouten på sidan är nu densamma som på sidan **Kontoplan** (det finns bara färre), så du behöver inte omorientera dig själv, och du kan expandera eller dölja de hierarkiska nivåerna för att kondensera vyn. För att det ska bli lättare att växla mellan sidorna är sidan **Kontoplansöversikt** tillgänglig på sidan **Kontoplanen**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Åtkomst för att skapa och redigera konton och kontokategorier

I en liten organisation, t.ex. CRONUS demonstrationsföretaget, kan de flesta användare redigera kontoplanen, utom användare med en licens från en gruppmedlem. I större organisationer begränsas till gång till redigering av kontoplanen av roller och behörigheter. Om du är administratör eller har rollen *företagschef* eller *revisor* kan du kontrollera att alla användare har till gång till de aktuella tabellerna med behörighet. Mer information finns i avsnittet [Så här får du en översikt en användares behörigheter](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md)  
[Affärsstöd](bi.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]

---
title: Förstå redovisningen och kontoplanen
description: 'Beskriver redovisningen, kontoplanen och kontokategorierna. På sidan Redovisningsinställningar anger du hur du vill hantera vissa bokföringsfrågor i företaget som t. ex.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="understand-the-general-ledger-and-chart-of-accounts"></a>Förstå redovisningen och kontoplanen

Redovisningen lagrar dina ekonomiska data, och kontoplanen visar de konton som du bokför redovisningstransaktioner på. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar en standardkontoplan som är klar att stödja din verksamhet.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Redovisningsinställning och bokföringsinställning

Inställningarna för redovisningen är kärnan i ekonomiska processer eftersom den definierar hur du bokför data. Två sidor i synnerhet spelar en viktig roll när det är att konfigurera ekonomiprocesserna:  

* **Redovisningsinställning**
* **Bokföringsinställningar**

### <a name="the-general-ledger-setup-page"></a>Sidan **Redovisningsinställningar**

Använd sidan **Redovisningsinställningar** för att ange hur du vill hantera vissa bokföringsfrågor i företaget som t. ex.:  

* Öresutjämning  
* Adresslayout  
* Ekonomisk rapportering

> [!TIP]
> Sidan **redovisningsinställning** innehåller allmänna fält och fält som är specifika för ditt land eller din region. Om du är osäker på innebörden av ett fält föreslår vi att du arbetar med revisorn för att avgöra om det är relevant för organisationen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

För att öppna sidan nu, använd följande länk [Redovisningsinställningar](https://businesscentral.dynamics.com/?page=118).

### <a name="the-general-posting-setup-page"></a>Sidan **Bokföringsinställningar**

Du kan använda sidan **Bokföringsinställningar** för att ställa in kombinationer av rörelse- och produktbokföringsmallar. Bokföringsmallar mappar enheter som t. ex. kunder, leverantörer, artiklar, resurser och försäljning och inköpsdokument till redovisningskonton. Du fyller i en rad för varje kombination av rörelse- och produktbokföringsmall. Du kan emellertid också öppna varje enskild rad i dess kort för bokföringsinställning. Läs mer i [Inställning av bokföringsmall](finance-posting-groups.md).  

> [!TIP]
> Om fälten du söker inte visas på sidan **Bokföringsinställningar** kan du använda den vågräta rullningslisten längst ned på sidan för att rulla åt höger.  

För att öppna sidan nu, använd följande länk [Bokföringsinställningar](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Kontoplanen

Sidan **Kontoplan** visar alla redovisningskonton. Från kontoplanen, kan du göra sådant som:  

* Visa rapporter som visar transaktioner och saldon.  
* Avslut av resultatkonton.  
* Öppna redovisningkontokortet om du vill lägga till eller ändra inställningar.  
* Visa en lista med bokföringsmallar för det kontot.
* Visa separatea debet- och kreditsaldon för ett enskilt konto.

För mer information, gå till [Förstå kontoplanen](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Kontokategorier

Med kontokategorier kan du mappa redovisningskonton till kategorier som en anpassning av strukturen på din redovisning.  

På sidan **Redovisningskontokategorier** visas dina kategorier och delkategorier och redovisningskontona som har tilldelats dem. Du kan skapa nya delkategorier och tilldela de kategorierna till befintliga konton.  

Du kan skapa en kategorigrupp genom att dra in andra delkategorier under en rad på sidan **Redovisningskontokategorier**. Kategorigrupper gör det lätt för dig att få en översikt, eftersom varje grupp visar ett totalt saldo. Du kan till exempel skapa delkategorier för andra typer av tillgångar och sedan skapa kategorigrupper för t.ex. anläggningstillgångar jämfört med omsättningstillgångar.  

Du kan definiera om specifika typer av rapporter måste innehålla kontona i varje delkategori. Du kan använda kontokategorier för att ändra layout på din redovisning.  

### <a name="example"></a>Exempel

Till exempel har det standardinställda saldo vid kontoavstämning en enkelt transaktion för *kontanter* under *tillgångar*. Om du vill att saldot överväger handkassa och check, kan du göra följa steg:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Redovisningskategorier** och väljer sedan relaterad länk.
   1. Alternativt [öppnar du sidan här](https://businesscentral.dynamics.com/?page=790).
2. Välj åtgärden **Redigera lista**.
3. Lägg till två nya delkategorier: En för handkassa och en för ditt checkkonto:
   1. Väj kategorin **Aktuella tillgångar**.
   2. Välj åtgärden **Ny**.
   3. Ange delkategorins namn i fältet **Beskrivning**.
   4. I fältet **Redovisningskonton i Kategori** väljer du lämpligt redovisningskonto.
   5. I fältet **Ytterligare rapportdefinition** väljer du alternativet **Kassakonton**.
4. Dra in dem under underkategorin **kontant**.
   1. Välj den delkategori som skapades i steg 3.
   2. Välj åtgärden **Indrag**.
   3. Välj åtgärden **Flytta ned**.
   4. Välj åtgärden **Indrag** för att dra in under delkategorin **Kassa**.

När du väljer åtgärden **Skapa ekonomiska rapporter**, eller nästa gång rapporten genereras, visas följande rader i saldot:

* Totalt saldo för kontanter.
* Rader med saldon för handkassa och checkkonto.  

> [!NOTE]
> Om du skapar ett redovisningskonto utan att tilldela en kontokategori, tilldelar du kontot till en bokföringsmall [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt en kontokategori från redovisningskonto ovanför kontot i kontoplanen. Om du vill inkludera det nya kontot i dina ekonomiska rapporter måste du välja åtgärden **Skapa ekonomiska rapporter** på sidan **Kategorier på redovisningskonton**. Du kan också öppna sidan Redovisningskontokort, ange kontokategorin och sedan generera om den ekonomiska rapporten.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Åtkomst för att skapa och redigera redovisningskonton och kontokategorier

I en liten organisation, t.ex. demonstrationsföretaget CRONUS, kan de flesta användare redigera finansiella entiteter, t.ex. redovisningskonto, kontokategorier och kontoplaner förutom de användare med en licens som GRUPPMEDLEM. Större organisationer använder dock vanligtvis roller och behörigheter för att begränsa åtkomsten till att redigera dessa entiteter. Om du är administratör eller har rollen *Företagschef* eller *Revisor* kan du kontrollera användarbehörigheter för att ge rätt personer tillgång till de relevanta tabellerna. Gå till [Så här får du en översikt en användares behörigheter](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions) för mer information.  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Använd dimensioner för att förenkla kontoplanen

Dimensioner är värden som kategoriserar transaktioner så att du kan spåra och analysera dem i dokument, exempelvis försäljningsorder. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån. Så i stället för att skapa separata redovisningskonton för varje avdelning och projekt kan du använda dimensioner som grund för analys och slippa behöva skapa en komplicerad kontoplan.

För att lära dig mer om dimensioner, gå till [Konfigurera standarddimensioner för kunder, leverantörer och andra konton](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Se även

[Förstå kontoplanen](finance-chart-of-accounts.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Tilldela användare och grupper behörigheter](ui-define-granular-permissions.md)  
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

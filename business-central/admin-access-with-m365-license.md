---
title: Business Central-åtkomst med Microsoft 365-licenser
description: 'Lär dig hur användare kan få tillgång till Business Central-data, till exempel i Microsoft Teams chattar och kanaler endast med en Microsoft 365-licens, men ingen Business Central-licens.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="business-central-access-with-microsoft-365-licenses" />Business Central-åtkomst med Microsoft 365-licenser

[!INCLUDE[prod_short](includes/prod_short.md)] användare tilldelas en Dynamics 365 Business Central-licens som gör att de kan visa, ändra och arbeta med affärs data från alla användargränssnitt. För alla andra anställda i organisationen som bara behöver kunna visa data ibland kan Business Central komma åt via Microsoft 365.  

När en organisation har både en Dynamics 365 Business Central och Microsoft 365-prenumeration kan administratörer konfigurera miljöer för att aktivera åtkomst med Microsoft 365-licenser och välja exakt vilka tabeller och andra objekt som den här användarkategorin ska ha åtkomst till. När de är konfigurerade kan anställda som har en Microsoft 365-licens men ingen [!INCLUDE [prod_short](includes/prod_short.md)]-licens kan visa [!INCLUDE [prod_short](includes/prod_short.md)]-poster som delas med dem i Microsoft Teams chattar och kanaler.

## <a name="why-enable-access-with-microsoft-365-licenses" />Varför aktivera åtkomst med Microsoft 365-licenser

- Lås upp huvuddata som varje anställd i organisationen ska ha åtkomst till.

- Bemyndiga avdelningar som inte körs på [!INCLUDE [prod_short](includes/prod_short.md)] till självbetjäning, genom att använda nyckeldata som behövs för att utföra sina uppgifter, vilket eliminerar behovet av att kontinuerligt begära data från andra.

- Öka samarbetetseffektivitet så att uppgifter och projekt som sträcker sig över flera avdelningar i tid, genom att ta bort friktionen som vanligen beror på nekade åtkomst fel på grund av licensiering.

- Öka teamets prestanda så att andra kan göra data drivna beslut som ingår i gruppen, även om de inte fungerar i [!INCLUDE [prod_short](includes/prod_short.md)].

- Uppnå licensbudgetmål genom att tilldela licenser som successivt matchar medarbetarnas behov Microsoft 365-licenser för skrivskyddad åtkomst, Dynamics 365 Business Central teammedlemslicenser för begränsad skrivåtkomst och Dynamics 365 Business Central Essentials eller Premium för fullständig skrivåtkomst.

- Förbättra datasäkerheten genom att minska behovet av att klistra in datautdrag från företagsdata utanför datastyrningsgränser.

## <a name="use-rights" />Använda rättigheter

När en person har åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)] med en Microsoft 365-licens, ger denna licens användaren rätt att läsa (men inte skriva) [!INCLUDE [prod_short](includes/prod_short.md)]-data genom ett förenklat användargränssnitt i Microsoft Teams. I det här avsnittet beskrivs dessa användningsrättigheter och begränsningar som hjälper dig att planera hur du ska konfigurera och utnyttja den mesta möjliga av funktionen. Mer information om den här licenstypen jämfört med andra [!INCLUDE [prod_short](includes/prod_short.md)]-licenser finns i[ Dynamics 365 licensguiden](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access" />Klientåtkomst

Användare har rätt att komma åt [!INCLUDE [prod_short](includes/prod_short.md)]-data i Microsoft Teams. I följande tabell sammanfattas vilka av de olika metoderna för att komma åt [!INCLUDE [prod_short](includes/prod_short.md)]-tjänsten med denna licens.

|Klient som ansluter till Business Central-tjänst |Åtkomst|
|-|-|
|Business Central-app för Microsoft Teams|![Ja](media/check.png)|
|Business Central-webbklient |![Nr](media/x-icon.png ) |
|Business Central-mobilappar|![Nr](media/x-icon.png )|
|Business Central API:er|![Nr](media/x-icon.png )|
|Business Central-integration med andra Office-program|![Nr](media/x-icon.png )|
|Business Central inbäddat i andra program |![Nr](media/x-icon.png )|

### <a name="data-access" />Dataåtkomst

Användare har rätt att läsa tabell data men kan inte ändra, skapa eller ta bort poster. [!INCLUDE [prod_short](includes/prod_short.md)]-plattformen förhindrar automatiskt skrivning till datatabeller.  

### <a name="use-of-objects" />Användning av föremål

Åtkomst med Microsoft 365-licenser begränsar inte vilka Business Central objekt eller objekt intervall du kan komma åt. Användarna har rätt att komma åt Microsoft basprogrammet och eventuella tillägg som anpassningar och program för tilläggsprogram.

## <a name="simplified-user-interface" />Förenklat användargränssnitt

Användarna har rätt till en reducerad uppsättning funktioner som ingår i [!INCLUDE [prod_short](includes/prod_short.md)] i Microsoft Teams. I tabellerna nedan anges de intressanta funktionerna. Det här är inte en uttömmande lista och kan komma att ändras.

Funktioner för [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams:

|Funktion  |Disponibelt|
|-|-|
|Visa [!INCLUDE [prod_short](includes/prod_short.md)] kort|![Ja](media/check.png)|
|Visa kortinformation |![Ja](media/check.png) |
|PIN-kortsdetaljer som en flik |![Ja](media/check.png)|
|Visa [!INCLUDE [prod_short](includes/prod_short.md)] flikar|![Ja](media/check.png)|
|Lägg till en [!INCLUDE [prod_short](includes/prod_short.md)] flik|![Nr_](media/x-icon.png )|
|Sök efter företagskontakter |![Nej](media/x-icon.png )|
|Klistra in och dela en länk för förhandsgranskning som ett kort|![Nej](media/x-icon.png )|

Funktioner för den [!INCLUDE [prod_short](includes/prod_short.md)] klient som är inbäddad i Teams:

|Funktion |Disponibelt|Exempelfunktioner|
|-|-|-|
|Åtgärder för datamanipuleringssystem |![Nr](media/x-icon.png )|Redigera, skapa, ta bort|
|Grundläggande funktioner i listor|![Ja](media/check.png)|Sök, sortera, ändra layout|
|Avancerade funktioner i listor|![Nr](media/x-icon.png )|Filterruta, vyer|
|Detaljgranska ned i listan till kort |![Ja](media/check.png)||
|Åtkomstdata från relaterade tabeller|![Nr](media/x-icon.png )|Rutan Faktabox, specificera fält, granska, slå upp |
|Åtgärder|![Nr](media/x-icon.png )|Åtgärdsfält, åtgärdsmenyer, åtgärder för sidavisering|
|Systemomfattande genvägar|![Nr](media/x-icon.png )|Mina inställningar, rollutforskaren, berätta sökning  |
|Kopiera|![Ja](media/check.png)|Kopiera rader, kopiera fältvärde, kopiera länk till sida|
|Anpassning av användargränssnitt|![Nr](media/x-icon.png )|Anpassa| 
|Infogad anpassning|![Ja](media/check.png)|Ändra storlek på kolumn, visa/dölj, visa fler |
|Dela data |![Nr](media/x-icon.png )|Öppna eller redigera i Excel, dela till Teams|
|Hjälp för infogade användare|![Ja](media/check.png) |Knappbeskrivningar, länkar till dokumentation|
|Avancerad användarhjälp |![Nr](media/x-icon.png )|Undervisningstips för sida och fält, Hjälp-fönstret|

## <a name="minimum-requirements" />Minsta krav

I det här avsnittet beskrivs de minimikrav som måste uppfyllas för organisationen för att ge åtkomst till Microsoft 365-licenser och för att enskilda Microsoft Teams-användare ska få till gång till [!INCLUDE [prod_short](includes/prod_short.md)]-data utan en [!INCLUDE [prod_short](includes/prod_short.md)]-licens.

### <a name="requirements-to-enable-access" />Krav för att möjliggöra åtkomst

- [!INCLUDE [prod_short](includes/prod_short.md)] Online (SaaS).

- Miljöer måste vara av plattform version 21.1 eller senare.

### <a name="requirements-for-individual-users-to-access-data-in-teams" />Krav för att enskilda användare ska ha åtkomst till data i Teams

- Det går att komma åt data med hjälp av [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams. Användare måste ha [!INCLUDE [prod_short](includes/prod_short.md)]-app för Teams installerade och måste använda en av de Teams-klienter som stöds. En lista över vilka Teams-klienter som stöds av [!INCLUDE [prod_short](includes/prod_short.md)] finns i [Minimikrav för att använda Business Central](product-requirements.md#teams)

- Användare måste vara interna för organisationen, vilket innebär att en användaridentitet kommer från samma startklientorganisation där [!INCLUDE [prod_short](includes/prod_short.md)] distribueras och åtkomst är aktiverat. Externa identiteter stöds inte. [!INCLUDE [prod_short](includes/prod_short.md)] förhindrar automatiskt åtkomst till gäster.

- Användare måste tilldelas en Microsoft 365-licens från en av följande planer.
  
  |Plan som stöds|Produkt-ID |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Azure AD Identity) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  De flesta erbjudanden baserade på dessa planer stöds också. Om du t.ex. prenumererar på Microsoft 365 Business Premium (pris ej vinst personal), är det ett särskilt erbjudande för ideella organisationer som bygger på en Microsoft 365 Business Premium-plan, och stöds därför.

  > [!NOTE]
  > Hittar du inte din plan i listan? Microsoft söker kontinuerligt efter feedback på hur vi kan förbättra vår service och utöka vårt erbjudande så att fler kunder kan utnyttja denna möjlighet. Dela med dig av din idé om vilka planer vi ska stödja nästa på [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Användare måste tilldelas en Microsoft 365-licens där Microsoft Teams-appen har aktiverats i listan över appar för den aktuella licensen.

  |Program som stöds|Serviceplan-ID|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- Organisationen måste ha minst en användare som tilldelats en Dynamics 365 Business Central-licens.

## <a name="next-steps" />Nästa steg

- Få en förståelse för användaråtkomst flödet så att du kan planera ditt sätt att arbeta och konfigurera Business Central så att det passar företagets behov. Se [Användaråtkomstflöde](admin-access-with-m365-license-flow.md).
- Konfigurera miljön och användare för åtkomst med Microsoft 365-licenser. Se [Ställ in åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-setup.md).

## <a name="see-also" />Se även

[Business Central- och Microsoft Teams-integration](across-teams-overview.md)  

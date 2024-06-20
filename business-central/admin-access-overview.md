---
title: Hantera åtkomst till Business Central
description: Administratörer använder ett skiktat tillvägagångssätt för att kontrollera åtkomsten till Business Central och dess funktioner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Hantera åtkomst till Business Central

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I den här artikeln får administratörer och programutvecklare en översikt på hög nivå av hur åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)] och dess funktioner kan kontrolleras. Använd länkarna om du vill gå till andra artiklar som innehåller mer information om ämnena.

## Skiktad åtkomst

[!INCLUDE [prod_short](includes/prod_short.md)] använder ett skiktat tillvägagångssätt för appsäkerhet, enligt vad som beskrivs i följande diagram. Om du vill veta mer om de olika skikten går du till [Appsäkerhet i Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Skiktad appsäkerhet i Business Central.":::

## Licenser

Tilldela [!INCLUDE [prod_short](includes/prod_short.md)] användare till en **Dynamics 365 Business Central**-licens så att de kan visa, ändra och arbeta med affärsdata från alla användargränssnitt. Om du vill veta mer om licenser går du till [Licenser i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Människor som ibland behöver skrivskyddad åtkomst till information i [!INCLUDE [prod_short](includes/prod_short.md)] kan använda en **Microsoft 365**-licens. Om du vill veta mer om att ge begränsad åtkomst, gå till [Åtkomst till Business Central med Microsoft 365 licenser](admin-access-with-m365-license.md).

För omfattande information om olika typer av licenser och hur licensiering fungerar i [!INCLUDE[prod_short](includes/prod_short.md)], [hämta licensguiden för Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

## Administrationsuppgifter i Business Central

I följande tabell visas hur administratörer kan kontrollera åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)] och vilka funktioner som man använder. Vissa uppgifter hjälper dig också att upprätthålla åtkomstinställningarna.

|Uppgift| Läs mer |
|--|--|--|
|Varje användare måste ha ett användarkonto innan de kan logga in på [!INCLUDE [prod_short](includes/prod_short.md)]. Det enklaste sättet att skapa användare är att lägga till dem en i taget i [Microsoft 365 administrationscenter](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[ Lägg till användare och tilldela licenser på samma gång](/microsoft-365/admin/add-users/add-users)|
|Hantera åtkomst för alla användare på miljönivå. Skapa en Microsoft Entra-säkerhetsgrupp och tilldela den till miljön.<br><br> Du kan också använda säkerhetsgrupper om du vill hantera åtkomst för vissa användargrupper. | [Hantera åtkomst till miljöer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Styra åtkomsten till Business Central med hjälp av säkerhetsgrupper](ui-security-groups.md) |
|Skapa användare i [!INCLUDE [prod_short](includes/prod_short.md)] och ange vem som kan logga in. | [Skapa användare utifrån licenser](ui-how-users-permissions.md) |
|I kombination med användarlicenser definierar behörigheter de objekt som en användare kan komma åt inom varje databas eller miljö. Ange om personer kan läsa, ändra eller ange data i databasobjekt. |[Tilldela användare och grupper behörigheter](ui-define-granular-permissions.md)|
|Om en extern revisor hanterar dina böcker och ekonomisk rapportering, bjuder du in dem till din [!INCLUDE [prod_short](includes/prod_short.md)]. De kan samarbeta närmare med dig och dina skatteuppgifter.|[Revisorupplevelse i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Om du är en [!INCLUDE [prod_short](includes/prod_short.md)] återförsäljare av partner kan du skicka ett e-postmeddelande till en kund för att be om en återförsäljarrelation. Du kan ta med delegerade administrationsprivilegier för Microsoft Entra ID och Microsoft 365 i e-postmeddelandet.| [Tilldelad administratörsåtkomst till Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Ett Azure-tjänstetagg representerar en grupp IP-adresser som trafik för en tjänst kan komma från eller gå till. Använd tjänstetaggar för att konfigurera brandväggar så att trafiken endast tillåter trafik från vissa tjänster. Med taggen **Dynamics365BusinessCentral** kan du använda brandväggs- och nätverkssäkerhetsgruppregler för att begränsa trafik till och från [!INCLUDE [prod_short](includes/prod_short.md)].| [Azure-tjänstetaggar för säkerhet](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|När du använder Microsoft Entra-autentisering med [!INCLUDE [prod_short](includes/prod_short.md)] rekommenderar vi att du utnyttjar [Microsoft Entra ID-multifaktorsautentisering (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). MFA skyddar tillgången till program och data.|[Multifaktorsautentisering för Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## Business Central utvecklaruppgifter

Det finns också en utvecklingsberättelse för att hantera åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)]. Utvecklare och administratörer kan t.ex. skapa och ansluta program till [!INCLUDE [prod_short](includes/prod_short.md)] som gynnar verksamheten:  

* Förenkling av affärsprocesser
* Förbättra kundinteraktioner
* Fatta bättre beslut, snabbare

I följande tabell länkas till information om hur du ger appar och tillägg åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)] data.

| Uppgift | Läs mer |
|--|--|
|De två viktigaste begreppen för att definiera åtkomst till funktioner är berättiganden och behörigheter. Avrop ger omfattande åtkomst till objekt enligt licenser eller Microsoft Entra roller. Med behörigheter och behörighetsgrupper kan du finjustera åtkomsten till objekt. |[Berättiganden och behörighetsgrupper – översikt](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## Se även

[Säkerhet i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)

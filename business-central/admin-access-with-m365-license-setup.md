---
title: Ställ in åtkomst med Microsoft 365-licenser
description: En guide för hur administratörer kan konfigurera åtkomst till Business Central med Microsoft 365-licenser.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: 9061
---
# Konfigurera Business Central Access i Teams med Microsoft 365-licenser

Administratörer måste slutföra flera aktiviteter innan de får åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)] med deras Microsoft 365-licens. Stegen nedan representerar den minsta inställning som krävs för att komma igång. Om du vill veta mer om åtkomst med Microsoft 365 licenser går du till [Business Central åtkomst med Microsoft 365 licenser](admin-access-with-m365-license.md).

## Riktlinjer

När du konfigurerar åtkomst med  Microsoft 365-licenser måste du göra följande:

||Uppgift|Obligatoriskt|
|-|-|-|
|1|[Konfigurera vilka Business Central-data de Microsoft 365-licensierade användare har behörighet att visa](#configure-permissions)|![bock](media/check.png "kontroll")|
|2|[Aktivera åtkomst med Microsoft 365-licenser på Business Central-miljön](#enable-access-with-microsoft-365-licenses)|![bock](media/check.png "kontroll")|
|3|[Tilldela säkerhetsgrupp till miljön](#choose-who-gets-access-by-using-security-group)|
|4|[Distribuera appen Business Central för Teams till användare](#deploy-the-business-central-app-for-teams)|![bock](media/check.png "kontroll")|
|5|[Testa inställningen](#test-your-setup)||

> [!TIP]
> Med undantag för den sista aktiviteten kan du slutföra uppgifterna i valfri ordning. Du kan utföra uppgifter separat, enligt beskrivningen i de avsnitt som följer eller använda guiden för assisterad konfiguration **Microsoft 365-licensing** för att beskriva dig.
>
> Gör följande för att köra den assisterade installationen:
>
> 1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Assisterad konfiguration** och väljer sedan relaterad länk.
> 2. På sidan **Assisterad konfiguration** gå till **Gör mer med Business Central** och välj **Åtkomst till Microsoft 365-licenser**.
> 3. Följ instruktionerna:  

## Konfigurera behörigheter

[!INCLUDE [prod_short](includes/prod_short.md)] är säkert genom att designa och minimera risk genom att bevilja inga behörigheter till medföljande Microsoft 365-användare. Administratörer måste konfigurera objekt behörigheter som avgör vilka tabeller, sidor och rapporter som kan kommas åt i Teams med endast en Microsoft 365-licens. Dessa behörigheter är de start behörigheter som tilldelas när en användare loggar in för första gången med Microsoft 365-licens. 

Så här konfigurerar du startbehörigheter:

1. I [!INCLUDE [prod_short](includes/prod_short.md)], sök efter **licenskonfiguration**.
2. Välj Microsoft 365-licens.
3. Högst upp på **Microsoft 365**-licenssida, välj redigeringsikonen ![ikonen redigera](media/edit-pencil.png), aktivera **Anpassa behörigheter**. 
4. I avsnittet **Anpassade behörighetsuppsättningar** lägg till lämpliga behörighetsuppsättningar och välj om de är tillämpliga på ett enda företag eller alla företag inom miljön.

Med denna konfiguration kan användare med endast en Microsoft 365-licens läggs till i listan **användare** när de får åtkomst till [!INCLUDE [prod_short](includes/prod_short.md)] första gången. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).

> [!NOTE]
> När du synkroniserar användarlistan i [!INCLUDE [prod_short](includes/prod_short.md)] med användare i Microsoft 365, läggs endast användare med en [!INCLUDE [prod_short](includes/prod_short.md)]-licens till i [!INCLUDE [prod_short](includes/prod_short.md)] användarlista. Du kan tilldela en säkerhets grupp till miljön mer administrativ kontroll över behörigheter och profiler. När miljöer skyddas med hjälp av en säkerhetsgrupp och aktiverar åtkomst med Microsoft 365 licenser, kommer åtgärden **Uppdatera användare från Microsoft 365** på sidan **användare** även att innehålla användare som bara har en Microsoft 365 licens. Mer information om hur du skyddar miljöer finns i [ Hantera åtkomst med hjälp av Azure Active Directory grupper ](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjälpen för utvecklare och IT-proffs.

> [!TIP]
> Letar du efter ett snabbare sätt att komma igång när du försöker med den här funktionen eller utvärderingsföretag? Tilldela **D365 läs** behörighetsuppsättning, som ger behörighet till de flesta objekt.  

När du arbetar med flera miljöer måste licens konfigurationen tillämpas på varje miljö och kan vara olika i varje miljö.

Mer information om [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md) och [Att komponera behörighetsuppsättningar](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## Aktivera åtkomst med Microsoft 365-licenser

Åtkomst med Microsoft 365-licenser är som standard inaktiverat. Åtkomsten måste vara aktiverad för varje miljöoberoende, vilket ger administratörer kontroll och möjlighet till mellanlagrad lansering i hela organisationen. Du aktiverar åtkomst med [!INCLUDE [prod_short](includes/prod_short.md)] administrationscentret: 

1. Längst upp till höger, välj **Inställningar** ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") > **Administrationscenter**.  
2. I administratörscenter, välj  **miljöer**, välj sedan den miljö där du vill ändra licensåtkomst. 
3. På sidan **Miljöinformation**, välj **Ändra** för **Åtkomst med Microsoft 365 licenser** inställningarna.
4. I rutan **Microsoft 365 licenser** slå på strömbrytaren. 
5. Välj **Spara** när du är klar och acceptera bekräftelsen. Ändringen träder i kraft omedelbart.

## Välj vem som får åtkomst genom att använda säkerhetsgrupp

I Business Center administrationscenter kan en miljö kopplas till en eller flera säkerhetsgrupper för att kontrollera åtkomsten. Du kan tilldela en Azure Active Directory (Azure AD) grupp till miljön. Genom att tilldela en Azure AD-grupp till en miljö beviljas endast direkta och indirekta medlemmar i gruppen åtkomst till miljön. Indirekta medlemmar är användare i en annan grupp, som i sig är medlemmar i den grupp som är tilldelad till miljön. Även om alla licensierade användare i Azure AD kommer att läggas till i miljön när den synkroniseras med Microsoft 365 kan endast gruppmedlemmar logga in. Mer information finns i [Hantera åtkomst med hjälp av Azure Active Directory grupper ](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjälpen för utvecklare och IT-proffs.

## Distribuera Business Central-appen för Teams

För att [!INCLUDE [prod_short](includes/prod_short.md)]-licensinnehavare att dela data i Teams och för Microsoft 365-licensinnehavaren måste ha till gång till dessa data, måste var och en ha [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams installerad. Även om användare kan installera själva appen av sig, rekommenderas administratörer att använda centraliserad distribution. Centraliserad distribution gör att du kan lyfta upp appen till en bredare publik i organisationen och minimera enskilda användares ansträngningar. 

Information om hur du distribuerar [!INCLUDE [prod_short](includes/prod_short.md)]-appen för Teams finns i [Installera Business Central-appen genom att använda centraliserad distribution](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Om du kör centraliserad distribution innan och endast distribuerade appen till säkerhets gruppen för licensierade [!INCLUDE [prod_short](includes/prod_short.md)]-användare, måste du köra den igen för att distribuera till ytterligare grupper eller hela organisationen, beroende på hur du konfigurerar åtkomst.

> [!TIP]
> Letar du efter ett snabbare sätt att komma igång när du försöker med den här funktionen? Test användare kan installera appen vid [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## Testa din inställning

För att verifiera att din installation är redo för produktion hjälper följande steg dig att bygga upp förtroendet för att allt fungerar som det ska.

1. Skapa eller identifiera två test användare (A och B).

   - Test användare A måste ha en [!INCLUDE [prod_short](includes/prod_short.md)]-licens och Microsoft 365-licens för åtkomst till Teams.
   - Test användare B måste ha endast en Microsoft 365-licens med åtkomst till Teams.

2. Logga in på [!INCLUDE [prod_short](includes/prod_short.md)] webbklient som test användare A.

   1. Öppna en post som test användare B ska ha till gång till, t.ex. ett **artikel** kort i lämpligt företag och miljö.
   2. Välj **Dela** ![!Dela med andra appar åtgärder på sidor.](media/share-icon.png) > **Dela på Teams** om du vill öppna fönstret Dela till Teams.
   3. I fältet **Dela till**, lägg till testanvändare B som mottagare.
   4. Vänta tills länken har expanderats till ett kort och välj Dela.

3. Logga in Microsoft Teams som testanvändare B.

   1. Välj Chatt och öppna konversationen med testanvändare A.
   2. Välj knappen Detaljer på kortet i meddelandet som skickas av testanvändare A. Om [!INCLUDE [prod_short](includes/prod_short.md)]-klienten visas och är skrivskyddad, lyckades installationen.

> [!TIP]
> Något gick fel? Se [Felsöka åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md).

## Se även

[Översikt över Business Central-åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Felsöka åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md)  
[Business Central- och Microsoft Teams-integration](across-teams-overview.md)  

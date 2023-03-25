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

Administratörer måste slutföra flera aktiviteter innan de får åtkomst till Business Central med deras Microsoft 365-licens. Stegen nedan representerar den minsta inställning som krävs för att komma igång. Om du vill veta mer om åtkomst med Microsoft 365 licenser går du till [Business Central åtkomst med Microsoft 365 licenser](admin-access-with-m365-license.md).

## Distribuera appen Business Central för Teams

För att Business Central-licensinnehavare att dela data i Teams och Microsoft 365-licensinnehavaren måste ha till gång till dessa data, måste han/ hon ha Business Central-appen för Teams installerade. Även om användare kan installera själva appen av sig, rekommenderas administratörer att använda centraliserad distribution. Centraliserad distribution gör att du kan lyfta upp appen till en bredare publik i organisationen och minimera enskilda användares ansträngningar. 

Information om hur du distribuerar Business Central-appen för Teams finns i [installera Business Central-appen med hjälp av centraliserad distribution](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Om du kör centraliserad distribution innan och endast distribuerade appen till säkerhets gruppen för licensierade Business Central-användare, måste du köra den igen för att distribuera till ytterligare grupper eller hela organisationen, beroende på hur du konfigurerar åtkomst.

> [!TIP]
> Letar du efter ett snabbare sätt att komma igång när du försöker med den här funktionen? Testanvändare kan installera appen på [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## Konfigurera behörigheter

Business Central är säkert genom att designa och minimera risk genom att bevilja inga behörigheter till medföljande Microsoft 365-användare. Administratörer måste konfigurera objekt behörigheter som avgör vilka tabeller, sidor och rapporter som kan kommas åt i Teams med endast en Microsoft 365-licens. Dessa behörigheter är de start behörigheter som tilldelas när en användare loggar in för första gången med Microsoft 365-licens. 

Så här konfigurerar du startbehörigheter:

1. I Business Central söker du efter **licenskonfiguration**.
2. Välj Microsoft 365-licens.
3. Högst upp på **Microsoft 365**-licenssida, välj redigeringsikonen ![ikonen redigera](media/edit-pencil.png), aktivera **Anpassa behörigheter**. 
4. I avsnittet **Anpassade behörighetsuppsättningar** lägg till lämpliga behörighetsuppsättningar och välj om de är tillämpliga på ett enda företag eller alla företag inom miljön.

Med denna konfiguration kan användare med endast en Microsoft 365 licens läggs till i listan **användare** när de får åtkomst till Business Central första gången. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).

> [!NOTE]
> När du synkroniserar användarlistan i Business Central med användare i Microsoft 365, läggs endast användare med en Business Central-licens till i Business Central användarlista. Du kan tilldela en säkerhets grupp till miljön mer administrativ kontroll över behörigheter, användar grupper och profiler. När miljöer skyddas med hjälp av en säkerhetsgrupp och aktiverar åtkomst med Microsoft 365 licenser, kommer åtgärden **Uppdatera användare från Microsoft 365** på sidan **användare** även att innehålla användare som bara har en Microsoft 365 licens. Mer information om hur du skyddar miljöer finns i [ Hantera åtkomst med hjälp av Azure Active Directory grupper ](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjälpen för utvecklare och IT-proffs.

> [!TIP]
> Letar du efter ett snabbare sätt att komma igång när du försöker med den här funktionen eller utvärderingsföretag? Tilldela **D365 läs** behörighetsuppsättning, som ger behörighet till de flesta objekt.  

När du arbetar med flera miljöer måste licens konfigurationen tillämpas på varje miljö och kan vara olika i varje miljö. 

Mer information om [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md) och [Att komponera behörighetsuppsättningar](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## Slå på åtkomst med Microsoft 365-licenser

Åtkomst med Microsoft 365-licenser är som standard inaktiverat. Åtkomsten måste vara aktiverad för varje miljöoberoende, vilket ger administratörer kontroll och möjlighet till mellanlagrad lansering i hela organisationen. Du aktiverar åtkomst med administrationscentret för Business Central: 

1. Längst upp till höger, välj **Inställningar** ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") > **Administrationscenter**.  
2. I administratörscenter, välj  **miljöer**, välj sedan den miljö där du vill ändra licensåtkomst. 
3. På sidan **Miljöinformation**, välj **Ändra** för **Åtkomst med Microsoft 365 licenser** inställningarna.
4. I rutan **Microsoft 365 licenser** slå på strömbrytaren. 
5. Välj **Spara** när du är klar och acceptera bekräftelsen. Ändringen träder i kraft omedelbart.

## Testa din inställning

För att verifiera att din installation är redo för produktion hjälper följande steg dig att bygga upp förtroendet för att allt fungerar som det ska. 

1. Skapa eller identifiera två test användare (A och B).

   - Test användare A måste ha en Business Central-licens och Microsoft 365-licens för åtkomst till Teams.
   - Test användare B måste ha endast en Microsoft 365-licens med åtkomst till Teams.

2. Logga in på Business Central webbklient som test användare A.

   1. Öppna en post som test användare B ska ha till gång till, t.ex. ett **artikel** kort i lämpligt företag och miljö.
   2. Välj **Dela** ![!Dela med andra appar åtgärder på sidor.](media/share-icon.png) > **Dela på Teams** om du vill öppna fönstret Dela till Teams.
   3. I fältet **Dela till**, lägg till testanvändare B som mottagare. 
   4. Vänta tills länken har expanderats till ett kort och välj Dela. 

3. Logga in Microsoft Teams som testanvändare B.

   1. Välj Chatt och öppna konversationen med testanvändare A. 
   2. Välj knappen Detaljer på kortet i meddelandet som skickas av testanvändare A. Om Business Central-klienten visas och är skrivskyddad, lyckades installationen. 

> [!TIP]
> Något gick fel? Se [Felsöka åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md).

## Se även

[Översikt över Business Central-åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Felsöka åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-troubleshooting.md)  
[Business Central- och Microsoft Teams-integration](across-teams-overview.md)  

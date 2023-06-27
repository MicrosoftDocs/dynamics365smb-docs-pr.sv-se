---
title: Status för sekretessmeddelanden i Business Central
description: En översikt över statussidan för sekretessmeddelanden i Business Central
author: javariya
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: null
ms.search.form: 1565
audience: null
ms.author: a-jaaamir
ms.date: 07/21/2022
---

# <a name="privacy-notices-status-in-" />Status för sekretessmeddelanden i [!INCLUDE[prod_long](includes/prod_long.md)]

I den här artikeln beskrivs hur sekretess meddelandet är och förklarar syftet med sidan **Status för sekretessmeddelanden** i [!INCLUDE[prod_short](includes/prod_short.md)]. Du får också lära dig hur administratörer kan använda den här sidan.

## <a name="privacy-notice" />Sekretesspolicy

I sekretessmeddelandet anges datainsamling, databehandling och datasekretesspolicy, följt av organisationernas datastyrenhet. Det är ett dokument som beskriver vilka data som samlas in och för vilket ändamål, hur användarens data behandlas, hur de lagras och vem som ska kontaktas om en användare vill fråga något om deras data. 

## <a name="privacy-notices-status-page" />Sidan status för sekretessmeddelanden

I [!INCLUDE[prod_short](includes/prod_short.md)] om användare vill integrera data med Microsoft Exchange Microsoft OneDrive och Microsoft Teams måste acceptera sekretess meddelandet för varje entitet. Eller en administratör kan godkänna sekretessmeddelandena för deras räkning. Administratörer kan se statusen för sekretess meddelanden på sidan **status för sekretessmeddelanden**. Du hittar sidan **status för sekretessmeddelanden** i [!INCLUDE[prod_short](includes/prod_short.md)] genom att skriva namnet på sidan i sökfältet.  

På den sidan hittar du en tabell med godkännande alternativ för var och en av de tjänster som nämns ovan. 

| Kolumn | Description |
| ----------- | ----------- | 
| **Integrationsnamn** | Tjänstens namn, t.ex Microsoft OneDrive. |
| **Acceptera för alla** | En administratör godkänner sekretessmeddelandet för alla användare. |
| **Acceptera inte för alla** | En administratör godkänner inte sekretessmeddelandet för alla användare. |
| **Låt användarna bestämma** | Användare bestämmer sig för att godkänna sekretessmeddelandet för tjänsten eller inte. |

> [!NOTE]
> Du kan bara visa statusen för sekretess meddelanden på huvudsidan **status för sekretessmeddelanden**. För att redigera svaren, gå till **redigera listan** i åtgärdsfältet på sidan där alternativen nu är klickbara och inte nedtonade.

## <a name="privacy-notice-approvals" />Godkännanden för sekretessmeddelanden

Administratörer kan se enskilda godkännanden och hantera dem på undersidan för **godkännanden av sekretessmeddelanden**. Gå till fältet *Åtgärd* på sidan **Åtgärd för integritetsmeddelanden** under *Åtgärder* för att hitta alternativet *Visa enskilda godkännanden*. Det här alternativet leder till sidan **godkännanden av sekretessmeddelanden**.<br>

På den sidan hittar du en tabell med godkännande alternativ. 

| Kolumn | Description |
| ----------- | ----------- | 
| **Integrationsnamn** | Tjänstens namn, t.ex Microsoft OneDrive. |
| **Användarnamn** | Den användare som innehar det godkännandet. Om *organisationen* skrivs i kolumnen användarnamn hör godkännandet till hela organisationen. 
| **Acceptera** | Användaren godkänner sekretessmeddelandet. |
| **Acceptera inte** | Användaren godkänner inte sekretessmeddelandet. |
| **Godkännarens användarnamn** | Den som godkänner sekretessmeddelandet. |

## <a name="see-also" />Se även

[Regelefterlevnad – översikt](/dynamics365/business-central/compliance/compliance-overview)  
[Svara på begäranden om personuppgifter](/dynamics365/business-central/admin-responding-to-requests-about-personal-data)  
[Sekretesspolicy och användningsvillkor](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-checklist-i-privacypolicy-termsofuse)  
[Principer för datalagring](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/define-retention-policies) 

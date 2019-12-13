---
title: Business Central revisormiljö | Microsoft Docs
description: Läs mer om revisorportalen för Business Central och rollcentret för revisor som stöder interna och externa revisorer i kundföretaget.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896139"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Revisorupplevelse i Financials [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Oavsett vilken typ av revisor som du är kan du använda rollcentret **revisor** som din startsida i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Härifrån kan du komma åt alla sidor som behövs i arbetet.  

## <a name="accountant-role-center"></a>Rollcentret Revisor
Rollcentret är en instrumentpanel med aktivitetpaneler sida som visar nyckeltal i realtid och ger dig snabb åtkomst till data. På menyn längst upp på sidan har du tillgång till fler åtgärder, t ex öppna mest vanliga ekonomiska rapporter och rapporter i Excel. I navigeringsbalken högst upp kan du snabbt växla mellan de listor som du använder oftast. Här visas andra områden som exempelvis **bokförda dokument** med olika typer av dokument som har bokförts i företaget.  

Om du precis har börjat använda [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du köra videoförteckning direkt från ditt rollcenter. Du kan också starta en **komma igång** som pekar ut viktiga områden.  

## <a name="inviteaccountant"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]
Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till dina [!INCLUDE[d365fin](includes/d365fin_md.md)] så att de kan arbeta med dig med räkenskapsårets informationen.

När din revisorn har fått tillgång till din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de använda rollcenter **revisorn** som ger enkel åtkomst till de mest relevanta sidor för att kunna arbeta.  

Vi har gjort det lätt för dig att bjuda in en extern revisor. Öppna bara sidan **Användare** och välj åtgärden **Bjuda in extern revisor** i menyfliksområdet. Ett e-postmeddelande är redo för dig, lägg bara till din revisors e-postadress för arbete och skicka inbjudan.  
> [!Note]  
> Detta kräver att du har installerat SMTP-e-post. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).   

![Bjud in din revisor](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> Revisorns e-postadress måste vara en arbetsadress som baseras på ett Azure Active Directory. Om revisorn har en annan typ av e-post kan inte inbjudan skickas.  

### <a name="behind-the-scenes"></a>Bakom kulisserna
[!INCLUDE[d365fin](includes/d365fin_md.md)] omfattar tre licenser av typen extern revisor. Om ditt företag använder en extern revisor kan du ge åtkomst till din [!INCLUDE[d365fin](includes/d365fin_md.md)] genom att tilldela dem en sådan licens. Mer information om licenser finns i [Microsoft Dynamics 365 Busincess Central licensieringsguide](https://go.microsoft.com/fwlink/?LinkId=871590). 

Om din prenumeration fortfarande har en tillgänglig licens kan administratören eller partnern lägga till en extern användare via Azure Portal och tilldela användaren den externa revisorlicensen. Mer information finns i [lägga till Azure Active Directory B2B-samarbetsanvändare i Azure-portalen](/azure/active-directory/b2b/add-users-administrator).

Du kan sedan bjuda in revisorn från [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av uiden för assisterad konfiguration **Bjud in extern revisor**. Eftersom den här uppgiften kräver åtkomst för att hantera användare och licenser i Azure Active Directory, måste dock användaren som skickar den här inbjudan tilldelas rollen **global administratör** eller **användaradministratör** i Office 365 administrationscenter. Mer information finns i [Om administratörsroller](/office365/admin/add-users/about-admin-roles) i Office 365 administratörsinnehållet. 

## <a name="accountant-hub"></a>Accountant Hub
Om du är en revisor med flera klienter, använd [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] för en bättre överblick över dina kunder. Härifrån kan du komma åt varje klients klientorganisationen i [!INCLUDE[d365fin](includes/d365fin_md.md)] och använda den för tollcentret redovisare som beskrivs ovan. Mer information finns i [Välkommen till [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] är för närvarande i allmän förhandsgranskning på ett begränsat antal marknader.

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
redovisning[Redovisningen och kontoplanen](finance-general-ledger.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Analysera finansiella rapporter i Excel](finance-analyze-excel.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ställa in analys för kassaflöde](finance-setup-cash-flow-analyses.md)  
[Välkommen till [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub på Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  

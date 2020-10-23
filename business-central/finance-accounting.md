---
title: Revisorlösningar i Business Central
description: Läs mer om rollcentret Revisor och företagsnavet som stöder intern och extern revisor i kundföretaget.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5aaf2b72fc282eceabb6991345a2eac9508bdb13
ms.sourcegitcommit: aea079b66e35c447bf31a11ffc2069cfdaf2ef38
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "3970418"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Revisorupplevelse i Financials [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]

Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Oavsett vilken typ av revisor som du är kan du använda rollcentret **revisor** som din startsida i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Härifrån kan du komma åt alla sidor som behövs i arbetet.  

## <a name="accountant-role-center"></a>Rollcentret Revisor

Rollcentret är en instrumentpanel med aktivitetpaneler sida som visar nyckeltal i realtid och ger dig snabb åtkomst till data. På menyn längst upp på sidan har du tillgång till fler åtgärder, t ex öppna mest vanliga ekonomiska rapporter och rapporter i Excel. I navigeringsbalken högst upp kan du snabbt växla mellan de listor som du använder oftast. Här visas andra områden som exempelvis **bokförda dokument** med olika typer av dokument som har bokförts i företaget.  

Om du precis har börjat använda [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du köra videoförteckning direkt från ditt rollcenter. Du kan också starta en **komma igång** som pekar ut viktiga områden.  

## <a name="company-hub"></a>Företagsnav

Om du arbetar i flera [!INCLUDE [prodshort](includes/prodshort.md)]-företag kan det vara praktiskt att använda sidan **Företagsnav** för att hålla ordning på arbetet.  Mer information finns i [Hantera arbete över flera företag i företagsnavet](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]

Om du använder en extern revisor för att hantera böcker och redovisning kan din administratör bjuda in dem till ditt [!INCLUDE[d365fin](includes/d365fin_md.md)] så att de kan arbeta tillsammans med dig på räkenskapsårets data. [!INCLUDE[d365fin](includes/d365fin_md.md)] omfattar tre licenser av typen extern revisor. Mer information om licenser finns i [Licensieringsguiden för Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

När din revisorn har fått tillgång till din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de använda rollcenter **revisorn** som ger enkel åtkomst till de mest relevanta sidor för att kunna arbeta. De kan också använda företagsnavet i sitt eget [!INCLUDE [prodshort](includes/prodshort.md)] för att hantera sitt arbete. Mer information finns i [Hantera arbete över flera företag i företagsnavet](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Vi har gjort det lätt för dig att bjuda in en extern revisor. Öppna bara sidan **Användare** och välj åtgärden **Bjuda in extern revisor** i menyfliksområdet. Ett e-postmeddelande är redo för dig, lägg bara till din revisors e-postadress för arbete och skicka inbjudan.  

> [!Note]  
> Detta kräver att du har installerat SMTP-e-post. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).  

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Revisorns e-postadress måste vara en arbetsadress som baseras på ett Azure Active Directory. Om revisorn har en annan typ av e-post kan inte inbjudan skickas.
>
> För den här uppgiften krävs åtkomst till hantering av användare och licenser i Azure Active Directory. Användaren som skickar den här inbjudan måste tilldelas rollen **Global administratör** eller **Användaradministratör** i administratörscentret för Microsoft 365. Mer information finns i [Om administratörsroller](/microsoft-365/admin/add-users/about-admin-roles) i Microsoft 365 administratörsinnehållet.  

### <a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Lägga till din revisor i Microsoft 365 via Azure Portal

Om din administratör eller återförsäljarpartner inte vill använda guiden **Bjud in extern revisor** kan de lägga till en extern användare i Azure-portalen och tilldela denna användare licensen *Extern revisor*. Mer information finns i [Snabbstart: Lägg till gästanvändare i din katalog i Azure Portal](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Så här lägger du till din revisor som gästanvändare

1. Öppna [Azure Portal](https://portal.azure.com/).
2. Välj **Azure Active Directory** i rutan till vänster.
3. Under **Hantera** väljer du **Användare**.
4. Välj **Ny gästanvändare**.
5. På sidan **Ny användare** väljer du **Bjud in användare** och lägger sedan till information om din externa revisor.  

   Du kan också inkludera ett personligt välkomstmeddelande till revisorer för att låta dessa veta att du lägger till dem i ditt [!INCLUDE[prodshort](includes/prodshort.md)].

6. Välj **Bjud in** för att skicka inbjudan automatiskt. Ett meddelande visas uppe till höger med meddelandet **Användaren har bjudits in**. 
7. När du har skickat inbjudan läggs användarkontot automatiskt till i katalogen som en gäst.

Därefter måste du tilldela den nya gästanvändaren en licens till [!INCLUDE[prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>För att ge din revisor åtkomst till ditt [!INCLUDE[prodshort](includes/prodshort.md)]

1. I den Azure-portalen, på den nyligen tillagda användaren, väljer du **Profil** och sedan **Redigera**
2. Uppdatera fältet **Användningsplats** till det aktuella landet och välj sedan **Spara**.
3. Välj **Licenser** och öppna sedan **Tilldelningar**.
4. Välj licensen **Dynamics 365 Business Central för extern revisor**.  

    Om denna licens inte är tillgänglig måste du använda en tillgänglig **Dynamics 365 Business Central för IWS**-licens i stället.
5. Spara tilldelningen.

Om det lyckas tilldelas licensen till gästanvändaren och gästkontot skapas.

### <a name="importing-the-new-user-into-prodshort"></a>Importera den nya användaren till [!INCLUDE[prodshort](includes/prodshort.md)]

Revisorn får ett e-postmeddelande som meddelar dem att de har fått åtkomst till ditt Active Directory. Därefter måste du ge dem åtkomst till rätt företag i [!INCLUDE[prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Så här lägger du till revisorn till rätt företag

1. Öppna det [!INCLUDE[prodshort](includes/prodshort.md)]-företag som du vill ge revisorn åtkomst till på [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra"), ange **Användare** och välj sedan relaterad länk.  
3. Välj åtgärden **Skaffa nya användare från Office 365**.

Detta importerar användarkontot som du skapade i Azure-portalen till företaget. Mer information finns i [S¨här lägger du till en användare i Business Central](ui-how-users-permissions.md#adduser).  

Om du vill ge åtkomst till flera företag måste du logga in på respektive företag och upprepa den här processen. Du kan också uppdatera behörighetsgrupperna för revisorns användarprofil i [!INCLUDE[prodshort](includes/prodshort.md)], till exempel tilldela dem användargruppen *D365 Bus Premium*. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Analysera finansiella rapporter i Excel](finance-analyze-excel.md)  
[Hantera arbete i flera företag med företagsnavet](company-hub.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ställa in analys för kassaflöde](finance-setup-cash-flow-analyses.md)  

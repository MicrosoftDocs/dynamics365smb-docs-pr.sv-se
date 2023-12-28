---
title: Revisorlösningar i Business Central (innehåller video)
description: Läs mer om rollcentret Revisor och företagsnavet som stöder intern och extern revisor i kundföretaget.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 10/19/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# Revisorupplevelse i Financials [!INCLUDE[prod_long](includes/prod_long.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Oavsett vilken typ av revisor som du är kan du använda rollcentret **revisor** som din startsida i [!INCLUDE[prod_short](includes/prod_short.md)]. Härifrån kan du komma åt alla sidor som behövs i arbetet.  

## Rollcentret Revisor

Rollcentret är en instrumentpanel med aktivitetpaneler sida som visar nyckeltal i realtid och ger dig snabb åtkomst till data. På menyn längst upp på sidan har du tillgång till fler åtgärder, t ex öppna mest vanliga ekonomiska rapporter och rapporter i Excel. I navigeringsbalken högst upp kan du snabbt växla mellan de listor som du använder oftast. Här visas andra områden som exempelvis **bokförda dokument** med olika typer av dokument som har bokförts i företaget.  

Om du precis har börjat använda [!INCLUDE[prod_short](includes/prod_short.md)] kan du köra videoförteckning direkt från ditt rollcenter. Du kan också starta en **komma igång** som pekar ut viktiga områden.  

## Företagsnav

Om du arbetar i flera [!INCLUDE [prod_short](includes/prod_short.md)]-företag kan det vara praktiskt att använda sidan **Företagsnav** för att hålla ordning på arbetet.  Mer information finns i [Hantera arbete över flera företag i företagsnavet](company-hub.md).  

## <a name="inviteaccountant"></a>Bjud in din externa revisorn till [!INCLUDE[prod_short](includes/prod_short.md)]

Om du använder en extern revisor för att hantera böcker och redovisning kan din administratör bjuda in dem till ditt [!INCLUDE[prod_short](includes/prod_short.md)] så att de kan arbeta tillsammans med dig på räkenskapsårets data. [!INCLUDE[prod_short](includes/prod_short.md)] omfattar tre licenser av typen extern revisor. För information om licenser, ladda ned [Licensieringsguiden för Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=866544).

När din revisorn har fått tillgång till din [!INCLUDE[prod_short](includes/prod_short.md)], kan de använda rollcenter **revisorn** som ger enkel åtkomst till de mest relevanta sidor för att kunna arbeta. De kan också använda företagsnavet i sitt eget [!INCLUDE [prod_short](includes/prod_short.md)] för att hantera sitt arbete. Mer information finns i [Hantera arbete över flera företag i företagsnavet](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Vi har gjort det lätt för dig att bjuda in en extern revisor. Öppna bara sidan **Användare** och välj åtgärden **Bjuda in extern revisor** i menyfliksområdet. Ett e-postmeddelande är redo för dig, lägg bara till din revisors e-postadress för arbete och skicka inbjudan.  

> [!Note]  
> Detta kräver att du har installerat SMTP-e-post. Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Revisorns e-postadress måste vara en arbetsadress som baseras på ett Microsoft Entra ID. Om revisorn har en annan typ av e-post kan inte inbjudan skickas.
>
> För den här uppgiften krävs åtkomst till hantering av användare och licenser i Microsoft Entra ID. Användaren som skickar den här inbjudan måste tilldelas rollen **Global administratör** eller **Användaradministratör** i administratörscentret för Microsoft 365. Mer information finns i [Om administratörsroller](/microsoft-365/admin/add-users/about-admin-roles) i Microsoft 365-administratörsinnehållet.  

### Lägga till din revisor i Microsoft 365 i Azure Portal

Om din administratör eller återförsäljarpartner inte vill använda guiden **Bjud in extern revisor** kan de lägga till en extern användare i Azure-portalen och tilldela denna användare licensen *Extern revisor*. Mer information finns i [Snabbstart: Lägg till gästanvändare i din katalog i Azure Portal](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### Så här lägger du till din revisor som gästanvändare

1. Öppna [Azure Portal](https://portal.azure.com/).
2. I rutan till vänster väljer du **Microsoft Entra ID**.
3. Under **Hantera** väljer du **Användare**.
4. Välj **Ny gästanvändare**.
5. På sidan **Ny användare** väljer du **Bjud in användare** och lägger sedan till information om din externa revisor.  

   Du kan också inkludera ett personligt välkomstmeddelande till revisorer för att låta dessa veta att du lägger till dem i ditt [!INCLUDE[prod_short](includes/prod_short.md)].

6. Välj **Bjud in** för att skicka inbjudan automatiskt. Ett meddelande visas uppe till höger med meddelandet **Användaren har bjudits in**. 
7. När du har skickat inbjudan läggs användarkontot automatiskt till i katalogen som en gäst.

Därefter måste du tilldela den nya gästanvändaren en licens till [!INCLUDE[prod_short](includes/prod_short.md)].

#### För att ge din revisor åtkomst till ditt [!INCLUDE[prod_short](includes/prod_short.md)]

1. I den Azure-portalen, på den nyligen tillagda användaren, väljer du **Profil** och sedan **Redigera**
2. Uppdatera fältet **Användningsplats** till aktuella landet/regionen och välj sedan **Spara**.
3. Välj **Licenser** och öppna sedan **Tilldelningar**.
4. Välj licensen **Dynamics 365 Business Central för extern revisor**.  
    
    Om licensen inte är tillgänglig kontaktar du återförsäljningspartnern och lägger till licensen i prenumerationen.

    Specifikt för utvärderingssyfte i en testklientorganisation kan du istället använda en tillgänglig **Dynamics 365 Business Central för IWs**-licens. Du kan emellertid inte använda den här typen av licens om du redan har köpt [!INCLUDE[prod_short](includes/prod_short.md)]. 
5. Spara tilldelningen.

Om det lyckas tilldelas licensen till gästanvändaren och gästkontot skapas.

### Importera den nya användaren till [!INCLUDE[prod_short](includes/prod_short.md)]

Revisorn får ett e-postmeddelande som meddelar denne om att han/hon har fått åtkomst till ditt Microsoft Entra ID. Därefter måste du ge dem åtkomst till rätt företag i [!INCLUDE[prod_short](includes/prod_short.md)].

#### Så här lägger du till revisorn till rätt företag

1. Öppna det [!INCLUDE[prod_short](includes/prod_short.md)]-företag som du vill ge revisorn åtkomst till på [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **användare** och väljer sedan relaterad länk.  
3. Välj åtgärden **Hämta nya användare från Microsoft 365**.

Detta importerar användarkontot som du skapade i Azure-portalen till företaget. Mer information finns i [S¨här lägger du till en användare i Business Central](ui-how-users-permissions.md#adduser).  

Om du vill ge åtkomst till flera företag måste du logga in på respektive företag och upprepa den här processen. Du kan också uppdatera behörighetsgrupperna för revisorns användarprofil i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel tilldela dem användargruppen *D365 Bus Premium*. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).  

## Se även

[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Huvudbok och kontolista](finance-general-ledger.md)  
[Avsluta år och perioder](year-close-years-periods.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Analysera finansiella rapporter i Excel](finance-analyze-excel.md)  
[Hantera arbete i flera företag med företagsnavet](company-hub.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ställa in analys för kassaflöde](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
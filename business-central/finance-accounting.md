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
ms.date: 05/02/2019
ms.author: edupont
ms.openlocfilehash: f088e1319684b9a18a2b0c8ab5305f73747f6889
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446928"
---
# <a name="accountant-experiences-in-included365finlongincludesd365finlongmdmd"></a>Revisorupplevelse i Financials [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Alla företag måste göra sin redovisning och godkänna redovisningen. Vissa företag använder en extern revisor och andra har en revisor bland personalen. Oavsett vilken typ av revisor som du är kan du använda rollcentret **revisor** som din startsida i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Härifrån kan du komma åt alla sidor som behövs i arbetet.  

## <a name="accountant-role-center"></a>Rollcentret Revisor
Rollcentret är en instrumentpanel med aktivitetpaneler sida som visar nyckeltal i realtid och ger dig snabb åtkomst till data. På menyn längst upp på sidan har du tillgång till fler åtgärder, t ex öppna mest vanliga ekonomiska rapporter och rapporter i Excel. I navigeringsbalken högst upp kan du snabbt växla mellan de listor som du använder oftast. Här visas andra områden som exempelvis **bokförda dokument** med olika typer av dokument som har bokförts i företaget.  

Om du precis har börjat använda [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du köra videoförteckning direkt från ditt rollcenter. Du kan också starta en **komma igång** som pekar ut viktiga områden.  

## <a name="accountant-hub"></a>Accountant Hub
Om du är en revisor med flera klienter, använd [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] för en bättre överblick över dina kunder. Härifrån kan du komma åt varje klients klientorganisationen i [!INCLUDE[d365fin](includes/d365fin_md.md)] och använda den för tollcentret redovisare som beskrivs ovan. Mer information finns i [Välkommen till [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]
Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till dina [!INCLUDE[d365fin](includes/d365fin_md.md)] så att de kan arbeta med dig med räkenskapsårets informationen.

När din revisorn har fått tillgång till din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de använda rollcenter **revisorn** som ger enkel åtkomst till de mest relevanta sidor för att kunna arbeta.  

Vi har gjort det lätt för dig att bjuda in en extern revisor. Öppna bara sidan **Användare** och välj åtgärden **Bjuda in extern revisor** i menyfliksområdet. Ett e-postmeddelande är redo för dig, lägg bara till din revisors e-postadress för arbete och skicka inbjudan.  

![Bjud in din revisor](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Detta kräver att du har installerat SMTP-e-post. Du kan göra det själv eller fråga din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner. Dessutom måste du vara inloggad i [!INCLUDE[d365fin](includes/d365fin_md.md)] som en användaradministratör och inte som ansvarig chef eller andra användare. Slutligen kan ha du lämnat testföretaget så att du får en Azure Active Directory-administratör.  

> [!IMPORTANT]  
> Revisorns e-postadress måste vara en arbetsadress som baseras på ett Azure Active Directory. Om revisorn har en annan typ av e-post kan inte inbjudan skickas.  

### <a name="separate-license"></a>Separera licens
I bakgrunden läggs revisorn till i din Active Directory-innehavare. Administratören kan verifiera att revisorn har accepterat din inbjudan och tilldelas rätt licens. Stegen för att göra detta beror på vilken typ av konto som du använde när du registrerade dig för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här avsnittet baseras på användning av ett Office 365-konto som använder Microsoft Azure Active Directory.  

Om du har aktiverat prenumerationen av [!INCLUDE[d365fin](includes/d365fin_md.md)] och är inte längre med utvärderingen företaget kan du har en Azure Active Directory för klientorganisation. Administratören eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner hanterar den här klientorganisationen i [Azure portal](https://portal.azure.com). Det är där nya användare läggs till och licenser används och tas bort. Mer information finns i [Microsoft Azure portalöversikten](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

En av licenstyperna för [!INCLUDE[d365fin](includes/d365fin_md.md)] är licens *externa revisorn*. Den här typen av licens är avsedd att användas av användare, till exempel externa revisorer. Detta innebär att du inte behöver köpa ett extra säte i den aktuella Active Directory eller använda en av dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-konton på en extern revisor. Om din aktuella prenumeration i Office 365 omfattar 10 användare för exempelvis [!INCLUDE[d365fin](includes/d365fin_md.md)], och du använder 10 *fullständiga användare*-licenser kan din administratör bara lägga till en extern revisor som gästanvändare i Azure portalen och tilldela användaren licensen *extern revisor* utan extra kostnad. Du kan dock endast ha en användare med licensen *extern revisor*. Om du vill lägga till fler användare, måste du uppdatera prenumerationen på Office 365 i enlighet med detta.

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
[Dynamics 365 - Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
